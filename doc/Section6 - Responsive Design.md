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

## Topic 5 making site responsive

- i want the image to be on top side by side, text below the images then button
- Solution: 
- in our content target, when we click on , wiith should fit content width: fit-content;
- hide the whole image/right side  with width:0; and oapcity:0;

## Topic 7 - Responsive images

- Responsive images is to serve the right image to the right screen size and device

- The 3 use cases

- Resoulation swtiching(serve same image but decresed resolution to small screen)
- Density swtiching (serve same image but based on the screen resolution, double the size for high resolution screens like modern devices)
- Art direction(serve different image on specific defices)

## Topic 8 - Responsive Img in HTML - Art Direction/Density Switching

- density swtiching,

<img srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x">

- 1x= DPR - normal device pixel resolution, 2x: higher resolution
- the 1x and 2x are the density descriptive
- art directory

<picture class="footer__logo">
            <source
              srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x"
              media="(max-width: 37.5em)"
            >
            <img
              srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x"
              alt="logo"
              class="footer__logo"
              src="img/logo-green-2x.png"
            >
</picture>

## Topic 9 - Density and Resolution Switching 

- use srcset attribute on the img and source elements, together with density descriptors
- how and why to use the picture elemenet for art direction
- write media queries for html
- resolution swiching uses the size provided, so the browser have choice which one to use.

## Topic - 10 : Resposive images in css

1.combine multiple condition in media queries
2.use resolution media queries to target high-resolution screens 2x
3.implemenet responsive images in CSS

- @media (min-resolution: 192pi) and (min-width: 600px),(min-width: 600px){} - and combines two condition while , stands for or
- 192dpi dots-per-inch = high resolution 2x

- 192dpi apple retina display
- to support safari browser for the media resolution add this line to the condition(-webkit-min-pixel-device-ratio: 2) and (min-width: 600px)

## Topic 11 - Testing for Browser Support with @supports

- always check caniuse.com
- gracefull degardation with @supports fearure queries, this makes the code apply only if the brwser supports the feature used
- use backdrop-filter: blur()
- the filter() value of the backdrop-filter is applied to the element it self, while other value like blur() brightness(), sepia, apply to background element

## Topic 12 - Build process after development

- simple build process with npm scripts
- main.sass -> style.comp.css -> style.concat.css -> style.prefix.
- we need the build process because to reduce the http request made by brwoser
 to work with autoprefuxer we need css postcss-cli
css -> style.css
- "devDependencies"
    "autoprefixer": "^9.8.0",
    "concat": "^1.0.3",
    "node-sass": "^4.14.1",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^7.1.1"

## Topic 13 - Last touches

- media only screen = only apply to screens and not prints
- only screen(hover:none) = is for tablet or screens that dont have hover effect but with high width that exceeds the mobile media queries, like we did in card.scss