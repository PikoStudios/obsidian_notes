## Applet.h
**Description**: Including the initialization functions and Applet type

### Functions
***

> `void StartApplet(Applet *self);`

**Description**: Starts the game loop

**Returns**: Nothing

> `Applet InitializeApplet(const int WIDTH, const int HEIGHT, const char* WINDOW_TITLE, int RESIZEABLE, int VSYNC);`

**Description**: Initializes GLFW and the Applet.

**Returns**: Applet

### Types
***

> `typdef struct Applet`

**Description**: A structure with all the required variables for GLFW

**Contents**: 
`int with, height;` 
`char* WindowTitle;`
`GLFWwindow *window_handle;`

