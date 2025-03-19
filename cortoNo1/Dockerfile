# Usar una imagen base de JDK 17
FROM eclipse-temurin:17-jdk-alpine

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar los archivos del proyecto
COPY . /app

# Dar permisos al wrapper de Maven
RUN chmod +x mvnw

# Construir la aplicación dentro del contenedor evitando la compilación local
RUN ./mvnw package -DskipTests

# Exponer el puerto de la aplicación
EXPOSE 8080

# Ejecutar la aplicación
CMD ["java", "-jar", "target/*.jar"]
