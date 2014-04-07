SideMenu App
-

- [Left-Side Menu Template](#left-side-menu-template)
- [Right-Side Menu Template](#right-side-menu-template)
- [Both-Side Menu Template](#both-side-menu-template)
- [Side Menu with header](#side-menu-with-header)


This template can be used for simple app with side menu that can be opened to switch views, this template can be used for creating applications similar to __Youtube app__ or __Gmail app__. This template can also be used for chat app with right side menu that can be opened to select items, this template can be used for creating applications similar to __Facebook Chat app__.

![SideMenuApp](https://raw.github.com/krisrak/appframework-templates/master/screenshots/SideMenuApp.png)

Left-Side Menu Template
-
The left side menu can be created by adding `<nav></nav>` element in the main `afui` DIV:
```
      <div id="afui">
        <nav>
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </nav>
        
        ...
        
      </div>  
```

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-SideMenuApp-left.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-SideMenuApp-left.html)

The left side menu can be toggled by using the method `$.ui.toggleLeftSideMenu()`

The left side menu width can be set by using the method `$.ui.setLeftSideMenuWidth(WIDTH);`

Right-Side Menu Template
-
The right side menu can be created by adding `<aside></aside>` element in the main `afui` DIV:
```
      <div id="afui">
        <aside>
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </aside>
        
        ...
        
      </div>  
```
&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-SideMenuApp-right.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-SideMenuApp-right.html)

The right side menu can be toggled by using the method `$.ui.toggleRightSideMenu()`

The left side menu width can be set by using the method `$.ui.setRightSideMenuWidth(WIDTH);`

Both-Side Menu Template
-
The left and right side menu can be created by adding `<nav></nav>` and `<aside></aside>` elements in the main `afui` DIV:
```
      <div id="afui">
        <nav>
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </nav>      
        <aside>
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </aside>
        
        ...
        
      </div>  
```
&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-SideMenuApp-both.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-SideMenuApp-both.html)

The left and right side menu can be toggled by using the methods `$.ui.toggleLeftSideMenu()` and `$.ui.toggleRightSideMenu()`

The left and right side menu width can be set by using the methods `$.ui.setLeftSideMenuWidth(WIDTH);` and `$.ui.setRightSideMenuWidth(WIDTH);`

Side Menu with header
-
A header similar to the header in main pages can be created in Side Menu by setting `title` attribute. This will created a header in side menu and add the value of `title` attribute as the title:
```
      <nav title="SideMenu">
            ...
      </nav>
      
      <aside title="Right">
            ...
      </aside>
```
![screen shot 2014-04-07 at 2 45 40 pm](https://cloud.githubusercontent.com/assets/1414842/2637507/2527feb8-be9e-11e3-9160-96744b0afdb7.png)

If you want to create the Side Menu header with custom buttons, then you can create a header manually like this:
```
      <nav title="SideMenu">
            <header class="header">
                  <h1>SideMenu</h1>
                  <a class="button icon settings"></a>
            </header>
      </nav>
```
![screen shot 2014-04-07 at 2 45 55 pm](https://cloud.githubusercontent.com/assets/1414842/2637511/297bc152-be9e-11e3-9f16-b06bb025b02f.png)


Documentation
-
Full documentation for AFUI are below, it explains all styled list in AFUI:
- [Side Menu](http://app-framework-software.intel.com/documentation.php#afui/afui_side)
- [Full Documentation](http://app-framework-software.intel.com/documentation.php#afui/afui_about)
