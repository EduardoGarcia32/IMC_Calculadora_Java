# IMC_Calculadora_Java

Evidencia de Computación avanzada en Java

## Instalación
1. Clona el proyecto
2. Importa el proyecto en tu IDE favorito
3. Conviertelo a Maven y actualizalo

Con esto debería ser posible correrlo en un servidor como Tomcat

## Uso
IMC_Calculadora API

**Recurso /api/v1/**  
1. **GET**: Lista los recursos disponibles.
2. **OPTIONS**: Documentación del recurso.

**Recurso /api/v1/file**  
1. **GET**: Descarga un archivo mediante el parámetro path. 
```
api/v1/file/?path=
```
2. **POST**: Sube un archivo mediante los parámetros name, dir y file.
```
api/v1/file/ name="imagen.jpg" dir="/Files" file@/Users/Usuario/Downloads/imagneasubir.jpg --form
```
3. **DELETE**: Elimina un archivo mediante el parámetro path.
```
api/v1/file/?path=
```
4. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/directory**  
1. **GET**: Lista los archivos de un directorio mediante el parámetro dir. 
```
api/v1/directory/?dir=
```
2. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/notify**  
1. **GET**: Lista las notificaciones enviadas.
2. **POST**: Envía una notificación mediante los parámetros subject, message, toAddress y ccAddress.
```
api/v1/notify subject="hola" message="Hola de RestfulWS" toAddress="a@b.com" ccAddress="a@b.com"
```
3. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/user**  
1. **GET**: Lista los usuarios.
2. **POST**: Crea un usuario mediante los parámetros username, password y fullName.
```
api/v1/user username="user" password="pass" fullName="John Doe"
```
3. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/user/{username}**  
1. **GET**: Muestra la información del usuario.
2. **PUT**: Actualiza la información del usuario mediante los parámetros username, password y fullName.
