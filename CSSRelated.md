#### How to start work with SASS?

We can create a sample project using SASS and try some CSS and can generate the CSS on the fly using a watcher.
1. Install SASS using the below command.
  
  sudo gem install sass
  
2. Run the following command to run the watcher for SASS file   (styles.scss) this will generate the CSS file on the fly whenever there is a change in this SASS file.

sass --watch path/sass-directory/styles.scss

Ref the below link for samples and steps:
https://github.com/sareeshv/PositionTest

#### How to create a triangle in CSS

```css
#triangle-up {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-bottom: 100px solid red;
  }
```
Ref: http://stackoverflow.com/questions/7073484/how-do-css-triangles-work

#### What is position and its attributes


#### What is z-index


#### What are the CSS3 features


#### How to create a circle
```html
<!-- full width container -->
<div style="width: 100%; margin:10px 0;">
    <div class="circle"></div>
</div>

<!-- half width container demo -->
<div style="width: 50%; margin:10px 0;">
    <div class="circle"></div>
</div>
```
```css
.circle {
  height: auto;
  padding-top: 25%;
  width: 25%;
  border-radius: 50%;
  background: red;
}

```
#### How to create the text inside a circle in CSS


#### What is RWD
Make pages that look great at any size.
RWD uses so-called breakpoints to determine how the layout of a site will appear: one design is used above a breakpoint and another design is applied below that breakpoint. The breakpoints are commonly based on the width of the browser.

The same HTML is served to all devices, using CSS (which determines the layout of webpage) to change the appearance of the page. Rather than creating a separate site and corresponding codebase for wide-screen monitors, desktops, laptops, tablets and phones of all sizes, a single codebase can support users with differently sized viewports.

In responsive design, page elements reshuffle as the viewport grows or shrinks. A three-column desktop design may reshuffle to two columns for a tablet and a single column for a smartphone. Responsive design relies on proportion-based grids to rearrange content and design elements.

The use of a single codebase can make development faster, compared to developing 3 or 4 distinct sites, and makes maintenance easier over time, as one set of code and content needs to be updated rather than 3 or 4. RWD is also relatively “future-proof” in that it can support new breakpoints needed at any time. If a 5-inch device or 15-inch device takes off in the market, the code can support the new devices. RWD doesn’t tie design to a particular device.

[Ref: http://www.smashingmagazine.com/2011/01/guidelines-for-responsive-web-design/]

[Ref: http://www.nngroup.com/articles/responsive-web-design-definition/]

Visual ref: http://www.starbucks.com/

#### What is media queries
CSS3 media queries to detect the width of the web browser window and apply CSS accordingly

Ref: http://cssmediaqueries.com/
Ref: http://www.smashingmagazine.com/2010/07/how-to-use-css3-media-queries-to-create-a-mobile-version-of-your-website/
Ref: http://mediaqueri.es/

#### Why to use bootstrap? How to achieve the same without bootstrap?
Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web.

It provides a faster, easier, and less repetitive solution to presentation, which will no doubt appeal to any seasoned web/app developer.Twitter Bootstrap does have some amazing built-in features, namely:

- A fluid grid layout
- Responsive design
- Custom form elements
- Typography
- JavaScript interaction
- Cross-browser compatibility

Ref: http://getbootstrap.com/getting-started/
Ref: http://bootsnipp.com/
Ref: http://www.bootply.com/


#### CSS3 animations

