# Para acessar e editar as rotas:
+ Acessar **CONFIG/routes.rb**

## Para fazermos o mapeamento padrão (a página inicial da aplicação) usamos:
~~~
root to: "welcome#index"
~~~

# RESOURCES
*Cria as 7 rotas padrão do CRUD* (index, new, create, delete, edit, show, update) apenas com:
~~~
resources :exemplo
~~~
*Para habilitar APENAS as rotas escolhidas:
~~~
resources :admins, only: [:index, :edit]
~~~

#Img: tabela das rotas.

# Criar as próprias rotas:
*Basta declarar o VERBO; a URL; o CONTROLLER e a ACTION... Exemplo:*
~~~lang-rb
get '/inicio', to: 'welcome#index'
~~~
**A rota acima quando digitar url/inicio acessará o controller WELCOME e a ação INDEX**
