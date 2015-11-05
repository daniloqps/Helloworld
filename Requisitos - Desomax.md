#Análise de Requisitos
###Desomax

##Objetivo

Sistema web para lançamento de pedidos

##Tecnologia

PHP+BOOTSTRAP+MYSQL

##Telas

1. Vendedor [ Usuario, Senha, Nome, Email, Ativo ]
2. Produtos [ Codigo, Descrição, Preço Unitário ]
3. Cliente [ Codigo, Nome ]
4. Vendas [Codigo, FK-CódigoCliente DataEmissao, Condição de Pagamento, Valor Total ]
5. VendasItem [CodigoVenda, FK-CodigoProduto, Quantidade, Preço Unitario ]
6. Configuração [Ip, CaminhoDB, Usuario, Senha, EmailInterno, Importar Produtos, Importar Clientes]
7. Relatório de Vendas [Campos de Vendas e VendasItem]

##Visão do Vendedor
- Login do vendedor
- Pedidos [Visualizar, Cadastrar, Imprimir, Cancelar, Enviar por Email]

##Visão do Administrador
- Login do administrador
- Pedidos [Visualizar de todos vendedores, Cancelar, Excluir, Imprimir]
- Vendedores [Visualizar, Cadastrar, Excluir, Bloquear, Zerar Senha]
- Configuração [ Config. de Infra, Importação de Cadastros ]

##Funcionalidades
- Enviar por email: o pedido deverá ser encaminhado por email (Config->EmailInterno e Vendedor->Email) com 2 anexos : PDF e XML.
- WebService de Cadastros: deverá ser disponibilizado um webservice para que o sistema ERP envie um lote de cadastros de produtos e clientes. 
- WebService de Integração: deverá ser disponibilizado um webservice para que o sistema ERP capture os ultimos pedidos gerados, mandando retorno de OK, para dizer que foi integrado ao sistema.

##Layout
Simples e intuitivo (usuários leigos), sem complicações. Campos grandes, bem formatados, com dicas de preenchimento. Menu lateral, Barra superior para Logotipo da empresa.

##Teste - Pontos Críticos

- Teste de interface: Lançamentos de Pedidos (validações dos campos), Teste de Login(Sessão)
- Teste de persistência: Lançamentos de Pedidos (Inserção, Alteração, Confirmação, Cancelamento)
- Teste de Integração: Envio de Email com os pedidos, WebService de Lote de Produtos e Clientes, WebService de Pedidos

  Os testes de WebService são opcionais do cliente e envolverá responsável pelo E.R.P, orçamento de testes deverá ter custos compartilhados.

##Observações

- O envio por email é para que o sistema esteja funcional antes que o ERP desenvolva a integração
- Os campos de produtos e clientes ainda serão todos especificados conforme layout de telas anexados. As tabelas e campos ainda serão encaminhados
- Os arquivos serão alocados no servidor de hospedagem do cliente com LINUX, MYSQL, PHP, com liberação para implantação e manutenção.

