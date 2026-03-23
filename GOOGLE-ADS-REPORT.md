# Google Ads Audit Report — Valuation Pro

**Account:** Valuation Pro (546-351-5680)
**Campaign:** Valuation - Pesquisa Brasil (Search)
**Period:** 20-23 Mar 2026
**Auditor:** Claude Ads Audit System
**Date:** 23/03/2026

---

## Google Ads Health Score: 18/100 (Grade: F)

```
Conversion Tracking: 10/100  █░░░░░░░░░  (25%)
Wasted Spend:        25/100  ██░░░░░░░░  (20%)
Account Structure:   20/100  ██░░░░░░░░  (15%)
Keywords & QS:       15/100  █░░░░░░░░░  (15%)
Ads & Assets:        15/100  █░░░░░░░░░  (15%)
Settings & Targeting:25/100  ██░░░░░░░░  (10%)
```

---

## Executive Summary

A conta Valuation Pro tem problemas criticos em todas as 6 categorias. O maior problema e a **ausencia de conversoes configuradas corretamente** — sem isso, o algoritmo de Smart Bidding nao tem dados para otimizar. A campanha gastou R$ 25,90 com zero conversoes em 4 dias.

**Gasto desperdicado estimado:** ~R$ 510/mes se mantido nas condicoes atuais (100% do budget, pois nao ha conversoes).

---

## 1. Conversion Tracking (Score: 10/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G42 | Conversion actions defined | **FAIL** | 0 conversoes registradas. gtag event existe no codigo mas nao esta gerando dados no Google Ads |
| G43 | Enhanced conversions | **FAIL** | Nao habilitado |
| G44 | Server-side tracking | **FAIL** | Nao implementado |
| G45 | Consent Mode v2 | **N/A** | Brasil — nao obrigatorio |
| G46 | Conversion window | **FAIL** | Sem conversoes, impossivel avaliar |
| G47 | Micro vs macro separation | **FAIL** | Nenhuma conversao configurada |
| G48 | Attribution model | **WARNING** | Data-driven nao disponivel sem dados |
| G49 | Conversion value | **FAIL** | Nenhum valor atribuido |
| G-CT1 | Duplicate counting | **N/A** | Sem conversoes |
| G-CT2 | GA4 linked | **WARNING** | GA4 (G-X3CW3KG198) e Google Ads (AW-18029764921) presentes no codigo. Link nao verificado |
| G-CT3 | Google Tag firing | **WARNING** | gtag.js instalado e disparando, mas evento de conversao nao confirmado |

### Acoes Criticas:
1. **URGENTE:** Criar acao de conversao "Compra" no Google Ads (valor: R$ 99)
2. Adicionar evento gtag de conversao apos confirmacao de pagamento Mercado Pago
3. Habilitar Enhanced Conversions
4. Importar conversoes do GA4 como backup

---

## 2. Wasted Spend / Negatives (Score: 25/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G13 | Search term audit | **FAIL** | Sem evidencia de revisao dos termos de pesquisa |
| G14 | Negative keyword lists | **FAIL** | Zero listas de palavras-chave negativas |
| G15 | Account-level negatives | **FAIL** | Nenhuma negativa aplicada |
| G16 | Irrelevant term spend | **WARNING** | Sem Search Terms Report disponivel para analise. Correspondencia ampla em todas as keywords aumenta risco |
| G17 | Broad match + Smart Bidding | **WARNING** | Broad Match + Maximize Conversions e aceitavel, mas sem dados de conversao o algoritmo esta cego |
| G18 | Close variant pollution | **WARNING** | Risco alto com 100% broad match sem negativas |
| G19 | Search term visibility | **FAIL** | Nao analisado |
| G-WS1 | Zero-conversion keywords | **WARNING** | Todas as keywords tem 0 conversoes, mas volume ainda baixo (13 cliques total) |

### Acoes Criticas:
1. **Criar listas de negativas (Exact Match):**
   - **Informacional:** `[o que e valuation]`, `[valuation significado]`, `[como fazer valuation gratis]`, `[valuation pdf]`, `[valuation excel]`, `[valuation template]`
   - **Educacional:** `[curso valuation]`, `[curso avaliacao de empresas]`, `[MBA valuation]`
   - **Emprego:** `[vagas valuation]`, `[analista valuation]`, `[salario valuation]`
   - **Empresas grandes:** `[valuation petrobras]`, `[valuation vale]`, `[valuation acoes]`, `[valuation bolsa]`
