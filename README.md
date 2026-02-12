# Simple-Chatbot-with-Open-Source-LLMs
Create Simple Chatbot with Open Source LLMs using Python and Hugging Face

Chatbots use a special kind of computer program called a transformer, which is like its brain. Inside this brain, there is something called a language model (LLM), which helps the chatbot understand and generate human-like responses. It deciphers many examples of human conversations it has seen prior to responding in a sensible manner.

Transformers and LLMs work together within a chatbot to enable conversation. Here's a simplified explanation of how they interact:

Input processing: When you send a message to the chatbot, the transformer helps process your input. It breaks down your message into smaller parts and represents them in a way that the chatbot can understand. Each part is called a token.

Understanding context: The transformer passes these tokens to the LLM, which is a language model trained on lots of text data. The LLM has learned patterns and meanings from this data, so it tries to understand the context of your message based on what it has learned.

Generating response: Once the LLM understands your message, it generates a response based on its understanding. The transformer then takes this response and converts it into a format that can be easily sent back to you.

Iterative conversation: As the conversation continues, this process repeats. The transformer and LLM work together to process each new input message, understand the context, and generate a relevant response.

The key is that the LLM learns from a large amount of text data to understand language patterns and generate meaningful responses. The transformer helps with the technical aspects of processing and representing the input/output data, allowing the LLM to focus on understanding and generating language.

Once the chatbot understands your message, it uses the language model to generate a response that it thinks will be helpful or interesting to you. The response is sent back to you, and the process continues as you have a back-and-forth conversation with the chatbot.

## Step 1: Installing requirements
Follow these steps to create a Python virtual environment and install the necessary libraries. Open a new terminal first.
Set up your virtual environment:
  pip3 install virtualenv 
  virtualenv my_env # create a virtual environment my_env
  source my_env/bin/activate # activate my_env

For this example, you will be using the transformers library, which is an open-source natural language processing (NLP) toolkit with many useful features, and also let's install a torch library.
  python3 -m pip install transformers==4.30.2 torch

## Step 2: Import our required tools from the transformers library
  For this example, we will be using AutoTokenizer and AutoModelForSeq2SeqLM from the transformers library.
## Step 3: Choosing a model  
  Choosing the right model for your purposes is an important part of building chatbots! You can read on the different types of models available on the Hugging Face website: https://huggingface.co/models.
  LLMs differ from each other in how they are trained. Let's look at some examples to see how different models fit better in various contexts.  
    Text generation:
    If you need a general-purpose text generation model, consider using the GPT-2 or GPT-3 models. They are known for their impressive language generation capabilities.
    Example: You want to build a chatbot that generates creative and coherent responses to user input.
    
    Sentiment analysis:
    For sentiment analysis tasks, models like BERT or RoBERTa are popular choices. They are trained to understand the sentiment and emotional tone of text.
    Example: You want to analyze customer feedback and determine whether it is positive or negative.
    
    Named entity recognition:
    LLMs such as BERT, GPT-2, or RoBERTa can be used for Named Entity Recognition (NER) tasks. They perform well in understanding and extracting entities like person names, locations, organizations, etc.
    Example: You want to build a system that extracts names of people and places from a given text.
    
    Question answering:
    Models like BERT, GPT-2, or XLNet can be effective for question-answering tasks. They can comprehend questions and provide accurate answers based on the given context.
    Example: You want to build a chatbot that can answer factual questions from a given set of documents.
    
    Language translation:
    For language translation tasks, you can consider models like MarianMT or T5. They are designed specifically for translating text between different languages.
    Example: You want to build a language translation tool that translates English text to French.
  
  However, these examples are very limited and the fit of an LLM may depend on many factors such as data availability, performance requirements, resource constraints, and domain-specific considerations. It's important to explore different LLMs thoroughly and experiment with them to find the best match for your specific application.
  Other important purposes that should be taken into consideration when choosing an LLM include (but are not limited to):    
    Licensing: Ensure you are allowed to use your chosen model the way you intend
    Model size: Larger models may be more accurate, but might also come at the cost of greater resource requirements
    Training data: Ensure that the model's training data aligns with the domain or context you intend to use the LLM for
    Performance and accuracy: Consider factors like accuracy, runtime, or any other metrics that are important for your specific use case
    To explore all the different options, check out the available models on the Hugging Face website.

## Step 4: Fetch the model and initialize a tokenizer
  Here, we initiate variables using two handy classes from the transformers library:
    model is an instance of the class AutoModelForSeq2SeqLM, which allows you to interact with your chosen language model.
    tokenizer is an instance of the class AutoTokenizer, which optimizes your input and passes it to the language model efficiently. It does so by converting your text input to “tokens”, which is how the model interprets the text.

## Step 5: Chat
  Step 5.1: Keeping track of conversation history
  Step 5.2: Encoding the conversation history
  Step 5.3: Fetch prompt from user
  Step 5.4: Tokenization of user prompt and chat history
  Step 5.5: Generate output from the model
  Step 5.6: Decode output
  Step 5.7: Update conversation history
  Step 6: Repeat
