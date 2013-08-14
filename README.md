list-searcher
=============

A jQuery plugin to search through an HTML list using a form input - an alternative to autocomplete, especially useful where the only function of the page is to select from the list.

<h2>Usage:</h2>
$('ul.myList').listSearcher();<br>
$('ul.myList').listSearcher({<br>
  <i>...options...</i><br>
});

<h2>Options:</h2>

<dl>
<dt>search_input <i>string</i></dt>
<dd><b>Default:</b> .search<br>
The selector to find the input used to trigger the search action. Is bound to keyup to trigger search.</dd>
</dl>
<dl>
<dt>list_element <i>string</i></dt>
<dd><b>Default:</b> > li<br>
A selector used to find the list items (searchable items). Must be contained within the element on which the plugin is initialised.</dd>
</dl>
<dl>
<dt>search_element_text <i>boolean</i></dt>
<dd><b>Default:</b> true<br>
If true, the text contained within list items will be searched. If false, a data-* attribute on each item can be searched instead.</dd>
</dl>
<dl>
<dt>search_data <i>string</i></dt>
<dd><b>Default:</b> name<br>
If search_element_text is false, the data-* attribute matching this option will be searched instead of the element text. Eg. default is data-name attribute. <b>Warning:</b> As of version 1.0, this will cause an error if not all searchable items have the attribute.</dd>
</dl>
<dl>
<dt>visibility_data <i>string</i></dt>
<dd><b>Default:</b> he_list_vis<br>
The data-* attribute used to store visibility data used internally by the plugin. Change this if it clashes with a data-* atrribute you are using, for example.</dd>
</dl>
<dl>
<dt>animate <i>boolean</i></dt>
<dd><b>Default:</b> false<br>
If true, the list elements will animate instead of just disappearing and reappearing. Not recommended for large lists.</dd>
</dl>
<dl>
<dt>delay <i>float</i></dt>
<dd><b>Default:</b> 0.01<br>
The amount of time in seconds to delay each sequential animation by. Only used if animate is true. Adjust this if your list disappears too quickly or too slowly, set to 0 to animate all at once.</dd>
</dl>
<dl>
<dt>before_update <i>function</i></dt>
<dd><b>Default:</b> function() { return true; }<br>
Executed before updating the visibility of the items on the list. If the function returns false the list item visibility is not changed. For example, you could use this to prevent searching until the user has entered at least 3 characters.</dd>
</dl>
<dl>
<dt>after_update <i>function</i></dt>
<dd><b>Default:</b> function() { }<br>
Executed after updating the visibility of the items on the list.</dd>
</dl>
<dl>
<dt>debug <i>boolean</i></dt>
<dd><b>Default:</b> false<br>
Enable this to allow the plugin to write to the console. Useful for debugging &amp; development.</dd>
</dl>

<a href="http://heatherevens.me.uk">http://heatherevens.me.uk</a>
