# Responsive Navbar with Dropdown Menu

Este proyecto proporciona un ejemplo de un navbar responsivo con un menú desplegable, utilizando HTML, CSS y JavaScript. El diseño es adaptable y funcional tanto en dispositivos móviles como en pantallas grandes.

## Características

- Navbar responsivo con un menú desplegable.
- Enlaces de navegación que cubren toda el área del `li` para facilitar la usabilidad.
- Botón de acción destacado.
- Diseño estético con efectos `hover`.
- Fácil personalización para otros proyectos.

## Capturas de Pantalla

![Navbar Desktop](/assets/responsive_navbar_desktop.png)
![Navbar Mobile](/assets/responsive_navbar_mobile.png)

## Instalación

1. Clona este repositorio en tu máquina local:

    ```bash
    git clone https://github.com/tu-usuario/responsive-navbar.git
    ```

2. Navega al directorio del proyecto:

    ```bash
    cd responsive-navbar
    ```

3. Abre `index.html` en tu navegador para ver el navbar en acción.

## Uso

Puedes reutilizar este navbar en tus proyectos siguiendo estos pasos:

1. **HTML**: Copia el marcado HTML en el archivo `index.html` o en la sección correspondiente de tu proyecto.

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>Responsive Navbar</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <header>
            <div class="navbar">
                <div class="logo">
                    <a href="#">Web Design</a>
                </div>
                <ul class="links">
                    <li><a href="hero">Home</a></li>
                    <li><a href="about">About</a></li>
                    <li><a href="services">Services</a></li>
                    <li><a href="contact">Contact</a></li>
                </ul>
                <a href="#" class="action_btn">Get started</a>
                <div class="toggle_btn">
                    <i class="fa-solid fa-bars"></i>
                </div>
            </div>
            <div class="dropdown_menu">
                <ul class="links">
                    <li><a href="hero">Home</a></li>
                    <li><a href="about">About</a></li>
                    <li><a href="services">Services</a></li>
                    <li><a href="contact">Contact</a></li>
                    <li><a href="#" class="action_btn">Get started</a></li>
                </ul>
            </div>
        </header>
        
        <script src="script.js" async defer></script>
    </body>
    </html>
    ```

2. **CSS**: Copia los estilos CSS en el archivo `style.css` o en el archivo de estilos correspondiente de tu proyecto.

    ```css
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Times New Roman', Times, serif;
    }

    body {
        height: 100vh;
        background-color: #fff;
        background-image: url("/assets/9154465.jpg");
        background-size: cover;
        background-position: center;
    }

    li {
        list-style: none;
    }

    a {
        text-decoration: none;
        color: #fff;
        font-size: 1rem;
        display: block; /* Hace que el enlace cubra toda el área del li */
        width: 100%;
        height: 100%;
        padding: 0.7rem;
    }

    a:hover {
        color: chocolate;
    }

    /*  HEADER */

    header {
        position: relative;
        padding: 0 2rem;
    }

    .navbar {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .navbar .logo a {
        font-size: 1.5rem;
        font-weight: bold;
    }

    .navbar .links {
        display: flex;
        gap: 2rem;
    }

    .navbar .toggle_btn {
        color: #fff;
        font-size: 1.5rem;
        cursor: pointer;
        display: none;
    }

    .action_btn {
        background-color: chocolate;
        color: #fff;
        padding: 0.5rem 1rem;
        border: none;
        outline: none;
        border-radius: 15px;
        font-size: 15px;
        font-weight: bold;
        transition: scale 0.2s ease;
    }

    .action_btn:hover {
        scale: 1.05;
        color: #fff;
    }

    .action_btn:active {
        scale: 0.95;
    }

    /* DROPDOWN MENU */
    .dropdown_menu {
        position: absolute;
        right: 2rem;
        top: 60px;
        width: 300px;
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(15px);
        border-radius: 15px;
        overflow: hidden;
    }

    .dropdown_menu li {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .dropdown_menu li:hover {
        background-color: rgba(240, 248, 255, 0.9); /* aliceblue con opacidad */
        border-radius: 30px;
    }

    .dropdown_menu li:not(.action_btn) a:hover {
        color: #000; /* Color del texto negro o cualquier color oscuro */
    }

    .dropdown_menu .action_btn {
        width: 100%;
        display: flex;
        justify-content: center;
    }

    /* RESPONSIVE */

    @media (max-width: 800px) {
        .navbar .links,
        .navbar .action_btn {
            display: none;
        }

        .navbar .toggle_btn {
            padding: 10px;
            display: block;
        }
    }
    ```

3. **JavaScript**: Asegúrate de incluir el archivo `script.js` en tu proyecto para manejar la funcionalidad del menú desplegable.

    ```javascript
    // script.js
    document.addEventListener('DOMContentLoaded', function() {
        const toggleBtn = document.querySelector('.toggle_btn');
        const dropdownMenu = document.querySelector('.dropdown_menu');

        toggleBtn.addEventListener('click', function() {
            dropdownMenu.classList.toggle('open');
        });
    });
    ```

## Personalización

Para personalizar este navbar para otros proyectos, puedes modificar:

- **Estilos**: Cambia los colores, fuentes, tamaños y otros estilos en `style.css`.
- **Estructura**: Modifica los enlaces y el contenido en el HTML según tus necesidades.
- **Funcionalidad**: Agrega o modifica el comportamiento con JavaScript en `script.js`.

## Contribuciones

Si deseas contribuir a este proyecto, por favor sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama con tu nueva funcionalidad (`git checkout -b nueva-funcionalidad`).
3. Haz commit de tus cambios (`git commit -am 'Agrega nueva funcionalidad'`).
4. Haz push a la rama (`git push origin nueva-funcionalidad`).
5. Crea un Pull Request.

## Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).

## Contacto

Para cualquier consulta o comentario, puedes contactarme en [tu-email@dominio.com](mailto:bfbacchi@gmail.com).
