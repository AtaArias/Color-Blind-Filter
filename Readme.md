# Color Blind Filter for Love2d
    
    This a shader to simulate how a color blind people see things

## Usage

    Require the main file in the project

    ```lua
        require 'location/cvd'
    ```

    Call the start function to begin the shader

    ```lua
        function love.draw()
            cvd.start(cvdKind, severeness)

            -- draw stuff

            cvd.finish()
        end
    ```

    The first parameter is the kind of color vission deficiency, this can be:

    't' for Tritanomaly that makes it hard to tell the difference between blue and green, and between yellow and red.

    ```lua
        cvd.start('t', severeness) -- t for Tritanomaly
    ```

    'd' for Deuteranomaly that makes the green look more red

    ```lua
        cvd.start('d', severeness) -- d for Deuteranomaly
    ```

    'p' for Protanomaly that makes red look mor green and less bright.

    ```lua
        cvd.start('p', severeness) -- p for Protanomaly
    ```

    The second parameter is the severness of the color vission deficiency severness, this is a value from 1 to 10. 
    
    10 being zero distinction.

    1 a little deficiency.

## Things to take into consideration

    This is a shader, when you call cvd.start() it will disable the previous shader and if you set a shader after calling cvd.start() that will disable the cvd filter.

## Source
https://www.inf.ufrgs.br/~oliveira/pubs_files/CVD_Simulation/CVD_Simulation.html

## More info about colorblindess
https://www.nei.nih.gov/learn-about-eye-health/eye-conditions-and-diseases/color-blindness


