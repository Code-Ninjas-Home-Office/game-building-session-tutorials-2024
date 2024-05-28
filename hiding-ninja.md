# Code Ninjas Hiding Ninjas GBS

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "images.g.jres": "{\n    \"P4(`CNLh^)P:D9Kpa+R5\": {\n        \"data\": \"hwQMABAAAAAADw8AAAAAAADwAAAA8A8AAP//APAPAADwv/0P//8P8P//Ef/////////x/////////9v/////AP//8f////////8R///////wv/0P//8P8AD//wDwDwAAAAAAAADwDwA=\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"ninjaSprite\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}",
  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"P4(`CNLh^)P:D9Kpa+R5\":\n            case \"ninjaSprite\":return img`\n. . . . f f f f f . . . \n. . . f f f f f f f . . \nf . f f f f f f f f f . \n. f f b f f f f f b f . \nf . f d 1 1 b 1 1 d f . \n. . f f 1 f d f 1 f f . \n. . . f f f f f f f . . \n. . . . f f f f f . . . \n. . . f f f f f f f . . \n. . f f f f f f f f f . \n. . f f f f f f f f f . \n. f . f f f f f f f . f \n. f . f f f f f f f . f \n. . . . f f f f f . . . \n. . . . f f . f f . . . \n. . . f f f . f f f . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"song\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><variables><variable id=\"W)t)RD5T*{kylRj-;L]a\">mySprite</variable><variable type=\"KIND_SpriteKind\" id=\"5bdv9B~8K.:##DQEJ`|g\">Player</variable><variable type=\"KIND_SpriteKind\" id=\"HLjMyi$oA.5AZIiJn#i;\">Projectile</variable><variable type=\"KIND_SpriteKind\" id=\"$n4#WqCz^D~`PmLUo]tx\">Food</variable><variable type=\"KIND_SpriteKind\" id=\"(uYX/Oj@Oq5d3SRMzGa8\">Enemy</variable></variables><block type=\"pxt-on-start\" x=\"0\" y=\"0\"><statement name=\"HANDLER\"><block type=\"variables_set\"><field name=\"VAR\" id=\"W)t)RD5T*{kylRj-;L]a\">mySprite</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`ninjaSprite`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"P4(`CNLh^)P:D9Kpa+R5\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Player</field></shadow></value></block></value></block></statement></block></xml>",
  "main.ts": "let mySprite = sprites.create(assets.image`ninjaSprite`, SpriteKind.Player)\n",
  "pxt.json": "{\n    \"name\": \"Ninja Sprite\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"images.g.jres\",\n        \"images.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.12.30\",\n        \"tag\": \"v1.12.30\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/33228b1cc7e1bea3f728c26a6047bdef35fd2c09\",\n        \"target\": \"1.12.30\",\n        \"pxt\": \"8.5.41\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n"
}
```
```blocks
info.onScore(10, function () {
    game.gameOver(true)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    sprites.destroy(otherSprite, effects.disintegrate, 200)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    ninja.setPosition(randint(0, 160), randint(0, 120))
    for (let index = 0; index < 40; index++) {
        blocker = sprites.create(img`
            . . . . c c c b b b b b . . . . 
            . . c c b 4 4 4 4 4 4 b b b . . 
            . c c 4 4 4 4 4 5 4 4 4 4 b c . 
            . e 4 4 4 4 4 4 4 4 4 5 4 4 e . 
            e b 4 5 4 4 5 4 4 4 4 4 4 4 b c 
            e b 4 4 4 4 4 4 4 4 4 4 5 4 4 e 
            e b b 4 4 4 4 4 4 4 4 4 4 4 b e 
            . e b 4 4 4 4 4 5 4 4 4 4 b e . 
            8 7 e e b 4 4 4 4 4 4 b e e 6 8 
            8 7 2 e e e e e e e e e e 2 7 8 
            e 6 6 2 2 2 2 2 2 2 2 2 2 6 c e 
            e c 6 7 6 6 7 7 7 6 6 7 6 c c e 
            e b e 8 8 c c 8 8 c c c 8 e b e 
            e e b e c c e e e e e c e b e e 
            . e e b b 4 4 4 4 4 4 4 4 e e . 
            . . . c c c c c e e e e e . . . 
            `, SpriteKind.Food)
        blocker.setPosition(randint(0, 160), randint(0, 120))
    }
    info.changeScoreBy(1)
})
let blocker: Sprite = null
let ninja: Sprite = null
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
ninja = sprites.create(img`
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    f . f f f f f f f f f . 
    . f f b f f f f f b f . 
    f . f d 1 1 b 1 1 d f . 
    . . f f 1 f d f 1 f f . 
    . . . f f f f f f f . . 
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    . . f f f f f f f f f . 
    . . f f f f f f f f f . 
    . f . f f f f f f f . f 
    . f . f f f f f f f . f 
    . . . . f f f f f . . . 
    . . . . f f . f f . . . 
    . . . f f f . f f f . . 
    `, SpriteKind.Enemy)
ninja.setPosition(randint(0, 160), randint(0, 120))
info.setScore(0)
game.showLongText("Find the Hiding Ninja!", DialogLayout.Bottom)
```


## Introduction @showdialog 
**Hiding Ninja!**

In this tutorial, you will create your very own video game. A ninja is playing hide and seek, and it's up to you to find them in each round. The game will get harder each time you find the ninja. 

Click **Ok** to get started! 

![Game Example](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/hiding_ninja.gif?raw=true "Hiding Ninja project") 

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

## Making Our Background   

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

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set mySprite to||`` block to the bottom of the ``||loops: on start||`` container. 
- :mouse pointer: Click the grey oval and select a sprite of your choice from **Gallery**. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blocks
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
```

## Let's Get Moving 
Code the sprite to move around the screen.

- :game controller: Open ``||controller:Controller||`` and drag ``||controller:move mySprite with buttons||`` block to the bottom of the ``||loops:on start||`` container. 
- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:set mySprite stay in screen |`` to the bottom of our ``||loops:on start||``.

Try it out: use the **arrow keys** or **WASD** to move the sprite around the screen. Notice how the sprite cannot leave the screen.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blocks
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
```

## Add The Hiding Ninja 
Now we are going to create our hiding ninja character. 

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set ninja to||`` block to the bottom of the ``||loops:on start||`` container. 
- :mouse pointer: Click the grey oval and select the **ninja** from **My Assets**. 
- :paper plane: Open ``||sprites:Sprites||`` again and drag the ``||sprites:set ninja position to||`` block to the bottom of the ``||loops:on start||``.

The ``||math:pick random||`` block will set the ninja sprite to hide in a different position each round of the game.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let ninja = sprites.create(img``, SpriteKind.Enemy)
ninja.setPosition(randint(0, 160), randint(0, 120))
```

```blocks
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let ninja = sprites.create(img`
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    f . f f f f f f f f f . 
    . f f b f f f f f b f . 
    f . f d 1 1 b 1 1 d f . 
    . . f f 1 f d f 1 f f . 
    . . . f f f f f f f . . 
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    . . f f f f f f f f f . 
    . . f f f f f f f f f . 
    . f . f f f f f f f . f 
    . f . f f f f f f f . f 
    . . . . f f f f f . . . 
    . . . . f f . f f . . . 
    . . . f f f . f f f . . 
    `, SpriteKind.Enemy)
ninja.setPosition(randint(0, 160), randint(0, 120))
```

## Find the Ninja 
Add code to detect when the **Player** sprite finds the ninja, or **Enemy** sprite. 

- :paper plane: Open ``||sprites:Sprites||`` and drag out a ``||sprites:on sprite (Player) overlaps (Enemy)||`` container and place it anywhere in the editor.
- :paper plane: Open ``||sprites:Sprites||`` again and drag another ``||sprites:set ninja position to||`` block inside the ``||sprites:overlap||`` container.  
  

Whenever the **Player** touches the **Enemy**, the code inside the ``||sprites:overlap||`` container will run. Try the game out: see what happens when the sprites overlap! 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {

})
let ninja: Sprite = null
ninja.setPosition(randint(0, 160), randint(0, 120))
```

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    ninja.setPosition(randint(0, 160), randint(0, 120))
})
let ninja: Sprite = null
```

## Spawn The Blocker Sprites
The Enemy sprite is always out in the open and easy to find, so let's fix that. 

- :repeat: Open ``||loops:Loops||`` and drag out a ``||loops:repeat (4) times||`` block into the bottom of the ``||sprites:overlap||`` container.
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||variables(sprites):set blocker to||`` block inside the ``||loops:repeat||`` loop. 
- :mouse pointer: Click the grey oval and select a sprite of your choice from **Gallery**.
- :paper plane: Open ``||sprites:Sprites||`` and drag a ``||sprites:set blocker position to||`` block inside the ``||loops:repeat||`` loop.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let blocker = sprites.create(img``, SpriteKind.Food)
blocker.setPosition(randint(0, 160), randint(0, 120))
```

