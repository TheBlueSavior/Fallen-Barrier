## Initialization
When creating a Fairy you must override their `start()` method where most logic is defined.
Ex:
```cs
override void start() {
    super.start();
}
```

## Sprites
To assign sprites you simply push a some sprites to your fairy can use
Ex:
```cs
possSprite.push("FA_1");
possSprite.push("FA_2");
```

## Attacks
Attacks are pretty easy to add but is kinda tedious.
First you create an array that holds all of the statelabels of your attacks.
```cs
static const statelabel posStates[] = {
	"RegularBarrage",
	"SuperBurst",
	"DestructibleBullets",
	"WeaverBullets",
	"RedLaser"
};
```
Then in your start method assign `attack` to one of your array's elements.
In this instance we are just picking a random attack:
```cs
attack = posStates[random(0, 4)];
```

## Hit sounds
Hit sounds are straight forward. Just push the sounds you want to use.
```cs
hitSounds.push("FA_1");
hitSounds.push("FA_2");
```

## Finishing up
Once all of your Fairy's fields are filled out you may run `super.start()`
`super.start` will finish up the rest of the start function and assign sprites, sounds, or whatever
Final code:
```cs
static const statelabel posStates[] = {
	"RegularBarrage",
	"SuperBurst",
	"DestructibleBullets",
	"WeaverBullets",
	"RedLaser"
};
override void start() {
    possSprite.push("FA_1");
    possSprite.push("FA_2");

    attack = posStates[random(0, 4)];

    hitSounds.push("FA_1");
    hitSounds.push("FA_2");
    super.start();
}
```