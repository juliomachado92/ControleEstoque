# ControleEstoque
Documentação Teste prático 
Autor: Júlio Miranda Machado


Motivação: 
	Deseja-se criar um aplicação, voltada  para um teste prático realizado pela DTI digital no intuito de testar conhecimentos.
	
Objetivo:
	Criar uma aplicação que permita um estoquista cadastrar/alterar e excluir produtos no meu sistema de estoque. 
O produto deve conter as seguintes informações
Nome do produto
Quantidade de itens do produto
Valor unitário do produto

Requisitos 
O sistema deve permitir cadastrar produto 
O sistema deve permitir excluir produto
O sistema deve permitir alterar produto
O sistema deve permitir listar produtos
O sistema deve conter uma tela de listagem 
O sistema deve conter uma tela de inclusão

Ferramentas utilizadas : 
Visual studio 2017
GitHub
 
Definições arquiteturais
	
Para elaboração dessa situação, será criado um projeto no Visual Studio 2017, do tipo ASP.NET Core MVC Web Application , que é um padrão Model-View-Controller que separa as regras e lógicas de negócio da apresentação , que nos permite ter maior controle da aplicação e ter uma estrutura de arquivos melhor.
	Esse projeto também utiliza ferramentas como o Bootstrap, para manipulação de estilos de páginas(CSS) e jquery para manipulação de elementos por javascript.
	Será utilizado o Entity Framework Core(EF Core) , que é a versão mais leve, extensível e multiplataforma do Entity Framework. Considerando a evolução posterior do sistema com isso devemos utilizar recursos leve e fácil portabilidade , com isso a escolha do EF Core pois o mesmo é mais leve e muito similar ao EF6.
	Será utilizado uma ferramenta do entity framework que é o Migrations, que nos auxiliará no controle de versão do banco de dados.
	O banco de dados escolhido foi o SQLite, devido a não ter que instalar sistemas próprios , como no caso do SQL server, ser fácil de integração com o sistema do VS17.

Pacotes 
Microsoft.EntityFrameworkCore.Sqlite
Microsoft.EntityFrameworkCore.Sqlite.Design
Microsoft.EnityFrameworkCore.Tools

Casos de usos

Caso de uso UC1
O estoquista poderá visualizar produtos.
Atores
Estoquista .
Pré-condições
Estoquista ter acessado sistema.
Descrição Detalhada
- Fluxo Principal
O caso de uso é iniciado quando o estoquista acessa o Sistema .
O Sistema apresenta a interface de listagem de produtos.
O caso de uso é encerrado.
Pós-condições
O estoquista cadastrar, editar ou excluir produto.

Caso de uso UC2
O estoquista poderá cadastrar produto.
Atores
Estoquista .
Pré-condições
Estoquista ter acessado sistema.
Descrição Detalhada
- Fluxo Principal
O caso de uso é iniciado quando o estoquista acessa o Sistema e seleciona a opção novo produto 
O Sistema apresenta a interface de cadastro de produto.
O estoquista preenche o nome, a quantidade e o valor do produto
O estoquista escolher salvar.
O Sistema grava no banco de dados o novo produto e retorna para listagem de produtos.
 O caso de uso é encerrado.
Pós-condições
Sistema retorna para a listagem de produtos.


Caso de uso UC3
O estoquista poderá cadastrar excluir.
Atores
Estoquista .
Pré-condições
Estoquista ter acessado sistema.
Descrição Detalhada
- Fluxo Principal
O caso de uso é iniciado quando o estoquista acessa o Sistema e seleciona a opção excluir 
O Sistema apresenta as informações do produto .
O estoquista válida e opta por excluir.
O Sistema exclui registro do banco de dados e retorna para listagem de produtos.
 O caso de uso é encerrado.
Pós-condições
Sistema retorna para a listagem de produtos.

Caso de uso UC4
O estoquista poderá alterar produto.
Atores
Estoquista .
Pré-condições
Estoquista ter acessado sistema.
Descrição Detalhada
- Fluxo Principal
O caso de uso é iniciado quando o estoquista acessa o Sistema e seleciona a opção alterar 
O Sistema apresenta a interface de alteração de produto.
O estoquista editar as informações nome, quantidade e/ou valor do produto
O estoquista escolher salvar.
O Sistema grava no banco de dados e retorna para listagem de produtos.
 O caso de uso é encerrado.
Pós-condições
Sistema retorna para a listagem de produtos.

