---
title: List of Points in Python
description: This guide provides an overview of a rhinoscriptsyntax list of Point Geometry in Python.
authors: ['Dale Fugier']
author_contacts: ['dale']
apis: ['RhinoPython']
languages: ['Python']
platforms: ['Mac', 'Windows']
categories: ['Python in Rhino']
origin:
order: 3
keywords: ['script', 'Rhino', 'python']
layout: toc-guide-page
---

## Lists of Points

Many rhinoscriptsyntax functions require a [list]({{ site.baseurl }}/guides/rhinopython/python-datatypes/#list) of  [points]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-points) as an argument or return. For example the 'DivideCurve()' function will return a list of points:

```python
import rhinoscriptsyntax as rs

obj = rs.GetObject("Select a curve")

if obj:
    points = rs.DivideCurve(obj, 4)
    
print(points)
```

There are a number of ways to access the information in these lists.

Use an index to access any one of the points:

```python
print(points[0]) # Returns the first point.
```

With Python, it is easy to walk through the list with a `for` loop  and print out the coordinates for each point,

```python
for i in points:
    print i
```

It is also possible to use nested indexes to access a specific coordinate of a point in the list.  This example will access the Y coordinate of the second point in the list:


```python
print(points[1][1])
```

Using the .Y property on the [point]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-points) also would work:

```python
print(points[1].Y)
```

To add a point to this list, create the point with `CreatePoint()`, then [append](https://docs.python.org/2/tutorial/datastructures.html) it to the list:

```python
points.append(rs.CreatePoint(1.0, 2.0, 3.0))

for i in points:
    print i
```

---

## Related Topics

- [What is Python and RhinoScript?]({{ site.baseurl }}/guides/rhinopython/what-are-python-rhinoscript)
- [Python Points]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-points)
- [Python Vectors]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-vectors)
- [Python Lines]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-lines)
- [Python Planes]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-planes)
- [Python Objects]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-objects)
