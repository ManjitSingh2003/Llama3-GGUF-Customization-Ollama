# **Customizing and Importing Models using Ollama Framework with GGUF Support**

## **Project Overview**

This project demonstrates how to customize large language models (LLMs) using the **Ollama framework** and how to import and run **GGUF models** locally. The focus is on modifying the behavior of a base model (Llama 3) using a Modelfile, importing a GGUF model, and comparing their performance. This repository also includes performance tests and documentation on the comparison of model responses.

---

## **Repository Structure**

- **`Modelfile.txt`**: Contains the customization instructions for the Llama 3 model, modifying the temperature and system prompt to fine-tune the model's responses.

- **`Modelfile (1).txt`**: Contains instructions for importing a GGUF model (`Indic-gemma-2b-finetuned-sft-Navarasa-2.0.gguf`) using the Ollama framework.

- **`GGUF_file_conversion_using_huggingface.ipynb`**: A Jupyter notebook that demonstrates how to convert a model into GGUF format using the Hugging Face library. This notebook covers the model conversion process for more efficient local inference.

- **`TechnologyDocumentation.pdf`**: Detailed comparison of the customized GGUF model and the default Llama 3 model. This document highlights key differences in model behavior and provides insights into the benefits of customization.

- **`Customized_Model_Test_Results.pdf`**: Contains the test results and observations from interacting with the customized GGUF model. This includes examples of questions asked to the model and its responses, along with findings and key observations.

---

## **Project Setup**

### **Requirements**

1. **Ollama Framework**: Ensure that you have the Ollama CLI installed for running LLMs locally.
   - To install Ollama, follow the instructions on the official [Ollama website](https://ollama.com).

2. **GGUF Model File**: A GGUF model like `Indic-gemma-2b-finetuned-sft-Navarasa-2.0.gguf` should be available locally.

3. **Python Environment**: Install necessary packages for GGUF model conversion (found in the Jupyter notebook).

### **Steps to Run the Project**

#### **Task 1: Customizing the Llama 3 Model**

1. **Pull the Llama 3 Model**:
   ```bash
   ollama pull llama3
   ```

2. **Create and Customize the Model**:
   Use the `Modelfile.txt` to customize the Llama 3 model with a system prompt and temperature setting.
   ```bash
   ollama create custom_llama3 -f ./Modelfile.txt
   ```

3. **Run the Customized Model**:
   ```bash
   ollama run custom_llama3
   ```

4. **Test the Model**:
   Interact with the model by asking various questions and note the differences in behavior due to customization.

#### **Task 2: Importing and Using a GGUF Model**

1. **Download the GGUF Model**:
   Ensure that the model (e.g., `Indic-gemma-2b-finetuned-sft-Navarasa-2.0.gguf`) is saved locally.

2. **Create the GGUF Model**:
   Use `Modelfile (1).txt` to import the GGUF model.
   ```bash
   ollama create imported_vicuna -f ./Modelfile\ (1).txt
   ```

3. **Run the Imported GGUF Model**:
   ```bash
   ollama run imported_vicuna
   ```

4. **Convert Models to GGUF Format**:
   If you wish to convert models into GGUF format, use the provided `GGUF_file_conversion_using_huggingface.ipynb` notebook.

---

## **Model Comparison and Test Results**

### **Comparison of Customized and Default Llama 3 Models**
The results of the comparison can be found in the `TechnologyDocumentation.pdf`. Key differences in model behavior, such as the tone and style of responses, are discussed.

### **GGUF Model Testing Results**
The results of testing the customized GGUF model, along with detailed findings and observations, are documented in the `Customized_Model_Test_Results.pdf` file. This includes examples of questions posed to the model and the generated responses.

---

## **Key Findings**

- **Custom Model vs. Default Model**: The customized Llama 3 model, with a temperature of 0.7 and a specific system prompt, generates more **focused and insightful responses** compared to the default model.
- **Performance of GGUF Model**: The GGUF model is optimized for local inference, showing **significant improvements in memory usage and speed** without a noticeable drop in response quality.
- **Response Behavior**: Adjusting parameters like temperature and system prompt allows for fine-tuning the **tone, conciseness, and depth of responses**.

---

## **Conclusion**

This project provides a hands-on guide to customizing LLMs using the Ollama framework and importing GGUF models for efficient local inference. The provided documentation, test results, and model files offer a comprehensive look at the effects of model customization and performance optimization through quantization.

Feel free to explore the repository and experiment with further customizations or model imports!

---

## **Contributing**

If you would like to contribute to this project or suggest improvements, feel free to open an issue or submit a pull request. All contributions are welcome!
