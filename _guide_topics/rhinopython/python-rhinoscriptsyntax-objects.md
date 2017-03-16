---
title: Rhino objects in Python
description: This guide provides an overview of a RhinoScriptSytntax Object Geometry in Python.
authors: ['Dale Fugier']
author_contacts: ['dale']
apis: ['RhinoPython']
languages: ['Python']
platforms: ['Mac', 'Windows']
categories: ['Python in Rhino']
origin:
order: 6
keywords: ['script', 'Rhino', 'python']
layout: toc-guide-page
---

## Objects

Rhino can create and manipulate a number of geometric objects, including points, point clouds, curves, surfaces, B-reps, meshes, lights, annotations, and references.   Any geometry object that exists in Rhino's document database is assigned an object identifier. Each object in the Rhino document is identified by a [globally unique identifier (GUID)](https://en.wikipedia.org/wiki/Universally_unique_identifier), that is generated and assigned to objects when they are created.  The [Guid's object]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-objects) is something that can be drawn, belongs to a layer, is saved to a Rhino file and is counted as a Rhino object. Because identifiers are saved in the 3DM file, an object's identifier will be the same between editing sessions.

To view an object's unique identifier, use Rhino's Properties command.

A GUID is a series of numbers, but for convenience RhinoScriptSyntax can viewed the GUID in the form of a string.  An object's identifier looks something like the following:

F6E01514-3264-4598-8A07-A58BFE739C38

The majority of RhinoScriptSyntax's object manipulation methods require one or more object identifiers to be acquired before the method can be executed.

## Rhino Geometry and Attributes

Rhino objects consist of two components: the object's geometry and the object's attributes.

The types of geometry support by Rhino include points, point clouds, curves, surfaces, polysurfaces, extrusions, meshes, annotations and dimensions, and other.

The attributes of an object include such properties as object color, layer, linetype, render material, group membership, and more.

In RhinoScriptSyntax there is a series of functions to add geometry and the necessary attributes to create a Rhino object.  Once the geomtry, attributes are added to the document, the GUID is added to identify the set of information. 

### Example

Here is an example using Object IDs to work reference geometry:

```python
import rhinoscriptsyntax as rs

startPoint = [1.0, 2.0, 0.0]
endPoint = [4.0, 5.0, 0.0]
line1 = [startPoint, endPoint]

line1ID = rs.AddLine(line1[0],line1[1]) # Adds a line to the Rhino Document and returns an ObjectID

startPoint2 = [1.0, 4.0, 0.0]
endPoint2 = [4.0, 2.0, 0.0]
line2 = [startPoint2, endPoint2]

line2ID = rs.AddLine(line2[0],line2[1]) # Returns another ObjectID

int1 = rs.LineLineIntersection(line1ID,line2ID) # passing the ObjectIDs to the function.
```

## Using Guids

Most of the time Guids can be used directly in RhinoScriptSyntax functions.

```python
import rhinoscriptsyntax as rs

obj = rs.GetObject("Select object to rotate") #Returns a GUID
if obj:
    point = rs.GetPoint("Center point of rotation")
    if point: 
      rs.RotateObject(obj, point, 45.0, None, copy=True) # Pass the Guid directly into function
```

Sometimes it is necessary to convert a Guid to a string.  Common reasons for this might be passing the GUID to the Rhino command line or generating a GUID string to store in a simple file format. Guids have a `.ToString()` method.

```python
import rhinoscriptsyntax as rs
obj = rs.GetObject("Select object to rotate") #Returns a GUID
GuidString = id.ToString()
```

The `rs.Command()` function is commonly used with GUID strings.  The command line takes strings.  Formatting existing object identifiers from a Guid to a string is required.  In
Python, this can be done through the [automatic string formatting '{}']({{ site.baseurl }}/guides/rhinopython/python-datatypes/#string) syntax as follows:

```python
import rhinoscriptsyntax as rs

  obj = rs.GetObject("select object")
  rs.Command("_move selid {} enter 0,0,0 0,0,1".format(obj))
```
The `selid` command will take a GUID and select the object with that identifier.  The `{}` is replaced with a string version of the GUID value in the variable `obj`.



## Related Topics

- [What is Python and RhinoScript?]({{ site.baseurl }}/guides/rhinopython/what-are-python-rhinoscript)
- [Points]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-points)
- [Vectors]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-vectors)
- [Lines]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-lines)
- [Planes]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-planes)
- [Rhino NURBs Geometry]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-nurbs)
