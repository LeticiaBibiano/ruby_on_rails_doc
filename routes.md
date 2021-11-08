# Para acessar e editar as rotas:
+ Acessar **CONFIG/routes.rb**

## Para fazermos o mapeamento padrão (a página inicial da aplicação) usamos:
~~~
root to: "welcome#index"
~~~

# RESOURCES
*Cria as 7 rotas padrão do CRUD*, apenas com:
~~~
resources :exemplo
~~~

| HTTP Verb |	Path |	Controller#Action | Used for |
|---|---|
| GET	| /photos |	photos#index |	display a list of all photos |
| GET |	/photos/new |	photos#new |	return an HTML form for creating a new photo |
| POST |	/photos	| photos#create | create a new photo |
| GET	| /photos/:id	| photos#show |	display a specific photo |
| GET	| /photos/:id/edit |	photos#edit |	return an HTML form for editing a photo |
| PATCH/PUT	| /photos/:id	| photos#update	| update a specific photo |
| DELETE | /photos/:id	| photos#destroy	| delete a specific photo |
