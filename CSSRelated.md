1. How to start work with SASS?
--------------------------------
We can create a sample project using SASS and try some CSS and can generate the CSS on the fly using a watcher.
1. Install SASS using the below command.
  
  sudo gem install sass
  
2. Run the following command to run the watcher for SASS file   (styles.scss) this will generate the CSS file on the fly whenever there is a change in this SASS file.

sass --watch path/sass-directory/styles.scss

Ref the below link for samples and steps:
https://github.com/sareeshv/PositionTest

2. How to create a triangle
--------------------------------
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
