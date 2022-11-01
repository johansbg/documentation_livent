## Documentación de rutas utilizadas en LiventX App Front

En esta sección se detallan las rutas utilizadas en Page LiventX en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

### Rutas de la APP PUBLICAS (sin autenticación)

| Pantalla | Privilegio | Descripción | Componente |
|----------|------------|--------|-------------|
| AuthLoadingScreen | Public | Ruta principal para comprobar si esta logueado el usuario | AuthLoadingScreen |
| IntroScreen | Public | Ruta principal para mostrar la introducción de la aplicación | IntroScreen |
| Login | Public | Ruta principal para mostrar el login de la aplicación | LoginScreen |
| ForgotPassword | Public | Ruta principal para mostrar el formulario de recuperación de contraseña | ForgotPasswordScreen |
| SignupEventListScreen | Public | Ruta principal para mostrar la lista de eventos para registrarse | SignupEventListScreen |
| ForgotPasswordSetNewScreen | Public | Ruta principal para mostrar el formulario de cambio de contraseña | ForgotPasswordSetNewScreen |
| ForgotPasswordTokenScreen | Public | Ruta principal para generar una contraseña temporal | ForgotPasswordTokenScreen |
| SignupScreen | Public | Ruta principal para mostrar el formulario de registro | SignupScreen |
| PdfPreview | Public | Ruta principal para mostrar el pdf de la factura | PdfPreview |

### Rutas de la APP PRIVADAS ( autenticación)
| Pantalla | Privilegio | Descripción | Componente |
|----------|------------|--------|-------------|
| WelcomeScreen | Auth | Ruta principal para mostrar el inicio de la aplicación | WelcomeScreen |
| MyEventsScreen | Auth | Ruta principal para mostrar la lista de eventos del usuario | MyEventsScreen |
| VrScreen | Auth | Ruta principal para mostrar el contenido de realidad virtual | VrScreen |
| ContentCenterScreen | Auth | Ruta principal para mostrar el contenido del centro de contenidos | ContentCenterScreen |
| ContentCenterDetail | Auth | Ruta principal para mostrar el detalle del contenido del centro de contenidos | ContentCenterDetailScreen |
| SearchContentCenter | Auth | Ruta principal para mostrar el buscador del centro de contenidos | SearchContentCenterScreen |
| CompleteProfileScreen | Auth | Ruta principal para mostrar el formulario de perfil del usuario | CompleteProfileScreen |
| AgendaSimpleScreen | Auth | Ruta principal para mostrar la agenda del evento | AgendaSimpleScreen |
|  AgendaDetailScreen | Auth | Ruta principal para mostrar el detalle de la agenda del evento | AgendaDetailScreen |
| CommunityScreen | Auth | Ruta principal para mostrar la comunidad del evento | CommunityScreen |
| NewCommunityPublishScreen | Auth | Ruta principal para mostrar el formulario de publicación de la comunidad | NewCommunityPublishScreen |
| QuestionListScreen | Auth | Ruta principal para mostrar la lista de preguntas del evento | QuestionListScreen |
| CommunityCommentsScreen | Auth | Ruta principal para mostrar los comentarios de la comunidad | CommunityCommentsScreen |
| HelpDeskFormScreen | Auth | Ruta principal para mostrar el formulario de ayuda | HelpDeskFormScreen |
| QuestionsCategoriesScreen | Auth | Ruta principal para mostrar las categorías de preguntas | QuestionsCategoriesScreen |
| TriviaScreen | Auth | Ruta principal para mostrar la trivia del evento | TriviaScreen |
| NotificationsScreen | Auth | Ruta principal para mostrar las notificaciones del usuario | NotificationsScreen |