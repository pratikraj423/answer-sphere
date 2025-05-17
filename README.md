# answer-sphere

// html code  
<!-- // THE INSTRUCTIONS THAT ARE FULL FILL BY ANSWER SPHERE:-


hello          
who are you 
HOW ARE YOU
news
quotes
weather
bye
FOR OPEN LINK:-
open instagram
open youtube
open linkedin
open facebook
open twitter
OPEN spotify
open chatgpt 
open vscode
open chrome
open google
open whatsapp 
for better output you can copy from here -->


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ChatGPT Clone</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>ANSWER SPHERE !</h1>
        <h2>Chat with AI</h2>
        <div class="chat-container" id="chatContainer">
            <!-- Chat messages will appear here -->
        </div>
        <div class="prompt-area">
            <input type="text" id="userInput" placeholder="Type your message..." />
            <button class="btn" onclick="sendMessage()">Send</button>
        </div>
        <!-- Pratik's Name in Top-Right Corner -->
        <div class="name-container">
            <p>Pʀᴀᴛɪᴋ ꜱᴘʜᴇʀᴇ𝗫   </>
        </div>
    </div>

    <script src="app.js"></script>
</body>
</html>




// CSS


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

body {
    width: 100%;
    height: 100%;
    background-color: rgb(27, 33, 41);
}

.container {
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 20px;
    padding-top: 100px;
}

.container h1 {
    display: inline-block;
    font-size: 7vw;
    background: linear-gradient(to right, white, rgb(45, 183, 225), rgb(196, 14, 93));
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.container h2 {
    font-size: 3vw;
    color: rgb(241, 241, 241);
}

.chat-container {
    width: 100%;
    max-height: none; /* Allow the chat container to grow infinitely */
    overflow-y: auto;
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-bottom: 80px; /* Add some space for input */
}

.chat-message {
    padding: 15px;
    border-radius: 15px;
    font-size: 16px;
    max-width: 80%;
    word-wrap: break-word;
}

.user-message {
    background-color: rgb(96, 136, 173);
    align-self: flex-end;
    color: white;
}

.ai-message {
    background-color: rgba(120, 169, 215, 0.7);
    align-self: flex-start;
    color: white;
}

.prompt-area {
    width: 100%;
    background-color: rgb(27, 33, 41);
    padding: 10px;
    position: fixed;
    bottom: 0;
    display: flex;
    justify-content: center;
}

#userInput {
    width: 70%;
    padding: 10px;
    border-radius: 20px;
    border: 2px solid #ccc;
    font-size: 16px;
    margin-right: 10px;
    color: white;
    background-color: rgb(27, 33, 41);
}

.btn {
    width: 15%;
    padding: 10px;
    background-color: rgb(10, 183, 235);
    color: white;
    border-radius: 20px;
    border: none;
    cursor: pointer;
}

.btn:hover {
    background-color: rgba(14, 122, 155, 0.7);
}

/* Added Styles to Position Name in Right-Top Corner */
.name-container {
    position: absolute;
    top: 30px; /* Positioned at the top */
    right: 30px; /* Positioned to the right */
    font-size: 2vw;
    font-weight: bold;
    color: #f1f1f1;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.8), 0 0 20px rgba(45, 183, 225, 0.8);
}

#name {
    animation: glow 1.5s ease-in-out infinite alternate;
}

@keyframes glow {
    0% { text-shadow: 0 0 5px rgba(255, 255, 255, 0.8); }
    100% { text-shadow: 0 0 20px rgba(255, 165, 0, 0.9), 0 0 30px rgba(30, 144, 255, 0.9); }
}

JAVA 

// Get elements
const chatContainer = document.getElementById("chatContainer");
const userInput = document.getElementById("userInput");

