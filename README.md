# LLM Classifier

This is an example of using [function calling](https://anth.us/blog/how-ai-agents-do-things/) to transform unstructured input into structured data.  In this case, a binary classifier, mirroring the ML text classifiers that we [recently demonstrated](https://anth.us/blog/maximize-profit-not-intelligence/).

In this example, we only send one request to the LLM instead of sending the second request with the results of the function.  In this use case the only thing that we want from the model is a response in a predictable, structured format.

We do that by setting up one tool that accepts one required parameter: A boolean value: true or false.  This is the structured data that we want.

We're using the LLM as a reasoning engine to decide that it should call the tool, since the prompt explicitly tells it to use the tool.  And to classify the sentence so that it can provide the required parameter.