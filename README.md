# PlanoTeste
Plano de Teste Padrão


PLANO DE TESTE – Módulo de Usuário – Sprint 01
1. Identificação do Plano de Teste
Nome: Plano de Teste – Módulo de Usuário

ID: PT-001-USUARIO

Projeto: Sistema de Gerenciamento XYZ

Versão: 1.0

Data: 22/07/2025

Responsável: QA Specialist – ChatGPT

2. Itens a serem testados
Cadastro de usuário

Edição de usuário

Exclusão de usuário

Autenticação (login)

Visualização de perfil

Listagem de usuários

Controle de permissões

3. Itens fora do escopo
Integração com terceiros (Ex: login social)

Recuperação de senha (Sprint futura)

4. Abordagem de Teste
Utilizaremos uma abordagem funcional, exploratória e automatizada com foco em:

Validação de regras de negócio

Testes de segurança e autenticação

Verificação de UI/UX (acessibilidade, responsividade)

Testes de integração REST API

Validação de banco de dados (consistência e persistência)

5. Critérios de Aceitação / Saída
100% dos testes críticos devem passar

95% dos testes funcionais devem ser aprovados

Zero bugs bloqueadores ou críticos

Aprovação do PO

6. Critérios de Suspensão e Retomada
Suspensão: Erros bloqueadores em endpoints principais

Retomada: Correção validada pelo time de desenvolvimento

7. Entregas de Teste
Casos de teste

Evidências de execução

Relatório de bugs

Relatório de cobertura

Checklists de regressão

8. Ambiente de Teste
Frontend: Angular (última versão)

Backend: FastAPI + PostgreSQL

Ambientes: Local, Homologação (Staging)

9. Responsabilidades
Função	Responsável
Planejamento de Teste	QA Engineer
Execução Manual	QA / Devs
Execução Automatizada	QA Automation
Homologação final	PO

10. Riscos
Alterações tardias nos requisitos

Ambientes instáveis

Integrações externas instáveis

🔄 CICLO DE TESTE – Sprint 01
Etapas por Sprint
Etapa	Responsável	Duração estimada
Planejamento de Teste	QA	1 dia
Criação de Casos	QA	2 dias
Execução Manual	QA / Devs	3 dias
Testes Automatizados	QA Automation	3 dias
Registro de Evidências	QA	Contínuo
Homologação	PO	1 dia

🧪 CENÁRIOS DE TESTE (Sprint 01 – Módulo Usuário)
🔹1. Cadastro de Usuário
ID	Descrição	Tipo	Criticidade
US-01	Cadastrar usuário com dados válidos	Funcional	Alta
US-02	Cadastrar com e-mail já existente	Funcional	Alta
US-03	Cadastrar com senha fraca	Validação	Média
US-04	Cadastrar sem campos obrigatórios	Funcional	Alta

🔹2. Login
ID	Descrição	Tipo	Criticidade
US-05	Login com credenciais válidas	Funcional	Alta
US-06	Login com senha incorreta	Segurança	Alta
US-07	Login com usuário inexistente	Funcional	Alta
US-08	Token JWT deve ser retornado	API	Alta

🔹3. Edição de Usuário
ID	Descrição	Tipo	Criticidade
US-09	Editar nome e e-mail	Funcional	Alta
US-10	Editar sem autenticação	Segurança	Alta
US-11	Editar com dados inválidos	Validação	Média

🔹4. Listagem e Visualização
ID	Descrição	Tipo	Criticidade
US-12	Listar todos os usuários (admin)	Funcional	Alta
US-13	Ver dados de um usuário	Funcional	Alta
US-14	Paginação e busca	Usabilidade	Média

🔹5. Permissões e Segurança
ID	Descrição	Tipo	Criticidade
US-15	Verificar que usuários comuns não veem admins	Segurança	Alta
US-16	Teste de injeção de SQL	Segurança	Alta
US-17	Teste de acesso direto por rota	Segurança	Alta

📚 TIPOS DE TESTE NECESSÁRIOS
🔸 BACKEND
Tipo de Teste	Descrição
Teste Unitário	Testar funções isoladas como hash de senha, geração de token, etc.
Teste de Integração	Testar endpoints REST integrados com banco
Teste de API (Postman / Pytest)	Validação de todos os endpoints, com entradas válidas e inválidas
Teste de Segurança	Testar JWT, CSRF, SQLi, validação de permissões
Teste de Performance (mínimo)	Carga básica nos endpoints críticos (ex: login, cadastro)
Teste de Regressão	Após cada mudança no backend

🔸 FRONTEND
Tipo de Teste	Descrição
Teste Funcional (manual)	Usar Cypress ou testes manuais para garantir que a UI funciona
Teste de UI/UX	Responsividade, acessibilidade, consistência visual
Teste de Componentes	Testar se inputs, botões e formulários funcionam corretamente
Teste de Integração	Testar se frontend consome corretamente o backend
Teste de Regressão	Automatizar navegação e formulários após cada release
Teste de Navegação	Garantir que rotas e menus levam às telas certas

Se desejar, posso gerar os casos de teste em formato Excel ou JSON, ou criar um template para TestRail, Zephyr, Xray ou Notion.

Você gostaria agora que eu:

Detalhasse os casos de teste (com steps e dados)?

Criasse os testes automatizados para backend (ex: Pytest)?

Criasse um checklist de testes manuais com marcação de status?

Me avise para a próxima entrega do Sprint 01 ou para preparar já o Sprint 02.
