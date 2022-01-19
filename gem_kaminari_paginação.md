# Gem Kaminari

+ Utilizada para "paginar"

+ Ou seja, dividir em várias páginas um grande conteúdo que ficaria muito extenso em uma única página.

+ [Documentação Kaminari](https://github.com/kaminari/kaminari)

+ Instalar:
~~~
# Used to paginate
gem 'kaminari'
~~~

+ Determinar quantos itens aparecem por página *.per(0)*
~~~
@admins = Admin.all.page(params[:page]).per(X)    #X é o número que vc quer colocar.
~~~

+ Para traduzir (ANTES DEVE ESTAR CONFIGURADO O i18n):
~~~
gem 'kaminari-i18n'
~~~



