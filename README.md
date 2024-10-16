# Chat-UbuntuLlama
- Converting windows python chatbot, to optimized use on Ubuntu. Still Getting the scripts done currently.

### Planner:
- It will be optimized towards AVX2 and Non-Rocm AMDGPU, at least to start with.
- It will feature better libraries, only available on linux python.
- a new optional window for data visualization using plotly. I should use a gradio interface for the chat interactions, while engine window remains straight terminal.

### Details:
- Below is old content, that will be in some stage of update in project conversion from Chat-VulkanLlama...


```
# CURRENT STATUS: Development... 
- Test and fix scipts.
- Explore GPU load testing: if we can obtain the gpu load average over say a 2-3 second period, then threads to use could be auto/dynamic, calculate "(100/totalthreads)*(%cpufree - 10) = threads to use", so as to have a safe amount of threads within the free cpu % converted into theoretically relating number of threads. for example, if 20% of the processor was in use, then 80%-10% would be 70%, so for a 10 thread processior it would be or 7/10 threads to use, the theoretical free number of threads.
- creation of gradio interfaces, for chat and engine windows. Engine window (Window_1) should have gradio interface, where the window should be displaying the normal engine printed text output in a text box, the second tab should be top half is configuration of model parameters and model name etc, all maintained in globals with a reset button to save the globals to the json and restart with a re-load of the model into ram with the new parameters. Chat Window (Window_2) also with gradio interface, should be the main chat interface, and on page 2 the roleplay configuration, player name npc name etc, and when settings are changed there then it will just be using those settings when the user next submits their response with the submit button on the chat interface. 
- Allow user to assign syntax presets to models (ah thats what the maps are for!).

### DESCRIPTION:
- Enhancing my Llama-based Python chatbot. Currently the plan is llama-cpp-vulkan pre-compiled binaries for context-aware conversations, building upon my previous Llama2 RP Chatbot. Now Compatible with Windows Only, but it also does not require WSL anymore either, and its got vulkan, AND it uses my new flashy batch code to detect where, 7-Zip and Python and Pip, are installed. If I didnt drop linux to streamline, I would not even be able to consider a gradio interface, that is coming next hopefully.

### FEATURES:
- Optimized code, 5 main scripts, creation of required folders.
- Testing only with GGUF models, working towards llama3.
- TTS and sound integration.
- Multi-window interface running parallel scripts.
- Context support from 4K, 8K. 16K, models.
- Dynamic model initialization with optimized threading.
- Continuous interactive user loop.
- Intelligent, context-aware response generation.
- Model response rotation for varied dialogue.
- YAML state management for persistent settings.

### INTERFACE:
- **Window 1:** Title screen with fortune cookie wisdom.
- **Window 2:** Roleplay summary, showing inputs, responses, and event history.

### USAGE (Windows):
1) Download and extract the package to a suitable folder, like "D:\Programs\Chat-VulkanLlama\", a path without spaces is always a better idea in general for GitHub projects.
2) Install dependencies via `Installer.Bat`, if you get errors, then either you, installed 7-Zip to an unusual folder, or otherwise you need to, turn your firewall off temporarely or make a rule to allow (I dont advise the second, as its for cmd).
3) Place a GGML model in `./models`, later on there will be selection from models library or something.. 
4) Launch with `Launcher.Bat`, by default, sounds and text to speach are ON, edit arguments in `Launcher.bat`. Optionally resize window with Ctrl + scroll mouse.

### USAGE (Linux):
- Download and use "LlmCppPyBot_v1p07", and some earlier ones, they possibly have linux compatibility, but I was never able to test this. So probably don't.

### CODE INFO:
- Main scripts: `window_1.py`, `window_2.py`.
- Utilities: `utility.py`, `model.py`, `interface.py`.

### TEST PROMPTS:
1) "Hello there! I never thought I would see you here on the mountain..."
2) "Wow, you can actually talk? What's your story?"
3) "You look wise, do you have any ancient wisdom to share?"
4) "Tell me, Wise-Llama, what is the purpose of humanity?"

### REQUIREMENTS:
- Windows 8-11 - The official Python 3.9 wont run on earlier versions of windows, but the batches will. Though if need be, then earlier versions of python can be installed/used see below.
- Python 3.9 non-Wsl (libraries `./data/requirements.txt`). Want to try other versions, then change "Python39" in the batch files to say "Python310", or whatever, in all cases. It will find it unless its in a wierd location.
- Large Language Models in Llama 3 GGUF format, I advise "L3-8B-Stheno-v3.2-GGUF-IQ-Imatrix", 8B is probably Optimal, the better q3s and most q4s, will be able to handle the text processing prompts.

### FUTURE PLANS:
2) Implement AI-generated theme prompts, to generate the rp aspects, such as random meetings, etc.
3) Explore integrating stable diffusion models for AI-generated maps and scenarios, there are some in gguf. If maps were able to be generated, and the user types in the name of the place to go, then little else need be done other than 

## DISCLAIMER:
- Refer to License.Txt for terms covering usage, distribution, and modifications.
```

### Notes:
- Its not possible to convert batch scripts into bash scripts over the original file; bash scripts must be made in linux from the start, or they wont execute correctly.
