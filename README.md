# 🏡 n8n AI Listings Ingestion (SaaS Prototype)

![Status](https://img.shields.io/badge/Status-Prototype-blue) ![Stack](https://img.shields.io/badge/Stack-Astro_Supabase_n8n_Gemini-orange) ![License](https://img.shields.io/badge/License-MIT-green)

> **A Full-Stack Real Estate ETL Pipeline.**
> Automates property listing creation from unstructured chat messages using AI agents and serverless architecture.

---

### 🌐 [Live Demo (Vercel)](https://n8n-ai-listings-demo.vercel.app/) | 📺 [Watch the Video Demo](#)

---

## 🇺🇸 English Description

### 💡 The Problem
Real Estate agents spend hours manually uploading property details from WhatsApp/Facebook Marketplace to their websites. This process is slow, error-prone, and unscalable.

### 🚀 The Solution
I built an **Automated Ingestion Pipeline (ETL)**. The agent simply forwards a raw text message or link to a Telegram/WhatsApp Bot. The system processes the unstructured data, generates a sales pitch using AI, extracts structured JSON (price, beds, location), and deploys it to the web in real-time.

### 🏗️ Architecture & Workflow

1.  **Ingestion:** Webhook receives raw data from Telegram/WhatsApp (via **n8n**).
2.  **Transformation (AI):** **Google Gemini 1.5 Flash** analyzes the text/images to:
    * Extract key metadata (Price, Bathrooms, Sq Meters).
    * Write a persuasive sales description (Copywriting).
    * Standardize the address.
3.  **Loading:** Data is inserted into **Supabase (PostgreSQL)**.
4.  **Deployment:** **Astro** (SSR) detects the DB change and serves the new listing instantly with high performance.

### 🛠️ Tech Stack
* **Frontend:** Astro 5, TailwindCSS (Hybrid Rendering).
* **Backend & DB:** Supabase (PostgreSQL), Edge Functions.
* **Automation:** n8n (Self-Hosted Workflow).
* **Artificial Intelligence:** Google Gemini API (Structured Output).
* **Infrastructure:** Vercel (Hosting), ngrok (Tunneling).

---

## 🇲🇽 Descripción en Español

### 💡 El Problema
Los agentes inmobiliarios pierden horas subiendo manualmente fotos y descripciones de casas a sus sitios web. Es un proceso lento, repetitivo y propenso a errores humanos.

### 🚀 La Solución
Desarrollé un **Pipeline de Ingesta Automatizada (ETL)**. El agente solo reenvía el mensaje de WhatsApp o el link de Facebook a un Bot. El sistema procesa la información desestructurada, redacta un texto de venta usando IA, extrae datos técnicos (precio, baños, ubicación) y publica la propiedad en la web en tiempo real.

### 🏗️ Arquitectura y Flujo

1.  **Ingesta:** Un Webhook recibe los datos crudos desde Telegram/WhatsApp (vía **n8n**).
2.  **Transformación (IA):** **Google Gemini 1.5 Flash** analiza el texto/imágenes para:
    * Extraer metadatos clave (Precio, Baños, m²).
    * Redactar una descripción de venta persuasiva (Copywriting).
    * Estandarizar la dirección.
3.  **Carga (Load):** Los datos limpios se insertan en **Supabase (PostgreSQL)**.
4.  **Despliegue:** **Astro** (SSR) detecta el cambio en la BD y sirve la nueva ficha técnica al instante con alto rendimiento.

### 🛠️ Tecnologías
* **Frontend:** Astro 5, TailwindCSS (Renderizado Híbrido).
* **Backend & DB:** Supabase (PostgreSQL), Edge Functions.
* **Automatización:** n8n (Workflow Self-Hosted).
* **Inteligencia Artificial:** Google Gemini API (Salida Estructurada).
* **Infraestructura:** Vercel (Hosting), ngrok (Tunneling).

---

## 📸 Screenshots / Demo

*(Place your GIF or Screenshots here showing the Chat-to-Web flow)*

| Chat Input (WhatsApp) | AI Processing (n8n) | Final Web Result |
| :---: | :---: | :---: |
| ![Chat](path/to/chat-screenshot.png) | ![n8n](path/to/n8n-screenshot.png) | ![Web](path/to/web-screenshot.png) |

---

## 💻 Local Setup

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/tu-usuario/n8n-ai-listings-ingestion.git](https://github.com/tu-usuario/n8n-ai-listings-ingestion.git)
    cd n8n-ai-listings-ingestion
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Environment Variables**
    Create a `.env` file based on `.env.example`:
    ```env
    PUBLIC_SUPABASE_URL=your_supabase_url
    PUBLIC_SUPABASE_ANON_KEY=your_supabase_key
    ```

4.  **Run Development Server**
    ```bash
    npm run dev
    ```

---

*Developed by **enyeel** - Full Stack Developer specialized in AI Automation.*
*Available for freelance work.*
