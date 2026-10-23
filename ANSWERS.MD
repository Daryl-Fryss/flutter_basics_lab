
# Flutter Architecture, Widgets and Basic UI
## IT 120 Laboratory Activities 1-5

**Student Name:** DARYL FRYSS M. PUSA
**Student ID:** 241-01031
**Section:** ICLX3

## GitHub Repository

Repository Link: (https://github.com/Daryl-Fryss/flutter_basics_lab.git)

## Activity 2: Debug Console

Copy the last three actual build() called lines from your VS Code Debug Console below.

1. build() called: 4 glasses
2. build() called: 5 glasses
3. build() called: 6 glasses

## Activity 2: setState() Experiment

When I changed the glasses variable without calling setState(), the displayed count did not update immediately. This happened because Flutter was not notified to rebuild the widget. I restored the original code so the variable changes inside setState().

## Activity 3: Expanded Experiment

When I removed Expanded from one StatBox, the boxes no longer shared the available row width equally. The layout became uneven and could overflow because there was not enough horizontal space. I restored Expanded to the box afterward.

## Activity 5: Theme Customization Experiment

I changed the button corner radius from 8 to 20. The buttons became more rounded. The change was applied through the ElevatedButton theme in buildTheme().

## Review Questions

### 1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.

A StatelessWidget displays UI that does not manage changing state of its own. An example is ProfileCard in Activity 1. A StatefulWidget is used when the UI needs to change while the app runs. An example is WaterTrackerPage in Activity 2.

### 2. Why is a StatefulWidget written as two classes? What does each class do?

The StatefulWidget class defines the widget and creates its State object. The State class stores changing data and contains the build() method that displays the interface. This separates the widget definition from its changing state.

### 3. In Activity 2, what happened when you changed _glasses outside setState()? Why?

When I changed _glasses without calling setState(), the displayed count did not update immediately. Flutter was not told to rebuild the screen. Calling setState() after a change tells Flutter to refresh the UI.

### 4. Looking at the Debug Console in Activity 2, when is build() called?

The build() method is called when Flutter needs to create or rebuild the interface. In Activity 2, it runs when the page is first displayed and when setState() triggers a rebuild after a button tap.

### 5. Explain the main axis and the cross axis of a Row and of a Column.

For a Row, the main axis is horizontal and the cross axis is vertical. For a Column, the main axis is vertical and the cross axis is horizontal.

### 6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?

Without Expanded, the box no longer shared the available row width equally with the other boxes. Expanded allows a widget to take its allocated share of the remaining available space.

### 7. Why do we use GridView.builder for the menu instead of a Column with many children?

GridView.builder arranges items in rows and columns and can build items as they are needed for display. A Column arranges its children vertically and is not designed to create a grid of menu cards.

### 8. How do Stack and Positioned create the Best seller badge in Activity 4?

Stack places the menu card's content and badge on top of each other. Positioned places the badge near the top-left corner. A conditional checks bestSeller so the badge appears only on selected items.

### 9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.

ThemeData applies shared styling across the app, such as the button style in buildTheme(). A style applied to one widget affects that specific widget, such as a TextStyle used to make the Campus Café title bold in Activity 4.

### 10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?

The _ThemeDemoAppState class holds the _isDark variable. The switch calls _setDark(), which updates the variable inside setState(). MaterialApp rebuilds and uses themeMode to select the light or dark theme.
