# GridView 使用技巧

## 构造

```dart
GridView.builder(
    gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
      crossAxisCount:3,
      childAspectRatio:1.0,
      crossAxisSpacing:4,
      mainAxisSpacing:4,
    ),
    itemBuilder: _buildItem,
    itemCount: photos.length,
  )
```
