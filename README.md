# Red8 x Prestadores · Análises Clínicas

Análise do valor pago à Red8 em exames de análises clínicas comparado ao menor preço do mercado (DASA, CDB, Rede, Pardini e Fleury).

**Uso interno. Contém preços de contrato.**

## Arquivos

- `index.html`: o painel. Abre direto no navegador.
- `dados_exames.csv`: base consolidada por exame (separador `;`).

## Metodologia

- Período: jan/26 a out/26 (10 meses). Volumes de jan/26 a jun/26 da planilha comparativa e de jul/26 a out/26 dos relatórios de repasse da Red8, contando só exames com laudo.
- Valores anuais = preço unitário × média mensal de jan/26 a out/26 × 12. Exames sem preço unitário: valor de jun/25 a jun/26 ÷ 13 × 12.
- Preços da Red8 da planilha comparativa, exceto PSA Total (MV 1067): R$ 23,73, valor faturado nos relatórios.
- Menor preço: menor valor entre DASA, CDB, Rede, Pardini e Fleury para cada exame. Zero foi tratado como sem cotação.
- Homocisteína (MV 818): sem o preço da Rede.
- Códigos MV repetidos foram contados uma vez.
- Cenários: conservador (50% da diferença para o menor preço), moderado (75%) e agressivo (igualar o menor preço).
- Rede, Pardini e Fleury têm preço apenas em uma lista de cerca de 90 exames; DASA e CDB cobrem a carteira.

## Colunas do CSV

`red8`, `dasa`, `cdb`, `rede`, `pardini`, `fleury`: valor anual por prestador.
`u_*`: preço unitário por exame, quando disponível. `qtd`: solicitações anualizadas (média mensal de 2026 × 12).
