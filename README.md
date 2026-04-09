# Architect AI: Technical Diagram Analyzer

Architect AI is a multimodal artificial intelligence tool designed to analyze, explain, and summarize complex technical diagrams. Built with the Qwen2-VL-7B-Instruct vision-language model and augmented with EasyOCR, this application acts as an automated technical architect capable of understanding system architectures, sequence diagrams, and database schemas in multiple languages.

## Key Features

* **Type-Aware Analysis:** Automatically detects the type of diagram and adjusts its output structure accordingly. Supported types include System Architectures, Sequence Diagrams, Entity-Relationship (ER) Diagrams, and Process Flowcharts.
* **Multilingual Pipeline:** Supports English, Hindi, Spanish, Chinese, Japanese, French, and German. It uses a two-pass system (analyzing in English first, then translating) to maintain high technical accuracy across different languages and scripts.
* **Interactive Q&A Chatbot:** Includes a chat interface that allows users to ask specific follow-up questions about the uploaded diagram.
* **Quick Summarization:** Generates a concise, two-sentence high-level overview of the diagram's core purpose.
* **Strict Visual Tracing:** Engineered to trace visual elements (such as directional arrows in a sequence diagram) rather than simply reading text from left to right.

## Technical Stack

* **Vision-Language Model:** Qwen/Qwen2-VL-7B-Instruct
* **Text Extraction:** EasyOCR
* **User Interface:** Gradio 6.0
* **Memory Optimization:** bitsandbytes (4-bit quantization)

## Usage Instructions

1. **Upload:** Upload a technical diagram (PNG, JPG, or JPEG) into the interface.
2. **Select Language:** Choose your desired output language from the dropdown menu.
3. **Analyze or Summarize:**
   * Click "Deep Analyze" for a complete, structured breakdown.
   * Click "Quick Summary" for a brief overview.
4. **Ask Questions:** Use the chat panel on the right to ask follow-up questions regarding the uploaded diagram.

## Known Limitations

* **Processing Time:** Generating responses in non-English languages may take slightly longer due to the two-pass translation pipeline required for accurate localization.
* **Token Constraints:** Exceptionally large or complex diagrams with dozens of interactions may occasionally reach the output token limit during translation.
