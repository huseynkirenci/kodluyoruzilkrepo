# kodluyoruzilkrepo
Kodluyoruz Eğitimi kapsamında açtığım ilk repo
# Symfony HelloController Example

This is a basic Symfony project demonstrating the use of controllers, routing, and template rendering with Twig.

## Project Structure

This project contains a `HelloController` that renders a list of messages and also allows you to view individual messages by their ID.

### Controller: HelloController

- **Namespace**: `App\Controller`
- **Base Class**: `AbstractController`

### Routes

1. **/ (Index Route)**
   - **Route**: `/{limit?3}`
   - **Controller Method**: `index()`
   - **Description**: Renders a list of messages with a configurable limit (default: 3).
   - **Template**: `hello/index.html.twig`
   - **Variables Passed**: 
     - `messages`: An array of message objects (each with 'message' and 'created' fields).
     - `limit`: The limit of messages to display (default: 3).

2. **/messages/{id} (Show One Message)**
   - **Route**: `/messages/{id<\d+>}`
   - **Controller Method**: `showOne()`
   - **Description**: Displays a single message by its ID.
   - **Template**: `hello/show_one.html.twig`
   - **Variables Passed**:
     - `message`: The message at the provided ID.

### Message Data Structure

The controller contains a sample array of messages in the form:

```php
[
    ['message' => 'Hello', 'created' => '2024/09/10'],
    ['message' => 'Hi', 'created' => '2024/07/10'],
    ['message' => 'Bye!', 'created' => '2023/08/10']
]
