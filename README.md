#  Local LLM VRAM Calculator & Discovery Tool

###  **[LIVE TOOL: Click here to use the Calculator (gpuforllm.com)](https://gpuforllm.com)**

Stop guessing if your GPU can run Llama 4 or DeepSeek V3.
This tool calculates the **exact** VRAM requirements for modern Large Language Models based on GGUF quantization standards.

##  Features

* **Engineering-Grade Math:** Accurately calculates **KV Cache** size using **GQA** (Grouped Query Attention) ratios. No more false OOM errors.
* **Smart Optimization:** If a model doesn't fit, the tool calculates the exact Context Window reduction needed to make it run on your hardware.
* **Model Discovery:** Input your GPU specs and get a list of every compatible model (Green/Yellow/Red status).
* **Latest Models (Nov 2025):** Native support for **Llama 4 (Scout/Maverick)**, **DeepSeek V2.5**, **Qwen 2.5**, **Mistral Nemo**, and **Microsoft Phi-4**.

##  How it works

Unlike basic calculators that just multiply parameters by 2, this tool accounts for:
1.  **GGUF Overhead:** Uses real-world BPW (Bits Per Weight) measurements (e.g., 4.85 bpw for Q4_K_M).
2.  **Context Window:** Calculates the memory footprint of the context using the model's specific architecture (Layers, Hidden Size, Heads, KV Heads).
3.  **System Overhead:** Reserves VRAM buffer for OS and display output to prevent crashes.

##  Usage

This is a client-side tool (HTML/JS).
You can run it locally or use the live version at **[gpuforllm.com](https://gpuforllm.com)**.

##  Contributing

* **Found a bug?** Open an Issue.
* **New model released?** Open an Issue with the `config.json` details.

*(Note: While the code is open source under MIT, the "GPUforLLM" branding, logo, and site content are the property of the creator.)*

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
**However, please link back to [gpuforllm.com](https://gpuforllm.com) if you use this logic in your own projects.**
