---
wrapper_template: _layouts/docs.html
context:
  title: Search and filter | Design Guidelines
  status: braindump
---
Modular Search & Filter Pattern

# Introduction

The Search and Filtering pattern allows a user to trim down specific items through large data sets. The data set will be queried when the filters are applied and/or a string search is run by user’s keywords.

\[Initial Spec + Benchmarking](https://docs.google.com/document/d/122Y2tgUzufBCF_qhWevbDt9rXBDLyf82aQ3noRitih4/edit#heading=h.2nswjpku28jg)

\[Product Requirements ](https://docs.google.com/spreadsheets/d/19fNwwEZ24WGek0q3ioc8au5W7E2JFzvIlt3a0thEAp0/edit#gid=0)

# Variants

<table>

  <tr>

   <td>Types

   </td>

   <td>Description

   </td>

   <td><a href="https://docs.google.com/document/d/122Y2tgUzufBCF_qhWevbDt9rXBDLyf82aQ3noRitih4/edit#heading=h.qpuwnwxnl1rj">Use cases</a>

   </td>

  </tr>

  <tr>

   <td rowspan="3" >

<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "Combo"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

<a href="#heading=h.9lybullge9mf">Combo</a>

   </td>

   <td rowspan="3" >Both search and filter functions will be performed on one search bar. 

<p>

The user can type and pick the filter items from a menu, or submit direct keywords to query the data. All input will be converted into input chips held in the search bar, joined by logic operators defined by the user.

   </td>

   <td rowspan="2" >JAAS Dashboard:

<ul>

<li>Find all the models running on a particular cloud

<li>Find all the models running on a particular region

<li>Search for the name of a specific model

<li>Filter models for a specific group of owners

</li>

</ul>

   </td>

  </tr>

  <tr>

  </tr>

  <tr>

   <td>Snapcraft

<ul>

<li>Licence - autocomplete field while typing 

</li>

</ul>

   </td>

  </tr>

  <tr>

   <td>

<a href="#heading=h.7o6m2eq2x79r">Split</a>

   </td>

   <td>Split filter dropdown - to give the user better vision of all the filter options. 

<p>

Split search bar - to hold input chips converted from selected filter items and user input, which are joined by logic operators defined by the user.

   </td>

   <td>MAAS Dashboard:

<ul>

<li>Find machines with similar characteristics e.g. number of disks, RAM, storage to deploy with a certain image

<li>Find machines with specific, special piece of hardware e.g. SR-IOV that has been enabled

<li>Search for machines that have a note on them

<li>Search for machines with certain tags - both tags that are visible in the table and ones that won’t be (e.g. machine tags and network tags or storage tags)

<li>\\[Future] Find virtual machines that are on the same host machine

<li>\\[Future] Find machines with available resources on the same NUMA node 

<li>Support MAAS  specific search <a href="https://maas.io/docs/interactive-search ">DSL</a> (domain-specific language) 

</li>

</ul>

   </td>

  </tr>

  <tr>

   <td>

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "Split - Simple"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

<a href="#heading=h.oummcrf2du4r">Split - Simple</a>

   </td>

   <td>Split filter dropdown - to give the user better vision of all the filter options. (Or, split expanded filter menu e.g. charmhub)

<p>

Simple search bar - only allow string search, not linked to the filter

<p>

Optional: other functions - sort, picker etc.

   </td>

   <td>RBAC

<ul>

<li>Filter and search for specific groups and users

<li>Filter all the directory for a specific backend domain

<p>

Charmhub

<ul>

<li>Filter by category and publisher, while searching by keyword

<p>

MAAS logs

<ul>

<li>Filter by log type, while searching by keyword

</li>

</ul>

</li>

</ul>

</li>

</ul>

   </td>

  </tr>

</table>



# Components

## Overview

### Combo

1. Search bar
2. Combo Menu
3. Chips

### Split

1. Search bar
2. Dropdown
3. Chips

## Search bar

### Anatomy

1. ### Text entry field

\    Where a user enters their search/filter keywords

2. Placeholder text

   Short text indicating what this field is for, also used to display the user’s input
3. Icon (optional)

\    Search icon is used to indicate search universally; X icon for removing all the input

4. Input Chips (optional)

\    Selected filter chips from the menu, or converted user’s input to use in search/filter queries

\### States

\* Inactive (with or without populated)

\* Hover

\* Focused

\* Activated 

\### Behaviours

\#### Clear Icon

The clear icon will show up as there is content existing in the search field. Clicking on will clear the content of the entire field.

\#### Focus with keyboard shortcut

Many ‘expert’ users would benefit from auto-focusing the search control with a keyboard shortcut - so they know they can instantly jump to the search field on any given view with (for example) ⌘+/  or /

\## Autocomplete list

\### Anatomy

<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.jpg). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image5.jpg "image_tooltip")

