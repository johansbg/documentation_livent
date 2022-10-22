## Documentación de rutas utilizadas en Page LiventX

En esta sección se detallan las rutas utilizadas en Page LiventX en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

| Endpoint | Privilegio | Método | Descripción | Controlador | Parámetros | Salida |
|----------|------------|--------|-------------|-------------|------------|--------|
| / | Public | GET | Ruta principal | App\Http\Controllers\LoginController@index | - | - |
| /login | Public | GET | Ruta de login | App\Http\Controllers\LoginController@index | - | - |
| /registro | Public | GET | Ruta de registro | App\Http\Controllers\LoginController@register | - | - |
| /cities-ajax/{country_id} | Public | GET | Ruta para obtener las ciudades de un país | App\Http\Controllers\LoginController@cities | - | - |
| /new-login | Public | POST | Ruta para iniciar sesión | App\Http\Controllers\LoginController@authenticate | - | - |
| /signup | Public | GET | Ruta para registrar un usuario | App\Http\Controllers\SignupController@index | - | - |
| signup | Public | POST | Ruta para registrar un usuario | App\Http\Controllers\SignupController@store | - | - |
| /forgot-password | Public | GET | Ruta para recuperar contraseña | App\Http\Controllers\LoginController@forgot | - | - |
| /forgot-password | Public | POST | Ruta para recuperar contraseña | App\Http\Controllers\LoginController@forgot_send | - | - |
| /reset-password-forgot | Public | GET | Ruta para cambiar contraseña | App\Http\Controllers\LoginController@reset_password_forgot | - | - |
| /reset-password-forgot-send | Public | POST | Ruta para cambiar contraseña | App\Http\Controllers\LoginController@reset_password_forgot_send | - | - |
| /set-password/{code} | Public | GET | Ruta para cambiar contraseña | App\Http\Controllers\LoginController@set_password_last | - | - |
| /reset-password/{code} | Public | GET | Ruta para cambiar contraseña | App\Http\Controllers\LoginController@reset_password_last | - | - |
| /reset-password-send | Public | POST | Ruta para cambiar contraseña | App\Http\Controllers\LoginController@reset_password_update | - | - |
| /interaction/{stand}/{code} | Auth | GET | Ruta para interactuar con un stand | App\Http\Controllers\InteractionController@index | - | - |
| /data_share/{id} | Public | Auth | Ruta para compartir datos | App\Http\Controllers\InteractionController@data_share | - | - |
| /living_room | Auth | GET | Ruta para la sala de espera | App\Http\Controllers\InteractionController@living_room | - | - |
| /go/chat/{stand_id} | Auth | GET | Ruta para ir al chat | App\Http\Controllers\ChatController@chat | - | - |
| /profile/{id} | Auth | GET | Ruta para ver el perfil de un usuario | App\Http\Controllers\ProfileController@show | - | - |
| /profile/{id} | Auth | PATCH | Ruta para actualizar el perfil de un usuario | App\Http\Controllers\ProfileController@update | - | - |
| /home | Auth | GET | Ruta para ir al home | App\Http\Controllers\HomeController@index | - | - |
| /agenda | Auth | GET | Ruta para ir a la agenda | App\Http\Controllers\ScheduleController@index | - | - |
| /reproductor | Auth | GET | Ruta para ir al reproductor | App\Http\Controllers\event_stageController@index | - | - |
| /memorias | Auth | GET | Ruta para ir a las memorias | App\Http\Controllers\event_memoriesController@index | - | - |
| /recorrido-virtual | Auth | GET | Ruta para ir al recorrido virtual | App\Http\Controllers\vrController@index | - | - |
| /patrocinador | Auth | VIEW | Ruta para ir a los patrocinadores | App\Http\Controllers\patrocinador | - | - |
| /sala/{id}/video/{video_id} | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\event_stageController@videos | - | - |
| /sala/{id} | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\standController@index | - | - |
| /stand/{id} | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\standController@index | - | - |
| /stands | Auth | GET | Ruta para ir a la sala de un evento | App\Http\Controllers\standController@index_page | - | - |
| /NetworkingPartner | Auth | GET | Ruta para ir a los NetworkingPartner | App\Http\Controllers\NetworkingRes_partnerController@index | - | - |
| /NetworkingPartner-criterio-delete | Auth | POST | Ruta para ir a los NetworkingPartner | App\Http\Controllers\NetworkingRes_partnerController@CriterioDelete | - | - |
| GuestProfile-category-create | Auth | POST | Ruta para ir a los NetworkingPartner | App\Http\Controllers\NetworkingAjaxController@ProfileCategoryCreate | - | - |
| GuestProfile-attribute-create | Auth | POST | Ruta para ir a los NetworkingPartner | App\Http\Controllers\NetworkingAjaxController@ProfileAttributeCreate | - | - |
| api | Auth | GET | Ruta API | App\Http\Controllers\apiController@api | - | - |