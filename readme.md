# Importador de bases de dados notion

Esta é a versão inicial do importador

## Instalação

```
npm install
```

## Configuração
Criar uma API Key do NOTION e definir as permissões de acesso para as bases de dados origem e destino

Para fazer isso use este link: https://developers.notion.com/docs/create-a-notion-integration


Clonar e instalar o projeto com

```
npm install
```

na pasta do projeto criar um arquivo .env contendo
NOTION_API_KEY=<SUA API KEY DO NOTION>


## Execução
Existem 2 metodos de execução: simulação e execução final

### SIMULACAO
```
npm start <SOURCE_DATABASE_ID> <DESTINATION_DATABASE_ID>
```

### EXECUCAO
```
npm start <SOURCE_DATABASE_ID> <DESTINATION_DATABASE_ID> true
```

A execução adicionará os valores na tabela destino

### RESTRIÇÕES

O notion não permite a criação via API de colunas da tabela do database. Portanto o banco de dados de destino já deve possuir as mesmas colunas do banco de dados de origem. Para fazer isso basta utilizar a opção "Duplicate/Duplicate Without Content" do banco de dados de origem.

### ROADMAP
Proximo passo é definir as queries para fazer a migração e bora

