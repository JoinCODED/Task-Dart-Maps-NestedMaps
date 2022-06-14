### 🍋 Given the following list of students:

```dart
class Student {
  String name;
  String major;
  List<int> marks;
  double average = 0;
  Student({required this.name,required this.major,required this.marks});
}

void main() {
  List<Student> students = [
    Student(
      name: 'omar',
      major: 'engineering',
      marks: [75, 83, 70, 74, 88],
    ),
    Student(
      name: 'mohammad',
      major: 'medicine',
      marks: [95, 82, 89, 98, 85],
    ),
    Student(
      name: 'salem',
      major: 'literature',
      marks: [60, 80, 67, 55, 77],
    ),
  ];
}
```

The professor wants to calculate the average mark for each student, and then adds it as an `'average': value` key-value pair for that student.

### Bonus: 🍋 Maps

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
