Title: Example of box
Description: Example of a box with children
Date Created: 2021-09-23
Tags: #example #muzzle #notes #muzzle_notes #code #c99 [[examples/examples]] [[examples/muzzle/examples]]

```c
#define MUZZLE_DEPS

#include <Muzzle.h>

#include <stdbool.h>

  

#define SCREEN_WIDTH 1280

#define SCREEN_HEIGHT 720

  

#define BORDER_SIZE 15

  

Applet applet;

  

void OnAppletUpdate()

{

 bool move = false;

  

 vec2 box_position = (vec2)

 {

 250, // X //

 400 // Y //

 };

  

 vec2 box_size = (vec2)

 {

 150, // X //

 200 // Y //

 };

  

 vec2 inner_pos = (vec2)

 {

 box_position.x + 60,

 box_position.y + 60

 };

  

 while (keep_applet(applet.window_handle))

 {

 if (move)

 {

 vec2_d buf = get_mouse_posititon(&applet);

 box_position = (vec2)

 {

 buf.x,

 buf.y

 };

  

 inner_pos = (vec2)

 {

 box_position.x + 60,

 box_position.y + 60

 };

  

 if (mouse_up(&applet, MOUSE_LEFT)) move = false;

 }

  

 if (mouse_down(&applet, MOUSE_LEFT) && move != true) move = true;

  
  

 begin_drawing();

 clear_screen(ORANGE);

  

 draw_rectangle(box_position.x - 5, box_position.y - 5, box_size.x + BORDER_SIZE, box_size.y + BORDER_SIZE, GRAY);

 draw_rectangle_vec2(box_position, box_size, BLACK);

 draw_rectangle(inner_pos.x, inner_pos.y, 50,50, WHITE);

 end_drawing(&applet);

 }

}

  

int main(void)

{
 applet = InitializeApplet(SCREEN_WIDTH, SCREEN_HEIGHT, "MuzzleStudio v0.1 - BETA", MUZZLE_FALSE, MUZZLE_TRUE);
 StartApplet(&applet);

 QuitMuzzle(applet);
 return 0;
}
```