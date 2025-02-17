# Create Custom Models with LLaMA 

## Overview
By using this model file, you can create any custom model based on an existing LLaMA model. In this project, we demonstrate how to create a Mario-themed AI model. This approach allows for the customization of responses, persona development, and specialized AI behavior.

## Prerequisites
Before proceeding, ensure you have the following installed:

- **Python 3.8+**
- **Ollama**
- **LLaMA 3.2 or any LLaMA model**
- **A model system file** (to define your own model theme)

## Installation
Follow these steps to set up the project:

### Step 1: Download and Install Ollama
```sh
 curl -fsSL https://ollama.ai/install.sh | sh
```

### Step 2: Pull the LLaMA 3.2 Model
```sh
 ollama pull llama3.2
```

### Step 3: Clone the Repository
```sh
 git clone https://github.com/techwithtim/OllamaTutorial.git
 cd OllamaTutorial
```

### Step 4: Create Your Custom Model
```sh
 ollama create <model-name> -f ./ModelFile
 # Change <model-name> with your desired model name
```

### Step 5: Run the Model
```sh
 ollama run <model-name>
```

## Usage
After running the model, you can interact with it through the command line or integrate it into an application.

- **Example Query:**
```sh
 Mario: "What do you think of Bowser?"
```

- **Expected Output:**
```sh
 "It's-a me, Mario! Bowser is always causing trouble, but I'll save the day!"
```

## Configuration
Modify the `ModelFile` to change system behavior, persona, or other model parameters.

### Sample ModelFile:
```sh
# Use LLaMA 3.2 as the base model
FROM llama3.2

# Set the temperature to 1 (higher is more creative, lower is more coherent)
PARAMETER temperature 1

# Set the system message
SYSTEM """
You are Mario from Super Mario Bros. Answer as Mario, the assistant, only.
"""
```

## Troubleshooting
If you encounter issues:

1. **Ensure all dependencies are installed correctly.**
2. **Check if Ollama is running properly.**
3. **Verify the model file is correctly formatted.**

## License
This project is released under the MIT License.

---

Create and customize your own AI models effortlessly!