5. Container

   Loads all other components
6. Textual items

\    Clickable items, can be item names (e.g. Kubeflow Edge) or “Search for ‘xxx’...”(optional)

7. Divider

\    To separate content into clear groups

8. Highlighted hint

To stress the focus at a glance on the result findings

9. Label text (optional)

\    Item details like charms publisher or “Bundle”, not clickable here

\### States

\* Inactive (without populated) \

<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image6.png "image_tooltip")

\* Focused

\* Activated  \

As soon as you start typing \

<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.jpg). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image7.jpg "image_tooltip")

\### Behaviour

\#### Position

the menu will match the width of its search bar, and be opened right below the search bar. It will expand downwards with a certain height limit.

\#### Cancelling

The menu can be cancelled by clicking the overlay, pressing the Esc key or the cancel icon.

\#### Selecting an item

You can navigate between the suggested search results by pressing the arrow keys or hovering them. 

You can click or press enter to select them. \

It will update the page with the search results or the item page and close the autocomplete list.

\#### Scrolling

If not all menu items are displayed at once, menus can be scrollable. In this state, menus show a persistent scrollbar.

\#### As you type

While the user types, the menu will update its content by filtering out the irrelevant and highlighting the matched characters (in blue).  \

The matched highlighted hint can be at any place of the suggested results, like at the beginning, in between or in the middle of keywords results.

By selecting the textual item, the list menu will close and the page will be updated accordenly.

The ‘search for’ contextual item will always be displayed in the menu, even when there is no matched content to the user’s input.

\## Combo Menu

\### Anatomy

\### 

<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image8.png "image_tooltip")

1. Container

   Loads all other components
2. Filter Chips

\    Provide options for the user to choose from. Here the chips can be operators, or items from a category.

3. Textual items

\    Clickable items, can be category names (e.g. Regions) or “Search for ‘xxx’...”

4. Divider

\    To separate content into clear groups

5. Expanding menu indicator

\    To indicate more and how many items to be loaded within this category

\### Behaviour 

\#### Position

\##### Visual Option 1 - for long search bar

The menu will be opened by the right bound of the last chip in the search bar, until the menu’s right bound reaches the end of the search bar. It will expand downwards with a certain height limit.

\##### Visual Option 2 - for limited space

To fit limited space, the menu will match the width of its search bar, and be opened right below the search bar. It will expand downwards with a certain height limit.

\#### Cancelling

The menu can be cancelled by clicking the overlay or pressing the Esc key.

\#### Selecting an item

Upon selecting an item, the menu will stay expanded and update its content accordingly. 

The selected item will be displayed inside the search bar above. 

The menu’s position might shuffle based on the 

