# Nested Attributes
+ São ATRIBUTOS ANINHADOS, ou seja, atributos de DUAS TABELAS em uma só!

~~~
  has_many :answers
  accepts_nested_attributes_for :answers #aceita atributos de outra tabela!
~~~
