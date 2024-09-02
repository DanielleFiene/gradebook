# gradebook

# Gradebook Manipulation in Python

This project demonstrates basic list manipulation in Python by simulating the management of a gradebook. The script performs operations such as appending new subjects, modifying existing grades, and combining gradebooks from different semesters.

## Project Overview

The code showcases how to:
- Create and manipulate nested lists.
- Append new elements to lists.
- Modify specific elements within nested lists.
- Remove elements from lists.
- Combine two lists to form a complete gradebook.

## Code Breakdown

### Initial Data Setup

We begin with data representing grades from the last semester and the current semester:

```python
last_semester_gradebook = [["politics", 80], ["latin", 96], ["dance", 97], ["architecture", 65]]

subjects = ['physics', 'calculus', 'poetry', 'history']
grades = [98, 97, 85, 88]

gradebook = [
    ['physics', 98],
    ['calculus', 97],
    ['poetry', 85],
    ['history', 88]
]
```

### Adding New Subjects and Modifying Grades

We append two new subjects, `computer science` and `visual arts`, to the `gradebook` and then update the grade for `visual arts`:

```python
gradebook.append(['computer science', 100])
gradebook.append(['visual arts', 93])
gradebook[-1][-1] = 98  # Update visual arts grade to 98
```

### Removing and Replacing a Grade

We remove the numeric grade for `poetry` and replace it with a pass/fail indication:

```python
gradebook[2].remove(85)
gradebook[2].append('Pass')  # Replace the grade with 'Pass'
```

### Combining Gradebooks

Finally, we combine the grades from the last semester with the current semester to form a `full_gradebook`:

```python
full_gradebook = last_semester_gradebook + gradebook
print(full_gradebook)
```

### Output

The `full_gradebook` will contain the following data:

```python
[['politics', 80], ['latin', 96], ['dance', 97], ['architecture', 65], 
['physics', 98], ['calculus', 97], ['poetry', 'Pass'], 
['history', 88], ['computer science', 100], ['visual arts', 98]]
```

## How to Run the Code

1. Clone this repository.
2. Ensure you have Python installed.
3. Run the Python script using:

   ```bash
   python gradebook.py
   ```

## Learning Outcomes

By studying this script, you'll gain insights into:
- Basic list operations in Python.
- Working with nested lists.
- Practical use cases for list manipulation in real-world scenarios.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have suggestions for improvements or additional features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

