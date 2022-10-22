## Documentación de rutas utilizadas en Livent Panel

En esta sección se detallan las rutas utilizadas en Livent Panel en una tabla con el endpoint, el método, la descripción, el controlador, parametros que recibe y salidas que retorna.

    Route::post('/WebSite-setups-schedule-day', 'WebSiteController@website_schedule_day')
        ->name('website.schedule-day');

    Route::post('/WebSite-setups-schedule-item', 'WebSiteController@website_schedule_item')
        ->name('website.schedule-item');

    Route::post('/WebSite-setup-news', 'WebSiteController@store_new')
        ->name('website.new-store');

    Route::post('launch/questions', 'WebSiteController@launch_question')->name('launch_question');

    Route::post('remove/shedule', 'WebSiteController@remove_schedule')->name('schedule.remove');
    Route::post('remove/shedule/item', 'WebSiteController@remove_schedule_item')->name('schedule.remove.item');

    Route::post('/WebSite-setup-questions', 'WebSiteController@store_question')
        ->name('website.question-store');

    Route::post('/WebSite-setup-question-option', 'WebSiteController@store_question_option')
        ->name('website.question-option-store');

    Route::delete('/WebSite-setup-question-option/{event_id}/{tab_id}/{option_id}', 'WebSiteController@delete_question_option')
        ->name('website.question-option-delete');

    Route::post('/WebSite-setup-page','WebSiteController@store_page')
        ->name('website.page-store');

    Route::delete('/WebSite-setup-register-config-page/{event_id}/{config_id}', 'WebSiteController@website_register_config_page_delete_option')
        ->name('website.register-config-page-delete-option');

    Route::post('/WebSite-setup-register-config/{event_id}', 'WebSiteController@website_register_config_page')
        ->name('website.register-config-page');

    Route::delete('/WebSite-setup-page/{event_id}/{option_id}', 'WebSiteController@delete_page_slider_option')
        ->name('website.page-slider-option-delete');

    Route::patch('/WebSite-setup-page/{event_id}/{option_id}', 'WebSiteController@change_page_slider_option')
        ->name('website.page-slider-option-change');

    Route::post('/WebSite-setup-app','WebSiteController@store_app')
        ->name('website.app-store');

    Route::post('/WebSite-setup-menu-app/{event_id}', 'WebSiteController@website_menu_app')
        ->name('website.menu-app');

    Route::delete('/WebSite-setup-menu-app/{event_id}/{option_id}', 'WebSiteController@website_menu_app_delete_option')
        ->name('website.menu-app-delete-option');

    Route::post('/WebSite-setup-bussines-selectors-config/{event_id}', 'WebSiteController@website_bussines_selectors_config_page')
        ->name('website.bussines_selectors_config');

    Route::post('/WebSite-setup-page/meeting-live','WebSiteController@store_meeting_live')
        ->name('website.meeting-live-store');

    Route::post('/WebSite-setup-page/zoom-room', 'WebSiteController@store_zoom_room')
        ->name('website.zoom-room-store');

    Route::post('/WebSite-setup-company-registration/company-registration', 'WebSiteController@company_registration_store')
        ->name('company-registration.store');

    Route::post('/WebSite-setup-company-registration-option/company-registration-option', 'WebSiteController@company_registration_option_store')
        ->name('company-registration-option.store');

     Route::delete('/WebSite-setup-company-registration/company-registration/{id}', 'WebSiteController@company_registration_destroy')
        ->name('company-registration.destroy');

    Route::delete('/WebSite-setup-company-registration-option/company-registration-option/{id}', 'WebSiteController@company_registration_option_destroy')
        ->name('company-registration-option.destroy');

    Route::post('/WebSite-setup-meetings', 'WebSiteController@store_setup_meetings')
        ->name('WebSite.setup-meetings-store');

    Route::post('/WebSite-setup-categories-nw', 'WebSiteController@store_setup_categories_nw')
        ->name('WebSite.setup-categories-nw-store');

    Route::delete('/WebSite-setup-categories-nw/{id}', 'WebSiteController@delete_setup_categories_nw')
        ->name('WebSite.setup-categories-nw-delete');

    Route::post('/WebSite-setup-subcategories-nw', 'WebSiteController@store_setup_subcategories_nw')
        ->name('WebSite.setup-subcategories-nw-store');

    Route::delete('/WebSite-setup-subcategories-nw/{id}', 'WebSiteController@delete_setup_subcategories_nw')
        ->name('WebSite.setup-subcategories-nw-delete');

    Route::post('/WebSite-setup-type-company-nw', 'WebSiteController@store_setup_type_company_nw')
        ->name('WebSite.setup-type-company-nw-store');

    Route::delete('/WebSite-setup-type-company-nw/{id}', 'WebSiteController@delete_setup_type_company_nw')
        ->name('WebSite.setup-type-company-nw-delete');

    Route::post('/WebSite-setup-feedback-nw', 'WebSiteController@store_setup_feedback_nw')
        ->name('WebSite.setup-feedback-nw-store');

    Route::delete('/WebSite-setup-feedback-nw/{id}', 'WebSiteController@feedback_question_delete')
        ->name('WebSite.setup-feedback-nw-delete');



      /* Virtual Space */
      Route::get('/VirtualSpace2D', 'InteractionController@index2')->name('VirtualSpace2d');
      Route::get('/VirtualSpace2D-setup/{event_id}', 'InteractionController@setup')->name('VirtualSpace2d.setup');

      Route::get('/InteractionList/{stand}', 'InteractionController@index')->name('VirtualSpace2d.interactionList');
      Route::get('/Interaction/edit/{id}/{stand}', 'InteractionController@edit')->name('VirtualSpace2d.interactionedit');
      Route::put('/Interaction/edit/{id}/{stand}', 'InteractionController@update')->name('VirtualSpace2d.interactionupdate');


    /* Virtual Space */
    Route::get('/VirtualSpace', 'VirtualSpaceController@index')->name('VirtualSpace');
    Route::get('/VirtualSpace-setup/{event_id}', 'VirtualSpaceController@setup')->name('VirtualSpace.setup');

    Route::get('/VirtualSpace-create_catalog/{event_id}', 'VirtualSpaceController@create_catalog')->name('VirtualSpace.create-catalog');
    Route::post('/VirtualSpace-create', 'VirtualSpaceController@store_catalog')->name('VirtualSpace.store_catalog');
    Route::get('/VirtualSpace-edit_catalog/{catalog_id}/{event_id}', 'VirtualSpaceController@edit_catalog')->name('VirtualSpace.edit_catalog');
    Route::put('/VirtualSpace-update_catalog/{catalog_id}/{event_id}', 'VirtualSpaceController@update_catalog')->name('VirtualSpace.update_catalog');

    Route::get('/VirtualSpace-create_brand/{catalog_id}/{event_id}', 'VirtualSpaceController@create_brand')->name('VirtualSpace.create_brand');
    Route::post('/VirtualSpace-store-brand', 'VirtualSpaceController@store_brand')->name('VirtualSpace.store_brand');
    Route::get('/VirtualSpace-catalog_brand/{space_id}/{type_id}', 'VirtualSpaceController@catalog_brand')->name('VirtualSpace.catalog_brand');
    Route::get('/VirtualSpace-edit_brand/{catalog_id}/{event_id}/{id}','VirtualSpaceController@edit_brand')->name('VirtualSpace.edit_brand');
    Route::put('/VirtualSpace-update_brand/{id}','VirtualSpaceController@update_brand')->name('VirtualSpace.update_brand');

    /**NOTIFICACIONES */

    Route::get('/Notification', 'NotificationController@index')
        ->name('Notifications');

    Route::get('/Notification-send/{event_id}', 'NotificationController@notifications_send')
        ->name('Notifications.send');

    Route::post('/Notification-send/{event_id}', 'NotificationController@send_notification')
        ->name('Notification.send');

    Route::get('/Notification-email-send/{event_id}', 'NotificationController@notifications_email')
        ->name('Notifications.email');

    Route::post('/Notification-email-send/{event_id}', 'NotificationController@notifications_email_send')
        ->name('Notifications.email.send');

    ///Solicitud ajasx de las noticas
    Route::get('/news', 'NewController@get_news');


    Route::get('/Execute', 'executeController@index')
        ->name('Execute');
    Route::get('/Setting', 'SettingController@index')
        ->name('Setting');

    Route::prefix('Networking')->group(function () {

        //Rutas de inicio
        Route::post('NetworkingPlan', 'NetworkingPlanController@index')
            ->name('NetworkingPlan');

        Route::get('NetworkingPlan', 'NetworkingPlanController@index')
            ->name('NetworkingPlan');


        // Customer - Clientes
        Route::get('Customer', 'NetworkingCustomerController@index')
            ->name('NetworkingCustomer');

        Route::get('Customer-create', 'NetworkingCustomerController@create')
            ->name('NetworkingCustomerCreate');

        Route::post('Customer-store', 'NetworkingCustomerController@store')
            ->name('NetworkingCustomerStore');

        Route::get('Customer-edit/{NwCustomer}', 'NetworkingCustomerController@edit')
            ->name('NetworkingCustomerEdit');

        Route::patch ('Customer-update/{NwCustomer}', 'NetworkingCustomerController@update')
            ->name('NetworkingCustomerUpdate');

        Route::delete('Customer-delete','NetworkingCustomerController@destroy')
            ->name('NetworkingCustomerDelete');

        Route::post('Customer-status', 'NetworkingCustomerController@status')
            ->name('NetworkingCustomerStatus');


        // Halls - Pabellones
        Route::get('Hall', 'NetworkingHallController@index')
            ->name('NetworkingHall');

        Route::get('Hall-create', 'NetworkingHallController@create')
            ->name('NetworkingHallCreate');

        Route::post('Hall-store', 'NetworkingHallController@store')
            ->name('NetworkingHallStore');

        Route::get('Hall-edit/{NwHall}', 'NetworkingHallController@edit')
            ->name('NetworkingHallEdit');

        Route::patch('Hall-update/{NwHall}', 'NetworkingHallController@update')
            ->name('NetworkingHallUpdate');

        Route::delete('Hall-delete', 'NetworkingHallController@destroy')
            ->name('NetworkingHallDelete');

        Route::post('Hall-status', 'NetworkingHallController@status')
            ->name('NetworkingHallStatus');


        // Stands - exhibidores
        Route::get('Stand', 'NetworkingStandController@index')
            ->name('NetworkingStand');

        Route::get ('Stand-create', 'NetworkingStandController@create')
            ->name('NetworkingStandCreate');

        Route::get ('Stand-edit/{NwStand}', 'NetworkingStandController@edit')
            ->name('NetworkingStandEdit');

        Route::post('Stand-store', 'NetworkingStandController@store')
            ->name('NetworkingStandStore');

        Route::get ('Stand-edit/{NwStand}', 'NetworkingStandController@edit')
            ->name('NetworkingStandEdit');

        Route::patch ('Stand-update/{NwStand}', 'NetworkingStandController@update')
            ->name('NetworkingStandUpdate');

        Route::delete('Stand-delete', 'NetworkingStandController@destroy')
            ->name('NetworkingStandDelete');

        Route::post('Stand-status', 'NetworkingStandController@status')
                ->name('NetworkingStandStatus');

         // Meeting - Reuniones
        Route::get('Meeting', 'NetworkingMeetingController@index')
            ->name('NetworkingMeeting');

        Route::get ('Meeting-create', 'NetworkingMeetingController@create')
            ->name('NetworkingMeetingCreate');

        Route::post('Meeting-store', 'NetworkingMeetingController@store')
            ->name('NetworkingMeetingStore');

        Route::get ('Meeting-edit/{NwMeeting}', 'NetworkingMeetingController@edit')
            ->name('NetworkingMeetingEdit');

        Route::delete('Meeting-delete', 'NetworkingMeetingController@destroy')
            ->name('NetworkingMeetingDelete');

        Route::post('Meeting-status', 'NetworkingMeetingController@status')
            ->name('NetworkingMeetingStatus');

        Route::get('Meeting-Attend', 'NetworkingMeetingController@attend')
            ->name('NetworkingMeetingAttend');

        Route::post('Meeting-Finish', 'NetworkingMeetingController@finish')
            ->name('NetworkingMeetingFinish');

        Route::patch ('Meeting-update/{NwMeeting}', 'NetworkingMeetingController@update')
            ->name('NetworkingMeetingUpdate');

        Route::get ('Meeting-update-show/{NwMeeting}', 'NetworkingMeetingController@show')
            ->name('NetworkingMeetingAttendShow');

        Route::get ('Meeting-video-show', 'NetworkingMeetingController@video')
            ->name('NetworkingMeetingVideo');

        Route::get('Videoconference', 'NetworkingMeetingController@videoconference')
            ->name('NetworkingVideoconference');



        // Executive - Ejecutivos
        Route::get('Executive', 'NetworkingExecutiveController@index')->name('NetworkingExecutive');
        Route::get ('Executive-create', 'NetworkingExecutiveController@create')->name('NetworkingExecutiveCreate');
        Route::post ('Executive-store', 'NetworkingExecutiveController@store')->name('NetworkingExecutiveStore');
        Route::post ('Executive-show-user', 'NetworkingExecutiveController@showuser')->name('NetworkingExecutiveShowUser');
        Route::post ('Executive-delete', 'NetworkingExecutiveController@destroy')->name('NetworkingExecutiveDelete');

        // Users - Usuarios
        Route::get('Users', 'NetworkingUsersController@index')->name('NetworkingUsers');
        Route::get ('Users-create', 'NetworkingUsersController@create')->name('NetworkingUsersCreate');
        Route::post ('Users-store', 'NetworkingUsersController@store')->name('NetworkingUsersStore');
        Route::get ('Users-edit/{UsersNw}', 'NetworkingUsersController@edit')->name('NetworkingUsersEdit');
        Route::patch ('Users-update/{UsersNw}', 'NetworkingUsersController@update')->name('NetworkingUsersUpdate');
        Route::post('Users-status', 'NetworkingUsersController@status')->name('NetworkingUsersStatus');

        // Participantes
        Route::get('Guest', 'NetworkingGuestController@index')->name('NetworkingGuest');
        Route::get('GuestVisitStand/{stand_id}', 'NetworkingGuestController@VisitStand')->name('GuestVisitStand');
        Route::get('GuestMyMeeting/{event_id}', 'NetworkingGuestController@MyMeeting')->name('GuestMyMeeting');
        Route::get('GuestProfile/{event_id}', 'NetworkingGuestController@Profile')->name('GuestProfile');
        Route::post('GuestAttend', 'NetworkingGuestController@Attend')->name('GuestAttend');
        Route::get('GuestTarget/{event_id}', 'NetworkingGuestController@Target')->name('GuestTarget');
        Route::get('GuestExplore/{event_id}', 'NetworkingGuestController@Explore')->name('GuestExplore');


    });
    Route::post('showexecutivecustomer', 'NetworkingAjaxController@showexecutivecustomer')->name('NetworkingExecutiveShowCustomer');
    Route::post('GuestReadMeeting', 'NetworkingAjaxController@GuestReadMeeting')->name('NetworkingGuestReadMeeting');
    Route::post('ActivateRoom', 'NetworkingAjaxController@ActivateRoom')->name('NetworkingActivateRoom');

    Route::post('GuestProfile-delete', 'NetworkingAjaxController@ProfileDelete')->name('NetworkingGuestProfileDelete');
    Route::post('GuestProfile-insert', 'NetworkingAjaxController@ProfileInsert')->name('NetworkingGuestProfileInsert');
    Route::post('GuestProfile-show-attribute', 'NetworkingAjaxController@ProfileShowAttribute')->name('NetworkingGuestProfileShowAttribute');
    Route::post('GuestProfile-show-attribute-profile', 'NetworkingAjaxController@ProfileShowAttributeProfile')->name('NetworkingGuestProfileShowAttributeProfile');
    Route::post('GuestProfile-category-create', 'NetworkingAjaxController@ProfileCategoryCreate')->name('NetworkingGuestProfileCategoryCreate');
    Route::post('GuestProfile-attribute-create', 'NetworkingAjaxController@ProfileAttributeCreate')->name('NetworkingGuestProfileAttributeCreate');

    Route::post('GuestTarget-create', 'NetworkingAjaxController@TargetCreate')->name('NetworkingGuestTargetCreate');
    Route::post('GuestTarget-show-attribute-free', 'NetworkingAjaxController@TargetShowAttributeFree')->name('NetworkingGuestShowAttributeFree');
    Route::post('GuestTarget-show-attribute', 'NetworkingAjaxController@TargetShowAttribute')->name('NetworkingGuestShowAttribute');
    Route::post('GuestTarget-insert', 'NetworkingAjaxController@TargetInsert')->name('NetworkingGuestTargetInsert');
    Route::post('GuestTarget-delete', 'NetworkingAjaxController@TargetDelete')->name('NetworkingGuestTargetDelete');


    /**
     * REPORTES
     */
    Route::get('Reports/networking', 'ReportController@networking')
        ->name('Reports.networking');

    Route::get('Reports/networking/meetings', 'ReportController@networking_meetings')
        ->name('Reports.networking.meetings');

    Route::post('Reports/networking/meetings/generate', 'ReportController@networking_meetings_generate')
        ->name('Reports.networking.meetings.generate');


    Route::get('Reports/networking/feedback', 'ReportController@networking_feedback')
        ->name('Reports.networking.feedback');

    Route::post('Reports/networking/feedback/generate', 'ReportController@networking_feedback_generate')
        ->name('Reports.networking.feedback.generate');

    Route::get('Reports/networking/company', 'ReportController@networking_company')
        ->name('Reports.networking.company');

    Route::post('Reports/networking/company/generate', 'ReportController@networking_company_generate')
        ->name('Reports.networking.company.generate');


    Route::get('question/feedback/get', 'ReportController@get_questions')
    ->name('feedback.feedback.get');



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
