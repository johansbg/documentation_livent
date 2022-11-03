## Documentación de rutas utilizadas en Page LiventX

En esta sección se detallan las rutas utilizadas en Page LiventX en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

| Endpoint | Privilegio | Método | Descripción | Controlador | Parámetros | Salida |
|----------|------------|--------|-------------|-------------|------------|--------|
| / | Public | GET | Ruta principal de la página, la cual renderiza la vista para iniciar sesión.  | App\Http\Controllers\LoginController@index | - | Retorna la vista o 404 |
| /login | Public | GET | Ruta principal de la página, la cual renderiza la vista para iniciar sesión. | App\Http\Controllers\LoginController@index | - | Retorna la vista o 404 |
| /registro | Public | GET | Retorna la vista de registro a la página. | App\Http\Controllers\LoginController@register | - | Retorna la vista o 404|
| /cities-ajax/{country_id} | Public | GET | Ruta para obtener las ciudades de un país según el ID. | App\Http\Controllers\LoginController@cities | country_id | Retorna listado de ciudades |
| /new-login | Public | POST | Ruta para autenticar al usuario en la plataforma. | App\Http\Controllers\Auth\LoginController@authenticate | email, password  | Retorna la vista de home o error de autenticación |
| /signup | Public | GET | Retorna la vista de registro a la página. | App\Http\Controllers\SignupController@index | - | Retorna la vista o 404 |
| signup | Public | POST | Guarda los datos enviados por el formulario de registro y comprueba si el registro fue exitoso. | App\Http\Controllers\SignupController@store | email, name, lastname, company, address, país, estate, city, gender, password  | Retorna mensaje de registrado con éxito o error. |
| /forgot-password | Public | GET | Renderiza la vista para recuperar la contraseña | App\Http\Controllers\LoginController@forgot | - | Retorna la vista o 404 |
| /forgot-password-send | Public | POST | Ruta para enviar código de verificación al email indicado | App\Http\Controllers\LoginController@forgot_send | email | Retorna vista para comprobar código |
| /reset-password-forgot | Public | GET | Retorna vista para comprobar código | App\Http\Controllers\LoginController@reset_password_forgot | - | Retorna la vista o 404  |
| /reset-password-forgot-send | Public | POST | Realiza la comprobación para validar si el código es válido | App\Http\Controllers\LoginController@reset_password_forgot_send | email, code | Retorna la vista con el formulario para cambiar la contraseña |
| /set-password/{code} | Public | GET | Decodifica el código y comprueba si es válido en la plataforma | App\Http\Controllers\LoginController@set_password_last | - | Retorna el formulario de reinicio de contraseña o redirige al login |
| /reset-password/{code} | Public | GET | Retorna la vista con el formulario para cambiar la contraseña | App\Http\Controllers\LoginController@reset_password_last | code | Retorna la vista o 404 |
| /reset-password-send | Public | POST | Comprueba que el código sea válido y realiza el cambio a la nueva contraseña digitada | App\Http\Controllers\LoginController@reset_password_update | password, code  | Retorna al login |
| /interaction/{stand}/{code} | Auth | GET | Ruta para interactuar con un stand de un cliente | App\Http\Controllers\InteractionController@index | code, stand | Retorna la vista o 404 |
| /data_share/{id} | Public | Auth | Guarda los datos de interaccion del usuario | App\Http\Controllers\InteractionController@data_share | id (user_id-interaction_id) | Retorna mensaje de éxito |
| /living_room | Auth | GET | Renderiza la vista del listado de las salas de estar disponibles  | App\Http\Controllers\InteractionController@living_room | - | Retorna la vista o 404 |
| /go/chat/{stand_id} | Auth | GET | Muestra la vista del chat del stand | App\Http\Controllers\ChatController@chat | stand | Retorna la vista o 404 |
| /profile/{id} | Auth | GET | Ruta para ver el perfil de un usuario | App\Http\Controllers\ProfileController@show | - | Retorna la vista o 404 |
| /profile/{id} | Auth | PATCH | Ruta para actualizar el perfil de un usuario con los datos solicitados | App\Http\Controllers\ProfileController@update | email, name, lastname, company, address, país, estate, city, gender, | Retorna mensaje de éxito o error |
| /home | Auth | GET | Ruta para ir al home de la plataforma | App\Http\Controllers\HomeController@index | - | Retorna la vista o 404 |
| /agenda | Auth | GET | Renderiza los listados de la agenda de eventos a la que pertenece el usuario | App\Http\Controllers\ScheduleController@index | - | Retorna la vista o 404 |
| /reproductor | Auth | GET | Ruta para listar las noticias de los eventos creados en la plataforma | App\Http\Controllers\event_stageController@index | - | Retorna la vista o 404 |
| /memorias | Auth | GET | Ruta que renderiza las memorias de un evento | App\Http\Controllers\event_memoriesController@index | - | Retorna la vista o 404 |
| /recorrido-virtual | Auth | GET | Ruta para ir al recorrido en realidad virtual | App\Http\Controllers\vrController@index | - | Retorna la vista o 404 |
| /patrocinador | Auth | VIEW | Ruta para ir a los patrocinadores | App\Http\Controllers\patrocinador | - | Retorna la vista o 404 |
| /sala/{id}/video/{video_id} | Auth | GET | Ruta para ver el video de una sala | App\Http\Controllers\event_stageController@videos | id, video | Retorna video o 404 |
| /sala/{id} | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\standController@index | id | Retorna vista o 404  |
| /stand/{id} | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\standController@index | id | Retorna vista o 404 |
| /stands | Auth | GET | Renderiza el listado de salas o stands que hay | App\Http\Controllers\standController@index_page | - | Retorna vista o 404 |
| /NetworkingPartner | Auth | GET | Ruta para ir el perfil de Networking del usuario | App\Http\Controllers\NetworkingRes_partnerController@index | - | Retorna vista o 404 |
| /NetworkingPartner-criterio-delete | Auth | POST | Ruta para eliminar un criterio de búsqueda en Networking | App\Http\Controllers\NetworkingRes_partnerController@CriterioDelete | - | Retorna vista o 404 |
| GuestProfile-category-create | Auth | POST | Ruta que crea un perfil de una categoria | App\Http\Controllers\NetworkingAjaxController@ProfileCategoryCreate | event_id, nameCategory | json |
| GuestProfile-attribute-create | Auth | POST | Ruta que crea un perfil de un atributo | App\Http\Controllers\NetworkingAjaxController@ProfileAttributeCreate | event_id, nw_category_id, nameAttribute | json |
| api | Auth | GET | Ruta que cuenta la cantidad de usuarios que hay en la plataforma | App\Http\Controllers\apiController@api | - | Numero |