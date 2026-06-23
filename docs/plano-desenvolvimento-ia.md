# 🚀 Plano de Desenvolvimento — Console LÂMINA IA

## 1. Objetivo do Console LÂMINA IA
Desenvolver a interface do cockpit administrativo do **LÂMINA IA** focada em barbearias, utilizando o Design System Obsidian Steel (`lamina-tokens.css`). 

O console integrará as principais funcionalidades de inteligência artificial de atendimento e gestão (mapeadas a partir do projeto de referência interna):

*   **Inbox / Central de Atendimento:** Monitoramento em tempo real do assistente de IA conversando com clientes no WhatsApp.
*   **Base de Conhecimento RAG:** Upload e edição das regras do salão, FAQ e lista de serviços/preços para treinamento da IA.
*   **Configurações do Agente IA:** Regras de negócio da agenda, restrições e tom de voz (persona).
*   **Assessor Preditivo / Insights:** Dicas de negócios e detecção de ociosidades geradas de forma autônoma pela IA.

---

## 2. Abas do Protótipo (SPA em Vanilla JS)

### 2.1 Dashboard de Inteligência
*   **Métricas em Tempo Real:** Conversas ativas, taxa de resolução por IA (sem necessidade de atendente humano), tempo médio de resposta e economia estimada de horas.
*   **Módulo Preditivo (Assessor IA):** Alertas de no-show recorrente ou lacunas na agenda com sugestão de disparo automático de promoções.

### 2.2 Central de Conversas (Inbox WhatsApp)
*   **Simulador de Atendimento:** Um painel ativo de chat onde simula-se a interação do cliente marcando um corte de cabelo e barba pelo WhatsApp.
*   **Handoff Humano:** Botão de controle de status da IA ("Pausar LÂMINA IA" / "Retomar") permitindo que o barbeiro assuma a conversa.
*   **Score IA:** Exibição gráfica do nível de intenção de compra / agendamento do cliente (ex: `Score IA: 98% (Agendamento Próximo)`).

### 2.3 Base de Conhecimento (Treinamento)
*   **Regras Operacionais:** Onde o salão dita o comportamento da IA (ex: tolerância a atrasos, prazo de cancelamento).
*   **Catálogo de Serviços:** Sincronização dos serviços com preços e durações para que a IA possa agendar corretamente.
*   **Status de Indexação:** Badges mostrando se as regras já foram assimiladas pela IA (`✓ Indexado` ou `⌛ Processando`).

### 2.4 Persona & Configuração
*   **Ajuste de Tom:** Slider ou botões selecionando a persona da IA (ex: "Descontraído e Moderno" vs "Premium e Clássico").
*   **Restrições de Agenda:** Intervalo mínimo entre agendamentos, limite diário, etc.

---

## 3. Cronograma de Desenvolvimento (Fase 2)
1.  **Fundação e Layout:** Sidebar responsiva, Topbar de status e Router SPA básico.
2.  **Desenvolvimento do Dashboard:** Widgets de estatísticas e gráficos de fluxo.
3.  **Desenvolvimento do Inbox Simulator:** Lógica de script de conversa interativa para demonstração do agendamento autônomo.
4.  **Desenvolvimento da Base de Conhecimento:** Formulários de cadastro de regras e visualizador de arquivos.
5.  **Ajustes Finais e Validação:** Auditoria visual com o Design System Obsidian Steel.