```blocks
let ninja: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    ninja.setPosition(randint(0, 160), randint(0, 120))
    for (let index = 0; index < 4; index++) {
        let blocker = sprites.create(img`
            . . . . c c c b b b b b . . . . 
            . . c c b 4 4 4 4 4 4 b b b . . 
            . c c 4 4 4 4 4 5 4 4 4 4 b c . 
            . e 4 4 4 4 4 4 4 4 4 5 4 4 e . 
            e b 4 5 4 4 5 4 4 4 4 4 4 4 b c 
            e b 4 4 4 4 4 4 4 4 4 4 5 4 4 e 
            e b b 4 4 4 4 4 4 4 4 4 4 4 b e 
            . e b 4 4 4 4 4 5 4 4 4 4 b e . 
            8 7 e e b 4 4 4 4 4 4 b e e 6 8 
            8 7 2 e e e e e e e e e e 2 7 8 
            e 6 6 2 2 2 2 2 2 2 2 2 2 6 c e 
            e c 6 7 6 6 7 7 7 6 6 7 6 c c e 
            e b e 8 8 c c 8 8 c c c 8 e b e 
            e e b e c c e e e e e c e b e e 
            . e e b b 4 4 4 4 4 4 4 4 e e . 
            . . . c c c c c e e e e e . . . 
            `, SpriteKind.Food)
        blocker.setPosition(randint(0, 160), randint(0, 120))
    }
})
``` 

