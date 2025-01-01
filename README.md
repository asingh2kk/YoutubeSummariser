# YouTube AI Summariser Chrome Extension

A Chrome Extension that summarizes YouTube videos using OpenAI's GPT-4 model. This extension extracts the transcript of a video, generates a concise summary, and displays it in a sidebar on the YouTube page.

---

## Features

- Automatically fetches transcripts for YouTube videos with captions.
- Generates concise, AI-powered summaries using OpenAI's GPT-4 API.
- Integrates seamlessly into YouTube's interface via a sidebar.
- Dynamically updates the sidebar as users navigate between videos.
- Responsive UI for different screen sizes and layouts.

---

## Project Structure

The project is built using **Node.js** and **TypeScript**, compiled to JavaScript using Webpack for execution by Chrome.

### Key Files:

- **`manifest.json`**: Configures the extension, including permissions and scripts.
- **`content.ts`**: Interacts with the YouTube DOM, fetches video information, and injects the sidebar.
- **`Sidebar.tsx`**: React component for the summarization sidebar.
- **`open-ai.ts`**: Handles OpenAI API calls to generate summaries.
- **`popup.tsx`**: React component for the extension's popup menu.
- **`index.css`**: Styled using TailwindCSS for responsive and clean UI.
- **`webpack.config.js`**: Configures Webpack for bundling files.
- **`postcss.config.js`**: Processes TailwindCSS directives.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/asingh2kk/YoutubeSummariser.git
   cd YoutubeSummariser
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Build the Extension**:
   ```bash
   npm run build
   ```

4. **Load the Extension in Chrome**:
   - Navigate to `chrome://extensions/` in your browser.
   - Enable "Developer Mode" (toggle at the top right).
   - Click "Load Unpacked" and select the `public/` directory.

5. **Configure OpenAI API Key**:
   - Create a `.env` file in the project root with the following:
     ```
     OPENAI_API_KEY=your_openai_api_key
     ```
   - Replace `your_openai_api_key` with your OpenAI API key.

---

## Usage

1. Go to any YouTube video page with captions.
2. Click the extension icon in the Chrome toolbar to enable the summarization sidebar.
3. The sidebar will appear on the right-hand side of the video. Click the sidebar to fetch and display the summary.

---

## Technologies Used

- **TypeScript**: Strongly typed JavaScript for robust development.
- **Webpack**: Module bundler for compiling and optimizing files.
- **TailwindCSS**: Utility-first CSS framework for rapid UI development.
- **React**: Frontend library for building interactive components.
- **OpenAI GPT-4 API**: AI-powered text summarization.
