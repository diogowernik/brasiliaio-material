### Brasília \o Mobile App - Ionic-Material


#### Tarefa 1 - Login**

Aplicação Web: http://yoga.brasilia.io

Aplicação Mobile: https://github.com/diogowernik/brasiliaio-material ( http://git-music.org )

**demo/www/templates/login.html**

1) Realizar login na aplicação utilizando email

2) Realizar login na aplicação utilizando google plus

3) Realizar login na aplicação utilizando facebook

#### Tarefa 2 - Criação de Conta

Aplicação Web: http://yoga.brasilia.io

Aplicação Mobile: https://github.com/diogowernik/brasiliaio-material ( http://git-music.org )

**demo/www/templates/sign-up.html**

1) Criar conta por email

2) Criar conta com facebook

3) Criar conta com google plus

#### Observações:

Login aplicação web: http://yoga.brasilia.io/login

Sign up aplicação web: http://yoga.brasilia.io/sign_up

#### Rotas Users (GET, POST, DELETE, PUT, PATCH)

```
new_user_session_path       	GET	        /login(.:format)	devise/sessions#new
user_session_path	            POST	    /login(.:format)	devise/sessions#create
destroy_user_session_path	    DELETE	    /sign_out(.:format)	devise/sessions#destroy
user_omniauth_authorize_path	GET|POST	/auth/:provider(.:format)	omniauth_callbacks#passthru {:provider=>/facebook|google_oauth2/}
user_omniauth_callback_path	    GET|POST	/auth/:action/callback(.:format)	omniauth_callbacks#(?-mix:facebook|google_oauth2)
user_password_path	            POST    	/password(.:format)	devise/passwords#create
new_user_password_path	        GET	        /password/new(.:format)	devise/passwords#new
edit_user_password_path	        GET	        /password/edit(.:format)	devise/passwords#edit
                                PATCH      	/password(.:format)	devise/passwords#update
                                PUT     	/password(.:format)	devise/passwords#update
cancel_user_registration_path	GET     	/cancel(.:format)	devise/registrations#cancel
user_registration_path	        POST	/   devise/registrations#create
new_user_registration_path	    GET	        /sign_up(.:format)	devise/registrations#new
edit_user_registration_path	    GET     	/profile(.:format)	devise/registrations#edit
                                PATCH	/	devise/registrations#update
                                PUT	    /	devise/registrations#update
                                DELETE	/	devise/registrations#destroy
```



**about this template**

https://github.com/zachfitz/Ionic-Material
