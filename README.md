# DrawerView-SwiftUI
 **A drawer view implemented by SwiftUI. This is not just simply a demo, instead, it can be directly used in project as a module as it has rudimentary customization flexibility.**

## Introduction & Demo

### Basic Functionality Demo

*A drawer with some bouncing animation*

![](img/basic.gif)



### Further Step

#### Click Anywhere of the Background to Dismiss DrawerView

You can click anywhere of the darken background to dismiss the DrawerView

![](img/backdismiss.gif)

#### Drag to Dismiss DrawerView

* You can drag the draggable area to dismiss the DrawerView

  ![](img/dragdismiss.gif)

* However, if the translation of drag action is shorter than you want, you can still restore the DrawerView.

  ![](img/dragrestore.gif)

* Actually, you can even drag it up if you want. You can modify this behavior in the code.

  ![](img/drag.gif)

## Usage

The entire `DrawerView` is coded in the file with the same name as `DrawerView.swift`. The setup code written in `Content.swift` which demonstrates how to use `DrawerView.swift`.

*`DrawerView` takes one required argument `isShow` to open and dismiss itself. You need to create one in your main view and bind it to `DrawerView`*

* Use `DrawerView` as `overlay`

  The code provided in the `Content.swift` uses `DrawerView` as a `overlay` of the main view.

  ``` swift
  VStack {
    // Create your own main view
  }
  .overlay(DrawerView(isShow: $isShow))
  ```

* Use `DrawerView` in `ZStack`

  ``` swift
  ZStack {
    VStack {
      // Create your own main view
    }
    
    DrawerView(isShow: $isShow)
  }
  ```

## Customization

*All customizable properties have provided in the `DrawerView.swift`. You can directly assign the preferred value to these variables when you initialize the `DrawerView`*

* `backLayerColor`
* `backLayerOpacity`
* `backLayerAnimation`
* `drawerOrientation`
* `drawerHeight`
* `drawerWidth`
* `drawerCornerRadius`
* `drawerBackgroundColor`
* `drawerOutAnimation`
* **To Be Continued**

## Contribution

This project is for demonstration purpose. Any contribution is welcome!

**Best Luck and Happy Coding!**

