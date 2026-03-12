# Sistema de Gerenciamento de Leilões 

Este projeto consiste em uma aplicação Java Desktop (Swing) integrada a um banco de dados MySQL para a gestão de rotinas de uma casa de leilões. O sistema permite o cadastro de produtos, controle de inventário e gestão de vendas.

## Funcionalidades

O sistema foi desenvolvido seguindo as práticas de versionamento (Git/GitHub) e está dividido em:

* **Cadastro de Produtos:** Registro de novos itens com nome, valor e status inicial "A Venda".

* **Listagem de Inventário:** Visualização de todos os produtos cadastrados no banco de dados.

* **Gestão de Vendas:**
    * Funcionalidade para alterar o status de um produto para "Vendido" através do ID.
    * Tela exclusiva para consulta de histórico de itens vendidos.

* **Integração com Banco de Dados:** Persistência de dados utilizando JDBC e MySQL.

## Tecnologias Utilizadas

* **Linguagem:** Java (JDK 17+)
* **Interface Gráfica:** Java Swing
* **Banco de Dados:** MySQL 8.0
* **Driver de Conexão:** MySQL Connector/J
* **Controle de Versão:** Git & GitHub

## Estrutura do Projeto (DAO/DTO)

A arquitetura do projeto segue o padrão de camadas para organização do código:
* `conectaDAO`: Responsável pela configuração e estabelecimento da conexão com o MySQL.
* `ProdutosDAO`: Contém a lógica de persistência (Insert, Select, Update).
* `ProdutosDTO`: Objeto de transferência de dados representando a entidade Produto.
* `VIEWs`: Classes responsáveis pela interface gráfica e interação com o usuário.

## Como executar o projeto

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/liviahugentobler/leilao-sistema.git](https://github.com/liviahugentobler/leilao-sistema.git)
    ```
2.  Importe o banco de dados `uc11` localizado na pasta do projeto para o seu MySQL.
3.  Certifique-se de ajustar as credenciais (usuário e senha) no arquivo `conectaDAO.java`.
4.  Execute a classe `cadastroVIEW.java` como a tela principal.

---
Desenvolvido por **Lívia Hugentobler** como parte da Unidade Curricular de Versionamento e Manutenção de Software.