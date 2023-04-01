# Object Oriented Modeling - Graphic Editor
Step-wise procedure to translate a problem statement into class diagram
## Problem Statement
*"Develop a graphic editor that can draw different geometric shapes such as line, circle and triangle. User can select, move or rotate a shape. To do so, editor provides user with a menu listing different commands. Individual shapes can be grouped together and can behave as a single shape."* 

---
### Step 1). Identify Classes
Extract nouns in the problem statement. # ask myself how to do that?

Develop a graphic **editor** that can draw different geometric **shapes** such as **line**, **circle** and **triangle**. **User** can select, move or rotate a **shape**. To do so, **editor** provides **user** with a **menu** listing different **commands**. Individual **shapes** can be grouped together and can behave as a single **shape**. 

Eliminate irrelevant classes.
* Editor - Very broad scope
* User – Out of system boundary
* commands – Broad scope

Add more classes by analyzing requirements
* Group - required to behave as a shape
  * Individual shapes can be grouped together and can behave as a single shape
* View – editor must have a display area

Following classes have been identified:
* Shape
* Line
* Circle
* Triangle
* Menu
* **Group**
* **View**
### Basic Object Model - Graphic Editor
![initial](https://user-images.githubusercontent.com/41892175/45860923-6614ff00-bd9c-11e8-87fb-530b0b6dc907.jpg)

---
### Step 2). Identify Associations
Extract verbs connecting objects.

**"Individual shapes can be grouped together"**
* Group consists of lines, circles, triangles
* Group can also consists of other groups

(Composition)

Verify access paths.

**View contains shapes**
* View contains lines
* View contains circles
* View contains triangles
* View contains groups

(Aggregation)

**Menu sends message to View**

(Simple One-Way Association)
### Basic Object Model - Graphic Editor
![45861910-dbcf9980-bda1-11e8-9004-d37512a6f1fe](https://user-images.githubusercontent.com/41892175/45867325-c8c6c480-bdb5-11e8-9e97-c83869ab384d.jpg)

---
### Step 3). Identify Attributes
Extract properties of the object from the domain knowledge.
* **Shape**
  * Color
  * Vertices
* **Line**
  * Color
  * Vertices
  * Length
* **Circle**
  * Color
  * Vertices
  * Radius
* **Triangle**
  * Color
  * Vertices
  * Angle
* **Menu**
  * Name
  * isOpen
* **Group**
  * noOfObjects
* **View**
  * noOfObjects
  * selected
### Basic Object Model - Graphic Editor
![initial](https://user-images.githubusercontent.com/41892175/45867370-e7c55680-bdb5-11e8-8a42-be5fcbee820b.jpg)

---
### Step 4). Identify Operations
Extract verbs connected with an object.

**Develop** a graphic editor that can **draw** different geometric shapes such as line, circle and triangle. User can **select**, **move** or **rotate** a shape. To do so, editor **provides** user with a menu listing different commands. Individual shapes can be **grouped** together and can **behave** as a single shape.

Eliminate irrelevant operations.
* Develop - out of system boundary
* Provides - have broad semantics
* Behave – broad semantics

Following are selected operations:
* **Shape**
  * Draw
  * Select
  * Move
  * Rotate
* **Line**
  * Draw
  * Select
  * Move
  * Rotate
* **Circle**
  * Draw
  * Select
  * Move
  * Rotate
* **Triangle**
  * Draw
  * Select
  * Move
  * Rotate
* **Menu**
  * Open
  * Select
  * Move
  * Rotate
* **Group**
  * Draw
  * Select
  * Move
  * Rotate

Extract operations using domain knowledge
* **View**
  * Add
  * Remove
  * Group
  * Show
### Basic Object Model - Graphic Editor
![initial](https://user-images.githubusercontent.com/41892175/45868828-5657e380-bdb9-11e8-8a65-c63c00f45aec.jpg)

---
### Step 5). Identify Inheritance
Search “is a kind of” by looking at keywords like “such as”, “for example”, etc

**"…shapes such as line, circle and triangle…"**
   * Line, Circle and Triangle inherits from Shape

By analyzing requiremens

**"Individual shapes can be grouped together and can behave as a single shape"**
   * Group inherits from Shape
### Refined Object Model - Graphic Editor
![initial](https://user-images.githubusercontent.com/41892175/45870172-d895d700-bdbc-11e8-86c9-048304dd22a2.jpg)
