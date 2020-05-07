
# Bitcoin Ticker 🤑

## Our Goal

The objective of this tutorial is to learn about using Cupertino and Material Widgets in parallel and providing a different user interface depending on the platform.


## What you will create

We’re going to make a crypto currency price checking app. By the end of the module, you'll be able to monitor your bitcoin investents on the move!



## What you will learn

- How to use the DropdownButton Widget from Material design.
- How to loop through code using Dart for and for-in loops.
- How to use Cupertino Widgets in your app.
- How to check the platform your app is being run on to customise the UI for that platform.
- Revise previous concepts by completing the challenges.

---
---

# For Loops
For loops are used to repeat certain sections of code and can iterate
through a list. I learned two types of for loops.

## for i loop
This loop assigns a variable and loops through the code for a certain number of times.

```dart
for(int i; i<10; i++){
    print i;
}
```

## for in loop
This loop iterates through a List and assigns each item of the list to a variable.
The for in loop can be used to manage more complex pieces of code, like a widget.

```dart
for (String currency in currenciesList) {
      var newItem = DropdownMenuItem(
        child: Text(currency),
        value: currency,
      );
      dropdownItems.add(newItem);
    }
```

---
---

# Cupertino Widget

[Cupertino Widget](https://flutter.dev/docs/development/ui/widgets/cupertino)  
are used to make an iOS-styled app and contain various widgets that
are found on the iPhone. For example, there is CupertinoButton, CupertinoDialog,  
and CupertinoSlider. I used the [CupertinoPicker](https://api.flutter.dev/flutter/cupertino/CupertinoPicker-class.html)
to create a iOS-styled picker.

![Flutter Widget](https://flutter.dev/images/widget-catalog/cupertino-picker.png)

```dart
CupertinoPicker(
  backgroundColor: Colors.lightBlue,
  itemExtent: 32.0,
  onSelectedItemChanged: (selectedIndex) {
    print(selectedIndex);
  },
  children: getPickerItems(),
),
```