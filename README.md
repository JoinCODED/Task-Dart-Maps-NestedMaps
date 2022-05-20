### 🍋 Maps

Given the following map of a restaurant menu:

```dart
const menu = {
  'burger': 6.5,
  'pizza': 5,
  'water': 1.5,
};
```

Calculate the total for a given order.

Example:

```dart
const order = ['pizza', 'water'];
```

Output:

```
Total: $6.5
```

and if an order element is not on the menu, the output should be:

```
rice is not on the menu
```

### 🍋 Given the following list of students:

```dart
void main() {
  List<Map<String,dynamic>> students = [
    {
      'name': 'omar',
      'major': 'engineering',
      'marks': [75, 83, 70, 74, 88],
    },
    {
      'name': 'mohammad',
      'major': 'medicine',
      'marks': [95, 82, 89, 98, 85],
    },
    {
      'name': 'salem',
      'major': 'literature',
      'marks': [60, 80, 67, 55, 77],
    },
  ];
}
```

The professor wants to calculate the average mark for each student, and then adds it as an `'average': value` key-value pair for that student.
