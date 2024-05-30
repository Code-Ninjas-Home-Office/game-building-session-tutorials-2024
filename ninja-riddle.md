# Code Ninjas Ninja Riddle Quest GBS

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "images.g.jres": "{\n    \"O*Le}YimT%e=ZFRw,=aq\": {\n        \"data\": \"hwQOABAAAAAAAAAAAAAAAAAPDwAAAAAAAPAAAADwDwAA//8A8A8AAPC//Q///w/w//8R//////////H/////////2/////8A///x/////////xH///////C//Q///w/wAP//APAPAAAAAAAAAPAPAAAAAAAAAAAA\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"ninja\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}",
  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"O*Le}YimT%e=ZFRw,=aq\":\n            case \"ninja\":return img`\n. . . . . f f f f f . . . . \n. . . . f f f f f f f . . . \n. f . f f f f f f f f f . . \n. . f f b f f f f f b f . . \n. f . f d 1 1 b 1 1 d f . . \n. . . f f 1 f d f 1 f f . . \n. . . . f f f f f f f . . . \n. . . . . f f f f f . . . . \n. . . . f f f f f f f . . . \n. . . f f f f f f f f f . . \n. . . f f f f f f f f f . . \n. . f . f f f f f f f . f . \n. . f . f f f f f f f . f . \n. . . . . f f f f f . . . . \n. . . . . f f . f f . . . . \n. . . . f f f . f f f . . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"song\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><variables><variable type=\"KIND_SpriteKind\" id=\"4-j3#IhM(kb#d]j6ODKR\">Player</variable><variable type=\"KIND_SpriteKind\" id=\"n7^]WHWahu?_NGa!wF7^\">Projectile</variable><variable type=\"KIND_SpriteKind\" id=\"x~9#ASzuu=*Re8cA1`7P\">Food</variable><variable type=\"KIND_SpriteKind\" id=\"g/f8p`J8XV?0}4ci,[[2\">Enemy</variable><variable id=\"BamhM%P#W+[Fnm4[P(,W\">mySprite</variable><variable id=\"EkI?:5acf$nnW0+|.7JE\">sensei1</variable><variable id=\"CV7`p8F${THAn*57~{;z\">sensei2</variable><variable id=\"uVsGyu^Bu#[lf9+N(U$s\">ninja</variable></variables><block type=\"pxt-on-start\" x=\"0\" y=\"0\"><statement name=\"HANDLER\"><block type=\"variables_set\"><field name=\"VAR\" id=\"uVsGyu^Bu#[lf9+N(U$s\">ninja</field><value name=\"VALUE\"><shadow type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`ninja`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"myImages.O*Le}YimT%e=ZFRw,=aq\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Enemy</field></shadow></value></block></value></block></statement></block></xml>",
  "main.ts": "let ninja = sprites.create(assets.image`ninja`, SpriteKind.Enemy)\n",
  "pxt.json": "{\n    \"name\": \"Ninja Riddle Quest Assets\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"images.g.jres\",\n        \"images.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.12.51\",\n        \"tag\": \"v1.12.51\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/eb9fd884260f64c934fb51355e36f8c76272b6b4\",\n        \"target\": \"1.12.51\",\n        \"pxt\": \"8.5.63\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n"
}
```
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    if (Math.percentChance(50)) {
        game.showLongText("Kids will create video games!", DialogLayout.Bottom)
    } else {
        game.showLongText("Kids will have fun learning!", DialogLayout.Bottom)
    }
    pause(1000)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    if (game.askForString("What do Code Senseis teach at Code Ninjas?", 6) == "coding") {
        game.gameOver(true)
    } else {
        game.showLongText("Guess again!", DialogLayout.Bottom)
        pause(1000)
    }
})
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let sensei1 = sprites.create(img`
    . f f f . f f f f . f f f . 
    f f f f f c c c c f f f f f 
    f f f f b c c c c b f f f f 
    f f f c 3 c c c c 3 c f f f 
    . f 3 3 c c c c c c 3 3 f . 
    . f c c c c 4 4 c c c c f . 
    . f f c c 4 4 4 4 c c f f . 
    . f f f b f 4 4 f b f f f . 
    . f f 4 1 f d d f 1 4 f f . 
    . . f f d d d d d d f f . . 
    . . e f e 4 4 4 4 e f e . . 
    . e 4 f b 3 3 3 3 b f 4 e . 
    . 4 d f 3 3 3 3 3 3 c d 4 . 
    . 4 4 f 6 6 6 6 6 6 f 4 4 . 
    . . . . f f f f f f . . . . 
    . . . . f f . . f f . . . . 
    `, SpriteKind.Player)
sensei1.setPosition(40, 30)
let sensei2 = sprites.create(img`
    . . . . f f f f . . . . . 
    . . f f f f f f f f . . . 
    . f f f f f f c f f f . . 
    f f f f f f c c f f f c . 
    f f f c f f f f f f f c . 
    c c c f f f e e f f c c . 
    f f f f f e e f f c c f . 
    f f f b f e e f b f f f . 
    . f 4 1 f 4 4 f 1 4 f . . 
    . f e 4 4 4 4 4 4 e f . . 
    . f f f e e e e f f f . . 
    f e f b 7 7 7 7 b f e f . 
    e 4 f 7 7 7 7 7 7 f 4 e . 
    e e f 6 6 6 6 6 6 f e e . 
    . . . f f f f f f . . . . 
    . . . f f . . f f . . . . 
    `, SpriteKind.Player)
sensei2.setPosition(120, 30)
let ninja = sprites.create(img`
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . f . f f f f f f f f f . . 
    . . f f b f f f f f b f . . 
    . f . f d 1 1 b 1 1 d f . . 
    . . . f f 1 f d f 1 f f . . 
    . . . . f f f f f f f . . . 
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . . . f f f f f f f f f . . 
    . . . f f f f f f f f f . . 
    . . f . f f f f f f f . f . 
    . . f . f f f f f f f . f . 
    . . . . . f f f f f . . . . 
    . . . . . f f . f f . . . . 
    . . . . f f f . f f f . . . 
    `, SpriteKind.Enemy)
ninja.setPosition(80, 100)
game.showLongText("What do Code Senseis teach kids at Code Ninjas?", DialogLayout.Center)
game.showLongText("Ask the Senseis for hints! Talk to the Ninja when you know the answer!", DialogLayout.Center)
music.play(music.melodyPlayable(music.baDing), music.PlaybackMode.UntilDone)
game.splash("")
info.startCountdown(10)
```


