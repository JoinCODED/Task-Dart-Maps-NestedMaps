### Maps

1. Your main method should look like this:

```dart
void main() {
const menu = {
  'burger': 6.5,
  'pizza': 5,
  'water': 1.5,
};
}
```

2. Let's create an order:

```dart
void main() {
    const menu = {
        'burger': 6.5,
        'pizza': 5,
        'water': 1.5,
    };
    const order = ['pizza', 'water'];
  }
```

3. Create a variable to store the total price:

```dart
double total = 0.0;
```

4. Using a `for` loop, iterate over the `order` list:

```dart
  for (var item in order) {
  }
```

5. To get the price of the item we access the `menu` map with the `[bracket]` notation:

```dart
  for (var item in order) {
      final price = menu[item];
  }
```

6. What if the item is not in the map? the `price` value will be `null`, so let's make an `if` condition to print the error message:

```dart
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      }
  }
```

7. Otherwise we want to add the `price` to our `total` variable:

```dart
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      } else {
          total += price;
      }
  }
```

8. After we are done iterating, we print the `total`:

```dart
void main() {
    const menu = {
        'burger': 6.5,
        'pizza': 5,
        'water': 1.5,
    };
    const order = ['pizza', 'water'];
    double total = 0.0;
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      } else {
          total += price;
      }
  }
    print(total);
  }
```

### 🍋 Given the following list of students:

1. First let's iterate over our `list` of `students`:

```dart
  for (Map<String,dynamic> student in students) {
  }
```

2. Now create a variable for `marks` and extract the `marks` list for each `student`:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'];
  }
```

3. We need to tell dart that this is a list of integers using the `as` keyword:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
  }
```

4. Create a variable to store the sum of all marks:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
  }
```

5. Loop over the list of `marks` and sum all elements:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
    for (int mark in marks) {
      sum += mark;
    }
  }
```

6. Create a variable and store the average in it:

```dart
final average = sum / marks.length;
```

7. Add the new value we just created to the `student` map under the key of `average`:

```dart
student['average'] = average;
```

8. Finally, print the `student`:

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

    for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
    for (int mark in marks) {
      sum += mark;
    }
    final average = sum / marks.length;
    student['average'] = average;
    print(student);
  }
}
```
