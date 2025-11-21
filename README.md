MEDDPICC Opportunity Analyzer

This is a single-page web application designed to help sales professionals analyze raw data—such as meeting notes, document text, or images of whiteboards—and extract the eight critical fields of the MEDDPICC sales methodology: Metrics, Economic Buyer, Decision Criteria, Decision Process, Paper Process, Identify Pain, Champion, and Competition.

The application leverages the Gemini API for natural language processing and multimodal analysis (handling both text and images) with a structured JSON output to ensure high accuracy and reliability.

Features

Text Input: Analyze manually pasted meeting notes, email transcripts, or text extracted from documents.

Multimodal Image Analysis: Upload PNG or JPG images (e.g., screenshots, photos of whiteboards) for direct analysis.

Structured Output: Uses a structured response schema to guarantee accurate, categorized results.

Anti-Hallucination Guardrails: Explicitly instructs the model to state when information is "Missing or Vague" rather than fabricating data.

Responsive Design: Built with Tailwind CSS for a modern, mobile-friendly interface.

Setup and Hosting

This is a client-side only application, meaning it runs entirely in the user's web browser and does not require a complex backend server.

1. Obtain a Gemini API Key

Get your API key from [Google AI Studio].

Keep this key secure.

2. File Structure

The project only requires the following files in your repository root:

/
├── index.html
└── README.md
└── .gitignore


3. Deploy

Since this is a static HTML file, you can host it easily:

GitHub Pages: Push the files to a repository and enable GitHub Pages on the main branch. The app will be available at your-username.github.io/your-repo-name.

Local Hosting: Simply open the index.html file directly in any modern web browser.

4. Configure the API Key (CRITICAL STEP)

The index.html file currently has the apiKey variable empty for compatibility with certain environments:

const apiKey = ""; // Leave as empty string for automatic provision


To run this application successfully on your local machine or through GitHub Pages, you must replace the empty string with your Gemini API key.

In index.html, change the line to:

const apiKey = "YOUR_API_KEY_HERE"; // <-- Replace this with your actual key!


Usage

Paste Text: Copy meeting notes, discovery questions, or text from documents (PDF/DOCX) into the large textarea.

Upload Image (Optional): Click the "Drag & Drop" area to select a PNG or JPG file.

Analyze: Click the "Analyze MEDDPICC" button.

Review Results: The analysis will appear in the cards on the right, clearly identifying and separating each MEDDPICC element. Missing or vague information will be flagged in red.
