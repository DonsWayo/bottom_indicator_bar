# bottom_indicator_bar

A flutter bottom tab with indicator, similar to the bottom tab of facebook app 

## Getting Started

Add the dependency in `pubspec.yaml`:

```yaml
dependencies:
  ...
  bottom_indicator_bar: lastest_version
```

## Basic Usage


```dart
class HomePage extends StatefulWidget {
  @override
  State createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  final List<BottomIndicatorNavigationBarItem> items = [
    BottomIndicatorNavigationBarItem(icon: Icons.home),
    BottomIndicatorNavigationBarItem(icon: Icons.search),
    BottomIndicatorNavigationBarItem(icon: Icons.settings),
  ];


  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Indicator Bottom Bar"),
        backgroundColor: Colors.teal,
      ),
      body: Center(
        child: Column(
          mainAxisSize: MainAxisSize.min,
          children: <Widget>[
          ],
        ),
      ),
      bottomNavigationBar: BottomIndicatorBar(
        onTap: (index) => {},
        items: items,
        activeColor: Colors.teal,
        inactiveColor: Colors.grey,
        indicatorColor: Colors.teal,
      ),
    );
  }
}
```