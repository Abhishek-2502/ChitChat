# ChitChat - AI Chatbot App

ChitChat is an Android application that uses OpenAI's GPT API to create an interactive chatbot. It allows users to send prompts and receive AI-generated responses directly within the app. This application features a sleek user interface with a smooth and responsive chat experience.

## Table of Contents

- [Features](#features)
- [Images](#images)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Code Walkthrough](#code-walkthrough)
- [API Integration](#api-integration)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Author](#author)


## Features

- Simple and user-friendly interface.
- Real-time chat functionality using OpenAI's GPT-3.5-turbo API.
- Displays AI responses in a conversational format.
- Typing indicator for bot responses.
- Status bar customization to blend with the app's theme.
- RecyclerView implementation for an optimized chat experience.

## Images
<img src="screenshots/Screenshot_2024-08-26-17-45-43-05_9a3c0f303d55a4678b3df58d675dc03a.jpg" alt="App Screenshot" width="250"/>

## Installation

1. Clone this repository to your local machine.
   ```
   git clone https://github.com/your-repo/chitchat.git
   ```

2. Open the project in Android Studio.

3. Ensure you have the required dependencies added in your `build.gradle` files:
   ```gradle
   dependencies {
       implementation 'com.squareup.okhttp3:okhttp:4.9.1'
   }
   ```

4. Obtain an API key from [OpenAI](https://beta.openai.com/signup/).

5. Add your OpenAI API key in the `callAPI` method:
   ```java
   String api = "YOUR_API_KEY_HERE";
   ```

6. Build and run the app on your Android device or emulator.

## Usage

1. Upon launching the app, you are greeted with a clean chat interface.

2. Enter a prompt or question in the input field and press the send button (paper plane icon).

3. The app will display a "Typing..." indicator while awaiting a response from the API.

4. Once the response is received, it will be displayed in the chat interface.

## Technologies Used

- **Java**: For implementing the business logic.
- **OkHttp**: To handle network requests.
- **RecyclerView**: To display messages in a list format.
- **OpenAI API**: To integrate ChatGPT responses.
- **JSON**: For formatting API requests and handling responses.
- **Android EdgeToEdge**: To provide immersive UI by handling system bars insets.

## Code Walkthrough

- **MainActivity.java**: This is the core activity where all major interactions happen. It handles:
  - Setting up the chat interface.
  - Sending the prompt to OpenAI's API and displaying the response.
  - Using `OkHttp` to send HTTP POST requests with the user input.
  
- **MessageAdapter.java**: This adapter connects the message data (both user and bot messages) to the `RecyclerView` for display.

- **Message.java**: A simple class that represents a message object with properties like `message` and `sentBy` (user or bot).

## API Integration

- The app sends a POST request to the OpenAI API endpoint `/v1/chat/completions` with the user's prompt, API model, temperature, and token limit.

- On success, it parses the JSON response to extract the bot's reply and displays it in the chat.

## Future Enhancements

- Add support for multiple language models.
- Improve the design of the chat interface with user avatars.
- Implement voice input and output functionality for hands-free interaction.
- Add persistent chat history.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Abhishek Rajput

