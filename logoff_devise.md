# Como criar o LOGOFF para a Gem Devise

+ Olhando as rotas em **/rails/info/routes**, descobrimos a rota de sign_out = *destroy_admin_session_path*, com method = *DELETE*, portanto:

~~~
<%= link_to 'Fazer Logoff', destroy_admin_session_path, method: :destroy%>
~~~

*Tanto para ADMIN, quanto para USER!*

🧧⚠️ **ATENÇÃO:** O DEVISE por PADRÃO, faz LOGOFF de todos os escopos (áreas) de uma vez, para mudar esse configuração... OLHA AÍ: 

+ Em 📂***config/initializers/devise.rb***, descomentar:
~~~
# config.sign_out_all_scopes = true
~~~
E mudar para FALSE:
~~~
config.sign_out_all_scopes = false
~~~
