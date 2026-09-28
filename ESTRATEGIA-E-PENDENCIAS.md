# Vareiro & Haddad Advocacia: 2 LPs de conversão

Webdesigner: Paulo Jr · Solicitante: Júnior Silva

| LP | Pasta | GTM | CTA | Mensagem pré-preenchida |
|---|---|---|---|---|
| Direito Ambiental Rural | `lp-direito-ambiental-rural/` | GTM-5TTGL23T | Entenda sua situação ambiental | Olá, vi a página sobre Direito Ambiental Rural e gostaria de informações. |
| Alongamento de Dívida de Crédito Rural | `lp-divida-credito-rural/` | GTM-5SSZZ67V | Solicitar informações pelo WhatsApp | Olá, vi a página sobre dívida rural e gostaria de solicitar informações. |

Cada pasta é autossuficiente: `index.html` (HTML e CSS inline, sem dependências) e `assets/` (logo, favicon, fotos dos sócios em WebP). É só subir a pasta.

---

## 1. Estratégia e promessa central

**Ambiental.** O produtor precisa se reconhecer no problema ("isso aconteceu comigo"), não no tema "Direito Ambiental".
- Promessa: *entender o que foi determinado, qual prazo corre e o que pode ser avaliado, a partir da análise individual da autuação.*
- Tom: consequências reais (prazo, embargo mantido, cobrança, impacto na produção), sempre com "dependendo da situação" e sem alarmismo.

**Crédito rural.** A página não vende "reduzir dívida" nem "salvar patrimônio".
- Promessa: *primeiro compreender tecnicamente a operação e o estágio do problema; depois identificar quais medidas podem ser juridicamente avaliadas.*
- O desejo trabalhado é clareza e previsibilidade para decidir.

**Nas duas:**
- Sem promessa de resultado, sem comparação com outros escritórios e sem "consulta gratuita".
- Um único objetivo de conversão: WhatsApp.

## 2. Estrutura (seção por seção)

Versão enxuta, com 7 seções, porque o público rural prefere comunicação direta e rápida.

| # | Ambiental | Crédito rural |
|---|---|---|
| 1 | Hero com 100vh, foto dos sócios, logo, headline do anúncio, card "Atuamos em casos envolvendo" e CTA | Idem |
| 2 | Situações: 3 cards temáticos com checklist e CTA | Situações: 3 cards com as frases do produtor e CTA |
| 3 | Como funciona a atuação (6 etapas, seção escura) | Primeiro → Depois (seção escura) |
| 4 | Documentos para separar e CTA | Documentos para ter em mãos e CTA |
| 5 | Por que não deixar para depois (4 cards de alerta) e CTA | Dívidas podem evoluir de estágio (4 cards de alerta) e CTA |
| 6 | FAQ com 6 perguntas | FAQ com 6 perguntas |
| 7 | Sócios e credenciais, com CTA de fechamento, e rodapé | Idem |

Seções retiradas: lista "O que você precisa entender", "Diferenciais objetivos" e "O que é analisado" (só na de crédito). O FAQ caiu de 15 para as 6 objeções mais decisivas. As demais objeções do briefing ficaram cobertas pelos cards de situação e de documentos.

## 3. Copy

A copy final está nos arquivos `index.html`.
- Títulos, descrições e complementos do anúncio foram usados literalmente no hero, para manter a coerência com o anúncio.
- As objeções viraram FAQ com respostas condicionais ("depende do estágio", "pode ser analisado"), sem promessa.

## 4. Visual e hierarquia

- **Identidade:** escudo dourado (#C9A66B) sobre navy (#13223D), tirada do logo do cliente. Fundos creme (#F7F3EC) nas seções de apoio.
- **Tipografia:** Roboto nos títulos; Inter no texto, com base de 16 a 17px para leitura no celular.
- **Ritmo:** as seções alternam entre claro e escuro. A seção de consequências e a de credenciais ficam no navy, para dar peso.
- **CTAs:** 5 por página (hero, situações, documentos, consequências e fechamento), todos iguais e dourados, com ícone do WhatsApp.
- **Sem botão flutuante**, conforme o briefing, e sem header.
- **Mobile:** botões em largura total e FAQ em acordeão. Testado em 390px, sem rolagem horizontal.

## 5. Técnico, integrações e pendências

**Pronto**
- GTM instalado no `<head>` e no `<body>` (noscript), com o ID correto em cada LP.
- Links `wa.me/5565996302294` com a mensagem codificada. Funcionam mesmo com o JS desligado.
- Evento `dataLayer` a cada clique: `{event:'clique_whatsapp', lp:'…', cta_posicao:'hero|identificacao|documentos|consequencias|final'}`. No GTM, criar um acionador de Evento personalizado `clique_whatsapp` e ligar à conversão do Ads ou do GA4.
- Meta title, description e OG; favicon; imagens otimizadas (logo com 12KB, fotos entre 20 e 38KB).
- Rodapé com os nomes, as OABs e o aviso "caráter informativo, não constitui promessa de resultado".

**Pendências para o cliente validar**
1. **Credenciais dos sócios.** Foram extraídas do currículo institucional (PDF enviado) e precisam da validação final dos sócios, como o briefing pede. Marcadas com comentário `PENDÊNCIA` no HTML.
2. **Nome da marca.** O briefing e o Instagram usam "Vareiro & Haddad"; o currículo usa "Haddad & Vareiro Advocacia". A página segue "Vareiro & Haddad". Confirmar.
3. **Endereço.** O currículo traz dois endereços em Cuiabá. Usamos o do Eldorado Executive Center. Confirmar qual é o oficial.
4. **Atendimento remoto e prazos.** As FAQs "Preciso ir presencialmente?", "Outra cidade de MT?" e "Quanto tempo leva?" foram respondidas sem afirmar nada que o cliente não informou. Se o atendimento for 100% online, dá para reforçar isso nas respostas.
5. **Fotos de campo.** Resolvido: o hero de cada LP usa a foto enviada (`hero-bg.webp`, entre 76 e 111KB, com versão mobile de 35 a 50KB).
6. **Domínio e hospedagem.** O briefing diz "Não"; definir onde as LPs serão publicadas.
7. **Política de privacidade e cookies.** Com o GTM ativo, recomenda-se um link de política e LGPD no rodapé. O cliente não enviou nenhum.
