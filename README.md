# Projeto de Integração de Marketplaces

## Cenário 1: Integração de Marketplaces (Amazon e Mercado Livre)

### 1. Documentação e Materiais de Apoio

**1.1 - Identificação da documentação:**
		Especificação técnicas da API de integração - Documentação que descreve a integração entre o sistemas isso inclui os endpoints.
		Requisitos do projeto e regras de negócio - Definições dos objetivos do projeto e as regras que precisam ser guiadas na integração.
		
1.2 - Análise da Documentação:
		Revisar endpoints e requisitos obrigatórios - Verificar todos os endpoints fornecidos pela API para garantir que todas as informações necessãrias para o sucesso da integração.
		Analisar fluxos criticos de cada funcionalidade - Identificar quais fluxos de integração essenciais para o negócio e garantir o fluxo.
		
1.3 - Mapeamento dos Requisitos
		Criar uma matriz de rastreabilidade de requisitos e casos de teste - Este mapeamento conecta os requisitos do projeto e casos de teste.
		
1.4 - Utilização de Ferramentas:
		Jira/Trello para gerenciamento de requisitos
		Postman para teste de API
		Swagger para documentação interativa da API

### 2. Abrangência dos Testes

2.1 - Funcionalidades Testadas:
		Integração de estoque - Vericar se o sistema atualiza corretamente o estoque quando há mudanças o estoque do sistema.
		Atualização de anúcios - Testar se as alterações feitas no sistema são refletidas corretamente no marketplaces.
		Sicronização de faturamento e pedidos - Verificar se o sistema e os marketplaces trocam dados de pedidos e faturamento de forma precisa e em tempo real.
		Atualização de preço - Garantir que os preços dos produtos sejam corretamente ajustados e sicronizados entre o sistema e os marktplaces.

2.2 - Casos de Uso
		Cenários de sucesso e falha - Testar os fluxos tanto quando tudo ocorre conforme esperado (sucesso), quanto quando algum erro ocorre (falha).
		Teste de carga e desempenho - Avaliar como o sistema se comporta sob grandes volumes de dados, por exemplo, com vários pedidos simultâneos ou grandes quantidades de produtos sendo atualizados ao mesmo tempo.
		Testes de segurança e autenticação - Validar se a API está segura e se as autenticações estão funcionando corretamente para proteger os dados sensíveis.

2.3 - Priorização dos Testes
		Impacto no negócio - testes que impactam diretamente nas operações do negócio, como sicronização de pedidos e faturamento, devem ser priorizados.
		Riscos potenciais - Testar funcionalidades críticas que, se falharem, podem causar grandes problemas (Ex: atualização de estoque ou de preços).
		Falhas na integração - Avaliar como o sistema se comporta quando a integração falha, para garantir que o erro seja tratado corretamente.
		
### 3. Execução dos Testes

3.1 - Ambiente de Teste
		Ambiente de homologação com acesso à API - O ambiente de teste é onde todos os teste serão executados, geralmente um ambiente isolado para garantir que a produção não seja afetada. 
		
3.2 - Dados de Teste
		Dados fictícios de produtos, pedidos e preços - Usar dados de teste criados especificamente para verificar as funcionalidas, como dados de produtos, pedidos simulados e preços fictícios.
		
3.3 - Ferramentas de Automação
		Postman para realizar testes de API
		JMeter para testes de carga
		Selenium para testes funcionais
		
3.4 - Registro de resultdos
		Ferramentas de Gerenciamento de testes (TestRail, Zephyr, etc) - Usadas para documentar os resultados dos testes realizados, permintindo rastrear o status de cada teste e os erros encontrados.

## Cenário 2: Integração com Bling

### 1. Documentação e Materiais de Apoio

1.1 - Identificação da documentação:
		Especificação técnicas da API de integração
		Requisitos do projeto e regras de negócio
		
1.2 - Mapeamento dos Requisitos
		Criar uma matriz de rastreabilidade
		
1.3 - Utilização de Ferramentas:
		Jira/Trello para gerenciamento de requisitos
		Postman para teste de API
		Swagger para documentação interativa da API
		

### 2. Abrangência dos Testes

2.1 - Funcionalidades Testadas:
		Sicronização de produtos
		Atualização de estoque
		Processamento de pedidos
		Geração de relatórios

2.2 - Priorização dos Testes
		Impacto no negócio
		Riscos potenciais
		Falhas na integração
		
### 3. Execução dos Testes

3.1 - Dados de Teste
		Diferentes variações de produtos.
		
3.2 - Ferramentas de Automação
		Postman para realizar testes de API
		Selenium ou Cypress para testes funcionais
		
3.3 - Registro de resultdos
		Ferramentas de Gerenciamento de testes (TestRail, Zephyr, etc)

## Cenário 3:  Erro de Atualização de Estoque no Mercado Livre

