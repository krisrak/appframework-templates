SingleViewApp template
=
This template can be used for simple application that has just one view, this template can be used for creating applications similar to __Flash light__ app or __Calculator app__. 

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-SingleViewApp.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-SingleViewApp.html)

![SingleViewApp](https://raw.github.com/krisrak/appframework-templates/master/screenshots/SingleViewApp.png)

SingleView with header and footer
-
The HTML code for creating the above UI looks like this:
```
<div id="afui">
    <div id="content">
        <div class="panel" title="Title" id="page1" selected="true">
            <p>This is a Single View App template</p>
        </div>
    </div>
</div>
```
The `#content` DIV contains all the pages for app, the `.panel` DIV with `title` attribute will create a header on top with the `title`. A blank footer (also refered to as `#navbar`) is also created by default with this HTML code.


SingleView with no footer
-
If you want to create a page with just header and no footer, then you can set attribute `data-footer="none"` in the `.panel` DIV:
```
        <div class="panel" title="Title" id="page1" data-footer="none" selected="true">
        </div>
```

SingleView with header buttons
-
You will have to add a `<header>` element within the `.panel` to create a header with button on left and right. This `<header>` should also contain a `<h1>` element that will become the title for the page. The code for SingleView app with header buttons will look like this:
```
        <div class="panel" title="Title" id="page1" selected="true">
            <header>
                <h1>New Title</h1>
                <a href="#" class="button icon location" onclick="foo()"></a>
                <a href="#settings" class="button icon settings" style="float:right">Setup</a>
            </header>
            <p>This is a Single View App template</p>
        </div>
```
Things to note:
- `<h1>` element for title should be the first element, this text will override the `title` attribute in the `.panel`
- button can be specified like any other `afui` button
- button on the right should have a `style="float:right"`

![SingleViewApp](https://raw.github.com/krisrak/appframework-templates/master/screenshots/SingleViewApp-header.png)

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-SingleViewApp-header.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-SingleViewApp-header.html)

If you plan to use this same header in a different page then you can and a `id` move the `<header>` outside the `#content` DIV and reference the header `id` in the `.panel`'s `data-header` attribute. The code will look like this:
```
<div id="afui">

    <header id="header1">
        <h1>New Title</h1>
        <a href="#" class="button icon location" onclick="foo()"></a>
        <a href="#settings" class="button icon settings" onclick="foo()" style="float:right">Setup</a>
    </header>

    <div id="content">
        <div class="panel" title="Title" id="page1" data-header="header1" selected="true">
            <p>This is a Single View App template</p>
        </div>
    </div>

</div>
```
Documentation
-
Full documentation for AFUI are below, it explains all the attributes for `.panel` and also javascript properties and methods for manupilating UI:
- [Page Layout](http://app-framework-software.intel.com/documentation.php#afui/afui_layout)
- [Panel properties](http://app-framework-software.intel.com/documentation.php#afui/afui_panels)
- [Full Documentation](http://app-framework-software.intel.com/documentation.php#afui/afui_about)