// Function to send a message
function sendMessage() {
    const message = userInput.value.trim();
    if (message === "") return; // Ignore if the message is empty

    // Append the user message to the chat container
    const userMessageDiv = document.createElement("div");
    userMessageDiv.classList.add("chat-message", "user-message");
    userMessageDiv.textContent = message;
    chatContainer.appendChild(userMessageDiv);

    // Clear the input field
    userInput.value = "";
    chatContainer.scrollTop = chatContainer.scrollHeight; // Scroll to the bottom

    // Simulate AI response
    setTimeout(() => {
        const aiMessageDiv = document.createElement("div");
        aiMessageDiv.classList.add("chat-message", "ai-message");
        aiMessageDiv.textContent = getAIResponse(message);
        chatContainer.appendChild(aiMessageDiv);
        chatContainer.scrollTop = chatContainer.scrollHeight; // Scroll to the bottom
    }, 1000); // Simulate a 1-second delay for the AI response
}

// Simulated AI response and opening links
function getAIResponse(message) {
    const lowerMessage = message.toLowerCase();

    if (lowerMessage.includes("hello")) {
        return "Hello user ! How can I assist you today?";
    } else if (lowerMessage.includes("how are you")) {
        return "I'm just a AI assistant, but I'm doing well, thanks for asking!";
    } else if (lowerMessage.includes("who are you")) {
        return "I am an AI assistant created by Pʀᴀᴛɪᴋ ꜱᴘʜᴇʀᴇ𝗫 to assist you with tasks and answer questions.";
    } else if (lowerMessage.includes("help")) {
        return "I can help you with opening websites, answering questions, and providing information!";
    } else if (lowerMessage.includes("your name")) {
        return "I don't have a specific name, but you can call me Pʀᴀᴛɪᴋ ꜱᴘʜᴇʀᴇ𝗫 ";
    } else if (lowerMessage.includes("thank you")) {
        return "You're welcome! Feel free to ask if you need anything else.";
    } else if (lowerMessage.includes("bye")) {
        return "Goodbye! Have a great day!";
    } else if (lowerMessage.includes("youtube")) {
        window.open("https://www.youtube.com", "_blank");
        return "Opening YouTube for you!";
    } else if (lowerMessage.includes("chrome")) {
        window.open("https://www.google.com/chrome/", "_blank");
        return "Opening Chrome download page!";
    } else if (lowerMessage.includes("chatgpt")) {
        window.open("https://chat.openai.com", "_blank");
        return "Opening ChatGPT for you!";
    } else if (lowerMessage.includes("facebook")) {
        window.open("https://www.facebook.com", "_blank");
        return "Opening Facebook for you!";
    } else if (lowerMessage.includes("twitter")) {
        window.open("https://www.twitter.com", "_blank");
        return "Opening Twitter for you!";
    } else if (lowerMessage.includes("instagram")) {
        window.open("https://www.instagram.com", "_blank");
        return "Opening Instagram for you!";
    } else if (lowerMessage.includes("google")) {
        window.open("https://www.google.com", "_blank");
        return "Opening Google for you!";
    } else if (lowerMessage.includes("spotify")) {
        window.open("https://www.spotify.com", "_blank");
        return "Opening Spotify for you!";
    } else if (lowerMessage.includes("whatsapp")) {
        window.open("https://www.whatsapp.com", "_blank");
        return "Opening WhatsApp for you!";
    } else if (lowerMessage.includes("weather")) {
        return "I can't provide live weather updates, but you can check the weather on websites like Weather.com!";
    } else if (lowerMessage.includes("news")) {
        return "For the latest news, you can visit websites like BBC News or CNN.";
    } else if (lowerMessage.includes("joke")) {
        return "Why don't skeletons fight each other? They don't have the guts!";
    } else if (lowerMessage.includes("quote")) {
        return "'The only way to do great work is to love what you do.' - Steve Jobs";
    } else if (lowerMessage.includes("vs code") || lowerMessage.includes("vscode")) {
        window.open("https://code.visualstudio.com", "_blank");
        return "Opening Visual Studio Code for you!";
    } else {
        return "Sorry, I didn't quite get that. Can you ask something else?";
    }
}