## Introduction @showdialog 
**Ninja Riddle Quest**

In this tutorial, you will create your very own video game. Solve the Ninja's riddle by getting clues from the Code Senseis!

Click **Ok** to get started! 

![Game Example](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/NinjaRiddleQuestgif.gif?raw=true "Ninja Riddle Quest project") 

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
scene.setBackgroundColor(7)
```  

## The Game Window 
As you add code to your project, look at the Game Window on the **lower right** of your screen to see it update! 

![Game Window](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/GameWindow.png?raw=true "Game Window") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Add Our Player Sprite 
Now we are going to create our main character. 

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set mySprite to||`` block to the bottom of the ``||loops: on start||`` container. 
- :mouse pointer: Click the grey oval and select any image you would like from the **Gallery** of sprite images.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blocks
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
```

## Let's Get Moving 
Code the sprite to move around the screen.

- :game controller: Open ``||controller:Controller||`` and drag ``||controller:move mySprite with buttons||`` block to the bottom of the ``||loops:on start||`` container. 
- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:set mySprite stay in screen |`` to the bottom of our ``||loops:on start||``.

Try it out: use the **arrow keys** or **WASD** to move the sprite around the screen. Notice how the sprite cannot leave the screen.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blocks
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
```

## Add The Ninja
Now we are going to create our Ninja character with the riddle. 

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set ninja to||`` block to the bottom of the ``||loops:on start||`` container. 
- :mouse pointer: Click the grey oval, click on the **My Assets** tab, then select the **ninja** image. 
- :paper plane: Open ``||sprites:Sprites||`` again and drag the ``||sprites:set ninja position to||`` block to the bottom of the ``||loops:on start||``.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let ninja = sprites.create(img``, SpriteKind.Enemy)
ninja.setPosition(80, 100)
```

```blocks
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let ninja = sprites.create(img`
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . f . f f f f f f f f f . . 
    . . f f b f f f f f b f . . 
    . f . f d 1 1 b 1 1 d f . . 
    . . . f f 1 f d f 1 f f . . 
    . . . . f f f f f f f . . . 
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . . . f f f f f f f f f . . 
    . . . f f f f f f f f f . . 
    . . f . f f f f f f f . f . 
    . . f . f f f f f f f . f . 
    . . . . . f f f f f . . . . 
    . . . . . f f . f f . . . . 
    . . . . f f f . f f f . . . 
    `, SpriteKind.Enemy)
ninja.setPosition(80, 100)
```

## Riddle Me This!
Come up with your own riddle question and answer, then add it to the game!

