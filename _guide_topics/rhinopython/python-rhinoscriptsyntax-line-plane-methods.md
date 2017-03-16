---
title: Line and Plane Methods
description: This guide provides an overview of the rhinoscriptsytntax Line and Plane methods.
authors: ['Dale Fugier']
author_contacts: ['dale']
apis: ['RhinoPython']
languages: ['Python']
platforms: ['Mac', 'Windows']
categories: ['Python in Rhino']
origin:
order: 98
keywords: ['script', 'Rhino', 'python']
layout: toc-guide-page
---
 
## Line and Plane Methods

The following methods are available for creating and manipulating lines and planes.

Lines are represented as zero-based, one-dimensional arrays containing two elements: the start point (3-D point) and the end point (3-D point).

Planes are represented as zero-based, one-dimensional arrays containing four elements: the plane's origin (3-D point), the plane's x-axis direction (3-D vector), the plane's y-axis direction (3-D vector), and the plane's z-axis direction (3-D vector).

For more information in [RhinoScript Fundamentals]({{ site.baseurl }}/guides/rhinopython/python-rhinoscriptsyntax-introduction).

| Method | | |  Description |
|:--------|:-:|:-:|:--------|
| [DistanceToPlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-DistanceToPlane) | | | | Returns the distance from a plane to a point. |
| [EvaluatePlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-EvaluatePlane) | | | | Evaluates a point on a plane. |
| [IntersectPlanes]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-IntersectPlanes) | | | | Returns the point calculated by intersecting three planes. |
| [LineCylinderIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineCylinderIntersection) | | | | Calculates the intersection of a line and a cylinder. |
| [LineIsFartherThan]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineIsFartherThan) | | | | Determines if the shortest distance from a line to a point or another line is greater than a specified distance. |
| [LineLineIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineLineIntersection) | | | | Returns the point calculated by intersecting two lines. |
| [LineMaxDistanceTo]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineMaxDistanceTo) | | | | Finds the longest distance between the line, as a finite chord, and a point or another line. |
| [LinePlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LinePlane) | | | | Returns a plane that contains the line. |
| [LinePlaneIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LinePlaneIntersection) | | | | Returns the point calculated by intersecting a line with a plane. |
| [LineSphereIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineSphereIntersection) | | | | Calculates the intersection of a line and a sphere. |
| [LineTransform]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#line-LineTransform) | | | | Transforms a line. |
| [MovePlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-MovePlane) | | | | Moves the origin of a plane. |
| [PlaneClosestPoint]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneClosestPoint) | | | | Returns the closest point on a plane from a point. |
| [PlaneCurveIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneCurveIntersection) | | | | Intersects an infinite plane and a curve object. |
| [PlaneEquation]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneEquation) | | | | Returns the equation of a plane. |
| [PlaneFitFromPoints]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneFitFromPoints) | | | | Returns a plane through an array of points. |
| [PlaneFromFrame]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneFromFrame) | | | | Creates a plane from an origin point, X axis direction, and Y axis direction. |
| [PlaneFromNormal]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneFromNormal) | | | | Creates a plane from an origin point, and a normal direction. |
| [PlaneFromPoints]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneFromPoints) | | | | Creates a plane from three non-colinear points. |
| [PlanePlaneIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlanePlaneIntersection) | | | | Returns the line calculated by intersecting two planes. |
| [PlaneSphereIntersection]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneSphereIntersection) | | | | Calculates the intersection of a plane and a sphere. |
| [PlaneTransform]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-PlaneTransform) | | | | Transforms a plane. |
| [RotatePlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-RotatePlane) | | | | Rotates a plane. |
| [WorldXYPlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-WorldXYPlane) | | | | Returns Rhino's world XY plane. |
| [WorldYZPlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-WorldYZPlane) | | | | Returns Rhino's world YZ plane. |
| [WorldZXPlane]({{ site.baseurl }}/api/RhinoScriptSyntax/win/#plane-WorldZXPlane) | | | | Returns Rhino's world ZX plane. |
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
