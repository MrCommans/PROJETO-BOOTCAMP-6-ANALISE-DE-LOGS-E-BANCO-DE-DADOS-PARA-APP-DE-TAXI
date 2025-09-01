# Análise de Logs e Banco de Dados do Urban Routes - Sprint 6 TripleTen

## Visão Geral

Este projeto foi desenvolvido como parte do **Sprint 6 do Bootcamp de Análise de QA da TripleTen**. O objetivo foi realizar duas tarefas principais: **análise de logs** em um servidor remoto para identificar solicitações de um endereço IP específico e erros, e **consultas SQL** em um banco de dados de corridas de táxi de Chicago para investigar problemas relatados, como disponibilidade de veículos e cálculos de coeficientes de custo. O projeto envolveu comandos Linux para manipulação de logs e consultas SQL para análise de dados, com documentação dos resultados em um modelo do Google Sheets.

## Objetivos do Projeto

- **Tarefa 1 (Logs)**: Identificar solicitações de logs provenientes de endereços IP começando com "233.201." no diretório `logs/2019/12` e listar os registros correspondentes.
- **Tarefa 2 (Logs)**: Criar um diretório para armazenar logs de 30/12/2019, separando erros 400 e 500 em arquivos distintos.
- **Tarefa 3 (Banco de Dados)**: Contar o número total de táxis disponíveis na tabela `cabs` para verificar a disponibilidade de veículos.
- **Tarefa 4 (Banco de Dados)**: Listar empresas de táxi com menos de 100 carros, usando o operador `HAVING`.
- **Tarefa 5 (Banco de Dados)**: Classificar condições climáticas em "Good" ou "Bad" (baseado em chuva ou tempestade) para o dia 05/11/2017, para verificar o cálculo do coeficiente de custo.
- **Tarefa 6 (Banco de Dados)**: Contar o número de corridas por empresa de táxi em 15 e 16/11/2017, para investigar discrepâncias nos lucros reportados.

## Metodologia

### Tarefa 1: Análise de Logs por Endereço IP
- Acesse o servidor remoto e naveguei até o diretório `logs/2019/12`.
- Usei o comando `grep` com um padrão para filtrar registros de IPs começando com "233.201.".
- Documentei o comando e os registros encontrados no modelo do Google Sheets.

### Tarefa 2: Separação de Logs por Erro
- Criei o diretório `bug1` e o subdiretório `events` no servidor remoto.
- Extraí logs de 30/12/2019 para o arquivo `main.txt` no diretório `bug1`.
- Separei os logs com erros 400 e 500 em `400.txt` e `500.txt`, respectivamente, no diretório `events`.
- Anexei os comandos utilizados e o conteúdo dos arquivos no modelo.

### Tarefa 3: Contagem de Táxis Disponíveis
- Conectei-me ao banco de dados `chicago_taxi` com o usuário `morty` e senha `smith`.
- Executei uma consulta SQL para contar o número total de registros na tabela `cabs`.
- Registrei a consulta e o resultado no modelo.

### Tarefa 4: Empresas com Menos de 100 Carros
- Executei uma consulta SQL para contar o número de carros por empresa (`company_name`) na tabela `cabs`, usando `GROUP BY` e `HAVING` para filtrar empresas com menos de 100 carros.
- Ordenei os resultados em ordem decrescente e documentei a consulta e a lista no modelo.

### Tarefa 5: Classificação de Condições Climáticas
- Criei uma consulta SQL com o operador `CASE` para classificar as condições climáticas da tabela `weather_records` em "Good" ou "Bad" (contendo "rain" ou "storm") para o período de 05/11/2017.
- Retornei os campos `ts` (data e hora) e `weather_conditions`, documentando a consulta e a tabela resultante no modelo.

### Tarefa 6: Contagem de Corridas por Empresa
- Conectei as tabelas `trips` e `cabs` para contar o número de corridas (`trips_amount`) por empresa em 15 e 16/11/2017.
- Usei `GROUP BY` e ordenei os resultados por `trips_amount` em ordem decrescente.
- Documentei a consulta e a tabela resultante no modelo.

## Ferramentas Utilizadas

- **Console Linux**: Para manipulação de logs no servidor remoto (comandos como `grep`, `mkdir`, `cat`).
- **PostgreSQL**: Para consultas SQL no banco de dados `chicago_taxi`.
- **Google Sheets**: Para documentar comandos, resultados de logs e consultas SQL.
- **Google Docs**: Para anexar o link do modelo e outros recursos.
- **Urban Routes**: Aplicativo de táxi relacionado ao banco de dados testado.

## Estrutura do Repositório

- `Análise de Logs e Banco de Dados - Urban Routes.xlsx`: Modelo preenchido com comandos, logs, consultas SQL e resultados (nomeado como "[Seu Nome], [Sobrenome], [Grupo] — 6º sprint").
- `Análise de Logs e Banco de Dados - Urban Routes.docx`: Documento com links para a planilha e outros recursos (nomeado conforme instruções).
- `README.md`: Este arquivo, descrevendo o projeto.

## Resultados

- Identifiquei e documentei solicitações de logs para IPs começando com "233.201.", fornecendo registros específicos.
- Organizei logs de erros 400 e 500 em arquivos separados, facilitando a análise de bugs.
- Contei o número total de táxis disponíveis e listei empresas com menos de 100 carros, revelando possíveis lacunas na disponibilidade.
- Classifiquei condições climáticas para verificar o cálculo do coeficiente de custo, fornecendo dados claros para os desenvolvedores.
- Calculei o número de corridas por empresa em dois dias específicos, ajudando a investigar discrepâncias de lucro.
- Contribuí para a garantia de qualidade do Urban Routes, fornecendo dados acionáveis para a equipe de desenvolvimento.

## Sobre Mim

Sou um profissional em transição de carreira para a área de Qualidade de Software, com formação no **Bootcamp de Análise de QA da TripleTen**. Minha experiência prévia em ambientes dinâmicos me proporcionou habilidades como atenção aos detalhes, organização e colaboração. Estou comprometido em aplicar meus conhecimentos em QA, especialmente em análise de logs e bancos de dados, para garantir a qualidade de produtos digitais.

## Contato

- 📍 São Paulo, Brasil
- 📧 [Insira seu e-mail]
- 🔗 [Insira seu LinkedIn]
- 💻 [Insira link do GitHub ou portfólio]

Obrigado por visitar meu repositório! 🚖