# Chat-Ubuntu-Gguf
- Status: Alpha

### Project Details
The Reinvention of my WSL based ChatBot....
- Programmed towards Gguf models only, maintained in "./models"; The model must now have a relating "./models/model_config.json" (useually supplied with the model). the program needs to scan this folder upon start, and utilize whatever model is there.
- Gradio Interface is in runspace, and main scripts return to bash upon exit, and exiting the menu on the bash will shutdown all required things. the bash identifies the process upon launching the gradio interface; so long as people follow logical exit, then it will correctly close the gradio process in runspace). 
- additional scripts are generated as required, and placed in data folder, such as the yaml for persistent settings.
- we have 5 python scripts in total between "./" and "./scripts" and "./data", plus the bash script, and the rest, generates, such as the yaml or required folders.
- the main_script checking relevant folders for required files and performing any required basic maintenance, all before popping up the gradio interface in browser.

### Project Plans
1. Attempt to make the current scripts work flawlessly.
2. work on modular features, ie, voice/image recognition and voice/image genearion. 

### FEATURES
- Optimized code, 5 main scripts, creation of required folders.
- Running only with single GGUF model, featuring llama python.
- Terminal and Gradio interface.
- Memory Awareness and Optimized threading.
- Continuous interactive user loop in Gradio Interface.
- Intelligent, context-aware response generation with summary.
- YAML state management for persistent settings, names and roles.
- VENV - It uses a virtual environment in a "./venv" folder.
- BASH - Bash Launcher-Installer for convinience. 

### Example Prompts
1) "Hello there! I never thought I would see you here on the mountain..."
2) "Wow, you can actually talk? What's your story?"
3) "You look wise, do you have any ancient wisdom to share?"
4) "Tell me, Wise-Llama, what is the purpose of humanity?"

### Requirements
- Ubuntu - Its programmed on/towards Ubuntu 24.04-24.10.
- Python - It uses modern versions of Python in a VENV.
- LLMs in GGUF format; testing on "Llama-3.1-Unhinged-Vision-8B-GGUF".
- AMD - Programmed on AMD, not currently tested on other platforms.

### Usage
- No working version verified yet.

## DISCLAIMER:
- Refer to License.Txt for terms covering usage, distribution, and modifications.
