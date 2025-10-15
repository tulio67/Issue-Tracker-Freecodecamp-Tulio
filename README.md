# Issue Tracker - FreeCodeCamp Project

Este es un proyecto completo de Issue Tracker desarrollado para cumplir con los requisitos del curso de QA de FreeCodeCamp.

## ✅ Estado del Proyecto

**Todos los 14 tests funcionales están pasando** ✨

## 🚀 Instalación y Ejecución

### Prerrequisitos
- Node.js (versión 14 o superior)
- Docker (para la base de datos MongoDB)
- Git

### Pasos para ejecutar:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tulio67/Issue-Tracker-Freecodecamp-Tulio.git
   cd Issue-Tracker-Freecodecamp-Tulio
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Iniciar MongoDB con Docker:**
   ```bash
   docker run -d --name mongodb-test -p 27017:27017 mongo:5.0
   ```

4. **Ejecutar el proyecto:**
   ```bash
   npm start
   ```

5. **Ejecutar los tests:**
   ```bash
   npm test
   ```

## 📋 Tests Incluidos

### POST Requests (3/3 ✅)
- ✅ Create an issue with every field
- ✅ Create an issue with only required fields  
- ✅ Create an issue with missing required fields

### GET Requests (3/3 ✅)
- ✅ View issues on a project
- ✅ View issues on a project with one filter
- ✅ View issues on a project with multiple filters

### PUT Requests (5/5 ✅)
- ✅ Update one field on an issue
- ✅ Update multiple fields on an issue
- ✅ Update an issue with missing _id
- ✅ Update an issue with no fields to update
- ✅ Update an issue with an invalid _id

### DELETE Requests (3/3 ✅)
- ✅ Delete an issue
- ✅ Delete an issue with an invalid _id
- ✅ Delete an issue with missing _id

## 🛠 API Endpoints

### POST `/api/issues/{project}`
Crear un nuevo issue.

**Campos requeridos:**
- `issue_title`
- `issue_text`
- `created_by`

**Campos opcionales:**
- `assigned_to`
- `status_text`

### GET `/api/issues/{project}`
Obtener todos los issues de un proyecto. Soporta filtros mediante query parameters.

**Filtros disponibles:**
- `_id`
- `issue_title`
- `issue_text`
- `created_by`
- `assigned_to`
- `status_text`
- `open`

### PUT `/api/issues/{project}`
Actualizar un issue existente.

**Campo requerido:**
- `_id`

**Campos actualizables:**
- `issue_title`
- `issue_text`
- `created_by`
- `assigned_to`
- `status_text`
- `open`

### DELETE `/api/issues/{project}`
Eliminar un issue.

**Campo requerido:**
- `_id`

## 📁 Estructura del Proyecto

```
├── routes/
│   ├── api.js          # Rutas de la API principal
│   └── fcctesting.js   # Rutas para testing de FCC
├── tests/
│   └── 2_functional-tests.js  # Todos los 14 tests funcionales
├── views/
│   ├── index.html      # Página principal
│   └── issue.html      # Vista de issues
├── public/
│   └── style.css       # Estilos
├── models.js           # Modelos de MongoDB (Issue y Project)
├── db-connection.js    # Configuración de la base de datos
├── server.js           # Servidor principal
├── .env               # Variables de entorno (incluido para facilidad)
└── package.json       # Dependencias y scripts
```

## 🔧 Configuración

El archivo `.env` está incluido en el repositorio para facilitar la ejecución inmediata del proyecto:

```env
MONGO_URI="mongodb://127.0.0.1:27017/issue-tracker-test"
PORT=3000
NODE_ENV=test
```

**Nota:** En un entorno de producción, nunca deberías incluir el archivo `.env` en el repositorio.

## 🌐 Demo

Una vez ejecutando, puedes acceder a:
- **Aplicación:** http://localhost:3000/
- **API:** http://localhost:3000/api/issues/{project}

## 📝 Requisitos de FreeCodeCamp Cumplidos

Este proyecto cumple con todos los requisitos especificados en el desafío de FreeCodeCamp:

1. ✅ Envío de POST request con todos los campos
2. ✅ Envío de POST request solo con campos requeridos
3. ✅ Manejo de errores en POST request con campos faltantes
4. ✅ Visualización de issues en un proyecto
5. ✅ Filtrado de issues con uno y múltiples filtros
6. ✅ Actualización de uno y múltiples campos de un issue
7. ✅ Manejo de errores en actualizaciones (ID faltante, campos vacíos, ID inválido)
8. ✅ Eliminación de issues
9. ✅ Manejo de errores en eliminación (ID faltante, ID inválido)
10. ✅ Todos los 14 tests funcionales completos y pasando

## 👨‍💻 Desarrollado por

Tulio - Proyecto para FreeCodeCamp QA Certification

---

¿Tienes preguntas o sugerencias? ¡Siéntete libre de abrir un issue! 🚀
