# Ninja Invaders Tutorial

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "images.g.jres": "{\n    \"image1\": {\n        \"data\": \"hwQMABAAAAAADw8AAAAAAADwAAAA8A8AAP//APAPAADwv/0P//8P8P//Ef/////////x/////////9v/////AP//8f////////8R///////wv/0P//8P8AD//wDwDwAAAAAAAADwDwA=\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"ninja\"\n    },\n    \"P!SN:(/KL=)hR}9=bfH@\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAA/wAAAAAAAP//AAD/AADwjw8AAP//APD4DwAA8PgP8P8AAADwj///DwAAAAD//4gPAAAAAADwiP//AAAAAPD///gPAAAA/w/wjw8AAPCPDwD//wAA8PgPAAD/AAD//wAAAAAAAP8AAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"ninjaStar\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}",
  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"image1\":\n            case \"ninja\":return img`\n. . . . f f f f f . . . \n. . . f f f f f f f . . \nf . f f f f f f f f f . \n. f f b f f f f f b f . \nf . f d 1 1 b 1 1 d f . \n. . f f 1 f d f 1 f f . \n. . . f f f f f f f . . \n. . . . f f f f f . . . \n. . . f f f f f f f . . \n. . f f f f f f f f f . \n. . f f f f f f f f f . \n. f . f f f f f f f . f \n. f . f f f f f f f . f \n. . . . f f f f f . . . \n. . . . f f . f f . . . \n. . . f f f . f f f . . \n`;\n            case \"P!SN:(/KL=)hR}9=bfH@\":\n            case \"ninjaStar\":return img`\n. . . f f . . . . . . . . . . . \n. . . f f f f . . . . . . . . . \n. . . . f 8 f f . . . . . f f . \n. . . . f f 8 f . . . f f f f . \n. . . . . f f f . . f f 8 f . . \n. . . . . . f f f f f 8 f f . . \n. . . . . . f 8 8 f f f f . . . \n. . . f f f f 8 8 f . . . . . . \n. . f f 8 f f f f f . . . . . . \n. . f 8 f f . . f f f . . . . . \n. f f f f . . . f 8 f f . . . . \n. f f . . . . . f f 8 f . . . . \n. . . . . . . . . f f f f . . . \n. . . . . . . . . . . f f . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"song\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><variables><variable type=\"KIND_SpriteKind\" id=\"K2*z:_rzx9`[e$q8ZC0n\">Player</variable><variable type=\"KIND_SpriteKind\" id=\"VFp=:y%.@*gvR?Xi8u3Q\">Projectile</variable><variable type=\"KIND_SpriteKind\" id=\"KxeS}i?dXx4#:D3vE}w{\">Food</variable><variable type=\"KIND_SpriteKind\" id=\".xw^{:=xiscwN2qYYm:w\">Enemy</variable><variable id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</variable><variable id=\"os[Cf)P,X,yMSHHqVlN(\">mySprite2</variable><variable id=\"`^y]STmkDE$yv*LJDq~}\">projectile</variable><variable id=\"H^emu(|CU(bHXs!MOtGg\">y</variable><variable id=\"uF@8rkprr{!G:HXMN=-H\">alien</variable></variables><block type=\"pxt-on-start\" x=\"0\" y=\"0\"><statement name=\"HANDLER\"><block type=\"gamesetbackgroundcolor\"><value name=\"color\"><shadow type=\"colorindexpicker\"><field name=\"index\">4</field></shadow></value><next><block type=\"variables_set\"><field name=\"VAR\" id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`ninja`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"myImages.image1\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Player</field></shadow></value></block></value><next><block type=\"spritesetpos\"><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</field></block></value><value name=\"x\"><shadow type=\"positionPicker\"><field name=\"index\">76</field></shadow></value><value name=\"y\"><shadow type=\"positionPicker\"><field name=\"index\">101</field></shadow></value><next><block type=\"game_control_sprite\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"2\" _input_init=\"true\"></mutation><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</field></block></value><value name=\"vx\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">100</field></shadow></value><value name=\"vy\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">0</field></shadow></value><next><block type=\"spritesetsetstayinscreen\"><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</field></block></value><value name=\"on\"><shadow type=\"toggleOnOff\"><field name=\"on\">true</field></shadow></value><next><block type=\"hudsetScore\"><value name=\"value\"><shadow type=\"math_number\"><field name=\"NUM\">0</field></shadow></value><next><block type=\"hudSetLife\"><value name=\"value\"><shadow type=\"math_number\"><field name=\"NUM\">3</field></shadow></value></block></next></block></next></block></next></block></next></block></next></block></next></block></statement></block><block type=\"gameinterval\" x=\"582\" y=\"0\"><value name=\"period\"><shadow type=\"timePicker\"><field name=\"ms\">1000</field></shadow></value></block><block type=\"keyonevent\" x=\"670\" y=\"270\"><field name=\"button\">controller.A</field><field name=\"event\">ControllerButtonEvent.Pressed</field><statement name=\"HANDLER\"><block type=\"variables_set\"><field name=\"VAR\" id=\"`^y]STmkDE$yv*LJDq~}\">projectile</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreateprojectilefromsprite\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"{g8l|={8[d#ivD+h=yG4\"}}</data></shadow><block type=\"screen_image_picker\"><field name=\"img\">assets.image`ninjaStar`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"P!SN:(/KL=)hR}9=bfH@\"}}</data></block></value><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"spRe;C9SLdL:jzTGm{6H\">mySprite</field></block></value><value name=\"vx\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">0</field></shadow></value><value name=\"vy\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">-100</field></shadow></value></block></value></block></statement></block><block type=\"spritesoverlap\" x=\"0\" y=\"431\"><value name=\"HANDLER_DRAG_PARAM_sprite\"><shadow type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">sprite</field></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Projectile</field></shadow></value><value name=\"HANDLER_DRAG_PARAM_otherSprite\"><shadow type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">otherSprite</field></shadow></value><value name=\"otherKind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Enemy</field></shadow></value><statement name=\"HANDLER\"><block type=\"spritedestroy2\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"2\" _input_init=\"true\"></mutation><field name=\"effect\">effects.spray</field><value name=\"sprite\"><block type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">otherSprite</field></block></value><value name=\"duration\"><shadow type=\"timePicker\"><field name=\"ms\">200</field></shadow></value><next><block type=\"hudChangeScoreBy\"><value name=\"value\"><shadow type=\"math_number\"><field name=\"NUM\">1</field></shadow></value></block></next></block></statement></block></xml>",
  "main.py": "def on_on_overlap(sprite, otherSprite):\n    sprites.destroy(otherSprite, effects.spray, 200)\n    info.change_score_by(1)\nsprites.on_overlap(SpriteKind.projectile, SpriteKind.food, on_on_overlap)\n\ndef on_a_pressed():\n    global projectile\n    projectile = sprites.create_projectile_from_sprite(img(\"\"\"\n            . . . . . . . 6 6 . . . . . . . \n                    . . . . . . . 6 6 . . . . . . . \n                    . . . . . . 6 6 3 6 . . . . . . \n                    . . . . . . 6 3 3 6 . . . . . . \n                    . . . . . . 6 3 3 6 . . . . . . \n                    . . . . . . 6 3 3 6 . . . . . . \n                    . . . . . 6 6 3 3 3 6 . . . . . \n                    . . . . . 6 3 3 3 3 6 . . . . . \n                    . . . . . 6 3 3 3 3 6 . . . . . \n                    . . . . . 6 3 3 3 3 6 . . . . . \n                    . . . . 6 3 3 3 3 3 6 . . . . . \n                    . . . . 6 3 3 3 3 3 6 . . . . . \n                    . . . . 6 3 3 3 3 3 3 6 . . . . \n                    . . . . 6 3 3 3 3 3 3 6 . . . . \n                    . . . . 6 3 3 3 3 3 3 6 . . . . \n                    . . . . 6 6 6 6 6 6 6 6 . . . .\n        \"\"\"),\n        mySprite,\n        0,\n        -100)\ncontroller.A.on_event(ControllerButtonEvent.PRESSED, on_a_pressed)\n\nmySprite2: Sprite = None\nprojectile: Sprite = None\nmySprite: Sprite = None\nscene.set_background_color(4)\nmySprite = sprites.create(img(\"\"\"\n        . . . . f f f f f . . . \n            . . . f f f f f f f . . \n            f . f f f f f f f f f . \n            . f f b f f f f f b f . \n            f . f d 1 1 b 1 1 d f . \n            . . f f 1 f d f 1 f f . \n            . . . f f f f f f f . . \n            . . . . f f f f f . . . \n            . . . f f f f f f f . . \n            . . f f f f f f f f f . \n            . . f f f f f f f f f . \n            . f . f f f f f f f . f \n            . f . f f f f f f f . f \n            . . . . f f f f f . . . \n            . . . . f f . f f . . . \n            . . . f f f . f f f . .\n    \"\"\"),\n    SpriteKind.player)\nmySprite.set_position(76, 101)\ncontroller.move_sprite(mySprite, 100, 0)\nmySprite.set_stay_in_screen(True)\ninfo.set_score(0)\n\ndef on_update_interval():\n    global mySprite2\n    mySprite2 = sprites.create(img(\"\"\"\n            . . . . . . . 6 . . . . . . . . \n                    . . . . . . 8 6 6 . . . 6 8 . . \n                    . . . e e e 8 8 6 6 . 6 7 8 . . \n                    . . e 2 2 2 2 e 8 6 6 7 6 . . . \n                    . e 2 2 4 4 2 7 7 7 7 7 8 6 . . \n                    . e 2 4 4 2 6 7 7 7 6 7 6 8 8 . \n                    e 2 4 5 2 2 6 7 7 6 2 7 7 6 . . \n                    e 2 4 4 2 2 6 7 6 2 2 6 7 7 6 . \n                    e 2 4 2 2 2 6 6 2 2 2 e 7 7 6 . \n                    e 2 4 2 2 4 2 2 2 4 2 2 e 7 6 . \n                    e 2 4 2 2 2 2 2 2 2 2 2 e c 6 . \n                    e 2 2 2 2 2 2 2 4 e 2 e e c . . \n                    e e 2 e 2 2 4 2 2 e e e c . . . \n                    e e e e 2 e 2 2 e e e c . . . . \n                    e e e 2 e e c e c c c . . . . . \n                    . c c c c c c c . . . . . . . .\n        \"\"\"),\n        SpriteKind.food)\n    mySprite2.set_position(randint(0, 160), 0)\n    mySprite2.vy = 30\ngame.on_update_interval(1000, on_update_interval)\n",
  "main.ts": "controller.A.onEvent(ControllerButtonEvent.Pressed, function () {\n    projectile = sprites.createProjectileFromSprite(assets.image`ninjaStar`, mySprite, 0, -100)\n})\nsprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {\n    sprites.destroy(otherSprite, effects.spray, 200)\n    info.changeScoreBy(1)\n})\nlet projectile: Sprite = null\nlet mySprite: Sprite = null\nscene.setBackgroundColor(4)\nmySprite = sprites.create(assets.image`ninja`, SpriteKind.Player)\nmySprite.setPosition(76, 101)\ncontroller.moveSprite(mySprite, 100, 0)\nmySprite.setStayInScreen(true)\ninfo.setScore(0)\ninfo.setLife(3)\ngame.onUpdateInterval(1000, function () {\n\t\n})\n",
  "pxt.json": "{\n    \"name\": \"Ninja Invaders - Copy\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"main.py\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"images.g.jres\",\n        \"images.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.12.30\",\n        \"tag\": \"v1.12.30\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/33228b1cc7e1bea3f728c26a6047bdef35fd2c09\",\n        \"target\": \"1.12.30\",\n        \"pxt\": \"8.5.41\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"transparency16\":return transparency16;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    projectile = sprites.createProjectileFromSprite(assets.image`ninjaStar`, ninja, 0, -100)
})
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {
    sprites.destroy(sprite)
    sprites.destroy(otherSprite, effects.spray, 200)
    info.changeScoreBy(1)
})
let enemySprite: Sprite = null
let projectile: Sprite = null
let ninja: Sprite = null
scene.setBackgroundColor(9)
ninja = sprites.create(assets.image`ninja`, SpriteKind.Player)
ninja.setPosition(80, 100)
controller.moveSprite(ninja, 100, 0)
ninja.setStayInScreen(true)
info.setScore(0)
game.onUpdateInterval(1000, function () {
    enemySprite = sprites.create(img`
        . . . . . . . . . . b b b . . . 
        . . . . . . . . b e e 3 3 b . . 
        . . . . . . b b e 3 2 e 3 a . . 
        . . . . b b 3 3 e 2 2 e 3 3 a . 
        . . b b 3 3 3 3 3 e e 3 3 3 a . 
        b b 3 3 3 3 3 3 3 3 3 3 3 3 3 a 
        b 3 3 3 d d d d 3 3 3 3 3 d d a 
        b b b b b b b 3 d d d d d d 3 a 
        b d 5 5 5 5 d b b b a a a a a a 
        b 3 d d 5 5 5 5 5 5 5 d d d d a 
        b 3 3 3 3 3 3 d 5 5 5 d d d d a 
        b 3 d 5 5 5 3 3 3 3 3 3 b b b a 
        b b b 3 d 5 5 5 5 5 5 5 d d b a 
        . . . b b b 3 d 5 5 5 5 d d 3 a 
        . . . . . . b b b b 3 d d d b a 
        . . . . . . . . . . b b b a a . 
        `, SpriteKind.Enemy)
    enemySprite.setPosition(randint(0, 160), 0)
    enemySprite.setVelocity(0, 50)
})

