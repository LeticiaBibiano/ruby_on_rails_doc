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

# Algumas tags que podemos usar para interpolação no ERB:
~~~
<% Ruby code -- inline with output %>

<%= Ruby expression -- replace with result %>

<%# comment -- ignored -- useful in testing %>

% a line of Ruby code -- treated as <% line %> (optional -- see ERB.new)

%% replaced with % if first thing on a line and % processing is used

<%% or %%> -- replace with <% or %> respectively
~~~
