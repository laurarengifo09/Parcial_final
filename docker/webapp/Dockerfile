# Usar una imagen oficial de Python como base
FROM python

# La instrucción EXPOSE indica los puertos en los cuales un contenedor
# escuchará las conexiones
# Dado que las aplicaciones Flask escuchan en el puerto 5000 por defecto, lo exponemos
EXPOSE 5000

# Establece el directorio de trabajo para las siguientes instrucciones COPY y CMD
# Observa que no hemos creado un directorio con este nombre - esta instrucción
# crea un directorio con este nombre si no existe
WORKDIR /app

# Copia todos los archivos del directorio actual en el contenedor
COPY . .

# Instala los paquetes necesarios especificados en requirements.txt
RUN pip install -r requirements.txt --break-system-packages

# Ejecuta app.py cuando el contenedor se inicia
CMD python run.py
