# Layout APPLICATION
+ É a maior parte do template, que sempre carrega em TODAS AS PÁGINAS.
+ 📂**APP/VIEWS/LAYOUTS**/application.html.erb

## Criando outro layout
+ Na pasta de layouts crie outro arquivo no formato = **exemplo.html.erb**
+ **NO CONTROLLER DA VIEW =** coloque no código:
~~~
layout "exemplo"
~~~
+ Exemplo de arquivo CONTROLLER
~~~
class AdminsBackoffice::WelcomeController < ApplicationController
  layout 'admins_backoffice'
  def index
  end
end
~~~
*Caso nenhum layout seja especificado, o Rails utilizará o PADRÃO (application.html.erb).

## Os novos Layouts devem ter seus próprios *CONTROLLERS*:

+ Criar controller com o nome do layout:
~~~
💲 rails g controller nome_layout 

💲 rails g controller admins_backoffice #exemplo
~~~
