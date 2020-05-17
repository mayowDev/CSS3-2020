Lesson: 2. Mobile-First vs Desktop-First and Breakpoints

A: Desktop first = is the old way of doing the responve design by
designing desktop/large screen layout first, and then have 
mediaqueries for Breakpoints to shrink the design into small layout

html{font-size: 20px}
@media max-wdith(600px or 900px){html{ font-size: 16px}}
 max-width : width must be less than or = 600px to apply the code in this bracket. 

B: Mobile first = is the new way of doing responsive design, start writing 
for small layout/screens, and then expand the design using media query
for specif breakpoints.

html{font-size: 16px}
@media min-wdith(600px){html{ font-size: 20px}}
 min-width : width must be more than or equal to 600px to apply the code.

Pros and cons of Mobile-first

1.do you users even use mobile version of the website
2.less creative freedom. more difficult to develop. 
3.desktop version may feel empty. clients used to see the desktop version first

Tip: No matter which approahc you choose always remember responsive mobile and web

::3 Breakpoint options

1.Apple device breakpoints(bad approach)
2.most Popular devices breakpoint(good approach)
3.when Design breaks breakpoint(perfect)

![popular-breakpoint](https://user-images.githubusercontent.com/43674732/82157784-020e4b00-989d-11ea-8f07-f385af75db55.PNG)
