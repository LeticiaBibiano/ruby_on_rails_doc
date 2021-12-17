# Criando Backoffices (Áreas específicas)

+ Um backoffice pode ser uma Área do Usuário ou Área do Administrador.

## Criando:

+ Criamos um controller para cada Backoffice:
~~~
💲 rails g controller admins_backoffice/welcome index

💲 rails g controller users_backoffice/welcome index
~~~
*Nomes de controller sempre no PLURAL, por padrão!*
