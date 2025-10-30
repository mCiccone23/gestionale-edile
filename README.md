# 🏗️ Gestionale Edile

## 👤 Utenti

- **Capo**

---

## ⚙️ Funzionalità

- ➕ Aggiunta, modifica e rimozione **dipendenti**
- 🏗️ Aggiunta, modifica e rimozione **cantieri** associati a un cliente
- 👥 Aggiunta, modifica e rimozione **clienti**
- 📅 Aggiunta, modifica e rimozione **giornate di lavoro** associate a dipendenti e cantieri
- 💰 Aggiunta **acconti** a un dipendente
- 👁️ Visualizzazione **profilo dipendente** con giornate lavorate e compensi da ricevere

---

## 🧱 Entità

| Entità                 | Campi                                                     |
| ---------------------- | --------------------------------------------------------- |
| **Utente (Capo)**      | email, password                                           |
| **Clienti**            | nome, cognome, telefono *(opzionale)*, mail *(opzionale)* |
| **Dipendenti**         | nome, cognome                                             |
| **Cantieri**           | id, via, cliente                                          |
| **Giornate di lavoro** | id, dipendente, cantiere, data, paga *(opzionale)*        |
| **Acconti**            | id, somma, dipendente                                     |

---

## 🚀 Funzionalità Future

- 📦 Gestionale **Magazzino**
- 🧾 Gestionale **Lavori** (preventivo, percentuali lavori fatti, soldi ricevuti, scadenze, materiale relativo)

---

## 🧩 Architettura Generale

```
📱 React (Frontend)
      │
      ▼
🌐 Express + Node.js (Backend)
      │
      ▼
🗄️ PostgreSQL (Database)
```

**Deploy:**  

- Frontend → 🟢 **Vercel**  
- Backend → 🟣 **Render**  
- Database → 🟠 **Supabase**

---

## 🖥️ Frontend

**🎯 Obiettivo:** interfaccia semplice, moderna e ottimizzata per smartphone

**Tecnologie:**

- ⚛️ **React + TypeScript** → framework per creare l’app web  
- ⚡ **Vite** → build tool veloce e leggero  
- 🎨 **Tailwind CSS** → design responsive e mobile-friendly  
- 🔀 **React Router** → gestione delle pagine (Home, Dipendenti, Cantieri, ecc.)  
- 📱 **PWA (Progressive Web App)** → installabile come app sul telefono del capo  

**Deploy:**  

- 🌐 **Vercel (gratis)**  
  - Collegamento diretto con GitHub  
  - URL tipo: `https://gestionale-matteo.vercel.app`  
  - HTTPS automatico e caching CDN  
  - Ottimizzato per mobile out-of-the-box

---

## ⚙️ Backend

**🎯 Obiettivo:** API REST per gestire dipendenti, cantieri, giornate e acconti

**Tecnologie:**

- 🟩 **Node.js + Express + TypeScript** → server leggero e veloce  
- 🔐 **JWT (jsonwebtoken)** → autenticazione sicura per il login del capo  
- 🧩 **Zod** → validazione pulita dei dati in entrata *(opzionale)*

**Deploy:**

- 🚀 **Render (gratis)**  
  - Collega il repo GitHub  
  - Build automatica con `npm run build`  
  - Imposta variabile `.env` con `DATABASE_URL` (da Supabase)  
  - URL tipo: `https://gestionale-api.onrender.com`

---

## 🗄️ Database

**🎯 Obiettivo:** dati persistenti per dipendenti, giornate, cantieri, acconti

**Tecnologie:**

- 🐘 **PostgreSQL**
- ☁️ **Supabase** (DB as a Service, gratuito per uso base)

**Vantaggi:**

- Console web intuitiva  
- Backup automatico  
- Accesso sicuro con connection string  

**Deploy:**

- Crea un progetto su Supabase → ottieni `DATABASE_URL`  
- Copia l’URL nel file `.env` del backend  
- Prisma si collega direttamente al database

---

## ☁️ Deploy (Stack Gratuito)

| Componente                | Piattaforma | Funzione                   | Costo    |
| ------------------------- | ----------- | -------------------------- | -------- |
| **Frontend (React)**      | 🟢 Vercel    | Hosting e build automatica | ✅ Gratis |
| **Backend (Node.js)**     | 🟣 Render    | API REST online 24/7       | ✅ Gratis |
| **Database (PostgreSQL)** | 🟠 Supabase  | Gestione dati e backup     | ✅ Gratis |

---

## 📱 Ottimizzazione Mobile

Con **Tailwind** e **PWA**:

- Layout responsive automatico (flex, grid, w-full, p-4)  
- Modalità “Add to Home Screen”  
- Funziona anche offline (cache PWA)  
- Esperienza quasi identica a un’app nativa

---

📘 **Autore:** Matteo Ciccone  
📅 **Progetto:** Gestionale Edile  
