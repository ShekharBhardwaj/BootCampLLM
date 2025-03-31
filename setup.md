

# AI Environment Setup Guide

Setting up a powerful environment to work at the forefront of AI isn’t as straightforward as it could be. For most people, these instructions will work smoothly, but occasionally, issues arise. If you encounter any problems, please reach out—I’m here to help you get up and running quickly. Nothing is worse than feeling _stuck_. You can message me, email me, or send a LinkedIn message, and I’ll help you out.

I recommend using **Anaconda** to set up your environment. It’s a comprehensive tool that ensures compatibility by managing Python versions and packages consistently across different systems. Though it requires more time and hard drive space (5+ GB), it’s incredibly reliable once set up.

If you encounter issues with Anaconda, I’ve provided an alternative approach that’s faster and simpler, though it offers less compatibility assurance.

---

## Part 1: Clone the Repo

This step gets you a local copy of the code on your machine.

### 1. Install Git (if not already installed)

- Open Terminal (`Applications > Utilities > Terminal`)
- Type `git --version`. If not installed, you'll be prompted to install it.

### 2. Navigate to your projects folder:
```bash
cd ~/Documents/Projects
```
If this folder doesn’t exist, create it:
```bash
mkdir ~/Documents/Projects
cd ~/Documents/Projects
```

### 3. Clone the repository:
```bash
git clone https://github.com/ShekharBhardwaj/BootCampLLM.git
```
This will create a new directory named `BootCampLLM`. Navigate to it with:
```bash
cd BootCampLLM
```
This directory is known as the "project root directory."

---

## Part 2: Install Anaconda Environment

If you encounter issues with Anaconda, skip to **Part 2B** for an alternative approach.

### 1. Install Anaconda:
- Download from [Anaconda Install Guide](https://docs.anaconda.com/anaconda/install/mac-os/).
- Follow the installation prompts (this may take several GB of space and time).

### 2. Set up the environment:
```bash
cd ~/Documents/Projects/BootCampLLM  
conda env create -f environment.yml
```
This process can take up to 30 minutes. Once complete, activate your environment with:
```bash
conda activate llms
```
You should see `(llms)` in your prompt, indicating the environment is active.

### 3. Start Jupyter Lab:
```bash
jupyter lab
```
This will open Jupyter Lab in your browser. You’re ready to proceed.

---

## Part 2B: Alternative Setup (if Anaconda Fails)

### 1. Install Python:
- Ensure you’re using Python 3.11.
```bash
python --version
```
- Download from [Python Downloads](https://www.python.org/downloads/).

### 2. Set up a virtual environment:
```bash
python -m venv llms
source llms/bin/activate  # For MacOS/Linux
llms\Scripts\activate    # For Windows
```
You should see `(llms)` in your prompt.

### 3. Install dependencies:
```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Start Jupyter Lab:
```bash
jupyter lab
```

---

## Part 3: OpenAI Key (OPTIONAL but Recommended)

For Week 1, you’ll only need an OpenAI API key. Future weeks may require others.

### 1. Create an OpenAI account:  
- Visit [OpenAI Platform](https://platform.openai.com/).

### 2. Add credit:  
- Minimum is $5. API calls will spend against this balance. Disable auto-recharge if preferred.

### 3. Create your API key:  
- Generate a key at [OpenAI API Keys](https://platform.openai.com/api-keys).
- Store your key safely; it won’t be retrievable from OpenAI later.

---

## Part 4: .env File

Create a `.env` file in your project root directory to store API keys.

### 1. Create the file:
```bash
nano .env
```
Add your keys like this:
```
OPENAI_API_KEY=xxxx
GOOGLE_API_KEY=xxxx
ANTHROPIC_API_KEY=xxxx
HF_TOKEN=xxxx
```
Save and exit (Ctrl + O, Enter, Ctrl + X).

### 2. Confirm the file exists:
```bash
ls -a
```

---

## Part 5: Showtime!

### 1. Activate your environment:
```bash
conda activate llms
```
Or, if you used the alternative setup:
```bash
source llms/bin/activate
```

### 2. Launch Jupyter Lab:
```bash
jupyter lab
```

And you’re ready to go! If you encounter issues reach out to me.

Happy coding!

