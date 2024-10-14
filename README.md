# Simple chatbot using if-else statements

def chatbot_response(user_input):
    # Convert the user input to lowercase to handle case-insensitivity
    user_input = user_input.lower()
    
    # Responses based on keywords
    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I assist you today?"
    
    elif "how are you" in user_input:
        return "I'm just a bot, but I'm doing great! How about you?"
    
    elif "your name" in user_input:
        return "I am a simple chatbot created to help with basic tasks."
    
    elif "time" in user_input:
        return "I'm not equipped to tell the time, but you can check your device's clock."
    
    elif "bye" in user_input or "goodbye" in user_input:
        return "Goodbye! Have a great day!"
    
    else:
        return "Sorry, I don't understand that. Can you please rephrase?"

# Chatbot interaction loop
print("Chatbot: Hi! You can ask me anything. Type 'bye' to end the conversation.")

while True:
    user_input = input("You: ")
    
    if "bye" in user_input.lower():
        print("Chatbot: Goodbye! Have a great day!")
        break
    
    # Get the chatbot's response
    response = chatbot_response(user_input)
    print(f"Chatbot: {response}")

       
