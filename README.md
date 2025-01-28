def chatbot_response(user_input):
    # Predefined responses
    responses = {
        "hello": "Hi there! How can I help you today?",
        "how are you": "I'm just a bunch of code, but I'm doing great! How about you?",
        "what is your name": "I'm your friendly chatbot.",
        "bye": "Goodbye! Have a nice day!"
    }

    # Normalize user input
    normalized_input = user_input.lower()

    # Check for a match
    for key in responses:
        if key in normalized_input:
            return responses[key]

    # Default response
    return "I'm sorry, I didn't understand that. Can you please rephrase?"

# Main loop
while True:
    user_input = input("You: ")
    if user_input.lower() in ["exit", "quit"]:
        print("Chatbot: Goodbye!")
        break
    print("Chatbot:", chatbot_response(user_input))