- :paper plane: Open ``||sprites:Sprites||`` and drag out the entire ``||sprites:on sprite (Player) overlaps (Enemy)||`` chunk of code and place it anywhere in the editor.
- :mouse pointer: Click the bubble in the ``||game:ask for string||`` block to type your riddle's **question**.
- :mouse pointer: Click the bubble after the **=** sign to type your riddle's **answer**.

Try the game out: see what happens when the Player sprite overlaps the Ninja! 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    if (game.askForString("") == "") {
        game.gameOver(true)
    } else {
        game.showLongText("Guess again!", DialogLayout.Bottom)
        pause(1000)
    }
})
```

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    if (game.askForString("question") == "answer") {
        game.gameOver(true)
    } else {
        game.showLongText("Guess again!", DialogLayout.Bottom)
        pause(1000)
    }
})
```

## Add A Code Sensei to Help!
Add a Code Sensei sprite to provide a hint!

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set sensei1 to||`` block to the bottom of the ``||loops: on start||`` container. 
- :mouse pointer: Click the grey oval and select a sprite of your choice from **Gallery**. 
- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||sprites:set sensei1 position to||`` block into the bottom of the ``||loops: on start||`` container.

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let sensei1 = sprites.create(img``, SpriteKind.Player)
sensei1.setPosition(40, 30)
```

```blocks
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let ninja = sprites.create(img`
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . f . f f f f f f f f f . . 
    . . f f b f f f f f b f . . 
    . f . f d 1 1 b 1 1 d f . . 
    . . . f f 1 f d f 1 f f . . 
    . . . . f f f f f f f . . . 
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . . . f f f f f f f f f . . 
    . . . f f f f f f f f f . . 
    . . f . f f f f f f f . f . 
    . . f . f f f f f f f . f . 
    . . . . . f f f f f . . . . 
    . . . . . f f . f f . . . . 
    . . . . f f f . f f f . . . 
    `, SpriteKind.Enemy)
ninja.setPosition(80, 100)
let sensei1 = sprites.create(img`
    . f f f . f f f f . f f f . 
    f f f f f c c c c f f f f f 
    f f f f b c c c c b f f f f 
    f f f c 3 c c c c 3 c f f f 
    . f 3 3 c c c c c c 3 3 f . 
    . f c c c c 4 4 c c c c f . 
    . f f c c 4 4 4 4 c c f f . 
    . f f f b f 4 4 f b f f f . 
    . f f 4 1 f d d f 1 4 f f . 
    . . f f d d d d d d f f . . 
    . . e f e 4 4 4 4 e f e . . 
    . e 4 f b 3 3 3 3 b f 4 e . 
    . 4 d f 3 3 3 3 3 3 c d 4 . 
    . 4 4 f 6 6 6 6 6 6 f 4 4 . 
    . . . . f f f f f f . . . . 
    . . . . f f . . f f . . . . 
    `, SpriteKind.Player)
sensei1.setPosition(40, 30)
``` 

## Add Another Code Sensei!
Add a second Code Sensei to help solve the riddle!

- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||variables(sprites):set sensei2 to||`` block to the bottom of the ``||loops: on start||`` container. 
- :mouse pointer: Click the grey oval and select a sprite of your choice from **Gallery**. 
- :paper plane: Open ``||sprites:Sprites||`` and drag the ``||sprites:set sensei2 position to||`` block into the bottom of the ``||loops: on start||`` container.


![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
let sensei2 = sprites.create(img``, SpriteKind.Player)
sensei2.setPosition(120, 30)
```

```blocks
scene.setBackgroundColor(7)
let mySprite = sprites.create(img`
    . . . . . . f f f f . . . . . . 
    . . . . f f f 2 2 f f f . . . . 
    . . . f f f 2 2 2 2 f f f . . . 
    . . f f f e e e e e e f f f . . 
    . . f f e 2 2 2 2 2 2 e e f . . 
    . . f e 2 f f f f f f 2 e f . . 
    . . f f f f e e e e f f f f . . 
    . f f e f b f 4 4 f b f e f f . 
    . f e e 4 1 f d d f 1 4 e e f . 
    . . f e e d d d d d d e e f . . 
    . . . f e e 4 4 4 4 e e f . . . 
    . . e 4 f 2 2 2 2 2 2 f 4 e . . 
    . . 4 d f 2 2 2 2 2 2 f d 4 . . 
    . . 4 4 f 4 4 5 5 4 4 f 4 4 . . 
    . . . . . f f f f f f . . . . . 
    . . . . . f f . . f f . . . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
