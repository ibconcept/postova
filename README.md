# Postova  
*Make posts quickly, edit text with AI backgrounds or images from search*

---

## 📰 Postova – Breaking Poster Generator for Everyone

Postova is the fastest and most intuitive way to transform news, celebrity updates, announcements, and any text-based content into stunning, shareable visual posters. Designed for ease of use, it empowers anyone – from media teams to individual creators – to craft beautiful graphics without needing any design skills.

---

## ✨ Key Features

### Versatile Content Input  
- **Text & Image Upload:** Directly type or paste your text and upload an accompanying image.  
- **Article Extraction (AI-Powered):** Paste a news article URL, and Postova's AI will intelligently extract and condense the main text along with relevant images, preparing them for your poster.

### Intuitive Customization Controls  
- **Visual Styling:** Effortlessly select background colors, font styles, and text alignment using user-friendly dropdowns and selectors.  
- **Layout Options:** Choose from a variety of pre-defined layouts to perfectly frame your content.

### Intelligent AI Assistance  
- **Auto-Layout & Style Suggestions:** AI analyzes your content and suggests optimal layouts, font pairings, and color schemes for a visually appealing poster.  
- **Text Summarization:** Automatically condense lengthy articles into concise, impactful captions suitable for posters.  
- **OCR & Parsing:** (Future) Reads text directly from uploaded images (e.g., newspaper clippings) for immediate use.

### Seamless Export & Sharing  
- Generate high-quality posters and export them instantly as PNG or JPEG images.

### Optimized Performance  
- Built for speed and efficiency, ensuring a smooth experience even on low-end devices and slower internet connections.

### Fully Web-Based  
- No installations or complex setups – access Postova directly from your web browser, anywhere, anytime.

---

## 🛠️ Tech Stack  
**Optimized for Speed, Portability, Simplicity & Scalability**

| Layer              | Technology                      | Purpose                                                    |
|--------------------|--------------------------------|------------------------------------------------------------|
| Frontend           | Vite + React + Tailwind CSS     | Fast development, responsive utility-first styling        |
| Poster Rendering   | html2canvas or Fabric.js        | Render HTML to canvas for image export                     |
| Authentication    | Supabase Auth                   | User sign-up/login and identity management                 |
| Database          | Supabase PostgreSQL             | Relational DB with real-time capabilities                  |
| Storage           | Supabase Storage                | Store user-uploaded images and posters                      |
| Backend Logic     | Supabase Edge Functions         | Serverless functions for AI, OCR, and server-side logic    |
| Image/Text AI     | OpenAI GPT-4o                   | Text summarization, layout suggestions, content analysis   |
| Additional AI     | Replicate or Custom API          | Specialized image processing and OCR                        |

---

## 🚀 Setup Instructions  

### 1. Clone the repository  
```bash
git clone https://github.com/your-username/postova.git
cd postova
2. Configure Environment Variables
Create a .env file inside the frontend directory

Add your Supabase project URL, Anon Key, and AI API keys

3. Frontend Setup
bash
Copy
Edit
cd frontend
npm install       # Install dependencies
npm run dev       # Start development server (http://localhost:5173)
📁 Project Structure
bash
Copy
Edit
postova/
│
├── frontend/                     # Vite + React + Tailwind + Supabase Client
│   ├── public/                   # Static assets
│   ├── src/
│   │   ├── assets/               # Images, icons, fonts
│   │   ├── components/           # Reusable UI components
│   │   │   ├── PosterCanvas.jsx  # Render & export poster
│   │   │   ├── ControlsPanel.jsx # Input & customization controls
│   │   │   └── Auth.jsx          # Authentication UI
│   │   ├── hooks/                # Custom React hooks
│   │   ├── services/             # API integrations & Supabase client
│   │   ├── pages/                # Main app views/routes
│   │   ├── contexts/             # React Context for global state
│   │   ├── utils/                # Utility functions
│   │   ├── App.jsx               # Main app component
│   │   └── main.jsx              # React entry point
│   ├── .env                      # Env variables for frontend
│   └── index.html                # Main HTML file
│
├── supabase/                     # Supabase configurations
│   ├── functions/                # Edge Functions (serverless logic)
│   ├── migrations/               # DB schema migrations
│   └── seed.sql                  # Initial data seeding
│
└── README.md                     # Project README
✨ Core Functionalities Deep Dive
AI-Assisted Poster Creation
Accepts text, images, or URLs plus styling options

Uses AI for layout suggestions and styling

Renders final poster for export

/summarize-url
AI-powered article extraction and summarization

Prepares content for posters automatically

/upload
Direct image and content uploads stored via Supabase Storage

(Future) OCR support to read text from images

📦 Deployment Options
Platform	Notes
Netlify	Static frontend hosting with global CDN and custom domains
Supabase	Database, auth, storage, and serverless functions
Vercel	Static frontend hosting with great developer experience
Docker	Optional containerization for frontend

🔐 Environment Variables
Frontend .env
env
Copy
Edit
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_OPENAI_API_KEY=your_openai_key
VITE_REPLICATE_API_TOKEN=your_replicate_token
Supabase Edge Functions .env
env
Copy
Edit
OPENAI_API_KEY=your_openai_key
REPLICATE_API_TOKEN=your_replicate_token
📌 Future Features & Enhancements
Reusable poster templates

Direct social media sharing

Multilingual AI poster generation

Drag & drop layout editor

Version history & rollback

Collaboration features (real-time editing)

Advanced poster analytics

🧠 AI Use Cases
Intelligent text summarization for concise captions

OCR and text parsing from images

Dynamic auto-design with AI layout, fonts, colors

Contextual image selection from articles

🫶 Credits
Postova is built with passion for creators, broadcasters, and media teams worldwide, inspired by the universal need for fast, beautiful poster creation tools.
