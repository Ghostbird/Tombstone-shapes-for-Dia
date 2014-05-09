_This manual and the referenced Dia shapes, their icons (.png) and the .sheet file are released by the author into the public domain by means of the CC0 1.0 License_

![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)

To the extent possible under law, the person who associated CC0 with this work has waived all copyright and related or neighboring rights to this work. This work is published from: Netherlands.

#Tombstone Diagrams for Dia

Add four new shapes to Dia to allow easy construction of tombstone diagrams for compiler bootstrapping.

##Installation

Extract the folders _shapes_ and _sheets_ into your local or system-wide dia application folder. The latter may require elevated privileges (_root_ or _Administrator_ access).

###GNU/Linux

Extract into ~/.dia/ for your own use.

With root privileges, extract into /usr/share/dia for a system wide installation.

###Other systems

Look for the dia installation directory or the dia application data.

##Usage

###Placing and connecting the shapes

Click one of the four icons and then click in your diagram. A standard sized version of the shape will be created. Dia does not support connecting shapes directly. The standard size has taken this into account, and when you enable grid snapping (default 1cm grid size) in Dia, you can snap your shapes to the grid, and they will fit neatly together, even though they are not really connected as far as Dia is concerned.

###Text in the shapes
Dia shapes allow only one integrated textbox, this textbox activates by default as soon as you place the object. If you want to edit the text later, you can select the object and press the `<ENTER>` key. This will re-enable the textbox.

For the _machine_ shape, this is sufficient.

For the other shapes, you'll need to manually add extra text fields. The shapes have specific internal connection points to facilitate this.

To add a text field, click the text-cursor icon in the dia tool-bar or press `<F2>`. Then click in the shape __and drag__ the cursor to one of the connection points. Release the mouse button when the connection point is highlighted. When done correctly the text field is now connected to the shape, and will move with it. Next type the text, note that it is by default left aligned to the connection point. When you have entered your text, click outside the text to leave the text edit mode. Now right click the text and choose _Properties_ in the context menu. Here you can choose the alignment for the text.

####Suggested alignment

Shape               | Alignment
--------------------|----------
Interpreter         | Centre
Program             | Centre
Compiler left-hand  | Left
Compiler right-hand | Right

The default vertical alignment can fit up to two lines of default-sized text. Beyond that, you may have to change the vertical alignment and/or the text offset.

###Non-default shape sizes
You can freely resize the shapes, but to maintain easy grid snapping it is advisable to choose widths that are divisible by four and heights that are divisible by two relative to the grid.