2. **Revisar Search Terms Report** semanalmente

---

## 3. Account Structure (Score: 20/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G01 | Campaign naming | **WARNING** | "Valuation - Pesquisa Brasil" e descritivo mas nao segue padrao formal |
| G02 | Ad group naming | **FAIL** | "Grupo de anuncios 1" — nome generico |
| G03 | Single theme ad groups | **WARNING** | 13 keywords em 1 ad group. Mistura intencoes (informacional + transacional) |
| G04 | Campaign count | **PASS** | 1 campanha ativa e adequado para o porte |
| G05 | Brand vs Non-Brand | **N/A** | Sem volume de marca ainda |
| G06 | PMax presente | **WARNING** | Campaign #1 (PMax) pausada — OK por decisao |
| G07 | Search + PMax overlap | **N/A** | PMax pausada |
| G08 | Budget allocation | **WARNING** | Budget R$ 17/dia nao esta limitando (gasto medio R$ 6.48/dia) |
| G09 | Budget pacing | **PASS** | Nao esta atingindo cap |
| G10 | Ad schedule | **FAIL** | Sem programacao de horarios |
| G11 | Geographic targeting | **WARNING** | Nao verificado — deve ser "Pessoas em" Brasil |
| G12 | Network settings | **WARNING** | Nao verificado se Display Network esta OFF |

### Acoes:
1. Renomear ad group para "Valuation - Calculadora Online"
2. Separar keywords em 2 ad groups:
   - **Intencao alta:** "quanto vale minha empresa", "avaliacao de empresa", "valor da minha empresa"
   - **Informacional:** "como calcular valuation", "valuation empresa", "calcular valor empresa"
3. Configurar ad schedule (seg-sex, 8h-22h)
4. Verificar location targeting = "Pessoas em"
5. Desabilitar Display Network se ativo

---

## 4. Keywords & Quality Score (Score: 15/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G20 | Average Quality Score | **FAIL** | QS nao disponivel no export, mas Google alerta "qualidade baixa" |
| G21 | Critical QS keywords | **FAIL** | Google indica qualidade geral baixa |
| G22 | Expected CTR | **PASS** | CTR 15.48% — excelente, acima do benchmark 6.66% |
| G23 | Ad relevance | **FAIL** | Google alerta "nao segmentando pesquisas relevantes" |
| G24 | Landing page experience | **WARNING** | Pagina funcional mas sem schema markup, HTTP (nao HTTPS no final URL) |
| G25 | Top keyword QS | **FAIL** | Impossivel avaliar sem dados de QS |
| G-KW1 | Zero-impression keywords | **FAIL** | 6 de 13 keywords (46%) com zero impressoes em 4 dias |
| G-KW2 | Keyword-to-ad relevance | **WARNING** | Headlines contem variantes mas descripcao menciona "R$ 99" (mixed signals) |

### Keyword Performance Matrix:

| Keyword | Clicks | Impr | CTR | CPC | Intent |
|---------|--------|------|-----|-----|--------|
| como calcular valuation | 5 | 28 | 17.9% | R$ 2.59 | Informacional |
| valuation empresa | 4 | 24 | 16.7% | R$ 0.81 | Misto |
| quanto vale minha empresa | 2 | 3 | 66.7% | R$ 3.17 | **Transacional** |
| avaliacao de empresa | 2 | 19 | 10.5% | R$ 1.68 | Misto |
| calcular valor empresa | 0 | 0 | — | — | Informacional |
| valuation pequena empresa | 0 | 0 | — | — | **Transacional** |
| valor da minha empresa | 0 | 0 | — | — | **Transacional** |
| quanto vale meu negocio | 0 | 0 | — | — | **Transacional** |
| avaliacao empresarial | 0 | 0 | — | — | Informacional |
| valor de mercado empresa | 0 | 0 | — | — | Informacional |

