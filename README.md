# 🎓 LMS Gamifikasi SMKN 6 Garut

Learning Management System (LMS) berbasis gamifikasi untuk meningkatkan motivasi belajar siswa di SMKN 6 Garut.  
Dikembangkan menggunakan **Laravel (backend)** dan **Next.js (frontend)** dengan **PostgreSQL** sebagai basis data.

---

## 🧭 Project Overview
LMS ini menghadirkan pengalaman belajar seperti permainan dengan fitur **level, quest, achievement, badge, leaderboard**, dan **progress tracking**.  
Setiap siswa dapat mengumpulkan XP, naik level, dan bersaing di leaderboard, sementara guru dan admin dapat memantau perkembangan belajar melalui dashboard.

---

## ⚙️ Tech Stack
- **Frontend:** Next.js + TailwindCSS  
- **Backend:** Laravel + Sanctum  
- **Database:** PostgreSQL  
- **Deployment:** Vercel (frontend), Render (backend), Supabase (database)

---

## 📁 Repository Structure
| Folder | Deskripsi |
|---------|------------|
| `/frontend` | Source code antarmuka pengguna (Next.js) |
| `/backend` | REST API dan logika bisnis (Laravel) |
| `/docs` | Dokumentasi teknis, diagram, dan laporan proyek |

```
lms-gamifikasi-smkn6/
├── backend/
│   ├── app/
│   ├── routes/api.php
│   ├── database/migrations/
│   └── composer.json
│
├── frontend/
│   ├── pages/
│   ├── components/
│   ├── public/
│   └── package.json
│
├── docs/
│   ├── SRS.md
│   ├── ARCHITECTURE.md
│   ├── ERD.png
│   └── API_SPEC.md
│
└── README.md
```

---

## 🚀 Installation Guide

### 1. Clone Repository
```bash
git clone https://github.com/[username]/lms-gamifikasi-smkn6.git
cd lms-gamifikasi-smkn6
```

### 2. Setup Backend
```bash
cd backend
cp .env.example .env
composer install
php artisan key:generate
php artisan migrate --seed
php artisan serve
```

### 3. Setup Frontend
```bash
cd ../frontend
cp .env.example .env
npm install
npm run dev
```

Frontend default: http://localhost:3000  
Backend default: http://localhost:8000/api

---

## 🧩 Features
- Role-based login (Admin, Staff, Siswa)
- Manajemen kursus dan quest
- Sistem XP, level, dan badge
- Leaderboard dan statistik progres
- Dashboard interaktif untuk siswa dan guru

---

## 🧠 API Overview
| Endpoint | Method | Deskripsi |
|-----------|---------|-----------|
| `/api/login` | POST | Login pengguna |
| `/api/courses` | GET | Ambil semua kursus |
| `/api/quests` | GET | Ambil daftar quest aktif |
| `/api/leaderboard` | GET | Ambil data leaderboard |

---

## 🧱 Database Entities (Singkat)
| Tabel | Deskripsi |
|--------|------------|
| `users` | Data pengguna (admin, staff, siswa) |
| `courses` | Data kursus atau pelajaran |
| `quests` | Tantangan yang bisa diselesaikan siswa |
| `achievements` | Badge dan pencapaian siswa |
| `progress` | Rekam XP, level, dan quest siswa |
| `leaderboard` | Data agregat XP & ranking siswa |

---

## 🧰 Development Tools
- VS Code  
- GitHub Projects (kanban tracking)  
- Postman / Insomnia (API test)  
- Notion (project documentation)

---

## 📈 Version Control Strategy
- `main` → branch stabil untuk rilis  
- `dev` → branch aktif pengembangan  
- `feature/*` → branch spesifik fitur (misal `feature/quest-system`)  
- `fix/*` → branch perbaikan bug  

Pull request wajib dari `feature/*` ke `dev`, baru ke `main` setelah testing.

---

## 🧪 Testing
```bash
# Backend testing
php artisan test

# Frontend testing
npm run test
```

---

## 📦 Deployment
| Layer | Platform | Konfigurasi |
|--------|------------|-------------|
| Frontend | Vercel | Auto-deploy dari branch `main` |
| Backend | Render / Railway | Build otomatis via GitHub Action |
| Database | Supabase | PostgreSQL cloud |
| CI/CD | GitHub Actions | Deploy otomatis setelah merge ke main |

---

## 👥 Team
| Role | Name | Description |
|-------|------|-------------|
| Project Owner | Muhamad Rizki Ardiansyah | Penanggung jawab keseluruhan proyek |
| System Analyst | Muhamad Rizki Ardiansyah | Desain sistem dan model data |
| Developer | Muhamad Rizki Ardiansyah | Full-stack developer |
| QA Tester | Muhamad Rizki Ardiansyah | Pengujian sistem |

---

## 📄 License
MIT License — bebas digunakan untuk keperluan akademik dan pengembangan pendidikan.

---

> © 2025 LMS Gamifikasi SMKN 6 Garut | Made by Muhamad Rizki Ardiansyah
