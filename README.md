<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=220&section=header&text=Prashanth%20Adibhatla&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Gen%20AI%20%C2%B7%20Backend%20%C2%B7%20GPU%20%26%20Systems%20%C2%B7%20Emulation%20%C2%B7%20Competitive%20Programming&descAlignY=60&descSize=15" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=1000&color=38BDF8&center=true&vCenter=true&width=780&lines=Building+RAG+%26+LLM+apps+with+Pinecone+%2B+LangChain+%2B+Spring+AI+%F0%9F%A4%96;Shipping+Spring+Boot+microservices+with+Spring+JDBC+%E2%98%95;Writing+CUDA+C%2B%2B+kernels+for+Python+%E2%9A%A1;Emulating+the+PlayStation+1+in+C%2B%2B+%F0%9F%95%B9%EF%B8%8F;Competitive+programmer+%7C+Hackathon+builder+%F0%9F%8F%86" alt="Typing SVG" />

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=Prashanth-Adibhatla&label=Profile%20Views&color=0e75b6&style=flat-square)
![Followers](https://img.shields.io/github/followers/Prashanth-Adibhatla?style=flat-square&logo=github&color=2c5364)
![Public Repos](https://img.shields.io/badge/Public%20Repos-16-203a43?style=flat-square&logo=github)

</div>

---

## 👋 About Me

I work across the whole stack of "how computers do useful things": **LLM applications** at the top, **production Java microservices** in the middle, and **GPU kernels and console emulators** at the metal.

| | Focus | What I do |
|---|---|---|
| 🤖 | **Generative AI Developer** | Build RAG pipelines and LLM apps with **Pinecone**, **LangChain** and **Spring AI** |
| ☕ | **Backend Developer** | Design REST services and data layers with **Spring Boot** and **Spring JDBC** |
| ⚡ | **Competitive Programmer** | Algorithms, data structures and problem solving under time pressure |
| 🧬 | **GPU / Systems Programmer** | Write **CUDA C++** kernels and expose them to Python via **Pybind11** |
| 🕹️ | **Emulation Developer** | **PS1** and **CHIP-8** emulators in C++ |
| 🔬 | **Applied ML & Security** | Vision Transformers, explainable medical imaging, and PKI / X.509 attack simulation |
| 🏆 | **Hackathon Builder** | Ship fast: games, ML demos and prototypes |

---

## 🌟 Featured Projects

### ⚡ [Cuda-accelerated-python-library](https://github.com/Prashanth-Adibhatla/Cuda-accelerated-python-library)
**A GPU numerical, ML and ray-tracing engine in CUDA C++, bridged to Python with Pybind11 and exposed through a NumPy / SciPy / scikit-learn-style API.**

```
┌──────────────────────────────────────────────────────────────┐
│  Python layer      numeric_cuda.py  (NumPy / sklearn-style)  │
├──────────────────────────────────────────────────────────────┤
│  Pybind11 bridge   bindings.cpp  (zero-copy buffer protocol) │
├──────────────────────────────────────────────────────────────┤
│  CUDA host layer   memory mgmt · grid heuristics · ML loops  │
├──────────────────────────────────────────────────────────────┤
│  GPU kernels       map · reduce · GEMM · scan · stencil      │
└──────────────────────────────────────────────────────────────┘
```

- 🧠 **GPU ML estimators:** `KMeans`, `PCA`, `LinearRegression`, `LogisticRegression`, `KNeighborsClassifier/Regressor`, `GaussianNB`
- 📐 **Linear algebra:** shared-memory tiled `matmul`, warp-per-row `matvec`, bank-conflict-free `transpose`, `cov`, `corrcoef`, GPU symmetric solver
- 📏 **Distances:** 2D-tiled `cdist` (Euclidean, cosine, Manhattan)
- 🌊 **Parallel primitives:** warp-shuffle reductions, prefix scans, radix sort, `searchsorted`, shared-memory histograms, constant-memory 5×5 stencil
- 🎨 **CUDA ray tracer:** one thread per pixel, Blinn-Phong shading, recursive reflections

| Ray tracer (RTX 3060 Laptop GPU, per repo benchmark) | Time |
|---|---|
| CPU serial (Python) | ~35,000 ms |
| CUDA | **~5.33 ms** |
| **Speedup** | **> 4,000×** |

`CUDA C++` `Pybind11` `Thrust` `NumPy` `setuptools + NVCC`

---

### 🛰️ [netops-monitor](https://github.com/Prashanth-Adibhatla/netops-monitor)
**An AI-assisted network-operations platform: microservices, RAG-based incident analysis and a mobile supervisor app.** (42 commits)

```
 Mobile (React Native)  ┐
 Desktop (React Native) ├─▶  API Gateway ─▶ Auth Server (OAuth2 / JWT)
                        ┘          │
                                   ▼
                            netops-backend (Spring Boot 3.3, Java 17)
                      ┌────────────┼────────────────┬───────────────┐
                      ▼            ▼                ▼               ▼
              PostgreSQL +     Ollama LLM       Firebase FCM     Prometheus
              pgvector (HNSW)  (DeepSeek-R1)    push alerts      + Grafana
```

- 🤖 **RAG over incident history** using **Spring AI** with a **pgvector** store and a local **Ollama** model, with services for knowledge-base indexing and RAG incident narratives
- 🔐 **Security:** a standalone **Spring Authorization Server** issuing JWTs, with the gateway and backend as OAuth2 resource servers
- 🧱 **Resilience:** a queue service with scheduled flush, plus poll-interval and inactivity thresholds for node monitoring
- 📲 **Push notifications:** Firebase Cloud Messaging and SNS-style notification handling
- 🗄️ **Data:** PostgreSQL schema managed with **Flyway** migrations (incidents, network nodes, VLANs, supervisors, resolved incidents)
- 🐳 **Ops:** Docker Compose for the whole stack, Prometheus metrics, secrets mounted as files

`Spring Boot` `Spring AI` `Spring Security` `Spring Cloud Gateway` `pgvector` `Ollama` `Flyway` `Docker` `Prometheus` `React Native`

---

### 🕹️ [ps1emu](https://github.com/Prashanth-Adibhatla/ps1emu)
**A PlayStation 1 emulator written in C++ (Visual Studio solution).**

The core library models the console's hardware as separate components:

| Area | Components in the repo |
|---|---|
| **CPU** | R3000-style CPU, instruction decoder, **COP0**, interrupt control |
| **Graphics** | **GPU**, **GTE** (geometry coprocessor), renderer with shaders (VRAM copy, CLUT, 16/24-bit output) |
| **Audio** | **SPU** and an audio queue |
| **Storage / media** | **CD-ROM** drive with `.bin` / `.cue` parsing, **CD-XA**, **MDEC** macroblock decoder (FMV), memory cards |
| **System** | DMA, timers, BIOS loading, memory map and control, controller ports, serial port, **save states**, event scheduler |

Layered as `Foundation` → `Render` (OpenGL via Glad) → `PlaystationCore` → `App`.

`C++` `OpenGL` `GLSL` `Visual Studio`

---

### 🧠 [Explainable CNN + ViT for Brain Tumour Detection](https://github.com/Prashanth-Adibhatla/Explainable-CNN-VIT-model-for-brain-tumour-detection)
**A full-stack medical-imaging AI app with a two-stage pipeline and explainability.**

- **Detection:** ViT-Base/16 binary classifier (tumour vs no tumour)
- **Classification:** ResNet-50 for Glioma, Meningioma and Pituitary
- **Explainable AI:** Grad-CAM heatmap, binary tumour mask and overlay views
- **Clinical-style PDF report** generated with ReportLab
- **Stack:** Flask API (`/predict`, `/report`, `/health`) plus a React + Vite frontend

`Vision Transformer` `ResNet-50` `Grad-CAM` `Flask` `React`

---

### 🔐 [X.509 Vulnerability Simulator](https://github.com/Prashanth-Adibhatla/crypto-x.509-vulnerability-simulator)
**An educational simulation of how X.509 certificate-chain flaws were exploited, and how they were fixed.**

- Demonstrates **MD5 collision attacks**, **RSA e=3 cube-root forgery** and **MITM attacks**
- Compares a **weak** and a **strong** certificate validator side by side
- **Custom-built crypto stack with no third-party crypto libraries:** AES-GCM, RSA, RSA-PSS and SHA-256 implemented from scratch
- **PostgreSQL-backed** certificate store, a GUI, and a full project report (PDF)

`Python` `PostgreSQL` `Applied Cryptography` `PKI`

---

## 🧩 More Projects

| Project | What it is | Stack |
|---|---|---|
| ✍️ [**Canvas Text & Character Detection (TrOCR)**](https://github.com/Prashanth-Adibhatla/Canvas-text-and-character-detection-using-transferlearning-with-VIT-model) | Real-time handwriting recognition from a **Wacom pen tablet** using Microsoft's **TrOCR** (ViT encoder + Transformer decoder), comparing pretrained vs fine-tuned models. I also documented why ViTs struggle on isolated characters and why CNNs suit that task better. | `Jupyter` `TrOCR` `Transfer Learning` |
| 👾 [**CHIP-8 Emulator**](https://github.com/Prashanth-Adibhatla/chip-8) | A CHIP-8 interpreter in C++11 with the 4 KB memory, 16 registers, stack, timers, 64×32 display and keypad, rendered with **SDL2** and built with CMake. Bundled with 20+ classic ROMs (Pong, Tetris, Space Invaders and more). | `C++11` `SDL2` `CMake` |
| 💬 [**Autobot**](https://github.com/Prashanth-Adibhatla/autobot) | A Django-based WhatsApp marketing-automation platform with modular apps (CRM integration, social hub, message shooter, data wrangler, public API) and a Dockerised setup. | `Python` `Django` `Docker` |
| ♟️ [**Chess**](https://github.com/Prashanth-Adibhatla/Chess) | A local web-based chess app built with vanilla JavaScript. | `JavaScript` `HTML` `CSS` |
| 🎮 [**HackHub Game**](https://github.com/bawling-hackhub/hackhub-game) | A game built for **HackHub 2025** with the `bawling-hackhub` team. | `GDScript` `Godot` |

<details>
<summary><b>📚 Forked repos I use for learning and reference</b></summary>

<br/>

| Fork | Why I keep it |
|---|---|
| [project-based-learning](https://github.com/Prashanth-Adibhatla/project-based-learning) | Curated list of project-based tutorials |
| [SDFC](https://github.com/Prashanth-Adibhatla/SDFC) | System design roadmap and resources |
| [coding-resources](https://github.com/Prashanth-Adibhatla/coding-resources) | Roadmaps for learning to code |
| [VIT_sem6_notes](https://github.com/Prashanth-Adibhatla/VIT_sem6_notes) | Semester notes compilation |
| [Dynamic-Parkour-System](https://github.com/Prashanth-Adibhatla/Dynamic-Parkour-System) | Unity parkour controller (C#), studied for game dev |
| [Amazon-Clone](https://github.com/Prashanth-Adibhatla/Amazon-Clone) | HTML / CSS / JS frontend practice |

</details>

---

## 🧰 Tech Stack

### 🤖 Generative AI
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=for-the-badge&logo=pinecone&logoColor=white)
![Spring AI](https://img.shields.io/badge/Spring%20AI-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-Pipelines-7C3AED?style=for-the-badge)

### ☕ Backend
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring JDBC](https://img.shields.io/badge/Spring%20JDBC-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=for-the-badge&logo=flyway&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

### ⚙️ Systems, GPU & Emulation
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Pybind11](https://img.shields.io/badge/Pybind11-Python%20%E2%86%94%20C++-3776AB?style=for-the-badge)
![OpenGL](https://img.shields.io/badge/OpenGL-5586A4?style=for-the-badge&logo=opengl&logoColor=white)
![SDL2](https://img.shields.io/badge/SDL2-1B6AC6?style=for-the-badge)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white)

### 🧪 ML, Data & Frontend
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Godot](https://img.shields.io/badge/Godot-478CBF?style=for-the-badge&logo=godotengine&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## ⚡ Competitive Programming

I solve problems to keep my fundamentals sharp: graphs, dynamic programming, greedy strategies, number theory and more. The same habits (complexity analysis, memory access patterns, parallel thinking) show up in my GPU kernels and backend work.

<!-- 👉 Replace YOUR_USERNAME with your real handles. Delete any platform you don't use. -->
<div align="center">

[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/YOUR_USERNAME)
[![Codeforces](https://img.shields.io/badge/Codeforces-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/YOUR_USERNAME)
[![CodeChef](https://img.shields.io/badge/CodeChef-5B4638?style=for-the-badge&logo=codechef&logoColor=white)](https://www.codechef.com/users/YOUR_USERNAME)

</div>

---

## 📊 GitHub Stats

<div align="center">

<img height="180" src="https://github-readme-stats.vercel.app/api?username=Prashanth-Adibhatla&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" />
<img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Prashanth-Adibhatla&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=Prashanth-Adibhatla&theme=tokyonight&hide_border=true" />

</div>

---

## 🤝 Let's Connect

Open to collaborating on **Gen AI / RAG projects**, **Spring microservices**, **GPU computing**, **emulation** and **hackathons**.

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Prashanth--Adibhatla-181717?style=for-the-badge&logo=github)](https://github.com/Prashanth-Adibhatla)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_USERNAME)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL)

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=120&section=footer" width="100%"/>
