# Domain Modeling
Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

# Tables
A table represents information in a grid format. When representing information in a table, you need to think in terms of a grid made up of rows and columns (a bit like a
spreadsheet).

## Basic Table Structure
### 1. ```<table>```
The ```<table>``` element is used
to create a table. The contents
of the table are written out row
by row.
### 2. ```<tr>```
You indicate the start of each
row using the opening ```<tr>``` tag.
(The tr stands for table row.)
It is followed by one or more
```<td>``` elements (one for each cell
in that row).
At the end of the row you use a
closing ``</tr>`` tag.
### 3. ```<td>```
Each cell of a table is
represented using a ```<td>```
element. (The td stands for
table data.)
At the end of each cell you use a
closing ```</td>``` tag.
### 4. ```<th>```
The ```<th>``` element is used just
like the ```<td>``` element but its
purpose is to represent the
heading for either a column or
a row. (The th stands for table
heading.)
Even if a cell has no content,
you should still use a ```<td>``` or
```<th>``` element to represent
the presence of an empty cell
otherwise the table will not
render correctly. (The first cell
in the first row of this example
shows an empty cell.)
Using ```<th>``` elements for
headings helps people who
use screen readers, improves
the ability for search engines
to index your pages, and also
enables you to control the
appearance of tables better
when you start to use CSS.

### Example
```<table>
 <tr>
 <th></th>
 <th scope="col">Saturday</th>
 <th scope="col">Sunday</th>
 </tr>
 <tr>
 <th scope="row">Tickets sold:</th>
 <td>120</td>
 <td>135</td>
 </tr>
 <tr>
 <th scope="row">Total sales:</th>
 <td>$600</td>
 <td>$675</td>
 </tr>
</table>
```

# Functions, Methods, and Objects

## The this Keyword
In a function definition, ```this``` refers to the "owner" of the function.

In the example below, this is the person object that "owns" the fullName function.

In other words, ```this.firstName``` means the firstName property of this object.

Read more about the this keyword at JS this Keyword.

### Example

```const person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
```

## Accessing Object Methods
You access an object method with the following syntax:

```objectName.methodName()```

You will typically describe fullName() as a method of the person object, and fullName as a property.
### 
The fullName property will execute (as a function) when it is invoked with ().

### Adding a Method to an Object
Adding a new method to an object is easy:
###
```person.name = function () {
  return this.firstName + " " + this.lastName;
};```