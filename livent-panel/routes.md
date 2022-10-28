## Documentación de rutas utilizadas en Livent Panel

En esta sección se detallan las rutas utilizadas en Livent Panel en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

| Endpoint | Privilegio | Método | Descripción | Controlador | Parámetros | Salida |
|----------|------------|--------|-------------|-------------|------------|--------|
| /home | Auth | GET | Ruta principal de Livent Panel | App\Http\Controllers\HomeController@index |  |  |
| /Event | Auth | GET | Ruta para mostrar los eventos | App\Http\Controllers\EventController@index |  |  |
| /Event/create | Auth | GET | Ruta para crear un evento | App\Http\Controllers\EventController@create |  |  |
| /Event-store | Auth | POST | Ruta para almacenar un evento | App\Http\Controllers\EventController@store |  |  |
| /Event-edit/{id} | Auth | GET | Ruta para editar un evento | App\Http\Controllers\EventController@edit |  |  |
| /Event-update/{id} | Auth | PUT | Ruta para actualizar un evento | App\Http\Controllers\EventController@update |  |  |
| /Event-assistants/{id} | Auth | GET | Ruta para mostrar los asistentes de un evento | App\Http\Controllers\EventController@assistants |  |  |
| /Event-assistants-import | Auth | POST | Ruta para importar asistentes de un evento | App\Http\Controllers\EventController@fileImportExport |  |  |
| /Event-assistants-file | Auth | POST | Ruta para importar asistentes de un evento | App\Http\Controllers\EventController@fileImport |  |  |  
| /carlosbeltran | Auth | GET | Ruta para mostrar los eventos | App\Http\Controllers\EventController@manual_up |  |  |
| /Event-assistants-create/{id} | Auth | POST | Ruta para crear un asistente | App\Http\Controllers\EventController@assistants_create |  |  |
| /Event-assistants-delete/{id} | Auth | DELETE | Ruta para eliminar un asistente | App\Http\Controllers\EventController@assistantsDelete |  |  |
| //Event-activite/{id} | Auth | GET | Ruta para mostrar las actividades de un evento | App\Http\Controllers\EventController@activite |  |  |
| /downloads/attendess/template | Auth | GET | Ruta para descargar el template de asistentes | App\Http\Controllers\EventController@downloadAttendessTemplate |  |  |
| /Partner | Auth | GET | Ruta para mostrar los patrocinadores | App\Http\Controllers\PartnerController@index |  |  |
| /Partner-create | Auth | GET | Ruta para crear un patrocinador | App\Http\Controllers\PartnerController@create |  |  |
| /Partner-store | Auth | POST | Ruta para almacenar un patrocinador | App\Http\Controllers\PartnerController@store |  |  |
| /Partner-edit/{id} | Auth | GET | Ruta para editar un patrocinador | App\Http\Controllers\PartnerController@edit |  |  |
| /Partner-update/{id} | Auth | PUT | Ruta para actualizar un patrocinador | App\Http\Controllers\PartnerController@update |  |  |
| /Event/Registration/Report | Auth | GET | Ruta para mostrar el reporte de registro de asistentes | App\Http\Controllers\ReportController@event_report_index |  |  |
| /Event/Registration/Report/Generate | Auth | POST | Ruta para generar el reporte de registro de asistentes | App\Http\Controllers\ReportController@event_report_registration_generate |  |  |
| /Event/Tritiva/Report | Auth | GET | Ruta para mostrar el reporte de tritiva | App\Http\Controllers\ReportController@event_trivia_index |  |  |
| /Event/Tritiva/Report/Generate | Auth | POST | Ruta para generar el reporte de tritiva | App\Http\Controllers\ReportController@event_report_trivia_generate |  |  |
| /Event/Tritiva/get/list/{event_id} | Auth | GET | Ruta para obtener las trivias de un evento | App\Http\Controllers\ReportController@get_trivias_index |  |  |
| /Clients | Auth | GET | Ruta para mostrar los clientes | App\Http\Controllers\ClientController@index |  |  |
| /Clients-create | Auth | GET | Ruta para crear un cliente | App\Http\Controllers\ClientController@create |  |  |
| /Clients-store | Auth | POST | Ruta para almacenar un cliente | App\Http\Controllers\ClientController@store |  |  |
| /Clients-edit/{id} | Auth | GET | Ruta para editar un cliente | App\Http\Controllers\ClientController@edit |  |  |
| /Clients-update/{id} | Auth | PUT | Ruta para actualizar un cliente | App\Http\Controllers\ClientController@update |  |  |
| /Clients-delete/{id} | Auth | DELETE | Ruta para eliminar un cliente | App\Http\Controllers\ClientController@destroy |  |  |
| /WebSite | Auth | GET | Ruta para mostrar los sitios web | App\Http\Controllers\WebSiteController@index |  |  |
| /WebSite-setup/{event_id}/{tab_id?}/{item_modal_id?} | Auth | GET-POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_setup |  |  |
| /WebSite-setup-menu-page/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_menu_page |  |  |
| /WebSite-setup-menu-page/{event_id}/{option_id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_menu_page_delete_option |  |  |
| /WebSite-setups-schedule-day | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_schedule_day |  |  |
| /WebSite-setups-schedule-item | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_schedule_item |  |  |
| /WebSite-setup-news | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_new |  |  |
| /launch/questions | Auth | GET | Ruta para mostrar las preguntas | App\Http\Controllers\WebSiteController@launch_question |  |  |
| remove/shedule | Auth | POST | Ruta para eliminar un horario | App\Http\Controllers\WebSiteController@remove_shedule |  |  |
| remove/shedule/item | Auth | POST | Ruta para eliminar un horario | App\Http\Controllers\WebSiteController@remove_schedule_item |  |  |
| /WebSite-setup-questions | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_question |  |  |
| /WebSite-setup-question-option | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_question_option |  |  |
| /WebSite-setup-question-option/{event_id}/{tab_id}/{option_id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@delete_question_option |  |  |
| /WebSite-setup-page | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_page |  |  |
| /WebSite-setup-register-config-page/{event_id}/{config_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_register_config_page_delete_option |  |  |
| /WebSite-setup-register-config/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_register_config_page |  |  |
| /WebSite-setup-page/{event_id}/{option_id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@delete_page_slider_option |  |  |
| /WebSite-setup-page/{event_id}/{option_id} | Auth | PATCH | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@change_page_slider_option |  |  |
| /WebSite-setup-app | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_app |  |  |
| /WebSite-setup-menu-app/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_menu_app |  |  |
| /WebSite-setup-menu-app/{event_id}/{option_id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_menu_app_delete_option |  |  |
| /WebSite-setup-bussines-selectors-config/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@website_bussines_selectors_config_page |  |  |
| /WebSite-setup-page/meeting-live | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_meeting_live |  |  |
| /WebSite-setup-page/zoom-room | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_zoom_room |  |  |
| /WebSite-setup-company-registration/company-registration | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@company_registration_store |  |  |
| /WebSite-setup-company-registration-option/company-registration-option | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@company_registration_option_store |  |  |
| /WebSite-setup-company-registration/company-registration/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@company_registration_destroy |  |  |
| /WebSite-setup-company-registration-option/company-registration-option/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@company_registration_option_destroy |  |  |
| /WebSite-setup-meetings | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_setup_meetings |  |  |
| /WebSite-setup-categories-nw | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_setup_categories_nw |  |  |
| /WebSite-setup-categories-nw/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@delete_setup_categories_nw |  |  |
| /WebSite-setup-subcategories-nw | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_setup_subcategories_nw |  |  |
| /WebSite-setup-subcategories-nw/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@delete_setup_subcategories_nw |  |  |
| /WebSite-setup-type-company-nw | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_setup_type_company_nw |  |  |
| /WebSite-setup-type-company-nw/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@delete_setup_type_company_nw |  |  |
| /WebSite-setup-feedback-nw | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@store_setup_feedback_nw |  |  |
| /WebSite-setup-feedback-nw/{id} | Auth | DELETE | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\WebSiteController@feedback_question_delete |  |  |
| /VirtualSpace2D | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\InteractionController@index2 |  |  |
| /VirtualSpace2D-setup/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\InteractionController@setup |  |  |
| /InteractionList/{stand} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\InteractionController@index |  |  |
| /Interaction/edit/{id}/{stand} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\InteractionController@edit |  |  |
| /Interaction/edit/{id}/{stand} | Auth | PUT | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\InteractionController@update |  |  |
| /VirtualSpace | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@index |  |  |
| /VirtualSpace-setup/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@setup |  |  |
| /VirtualSpace-create_catalog/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@create_catalog |  |  |
| /VirtualSpace-create | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@store_catalog |  |  |
| /VirtualSpace-edit_catalog/{catalog_id}/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@edit_catalog |  |  |
| /VirtualSpace-update_catalog/{catalog_id}/{event_id} | Auth | PUT | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@update_catalog |  |  |
| /VirtualSpace-create_brand/{catalog_id}/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@create_brand |  |  |
| /VirtualSpace-store-brand | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@store_brand |  |  |
| /VirtualSpace-catalog_brand/{space_id}/{type_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@catalog_brand |  |  |
| /VirtualSpace-edit_brand/{catalog_id}/{event_id}/{id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@edit_brand |  |  |
| /VirtualSpace-update_brand/{id} | Auth | PUT | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\VirtualSpaceController@update_brand |  |  |
| /Notification | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NotificationController@index |  |  |
| /Notification-send/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NotificationController@notifications_send |  |  |
| /Notification-send/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NotificationController@send_notification |  |  |
| /Notification-email-send/{event_id} | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NotificationController@notifications_email |  |  |
| /Notification-email-send/{event_id} | Auth | POST | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NotificationController@notifications_email_send |  |  |
| /news | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\NewsController@index |  |  |
| /Execute | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\executeController@index |  |  |
| /Setting | Auth | GET | Ruta para mostrar la configuración de un sitio web | App\Http\Controllers\SettingController@index |  |  |
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
