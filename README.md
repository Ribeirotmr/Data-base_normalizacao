# Trabalho de designer e desenvolvimento de banco de dados


### Esse projeto de banco de dados tem como base transforma um modelo conceitual em modelo lógico por meio da primeira regra de normaliozação de banco de dados. 

# O que é o processo de normalização de banco de dados ? 

*A normalização do banco de dados é o processo de transformações na estrutura de um banco de dados que visa a eliminar redundâncias e a eliminar anomalias de inserção, atualização e exclusão. Ao efetuar o processo de normalização, os dados cadastrados no banco de dados ficarão organizados de uma forma melhor e na maioria das vezes também ocuparão menos espaço físico. Entretanto, o processo de normalização também sempre faz aumentar o número de tabelas e em muitos casos pode ser uma tarefa difícil de ser realizada. Além disso, bancos de dados normalizados além do necessário podem ter desempenho ruim e/ou complexidade excessiva.*


# O que são anomalias ? 

*A principal finalidade do processo de normalização é eliminar as anomalias de inserção, atualização e exclusão. A anomalia ocorre quando não há forma de se cadastrar alguma determinada informação sem que alguma outra informação também seja diretamente cadastrada. Por exemplo, imagine que você tenha uma tabela `funcionário` com os seguintes dados: `codigo`, `nome`, `projeto`, onde a coluna `projeto` corresponde ao nome do projeto no qual um funcionário foi alocado. E então você tem os seguintes dados:*

|       Código        |  Nome               | Projeto       |
| ------------------- | ------------------- | ------------- |
|        1            |     Pedro           |    Vendas     |
|        2            |     Maria           |   Vendas      |
|        3            |     Carlos          |  Cadastro de clientes|

*E então surgiu um projeto novo: O de emissão de notas fiscais. Como você cadastra esse novo projeto? A resposta é que não dá para cadastrar, pois para fazer isso você teria que ter algum funcionário nesse projeto - ou seja, temos uma anomalia de inserção. Se no exemplo anterior, o funcionário Carlos fosse desligado da empresa e o removermos da tabela, a informação sobre o projeto de cadastro de clientes é perdida. Isso é um efeito colateral indesejado - é a anomalia de exclusão. Se no entanto ele apenas fosse remanejado para o novo projeto de notas fiscais, nós também perderíamos a informação acerca da existência do projeto de cadastro de clientes - essa é a anomalia de alteração. O problema que origina essas anomalias é o fato de a informação do projeto estar toda dentro da tabela de funcionários, que não é o lugar dela. Se tivermos duas tabelas relacionadas (1-para-N) - funcionários e projetos - as anomalias desaparecem.*










