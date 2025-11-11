<!-- Shields -->
[![Python](https://img.shields.io/badge/Python-3.11%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115%2B-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18.3%2B-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![Oracle](https://img.shields.io/badge/Oracle%20DB-19c%2B-F80000?logo=oracle&logoColor=white)](https://www.oracle.com/database/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-En%20Desarrollo-brightgreen)](#)

<p align="center">
  <img src="https://via.placeholder.com/800x300.png?text=Residencial+del+Maule+-+Linares" alt="Banner Residencial del Maule" />
</p>

<h1 align="center">Residencial del Maule - Sistema CRUD</h1>

<p align="center">
  <strong>Sistema de gestión para el Hostal Residencial del Maule, ubicado en Linares, Chile.</strong>
</p>

---

## 📋 Descripción del Proyecto

Este es un sistema **CRUD completo** desarrollado para el **Hostal Residencial del Maule**, un acogedor alojamiento ubicado en la ciudad de **Linares, Región del Maule, Chile**.  
El sistema permite gestionar reservas, huéspedes, habitaciones, pagos y reportes, con una interfaz moderna y eficiente.

---

## 🛠️ Tecnologías Utilizadas

| Capa         | Tecnología                     | Versión       |
|-------------|--------------------------------|---------------|
| **Frontend** | React + Vite + Tailwind CSS    | `^18.3.0`     |
| **Backend**  | Python + FastAPI               | `^3.11` / `^0.115` |
| **Base de datos** | Oracle Database           | `19c+`        |
| **Despliegue** | Docker (opcional)            | -             |

---

## ✨ Características Principales

- Registro y gestión de **huéspedes**
- Administración de **habitaciones** (disponibilidad, tipo, precio)
- Sistema de **reservas** con check-in / check-out
- Control de **pagos** y facturación
- Panel de administrador con reportes
- Diseño responsive y amigable

---

## 🚀 Inicio Rápido

### Prerrequisitos

- Python 3.11+
- Node.js 18+
- Oracle Database (local o en la nube)
- Git

### Instalación

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/residencial-del-maule-crud.git
cd residencial-del-maule-crud

# Backend
cd backend
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
pip install -r requirements.txt

# Frontend
cd ../frontend
npm install
npm run dev
