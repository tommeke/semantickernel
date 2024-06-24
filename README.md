# semantic kernel testing

## introduction

Simple testing of LLMs with Semantic kernel in C#, based on Ollama LLM manager.
Ollama allows you to install and interface with "small" LLMs like Phi3, Llamma 2 and 3, mistral, etc...

Once Ollama is installed and serving some simple LLMs (through standard local openAI REST api), Semantic Kernel is used to interact with these LLMs

## Install Ollama and setup some simple small LLMs

In linux or wsl, install Ollama:

```curl -fsSL https://ollama.com/install.sh | sh```

start the Ollama service:

```ollama serve```

download and run a small LLM (probably will need to do in seperate terminal if the serve command wasn't run in background mode):

```ollama run phi3```

This will first download the model and start it up. Ollama will present you a prompt interface with which you can interact immediately with the loaded LLM.
Some other LLMs available (check the Ollama website for a more extensive list: https://ollama.com/models , https://github.com/ollama/ollama ): 
- mistral
- llama2-uncensored
- llama3
- llama3:70b
- phi3:medium

The Ollama REST API should now be listening on http://127.0.0.1:11434 , so you can just use that uri to connect to it through Semantic Kernel.

## Semantic Kernel

Currently just a simple example in C# is present that connects to a local running LLM through the Semantic Kernel Framework. It requires dotnet 8 and the dotnet package Microsoft.SemanticKernel.
On the command line, navigate to the clone of the project and add Semantic Kernel package:
```dotnet add package Microsoft.SemanticKernel```
Next build it:
```dotnet build```
Next navigate to the .\llms\ folder, and run it:
```dotnet run```
