# SolicitaGov

Protótipo front-end de um marketplace governamental de compras públicas, desenvolvido em **HTML e CSS puro**. Este projeto implementa **a visão do fornecedor**: a interface usada por empresas que cadastram produtos/serviços e acompanham suas licitações, pedidos e contratos com órgãos públicos. A visão do comprador (órgão público) não faz parte deste projeto.

## Sobre o projeto

O SolicitaGov conecta fornecedores a oportunidades de venda para órgãos públicos em todo o Brasil. Pelo painel do fornecedor é possível gerenciar produtos cadastrados, acompanhar licitações abertas, pedidos recebidos, contratos firmados e relatórios de desempenho.

## Estrutura de arquivos

```
solicita_gov/
├── index.html   
├── style.css    
├── principal.html    
├── principal.css
├── produtos.html  
├── produtos.css
├── cadastrar.html 
├── cadastrar.css
├── licitacoes.html 
├── licitacoes.css
├── pedidos.html 
├── pedidos.css
├── contrato.html 
├── contrato.css
├── relatorio.html
├── relatorio.css
└── img/                               
```

Cada página interna (exceto `index.html`) compartilha o mesmo `header` (logo, busca e seletor de cidade) e o mesmo `aside` de navegação lateral, mas cada uma tem seu próprio arquivo CSS.

## Páginas

### `index.html` — Login
Tela de entrada com apresentação da plataforma ("Segurança garantida", "Processos transparentes", "Fornecedores verificados") e formulário de e-mail/senha. O envio redireciona para `principal.html`.

### `principal.html` — Dashboard
Página inicial após o login, com:
- Banner com mapa e chamada "Conectando fornecedores a oportunidades em todo Brasil"
- Cards de desempenho (avaliação média, propostas vencedoras, faturamento atual)
- Estatísticas gerais da plataforma (órgãos públicos, fornecedores, produtos, licitações ativas)

### `produtos.html` — Meus produtos
Gestão dos produtos/serviços cadastrados pelo fornecedor:
- Cards resumo (total de produtos, ativos, inativos, visualizações no mês)
- Filtros por categoria e status
- Tabela de produtos com preço, estoque, status (Ativo/Inativo) e ações (editar, visualizar, mais opções)
- Botão para ir ao cadastro de novo produto (`cadastrar.html`)
- Paginação

### `cadastrar.html` — Cadastrar novo produto
Formulário de cadastro, dividido em abas (só "Dados gerais" implementada; Especificações, Imagens e Documentos aparecem como placeholders):
- Nome do produto, Categoria
- Descrição (textarea)
- Unidade de medida (Unidade, Caixa, Pacote, Kg, Litro, Metro, Metro², Hora, Mês, Outro)
- Preço unitário, Estoque disponível, Status

### `licitacoes.html` — Licitações abertas
Lista de licitações disponíveis para o fornecedor participar:
- Filtro por categoria (Todos, Materiais, Serviços, Obras, Tecnologia, Outros)
- Tabela com Objeto, Órgão, Data, Investimento e Status

### `pedidos.html` — Pedidos
Acompanhamento dos pedidos recebidos dos órgãos públicos:
- Filtro por status (Todos, Em andamento, Concluídos, Cancelados)
- Tabela com número do pedido, órgão, data, valor e status (com pílulas coloridas)

### `contrato.html` — Contratos
Gestão dos contratos firmados com os órgãos públicos:
- Filtro por status (Todos, Vigentes, Encerrados, Aguardando assinatura)
- Tabela com número do contrato, órgão, vigência e valor

### `relatorio.html` — Relatórios
Métricas de desempenho do fornecedor na plataforma:
- Filtro por período e botão de exportação
- Cards (licitações participadas, propostas enviadas, contratos firmados, faturamento)
- Gráficos de faturamento (imagens estáticas)

## Tecnologias

- HTML5
- CSS3 (Flexbox)
- Fontes Google: [Inter](https://fonts.google.com/specimen/Inter) e [Poppins](https://fonts.google.com/specimen/Poppins)

Não há dependências de build, framework ou backend — é um projeto estático.

## Como visualizar

Basta abrir `index.html` diretamente no navegador. A navegação entre as páginas funciona por links relativos (`principal.html`, `produtos.html` etc.).