<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "conditions"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[conditions](#heading=h.okkomipysq7c).

\#### Scrolling

If not all menu items are displayed at once, menus can be scrollable. In this state, menus show a persistent scrollbar.

\#### Expanding menu groups

Only a certain row of chips will be displayed in the menu. To expand all the items within the category, click on the indicator (e.g. ‘+7’).

<p id="gdcalert19" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert20">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image9.png "image_tooltip")

\## 

\## Filter Dropdown (for Split)

\### Anatomy - Dropdown Button

<p id="gdcalert20" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image10.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert21">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image10.png "image_tooltip")

1. Button area

   Click to expand the menu
2. Placeholder text

\    Short text indicating what this field is for, also used to display the returned feedback e.g. label, applied filter numbers

3. Icon

\    Chevrons to indicate for expanding and collapsing

\### Anatomy - Dropdown Menu

Basically the same as the 

<p id="gdcalert21" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "Combo Menu"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert22">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[Combo Menu](#heading=h.7pv7p4gt4v8d), except:

\* Without operator chips

\* Category names are just label texts, not clickable

<p id="gdcalert22" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image11.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert23">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image11.png "image_tooltip")

1. Container

   Loads all other components
2. Label Text

\    Category names, not clickable here

3. Filter Chips

\    Provide options for the user to choose from. Here the chips will be items from a category

4. Divider

\    To separate content into clear groups

5. Expanding menu indicator

\    To indicate more and how many items to be loaded within this category

\### States

\* Inactive

\    

<p id="gdcalert23" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image12.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert24">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image12.png "image_tooltip")

\* Hover

\* Focused

\* Activated (onclick)

\    

<p id="gdcalert24" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image13.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert25">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image13.png "image_tooltip")

\* Inactive but populated

\    

<p id="gdcalert25" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image14.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert26">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image14.png "image_tooltip")

\### Behaviour

\#### Selecting an item

Upon selecting an item, the menu will stay expanded, and the dropdown header will update with the number of items (filters) selected. 

\#### Cancelling

The menu can be cancelled by clicking back the dropdown header, or clicking the overlay or pressing the Esc key.

\#### Scrolling

If not all menu items are displayed at once, menus can be scrollable. In this state, menus show a persistent scrollbar.

\#### Expanding menu groups

Only a certain row of chips will be displayed in the menu. To expand all the items within the category, click on the indicator (e.g. ‘+7’).

\## 

\## Chips 

\### Anatomy

<p id="gdcalert26" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image15.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert27">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image15.png "image_tooltip")

1. Container

To hold all chip elements, and their size is determined by those elements. 

2. Text

Chip text here can be an item, or the selected or typed item name, or an operator.

3. Remove icon (optional)

To remove this chip

\### Types

\#### Input chips

Input chips represent information used in the input field. It can be converted by the user's input text, or the filter chips selected from the menu. 

Double-clicking input chips will also allow 

<p id="gdcalert27" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "text editing"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert28">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[text editing](#heading=h.wwsfqlg1juxj).

An input chip always contains a \[x] button to remove this chip from the input field.

\#### Filter Chips

Filter Chips display options in the menu for the user to select and filter content. They can be operators, or items from a category.

\### States

\#### Input chips

(NO activated state - as that would be in text editing mode)

\* Inactive

\* Hover

\* Focused

\#### Filter Chips

\* Enabled

\* Disabled

\* Hover

\* Focused

\* Pressed

\# 

\# Combo

The Combo allows the user to search and filter data on one search bar. 

The user can type and pick the filter items from a menu, or submit direct keywords to query the data. All input will be converted into input chips held in the search bar, joined by logic operators defined by the user.

\## Behaviours

\### Inactive

<p id="gdcalert28" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image16.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert29">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image16.png "image_tooltip")

\### On click

Search bar is activated. Combo menu opens, consisting with available operators, grouped categories and their items.

The initial Combo menu will automatically disable ‘AND’, ‘OR’ logics.

<p id="gdcalert29" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image17.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert30">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image17.png "image_tooltip")

\### Select a filter chip 

Selected filter chips will be added as an input chip to the search bar, formatted as ‘Category name : Item name’. 

<p id="gdcalert30" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image18.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert31">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image18.png "image_tooltip")

\### Add an operator

An operator can be selected from the menu to link two input chips.

<p id="gdcalert31" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image19.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert32">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image19.png "image_tooltip")

\### As you type

While the user types, the menu will update its content by filtering out the irrelevant and highlighting the matched characters (in blue). 

<p id="gdcalert32" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image20.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert33">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image20.png "image_tooltip")

By selecting the contextual item or press enter, the keyword will be submitted into an input chip formatting as ‘\_keyword\_’. 

<p id="gdcalert33" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image21.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert34">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image21.png "image_tooltip")

The ‘search for’ contextual item will always be displayed in the menu, even when there is no matched content to the user’s input.

<p id="gdcalert34" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image22.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert35">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image22.png "image_tooltip")

An operator can be typed and matched as well as other filter items.

<p id="gdcalert35" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image23.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert36">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image23.png "image_tooltip")

\### Default Logics without selecting an operator

Default logics will be automatically applied and displayed when there is no operator selected between 2 input chips.

<p id="gdcalert36" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image24.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert37">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image24.png "image_tooltip")

\### Search by Category names

The user can also search and filter by category names, this would be handy when searching across multiple categories with multiple items.

Press Tab to autocomplete the input or simply click on the category element, to form the input as ‘Category name :’. Then complete the query by selecting from the items within that category.

<p id="gdcalert37" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image25.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert38">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image25.png "image_tooltip")

\### Edit a chip

<p id="gdcalert38" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image26.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert39">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image26.png "image_tooltip")

\### Delete a chip

Delete by hitting delete or backspace key

\### 

<p id="gdcalert39" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image27.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert40">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image27.png "image_tooltip")

Delete by clicking \[x] icon on the input chip

<p id="gdcalert40" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image28.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert41">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image28.png "image_tooltip")

\### Chips Overflow

<p id="gdcalert41" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image29.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert42">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image29.png "image_tooltip")

\# Split

Split pattern performs search and filter functions separately on:

\* Split filter dropdown - to display all the filter options

\* Split search bar - to hold input chips converted from selected filter items and user input, which are joined by logic operators defined by the user.

The purpose of this pattern is to give the user a better vision of all the filter options, especially in the scenario of a large number of categories.  

\## Behaviours

\### Inactive

<p id="gdcalert42" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image30.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert43">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image30.png "image_tooltip")

\### Filter on click

Filter dropdown is activated. The dropdown menu opens, consisting with grouped categories and their items.

<p id="gdcalert43" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image31.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert44">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image31.png "image_tooltip")

\### Select a filter chip 

Upon selecting an filter chip, the filter chip will be added as an input chip to the search bar, formatted as ‘Category name : Item name’. The dropdown header will update with the number of filters selected. 

<p id="gdcalert44" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image32.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert45">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image32.png "image_tooltip")

\### Search bar on Click / Add an operator

operators menu appears when the search bar is clicked.

<p id="gdcalert45" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image33.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert46">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image33.png "image_tooltip")

\### As you type

While the user types, the menu will update its content by filtering out the irrelevant and highlighting the matched characters (in blue). 

<p id="gdcalert46" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image34.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert47">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image34.png "image_tooltip")

An operator can be typed and matched as well as other filter items.

<p id="gdcalert47" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image35.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert48">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image35.png "image_tooltip")

The ‘search for’ contextual item will always be displayed in the menu, even when there is no matched content to the user’s input.

<p id="gdcalert48" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image36.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert49">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image36.png "image_tooltip")

By selecting the contextual item or pressing enter, the keyword will be submitted into an input chip formatting as ‘\_keyword\_’. The string search is not counted as a filter in the dropdown header. 

<p id="gdcalert49" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image37.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert50">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image37.png "image_tooltip")

\### Default Logics without selecting an operator

Default logics will be automatically applied and displayed when there is no operator selected between 2 input chips.

Same as 

<p id="gdcalert50" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "here"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert51">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[here](#heading=h.zfusupl2yhh5).

\### Edit a chip

Same as 

<p id="gdcalert51" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "here"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert52">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[here](#heading=h.wwsfqlg1juxj).

\### Delete a chip

Same as 

<p id="gdcalert52" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "here"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert53">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[here](#heading=h.of7dnjjnp705).

\### Chips Overflow

Same as 

<p id="gdcalert53" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "here"). Did you generate a TOC with blue links? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert54">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

\[here](#heading=h.b32br8op58s).

\### 

\# Split - Simple

Split - simple pattern consists of split filter, search and other functionalities.

Split filter dropdown - to give the user better vision of all the filter options. (Or, split expanded filter menu e.g. charmhub)

Simple search bar - only allow string search, not linked to the filter

Optional: other functions - sort, picker etc.

\## 

<p id="gdcalert54" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image38.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert55">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

!\[alt_text](images/image38.png "image_tooltip")

\## 

\# Reference

Filtering

\[https://www.carbondesignsystem.com/patterns/filtering#selection-methods](https://www.carbondesignsystem.com/patterns/filtering#selection-methods)

Search

\[https://www.carbondesignsystem.com/patterns/search-pattern/#focused-search](https://www.carbondesignsystem.com/patterns/search-pattern/#focused-search)

\[https://material.io/components/text-fields#outlined-text-field](https://material.io/components/text-fields#outlined-text-field)

Chips

\[https://material.io/components/chips#input-chips](https://material.io/components/chips#input-chips)

Menus

\[https://material.io/components/menus#specs](https://material.io/components/menus#specs)

\[https://www.carbondesignsystem.com/components/dropdown/usage/#content](https://www.carbondesignsystem.com/components/dropdown/usage/#content)
