### 🌐 Sitio Web Institucional 

Este repositorio contiene el sitio web institucional utilizado como contenido estático en un entorno Kubernetes con Minikube.
Fue creado a partir de un fork del repositorio original: ewojjowe/static-website

✏️ Modificaciones realizadas al sitio web

El sitio fue adaptado y personalizado con los siguientes cambios:

### 1. ✅ Personalización del contenido

Se abrió el proyecto en VS Code con:

File → Open Folder → devops-web

y se editaron los archivos HTML y CSS correspondientes.


### 2. 📬 Formulario de contacto responsive

El formulario de contacto fue adaptado para funcionar correctamente en distintas resoluciones:

- **En pantallas grandes**: se muestra a la derecha junto con un div informativo a la izquierda.
- **En pantallas pequeñas**: se centra el formulario y se oculta el div izquierdo.

**Media Query utilizada:**


@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
    justify-content: center;
  }

  .contact-form-left {
    display: none;
  }

  .contact-form {
    margin: 0 auto;
    width: 90%;
    max-width: 500px;
  }
}

### 3. 🍔 Menú desplegable tipo hamburguesa
Se incorporó un menú hamburguesa para mejorar la navegación móvil.

HTML agregado:


<input type="checkbox" id="menu-toggle" class="menu-toggle">
<label for="menu-toggle" class="menu-button">
  <span class="menu-icon"></span>
</label>


Se oculta el menú por defecto y se muestra cuando se marca el checkbox.

Media queries para diferentes resoluciones:

Se adaptaron estilos para pantallas pequeñas (≤768px) y muy pequeñas (≤480px), permitiendo una experiencia más fluida.


### 🧰 Requisitos para manipular este repositorio desde tu directorio local

- Git instalado
- Conexión con tu cuenta de GitHub

### 📝 Comandos útiles

### 📥 Clonar el repositorio

git clone https://github.com/TU_USUARIO/static-website.git
cd static-website
Reemplazá TU_USUARIO por tu nombre de usuario real en GitHub.

### 🖊️ Editar y modificar contenido

Realizá las modificaciones que necesites (HTML, CSS, imágenes, etc.) dentro del repositorio clonado.

### 💾 Guardar y subir cambios a GitHub

git status                         # Verificar qué archivos fueron modificados
git add .                          # Agregar todos los cambios
git commit -m "Personalizo contenido web institucional"
git push origin main               # Subir los cambios al branch principal

📌 Nota: en algunos repositorios el branch principal puede ser master en lugar de main.

### 🔄 Descargar cambios del repositorio remoto

git pull origin main