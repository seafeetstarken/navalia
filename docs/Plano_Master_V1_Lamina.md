# Dossiê Master V2 (Enterprise) — LÂMINA SaaS
Nós não construímos apenas um software de agendamento. Construímos o motor financeiro e operacional que impulsiona o faturamento das maiores barbearias do mundo.

---

## 1. A Origem e Validação Laboratorial
A tese da LÂMINA foi forjada com sangue e suor na **Alces Barbearia**, nosso laboratório fundado em 2019.
*   **Outubro 2019:** Fundação (Fusca Vermelho).
*   **Julho 2020:** Primeiro App Próprio e Validação do mercado de nicho.
*   **Setembro 2023:** Validação do Alces Club (Recorrência via cartão/PIX).

### A Diretoria
*   **Gabriel Nascimento (Founder & Business Ops):** +7 anos de mercado. Fundador da Alces.
*   **Leonardo Pickler (Tech Founder & CTO):** +16 anos Sênior/Staff Engineer (.NET, Flutter). Ex-CTO Nortech. Especialista em IA e arquiteturas escaláveis.
*   **Juan Minni (Growth & Product Lead):** +12 anos de marketing, performance e UX.

---

## 2. LÂMINA Pay: O Motor Fintech
Um SaaS puro limita a receita. A LÂMINA rompe essa bolha posicionando-se como **Sub-Adquirente (Fintech)** via API White Label do Banco Asaas.

*   **Onboarding Frictionless:** O cliente digita apenas o CNPJ. A LÂMINA Pay cria a conta bancária dele em background. Zero configuração técnica com chaves de API.
*   **Receita Infinita (Take Rate):** Se o Asaas cobra R$ 0,99 por PIX, a LÂMINA Pay cobra R$ 1,99. Retemos R$ 1,00 de lucro limpo por cada corte agendado via App.
*   **Split Automático:** Cliente paga R$ 100 via LÂMINA Pay. Nossa API injeta a regra: R$ 50 vai para a conta bancária do barbeiro, R$ 50 para o dono da barbearia. Fim do fechamento de caixa manual.

---

## 3. Fábrica de Apps (CI/CD Whitelabel)
*   **Pipeline Fastlane + GitHub Actions:** O dono faz upload do logo e escolhe as cores. Um webhook dispara uma rotina em um servidor Cloud (Mac M1) que injeta o `tenant_id`, compila o app, assina os certificados (Apple/Google) e envia direto para aprovação nas lojas. 100% autônomo.

---

## 4. Cérebro LÂMINA IA (O Módulo Premium)
Não usamos "árvore de decisão". Usamos LLMs com **RAG (Retrieval-Augmented Generation)**.
*   **Conhecimento Profundo (Vector DB):** A IA é treinada com os preços e horários de cada barbearia.
*   **Handoff Silencioso:** Se a IA não atingir 95% de confiança de que entendeu o cliente, ela pausa o agente e envia uma notificação no Web Admin: "O Humano precisa assumir". 

---

## 5. A Matriz de Permissões RLS (Supabase)
Isolamos dados com Row Level Security (PostgreSQL) usando o `tenant_id`.
*   **Super Admin LÂMINA:** Visão de todas as barbearias, faturamento das taxas LÂMINA Pay.
*   **Owner (Dono):** Acesso financeiro total da *sua* rede de barbearias, liberação de folha.
*   **Manager (Gerente):** Abertura de PDV, caixa diário, resolução do Handoff da IA. Sem acesso a lucro geral ou split.
*   **Barber (Barbeiro):** Acesso restrito: sua própria agenda, métricas de comissão diária e encaixes para seus clientes.

---

## 6. A Matemática da Gamificação
A LÂMINA controla a inflação das recompensas:
*   **Burn Mechanism (Expiração):** XP e Coins vencem a cada 90 dias.
*   **Lock-in de Custo:** Atingir o nível Ouro exige consumo equivalente a 20 cortes, liberando um brinde de margem líquida pequena (ex: Pomada de R$ 15).

---

## 7. Go-To-Market & Pricing
Foco implacável em **Barbearias Tier 1 e Tier 2** (Mais de 3 cadeiras e faturamento > R$ 50k).

| Plano | Custo Mensal | Setup Inicial | Entregáveis |
| :--- | :--- | :--- | :--- |
| **Essencial** | R$ 197 / mês | R$ 2.500 | Web Admin + App nas Lojas + Gamificação Base |
| **Pro** | R$ 347 / mês | R$ 4.000 | Essencial + LÂMINA Pay Automático + Clube de Assinatura |
| **Plus (IA)** | R$ 597+ / mês | R$ 6.000 | Pro + Atendente LÂMINA IA no WhatsApp + Assessor Preditivo |
