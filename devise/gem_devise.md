# Para que serve a Gem Devise?
+ Para protegermos com LOGIN e SENHA as "Áreas" em nossa aplicação, por exemplo: Área do Usuário e Área do Administrador.
+ Com Devise, conseguimos criar Login's específicos para cada área.
+ OU SEJA, criamos uma AUTENTICAÇÃO para a nossa APP! 

[Documentação DEVISE](https://github.com/heartcombo/devise)

# Instalando

~~~
gem 'devise' #dentro do GEMFILE
~~~

+ Após rodar o "bundle", devemos instalar o *generate*:
~~~
💲 rails generate devise:install
~~~

+ No arquivo 📂**config/environments/development.rb**
~~~
# Devise config
config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
~~~

+ Para criar o MODEL para a área que queremos criar:
~~~
💲 rails generate devise NomeModel
~~~
*Caso queira duas áreas, crie dois Models, um para User e outro para Admin*

### Para habilitar 2 VIEWS DIFERENTES para cada Model (User e Admin):

+ No arquivo 📂**config/initializers/devise.rb** estará *# config.scoped_views = false*, "descomente" e mude para:
~~~
config.scoped_views = true
~~~

⚠️ *Se não habilitarmos essa opção, as Views serão as mesmas para todos!*

### Gerando as VIEWS:

~~~
💲 rails generate devise:views users #NOME DA VIEW NO PLURAL
~~~

### Para finalizar a instalação:
~~~
💲 rails db:migrate
~~~

# Protegendo com login e senha

+ No ***CONTROLLER*** da "área":
*Supondo que _user sejá o nome do Model, ex: user, admin*
~~~
  before_action :authenticate_user!
~~~





