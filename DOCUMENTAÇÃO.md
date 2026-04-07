# TaskFlow — Sistema Gerenciador de Tarefas Online
### Documentação do Projeto Extensionista

---

## 1. Contextualização Extensionista

### 1.1 Organização Parceira

**Nome:** M&A Soluções Financeiras Ltda.  
**Setor:** Serviços financeiros — Crédito consignado  
**Porte:** Pequena empresa (8 colaboradores)  
**Localização:** Goiânia – GO  
**Contato:** contato@masf.com.br  

**Descrição da organização:**  
A M&A Soluções Financeiras é uma empresa especializada na captação de clientes aposentados, pensionistas e servidores públicos para oferta de empréstimos consignados, modalidade em que as parcelas são descontadas diretamente na folha de pagamento ou benefício do INSS. A empresa atua como correspondente bancário, intermediando a contratação de crédito entre os clientes e instituições financeiras parceiras.

---

### 1.2 Problema Identificado

Durante o contato com os responsáveis da M&A Soluções Financeiras, identificou-se que a equipe de consultores comerciais não dispõe de um sistema centralizado para controle das atividades de prospecção, acompanhamento de clientes e formalização de contratos.

**Situação anterior à solução:**
- Listas de leads e contatos eram mantidas em planilhas Excel individuais por consultor, sem compartilhamento em tempo real;
- O status de cada cliente no funil (prospecção, contato realizado, proposta enviada, contrato assinado) era controlado de forma manual e descentralizada;
- A coordenação não tinha visibilidade consolidada do andamento das campanhas de captação;
- Prazos de regularização de contratos junto aos bancos parceiros eram frequentemente perdidos por falta de acompanhamento.

**Impacto do problema:**
- Perda de clientes por falta de follow-up no momento certo;
- Retrabalho de consultores ao abordar leads já contatados por outro colega;
- Dificuldade de mensurar a produtividade de cada consultor;
- Atrasos no envio de documentação aos bancos parceiros, gerando perda de comissões.

---

### 1.3 Objetivos da Solução Proposta

**Objetivo Geral:**  
Desenvolver um sistema web de gerenciamento de tarefas adaptado à operação comercial da M&A Soluções Financeiras, centralizando o controle de campanhas de captação, tarefas por consultor e prazos de formalização de contratos.

**Objetivos Específicos:**
1. Implementar cadastro e autenticação de usuários com controle de acesso por consultor;
2. Permitir a criação de campanhas de captação com prazos e consultores responsáveis;
3. Oferecer um quadro Kanban para visualização do andamento de cada atividade comercial;
4. Integrar calendário para acompanhamento de prazos de contratos e retornos de clientes;
5. Disponibilizar painel de indicadores para monitoramento da produtividade da equipe.

**Público Beneficiado:**  
Consultores comerciais, coordenadores e gestores da M&A Soluções Financeiras, além dos clientes que se beneficiarão de um atendimento mais ágil e organizado.


## 2. Metodologia de Desenvolvimento e Gerência do Projeto

### 2.1 Abordagem Adotada

O projeto foi conduzido com base na metodologia ágil **Scrum adaptado**, organizado em sprints semanais. Por se tratar de um projeto individual, os papéis de Scrum Master, Product Owner e Desenvolvedor foram exercidos pelo mesmo aluno.

### 2.2 Ferramentas Utilizadas

| Ferramenta | Finalidade |
| Trello | Gerência de tarefas e sprints do projeto |
| GitHub | Versionamento do código-fonte |
| VS Code | Ambiente de desenvolvimento |
| Figma | Prototipação das telas |
| Google Meet | Reuniões com o parceiro |

