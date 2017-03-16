---
title: Point and Vector Methods
description: This guide provides an overview of the RhinoScriptSytntax Point and Vector methods.
authors: ['Dale Fugier']
author_contacts: ['dale']
apis: ['RhinoPython']
languages: ['Python']
platforms: ['Mac', 'Windows']
categories: ['Python in Rhino']
origin:
order: 97
keywords: ['script', 'Rhino', 'python']
layout: toc-guide-page
---

## Point  & Vector Methods

The following methods are available for creating and manipulating 3-D points and 3-D vectors.  3-D points and 3-D vectors are represented as  zero-based, one-dimensional arrays that contain three numbers. For more information, see the [Points]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-points) and [Vectors]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-vectors) discussion in [RhinoScript Fundamentals]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-introduction).

| Method                                   |      |      | Description                              |
| :--------------------------------------- | :--: | :--: | :--------------------------------------- |
| [IsVectorParallelTo]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-IsVectorParallelTo) |      |      | Compares two vectors to see if they are parallel. |
| [IsVectorPerpendicularTo]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-IsVectorPerpendicularTo) |      |      | Compares two vectors to see if they are perpendicular. |
| [IsVectorTiny]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-IsVectorTiny)                             |      |      | Verifies a vector is tiny.               |
| [IsVectorZero]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-IsVectorZero)                             |      |      | Verifies a vector is zero.               |
| [PointAdd]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointAdd)                                 |      |      | Adds a point or a vector to a point.     |
| [PointArrayBoundingBox]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointArrayBoundingBox)                    |      |      | Returns the bounding box of an array of 3-D points. |
| [PointArrayClosestPoint]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointArrayClosestPoint)                   |      |      | Finds the point in an array of 3-D points that is closest to a test point |
| [PointArrayTransform]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointArrayTransform)                      |      |      | Transforms an array of 3-D points.       |
| [PointClosestObject]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointClosestObject)                       |      |      | Finds the object that is closest to a test point. |
| [PointCompare]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointCompare)                             |      |      | Compares two points.                     |
| [PointDivide]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointDivide)                              |      |      | Divides a point by a value.              |
| [PointsAreCoplanar]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointsAreCoplanar)                        |      |      | Verifies that a list of 3-D points are coplanar. |
| [PointScale]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointScale)                               |      |      | Scales a point by a value.               |
| [PointSubtract]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointSubtract)                            |      |      | Subtracts a point or a vector from a point. |
| [PointTransform]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PointTransform)                           |      |      | Transforms a point.                      |
| [ProjectPointToMesh]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-ProjectPointToMesh)                       |      |      | Projects one or more points onto one or more meshes. |
| [ProjectPointToSurface]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-ProjectPointToSurface)                    |      |      | Projects one or more points onto one or more surfaces |
| [PullPoints]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-PullPoints)                               |      |      | Pulls points to a surface or a mesh object. |
| [VectorAdd]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorAdd)                                |      |      | Adds two vectors.                        |
| [VectorAngle]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorAngle)                              |      |      | Returns the angle between two 3-D vectors. |
| [VectorCompare]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorCompare)                           |      |      | Compares two vectors.                    |
| [VectorCreate]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorCreate)                            |      |      | Create a vector from two 3-D points.     |
| [VectorCrossProduct]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorCrossProduct)                       |      |      | Returns the cross product of two vectors. |
| [VectorDivide]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorDivide)                             |      |      | Divides a vector.                        |
| [VectorDotProduct]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorDotProduct)                         |      |      | Returns the dot product of two vectors.  |
| [VectorLength]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorLength)                             |      |      | Returns the length of a vector.          |
| [VectorMultiply]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorMultiply)                           |      |      | Multiplies two vectors.                  |
| [VectorReverse]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorReverse)                            |      |      | Reverses a vector.                       |
| [VectorRotate]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorRotate)                             |      |      | Rotates a vector.                        |
| [VectorScale]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorScale)                              |      |      | Scales a vector.                         |
| [VectorSubtract]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorSubtract)                           |      |      | Subtracts two vectors.                   |
| [VectorTransform]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorTransform)                          |      |      | Transforms a vector.                     |
| [VectorUnitize]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#pointvector-VectorUnitize)                            |      |      | Unitizes, or normalizes, a vector.       |
|=====
|
{: rules="groups"}

---

## Related Topics

- [What is RhinoScriptSyntax and RhinoScript?]({{ site.baseurl }}/guides/rhinopython/what-are-python-rhinoscript)
- [Python List of Points]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-list-points)
- [Python Vectors]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-vectors)
- [Python Lines]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-lines)
- [Python Planes]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-planes)
- [Python Objects]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-objects)
- [RhinoScript Points and Vectors Methods]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-point-vector-methods)
