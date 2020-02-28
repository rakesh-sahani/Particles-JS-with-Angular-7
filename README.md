# Particles.js

How to implement particles.js with Angular 7

A lightweight JavaScript library for creating particles.

![Test Image 4](https://github.com/Only1Ryu/Particles-JS/blob/master/Screenshot%20from%202019-02-25%2016-45-08.png)

## Create new Angular 7 Project or existing App

Run `npm install` 
then Run `npm install` 
Run `npm install particles.js` 

The app will automatically install the all the dependecy.

## Add the Particle.js script path inside the angular.json

add `"scripts": ["node_modules/particles.js/particles.js"]` to adding the particle.js path location.

## how to use the Particle.js in app.component.ts and app.component.html

### src/app/app.component.ts

add this code inside this file
```
declare var particlesJS: any;
```

```
  ngOnInit(){
    
    particlesJS.load('particles-js', 'assets/particles.json', function() {
      console.log('callback - particles.js config loaded');
    });
    
  }
```

### src/app/app.component.html
 
add this code inside this file

`<div id="particles-js"></div>`

### Create the json file with the name of particles.json in this path src/assets/particles.json

```
{
    "particles": {
      "number": {
        "value": 80,
        "density": {
          "enable": true,
          "value_area": 800
        }
      },
      "color": {
        "value": "#888fff"
      },
      "shape": {
        "type": "circle",
        "stroke": {
          "width": 0,
          "color": "#000000"
        },
        "polygon": {
          "nb_sides": 5
        },
        "image": {
          "src": "img/github.svg",
          "width": 100,
          "height": 100
        }
      },
      "opacity": {
        "value": 0.5,
        "random": false,
        "anim": {
          "enable": false,
          "speed": 1,
          "opacity_min": 0.1,
          "sync": false
        }
      },
      "size": {
        "value": 10,
        "random": true,
        "anim": {
          "enable": false,
          "speed": 40,
          "size_min": 0.1,
          "sync": false
        }
      },
      "line_linked": {
        "enable": true,
        "distance": 300,
        "color": "#ffffff",
        "opacity": 0.4,
        "width": 2
      },
      "move": {
        "enable": true,
        "speed": 10,
        "direction": "none",
        "random": false,
        "straight": false,
        "out_mode": "out",
        "bounce": false,
        "attract": {
          "enable": false,
          "rotateX": 600,
          "rotateY": 1200
        }
      }
    },
    "interactivity": {
      "detect_on": "canvas",
      "events": {
        "onhover": {
          "enable": true,
          "mode": "repulse"
        },
        "onclick": {
          "enable": true,
          "mode": "push"
        },
        "resize": true
      },
      "modes": {
        "grab": {
          "distance": 800,
          "line_linked": {
            "opacity": 1
          }
        },
        "bubble": {
          "distance": 800,
          "size": 80,
          "duration": 2,
          "opacity": 0.8,
          "speed": 3
        },
        "repulse": {
          "distance": 400,
          "duration": 0.4
        },
        "push": {
          "particles_nb": 4
        },
        "remove": {
          "particles_nb": 2
        }
      }
    },
    "retina_detect": true
  }
```

### Running for test

Run `ng serve` to execute.

## Further help

To get more help on the Particle.js go check out the [Particle-JS README](https://vincentgarreau.com/particles.js/).
