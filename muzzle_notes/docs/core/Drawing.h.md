## Drawing.h
**Description**: Main Drawing Functions
**Tags**: #docs #muzzle #api

### Functions
***

> `void begin_drawing();`

**Description**: Prepares GLFW to start drawing.

**Returns**: Nothing

> `void end_drawing(Applet *applet);`

**Description**: Ends drawing.

**Returns**: Nothing

> `void clear_screen(tint color_drawn);`

**Description**: Clears the screen with a color.

**Returns**: Nothing

> `void update_viewport(Applet *applet, int w, int h);`

**Description**: Update the viewport size.

**Returns**: Nothing

> `void update_viewport_lite(Applet *applet, int w, int h);`

**Description**: Updates the viewport size without checking if the value if new, could have better performance

**Returns**: Nothing