```

## Introduction @showdialog 
**Ninja Invaders!**

In this tutorial, you will create your very own video game. Enemies will be falling from the sky, and it's up to you to destroy them before they can reach you.

Click **Ok** to get started! 

![Game Example](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/ninja-invader-gif.gif?raw=true "Ninja Invaders project")

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Welcome!
--- 

**Answer:** 

❓ Have you ever coded before?

❓ Have you ever used MakeCode Arcade?

--- 

**MakeCode Overview:** 

Your ``||text:Code Sensei||`` will now explain MakeCode Arcade's interface! 

![Ninja](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/NinjaDisplaying.png?raw=true "Explain Interface") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Make Our Background   
First up, our game needs a background. 

- :tree: Open ``||scene:Scene|`` and drag ``||scene:set background color||`` inside the ``||loops:on start||`` container already on the screen. 
- :mouse pointer: Click the grey bubble in the ``||scene: set background color||`` block and select a color to use as a background. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 
 
```blocks
scene.setBackgroundColor(9)
```

## The Game Window 
As you add code to your project, look at the Game Window on the **lower right** of your screen to see it update! 

![Game Window](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/GameWindow.png?raw=true "Game Window") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Add Our Player Sprite 
Now we are going to create our main character. 

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set ninja to||`` block to the bottom of the ``||loops: on start||`` container. 
- :mouse pointer: Click the grey square and select the **ninja** picture from **My Assets**. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let ninja = sprites.create(img``, SpriteKind.Player)
```

