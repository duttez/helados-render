# helados-render
Práctica 10.1 de IA

El objetivo de esta práctica es desplegar en la nube una aplicación de Inteligencia Artificial y comprobar su funcionamiento mediante una API REST.

Se trabajará todo el proceso:
uso de un modelo de IA,
creación de una API,
despliegue en la nube,
y prueba del servicio desde Internet.


# Tecnologías utilizadas.
Python
Scikit-learn
Flask
GitHub
Render
Thunder Client

# Pasos para ejecutar el proyecto en local.
En la terminal ejecutamos:
- pip install -r requirements.txt
- python entrenar_modelo.py
- python app.py

En el navegador introducimos las siguientes direcciones:
- 127.0.0.1:5000/
- 127.0.0.1:5000/health

Para usar el modelo de predicción lo hacemos desde VS Code, con la extensión Thunder Client:
- New Request
- Cambiamos el método GET por POST.
- En el apartado URL escribimos http://127.0.0.1:5000/predict.
- En la pestaña Body/JSON escribimos la temperatura sobre la que queremos trabajar en el formato del diccionario --> {"temperatura":30}
- Al pulsar SEND nos aparece la predicción a la derecha


# Pasos para el despliegue en la nube.
- Accedemos a la web Render, si no tenemos cuenta nos creamos una.
- Conectamos Render con GitHub.
- Creamos un Web Service a partir del repositorio.
- Elegimos el repositorio en el que hemos subido los archivos y configuramos el servicio: poner Python 3 como lenguaje y python app.py en Start Command.  También elegir el modo gratuito que para estas pruebas es suficiente.
- Pulsamos sobre Deploy Web Service y esperamos a que termine de ejecutarse.


# Ejemplo de uso del endpoint /predict.
Desde Thunder Client, en el apartado body:
- Elegimos POST.
- Introducimos la dirección que nos ha facilitado Render seguida de /predict
- En JSON introducimos el dato en el formato {"temperatura":30} donde el valor numérico se puede cambiar.
- Pulsamos sobre SEND y en la parte derecha aparecerá la predicción de ventas en función de la temperatura dada. 


# URL del servicio desplegado en Render.
https://helados-render-trqn.onrender.com 
