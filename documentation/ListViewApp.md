ListViewApp template
-

- [ListView with simple list](#listview-with-simple-list)
- [ListView with custom list](#listview-with-custom-list)
- [ListView with inset style](#listview-with-inset-style)
- [ListView with icons in list](#listview-with-icons-in-list)
- [ListView with pull-refresh](#listview-with-pull-refresh)
- [Dynamically create ListView](#dynamically-create-listview)

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
            <ul class="list inset">
                <li><a href="#item1">Item 1</a></li>
                <li><a href="#item2">Item 2</a></li>
                <li><a href="#item3">Item 3</a></li>
            </ul>
        </div>
```

ListView with icons in list
-
Adding a `icon` class and class for name of icon from [afui icons](https://github.com/krisrak/appframework-templates/blob/master/appframework/icons.css) for each list item will make the list appear like below:

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

ListView with pull-refresh
-
The `af.scroller.js` plugin included with the AFUI provides the functionality that allows you to update/refresh the listview with new content by pulling the listview down and releasing it. The `addPullToRefresh()` method of `$().scroller()` plugin can be used to enable pull-refresh feature and the `refresh-release` event handler can be used to make AJAX call to get data and update list or prepend the existing listview with new content.

The `af.scroller.js` plugin also provides the functionality that allows you to load new content when scroll reaches the end of listview. The `addInfinite()` method of `$().scroller()` plugin can be used to enable infinite scroller and the `infinite-scroll` event handler can be used to make an AJAX call to get new data and append to the listview.

&rarr; [__Demo__](http://htmlpreview.github.io/?https://raw.github.com/krisrak/appframework-templates/master/template-ListViewApp-pullRefresh.html) &rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/template-ListViewApp-pullRefresh.html)

![ListViewApp pull-refresh](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp-pullRefresh.png)

These features are helpful when creating social apps similar to Twitter, Facebook or Instagram that loads real-time data via a RESTful API and pagination is available for data feed. 

Dynamically create ListView
-
If you are loading data into a listview via a RESTful API, then the listview and corresponding detailviews will have to be created dynamically. 

This can be done in JavaScript by appending list items `<li>` to the `<ul class="list">` using `$().append()` and the detailview panels for each list item can be created using the `$.ui.addContentDiv()` method of AFUI.

Below is the code to create list item and detailview dynamically in JavaScript:

```
// get data for id, title and detail from API 
        var id, title, detail;

// create list item
        list_html += '<li><a href="#'+id+'">'+ title +'</a></li>';
        $(".list").append(list_html);

// create detailview panel for the list item
        var panel_html = '<p>'+detail+'</p>';
        $.ui.addContentDiv(id, panel_html, "Details");
```
HTML code for UI:
```
    <div id="content">
        <div class="panel" title="Title" data-footer="none" selected="true">
            <ul class="list"></ul>
        </div>
    </div>
```
__Things to note:__
- the list item `href` is assigned a unique value `id` from API, this same `id` is used for panel id
- the UI HTML contains just a panel for list view and the list is left empty
- `$.ui.addContentDiv()` will dynamically create a panel and takes parameters id, panel content and title for panel.

This sample below gets data from API* and dynamically creates list items and uses `$.ui.addContentDiv()` to dynamically add panels with content from API. _(In this sample, API data from Flixter is saved locally and then used for demo)_

&rarr; [Code](https://github.com/krisrak/appframework-templates/blob/master/app-ListViewApp-Movies.html)

![Maps App](https://raw.github.com/krisrak/appframework-templates/master/screenshots/ListViewApp-Movies.png)


Documentation
-
Full documentation for AFUI are below, it explains all styled list in AFUI:
- [Styled List](http://app-framework-software.intel.com/documentation.php#afui/afui_lists)
- [Full Documentation](http://app-framework-software.intel.com/documentation.php#afui/afui_about)
