una SPA para gestión de eventos con roles de usuario.


# 📅SPA de Gestión de Eventos – JavaScript (Módulo 3)

Aplicación web de una sola página (SPA) desarrollada en JavaScript puro, enfocada en la gestión de eventos. Permite a usuarios registrarse, iniciar sesión, ver y asistir a eventos. Los administradores pueden crear, editar y eliminar eventos. El proyecto cumple con todos los criterios técnicos del Módulo 3 de formación en desarrollo web.

---

##  Funcionalidades principales

- *Autenticación de usuarios* (login y registro)
- *Roles diferenciados*:
  - admin: puede crear, editar y eliminar eventos
  - user: puede registrarse para asistir a eventos
- *SPA con enrutamiento manual* (hash routing)
- *Persistencia con localStorage*
- *CRUD completo de eventos usando Fetch API*
- *Validaciones de campos, capacidad y acceso*
- *Manejo de errores y alertas informativas*

---

## 🧱 Estructura del proyecto

📁 js/ │ ├── api.js          # Módulo de consumo de API REST │ ├── auth.js         # Autenticación y sesión de usuario │ ├── router.js       # Enrutador SPA (hash routing) │ └── views.js        # Lógica de interfaz para cada vista

📄 index.html          # Entrada principal 🎨 styles.css          # Estilos generales 📝 README.md           # Documentación del proyecto

---

## 🧪 Requisitos

- Navegador moderno (Chrome, Firefox, Edge)
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) para entorno local
- [JSON Server](https://github.com/typicode/json-server) para simular la API REST

---

## 🛠 Instalación y uso

1. Clona o descarga este repositorio:

```bash
git clone https://github.com/usuario/proyecto-eventos-spa

2. Instala JSON Server globalmente (si no lo tienes):



npm install -g json-server

3. Crea un archivo db.json con esta estructura:



{
  "users": [],
  "events": []
}

4. Inicia el servidor de la API:



json-server --watch db.json --port 3000

5. Abre el proyecto en VSCode y ejecuta index.html con Live Server.



```
---

🌐 Rutas SPA disponibles

Ruta	Descripción

#/login	Iniciar sesión
#/register	Crear una cuenta
#/dashboard	Bienvenida según el rol
#/dashboard/events	Ver eventos disponibles
#/dashboard/events/create	Crear nuevo evento (admin)



---

💡 Tecnologías utilizadas

JavaScript (ES6+)

Fetch API

localStorage

JSON Server

HTML5 + CSS3


---

✅ Buenas prácticas implementadas

Modularización de código

Uso de async/await para asincronía

Control de errores con try/catch

Separación lógica y visual por archivos

Uso de variables universales (api.base, etc.)

Comentarios claros y explicativos

Rutas protegidas según autenticación


---

🙋 Autenticación

Los usuarios se almacenan con:

name

email

password

role (por defecto: "user", o "admin" manualmente)


Se mantiene la sesión mediante localStorage.


---

🔒 Seguridad y validaciones

Un email no puede registrarse dos veces

Solo el admin puede acceder a crear, editar, eliminar

Un usuario no puede asistir dos veces al mismo evento

Los eventos respetan límite de capacidad

---

 Autor

> Proyecto desarrollado por Joseph Hernández como entrega del Módulo 3 de JavaScript.
