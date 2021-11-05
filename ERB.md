# O que é ERB (Embedded Ruby):

*Em resumo, é a forma de mesclar texto com código Ruby*

## Diferente da interpolação com #{}...

O ERB também trabalha com textos, HTML e espressões Ruby, ou seja, é muito mais completo do que uma simples interpolação.

# <<-
Usamos <<-ABC (texto aqui) ABC, para textos grandes. 

**Não coloca-se texto grande dentro de "string"!**

+ Exemplo:
~~~
<<-EOF
    Textão aqui
    Textão aqui
    Textão aqui
    Textão aqui
EOF
~~~