```blocks
scene.setBackgroundColor(9)
let ninja = sprites.create(assets.image`ninja`, SpriteKind.Player)
```

## Let's Get Moving 
Code the sprite to move left and right across the screen.

- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:set ninja position||`` to the bottom of the ``||loops: on start||`` container. 
- :keyboard: Set the **x** value to 80 and the **y** value to 100. 
- :game controller: Open ``||controller:Controller||`` and drag the ``||controller:move ninja with buttons||`` block to the bottom of the ``||loops:on start||``.
- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:set ninja stay in screen |`` to the bottom of the ``||loops:on start||``.

Try it out: use the **left** and **right** arrow keys or **A** and **D** to move the ninja sprite! 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let ninja: Sprite = null
ninja.setPosition(0, 0)
controller.moveSprite(ninja, 100, 0)
ninja.setStayInScreen(true)
```
```blocks
let ninja = sprites.create(assets.image`ninja`, SpriteKind.Player)
ninja.setPosition(80, 100)
controller.moveSprite(ninja, 100, 0)
ninja.setStayInScreen(true)
```

## Spawn The Enemies Part 1 
Spawn Enemy sprites that fall from the sky!

- :circle: Open ``||game:Game||`` and drag out an ``||game:on game update every||`` container into the coding area. The code we place here will run on a repeating timer. 
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||variables(sprites):set enemySprite to||`` block into the ``||game:on game update||`` container. 
- :mouse pointer: Click the grey box and select a sprite of your choice from **Gallery**. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let enemySprite = sprites.create(img``, SpriteKind.Enemy)
```

