ListViewApp template
-
This template can be used for simple list view application that has a main view with scrollable list and detail view for each list item, this template can be used for creating applications similar to __Mail app__, __Messages app__ or __Twitter app__.

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-ListViewApp.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-ListViewApp.html)

![ListViewApp](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp.png)

ListView with simple list
-
The HTML for list view UI above looks like this:
```
        <div class="panel" title="Title" id="listview" data-footer="none" selected="true">
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </div>
```
Each of the list item links to a detail view `.panel` which has an `id` specified in the `href` of each list item:
```
        <div class="panel" title="Item 1" id="item1" data-footer="none">
            <p>This is detail view for Item 1</p>
        </div>
```
by default the detail view opens with slide transition and a back button is created on the detail view, which will slide back to main list view when clicked.

ListView with custom list
-
The list item can be customized to show image + text, similar to __Twitter__ or __Facebook__ apps which has an image on the left and some text next to it. 

The template below shows how the ListViewApp template can be customized to have an image and text within each list item.

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-ListViewApp-social.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-ListViewApp-social.html)

```
    <style>
        #afui #listview .list li {padding:10px 20px 10px 10px}
        .list-image {float:left;width:50px;height:50px}
        .list-text {margin-left:60px;min-height:50px}        
    </style> 
```

```
            <ul class="list">
                <li>
                    <a href="#item1">
                        <img class="list-image" src="data/male_user_icon.svg" />
                        <div class="list-text"><b>username1</b><br>Placeholder text for this list item 1.</div>
                    </a>
                </li>
            </ul>    
```

![ListViewApp Social](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp-social.png)

ListView with inset style
-
Adding a `inset` class for the list will make the list appear like below:

![ListViewApp inset](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp-inset.png)

```
        <div class="panel" title="Title" id="listview" data-footer="none" selected="true">
            <br/>
            <ul class="list">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </div>
```

ListView with icons in list
-
Adding a `icon` class and class for name of icon from (afui icons)[https://github.com/krisrak/appframework-templates/blob/master/appframework/icons.css] for each list item will make the list appear like below:

![ListViewApp icons](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp-icons.png)

```
        <div class="panel" title="Title" id="listview" data-footer="none" selected="true">
            <ul class="list">
                <li><a href="#item1" class="icon home">Item 1</a></li>
                <li><a href="#item2" class="icon camera">Item 2</a></li>
                <li><a href="#item3" class="icon calendar">Item 3</a></li>
            </ul>
        </div>
```

Documentation
-
Full documentation for AFUI are below, it explains all the attributes for `.panel` and also javascript properties and methods for manupilating UI:
- [Styled List](http://app-framework-software.intel.com/documentation.php#afui/afui_lists)
- [Full Documentation](http://app-framework-software.intel.com/documentation.php#afui/afui_about)
