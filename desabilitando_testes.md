# Podemos desabilitar os TDD que automaticamente são criados pela APP

+ Iniciando a APP sem testes:
~~~
💲 rails new nome_aplicação -T
~~~

### Retirando testes da sua APP já iniciada:

+ No arquivo 📂**config/application.rb**

**No início do arquivo**
~~~
  #require "rails/all"
  require "rails"
  # Pick the frameworks you want:
  require "active_model/railtie"
  require "active_job/railtie"
  require "active_record/railtie"
  require "active_storage/engine"
  require "action_controller/railtie"
  require "action_mailer/railtie"
  require "action_view/railtie"
  require "action_cable/railtie"
  require "sprockets/railtie"
  # require "rails/test_unit/railtie"
~~~

**Dentro de class Application < Rails::Application**
~~~
    # Don't generate system test files.
    config.generators.system_tests = nil
~~~

## Para que as atualizações funcione, devemos reiniciar o SPRING (Memória do Rails):
~~~
💲 spring stop
~~~

+ Depois, basta rodar um comando *generate* para a APP levantar novamente com spring atualizado ⚠️
