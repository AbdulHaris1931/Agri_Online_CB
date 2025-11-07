# Agri_Online_CB

🌾 AgriChat – AI-Powered Agricultural Assistant
📘 Overview

AgriChat is an intelligent chatbot fine-tuned on the TinyLlama 1.1B model to answer agriculture-related questions.
It uses LoRA (Low-Rank Adaptation) for efficient fine-tuning and features an interactive Gradio chat interface for real-time conversations.

🎯 Objective

To build an AI-powered agricultural assistant that provides accurate, quick, and contextual answers to farmers, students, and researchers in the agriculture domain.

⚙️ Features

✅ Fine-tuned on 300+ agriculture Q&A pairs
✅ Supports crop science, soil, irrigation, fertilizers, pests, and more
✅ LoRA fine-tuning for low-resource hardware (T4 GPU)
✅ Interactive Gradio-based chat UI
✅ Fallback mode (works even without LoRA weights)
✅ Option to download chat history

🧩 Tech Stack
Category	Tools / Libraries
Base Model	TinyLlama-1.1B-Chat
Fine-Tuning	LoRA (PEFT)
Frameworks	Transformers, Datasets, Accelerate
Interface	Gradio
Platform	Google Colab
Language	Python
🗂️ Project Structure
📂 AgriChat_Project
 ┣ 📄 train_lora.py                   # Training script
 ┣ 📄 instructions.jsonl              # Custom dataset (300+ Q&A)
 ┣ 📄 llm_lora_tiny_agri_chat_colab.ipynb  # Full training notebook
 ┣ 📄 agri_chat_tiny_fixed_prompt_colab.ipynb  # Final working chatbot
 ┣ 📄 agri_chat_tiny_fallback_colab.ipynb      # Fallback chat version
 ┗ 📄 README.md

🚀 How to Run the Project
Option 1: Train Your Model

Open llm_lora_tiny_agri_chat_colab.ipynb in Google Colab.

Upload the dataset (instructions.jsonl).

Set runtime → GPU → Save.

Run all cells to fine-tune the model.

Once complete, LoRA adapter is saved in ./outputs/lora_adapter.

Option 2: Chat with Your Model

Open agri_chat_tiny_fixed_prompt_colab.ipynb.

If ./outputs/lora_adapter exists, it loads automatically.

Start chatting via the Gradio interface.

Use 💾 “Download Chat History” to save your conversation.

🧠 Example Interactions

User: What is organic farming?
AgriChat: Organic farming avoids synthetic fertilizers and promotes natural soil fertility.

User: Explain drip irrigation.
AgriChat: Drip irrigation delivers water directly to the root zone through emitters, saving water.

📊 Results

Model fine-tuned successfully on 300+ agricultural questions.

Produces short, accurate, and context-specific answers.

Runs on free Google Colab GPU (TinyLlama 1.1B).

💡 Future Enhancements

Add multilingual support (Tamil, Hindi, etc.)

Expand dataset to 1,000+ agricultural Q&A pairs

Deploy the chatbot publicly on Hugging Face Spaces

Add voice input/output
