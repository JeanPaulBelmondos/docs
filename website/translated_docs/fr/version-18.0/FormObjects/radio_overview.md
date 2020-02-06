---
id: version-18.0-radiobuttonOverview
title: Bouton radio
original_id: radiobuttonOverview
---

## Aperçu

Les boutons radio sont des objets qui permettent à l’utilisateur de sélectionner une valeur parmi un groupe de valeurs.

Un bouton radio apparaît sous la forme d’un texte suivi d’un cercle. However, radio buttons can have [various appearances](#button-styles).

![](assets/en/FormObjects/radio1.png)

A radio button is selected:

- when the user clicks on it
- when it has the focus and the user presses the **Space bar** key.

## Configuring radio buttons

Radio buttons are used in coordinated sets: only one button at a time can be selected in the set. In order to operate in a coordinated manner, a set of radio buttons must share the same [Radio Group](properties_Object.md#radio-group) property.

Radio buttons are controlled with methods. Like all buttons, a radio button is set to 0 when the form is first opened. A method associated with a radio button executes when the button is selected. The following is an example of a group of radio buttons used in a video collection database to enter the speed of the recording (SP, LP, or EP):

![](assets/en/FormObjects/radio2.png)

Selecting one radio button in a group sets that button to 1 and all of the others in the group to 0. Only one radio button can be selected at a time.

> You can associate [Boolean type expressions](properties_Object.md#variable-or-expression) with radio buttons. In this case, when a radio button in a group is selected, its variable is True and the variables for the group's other radio buttons are False.

The value contained in a radio button object is not saved automatically (except if it is the representation of a Boolean field); radio button values must be stored in their variables and managed with methods.

## Styles de bouton

Radio [button styles](properties_TextAndPicture.md#button-style) control radio button's general appearance as well as its available properties. It is possible to apply different predefined styles to radio buttons. However, the same button style must be applied to all radio buttons in a group so that they work as expected.

4D provides radio buttons in the following predefined styles:

### Classique

The Regular radio button style is a standard system button (*i.e.*, a small bullseye with text) which executes code when a user clicks on it.

![](assets/en/FormObjects/radio_regular.png)

In addition to initiating code execution, the Regular radio button style changes bullsey color when being hovered.

### A plat

The Flat radio button style is a standard system button (*i.e.*, a small bullseye with text) which executes code when a user clicks on it.

![](assets/en/FormObjects/radio_flat.png)

By default, the Flat style has a minimalist appearance. Le style graphique du bouton A plat est particulièrement utile pour les formulaires à imprimer.

### Barre d’outils

The Toolbar radio button style is primarily intended for integration in a toolbar.

Par défaut, le style bouton Barre d'outils a un fond transparent avec un libellé au centre. En fonction du système d'exploitation, le design du bouton peut changer lorsque la souris le survole :

- *Windows* - the button is highlighted. 

![](assets/en/FormObjects/radio_toolbar.png)

- *macOS* - the highlight of the button never appears. 

### Bevel

The Bevel radio button style is similar to the [Toolbar](#toolbar) style's behavior, except that it has a light gray background and a gray outline. En fonction du système d'exploitation, le design du bouton peut changer lorsque la souris le survole :

- *Windows* - the button is highlighted.
    
    ![](assets/en/FormObjects/radio_bevel.png)

- *macOS* - the highlight of the button never appears.

### Bevel arrondi

Le style du bouton Bevel arrondi est presque identique au style [Bevel](#bevel), à l'exception des coins du bouton qui peuvent, selon le système d'exploitation, être arrondis.

- *Windows* - the button is identical to the [Bevel](#bevel) style.

- *macOS* - the corners of the button are rounded. ![](assets/en/FormObjects/roundedBevel.png)

### OS X Gradient

Le style du bouton OS X Gradient est presque identique au style [Bevel](#bevel), à l'exception de son apparence qui peut, en fonction du système d'exploitation, avoir deux tons.

- *Windows* - the button is identical to the [Bevel](#bevel) style.

- *macOS* - the button is displayed as a two-tone system button.

### OS X Texture

The OS X Textured radio button style is nearly identical to the [Toolbar](#toolbar) style except, depending on the OS, it may have a different appearance and does not display hover.

Par défaut, le style OS X Textured apparaît comme :

- *Windows* - a toolbar-like button with a label in the center and the background is always displayed.

- *macOS* - a standard system button displaying a color change from light to dark gray. Sa hauteur est prédéfinie : il n'est pas possible de l'agrandir ou de la réduire.
    
    ![](assets/en/FormObjects/OSXTextured.png)

### Office XP

The Office XP button style combines the appearance of the [Regular](#regular) style with the [Toolbar](#toolbar) style's behavior.

Les couleurs (surbrillance et arrière-plan) d'un bouton au style Office XP sont basées sur les couleurs du système. En fonction du système d'exploitation, le design du bouton peut changer lorsque la souris le survole :

- *Windows* - its background only appears when the mouse rolls over it.
    
    ![](assets/en/FormObjects/radio_xp.png)

- *macOS* - its background is always displayed.

### Contracter/Déployer

This button style can be used to add a standard collapse/expand icon. Ces boutons sont utilisés nativement dans les listes hiérarchiques. In Windows, the button looks like a [+] or a [-]; in macOS, it looks like a triangle pointing right or down.

![](assets/en/FormObjects/checkbox_collapse.png)

### Bouton disclosure

The disclosure radio button style displays the radio button as a standard disclosure button, usually used to show/hide additional information. The button symbol points downwards with value 0 and upwards with value 1.

![](assets/en/FormObjects/checkbox_disclosure.png)

### Personnalisé

The Custom radio button style accepts a personalized background picture and allows managing additional parameters such as [icon offset](properties_TextAndPicture.md#icon-offset) and [margins](properties_TextAndPicture.md#horizontalMargin).

## Supported properties

All radio buttons share the same set of basic properties:

[Bold](properties_Text.md#bold) - [Bottom](properties_CoordinatesAndSizing.md#bottom) - [Button Style](properties_TextAndPicture.md#button-style) - [Class](properties_Object.md#css-class) - [Expression Type](properties_Object.md#expression-type) - [Focusable](properties_Entry.md#focusable) - [Font](properties_Text.md#font) - [Font Color](properties_Text.md#font-color) - [Height](properties_CoordinatesAndSizing.md#height) - [Help Tip](properties_Help.md#help-tip) - [Horizontal Sizing](properties_ResizingOptions.md#horizontal-sizing) - [Italic](properties_Text.md#italic) - [Left](properties_CoordinatesAndSizing.md#left) - [Method](properties_Action.md#method) - [Object Name](properties_Object.md#object-name) - [Radio Group](properties_Object.md#radio-group) - [Right](properties_CoordinatesAndSizing.md#right) - [Shortcut](properties_Entry.md#shortcut) - [Title](properties_Object.md#title) - [Top](properties_CoordinatesAndSizing.md#top) - [Type](properties_Object.md#type) - [Underline](properties_Text.md#underline) - [Variable or Expression](properties_Object.md#variable-or-expression) - [Vertical Sizing](properties_ResizingOptions.md#vertical-sizing) - [Visibility](properties_Display.md#visibility) - [Width](properties_CoordinatesAndSizing.md#width)

Additional specific properties are available depending on the [button style](#button-styles):

- [Chemin d'accès arrière-plan](properties_TextAndPicture.md#backgroundPathname) - [Marge horizontale](properties_TextAndPicture.md#horizontalMargin) - [Décalage icône](properties_TextAndPicture.md#icon-offset) - [Marge verticale](properties_TextAndPicture.md#verticalMargin) (Personnalisé)
- [Nombre d'états](properties_TextAndPicture.md#number-of-states) - [Chemin d'accès image](properties_TextAndPicture.md#picture-pathname) - [Position Titre/Image](properties_TextAndPicture.md#title-picture-position) (Bouton barre outils, Bevel, Bevel arrondi, OS X Gradient, OS X Textured, Office XP, Personnalisé)