## Repeat The Enemies, Eat The Enemies 
Let's adjust the number of blocker sprites, but allow the Player sprite to clear them out!
   
- :mouse pointer: Click on the bubble in the ``||loops:repeat (4) times||`` block to change the number to something larger than 4. Test out a few options!
- :paper plane: Open ``||sprites:Sprites||`` and drag out a ``||sprites:on sprite (Player) overlaps (Food)||`` container and place it anywhere in the editor.
- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||sprites:destroy mySprite||`` inside the container. 
- :mouse pointer: Drag a ``||variables:otherSprite||`` from the container into where it says **mySprite**.

Notice what happens when the **Player** sprite overlaps the **Food**, or "blocker" sprites!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    
})
sprites.destroy(mySprite, effects.disintegrate, 200)
```

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    ninja.setPosition(randint(0, 160), randint(0, 120))
    for (let index = 0; index < 40; index++) {
        let blocker = sprites.create(img`
            . . . . c c c b b b b b . . . . 
            . . c c b 4 4 4 4 4 4 b b b . . 
            . c c 4 4 4 4 4 5 4 4 4 4 b c . 
            . e 4 4 4 4 4 4 4 4 4 5 4 4 e . 
            e b 4 5 4 4 5 4 4 4 4 4 4 4 b c 
            e b 4 4 4 4 4 4 4 4 4 4 5 4 4 e 
            e b b 4 4 4 4 4 4 4 4 4 4 4 b e 
            . e b 4 4 4 4 4 5 4 4 4 4 b e . 
            8 7 e e b 4 4 4 4 4 4 b e e 6 8 
            8 7 2 e e e e e e e e e e 2 7 8 
            e 6 6 2 2 2 2 2 2 2 2 2 2 6 c e 
            e c 6 7 6 6 7 7 7 6 6 7 6 c c e 
            e b e 8 8 c c 8 8 c c c 8 e b e 
            e e b e c c e e e e e c e b e e 
            . e e b b 4 4 4 4 4 4 4 4 e e . 
            . . . c c c c c e e e e e . . . 
            `, SpriteKind.Food)
        blocker.setPosition(randint(0, 160), randint(0, 120))
    }
})

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    sprites.destroy(otherSprite, effects.disintegrate, 200)
})

let ninja: Sprite = null
```

