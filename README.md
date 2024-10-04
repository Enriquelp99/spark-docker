# Docker PySpark

Este repositorio contiene un conjunto de archivos de configuración para crear un entorno de desarrollo con Apache Spark y PySpark utilizando Docker y Docker Compose. Esto permite la ejecución y el procesamiento de datos en Python de manera sencilla y eficiente.

## Características

- **Configuración sencilla**: Levanta un entorno de desarrollo de PySpark con solo un comando.
- **Compatibilidad**: Utiliza imágenes oficiales de Docker para garantizar compatibilidad y rendimiento óptimos.
- **Escalabilidad**: Docker Compose facilita la gestión de múltiples servicios y la configuración de redes entre contenedores.
- **Personalización**: Configura los contenedores según tus necesidades específicas, añadiendo librerías y configuraciones adicionales.

## Requisitos

- [Docker](https://www.docker.com/) instalado en tu máquina.
- [Docker Compose](https://docs.docker.com/compose/) instalado en tu máquina.
- Conexión a internet para descargar las imágenes necesarias.

## Estructura del proyecto

- **Dockerfile**: Define la imagen de Docker con Apache Spark, PySpark, Java y Scala.
- **docker-compose.yml**: Archivo de configuración de Docker Compose que define los servicios `spark-master` y `spark-worker`, así como las redes y volúmenes necesarios.
- **src/**: Contiene el código fuente del proyecto, incluyendo el archivo `requirements.txt` para las dependencias de Python.
- **worker.py**: Archivo Python que se utilizará en el contenedor.

## Instrucciones de uso

1. Clona este repositorio:  
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   ```

2. Navega al directorio del proyecto:  
   ```bash
   cd <NOMBRE_DEL_DIRECTORIO>
   ```

3. Levanta los servicios utilizando Docker Compose:  
   ```bash
   docker-compose up
   ```

4. Accede al contenedor interactivo del master:  
   ```bash
   docker exec -it <NOMBRE_DEL_CONTENEDOR_MASTER> /bin/bash
   ```

5. Accede al contenedor interactivo del worker:  
   ```bash
   docker exec -it <NOMBRE_DEL_CONTENEDOR_WORKER> /bin/bash
   ```

## Ejemplo de uso

Una vez dentro del contenedor del master, puedes iniciar una sesión de PySpark ejecutando el siguiente comando:

```bash
pyspark
```

Esto abrirá la interfaz interactiva de PySpark, donde podrás ejecutar tus scripts y realizar análisis de datos.

## Acceso a las interfaces web

- **Spark Master UI**: [http://localhost:8080](http://localhost:8080)  
- **Spark Worker UI**: [http://localhost:8081](http://localhost:8081)  

Estas interfaces te permitirán monitorear el estado de los servicios.

## Contribuciones

Las contribuciones son bienvenidas. Siéntete libre de abrir un issue o hacer un pull request. Agradecemos tu interés en mejorar este proyecto.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Contacto

Si tienes preguntas o sugerencias, no dudes en contactarme en [enrique.liepe.1999@gmail.com](mailto:enrique.liepe.1999@gmail.com).
