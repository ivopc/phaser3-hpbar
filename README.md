# Phaser3-hpbar
Based on existing HP bar for Phaser 2, I made it happens on Phaser 3.

# Demo
[Click here](https://ivopc.000webhostapp.com/phaser3-hpbar/)

# Usage
Import phaser3.hpbar file:
``` html
<script src="path/to/phaser3.hpbar.js"></script>
```

In the game instance (create) add a Phaser.HealthBar like this:
```javascript
function create () {
    new Phaser.HealthBar(this, {
        x: 100, y: 100, 
        width: 114, height: 6
    });
};
```

# Configuration
This is default configuration.

new Phaser.HealthBar(this, config);
```javascript
new Phaser.HealthBar(this, {
      x: 0, y: 0, 
      width: 250, height: 40,
      bar: {
          color: "#95A5A6"
      },
      bg: {
          color: "#70F8A8"
      },
      animationDuration: 200,
      isFixedToCamera: false
});
```

Where:

- **this:** (self) instance of the game

**config:**
- **x:** initial x position.
- **y:** initial y position.
- **width:** width.
- **height:** height.
- **bar.color:** bar color.
- **bg.color:** background color.
- **animationDuration:** the duration of animation when the setPercent method is called.
- **isFixedToCamera:** if the hp bar is fixed to camera view.

# Methods

### setPercent(value, callback)
Set the percetage of the bar of display width with animation.
Example:
```javascript
const bar = new Phaser.HealthBar(this, {...});
bar.setPercent(40, () => {
  console.log("The animation is done!");
});
```

### setPercentDirectly(value)
Set the display width of the bar directly (without animation).

### setPosition(x, y)
Change the position of bar.

### setFixedToCamera(boolean)
Set/unset the bar fixed to camera.

### setToContainer(container)
Set/unset the bar to cotainer.

### destroy()
Destroy the hpbar object.

# License

phaser3-hpbar is released under the [MIT License](https://opensource.org/licenses/MIT).
