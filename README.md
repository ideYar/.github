<div align="center">

<img src="https://avatars.githubusercontent.com/u/185948616?s=200&v=4" width="110" alt="IdeYar logo" />

# IdeYar

**Turn ideas into funded projects.**
A platform where creators share their ideas and the community backs the ones worth building.

[![Go](https://img.shields.io/badge/Go-1.23-00ADD8?logo=go&logoColor=white)](https://github.com/ideYar/IdeYar-server)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://github.com/ideYar/IdeYar-front)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://github.com/ideYar/IdeYar-front)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)](https://github.com/ideYar/IdeYar-server)
[![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)](#)

</div>

---

## 📦 Repositories

| Repository | Description | Stack | License |
|---|---|---|---|
| [**IdeYar-server**](https://github.com/ideYar/IdeYar-server) | Back-end API | Go · gRPC · gRPC-Gateway · GORM · PostgreSQL · JWT | MIT |
| [**IdeYar-front**](https://github.com/ideYar/IdeYar-front) | Web client | React · TypeScript · Vite · MUI · Redux Toolkit · i18next | GPL-2.0 |

## 🏗️ Architecture

```mermaid
flowchart LR
    U([User]) --> F["IdeYar-front<br/>React + Vite"]
    F -- "REST / JSON" --> G["gRPC-Gateway"]
    G -- gRPC --> S["IdeYar-server<br/>Go services"]
    S -- GORM --> DB[(PostgreSQL)]
```

- **API-first:** contracts are defined in Protocol Buffers; gRPC-Gateway exposes them as a REST/JSON API for the web client.
- **Auth:** stateless JWT authentication.
- **Persian-first UI:** full RTL layout and Jalali (Shamsi) calendar support, with i18n built in.
- **Quality:** end-to-end tests on the server, Jest + Testing Library on the client, and CI via GitHub Actions.

## 🚀 Quick start

```bash
# Back end
git clone https://github.com/ideYar/IdeYar-server.git
cd IdeYar-server
docker compose up -d

# Front end
git clone https://github.com/ideYar/IdeYar-front.git
cd IdeYar-front
npm install
npm run dev
```

See each repository's README for configuration details.

## 🤝 Contributing

Issues and pull requests are welcome. Please open an issue to discuss larger changes before starting work.