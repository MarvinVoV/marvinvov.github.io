---
layout: page
permalink: /python/io
categories:
  - python
---



## Json
### What distinguishes json.dump from json.dumps ?
`json.dump` and `json.dumps` are both functions provided by Python's `json` module for working with JSON data, but they serve different purposes and have distinct use cases:

1. **`json.dump()` (Write to a File)**:
   - `json.dump()` is used to serialize a Python object (typically a dictionary or a list) into a JSON formatted string and write it to a file.
   - It takes two arguments:
     - The Python object (e.g., a dictionary) to be serialized.
     - A file object (or a file-like object) where the JSON data will be written.
   - It does not return a JSON string; instead, it directly writes the JSON data to the specified file.
   - Example:

     ```python
     import json

     data = {"name": "Alice", "age": 30}
     with open("data.json", "w") as file:
         json.dump(data, file)
     ```

   - In this example, `json.dump()` writes the JSON data for the `data` dictionary to the "data.json" file.

2. **`json.dumps()` (Return JSON as a String)**:
   - `json.dumps()` is used to serialize a Python object (e.g., a dictionary or a list) into a JSON formatted string.
   - It takes one argument: the Python object to be serialized.
   - It returns a JSON formatted string containing the serialized data.
   - Example:

     ```python
     import json

     data = {"name": "Alice", "age": 30}
     json_string = json.dumps(data)
     ```

   - In this example, `json.dumps()` returns a JSON string that is stored in the `json_string` variable.

**Key Differences**:

- `json.dump()` writes JSON data to a file, whereas `json.dumps()` returns a JSON string.
- `json.dump()` is typically used when you want to store JSON data in a file for later use, such as when saving configuration settings or data for future retrieval.
- `json.dumps()` is useful when you need to work with JSON data as a string within your Python program, such as when sending JSON data in an HTTP request or processing JSON data in memory.
- `json.dump()` is often used in conjunction with a file-handling context manager (`with open(...) as ...`) to ensure proper file handling, while `json.dumps()` directly returns a JSON string that you can assign to a variable.

In summary, `json.dump` and `json.dumps` are both valuable for handling JSON data, but they are used in different contexts depending on whether you need to write JSON data to a file or work with it as a string in your Python code.