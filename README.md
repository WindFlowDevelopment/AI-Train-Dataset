# AI-Train-Dataset
AI Train Dataset (free to use for any project)

# Informations
This dataset is recommended for **training LLMs** using a Neural Network or you can also **finetune** an existing model.
This dataset is built from scratch and is **NOT DONE YET**. 100+ people are working on it and manually writing **dataset files**. Make sure that your **AI Train Structure** supports loading all .txt files from a folder.

# What your training tool MUST support
- Must support free learning so not just Input -> Output.
- Must be able to run an LLM with atleast ~ 25.000 parameters.
- Must be able to support our dataset file format.
- Must support atleast a 8k context window.
- Must support running LLMs (Not just simple chatbots)

# Tipps and Tricks
- You can copy-paste all content from here and send it to your AI agent your using and let it do the rest.
- We highly recommend to have a good GPU. But CPU is also okay.

# AI Context History
Format to follow if you want to train the AI so it can continue chatting:
[Click Me](contextformat.txt)
- Leave an empty line -> Hello! -> Hello! How can I help you today?  After that -> empty line -> then the next question.
- To implement history / context type [Previous: Example] Hey!
Line below: Hey again! You keep saying hello.
- [Previous: Hello] checks for, if the last response by the LLM included the word / part "Hello" exactly like there, if included and the content after the [] content is written after the Previous value then the AI should say that.
EXAMPLE:
```
[Previous: Hello!] Hello!
Hello again! You keep saying hello. What can I do for you?
```
- In this example, this chat would happen:
```
User: Hello!
AI: Hello! What can I do for you?
User: Hello!
AI: Hello again! You keep saying hello. What can I do for you?
```

# Same Training Data multiple times
### IMPORTANT:
- If the training file includes the following:
```
Hello!
How can I help you today?

Hello!
What can I do for you?
```
- then the AI chooses ONE of the available options, if [Previous] is included, it still works with both options, so don't worry about that.
- We would recommend that your training tool supports atleast ~ 250 repeats on same thing for best quality.

# Training - Parameters
### Recommended Parameters:
| Parameters   | Purpose        |
|--------|-------------|
| 25.000  | Small LLM for smalltalks   |
| 50.000    | Small LLM for testing small coding features or smalltalks    |
| 100.000  | Small LLM for testing code features or talking about some things     |
| 200.000 | Medium LLM for medium tasks with smarter outputs |
| 500.000 | Medium LLM for bigger medium tasks with alot of smarter outputs |
| 1.000.000 | Big Medium LLM for general coding tasks, debugging or chatting |
| 5.000.000 | Big Medium LLM for general coding tasks, debugging or chatting |
| 15.000.000 | Big Medium LLM for medium coding tasks with ALOT of smarter outputs |
| 30.000.000 | Big Medium LLM for medium coding tasks with ALOT of smarter outputs |
| 100.000.000 | Full LLM for big coding tasks with ALOT of smarter outputs and reasoning tasks |
| 1B+ | Brutally LLM for very large coding tasks, very hard tasks, complex questions |