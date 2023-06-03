# Dialogflow with Image Recognition

This is the README file for the final year university project on Dialogflow with Image Recognition. The project aims to develop a chatbot that can understand user queries and respond appropriately using Dialogflow's natural language processing capabilities along with image recognition.

## User Guide

To set up and use the chatbot, please follow the steps below:

### Prerequisites

1. **Install Python**: Ensure that Python is installed on your system. The chatbot's code requires Python to run.
2. **Install Visual Studio Code**: Visual Studio Code is recommended as an integrated development environment (IDE) for writing and debugging the chatbot's code.
3. **Create a Google Cloud Platform account**: Dialogflow, the cloud-based platform used for natural language processing, requires a Google Cloud Platform account. Create an account to access Dialogflow's services.
4. **Download Ngrok**: Ngrok is a tool that facilitates secure tunneling of local server traffic to the internet. Download Ngrok from [https://ngrok.com/download](https://ngrok.com/download). The chatbot uses Ngrok to communicate with external services.

### Setup

1. Clone or download the project repository and navigate to the "Chatbot FYP" folder.
2. Install the necessary libraries and packages by opening a fresh terminal window and running the following command:
   ```
   pip install -r requirements.txt
   ```

### Running the Chatbot

1. Run the `classification.py` file by executing the following command in the terminal:
   ```
   python classification.py
   ```

2. After executing the above command, you will be provided with the localhost IP address. Refer to the provided figure for an example.
3. Next, execute the following command on Ngrok, replacing "5000" with the port number being used by your device:
   ```
   ngrok http 5000
   ```

### Integrating with Dialogflow

1. Copy the forwarding URL obtained from the Ngrok CLI.
2. In the Dialogflow console, go to "Fulfillment" > "Webhook" > "URL" and paste the copied URL.
3. Append "/webhook" to the end of the URL.
4. Save the settings by clicking the "Save" button at the bottom of the screen.
5. Import the project's intents as a zip file named "chatbot" from the project directory into Dialogflow. Once imported, the intents will be visible on the Dialogflow intents page.

### Interacting with the Chatbot

1. To obtain a response from the Dialogflow chatbot, enter your question into the "Try it now" box on the right side of the screen.
2. If the chatbot's response is not satisfactory, you can refine your instructions for it on the Training page.

### Training the Image Recognition

1. If the bot is having difficulty properly classifying an image, you can train it by accessing the training page on the Dialogflow platform.
2. Review all the messages that the bot has received and check whether it has provided appropriate responses.
3. If the bot's response was correct, approve that prompt. If the bot's response was incorrect, manually review the message and URL of the image to troubleshoot the issue.
4. Approved requests on the training page are saved in the bot's intent for future image classification. This training process can also be applied to improve the bot's conversational abilities.

### Limitations

1. The chatbot's image classification capabilities are limited to the images included in its library, which can be seen in the `synset_words.txt` file.
2. If an image falls outside of the library, the chatbot will provide a default fallback response.

Please note that the chatbot's development is an ongoing process, and its capabilities can be enhanced over time through training and improvement in image classification.
