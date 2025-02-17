# Projeto de Integração de Marketplaces

## Cenário 1: Integração de Marketplaces (Amazon e Mercado Livre)

### 1. Documentação e Materiais de Apoio

**1.1 - Identificação da documentação:**</br>
		Especificação técnicas da API de integração - Documentação que descreve a integração entre o sistemas isso inclui os endpoints.</br>
		Requisitos do projeto e regras de negócio - Definições dos objetivos do projeto e as regras que precisam ser guiadas na integração.</br>
		
**1.2 - Análise da Documentação:**</br>
		Revisar endpoints e requisitos obrigatórios - Verificar todos os endpoints fornecidos pela API para garantir que todas as informações necessãrias para o sucesso da integração.</br>
		Analisar fluxos criticos de cada funcionalidade - Identificar quais fluxos de integração essenciais para o negócio e garantir o fluxo.</br>
		
**1.3 - Mapeamento dos Requisitos:**</br>
		Criar uma matriz de rastreabilidade de requisitos e casos de teste - Este mapeamento conecta os requisitos do projeto e casos de teste.</br>
		
**1.4 - Utilização de Ferramentas:**</br>
		Jira/Trello para gerenciamento de requisitos</br>
		Postman para teste de API</br>
		Swagger para documentação interativa da API</br>

### 2. Abrangência dos Testes</br>

**2.1 - Funcionalidades Testadas:**</br>
		Integração de estoque - Vericar se o sistema atualiza corretamente o estoque quando há mudanças o estoque do sistema.</br>
		Atualização de anúcios - Testar se as alterações feitas no sistema são refletidas corretamente no marketplaces.</br>
		Sicronização de faturamento e pedidos - Verificar se o sistema e os marketplaces trocam dados de pedidos e faturamento de forma precisa e em tempo real.</br>
		Atualização de preço - Garantir que os preços dos produtos sejam corretamente ajustados e sicronizados entre o sistema e os marktplaces.</br>

**2.2 - Casos de Uso:**</br>
		Cenários de sucesso e falha - Testar os fluxos tanto quando tudo ocorre conforme esperado (sucesso), quanto quando algum erro ocorre (falha).</br>
		Teste de carga e desempenho - Avaliar como o sistema se comporta sob grandes volumes de dados, por exemplo, com vários pedidos simultâneos ou grandes quantidades de produtos sendo atualizados ao mesmo tempo.</br>
		Testes de segurança e autenticação - Validar se a API está segura e se as autenticações estão funcionando corretamente para proteger os dados sensíveis.</br>

**2.3 - Priorização dos Testes:**</br>
		Impacto no negócio - testes que impactam diretamente nas operações do negócio, como sicronização de pedidos e faturamento, devem ser priorizados.</br>
		Riscos potenciais - Testar funcionalidades críticas que, se falharem, podem causar grandes problemas (Ex: atualização de estoque ou de preços).</br>
		Falhas na integração - Avaliar como o sistema se comporta quando a integração falha, para garantir que o erro seja tratado corretamente.</br>
		
### 3. Execução dos Testes</br>

**3.1 - Ambiente de Teste:**</br>
		Ambiente de homologação com acesso à API - O ambiente de teste é onde todos os teste serão executados, geralmente um ambiente isolado para garantir que a produção não seja afetada.</br>
		
**3.2 - Dados de Teste:**</br>
		Dados fictícios de produtos, pedidos e preços - Usar dados de teste criados especificamente para verificar as funcionalidas, como dados de produtos, pedidos simulados e preços fictícios.</br>
		
**3.3 - Ferramentas de Automação:**</br>
		Postman para realizar testes de API</br>
		JMeter para testes de carga</br>
		Selenium para testes funcionais</br>
		
**3.4 - Registro de resultdos:**</br>
		Ferramentas de Gerenciamento de testes (TestRail, Zephyr, etc) - Usadas para documentar os resultados dos testes realizados, permintindo rastrear o status de cada teste e os erros encontrados.</br>

## Cenário 2: Integração com Bling</br>

### 1. Documentação e Materiais de Apoio</br>

**1.1 - Identificação da documentação:**</br>
		Especificação técnicas da API de integração - Documentação que descreve a integração entre o sistemas isso inclui os endpoints.</br>
		Requisitos do projeto e regras de negócio - Definições dos objetivos do projeto e as regras que precisam ser guiadas na integração.</br>
		