### 3.1 - Passos para análise
		Verificar os logs da API para confirmação de envio da informação de estoque
		Testar envio manual de atualização de estoque para validar o comportamento esperado
		Hipóteses para a falha:
			API não está enviando a informação correta
			Delay no processamento do ML
			Erro de configuração do sistema
		Solicitar documentação do ML para verificar regras de atualização de estoque

## Cenário 4: Validações de Dados Cadastrais

### Casos de Teste: Validações seram realizadas de acordo com a documentação oficial ou regra de negócio.


  ### Testes para Nome Completo
  CT_001: Nome completo válido
    Dado que o usuário preencheu o campo "Nome completo" com "João da Silva"
    Quando o sistema valida o nome
    Então o sistema deve aceitar o nome "João da Silva"

  CT_002: Nome com caracteres inválidos
    Dado que o usuário preencheu o campo "Nome completo" com "João123"
    Quando o sistema valida o nome
    Então o sistema deve exibir a mensagem "Nome inválido. Apenas letras são permitidas."
	
  CT_003: Nome vazio
    Dado que o usuário não preencheu o campo "nome"
    Quando o sistema validar o nome
    Então o sistema deve exibir a mensagem "O campo nome é obrigatório."

  ### Testes para E-mail
  CT_004: E-mail válido
    Dado que o usuário preencheu o campo "E-mail" com "joao.silva@gmail.com"
    Quando o sistema valida o e-mail
    Então o sistema deve aceitar o e-mail "joao.silva@gmail.com"

  CT_005: E-mail inválido
    Dado que o usuário preencheu o campo "E-mail" com "joao.silva.com"
    Quando o sistema valida o e-mail
    Então o sistema deve exibir a mensagem "E-mail inválido. O formato deve ser nome@dominio.com."

  CT_006: E-mail vazio
    Dado que o usuário não preencheu o campo "E-mail"
    Quando o sistema valida o e-mail
    Então o sistema deve exibir a mensagem "O campo E-mail é obrigatório."

  ### Testes para Número de Telefone
  CT_007: Número de telefone válido
    Dado que o usuário preencheu o campo "Número de telefone" com "(11) 91234-5678"
    Quando o sistema valida o telefone
    Então o sistema deve aceitar o número de telefone "(11) 91234-5678"

  CT_008: Número de telefone inválido
    Dado que o usuário preencheu o campo "Número de telefone" com "(11) 912345678"
    Quando o sistema valida o telefone
    Então o sistema deve exibir a mensagem "Número de telefone inválido. O formato correto é (XX) XXXXX-XXXX."

  CT_009: Número de telefone vazio
    Dado que o usuário não preencheu o campo "Número de telefone"
    Quando o sistema valida o telefone
    Então o sistema deve exibir a mensagem "O campo Número de telefone é obrigatório."

  ### Testes para Data de Nascimento
  CT_010: Data de nascimento válida
    Dado que o usuário preencheu o campo "Data de nascimento" com "01/01/1990"
    Quando o sistema valida a data de nascimento
    Então o sistema deve aceitar a data "01/01/1990"

  CT_011: Formato de data inválido
    Dado que o usuário preencheu o campo "Data de nascimento" com "1990-01-01"
    Quando o sistema valida a data de nascimento
    Então o sistema deve exibir a mensagem "Formato de data inválido. Utilize DD/MM/AAAA."

  CT_012: Data de nascimento vazia
    Dado que o usuário não preencheu o campo "Data de nascimento"
    Quando o sistema valida a data de nascimento
    Então o sistema deve exibir a mensagem "O campo Data de nascimento é obrigatório."

  ### Testes para Endereço
  CT_013: Endereço completo válido
    Dado que o usuário preencheu o campo "Rua" com "Avenida Paulista", "Cidade" com "São Paulo", "Estado" com "SP", e "CEP" com "01310-000"
    Quando o sistema valida o endereço
    Então o sistema deve aceitar o endereço completo

  CT_014: Rua com caracteres inválidos
    Dado que o usuário preencheu o campo "Rua" com "Rua @123"
    Quando o sistema valida o endereço
    Então o sistema deve exibir a mensagem "Rua inválida. Somente caracteres alfanuméricos são permitidos."

  CT_015: CEP inválido
    Dado que o usuário preencheu o campo "CEP" com "1234-567"
    Quando o sistema valida o CEP
    Então o sistema deve exibir a mensagem "CEP inválido. O formato correto é XXXXX-XXX."

  CT_016: Estado inexistente
    Dado que o usuário preencheu o campo "Estado" com "ZZ"
    Quando o sistema valida o estado
    Então o sistema deve exibir a mensagem "Estado inválido."

  CT_017: Endereço vazio
    Dado que o usuário não preencheu os campos "Rua", "Cidade", "Estado" e "CEP"
    Quando o sistema valida o endereço
    Então o sistema deve exibir a mensagem "O campo Endereço é obrigatório."
