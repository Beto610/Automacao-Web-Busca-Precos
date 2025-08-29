# Automação Web para Monitoramento de Preços (Google Shopping + Buscapé)

## Descrição:

Este projeto implementa uma automação em Python com Selenium para buscar preços de produtos em dois sites de comparação: Google Shopping e Buscapé.

O fluxo funciona assim:

### Leitura da planilha (buscas.xlsx)

Contém os parâmetros da busca: produto, termos banidos, preço mínimo e máximo.

### Busca automática no Google Shopping e Buscapé

Selenium abre cada site e executa a pesquisa.

Filtra resultados de acordo com:

Nome do produto (sem termos banidos).

Faixa de preço desejada.

Extrai nome, preço e link das ofertas.

### Organização dos resultados

Todas as ofertas encontradas são consolidadas em um DataFrame do pandas.

Exportação para um arquivo Excel (Ofertas.xlsx).

### Envio automático por e-mail (Outlook)

Caso existam ofertas, o script gera uma tabela em HTML com os resultados.

Envia o e-mail automaticamente pelo Outlook (via pywin32).

## Principais bibliotecas utilizadas:

Selenium → automação da navegação web.

Pandas → manipulação e exportação dos dados.

OpenPyXL → escrita do arquivo Excel.

PyWin32 → envio de e-mails pelo Outlook.
