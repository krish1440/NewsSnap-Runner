# 🚀 NewsSnap-Runner (Public Ingestion Worker)

This public repository serves as the **automated background worker** for **NewsSnap (Authentic News)**.

Because this repository is **Public**, all GitHub Actions runner minutes are **100% UNLIMITED & FREE** (saving 3,000+ private runner minutes every month).

---

## 🔒 Security Guarantee
- **Zero Source Code**: This repository contains **NO private application or backend source code**.
- **In-Memory Checkout**: During GitHub Actions execution, the worker securely pulls the private `kc1404/NewsSnap` repository into temporary runner memory using a GitHub Personal Access Token (`PRIVATE_REPO_PAT`).

---

## 🛠️ Required Repository Secrets
To run this worker, the following Repository Secrets must be configured under **Settings -> Secrets and variables -> Actions**:

| Secret Name | Description |
| :--- | :--- |
| `PRIVATE_REPO_PAT` | Fine-grained GitHub Access Token (`Contents: Read-only` access to `NewsSnap`) |
| `RENDER_API_URL` | Deployed backend API domain (e.g. `https://news-snap-backend.onrender.com`) |
| `SUPABASE_URL` | Supabase Database URL |
| `SUPABASE_KEY` | Supabase Service Role Key |
| `GEMINI_API_KEYS` | Gemini API Keys (comma-separated list for rotation) |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary Cloud Name |
| `CLOUDINARY_API_KEY` | Cloudinary API Key |
| `CLOUDINARY_API_SECRET` | Cloudinary API Secret |
| `CLOUDINARY_URL` | Cloudinary connection URL string |
| `CLOUDINARY_ACCOUNTS` | Multi-account pool format |
| `PEXELS_API_KEY` | Pexels API Key |
| `SHABD_EMAIL` | Prasar Bharati SHABD login email |
| `SHABD_PASSWORD` | Prasar Bharati SHABD login password |

---

## 🚀 How to Push Changes to this Public Repo

To push the `public_runner/` directory to `https://github.com/krish1440/NewsSnap-Runner.git`:

```bash
cd public_runner
git init
git remote add origin https://github.com/krish1440/NewsSnap-Runner.git
git branch -M main
git add .
git commit -m "ci(worker): setup 24/7 public ingestion worker with API status check"
git push -u origin main
```