**1.2 - Mapeamento dos Requisitos:**</br>
		Criar uma matriz de rastreabilidade e de requisitos e casos de teste - Este mapeamento conecta os requisitos do projeto e casos de teste.</br></br>
		
**1.3 - Utilização de Ferramentas:**</br>
		Jira/Trello para gerenciamento de requisitos</br>
		Postman para teste de API</br>
		Swagger para documentação interativa da API</br>
		

### 2. Abrangência dos Testes</br>

**2.1 - Funcionalidades Testadas:**</br>
		Sicronização de produtos - Garantir que o sistema esteja integrando corretamente os dados de produtos entre a plataforma Bling e o sistema.</br>
		Atualização de estoque - Verificar se as alterações no estoque são refletidas corretamente.</br>
		Processamento de pedidos - Testar se os pedidos feitos no Bling são corretamente processados e integrados ao sistema.</br>
		Geração de relatórios - Validar a criação de relatórios com base nas integrações realizadas.</br>

**2.2 - Priorização dos Testes:**</br>
		Impacto no negócio - O processo de priorização continua com base no impacto para o negócio e riscos associados.</br>
		Riscos potenciais - Testar funcionalidades críticas que, se falharem, podem causar grandes problemas.</br>
		Falhas na integração - Avaliar como o sistema se comporta quando a integração falha, para garantir que o erro seja tratado corretamente.</br>
		
### 3. Execução dos Testes</br>


**3.1 - Dados de Teste:**</br>
		Aqui, o foco é testar diferentes variações de produtos, como categorias, preços e estoques, para garantir a integração.</br>
		
**3.2 - Ferramentas de Automação:**</br>
		Postman para realizar testes de API</br>
		Selenium ou Cypress para testes funcionais</br>
		
**3.3 - Registro de resultdos:**</br>
		Ferramentas de Gerenciamento de testes (TestRail, Zephyr, etc)</br>

## Cenário 3:  Erro de Atualização de Estoque no Mercado Livre</br>

### 1. Passos para análise do Problema
**1.1 - Consultar a documentação da API do Mercado Livre:</br>**
		Verificar como o status "Pausado (sem estoque)" deve ser atualizado.</br>
		Identificar os campos necessários na requisição.</br>
  
**1.2 - Analisar o comportamento atual:</br>**
		Quando o estoque acaba, o Magazord está enviando a atualização corretamente?</br>
		A atualização manual funciona, mas a automática não?</br>
  
**1.3 - Testar a atualização via API manualmente:**</br>
		Enviar uma requisição com "available_quantity": 0.</br>
		Verificar se o anúncio muda para "Pausado (sem estoque)".</br>

**1.4 - Checar os logs do Magazord:**</br>  
		Verificar se há registros de envio de estoque igual a zero.</br>
		Comparar os dados enviados pelo Magazord com a atualização manual.</br>
  
### 2. Possíveis Causas do Erro
	O Magazord não está enviando a atualização de estoque corretamente.
	O Mercado Livre pode exigir parâmetros adicionais para mudar o status.
	O Magazord pode estar pausando o anúncio antes de zerar o estoque.
	Pode haver um delay na API do Mercado Livre.
	O cliente pode ter configurações que impedem a mudança automática.

### 3. Próximos Passos
	Testar uma atualização manual via API e verificar se o status muda corretamente.
	Comparar o payload do Magazord com o da atualização manual.
	Ajustar a integração se necessário, garantindo que o estoque seja atualizado corretamente antes de pausar o anúncio.
  
## Cenário 4: Validações de Dados Cadastrais</br>