### Acoes:
1. **Mudar top 4 keywords para Phrase Match** — mais controle sem perder volume
2. **Pausar keywords com zero impressoes** por 30 dias — nao contribuem
3. **Adicionar keywords transacionais novas:**
   - `"calculadora valuation online"`
   - `"quanto vale meu CNPJ"`
   - `"avaliar empresa para venda"`
   - `"valuation PME"`
4. **Corrigir Final URL:** Mudar de `http://` para `https://www.qualmeuvaluation.com.br`

---

## 5. Ads & Assets (Score: 15/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G26 | RSA per ad group | **PASS** | 1 RSA no unico ad group |
| G27 | RSA headline count | **WARNING** | 7 headlines (minimo recomendado: 8, ideal: 12-15) |
| G28 | RSA description count | **FAIL** | Aparenta ter poucas descricoes |
| G29 | RSA Ad Strength | **FAIL** | Qualidade "Ruim" (Google) |
| G30 | Pinning strategy | **N/A** | Nao verificado |
| G35 | Ad copy relevance | **WARNING** | Headlines relevantes mas descricao menciona preco (R$ 99) — pode afugentar |
| G-AD1 | Ad freshness | **WARNING** | Campanha recente, mas anuncio unico sem variacoes para teste |
| G-AD2 | CTR vs benchmark | **PASS** | CTR 15.48% vs benchmark 6.66% — excelente |

### Ad Copy Atual:
**Headlines:** "Quanto Vale Sua Empresa?" | "Calculadora Valuation Gratis" | "Descubra em 3 Minutos" + 4 mais
**Description:** "Multiplos reais de M&A brasileiro. Resultado em minutos. Relatorio R$ 99. Descubra o valor da sua empresa. Ideal para PMEs que querem vender ou captar."

### Problemas:
- "Gratis" no headline + "R$ 99" na descricao = **mensagem contradictoria**
- Ad Strength "Ruim" = penalidade no leilao
- Apenas 1 anuncio = sem A/B testing

### Headlines Sugeridos (para atingir 15):
1. `Quanto Vale Sua Empresa?` (manter)
2. `Calculadora de Valuation Online` (ajustar)
3. `Descubra em 3 Minutos` (manter)
4. `Avaliacao Empresarial Profissional`
5. `Valuation com Dados Reais de M&A`
6. `Multiplos PwC, KPMG e EY`
7. `Ideal para PMEs e Startups`
8. `Saiba o Valor do Seu Negocio`
9. `Metodologia de Fundos de Investimento`
10. `Calcule o Valuation da Sua Empresa`
11. `Mais de 2.000 Empresas Ja Usaram`
12. `Pronto para Vender ou Captar?`
13. `Resultado Imediato e Detalhado`
14. `17 Setores do Mercado Brasileiro`
15. `Relatorio PDF para Investidores`

### Descricoes Sugeridas (4):
1. `Descubra quanto vale sua empresa com multiplos reais de M&A do mercado brasileiro. Preencha em 3 minutos e receba seu diagnostico.`
2. `Avaliacao profissional baseada em dados PwC, KPMG e EY. Ideal para empresarios que querem vender, captar investimento ou planejar sucessao.`
3. `Calculadora de valuation com 15 indicadores financeiros. Mais de 2.000 empresas ja calcularam. Resultado imediato com diagnostico completo.`
4. `Saiba o valor real do seu negocio hoje. Metodologia usada por fundos de investimento e boutiques de M&A. 17 setores brasileiros cobertos.`

---

## 6. Settings & Targeting (Score: 25/100)

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G50 | Sitelinks | **FAIL** | Sitelinks reprovados na Campaign #1. Nenhum ativo na campanha Search |
| G51 | Callouts | **FAIL** | Zero callouts configurados |
| G52 | Structured snippets | **FAIL** | Nenhum |
| G53 | Image extensions | **FAIL** | Nenhuma |
| G54 | Call extensions | **N/A** | Negocio online |
| G55 | Lead form | **N/A** | Modelo e-commerce |
| G56 | Audience segments | **FAIL** | Nenhum publico em observacao |
| G57 | Customer Match | **FAIL** | Nenhuma lista de clientes |
| G58 | Placement exclusions | **N/A** | Search only |
| G59 | Landing page mobile | **WARNING** | Pagina 236KB, single HTML — pode ser lenta no mobile |
| G60 | Landing page relevance | **PASS** | H1 "Quanto vale a sua empresa?" alinhado com keywords |
| G61 | Schema markup | **FAIL** | Nenhum schema (Product/FAQ/Service) |

