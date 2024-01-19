### Hi there 👋
- 🔭 I’m currently working on finishing my apprenticeship in software development.
- 🌱 I’m learning Kameleoon, JavaScript, HTML, CSS, Sitecore, C# & SQL in my apprenticeship right now. In my freetime I'm working through courses on Codecademy to improve my Git skills (amongst others).
- 😄 Pronouns: she/her
- 📫 How to reach me: www.linkedin.com/in/larissa-uttich
<!--
**Lauttich/Lauttich** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...

- ⚡ Fun fact: ...




---
Title: "Strings"
Description: "This concise guide covers Rust's distinctive treatment of strings, exploring types like `String` and `&str`, syntax details, and string manipulation using operators (`+`, `+=`, `format!`)."
Subjects:
  - "Computer Science"
  - "Code Foundations"
CatalogContent:
  - "concepts/slices/sliced.md"
  - "paths/computer-science"
---


## Strings
**Strings**, fundamental to any programmer's toolkit, undergo a distinctive treatment in Rust. The language's approach to string manipulation, influenced by its systems-focused design, sets it apart from conventional programming languages. This concept entry will provide insights into creating and manipulating strings in Rust, offering practical examples to illustrate key aspects. 
  
Tackling data structures of variable size, such as strings, can get a bit tricky, and Rust has its own spin on it. In Rust, a string is essentially a sequence of Unicode characters encoded in UTF-8. Consider the string "Codecademy Rust concept," where each character is a valid Unicode entity – "C," "o," "d," "e," "c," and so forth. Rust's distinctive approach to string representation adds depth to its system-level programming paradigm.**
  
### String types
  
In Rust, there are several types related to strings, each serving a specific purpose.
1. **`String`**
   - **Description:** A heap-allocated, growable, and mutable string type.
   - **Usage:** Used when dynamic string manipulation and ownership transfer are required.
   - **Example:**
     ```rust
     let mut dynamic_string = String::from("Hello, Rust!");
     ```

2. **`&str` (String Slice)**
   - **Description:** A reference to a sequence of UTF-8 bytes, often used as a view into a `String` or a string literal.
   - **Usage:** Commonly used for string references without ownership or when dealing with parts of a string.
   - **Example:**
     ```rust
     let string_literal: &str = "Hello, Rust!";
     ```

4. **`CString`**
   - **Description:** A string type representing a C-compatible, null-terminated string. Used for FFI (Foreign Function Interface) interactions with C code.
   - **Usage:** When interfacing with C libraries that expect null-terminated strings.
   - **Example:**
     ```rust
     use std::ffi::CString;

     let c_string = CString::new("Hello, C!").expect("CString creation failed");
     ```

> [!NOTE]
> These string types cover various scenarios, from dynamic and mutable strings (`String`) to static and immutable string slices (`&str`). Choosing the appropriate type depends on the specific requirements and characteristics of the data being manipulated.

  ***
    
## Syntax with Examples

Understanding the syntax of Rust strings involves creating, manipulating, and referencing strings.

### Creating Strings

1. **Using `String::new()`**:

   ```rust
   let mut empty_string = String::new();
   ```

   This creates a new, mutable, empty `String` that can be later modified and or assigned to a variable.

2. **Using String Literals with `String::from`**:

   ```rust
   let greeting = String::from("Hello, World!");
   ```

   `String::from` allocates memory on the heap and initializes a new string with the specified string literal.

### String Manipulation
  
1. **Concatenation**
  
   In Rust, there are multiple ways to concatenate strings, and the choice of operator or method depends on the ownership and borrowing considerations. The primary operators used for string concatenation are `+` and `+=`. Here's an explanation of each:

   > **`+` Operator:**

   - **Usage:** The `+` operator can be used for concatenating two strings.
   - **Ownership:** The `+` operator takes ownership of the left operand, which means the left operand is consumed.
   - **Borrowing:** To concatenate with a borrowed string (e.g., `&str`), you need to explicitly borrow it using the `&` operator.
   - **Example:**
     ```rust
     let hello = String::from("Hello, ");
     let world = String::from("World!");
     let hello_world = hello + &world;  // Takes ownership of 'hello'
     ```

   > **`+=` Operator:**

     - **Usage:** The `+=` operator is an in-place concatenation operation.
     - **Ownership:** Unlike `+`, `+=` does not take ownership of the left operand; it appends to the existing string.
     - **Borrowing:** It works directly with the mutable reference of the left operand.
     - **Example:**
       ```rust
       let mut hello = String::from("Hello, ");
       let world = String::from("World!");
       hello += &world;  // Appends 'World!' to the existing 'Hello, '
       ```

   > **`format!` Macro:**

     - **Usage:** The `format!` macro creates a new string by formatting text, allowing for string interpolation.
     - **Ownership:** It does not involve ownership transfer and is a convenient way to create strings without borrowing or ownership concerns.
     - **Example:**
       ```rust
       let hello = String::from("Hello, ");
       let world = String::from("World!");
       let hello_world = format!("{}{}", hello, world);  // Creates a new string without ownership issues
       ```

  > [!IMPORTANT]
  > When working with strings in Rust, it's crucial to be mindful of ownership and borrowing semantics, especially when using operators like `+`. The choice between `+` and `+=` depends on whether you want to create a new string or modify an existing one in place. Additionally, the `format!` macro provides a flexible and ownership-friendly way to concatenate strings with interpolation.
  

2. **Slicing & Appending with `push_str` and `push`**:
  
     ```rust
     let mut message = String::from("Rust");
     message.push_str(" Programming");
     message.push('!');
     // Slicing
     let part_of_message = &message[0..4];  // Extracts a slice from the string, starting at index 0 and ending before index 4
     ```

      In the given example, push_str is utilized to append a string slice to the existing string (message), and push is employed to add a single character ('!') to the end. The subsequent section demonstrates slicing, extracting a portion of the string (message) using the syntax &message[start_index..end_index]. Here, &message[0..4] extracts a slice, starting at index 0 and ending before index 4, resulting in 'Rust'.



### Referencing Strings

String slices (`&str`) can reference parts of a string without taking ownership:

```rust
let full_string = String::from("Hello, World!");
let slice = &full_string[0..5]; // Creating a reference to the first five characters
```

Here, `&full_string[0..5]` creates a reference to the first five characters of `full_string`.

Understanding the syntax of Rust strings involves familiarity with methods like `String::from`, `push_str`, `push`, and the operators used for concatenation. Additionally, grasping the concept of string slices (`&str`) is crucial for efficiently working with portions of string data.

-->
