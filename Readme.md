# FilesGPT — AI File Chat Application Prompt 🚀

<p align="center">
  <img src="https://img.icons8.com/fluency/96/chat.png" alt="FilesGPT Logo" width="96" />
</p>
<p align="center">
  <a href="https://filesgptaii.lovable.app/">
    <img src="https://img.shields.io/badge/🔗-Live%20Demo-2D9CDB?style=for-the-badge&logo=webflow&logoColor=white" alt="Live Demo" />
  </a>
</p>

Welcome to **FilesGPT**, your all-in-one platform to upload, manage, and chat with your files using cutting-edge AI. Below is the comprehensive project prompt to scaffold and build the system—no code or assets included.

---

## 📢 Project Prompt

### Project Name & Purpose
- **FilesGPT**: A web application where users can upload, organize, and chat with their files in one seamless interface.

### Hero Section
- **Layout & Branding**
  - **Logo:** Top-left “FilesGPT” (clean, bold sans-serif).  
  - **Sign Up Button:** Top-right coral `#FF6F61` → navigates to Auth.
- **Main Heading:**
  <h1 style="font-family:'Montserrat', sans-serif; font-weight:700; color:#333333; text-align:center;">
    Transform the Way You <span style="color:#FF6F61;">Interact</span> with Your Files
  </h1>
- **Subheading:**<br>
  <p style="font-family:'Roboto', sans-serif; font-weight:400; color:#333333; text-align:center;">
    Upload, manage, and chat with your files in a seamless, intuitive environment.
  </p>
- **Illustration / Play Icon**
  - Centered circular play-button overlay on a soft gradient (light coral → light blue).
  - Hover effect: scale-up + lower overlay opacity.
- **Primary CTA:**
  <button style="background:#2D9CDB; color:#FFF; font-family:'Montserrat'; font-weight:500; padding:0.75rem 1.5rem; border-radius:0.5rem;">Get Started →</button>
  <br>Hover: lighten 10%; click → Auth page.
- **Colors & Background:**
  - Page background: `#F7F7F7`.  
  - Hero background: diagonal gradient (`#F7F7F7` → light coral).

### Authentication Flow (Single-Page, Tabbed)
- Centered card with tabs: **Sign Up** | **Sign In**.
- **Fields:** Email (real-time validation), Password (strength meter on Sign Up).
- **Actions:** Sign Up → coral `Create Account`; Sign In → coral `Continue`.
- **Toggle Links:**
  - Sign In view: “Don’t have an account? Sign Up”
  - Sign Up view: “Already have an account? Sign In”
- Inline errors; on success → dashboard.

### Accessibility & Responsiveness
- Keyboard navigable with visible focus states.
- ARIA labels on controls.
- Breakpoints: mobile ≤640px, tablet 641–1024px, desktop ≥1025px.

### Deliverables
- React components (Tailwind CSS) for Hero & Auth.
- Animated, clickable CTAs & play icon.
- Consistent typography, spacing, and colors.

---

## 🛠️ Core Architecture
- **Frontend:** React + TypeScript + Tailwind CSS + Vite  
- **Backend:** Supabase (DB, Storage, Auth, RLS, Edge Functions)  
- **AI Integration:** Gemini API for chat  

> **Note:** All sensitive operations require **your credentials**.

---

## 📋 Database Schema
| Table                  | Purpose                                        | Access Scope  |
|------------------------|------------------------------------------------|---------------|
| `files`                | File metadata & extraction status              | User-scoped   |
| `n8n_chat`             | Chat sessions linked to files                  | User-scoped   |
| `n8n_chat_histories`   | Chat messages (user & assistant)               | User-scoped   |
| `daily_message_limits` | Tracks daily messages (5/day)                  | User-scoped   |
| `profiles`             | Extended user profiles                         | User-scoped   |
| `vectors_data`         | Embeddings for future RAG                      | User-scoped   |

### Database Functions
- `check_and_increment_message_count()` — rate limiting  
- `get_daily_message_count()` — current count fetch  
- `handle_new_user()` — signup hook

---

## ⚙️ Edge Functions
1. **upload-file** — upload handler (`your credentials`)  
2. **delete-file** — deletion handler (`your credentials`)  
3. **extract-text** — text extraction (`your credentials`)  
4. **chat-with-file** — AI chat endpoint (`your credentials`)

---

## 🧩 React Components & Hooks
**Components:**
- `FileUploader` — drag & drop 📂
- `FileList` — browse & delete 🗂️
- `ChatInterface` — AI chat 💬
- `AuthFlow` — Sign Up/Sign In 🔒

**Pages:** `Index`, `Auth`, `Dashboard`, `NotFound` 🚫

**Hooks:**
- `useFileOperations`  
- `useFileChat`  
- `useMessageLimit`

---

## ✅ Key Features
- Supabase Auth 🔐  
- File upload (50 MB limit) 📦  
- Text extraction 📄  
- AI chat via Gemini 🤖  
- 5/day message limit ⏳  
- Dark/light themes 🌗  
- Real-time updates 🔄  
- RLS security 👮

## 🔄 Future Enhancements
- Semantic search embeddings 🔮  
- PDF/DOCX support 📑  
- Chat session management 🗃️

---

> **Only the prompt** resides here; code & assets excluded.
