## Input.h
**Description**: Input functions and enums

### Functions
***

> `int key_up(Applet *applet, KeyInput key);`

**Description**: Checks if the key passed is up

**Returns**: Integer, 0 - The passed key is not up, 1 - The passed key is up

> `int key_down(Applet *applet, KeyInput key);`

**Description**: Checks if the key pressed is down

**Returns**: Integer, 0 - The passed key is not down, 1 - The passed key is down

> `int mouse_up(Applet *applet, MouseInput button);`

**Description**:  Checks if the passed button is up

**Returns**: Integer, 0 - The passed button is not up, 1 - The passed button is down

> `int mouse_down(Applet *applet, MouseInput button);`

**Description**: Checks if the passed key is down

**Returns** Integer, 0 - The passed button is not down, 1 - The passed button is down

> `vec2_d get_mouse_posititon(Applet* applet);`

**Description**: Returns mouse position

**Returns**: vec2_d (Vector2 with dobules)

> `double get_mouse_x(Applet* applet);`

**Description**: Returns the X position of the mouse

**Returns**: Double

> `double get_mouse_y(Applet* applet);`

**Description**: Returns the Y position of the mouse

**Returns**: Double

> `vec2 get_mouse_position_vec2(Applet* applet);`

**Description**: Returns mouse position

**Returns**: vec2

> `float get_mouse_xf(Applet* applet);`

**Description**: Returns X position of the mouse

**Returns**: float

> `float get_mouse_yf(Applet* applet);`

**Description**: Returns Y position of the mouse

**Returns**: float