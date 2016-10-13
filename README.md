Oi Helio,

Tudo bom :)

Então, estamos com os dois projetos rodando online. Estou te dando o acesso com um pouco antes de nosso encontro para você poder ir ficando familiar com o ambiente que estamos trabalhando :)

Compartilhei contigo o acesso pelo c9 aos dois ambientes:

    google-brasiliaio (aplicação ruby)
        default
            Está rodando no endereço web: http://yoga.smartmarket.io/subdomains/1

    brasiliaio-mob (aplicação ionic)
        brasiliaio-material/demo
            Está rodando no endereço: http://git-music.org/#/app/login

Fiz alguns testes e adicionei alguns arquivos...

**1) Criar conta e logar com email:**

consigo criar contas com email pelo site

consigo logar nas contas com email pelo site

consigo criar contas com e-mail usando o Postman (para testar api)

**Não consigo nem criar conta nem logar com email usando a aplicação ionic**


**2) Criar conta e logar com facebook e google plus**

As contas com google plus e facebook, são criadas pelo **site**, mas não é realizado o login

**não consigo criar logar pelo site, nem usando google plus nem facebook**

**não consigo criar contas nem logar usando o google plus ou facebook pela aplicação ionic**

Eu acredito que falte alguma configuração pequena que resolverá ambos os problemas :)


Valeu


Aqui estão as rotas que estabeleci e configurei ambas as aplicações:

    new_api_user_session_path	        GET 	/api/auth/sign_in(.:format)	    devise_token_auth/sessions#new
    api_user_session_path		        POST	/api/auth/sign_in(.:format)	    devise_token_auth/sessions#create
    destroy_api_user_session_path	    DELETE	/api/auth/sign_out(.:format)	devise_token_auth/sessions#destroy
    api_user_password_path		        POST	/api/auth/password(.:format)	devise_token_auth/passwords#create
    new_api_user_password_path	        GET	    /api/auth/password/new(.:format)   	devise_token_auth/passwords#new
    edit_api_user_password_path	        GET	    /api/auth/password/edit(.:format)	devise_token_auth/passwords#edit
                                        PATCH	/api/auth/password(.:format)	devise_token_auth/passwords#update
                                        PUT	    /api/auth/password(.:format)	devise_token_auth/passwords#update
    cancel_api_user_registration_path	GET	    /api/auth/cancel(.:format)	    devise_token_auth/registrations#cancel
    api_user_registration_path	        POST	/api/auth(.:format)	            devise_token_auth/registrations#create
    new_api_user_registration_path	    GET	    /api/auth/sign_up(.:format)	    devise_token_auth/registrations#new
    edit_api_user_registration_path	    GET	    /api/auth/edit(.:format)	    devise_token_auth/registrations#edit
                                        PATCH	/api/auth(.:format)	            devise_token_auth/registrations#update
                                        PUT	    /api/auth(.:format)	            devise_token_auth/registrations#update
                                        DELETE	/api/auth(.:format)	            devise_token_auth/registrations#destroy
    api_user_confirmation_path	        POST	/api/auth/confirmation(.:format)	devise_token_auth/confirmations#create
    new_api_user_confirmation_path	    GET	    /api/auth/confirmation/new(.:format)	devise_token_auth/confirmations#new
                                        GET	    /api/auth/confirmation(.:format)	devise_token_auth/confirmations#show
    api_auth_validate_token_path	    GET	    /api/auth/validate_token(.:format)	devise_token_auth/token_validations#validate_token
    api_auth_failure_path	            GET	    /api/auth/failure(.:format)	    devise_token_auth/omniauth_callbacks#omniauth_failure
                                        GET	    /api/auth/:provider/callback(.:format)	devise_token_auth/omniauth_callbacks#omniauth_success
                                        GET	    /omniauth/:provider/callback(.:format)	devise_token_auth/omniauth_callbacks#redirect_callbacks
    omniauth_failure_path	            GET	    /omniauth/failure(.:format)	    devise_token_auth/omniauth_callbacks#omniauth_failure
                                        GET	    /api/auth/:provider(.:format)	redirect(301)