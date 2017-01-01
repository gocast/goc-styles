# gocast-styles

This shared styles are used in the `gocast-client` and every widget.

It follows the BEM pattern. The main purpose of this is to have super simple css selector that make style calculation fast.

## header-layout-styles

`header-layout`: Defines a container where there is a fixed header and a content.

`header-toolbar`: Defines a toolbar that usually goes inside a header-layout__header.

`header-toolbar--secondary`: The secondary toolbar is highlighted and have position abolute. It's used along with a sibbling header-toolbar.
By default this toolbar is hidden. Add the class `header-toolbar--active` to show it.

`header-toolbar__main-content`: The toolbar content that is in the middle and flex towards both directions. Inside you can have a `header-toolbar__title` and a `header-toolbar__subtitle`.

`header-tabs`: Defines a block of tabs. `header-tabs__item` represent a tab item. Use `header-tabs__item--selected` when it's selected.

Example: 

```html
<div class="header-layout">

  <div class="header-layout__header">
    <div class="header-toolbar">
      <paper-icon-button icon="arrow-back"></paper-icon-button>
      <div class="header-toolbar__main-content">
        <div class="header-toolbar__title"></div>
        <div class="header-toolbar__subtitle"></div>
      </div>
      <paper-icon-button icon="dots-vertical"></paper-icon-button>    
    </div>

    <div class="header-toolbar header-toolbar--secondary"></div>

    <div class="header-tabs">
      <div class="header-tabs__item"></div>
      <div class="header-tabs__item header-tabs__item--selected"></div>
    </div>    
  </div>

  <div class="header-layout__content"></div>

</div>
```