```blocks
game.onUpdateInterval(1000, function () {
    let enemySprite = sprites.create(img``, SpriteKind.Enemy)
})
```

## Spawn The Enemies Part 2 
Make the Enemy sprites fall!
  
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||sprites:set enemySprite position to||`` block into the ``||game:on game update||`` container below the other code.
- :keyboard: In the ``||math:pick random||`` block, change the **10** to **160** so Enemy sprites will appear anywhere along the top of the screen.
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||sprites:set enemySprite velocity to||`` block into the ``||game:on game update||`` container below the other code.
- :keyboard: Change the **vx** to **0** so the Enemy sprites only move down.

*Change the number in the ``||game:on game update every||`` container to change how often the Enemy sprites are created!*

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let enemySprite: Sprite = null
enemySprite.setPosition(randint(0, 10), 0)
enemySprite.setVelocity(50, 50)
```

```blocks
game.onUpdateInterval(1000, function () {
    let enemySprite = sprites.create(img``, SpriteKind.Enemy)
    enemySprite.setPosition(randint(0, 160), 0)
    enemySprite.setVelocity(0, 50)
})
```

## Ready, Aim, LAUNCH! 
Now we are going to code our ninja sprite's projectiles. 

- :game controller: Open ``||controller:Controller||`` and drag out a ``||controller:on A button pressed||`` container into the coding area.
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||variables(sprites):set projectile to||`` block into the container. 
- :mouse pointer: Click the grey box and select **ninjaStar** from **My Assets**.
- :keyboard: Change the **vx** to **0** and the **vy** to **-100** to make the projectiles go straight up.

Try it out: use the A button or the space key to launch projectiles upwards!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let projectile = sprites.createProjectileFromSprite(img``, ninja, 50, 50)
```

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    projectile = sprites.createProjectileFromSprite(assets.image`ninjaStar`, ninja, 0, -100)
})
```
  

## Destroy The Enemies 
Write the code to destroy the enemies with the projectiles!

- :paper plane: Open ``||sprites:Sprites||`` and drag out a ``||sprites:on sprite overlaps||`` container into the coding area.
- :paper plane: Open ``||sprites:Sprites||`` and drag **2** ``||sprites:destroy||`` blocks into the ``||sprites:overlap||`` container.
- :mouse pointer: Drag the ``||variables:sprite||`` oval from the ``||sprites:overlap||`` container onto the ``||sprites:destroy||`` block to replace **mySprite**.
- :mouse pointer: Repeat with the ``||variables:otherSprite||`` oval into the other ``||sprites:destroy||`` block.
- :mouse pointer: Click the **+** to pick a fun effect. Change the duration time to either 100 ms or 200 ms. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {

})
```