**Casos de Teste: Validações seram realizadas de acordo com a documentação oficial ou regra de negócio.**</br>


  **CT_001: Nome completo válido**</br>
    Dado que o usuário preencheu o campo "Nome completo" com "João da Silva"</br>
    Quando o sistema valida o nome</br>
    Então o sistema deve aceitar o nome "João da Silva"</br>

  **CT_002: Nome com caracteres inválidos**</br>
    Dado que o usuário preencheu o campo "Nome completo" com "João123"</br>
    Quando o sistema valida o nome</br>
    Então o sistema deve exibir a mensagem "Nome inválido. Apenas letras são permitidas."</br>
	
  **CT_003: Nome vazio**</br>
    Dado que o usuário não preencheu o campo "nome"</br>
    Quando o sistema validar o nome</br>
    Então o sistema deve exibir a mensagem "O campo nome é obrigatório."</br>

  **CT_004: E-mail válido**</br>
    Dado que o usuário preencheu o campo "E-mail" com "joao.silva@gmail.com"</br>
    Quando o sistema valida o e-mail</br>
    Então o sistema deve aceitar o e-mail "joao.silva@gmail.com"</br>

  **CT_005: E-mail inválido**</br>
    Dado que o usuário preencheu o campo "E-mail" com "joao.silva.com"</br>
    Quando o sistema valida o e-mail</br>
    Então o sistema deve exibir a mensagem "E-mail inválido. O formato deve ser nome@dominio.com."</br>

  **CT_006: E-mail vazio**</br>
    Dado que o usuário não preencheu o campo "E-mail"</br>
    Quando o sistema valida o e-mail</br>
    Então o sistema deve exibir a mensagem "O campo E-mail é obrigatório."</br>
    
  **CT_007: Número de telefone válido**</br>
    Dado que o usuário preencheu o campo "Número de telefone" com "(11) 91234-5678"</br>
    Quando o sistema valida o telefone</br>
    Então o sistema deve aceitar o número de telefone "(11) 91234-5678"</br>

  **CT_008: Número de telefone inválido**</br>
    Dado que o usuário preencheu o campo "Número de telefone" com "(11) 912345678"</br>
    Quando o sistema valida o telefone</br>
    Então o sistema deve exibir a mensagem "Número de telefone inválido. O formato correto é (XX) XXXXX-XXXX."</br>

  **CT_009: Número de telefone vazio**</br>
    Dado que o usuário não preencheu o campo "Número de telefone"</br>
    Quando o sistema valida o telefone</br>
    Então o sistema deve exibir a mensagem "O campo Número de telefone é obrigatório."</br>

  **CT_010: Data de nascimento válida**</br>
    Dado que o usuário preencheu o campo "Data de nascimento" com "01/01/1990"</br>
    Quando o sistema valida a data de nascimento</br>
    Então o sistema deve aceitar a data "01/01/1990"</br>

  **CT_011: Formato de data inválido**</br>
    Dado que o usuário preencheu o campo "Data de nascimento" com "1990-01-01"</br>
    Quando o sistema valida a data de nascimento</br>
    Então o sistema deve exibir a mensagem "Formato de data inválido. Utilize DD/MM/AAAA."</br>

  **CT_012: Data de nascimento vazia**</br>
    Dado que o usuário não preencheu o campo "Data de nascimento"</br>
    Quando o sistema valida a data de nascimento</br>
    Então o sistema deve exibir a mensagem "O campo Data de nascimento é obrigatório."</br>

  **CT_013: Endereço completo válido**</br>
    Dado que o usuário preencheu o campo "Rua" com "Avenida Paulista", "Cidade" com "São Paulo", "Estado" com "SP", e "CEP" com "01310-000"</br>
    Quando o sistema valida o endereço</br>
    Então o sistema deve aceitar o endereço completo</br>

  **CT_014: Rua com caracteres inválidos**</br>
    Dado que o usuário preencheu o campo "Rua" com "Rua @123"</br>
    Quando o sistema valida o endereço</br>
    Então o sistema deve exibir a mensagem "Rua inválida. Somente caracteres alfanuméricos são permitidos."</br>

  **CT_015: CEP inválido**</br>
    Dado que o usuário preencheu o campo "CEP" com "1234-567"</br>
    Quando o sistema valida o CEP</br>
    Então o sistema deve exibir a mensagem "CEP inválido. O formato correto é XXXXX-XXX."</br>

  **CT_016: Estado inexistente**</br>
    Dado que o usuário preencheu o campo "Estado" com "ZZ"</br>
    Quando o sistema valida o estado</br>
    Então o sistema deve exibir a mensagem "Estado inválido."</br>

  **CT_017: Endereço vazio**</br>
    Dado que o usuário não preencheu os campos "Rua", "Cidade", "Estado" e "CEP"</br>
    Quando o sistema valida o endereço</br>
    Então o sistema deve exibir a mensagem "O campo Endereço é obrigatório."</br>
