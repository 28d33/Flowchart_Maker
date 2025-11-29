# 🧜‍♀️ FlowchartMaker  
**AI-powered Mermaid.js flowchart editor with live preview and infinite canvas**

FlowchartMaker is a lightweight, single-file web application for creating, editing, and visualizing Mermaid.js diagrams. It features real-time rendering, a split-pane editor, zoomable infinite canvas, and an integrated AI Assistant powered by Google Gemini to generate diagram code from natural language.

---

## ✨ Features

### 🔹 1. Live Editing & Preview
- Real-time Mermaid.js rendering into SVG
- Split-pane layout for code (left) & preview (right)
- Syntax highlighting with **Fira Code** font
- One-click **Copy SVG** export

### 🔹 2. Infinite Canvas
- Pan the diagram by dragging the background  
- Zoom between **0.1× – 10×** (mouse wheel or UI buttons)  
- Dot-grid dynamic background  
- Reset view to default position & zoom  

### 🔹 3. 🤖 AI Assistant (Gemini)
- Generate Mermaid code from plain English  
- Supports system API key or user-provided Gemini key  
- Secure: user input wrapped in a protected data block  
- Automatic exponential backoff for API errors  
- Output sanitization (strips code fences)

### 🔹 4. 🛡 Security & Guardrails
- Prompt-injection protection template  
- Input capped at **2000 characters**  
- Strict Mermaid-only output enforcement  
- Error diagram returned if violation is detected  

---

## 🛠 Tech Stack

| Component | Technology |
|----------|------------|
| Frontend | HTML5, Vanilla JavaScript (ES6 Modules) |
| Styling | Tailwind CSS (CDN) |
| Diagrams | Mermaid.js v10 |
| AI Model | Google Gemini 2.5 Flash (REST API) |
| Fonts | Inter (UI) & Fira Code (Editor) |
| Icons | Inline SVG |

---

## 📖 Usage

### 1. Open the App  
Just open **index.html** in any modern browser.  
No server or build step required.

### 2. Manual Editing  
Type Mermaid syntax in the editor.  
The preview updates automatically.

### 3. Using the AI Assistant  
1. Click **AI Assistant**  
2. Paste API key if asked  
3. Describe your diagram  
4. Click **Generate Code**  
5. The editor updates instantly

### 4. Canvas Controls  
- **Pan**: click & drag  
- **Zoom**: mouse wheel or + / – buttons  
- **Reset**: center & reset zoom  
- **Copy SVG**: one click button  

---

## 🔒 AI Prompt Architecture

FlowchartMaker uses a layered security prompt:

- Wraps the user message in a `"User Input Data"` block  
- Model instructed to treat everything inside as **data only**  
- Any attempt to override rules triggers a special **Error graph**  
- Strips Markdown fences to ensure output is raw Mermaid code  

This prevents injection attempts and ensures consistent, valid diagrams.

---

## 📦 Project Structure (single-file)
index.html # Full app (UI + JS + CSS + AI logic)

---

## 🧑‍💻 Development Notes
- No build tools or dependencies  
- Fully client-side  
- Works offline except for AI calls  
- Easily extensible (themes, templates, imports, etc.)

---

## 📝 License
MIT License

---

## ⭐ If this helped, consider starring the repository!
