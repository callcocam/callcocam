# Olá, eu sou o Claudio Campos 👋

Desenvolvedor full-stack em **Capão da Canoa – RS**. Construo produtos SaaS do zero à produção com **Laravel, Vue 3 e Inertia.js**, desde a modelagem do domínio até o deploy sem queda na VPS.

- 🛒 Hoje dedico a maior parte do tempo ao **[Plannerate](https://plannerate.com.br)**, plataforma de planogramas e trade marketing para supermercados
- 🤝 Também criei o **[Coordena](https://coordena.space)** e o **[Contas da Congregação](https://contas.coordena.space)**
- 🌐 Portfólio: **[sigasmart.com.br](https://sigasmart.com.br/portfolio)**

---

## 🛒 Plannerate: planogramas e trade marketing para o varejo

**[plannerate.com.br](https://plannerate.com.br)** · SaaS multi-tenant · Desenvolvedor principal (mais de 2.200 commits desde abr/2026)

Redes de supermercado e cooperativas usam o Plannerate para decidir **o que vai em cada gôndola, onde e em que quantidade**, conferir se a loja executou e vender espaço promocional para a indústria. Ele liga o ERP do varejista ao analista de categoria, ao repositor na loja e ao fornecedor.

### O que ele faz

| Módulo | O que resolve |
|---|---|
| **Editor de planogramas** | Gôndolas em canvas (seções → prateleiras → segmentos → camadas) com arrastar e soltar, desfazer/refazer, auto-save e presença em tempo real de quem está editando |
| **Geração automática** | Monta a gôndola a partir das vendas: curva ABC ponderada (quantidade, valor e margem), estoque-alvo por nível de serviço, Análise de Papel, matriz BCG, blocos por categoria e adjacência |
| **Templates + IA** | Motor por templates com slots e subtemplates, e "Sugerir com IA", que aprende com as gerações anteriores de cada loja |
| **Execução em loja** | Kanban por gôndola, mapa da planta da loja em tempo real e apps PWA: o repositor lê o QR Code e envia fotos, e o executor aprova pelo celular |
| **Ruptura** | Estoque projetado, pré-ruptura, ruptura de espaço, venda perdida estimada, conferência na loja e e-mail diário por loja |
| **Trade marketing / JBP** | Venda de pontas, ilhas e displays como inventário, contratos com aprovação por etapas, portal do fornecedor e Planejamento de Trade (JBP) com diagnóstico escrito por IA |
| **Catálogo por EAN** | Enriquecimento de cadastro em 14 estágios: fontes externas com pesos, busca por similaridade e vetorial (pgvector), voto ponderado, revisão humana e aprendizado com as correções |
| **Integrações ERP** | Integração por configuração (blueprint por API mais config por cliente), monitor de saúde e documentação pública com "Testar minha API" |

### Alguns resultados

- 📈 **Ocupação de gôndola de 39,7% para 87%** na geração automática, sem prateleiras vazias. Testei um empacotador exato (knapsack por programação dinâmica): ele ganhava só ~1 ponto percentual sobre o guloso. A medição mostrou que a perda real estava na divisão de espaço entre categorias, e foi isso que corrigi.
- 🚀 **Deploy sem queda**: migrei de `artisan serve` para FrankenPHP. Durante a troca de versão, 291 requisições, zero erros (antes eram ~30 s de falhas).
- ✅ **Mais de 3.400 testes** (Pest) e testes de frontend (Vitest).
- 🧩 Domínio separado em pacotes Laravel próprios: planogramas, enriquecimento de produtos por EAN e trade marketing. O pacote de trade roda em dois sistemas diferentes.

**Stack:** Laravel 13 · PHP 8.4 · Vue 3 · Inertia v3 · TypeScript · Tailwind 4 · Konva · PostgreSQL 17 + pgvector · Redis/Horizon · Reverb · Laravel AI · Spatie Multitenancy · FrankenPHP · Docker · Traefik · Cloudflare · GitHub Actions

---

## 🤝 Coordena: logística de voluntários

**[coordena.space](https://coordena.space)** · Projeto próprio

Escalas de voluntários para eventos, com um gerador automático que equilibra a carga e reforça os horários de pico. Também cuida da permuta de oradores entre congregações, de reuniões com pauta e ata colaborativa e de caravanas (inscrição com os dados exigidos pela ANTT, veículos, roteiro e manifesto). Quem participa não precisa de conta: tudo chega pelo **WhatsApp Cloud API**, com conversas modeladas como máquinas de estado.

## 📒 Contas da Congregação: contabilidade sem papel

**[contas.coordena.space](https://contas.coordena.space)** · Projeto próprio

Recibos, folha de contas, relatório mensal, autorizações de pagamento e auditoria seguindo as instruções oficiais. Cada regra cita o parágrafo em que se baseia. Documentos assinados são congelados com **hash SHA-256**, triggers do PostgreSQL impedem alterar registros que são só de acréscimo, e há separação de funções, passkeys e LGPD. São mais de 1.100 testes.

## 🏬 GoMark: plataforma para varejo

**[gomark.com.br](https://gomark.com.br)** · Participei do início do desenvolvimento (hoje mantido por outro responsável)

Liga ao ERP do varejista o cadastro de produtos com portal do fornecedor, as campanhas e ofertas, o trade marketing e a TV de loja com preços ao vivo.

---

## 📦 Open source

- **[laravel-whatsapp-cloud](https://github.com/callcocam/laravel-whatsapp-cloud)**: WhatsApp Cloud API (Meta) para Laravel, com templates, webhook e driver sandbox. Extraído do Coordena.
- **[inertia-rbac](https://github.com/callcocam/inertia-rbac)**: papéis e permissões para apps Laravel + Inertia.
- **[laravel-vps-scaffold](https://github.com/callcocam/laravel-vps-scaffold)**: provisionamento de VPS e deploy com Docker, Traefik e rollback.

## 🛠️ Ferramentas do dia a dia

`PHP` `Laravel` `Vue 3` `Inertia.js` `TypeScript` `Tailwind CSS` `Livewire` `Alpine.js` `PostgreSQL` `MySQL` `Redis` `Docker` `FrankenPHP` `GitHub Actions` `Pest` `Laravel AI`

📫 Fale comigo: [sigasmart.com.br](https://sigasmart.com.br)
