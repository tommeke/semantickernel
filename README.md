# semantic kernel testing

## introduction

Simple testing of LLMs with Semantic kernel in C#, based on Ollama LLM manager.
Ollama allows you to install and interface with "small" LLMs like Phi3, Llamma 2 and 3, mistral, etc...

Once Ollama is installed and serving some simple LLMs (through standard local openAI REST api), Semantic Kernel is used to interact with these LLMs

## Install Ollama and setup some simple small LLMs

In linux or wsl, install Ollama:

'''
curl -fsSL https://ollama.com/install.sh | sh
'''
