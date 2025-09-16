**Nota**: Este proyecto está en desarrollo activo. Las características pueden cambiar y se recomienda usarlo en producción con las debidas precauciones.
MedicalKenshin - Sistema de Gestión Médica

MedicalKenshin es una aplicación web desarrollada en Django para la gestión integral de consultorios médicos. Permite a los profesionales de la salud administrar pacientes, citas, historiales médicos, consultas, recetas y certificados médicos de manera eficiente.

✨ Características Principales
Gestión de Doctores: Registro y administración de perfiles médicos

Gestión de Pacientes: CRUD completo de pacientes con historial médico

Sistema de Citas: Agendamiento y seguimiento de citas médicas

Historial Clínico: Registro detallado del historial médico de pacientes

Consultas Médicas: Registro de consultas con diagnóstico y tratamiento

Recetas Médicas: Generación y envío de recetas por email

Certificados Médicos: Creación de certificados médicos con PDF

Dashboard Interactivo: Panel de control con estadísticas y resumen de actividades

Calendario de Citas: Vista mensual de todas las citas programadas

🚀 Tecnologías Utilizadas
Backend: Django 4.2.7

Frontend: HTML5, CSS3, JavaScript, Bootstrap

Base de Datos: SQLite (desarrollo), compatible con PostgreSQL/MySQL

Autenticación: Sistema de autenticación de Django

Generación de PDF: Bibliotecas Python para documentos médicos

Envío de Emails: Integración con servidores SMTP

📦 Instalación
Prerrequisitos
Python 3.8 o superior

pip (gestor de paquetes de Python)

virtualenv (recomendado)

Pasos de Instalación
Clonar el repositorio:

bash
git clone <url-del-repositorio>
cd medikenshin
Crear un entorno virtual:

bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
Instalar dependencias:

bash
pip install -r requirements.txt
Configurar la base de datos:

bash
python manage.py makemigrations
python manage.py migrate
Crear superusuario:

bash
python manage.py createsuperuser
Ejecutar el servidor:

bash
python manage.py runserver
Acceder a la aplicación:
Abre tu navegador y ve a http://127.0.0.1:8000

🏗️ Estructura del Proyecto
text
medikenshin/
├── medical_app/
│   ├── migrations/         # Migraciones de la base de datos
│   ├── templates/          # Plantillas HTML
│   ├── admin.py           # Configuración del admin de Django
│   ├── forms.py           # Formularios de la aplicación
│   ├── models.py          # Modelos de datos
│   ├── urls.py            # URLs de la aplicación
│   ├── views.py           # Vistas de la aplicación
│   └── utils.py           # Utilidades (generación de PDFs)
├── medikenshin/
│   ├── settings.py        # Configuración del proyecto
│   ├── urls.py            # URLs principales
│   └── wsgi.py            # Configuración WSGI
├── static/                # Archivos estáticos (CSS, JS, imágenes)
├── media/                 # Archivos multimedia subidos
├── requirements.txt       # Dependencias del proyecto
└── manage.py              # Script de gestión de Django
👨‍💻 Uso
Para Doctores
Registro: Crear una cuenta de doctor

Login: Acceder al sistema con credenciales

Perfil: Completar información profesional

Dashboard: Ver resumen de pacientes y citas

Gestión de Pacientes
Añadir nuevos pacientes con información completa

Buscar y filtrar pacientes

Ver historial médico completo

Editar información de pacientes

Sistema de Citas
Programar nuevas citas

Gestionar estados de citas (programada, confirmada, completada, cancelada)

Vista de calendario con todas las citas

Recordatorios de citas del día

Consultas Médicas
Registrar consultas después de cada cita

Añadir diagnósticos y tratamientos

Gestionar seguimientos médicos

Recetas y Certificados
Generar recetas médicas con medicamentos y dosificación

Crear certificados médicos con días de reposo

Enviar documentos por email a pacientes

Descargar documentos en formato PDF

⚙️ Configuración
Variables de Entorno
Crea un archivo .env en la raíz del proyecto con:

python
DEBUG=True
SECRET_KEY=tu-clave-secreta-aqui
DATABASE_URL=sqlite:///db.sqlite3
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=tu-email@gmail.com
EMAIL_HOST_PASSWORD=tu-contraseña-de-app
Base de Datos
Por defecto usa SQLite. Para PostgreSQL o MySQL:

Instalar el adaptador de base de datos correspondiente

Configurar en settings.py:

python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'nombredb',
        'USER': 'usuario',
        'PASSWORD': 'contraseña',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