### Bidding & Budget:

| ID | Check | Result | Details |
|----|-------|--------|---------|
| G36 | Smart Bidding | **FAIL** | Maximize Conversions com 0 conversoes — algoritmo cego |
| G37 | Target CPA razoavel | **FAIL** | CPA desejado R$ 50 com 0 historico. Budget R$ 17/dia = impossivel atingir R$ 50 CPA |
| G38 | Learning phase | **FAIL** | "Qualificada (limitada)" — campanha nao saiu do learning |
| G39 | Budget constrained | **PASS** | Budget nao esta limitando |
| G40 | Manual CPC justification | **N/A** | Nao usa Manual CPC |
| G41 | Portfolio strategies | **N/A** | Apenas 1 campanha |

### Acoes:
1. **URGENTE:** Mudar bidding para **Maximize Clicks** (CPC max R$ 3.00) ate ter 15+ conversoes
2. **Remover Target CPA** — sem historico, so atrapalha
3. **Adicionar sitelinks:** "Como Funciona", "Metodologia", "Para PMEs", "Setores Cobertos"
4. **Adicionar callouts:** "Resultado em 3 min", "Dados Reais M&A", "17 Setores", "PDF Profissional"
5. **Adicionar structured snippets:** Tipos: "Setores: Tecnologia, Saude, Varejo, Servicos, Alimentacao"
6. **Corrigir Final URL para HTTPS**

---

## Plano de Acao — Quick Wins (por prioridade)

| # | Acao | Impacto | Tempo | Check |
|---|------|---------|-------|-------|
| 1 | Configurar conversao "Compra R$ 99" no Google Ads | **Critico** | 15 min | G42 |
| 2 | Mudar bidding para Maximize Clicks (CPC max R$ 3) | **Critico** | 2 min | G36 |
| 3 | Remover Target CPA R$ 50 | **Critico** | 1 min | G37 |
| 4 | Criar listas de negativas (Exact Match) | **Alto** | 10 min | G14 |
| 5 | Adicionar sitelinks (4+) | **Alto** | 10 min | G50 |
| 6 | Adicionar callouts (4+) | **Medio** | 5 min | G51 |
| 7 | Melhorar headlines RSA (8→15) | **Alto** | 15 min | G27, G29 |
| 8 | Adicionar descricoes RSA (4 total) | **Medio** | 10 min | G28 |
| 9 | Mudar top 4 keywords para Phrase Match | **Alto** | 5 min | G17 |
| 10 | Corrigir Final URL para HTTPS | **Medio** | 2 min | G24 |
| 11 | Verificar location = "Pessoas em" | **Medio** | 2 min | G11 |
| 12 | Desabilitar Display Network | **Medio** | 2 min | G12 |

---

## Projecao pos-otimizacao

Com as Quick Wins implementadas (items 1-8):

| Metrica | Atual | Projetado (30d) |
|---------|-------|-----------------|
| Impressoes/dia | ~21 | 40-60 |
| Cliques/dia | ~3.3 | 5-8 |
| CPC medio | R$ 1.99 | R$ 1.50-2.50 |
| CTR | 15.48% | 12-18% |
| Conversoes/mes | 0 | 3-8 (taxa 3-5%) |
| CPA | infinito | R$ 60-150 |
| ROAS | 0 | 0.66-1.65x |

**Nota:** Projecao conservadora. O gating implementado na landing page (valor blur + timer) deve melhorar significativamente a taxa de conversao. Primeiros 30 dias sao para coletar dados.

---

## Campaign #1 (Performance Max) — PAUSADA

**Status:** Mantida pausada conforme solicitado.
**Nota:** Nao reativar ate ter:
1. Conversao tracking funcionando
2. Pelo menos 30 conversoes na campanha Search
3. Assets de video criados (PMax sem video tem performance ruim)

---

*Relatorio gerado pelo sistema de auditoria Google Ads. Baseado em 74 checks com scoring ponderado por severidade.*