## A Way To Win 
Use MakeCode Arcade's built-in scoring system to keep track of the ninjas you found!

- :id card: Open ``||info:Info||`` and drag a ``||info:set score to 0||`` block into the ``||loops:on start||`` container below the other code.
- :id card: Open ``||info:Info||`` and drag a ``||info:change score by 1||`` block into the ``||sprites: (Player) overlaps (Enemy)||`` container. 
- :id card: Open ``||info:Info||`` and drag the ``||info:on score 10||`` container anywhere in the editor.

The game will now end when the ninja has been found 10 times!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
info.onScore(10, function () {
    game.gameOver(true)
})
```

```blocks
info.onScore(10, function () {
    game.gameOver(true)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    ninja.setPosition(randint(0, 160), randint(0, 120))
    for (let index = 0; index < 40; index++) {
        let blocker = sprites.create(img`
            . . . . c c c b b b b b . . . . 
            . . c c b 4 4 4 4 4 4 b b b . . 
            . c c 4 4 4 4 4 5 4 4 4 4 b c . 
            . e 4 4 4 4 4 4 4 4 4 5 4 4 e . 
            e b 4 5 4 4 5 4 4 4 4 4 4 4 b c 
            e b 4 4 4 4 4 4 4 4 4 4 5 4 4 e 
            e b b 4 4 4 4 4 4 4 4 4 4 4 b e 
            . e b 4 4 4 4 4 5 4 4 4 4 b e . 
            8 7 e e b 4 4 4 4 4 4 b e e 6 8 
            8 7 2 e e e e e e e e e e 2 7 8 
            e 6 6 2 2 2 2 2 2 2 2 2 2 6 c e 
            e c 6 7 6 6 7 7 7 6 6 7 6 c c e 
            e b e 8 8 c c 8 8 c c c 8 e b e 
            e e b e c c e e e e e c e b e e 
            . e e b b 4 4 4 4 4 4 4 4 e e . 
            . . . c c c c c e e e e e . . . 
            `, SpriteKind.Food)
        blocker.setPosition(randint(0, 160), randint(0, 120))
    }
    info.changeScoreBy(1)
})
scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . . . . b c . . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    b d d d b b d 5 5 5 4 4 4 4 4 b 
    b b d 5 5 5 b 5 5 4 4 4 4 4 b . 
    b d c 5 5 5 5 d 5 5 5 5 5 b . . 
    c d d c d 5 5 b 5 5 5 5 5 5 b . 
    c b d d c c b 5 5 5 5 5 5 5 b . 
    . c d d d d d d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let ninja = sprites.create(img`
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    f . f f f f f f f f f . 
    . f f b f f f f f b f . 
    f . f d 1 1 b 1 1 d f . 
    . . f f 1 f d f 1 f f . 
    . . . f f f f f f f . . 
    . . . . f f f f f . . . 
    . . . f f f f f f f . . 
    . . f f f f f f f f f . 
    . . f f f f f f f f f . 
    . f . f f f f f f f . f 
    . f . f f f f f f f . f 
    . . . . f f f f f . . . 
    . . . . f f . f f . . . 
    . . . f f f . f f f . . 
    `, SpriteKind.Enemy)
ninja.setPosition(randint(0, 160), randint(0, 120))
info.setScore(0)
```

## Customizations!

### ``||variables:C||`` ``||controller:u||`` ``||loops:s||`` ``||animation:t||`` ``||logic:o||`` ``||sprites:m||`` ``||music:i||`` ``||math:z||`` ``||scene:e||`` 

The tutorial is finished, but now it's time to customize your game!

Otherwise, click **Done** to open your game in MakeCode Arcade then follow your Code Sensei's guidance to create a shareable link that will let you play your game at home!

---

Here are a few things to try:

- :paint brush: Customize the sprites and background to your liking. It's your game! 
- :headphones: Use a ``||music:play sound||`` block to add sound effects for even more fun!
- :id card: Use a ``||info:start countdown||`` timer to challenge the user to complete the game in a certain amount of time.
- :circle: Use ``||game:splash||`` or ``||game:show long text||`` blocks to add game instructions.

*Decide with your Sensei which customizations you want to make to your game. Click **Done** then use the MakeCode Arcade editor to access the full list of code blocks in the Toolbox.* 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 
