# Painel interativo: Status nutricional de escolares de Curitiba (2010–2018)

Painel de apoio ao artigo "Estado nutricional de escolares de Curitiba, Paraná, 2010–2018: integração, georreferenciamento e visualização interativa de bancos de dados de pesquisa em atividade física e saúde".

Trabalho desenvolvido no GPAFETEC (Grupo de Pesquisa em Atividade Física, Esporte e Tecnologia, UTFPR), a partir da dissertação de mestrado de Marcia Cristina da Silveira, defendida no Programa de Pós-Graduação em Engenharia Biomédica (PPGEB/UTFPR).

## Conteúdo

| Arquivo | Descrição |
| --- | --- |
| `index.html` | Painel interativo completo, em um único arquivo. Funciona offline e em qualquer hospedagem estática, sem servidor, login ou conexão com serviços externos. |
| `dados_agregados_escolares_curitiba.csv` | Dados agregados que alimentam o painel (UTF-8). |
| `LEIAME.md` | Este arquivo. |

## Dados

Amostra analítica de 8.599 escolares de 6 a 17 anos, de 73 escolas de Curitiba, provenientes de seis bancos de pesquisa (CEAFS/UFPR e GPAFETEC/UTFPR), coletados entre 2010 e 2018. Foram excluídos 271 registros duplicados e 4 com escore-z do IMC implausível (< −5).

Os dados são agregados: cada linha é uma contagem de escolares por escola, sexo, idade e classificação nutricional. Não há registros individuais nem informações que identifiquem participantes.

### Dicionário de dados (`dados_agregados_escolares_curitiba.csv`)

| Coluna | Descrição |
| --- | --- |
| `escola` | Nome da escola de coleta |
| `regional` | Regional administrativa de Curitiba registrada no banco de origem |
| `tipo` | Tipo de escola (Pública, Particular) |
| `latitude`, `longitude` | Coordenadas geográficas da escola (graus decimais, WGS 84) |
| `sexo` | Masculino, Feminino |
| `idade` | Idade em anos completos (6 a 17) |
| `faixa` | Faixa etária (6 a 9 anos, 10 a 14 anos, 15 a 17 anos) |
| `classificacao` | Estado nutricional pelo escore-z do IMC para idade e sexo, referência OMS 2007: Magreza (< −2), Eutrofia (−2 a +1), Sobrepeso (> +1 a +2), Obesidade (> +2) |
| `n` | Número de escolares na combinação das colunas anteriores |

Limites das regionais: Instituto de Pesquisa e Planejamento Urbano de Curitiba (IPPUC), Decreto Municipal nº 1.084/2015.

## Links diretos para as figuras do artigo

Acrescente o trecho abaixo ao endereço do painel para abri-lo já com os filtros de cada figura:

| Trecho | Abre |
| --- | --- |
| `#figura-mapa-excesso` | Mapa de excesso de peso por regional (todos os escolares) |
| `#figura-mapa-meninos` | Mapa de excesso de peso, meninos |
| `#figura-mapa-meninas` | Mapa de excesso de peso, meninas |
| `#figura-mapa-obesidade` | Mapa de obesidade por regional |
| `#figura-idade` | Prevalência por idade e sexo |
| `#tabela-regionais` | Prevalência por regional |
| `#tabela-escolas` | Tabela de escolas |

## Como publicar

### 1. GitHub Pages (endereço do painel)

Repositório: https://github.com/sssssfl2022/Gpafetec-

1. No repositório, clique em "Add file", "Upload files".
2. Arraste a pasta `status-nutricional-curitiba` inteira (com os três arquivos dentro) e clique em "Commit changes".
3. Em "Settings", "Pages", em "Build and deployment", escolha "Deploy from a branch", branch `main`, pasta `/ (root)`, e clique em "Save". O repositório precisa ser público.
4. Em alguns minutos o painel estará em https://sssssfl2022.github.io/Gpafetec-/status-nutricional-curitiba/
5. Teste esse endereço e um link de figura (por exemplo, https://sssssfl2022.github.io/Gpafetec-/status-nutricional-curitiba/#figura-idade) numa janela anônima.

### 2. Zenodo (DOI permanente)

1. Entre em zenodo.org com a mesma conta do GitHub.
2. Em "GitHub", ative o repositório e crie uma release (por exemplo, `v1.0`) no GitHub. O Zenodo arquiva a versão e gera um DOI.
3. Como alternativa, faça "New upload" diretamente no Zenodo com os três arquivos (tipo: Dataset), preencha autores, título, descrição, licença e publique.

### 3. No artigo

- Use o endereço do GitHub Pages nas legendas das figuras e na seção de disponibilidade dos dados.
- Cite o DOI do Zenodo na lista de referências e na seção de disponibilidade dos dados.

## Licença sugerida

Dados agregados e painel sob Creative Commons Atribuição 4.0 Internacional (CC BY 4.0), a confirmar pelos autores. A biblioteca D3.js (v7.9.0), embutida em `index.html`, é distribuída sob a licença ISC.

## Como citar

SILVEIRA, M. C. et al. **Painel interativo: status nutricional de escolares de Curitiba (2010–2018)**. Versão 1.0. GPAFETEC/UTFPR, 2026. Disponível em: https://sssssfl2022.github.io/Gpafetec-/status-nutricional-curitiba/. DOI: [a ser gerado no Zenodo].
