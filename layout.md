# Layout APPLICATION
+ É a maior parte do template, que sempre carrega em TODAS AS PÁGINAS.
+ 📂**APP/VIEWS/LAYOUTS**/application.html.erb

## Criando outro layout
+ Na pasta de layouts crie outro arquivo no formato = **exemplo.html.erb**
+ **NO CONTROLLER DA VIEW =** coloque no código:
~~~
layout "exemplo"
~~~
*Caso nenhum layout seja especificado, o Rails utilizará o PADRÃO (application.html.erb).
