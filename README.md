DaCSSlide [![Build Status](https://drone.io/github.com/olostan/dacsslide/status.png)](https://drone.io/github.com/olostan/dacsslide/latest)
===============

Port of [JaCSS](https://github.com/olostan/jacss) - tiny "framework" for building pure CSS3-animation based presentations. 

Demo
====

http://slides.olostan.name/dartFlight/dartflightslides.html


Example
========

Example could be found in `web` folder. 

In HTML file you need to speicfy "symbols":

```html
<presentation slides="8" class="hidden">
      <symbol id="hello">
        Hello {{world}}
      </symbol>
      <symbol id="center">
        Center
      </symbol>
</presentation>
```

And in SCSS file you need to specify behaviour (Note: syntax below is using DACSSlide additions to SCSS): 
```css
#center {
  opacity:0;
}
.s2 {
  #hello: move(50,100);
   
  #center {
    background-color:red;
    opacity:1;
  }
}
.s3 {
  #hello:move(+100,+100);
}
...
```

Where `.sN` means behaviour for slide (keyframe) `N`.
