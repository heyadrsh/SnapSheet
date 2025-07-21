# Setup Instructions for OCR to CSV Converter

## Prerequisites
- Node.js 18+ installed
- A Gemini API key from Google AI Studio

## Quick Setup

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Configure Environment**
   Create a `.env.local` file in the root directory:
   ```bash
   GEMINI_API_KEY=your_actual_gemini_api_key_here
   ```

   Get your API key from: https://ai.google.dev/gemini-api/docs/get-started

3. **Run the Application**
   ```bash
   npm run dev
   ```

4. **Open in Browser**
   Navigate to: http://localhost:3000

## How It Works

1. **Upload Image**: Upload any image containing text, tables, or forms
2. **AI Processing**: Gemini 2.5 Flash analyzes the image and extracts structured data
3. **CSV Generation**: The AI converts the extracted data into properly formatted CSV
4. **Download**: Preview and download the generated CSV file

## Supported File Types
- PNG, JPG, JPEG, WebP
- Tables, forms, receipts, documents
- Handwritten or printed text

## Features
- ✅ Drag & drop file upload
- ✅ AI-powered OCR with Gemini 2.5 Flash
- ✅ Automatic CSV conversion
- ✅ Download functionality
- ✅ Responsive design
- ✅ Error handling

## Troubleshooting

**Error: Gemini API key not configured**
- Make sure you've created `.env.local` with your API key
- Restart the development server after adding the key

**Error: Failed to process image**
- Ensure the uploaded file is a valid image
- Check your API key is valid and has quota available
- Try with a clearer image if the text is hard to read

## Project Structure
```
├── app/
│   ├── api/convert-image/route.ts  # Gemini API integration
│   ├── page.tsx                    # Main UI
│   ├── layout.tsx                  # App layout
│   └── globals.css                 # Styles
├── components/ui/
│   └── file-upload.tsx             # Upload component
└── lib/
    └── utils.ts                    # Utilities
``` 