let ninja = sprites.create(img`
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . f . f f f f f f f f f . . 
    . . f f b f f f f f b f . . 
    . f . f d 1 1 b 1 1 d f . . 
    . . . f f 1 f d f 1 f f . . 
    . . . . f f f f f f f . . . 
    . . . . . f f f f f . . . . 
    . . . . f f f f f f f . . . 
    . . . f f f f f f f f f . . 
    . . . f f f f f f f f f . . 
    . . f . f f f f f f f . f . 
    . . f . f f f f f f f . f . 
    . . . . . f f f f f . . . . 
    . . . . . f f . f f . . . . 
    . . . . f f f . f f f . . . 
    `, SpriteKind.Enemy)
ninja.setPosition(80, 100)
let sensei1 = sprites.create(img`
    . f f f . f f f f . f f f . 
    f f f f f c c c c f f f f f 
    f f f f b c c c c b f f f f 
    f f f c 3 c c c c 3 c f f f 
    . f 3 3 c c c c c c 3 3 f . 
    . f c c c c 4 4 c c c c f . 
    . f f c c 4 4 4 4 c c f f . 
    . f f f b f 4 4 f b f f f . 
    . f f 4 1 f d d f 1 4 f f . 
    . . f f d d d d d d f f . . 
    . . e f e 4 4 4 4 e f e . . 
    . e 4 f b 3 3 3 3 b f 4 e . 
    . 4 d f 3 3 3 3 3 3 c d 4 . 
    . 4 4 f 6 6 6 6 6 6 f 4 4 . 
    . . . . f f f f f f . . . . 
    . . . . f f . . f f . . . . 
    `, SpriteKind.Player)
sensei1.setPosition(40, 30)
let sensei2 = sprites.create(img`
    . . . . f f f f . . . . . 
    . . f f f f f f f f . . . 
    . f f f f f f c f f f . . 
    f f f f f f c c f f f c . 
    f f f c f f f f f f f c . 
    c c c f f f e e f f c c . 
    f f f f f e e f f c c f . 
    f f f b f e e f b f f f . 
    . f 4 1 f 4 4 f 1 4 f . . 
    . f e 4 4 4 4 4 4 e f . . 
    . f f f e e e e f f f . . 
    f e f b 7 7 7 7 b f e f . 
    e 4 f 7 7 7 7 7 7 f 4 e . 
    e e f 6 6 6 6 6 6 f e e . 
    . . . f f f f f f . . . . 
    . . . f f . . f f . . . . 
    `, SpriteKind.Player)
sensei2.setPosition(120, 30)
```

## Here's a Hint!
Provide 2 different hints that help solve the riddle!

- :paper plane: Open ``||sprites:Sprites||`` and drag out the entire ``||sprites:on sprite (Player) overlaps (Player)||`` chunk of code and place it anywhere in the editor.
- :mouse pointer: Click the bubble in the first ``||game:show long text||`` block to type the first **hint**.
- :mouse pointer: Click the bubble in the second ``||game:show long text||`` block to type the second **hint**.

Try the game out: see what happens when the Player sprite overlaps the Code Senseis! 

Ask someone else to try your game - see if they can figure out the Ninja's riddle using the Code Senseis' hints!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

```blockconfig.local
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    if (Math.percentChance(50)) {
        game.showLongText("", DialogLayout.Bottom)
    } else {
        game.showLongText("", DialogLayout.Bottom)
    }
    pause(1000)
})
```

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    if (Math.percentChance(50)) {
        game.showLongText("hint #1", DialogLayout.Bottom)
    } else {
        game.showLongText("hint #2", DialogLayout.Bottom)
    }
    pause(1000)
})
```

## Customizations!

### ``||variables:C||`` ``||controller:u||`` ``||loops:s||`` ``||animation:t||`` ``||logic:o||`` ``||sprites:m||`` ``||music:i||`` ``||math:z||`` ``||scene:e||`` 

The tutorial is finished, but now it's time to customize your game!

---

Here are a few things to try:

- :paint brush: Customize the sprites and background to your liking. It's your game! 
- :circle: Use ``||game:splash||`` or ``||game:show long text||`` blocks to add game instructions.
- :headphones: Use a ``||music:play sound||`` block to add sound effects for even more fun!
- :id card: Use a ``||info:start countdown||`` timer to challenge the user to solve the riddle in a certain amount of time.

When you are finished, click **Done** then follow your Code Sensei's guidance to create a shareable link that will let you play your game at home!

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials-2024/blob/master/images/CN-Logo.png?raw=true "CN Logo") 
