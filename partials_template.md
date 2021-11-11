# Partials
+ Partials permitem renderizar uma view dentro de outra, ou seja, *"reutilizar páginas/views"*.
+ Crie sempre arquivos únicos para cada Partial, dessa forma = **_menu.html.rb** (PERCEBA O UNDERLINE NO INÍCIO DO ARQUIVO!!!).

## Para utilizar a Partial criada...
+ No arquivo da view, usamos:
~~~
<%= render "menu" %>
~~~
*Escrevemos entre "aspas" apenas o nome da Partial, o sistema Rails identificará o arquivo automaticamente*
