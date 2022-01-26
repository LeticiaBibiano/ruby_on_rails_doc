# Devise Controller
+ A gem Devise cria seu próprio controller para LOGIN

## Usando outro layout na tela de LOGIN DEVISE (Lembrando que: se não informar nenhum layout = application)

+ Usando os helpers *devise_controller* e *resource_class*

### devise_controller
+ Verifica se o controller que está sendo acessado pertence ao Devise.

### resource_class
+ Verifica qual classe do Devise está sendo acessada.

+ No *application_controller.rb*
~~~
class ApplicationController < ActionController::Base
  layout :layout_by_resource #método protected

  protected

    def layout_by_resource
      if devise_controller? && resource_class == Admin #SE devise_controller? TRUE & classe ADMIN
        "admin_devise" #Usa esse layout
      else 
        "application" #senão usa esse layout
      end
    end
end

~~~