**Link do quadro Trello:** *[(Clique aqui para ir para a página)](https://trello.com/invite/b/69d45e8c3811db4734980f92/ATTIde185d6adaa00c921a5de7e7e03178bb10E377A2/taskflow-ma-solucoes-financeiras)*

### 2.3 Sprints do Projeto

| Sprint | Duração | Atividades |
| Sprint 1 | Semana 1–2 | Levantamento de requisitos com a M&A, definição de escopo, wireframes |
| Sprint 2 | Semana 3–4 | Estrutura do projeto, autenticação, CRUD de projetos e tarefas |
| Sprint 3 | Semana 5–6 | Kanban com drag-and-drop, filtros por campanha |
| Sprint 4 | Semana 7–8 | Calendário, dashboard com indicadores |
| Sprint 5 | Semana 9–10 | Testes, correções, documentação e vídeo |

### 2.4 Identificação de Riscos

| Risco | Probabilidade | Impacto | Mitigação |
| Mudança de escopo pelo parceiro | Média | Alta | Documento de escopo validado na Sprint 1 |
| Dificuldade técnica com drag-and-drop | Alta | Média | Prototipação isolada antes da integração |
| Prazo insuficiente | Média | Alta | Buffer de 2 semanas no planejamento |
| Parceiro sem disponibilidade para reuniões | Baixa | Média | Comunicação por e-mail como alternativa |

---

## 3. Descrição Técnica do Sistema

### 3.1 Tecnologias Utilizadas

| Camada | Tecnologia |
| Frontend | HTML5, CSS3, JavaScript |
| Tipografia | Google Fonts (DM Sans, DM Mono) |
| Armazenamento | Estado em memória (JavaScript) |
| Versionamento | GitHub |

### 3.2 Funcionalidades Implementadas

#### 3.2.1 Autenticação de Usuários
- Tela de login com e-mail e senha;
- Tela de cadastro de novos usuários;
- Exibição do nome do usuário logado na barra lateral;
- Funcionalidade de logout.

**Credenciais demo:** `admin@masf.com.br` / `123456`

#### 3.2.2 Gerenciamento de Campanhas
- Criação de campanhas de captação com nome, descrição, datas de início/entrega e consultores;
- Cards com barra de progresso e percentual de tarefas concluídas;
- Filtro rápido por campanha.

#### 3.2.3 Gerenciamento de Tarefas
- Criação com título, campanha, responsável, prazo, status e prioridade;
- Listagem completa em tabela com filtros;
- Destaque visual em vermelho para tarefas com prazo vencido.

#### 3.2.4 Quadro Kanban
- Três colunas: A Fazer, Em Andamento e Concluído;
- Drag-and-drop entre colunas;
- Filtro por campanha.

#### 3.2.5 Dashboard
- Métricas: Total de Tarefas, Concluídas, Em Andamento, Atrasadas;
- Grid de campanhas ativas com progresso;
- Tabela de tarefas recentes.

#### 3.2.6 Calendário
- Visualização mensal com navegação;
- Prazos de tarefas exibidos nos dias correspondentes;
- Destaque para o dia atual.

---

## 4. Estrutura do Repositório

```
taskflow/
├── sistema_web.html        # Aplicação completa
├── DOCUMENTACAO.md   # Este arquivo
└── README.md         # Instruções de uso
```

---

## 5. Instruções de Uso

1. Abra `sistema_web.html` em qualquer navegador moderno;
2. Login: `admin@masf.com.br` / `123456`;
3. Explore o Dashboard, Kanban, Tarefas e Calendário;
4. Crie novas campanhas e tarefas pelos botões no canto superior direito.

---

## 6. Desafios e Perspectivas Futuras

### 6.1 Desafios Enfrentados
- Drag-and-drop nativo sem bibliotecas externas;
- Sincronização de estado entre Kanban, lista e calendário;
- Adaptação da terminologia de gerência de projetos ao contexto de crédito consignado.

### 6.2 Melhorias Futuras
- Backend com banco de dados (Node.js + PostgreSQL);
- Funil de vendas com etapas de prospecção, contato, proposta e contrato assinado;
- Consulta de margem consignável via integração com Dataprev/INSS;
- Notificações automáticas para follow-up com clientes;
- Relatórios de produtividade por consultor em PDF;
- Modo mobile para uso em campo.

---

## 7. Considerações Finais

O TaskFlow atendeu às necessidades identificadas junto à M&A Soluções Financeiras, entregando um sistema funcional que centraliza o controle das campanhas de captação de crédito consignado e resolve o problema de dispersão de informações entre os consultores.

---

*Documento elaborado para a disciplina de Projeto Integrador III-B*  
*Desenvolvido por: Lucas Almeida de Jesus Silva*  
*Instituição: PUC Goiás - ADS EAD*
