muy importante siempre crear el entorno virtual primero y luego crear el proyecto 

"django"

Crea un entorno virtual:

"python -m venv venv"

activa el entorno:

"python -m venv venv"

en Visual Estudio Code con "F1" seleccionar el interpreter

instalamos django

"pip install django"

limpiar la terminal "cls"

actualizar "pip"

"python -m pip install --upgrade pip"

creamos el proyecto en django con:

"django-admin startproject portfolio ."

levantamos el servicio:

"python manage.py runserver"

creamos la aplicacion dentro del proyecto:

"python manage.py startapp blog"

"python manage.py startapp portafolio"

en 

"portfolio, setting.py" conectamos las aplicaciones al proyecto principal en 

"INSTALLED_APPS" 

en 

"portafolio, models.py" creamos las clases 

instalar un modulo con:

"pip install pillow"

realizar las migraciones siempre despues de crear las clases en "models.py"

"python manage.py makemigrations"

"python manage.py migrate"

ingresamos a la aplicacion en el navegador:

"http://127.0.0.1:8000/admin/login/?next=/admin/"

creamos el super usuario con:

"python manage.py createsuperuser"

ingresar la contraeña: "ROOT"

en 

"portafolio, admin.py" agregamos importamos "Project"

en 

"portfolio, settings.py" en "STATIC_URL = '/static/'" configuramos para que sirva 

una carpeta para las imagenes

"STATIC_URL = '/static/'

MEDIA_ROOT = BASE_DIR / 'media'" con esta ruta se creo una carpeta llamada "media" 

en el proyecto principal "portfolio"

para poder mostrar la imagen falta crear una nueva ruta debajo de la siguiente forma

"MEDIA_URL = '/media/'"

creamos una carpeta "templates" en portafolio y un archivo dentro

"portafolio, templates, home.html"

definimos la vista en 

"portafolio, views.py"

en "portfolio, urls.py" importamos la vista de "portafolio" y agregamos la ruta

en "blog, urls.py" creamos el archivo "urls.py"

en "blog" creamos la carpeta "templates"


en "blog, templates, post.html"

en "blog, views.py" creamos la funcion post

en "blog, urls.py" importamos la vista

importamos la ruta

"from django.urls import path
from .views import render_posts

urlspatterns = [
    path('', render_posts, name='posts'),
]"

en "portfolio, urls.py" declaramos una nueva ruta

en "blog, models.py" creamos el modelo 

en "blog, admin.py" registramos el modelo

hacemos la migracion del modelo con:

"python manage.py makemigrations"

"python manage.py migrate"

en "blog, urls.py" agregamos las demas rutas para poder ver cada articulo por 

separado

en "blog, templates, post_detail.html" creamos el archivo "post_detail.html"

en "portafolio, templates, layout.html" creamos el archivo "layout.html"

en "portafolio, templates, partials, navbar.html" creamos la carpeta "partials" y 

dentro el archivo "navbar.html"

en "portafolio, static"  creamos la carpeta "static"

dentro de "portafolio, static, main.css" creamos el archivo "main.css"

crear el "requirement.txt" se debe ejecuar:

"pip freeze > requirements.txt"

agregar el ".gitignore" para ignarar archivos que no sean necesarios cuando se 

empuje al repositorio github

con " git init" inicializamos el proyecto y haci verificamos que carpetas 

no son necesarias subirlas

------------------------------------------------------------------------------------
comandos para desplegar una aplicacion en PythonAnywhare

"git clone https://github.com/Dark-Data-Science/Web.git"

"mkvirtualenv --python=/usr/bin/python3.8 venv"

"cd Web"

"pip install -r requirements.tx"

<img src="{% static 'porta/profile.PNG' %}" alt="">



<header class="row bg-black">
    <div class="col-md-4">
        <img src="{% static 'porta/avatar.png' %}" alt="">
    </div>

    <div class="col-md-8 my-auto p-4">
        <h1> Hi I am <strong>Jose Ignacio</strong></h1>
        <h3>I am Data Scientisc and FullStack Developer</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Impedit laboriosam esse earum harum 
            nostrum eveniet, pariatur facere placeat, id, ipsa asperiores. Dignissimos iste quaerat 
            temporibus non! Nobis cumque inventore facilis alias tempore debitis velit. Incidunt tenetur 
            corporis sit at sunt voluptates deleniti pariatur magnam natus debitis eum cumque doloremque 
            quam, repudiandae assumenda dolor! Minima nemo sapiente, assumenda quo accusantium nesciunt 
            ex quia fuga vitae illo sunt eaque velit maxime atque at amet beatae natus aperiam dolores 
            aut, placeat labore cupiditate eligendi. Voluptas accusantium labore illo excepturi neque. 
            Optio sunt ducimus natus ut accusamus quibusdam error fugiat facere aspernatur. Odio, 
            inventore?</p>
            <a class="btn btn-primary btn-lg rounded-0 my-3" href="{% static 'porta/CV_Jose_Viola.pdf'%}" target="_blank"
            >Download CV</a>
    </div>
</header>
















































































































