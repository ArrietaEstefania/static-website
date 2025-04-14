# 🌐 Sitio Web Institucional

Este repositorio contiene el **sitio web institucional** utilizado como contenido estático en un entorno **Kubernetes con Minikube**.

Fue creado a partir de un **fork** del repositorio original: [ewojjowe/static-website](https://github.com/ewojjowe/static-website).

---

## ✏️ Modificaciones realizadas al sitio web

El sitio fue adaptado y personalizado con los siguientes cambios:

### 1. ✅ Personalización del contenido

Se abrió el proyecto en **VS Code**:

```mathematica
File → Open Folder → devops-web
```

Y se editaron los archivos **HTML** y **CSS** correspondientes.

---

### 2. 📬 Formulario de contacto responsive

El formulario de contacto fue adaptado para funcionar correctamente en distintas resoluciones:

- **Pantallas grandes:** se muestra a la derecha junto con un div informativo a la izquierda.
- **Pantallas pequeñas:** se centra el formulario y se oculta el div izquierdo.

**Media Query utilizada:**

```css
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
```

---

### 3. 🍔 Menú desplegable tipo hamburguesa

Se incorporó un **menú hamburguesa** para mejorar la navegación móvil.

**HTML agregado:**

```html
<input type="checkbox" id="menu-toggle" class="menu-toggle">
<label for="menu-toggle" class="menu-button">
  <span class="menu-icon"></span>
</label>
```

**Media queries para distintas resoluciones:**

```css
@media only screen and (max-width: 768px) {
  .menu-button {
    display: block;
  }

  .main-nav {
    position: fixed;
    top: 0;
    right: -300px;
    width: 250px;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.85);
    padding-top: 80px;
    transition: right 0.3s ease;
    z-index: 998;
  }

  .main-nav li {
    display: block;
    margin: 15px 0;
    text-align: center;
  }

  .main-nav li a {
    padding: 10px;
    font-size: 18px;
    display: block;
  }

  .menu-toggle:checked ~ .main-nav {
    right: 0;
  }

  .menu-toggle:checked ~ .menu-button .menu-icon {
    background-color: transparent;
  }

  .menu-toggle:checked ~ .menu-button .menu-icon::before {
    transform: rotate(45deg);
    top: 0;
  }

  .menu-toggle:checked ~ .menu-button .menu-icon::after {
    transform: rotate(-45deg);
    top: 0;
  }
}
```

---

## 🧰 Requisitos para manipular este repositorio

- Tener **Git** instalado.
- Conexión con tu cuenta de **GitHub**.

---

## 📝 Comandos útiles

### 📥 Clonar el repositorio

```bash
git clone https://github.com/TU_USUARIO/static-website.git
cd static-website
```

> **Nota:** Reemplazá `TU_USUARIO` por tu nombre de usuario real en **GitHub**.

---

### 🖊️ Editar y modificar contenido

Realizá las modificaciones necesarias (**HTML**, **CSS**, imágenes, etc.) dentro del repositorio clonado.

---

### 💾 Guardar y subir cambios a GitHub

```bash
git status                         # Verificar qué archivos fueron modificados
git add .                          # Agregar todos los cambios
git commit -m "Personalizo contenido web institucional"
git push origin master             # Subir los cambios al branch principal
```

> **Nota:** en algunos repositorios el branch principal puede ser `main` en lugar de `master`.

---

### 🔄 Descargar cambios del repositorio remoto

```bash
git pull origin master
```

---
