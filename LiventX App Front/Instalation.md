## Documentación de instalación de LiventX App Front

### Requisitos

* NodeJS v14.20.0
* NPM v6.14.17

### Instalación

1. Clonar el repositorio de GitHub
2. Instalar las dependencias de NodeJS con NPM
3. Correr el servidor de desarrollo

#### Clonar el repositorio de GitHub

Para clonar el repositorio de GitHub, ejecutar el siguiente comando:

    git clone https://{user}@bitbucket.org/inmovdev/liventx-app-front.git

#### Instalar las dependencias de NodeJS con NPM

Para instalar las dependencias de NodeJS con NPM, ejecutar el siguiente comando:

    npm install -f

Si requiere instalar NodeJS, puede hacerlo desde el siguiente enlace: [https://nodejs.org/es/download/](https://nodejs.org/es/download/)

#### Configurar el archivo .env

Copiar el archivo .env y configurar los datos de conexión

#### Correr el servidor de desarrollo

Para iniciar la app, ejecutar el siguiente comando:

    npm start

Luego para correr la app en ios ejecutar el siguiente comando:

    npx react-native run-ios

O para correr la app en android ejecutar el siguiente comando:

    npx react-native run-android

Se debe tener en cuenta para visualizar la app en un dispositivo virtual emulador, se debe tener instalado el SDK de Android o Xcode, o bien, un dispositivo físico con Android o iOS a través de un cable USB.

Para mas información sobre la instalación de React Native, puede consultar el siguiente enlace: [https://reactnative.dev/docs/environment-setup](https://reactnative.dev/docs/environment-setup)

### Generar APK

Para generar el APK, ejecutar el siguiente comando:

    generate-apk

### Publicar actualizaciones en Google Play

Para publicar actualizaciones en Google Play, ejecutar el siguiente comando:

    codepush-android


### Publicar actualizaciones en App Store

Para publicar actualizaciones en App Store, ejecutar el siguiente comando:

    codepush

Para mas información sobre CodePush, puede consultar el siguiente enlace: [https://docs.microsoft.com/en-us/appcenter/distribution/codepush/](https://docs.microsoft.com/en-us/appcenter/distribution/codepush/)