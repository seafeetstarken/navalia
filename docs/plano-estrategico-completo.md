# 🚀 Plano Estratégico Master — Ecossistema LÂMINA

## 1. Visão Executiva e Sociedade

A **LÂMINA** nasce de uma dor real do mercado e de uma união estratégica de expertises. Não somos apenas mais uma empresa de software de tecnologia genérica; somos uma plataforma feita **por barbeiros, para barbeiros**.

*   **Os Founders:** 
    *   **Gabriel Nascimento** (Founder & Business Operations): Empreendedor do setor de beleza masculina, fundador da rede Alces Barbearia (traz a inteligência operacional, validação real de mercado e foco na experiência do cliente final).
    *   **Leonardo Pickler** (Tech Founder & CTO): Sênior/Staff Engineer (+16 anos exp, .NET/C#, Next.js, Flutter, IA e Web3/Blockchain, ex-CTO Nortech App).
    *   **Juan Minni** (Co-Founder, Growth & Product Lead): CEO da Starken Tecnologia (+12 anos exp em marketing digital, performance, e-commerce e branding. R$ 3M+ gerados para negócios locais, especialista em growth e estruturação comercial).
*   **O Piloto (Proof of Concept):** A **Alces Barbearia** atua como nosso laboratório vivo e caso de sucesso principal. Tudo que vendemos foi testado e validado no mundo real na Alces.
*   **Posicionamento de Mercado:** *"Seu próprio App, sua própria Marca"*. Elevamos a barbearia comum a um ecossistema digital premium. Não somos um marketplace que mistura concorrência; entregamos **Tecnologia Dedicada**.

---

## 2. O Ecossistema do Produto (A Oferta)

A plataforma será composta por 4 grandes pilares interconectados, cobrindo 100% da operação de uma barbearia moderna.

### Pilar 1: App Nativo do Cliente (White-label Customizado)
O carro-chefe das vendas. Uma experiência premium focada em retenção e recorrência, entregue com a identidade visual de cada barbearia cliente.

*   **Agendamento Inteligente:** Seleção de unidade (para redes), profissional, data e horário com verificação de conflitos em tempo real.
*   **Assinaturas e Gateway Próprio:** Contratação de pacotes (ex: Clube da Barba) nativa no app.
    *   Integração transparente com **Gateway Próprio da Barbearia** (Asaas/Stripe).
    *   Gestão de cobranças automáticas: **PIX Recorrente** e **Cartão de Crédito**.
*   **Gamificação Avançada (Motor de Fidelidade):**
    *   *Níveis de EXP:* O cliente sobe de nível (ex: Bronze, Prata, Ouro, VIP) ao consumir no app.
    *   *Economia de Moedas:* Cashback virtual em compras que podem ser trocadas por serviços ou bebidas (ex: 500 Coins = 1 Pomada).
    *   *Conquistas (Badges):* Troféus por ações específicas (agendar 5x seguidas, horário de pico, etc.).
    *   *Ranking (Leaderboard):* Estímulo à competição saudável entre clientes frequentes.

### Pilar 2: Área In-App do Profissional (O Barbeiro)
O barbeiro não precisa acessar um computador. Ele resolve a vida dele pelo próprio aplicativo.

*   **Agenda Pessoal:** Visão clara de seus próximos cortes e horários livres.
*   **Agendamento Direto:** Capacidade do barbeiro agendar encaixes diretamente para seus clientes fidelizados pelo app.
*   **Acompanhamento de Metas:** Gráficos de comissão ganhos no dia/mês.

### Pilar 3: O "Web Admin Completasso" (Gestão Central)
O cérebro da operação (já construído e validado no piloto), permitindo ao dono da barbearia gerenciar tudo em telas focadas em dados e conversão.

*   **Dashboard & Relatórios:** Faturamento do dia, taxa de retorno, gráficos comparativos e ticket médio.
*   **Caixa (PDV):** Abertura/fechamento, registro de vendas de produtos/serviços e múltiplas formas de pagamento.
*   **Gestão Financeira & Comissões:** Cálculo automático de comissionamento de barbeiros baseado em serviços prestados, regras e metas.
*   **CRM (Clientes):** Histórico de atendimentos, preferências de corte, taxas de cancelamento.
*   **Catálogo & Estoque:** Controle de produtos e alerta de estoque baixo.

### Pilar 4: O LÂMINA IA (Módulo Premium / Plus)
A inteligência artificial não é o foco principal da venda padrão, mas sim o **upsell matador**. É um recurso avançado para planos maiores.

*   **Agendamento via WhatsApp Automático:** A IA atua como recepcionista e agenda diretamente no sistema, dialogando de forma natural com o cliente.
*   **Assessor Digital:** Disparo preditivo de mensagens (ex: reengajar cliente que não aparece há 30 dias).
*   **Base de Conhecimento:** Respostas automáticas a FAQs (preços, horários de funcionamento, localização).

---

## 3. Modelo de Negócio e Precificação

Venderemos uma **Transformação Digital**. O modelo é B2B SaaS (Software as a Service) com Setup inicial.

| Plano | Setup (Implementação) | Mensalidade | O que Inclui |
| :--- | :--- | :--- | :--- |
| **Essencial** | R$ 2.500 | R$ 197 / mês | Web Admin Completo + App Nativo Customizado + Gamificação Base |
| **Pro** | R$ 4.000 | R$ 347 / mês | Essencial + Clube de Assinaturas (Recorrência) + Metas/Relatórios Avançados |
| **Plus (IA)** | R$ 6.000+ | R$ 597+ / mês | Pro + LÂMINA IA (Atendimento WhatsApp automatizado) + Assessor Preditivo |

> *(Valores de referência baseados na pesquisa de mercado. O Setup justifica a publicação das lojas Apple/Google e configuração das contas de gateway e servidores).*

---

## 4. O Caminho de Execução Técnica (Próximos Passos)

Como vamos transformar o projeto Alces (mono-cliente) no produto LÂMINA (SaaS multi-tenant):

### Fase 1: Arquitetura SaaS (Refatoração do Backend)
- **Multi-tenant Supabase:** Ajustar as RLS (Row Level Security) e tabelas (adicionar `tenant_id` ou `workspace_id`) para que múltiplas barbearias possam usar a mesma estrutura de dados sem cruzar informações.
- **Parametrização de Gateway:** Transformar a integração Asaas para suportar múltiplas contas de recebedores (split de pagamentos ou contas independentes).

### Fase 2: O Motor de Gamificação (White-label)
- Abstrair o "Caminho do Alce" para um motor genérico (ex: "Programa de Fidelidade") onde o dono da barbearia (pelo Admin Web) cadastra seus próprios Níveis, Moedas e Recompensas.

### Fase 3: App Template "Whitelabel"
- Refatorar o Flutter App da Alces para consumir um arquivo de configuração (JSON / Firebase Remote Config) que altera Cores, Logo, e Fontes dependendo do `tenant_id` logado.
