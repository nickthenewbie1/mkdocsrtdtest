---
id: ui-builder
title: UI Builder
---

UI-builder is used in conjunction with the [UI-elements library](http://docs.leverege.com/docs/ui-elements) to be able to quickly style and restyle UIs. UI-builder also off loads work from developers by enabling non-technical members to edit the styling of the UI.

## Getting started

Follow the set up instructions found in [UI-elements library](http://docs.leverege.com/docs/ui-elements) to set up UI-elements and a theme in your project. In addition to this, follow the steps in [ui-active-theme](http://docs.leverege.com/docs/ui-active-theme) to install a live connection to firebase(when in development mode) that will instantly reflect any changes in UI-builder.

## Deploying 

When deploying, the css/Less needs to be exported. In the menu on the upper left, there is the option to export the theme in either Less or Css Vars. Css Vars is the recommended format, because it works better functionally with the live reloading feature. After exporting the theme, copy all the files into the theme folder in your project. 

## ThemeModel

The ThemeModel is a JSON file that UI-builder can construct a theme from. It is important to save this file in case undesired changes are made. In addition to this, if there is a common theme, you can import it into new projects to have a better starting point. Import a theme into a project, by opening the menu and selecting import them, then selecting the correct file in the file picker. UI-builder will automatically update firebase.

## Branding

Everything under the branding section of the UI-builder ui function like variables and can be used and reused throughout UI-builder. This is especially recommended for colors and sizes, so that if one needs to be changes, it only needs to be changed once to be changed everywhere. The fonts section allows for importing fonts from external sources. In the `other` section, more complex css properties can be pre-built to be reused throughout UI-builder as variables as well.

## Editing elements

When editing an element, all of its current states can be seen in the center. On the right of the screen, the widget editor is visible. The tabs at the top of the page control which state is being edited. Just under the tabs is the `Attributes +` button, which will add an attribute editor. All the current attributes can be seen in their respective editors below this. New variants can be added be typing a name in the `Add Variant` input, then clicking the `+` button next to it. Clicking on a variant will control which on is being edited. Variants can have inheritance as well; by default every variant inherits from the default variant.

## Appearances

Appearances are UI-builder projects and are the base of version control. They can have versions, which can be locked and prevented from being edited. Clicking on the purple button in the upper left corner brings you to the appearance selection screen. From here, selecting the versions option on a project will open up a side pane where the active version can be set, and any version can be locked. 
