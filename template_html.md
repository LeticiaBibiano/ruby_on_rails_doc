# Podemos usar TEMPLATES PRONTOS em nossa aplicação Rails!

+ Procuramos em sites de templates o arquivo que queremos, exemplos:
+ [Gentelella](https://github.com/ColorlibHQ/gentelella)
+ [SB-Admin2](https://github.com/BlackrockDigital/startbootstrap-sb-admin-2.git)

## Inserindo o TEMPLATE no projeto:

+ Na pasta 📂**public** = criar uma pasta chamada 📁**templates**
+ Na pasta 📂Templates = CLONE o projeto do template escolhido.
+ NÃO SE ESQUEÇA DE APAGAR A PASTA ***.git***
+ CLONAMOS o projeto do template para dentro de 📂**templates**
~~~
💲 git clone https://github.com/blablabla
~~~
+ Dentro da pasta 📂**production** ou 📂**pages** (DEPENDE DE CADA PROJETO) estão os arquivos HTML
+ No arquivo INDEX.HTML clicamos com o botão direito do mouse e copiamos o ***Relative Path***
+ Ao acessarmos essa rota = public/templates/gentelella/production/index.html = (APAGANDO O PUBLIC!!!), teremos o template completo aberto em nossa tela do projeto.

🥸 ***DESSA FORMA DISPONIBILIZAMOS OS TEMAS LOCALMENTE!*** 🤓

# Agora, vamos usar o tema no local da aplicação:

+ Remover o Turbolinks (Pois pode conflitar com o tema).
  1. Vá no Gemfile e comente a gem #turbolinks.
  2. Remover Tubolinks do arquivo ***application.js***.
  3. Remover o *media: turbolinks* de todos os 📁***LAYOUTS***

+ Abrir o tema no localhost, analisar e copiar o que você quer...
+ COLAR na view do projeto e fazer as devidas alterações!

+ Em ***application.CSS*** e ***application.JS***, retirar o *require_tree* = PARA NÃO PEGAR TODOS OS ARQUIVOS DE UMA VEZ!

+ Verificar quais as BIBLIOTECAS usadas no template para instalar no projeto e fazer o TEMA FUNCIONAR:
+ ACHOU AS VERSÕES DAS BIBLIOTECAS?? ➡️ Pois agora, instale via [YARN](https://yarnpkg.com/)
~~~
💲 yarn add bootstrap@3.3.7 #VERIFIQUE A VERSÃO
~~~


