# Gradient Bottom Navigation Bar
[![pub package](https://img.shields.io/pub/v/gradient_bottom_navigation_bar.svg)](https://pub.dartlang.org/packages/gradient_bottom_navigation_bar)

This package allows you to add a gradient to the standard Material Bottom Navigation Bar.

## Getting Started

First, add this line in your project's ` pubspec.yaml `

```yml
dependencies:
  ...
  gradient_bottom_navigation_bar: ^1.0.0+4
```

For help getting started with Flutter, view the online
[documentation](https://flutter.io/).

## Usage examples
Import `gradient_bottom_navigation_bar.dart` in your desired class

```dart
import 'package:gradient_bottom_navigation_bar/gradient_bottom_navigation_bar.dart';

...
```

### Basic implementation

```dart
@override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Example'),
      ),
      body: Center(
        child: _widgetOptions.elementAt(_selectedIndex),
      ),
      bottomNavigationBar: GradientBottomNavigationBar(
        backgroundColorStart: Colors.purple,
        backgroundColorEnd: Colors.deepOrange,
        items: <BottomNavigationBarItem>[
          BottomNavigationBarItem(icon: Icon(Icons.home), title: Text('Home')),
          BottomNavigationBarItem(icon: Icon(Icons.business), title: Text('Business')),
          BottomNavigationBarItem(icon: Icon(Icons.school), title: Text('School')),
        ],
        currentIndex: _selectedIndex,
        onTap: _onItemTapped,
      ),
    );
  }
```

You can also check the [example](https://github.com/JTorrus/GradientBottomNavigationBar/tree/master/example) for additional information.

## Screenshots
![Example](https://i.imgur.com/ALh6vY3.png)