```blocks
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {
    sprites.destroy(sprite)
    sprites.destroy(otherSprite, effects.spray, 200)
})
```
 

## Keep track of the score!
Use MakeCode Arcade's built-in scoring system to keep track of the Enemy sprites you destroyed!

- :id card: Open ``||info:Info||`` and drag a ``||info:set score to 0||`` block into the bottom of the ``||loops:on start||`` container.
- :id card: Open ``||info:Info||`` and drag a ``||info:change score by 1||`` block into the bottom of the ``||sprites:overlap||`` container. 
  
Try the game out! When you are ready, move on to the final step. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blocks
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {
    sprites.destroy(sprite)
    sprites.destroy(otherSprite, effects.spray, 200)
    info.changeScoreBy(1)
})
scene.setBackgroundColor(9)
let ninja = sprites.create(assets.image`ninja`, SpriteKind.Player)
ninja.setPosition(80, 100)
controller.moveSprite(ninja, 100, 0)
ninja.setStayInScreen(true)
info.setScore(0)
```

## Customizations!
### ``||variables:C||`` ``||controller:u||`` ``||loops:s||`` ``||animation:t||`` ``||logic:o||`` ``||sprites:m||`` ``||music:i||`` ``||math:z||`` ``||scene:e||`` 

The tutorial is finished, but now it's time to customize your game! 

---

Here are a few things to try:

- :paint brush: Customize the sprites and background to your liking. It's your game! 
- :headphones: Use a ``||music:play sound||`` block to add sound effects for even more fun!
- :circle: Use ``||game:splash||`` or ``||game:show long text||`` blocks to add game instructions.
- :trophy: Allow a way to win. From ``||info:Info||`` add a ``||info:start countdown||`` or a ``||info:on score||`` block to your game!
- :repeat: Add animations! Make the projectiles spin or change color as they fly. 
- :paper plane: Make a new type of enemy sprite. Maybe something that moves faster or is harder to destroy?  

Decide which customizations you want to make to your game. Click **Done** then use the MakeCode Arcade editor to access the full list of code blocks in the Toolbox.

Then, follow your Code Sensei's guidance to create a shareable link that will let you play your game at home!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 
