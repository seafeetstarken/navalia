# 🚀 Tasks — LÂMINA IA (Tecnologia Dedicada para Barbearias)

## Fase 1 — Fundação (Concluída) ✅
- [x] Definir nome da marca → **LÂMINA** ⟋
- [x] Validar disponibilidade de domínio e handles sociais
- [x] Criar identidade visual (paleta Obsidian Steel, tipografia, tokens)
- [x] Criar pasta do novo projeto com estrutura base (`lamina/`)
- [x] Documentar brand guidelines (Design System v1.0 com showcase interativo)

## Fase 2 — Console LÂMINA IA (Protótipo do Produto) ⟋
- [/] Atualizar a navegação e estrutura do app `lamina` para o formato de Console SaaS
  - [ ] Implementar Sidebar de navegação premium (Estilo Obsidian Steel)
  - [ ] Criar container principal SPA dinâmico (chaveamento de abas sem reload)
- [ ] Desenvolver Aba 1: Dashboard / Visão Geral da IA
  - [ ] Cards de métricas operacionais (Taxa de Agendamento IA, Conversas, Tempo Economizado)
  - [ ] Gráficos estilizados de volume de atendimento por hora/canal
- [ ] Desenvolver Aba 2: Central de Atendimento (Inbox)
  - [ ] Layout em 3 colunas (Conversas > Conversa Ativa com Chat Simulator > Detalhes do Lead)
  - [ ] Chat Simulator dinâmico mostrando a LÂMINA IA negociando e agendando com o cliente no WhatsApp
  - [ ] Botão "Intervir / Pausar IA" e exibição do status ativo da IA
  - [ ] Detalhes do lead com IA Score (0-100) e resumo das preferências do cliente gerado por IA
- [ ] Desenvolver Aba 3: Base de Conhecimento RAG
  - [ ] Área de upload e listagem de regras (FAQ, Regras do Salão, Valores dos Serviços)
  - [ ] Tabela/Lista de itens indexados com badges `✓ Indexado` e `Processando`
- [ ] Desenvolver Aba 4: Configurações do Agente IA
  - [ ] Ajuste do tom de voz do robô (Descontraído vs Formal)
  - [ ] Regras de restrição de agenda (intervalos, no-shows, etc.)
  - [ ] Integração com WhatsApp (QR Code de conexão simulado)

## Fase 3 — Landing Page (Postergada por enquanto) 🌐
- [ ] Desenvolver landing page de captação (quando solicitado pelo usuário)

## Fase 4 — Integração Supabase / Real IA (Futuro) 🤖
- [ ] Mapear as tabelas do Supabase para multi-tenant
- [ ] Integrar as Edge Functions de agendamento automático com a LLM
