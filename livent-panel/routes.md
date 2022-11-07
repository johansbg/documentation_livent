## Documentación de rutas utilizadas en Livent Panel

En esta sección se detallan los grupos de vistas utilizados en Livent Panel.
## Grupos de vistas
| Grupo | Privilegio | Método | Descripción |
| --- | --- | --- | --- |
| dashboard | Auth | VIEW | Vista del dashboard del panel |
| starter-kit | Auth | VIEW | Grupo de layouts del panel |
| others | Auth | VIEW | Grupo de vistas de errores del panel |
| /clear-cache | Guest | CALL | Grupo de llamados para limpiar la cache |

En esta sección se detallan las rutas utilizadas en Livent Panel en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

| Endpoint | Privilegio | Método | Descripción | Controlador | Parámetros | Salida |
|----------|------------|--------|-------------|-------------|------------|--------|
| /home | Auth | GET | Ruta principal de Livent Panel la cual redirige al dashboard | App\Http\Controllers\HomeController@index | - | Retorna vista o 404 |
| /Event | Auth | GET | Ruta para mostrar los eventos | App\Http\Controllers\EventController@index | order, id, order_type | Retorna vista o 404 |
| /Event/create | Auth | GET | Ruta para mostrar formulario de creación de un evento | App\Http\Controllers\EventController@create | - | Retorna vista o 404 |
| /Event-store | Auth | POST | Ruta para almacenar un evento | App\Http\Controllers\EventController@store | Parametros enviados en el formulario de la vista | Retorna Vista con alerta de éxito o fallo |
| /Event-edit/{id} | Auth | GET | Ruta la vista del formulario para actualizar un evento | App\Http\Controllers\EventController@edit | - | Retorna vista o 404 |
| /Event-update/{id} | Auth | PUT | Ruta para editar un evento | App\Http\Controllers\EventController@update | Parametros del formulario de update | Retorna Vista con alerta de éxito o fallo |
| /Event-assistants/{id} | Auth | GET | Ruta para mostrar los asistentes de un evento | App\Http\Controllers\EventController@assistants | - | Retorna vista o 404 |
| /Event-assistants-import | Auth | POST | Ruta para importar asistentes de un evento | App\Http\Controllers\EventController@fileImportExport | - | - |
| /Event-assistants-file | Auth | POST | Ruta para importar asistentes de un evento | App\Http\Controllers\EventController@fileImport | file | Retorna Vista con alerta de éxito o fallo  |  
| /carlosbeltran | Auth | GET | Ruta para importar partners del evento | App\Http\Controllers\EventController@manual_up | import | - |
| /Event-assistants-create/{id} | Auth | POST | Ruta para crear un asistente | App\Http\Controllers\EventController@assistants_create | Parámetros del formulario de creación | Retorna Vista con alerta de éxito o fallo |
| /Event-assistants-delete/{id} | Auth | DELETE | Ruta para eliminar un asistente | App\Http\Controllers\EventController@assistantsDelete | id | Retorna Vista con alerta de éxito o fallo |
| //Event-activite/{id} | Auth | GET | Ruta para activar un evento | App\Http\Controllers\EventController@activite | id | Retorna Vista con alerta de éxito o fallo |
| /downloads/attendess/template | Auth | GET | Ruta para descargar el template de asistentes | App\Http\Controllers\EventController@downloadAttendessTemplate | - | Descarga un excel de los asistentes del evento |
| /Partner | Auth | GET | Ruta para mostrar los patrocinadores | App\Http\Controllers\PartnerController@index | - | Retorna vista o 404 |
| /Partner-create | Auth | GET | Ruta que muestra el formulario de creación | App\Http\Controllers\PartnerController@create | - | Retorna ruta o 404 |
| /Partner-store | Auth | POST | Ruta para almacenar un patrocinador | App\Http\Controllers\PartnerController@store | Parámetros del formulario de creación | Retorna Vista con alerta de éxito o fallo |
| /Partner-edit/{id} | Auth | GET | Ruta que muestra el formulario de edición | App\Http\Controllers\PartnerController@edit | - | Retorna vista o 404 |
| /Partner-update/{id} | Auth | PUT | Ruta para actualizar un patrocinador | App\Http\Controllers\PartnerController@update | Parámetros del formulario de edición | Retorna vista o 404 |
| /Event/Registration/Report | Auth | GET | Ruta para mostrar el reporte de registro de asistentes | App\Http\Controllers\ReportController@event_report_index | - | Retorna vista o 404 |
| /Event/Registration/Report/Generate | Auth | POST | Ruta para generar el reporte de registro de asistentes | App\Http\Controllers\ReportController@event_report_registration_generate | Parametros de filtrado, fecha de inicio , fecha final, id evento | Descarga un excel del reporte  |
| /Event/Tritiva/Report | Auth | GET | Ruta para mostrar el reporte de tritiva | App\Http\Controllers\ReportController@event_trivia_index | event_id | Retorna vista o 404 |
| /Event/Tritiva/Report/Generate | Auth | POST | Ruta para generar el reporte de tritiva | App\Http\Controllers\ReportController@event_report_trivia_generate | event_id, report_type |  Descarga un excel del reporte |
| /Event/Tritiva/get/list/{event_id} | Auth | GET | Ruta para obtener las trivias de un evento | App\Http\Controllers\ReportController@get_trivias_index | event_id | - |
| /Clients | Auth | GET | Ruta para mostrar los clientes | App\Http\Controllers\ClientController@index | - | Retorna vista o 404 |
| /Clients-create | Auth | GET | Ruta para mostar el formulario de creación | App\Http\Controllers\ClientController@create | - | Retorna vista o 404 |
| /Clients-store | Auth | POST | Ruta para almacenar un cliente | App\Http\Controllers\ClientController@store | Parametros del formulario de creación | Retorna Vista con alerta de éxito o fallo |
| /Clients-edit/{id} | Auth | GET | Ruta para mostrar el formulario de edición | App\Http\Controllers\ClientController@edit | - | Retorna vista o 404 |
| /Clients-update/{id} | Auth | PUT | Ruta para actualizar un cliente | App\Http\Controllers\ClientController@update | Parametros del formulario de edición | Retorna Vista con alerta de éxito o fallo |
| /Clients-delete/{id} | Auth | DELETE | Ruta para eliminar un cliente | App\Http\Controllers\ClientController@destroy | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite | Auth | GET | Ruta para mostrar los los eventos disponibles | App\Http\Controllers\WebSiteController@index | Filtros | Retorna vista o 404 |
| /WebSite-setup/{event_id}/{tab_id?}/{item_modal_id?} | Auth | GET-POST | Ruta para mostrar la configuración de un evento | App\Http\Controllers\WebSiteController@website_setup | parametros de url | Retorna vista o 404 |
| /WebSite-setup-menu-page/{event_id} | Auth | POST | Ruta para crear un nuevo menu de un evento| App\Http\Controllers\WebSiteController@website_menu_page | event_id, tab_id  | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-menu-page/{event_id}/{option_id} | Auth | DELETE | Ruta para eliminar un menu de un evento | App\Http\Controllers\WebSiteController@website_menu_page_delete_option | tab_id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setups-schedule-day | Auth | POST | Ruta para configurar el calendario del evento | App\Http\Controllers\WebSiteController@website_schedule_day | event_id, tab_id, day, date, description | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setups-schedule-item | Auth | POST | Ruta para crear un item de un calendario | App\Http\Controllers\WebSiteController@website_schedule_item | Parametros de un item | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-news | Auth | POST | Ruta para guardar una nueva noticia de un evento | App\Http\Controllers\WebSiteController@store_new | parametros y archivos de la noticia | Retorna Vista con alerta de éxito o fallo |
| /launch/questions | Auth | GET | Ruta para retornar una pregunta | App\Http\Controllers\WebSiteController@launch_question | question_id, launched | - |
| remove/shedule | Auth | POST | Ruta para eliminar un horario | App\Http\Controllers\WebSiteController@remove_shedule | id | json |
| remove/shedule/item | Auth | POST | Ruta para eliminar un item de un horario | App\Http\Controllers\WebSiteController@remove_schedule_item | id | json |
| /WebSite-setup-questions | Auth | POST | Ruta guardar una pregunta | App\Http\Controllers\WebSiteController@store_question | Parametros de la pregunta | Retorna Vista con alerta de éxito o fallo  |
| /WebSite-setup-question-option | Auth | POST | Ruta para guardar una opcion de una pregunta | App\Http\Controllers\WebSiteController@store_question_option | parametros de la option | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-question-option/{event_id}/{tab_id}/{option_id} | Auth | DELETE | Ruta para eliminar una option de una pregunta  | App\Http\Controllers\WebSiteController@delete_question_option | paramteros url | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-page | Auth | POST | Ruta para guardar la pagina de un evento | App\Http\Controllers\WebSiteController@store_page | Parametros de la pagina |  |
| /WebSite-setup-register-config-page/{event_id}/{config_id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_register_config_page_delete_option | config_id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-register-config/{event_id} | Auth | POST | Ruta para guardar un menu website de un evento | App\Http\Controllers\WebSiteController@website_register_config_page | parametros del menu | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-page/{event_id}/{option_id} | Auth | DELETE | Ruta para eliminar un slider de la galeria del evento | App\Http\Controllers\WebSiteController@delete_page_slider_option | id, event_id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-page/{event_id}/{option_id} | Auth | PATCH | Ruta para actualizar un slider de la galeria de eventos  | App\Http\Controllers\WebSiteController@change_page_slider_option |  tab_id, event_id, id, file | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-app | Auth | POST | Ruta para guardar la app de un evento | App\Http\Controllers\WebSiteController@store_app | Parametros del formulario de la app | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-menu-app/{event_id} | Auth | POST | Ruta para guardar el menu de una app | App\Http\Controllers\WebSiteController@website_menu_app | event_id, parametros del formulario del menu | Retorna Vista con alerta de éxito o fallo|
| /WebSite-setup-menu-app/{event_id}/{option_id} | Auth | DELETE | Ruta para eliminar la opcion de un menu de la app | App\Http\Controllers\WebSiteController@website_menu_app_delete_option | event_menu_app_id, event_id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-bussines-selectors-config/{event_id} | Auth | POST | Ruta crear la configuración de negocio de un evento| App\Http\Controllers\WebSiteController@website_bussines_selectors_config_page | Parametros de la configuración de negocio | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-page/meeting-live | Auth | POST | Ruta para guardar el live meeting de un evento | App\Http\Controllers\WebSiteController@store_meeting_live | Parametros del live | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-page/zoom-room | Auth | POST | Ruta para guardar la sala de zoom del evento | App\Http\Controllers\WebSiteController@store_zoom_room | Parametros de la sala de zoom | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-company-registration/company-registration | Auth | POST | Ruta para registrar a una company a un evento | App\Http\Controllers\WebSiteController@company_registration_store | Parametros de una company | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-company-registration-option/company-registration-option | Auth | POST | Ruta para guardar las configuraciones de una company | App\Http\Controllers\WebSiteController@company_registration_option_store | Parametros de configuracion | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-company-registration/company-registration/{id} | Auth | DELETE | Ruta eliminar una company | App\Http\Controllers\WebSiteController@company_registration_destroy | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-company-registration-option/company-registration-option/{id} | Auth | DELETE | Ruta para eliminar una opcion de una company | App\Http\Controllers\WebSiteController@company_registration_option_destroy | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-meetings | Auth | POST | Ruta para guardar las configuraciones de una meeting | App\Http\Controllers\WebSiteController@store_setup_meetings | Parametros de la meeting | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-categories-nw | Auth | POST | Ruta para crear nuevas categorias de un evento | App\Http\Controllers\WebSiteController@store_setup_categories_nw | name, event_id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-categories-nw/{id} | Auth | DELETE | Ruta para eliminar una categoria | App\Http\Controllers\WebSiteController@delete_setup_categories_nw | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-subcategories-nw | Auth | POST | Ruta para crear una subcategoria | App\Http\Controllers\WebSiteController@store_setup_subcategories_nw | event_id, category_id, name | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-subcategories-nw/{id} | Auth | DELETE | Ruta para eliminar una subcategoria | App\Http\Controllers\WebSiteController@delete_setup_subcategories_nw | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-type-company-nw | Auth | POST | Ruta para guardar un tipo de company | App\Http\Controllers\WebSiteController@store_setup_type_company_nw | event_id, name | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-type-company-nw/{id} | Auth | DELETE | Ruta para eliminar un tipo de company | App\Http\Controllers\WebSiteController@delete_setup_type_company_nw | id | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-feedback-nw | Auth | POST | Ruta para crear un feedback de un evento | App\Http\Controllers\WebSiteController@store_setup_feedback_nw | parametros del feedback | Retorna Vista con alerta de éxito o fallo |
| /WebSite-setup-feedback-nw/{id} | Auth | DELETE | Ruta para eliminar un feedback de una evento | App\Http\Controllers\WebSiteController@feedback_question_delete | id | Retorna Vista con alerta de éxito o fallo |
| save/order | Auth | POST | Ruta para guardar el orden de los items | App\Http\Controllers\WebSiteController@save_order | table, items | Retorna json |
| /VirtualSpace2D | Auth | GET | Ruta para listar los espacio virtuales de los eventos  | App\Http\Controllers\InteractionController@index2 | - | Retorna vista o 404 |
| /VirtualSpace2D-setup/{event_id} | Auth | GET | Ruta para configurar un espacio virtual 2D de un evento | App\Http\Controllers\InteractionController@setup | event_id | Retorna vista o 404 |
| /InteractionList/{stand} | Auth | GET | Ruta para mostrar las interacciones en un stand de un espacio virtual 2D | App\Http\Controllers\InteractionController@index | stand | Retorna vista o 404 |
| /Interaction/edit/{id}/{stand} | Auth | GET | Ruta mostrar el formulario de editar de un stand | App\Http\Controllers\InteractionController@edit | id, stand | Retorna vista o 404 |
| /Interaction/edit/{id}/{stand} | Auth | PUT | Ruta para guardar la edicion del stand | App\Http\Controllers\InteractionController@update | Parametros del formulario | Retorna Vista con alerta de éxito o fallo |
| /VirtualSpace | Auth | GET | Ruta para listar los espacios virtuales | App\Http\Controllers\VirtualSpaceController@index | - | Retorna vista o 404 |
| /VirtualSpace-setup/{event_id} | Auth | GET | Ruta para mostrar la configuracion de un stand | App\Http\Controllers\VirtualSpaceController@setup | event_id | Retorna vista o 404 |
| /VirtualSpace-create_catalog/{event_id} | Auth | GET | Ruta para crear el catalogo de un evento | App\Http\Controllers\VirtualSpaceController@create_catalog | event_id | Retorna vista o 404 |
| /VirtualSpace-create | Auth | POST | Ruta para guardar la configuracion de un catalogo de un evento | App\Http\Controllers\VirtualSpaceController@store_catalog | Parametros del formulario | Retorna Vista con alerta de éxito o fallo |
| /VirtualSpace-edit_catalog/{catalog_id}/{event_id} | Auth | GET | Ruta para mostrar el formulario de edicion del catalogo del evento | App\Http\Controllers\VirtualSpaceController@edit_catalog | catalog_id, event_id | Retorna Vista o 404 |
| /VirtualSpace-update_catalog/{catalog_id}/{event_id} | Auth | PUT | Ruta para editar la configuracion de un catalogo de un evento | App\Http\Controllers\VirtualSpaceController@update_catalog | Parametros del formulario | Ruta para editar la configuracion de un catalogo de un evento |
| /VirtualSpace-create_brand/{catalog_id}/{event_id} | Auth | GET | Ruta para mostrar el formulario de creacion de marca de un espacio virtual | App\Http\Controllers\VirtualSpaceController@create_brand | catalog_id, event_id | Retorna vista o 404 |
| /VirtualSpace-store-brand | Auth | POST | Ruta para guardar una marca de un espacio virtual | App\Http\Controllers\VirtualSpaceController@store_brand | Parametros del formulario | Retorna Vista con alerta de éxito o fallo |
| /VirtualSpace-catalog_brand/{space_id}/{type_id} | Auth | GET | Ruta obtener el catalogo de marcas de un evento | App\Http\Controllers\VirtualSpaceController@catalog_brand | space_id, type_id  | Retorna valores event_catalog_brands |
| /VirtualSpace-edit_brand/{catalog_id}/{event_id}/{id} | Auth | GET | uta para mostrar el formulario de edicion de una marca | App\Http\Controllers\VirtualSpaceController@edit_brand | catalog_id, event_id, id | Retorna vista o 404 |
| /VirtualSpace-update_brand/{id} | Auth | PUT | Ruta para editar un marca | App\Http\Controllers\VirtualSpaceController@update_brand | Parametros del formulario | Retorna Vista con alerta de éxito o fallo |
| /Notification | Auth | GET | Ruta el listado de eventos para ver sus notificaciones | App\Http\Controllers\NotificationController@index | - | Retorna vista o 404 |
| /Notification-send/{event_id} | Auth | GET | Ruta para listar las notificaciones de un evento | App\Http\Controllers\NotificationController@notifications_send | event_id | Retorna vista o 404 |
| /Notification-send/{event_id} | Auth | POST | Ruta para enviar notificaciones a un evento | App\Http\Controllers\NotificationController@send_notification | Parametros del formularios | Retorna Vista con alerta de éxito o fallo |
| /Notification-email-send/{event_id} | Auth | GET | Ruta para mostrar la notificaciones enviadas por email | App\Http\Controllers\NotificationController@notifications_email | event_id | Retorna vista o 404 |
| /Notification-email-send/{event_id} | Auth | POST | Ruta para enviar notificaiones por email a un evento | App\Http\Controllers\NotificationController@notifications_email_send | Parametros del formulario | Retorna Vista con alerta de éxito o fallo |
| /news | Auth | GET | Ruta para obtener las noticias de un evento | App\Http\Controllers\NewsController@index | event_id | json |
| /Execute | Auth | GET | No tiene funcionalidad | App\Http\Controllers\executeController@index | - | - |
| /Setting | Auth | GET | No tiene funcionalidad | App\Http\Controllers\SettingController@index | - | - |
| /Networking/NetworkingPlan | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingPlanController@index |  |  |
| /Networking/NetworkingPlan | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingPlanController@index |  |  |
| /Networking/Customer | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@index |  |  |
| /Networking/Customer-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@create |  |  |
| /Networking/Customer-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@store |  |  |
| /Networking/Customer-edit/{NwCustomer} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@Edit |  |  |
| /Networking/Customer-update/{NwCustomer} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@update |  |  |
| /Networking/Customer-delete | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@destroy |  |  |
| /Networking/Customer-status | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingCustomerController@status |  |  |
| /Networking/Hall | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@index |  |  |
| /Networking/Hall-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@create |  |  |
| /Networking/Hall-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@store |  |  |
| /Networking/Hall-edit/{NwHall} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@Edit |  |  |
| /Networking/Hall-update/{NwHall} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@update |  |  |
| /Networking/Hall-delete | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@destroy |  |  |
| /Networking/Hall-status | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingHallController@status |  |  |
| /Networking/Stand | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@index |  |  |
| /Networking/Stand-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@create |  |  |
| /Networking/Stand-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@store |  |  |
| /Networking/Stand-edit/{NwStand} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@Edit |  |  |
| /Networking/Stand-update/{NwStand} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@update |  |  |
| /Networking/Stand-delete | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@destroy |  |  |
| /Networking/Stand-status | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingStandController@status |  |  |
| /Networking/Meeting | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@index |  |  |
| /Networking/Meeting-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@create |  |  |
| /Networking/Meeting-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@store |  |  |
| /Networking/Meeting-edit/{NwMeeting} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@Edit |  |  |
| /Networking/Meeting-delete | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@destroy |  |  |
| /Networking/Meeting-status | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@status |  |  |
| /Networking/Meeting-Attend | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingAttendController@attend |  |  |
| /Networking/Meeting-Finish | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingAttendController@finish |  |  |
| /Networking/Meeting-update/{NwMeeting} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@update |  |  |
| /Networking/Meeting-update-show/{NwMeeting} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@show |  |  |
| /Networking/Meeting-video-show | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingMeetingController@video |  |  |
| /Networking/Videoconference | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingVideoconferenceController@videoconference |  |  |
| /Networking/Executive | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingExecutiveController@index |  |  |
| /Networking/Executive-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingExecutiveController@create |  |  |
| /Networking/Executive-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingExecutiveController@store |  |  |
| /Networking/Executive-show-user | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingExecutiveController@showuser |  |  |
| /Networking/Executive-delete | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingExecutiveController@destroy |  |  |
| /Networking/Users | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@index |  |  |
| /Networking/Users-create | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@create |  |  |
| /Networking/Users-store | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@store |  |  |
| /Networking/Users-edit/{NwUser} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@Edit |  |  |
| /Networking/Users-update/{NwUser} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@update |  |  |
| /Networking/Users-status | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingUsersController@status |  |  |
| /Networking/Guest | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@index |  |  |
| /Networking/GuestVisitStand/{stand_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@VisitStand |  |  |
| /Networking/GuestMyMeeting/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@MyMeeting |  |  |
| /Networking/GuestProfile/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@Profile |  |  |
| /Networking/GuestAttend | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@Attend |  |  |
| /Networking/GuestTarget/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@Target |  |  |
| /Networking/GuestExplore/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingGuestController@Explore |  |  |
| showexecutivecustomer | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@showexecutivecustomer |  |  |
| GuestReadMeeting | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@GuestReadMeeting |  |  |
| ActivateRoom | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ActivateRoom |  |  |
| GuestProfile-delete | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileDelete |  |  |
| GuestProfile-insert | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileInsert |  |  |
| GuestProfile-show-attribute | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileShowAttribute |  |  |
| GuestProfile-show-attribute-profile | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileShowAttributeProfile |  |  |
| GuestProfile-category-create | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileCategoryCreate |  |  |
| GuestProfile-attribute-create | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@ProfileAttributeCreate |  |  |
| GuestTarget-create | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@TargetCreate |  |  |
| GuestTarget-show-attribute-free | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@TargetShowAttributeFree |  |  |
| GuestTarget-show-attribute | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@TargetShowAttribute |  |  |
| GuestTarget-insert | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@TargetInsert |  |  |
| GuestTarget-delete | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NetworkingAjaxController@TargetDelete |  |  |
| Reports/networking | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking |  |  |
| Reports/networking/meetings | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_meetings |  |  |
| Reports/networking/meetings/generate | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_meetings_generate |  |  |
| Reports/networking/feedback | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_feedback |  |  |
| Reports/networking/feedback/generate | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_feedback_generate |  |  |
| Reports/networking/company | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_company |  |  |
| Reports/networking/company/generate | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@networking_company_generate |  |  |
| question/feedback/get | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\ReportController@get_questions |  |  |
