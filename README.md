# xBean
A Micromanager macro of simple automation
A BeanShell script/macro for micromanager to pseudo automate image taking on a fluorescent microscope.

In Micromanager, if your microscope is not motorized, to take an image, you need:

1. click live in micromanager
2. find an interested region using eyepieces
3. pull out the light path switch handle
4. focus on the screen
5. click acquire on Micromanager
6. close the image taken
7. pushback light path switch handle
8. start over 1 again

This macro saves steps 1, 5, and 6 which require you move and click the computer mouse.
Here is how this macro works: Assign a hotkey to this macro, for example, Enter.

1. press Enter, macro will start live imaging
2. find the interested region
3. pull out light path switch
4. focus on the screen
5. turn the filter block turret to the dummy one, the camera will sense the strong light and all pixel value will be 4095 (for a 12-bit camera). This will tell the macro to trigger image taking.
6. push back the light path switch, then the macro senses pixel value changes and close the image that was taken.
7. turn the filter block turret to the real one you need

Repeat 2 When finish click Enter again and the macro will stop live and exit.
