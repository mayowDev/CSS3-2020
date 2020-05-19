## Topic 2 - Mobile-First vs Desktop-First and Breakpoints

### Desktop first -

* The old way of doing responve design by designing desktop/large screen layout first, and then have mediaqueries for Breakpoints to shrink the design into small layout

html{font-size: 20px}
@media max-wdith(600px or 900px){html{ font-size: 16px}}
 max-width : width must be less than or = 600px to apply the code in this bracket. 

### Mobile first 
* The new way of doing responsive design by designing for small layout/screens, and then expand the design using media query for specific breakpoints.

html{font-size: 16px}
@media min-wdith(600px){html{ font-size: 20px}}
 min-width : width must be more than or equal to 600px to apply the code.

Pros and cons of Mobile-first

1.do you users even use mobile version of the website
2.less creative freedom. more difficult to develop. 
3.desktop version may feel empty. clients used to see the desktop version first

Tip: No matter which approach you choose always remember responsive mobile and web

### Three popular Breakpoint used

1.Apple device breakpoints(bad approach)
2.most Popular devices breakpoint(good approach)
3.when Design breaks breakpoint(perfect)

![popular-breakpoint](https://user-images.githubusercontent.com/43674732/82157784-020e4b00-989d-11ea-8f07-f385af75db55.PNG)

## Topic 3 - Sass mixins for media queries

how to use mixins to write all media queries
how to use @contett and @iff sass directives
how to use dev tools for responsive design

### New conecpt

- in media queries em and rems are not effected in root font size.
- rems fail in some browsers when working with media queries, use em.
- 1em is equal to the  default  font size coming from browser = 16px
- The order of the media-query is important for how the browser reads, always the last media query  is applied. so the order matters
- background-size:100%; makes sure the image fit the container horizantaly 

## Topic 5 making responsive decisions

- i want the image to be on top side by side, text below the images then button
- Solution: 
- in our content target, when we click on , wiith should fit content width: fit-content;
- hide the whole image/right side  with width:0; and oapcity:0;