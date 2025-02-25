# Usa una imagen oficial de Python con TensorFlow
FROM tensorflow/tensorflow:2.13.0

# Establece el directorio de trabajo
WORKDIR /app

# Copia los archivos de la aplicación
COPY . /app

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Expone el puerto 8080 para Google Cloud Run
EXPOSE 8080

# Define el comando de inicio usando Gunicorn
CMD ["gunicorn", "-b", "0.0.0.0:8080", "app:app"]

