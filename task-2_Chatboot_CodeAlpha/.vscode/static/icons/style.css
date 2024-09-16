document.addEventListener("DOMContentLoaded", function() {
    const form = document.getElementById("question-form");
    const chatHistory = document.getElementById("chat-history");

    form.addEventListener("submit", function(event) {
        event.preventDefault(); // Prevent the default form submission

        const question = document.getElementById("question").value;
        if (question.trim() === "") return;

        // Append question to chat history
        const questionElement = document.createElement("div");
        questionElement.className = "message question";
        questionElement.innerHTML = '<img src="static/icons/user.png" class="icon" alt="You">' + question;
        chatHistory.appendChild(questionElement);

        fetch('/get_answer', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({ question: question })
        })
        .then(response => {
            if (!response.ok) {
                throw new Error('Network response was not ok ' + response.statusText);
            }
            return response.json();
        })
        .then(data => {
            // Append answer to chat history
            const answerElement = document.createElement("div");
            answerElement.className = "message answer";
            answerElement.innerHTML = '<img src="static/icons/chatbot.jpg" class="icon" alt="Chatbot">' + data.answer;
            chatHistory.appendChild(answerElement);
            chatHistory.scrollTop = chatHistory.scrollHeight;
        })
        .catch(error => {
            console.error('Error:', error);
            const errorElement = document.createElement("div");
            errorElement.className = "message answer";
            errorElement.innerHTML = '<img src="static/icons/chatbot.jpg" class="icon" alt="Chatbot">Sorry, something went wrong. Please try again.';
            chatHistory.appendChild(errorElement);
            chatHistory.scrollTop = chatHistory.scrollHeight;
        });

        form.reset(); // Clear the input field
    });
});
