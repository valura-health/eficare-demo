<div align="center">

# EfiCare — protótipo de interface

*by* **ValuraHealth**

**[▶ Abrir a demonstração](https://valura-health.github.io/eficare-demo/)**

</div>

---

## O que é isto

Protótipo navegável da interface do **EfiCare**, plataforma de gestão de suprimentos, custo e
padronização hospitalar da ValuraHealth.

É uma peça de **interface**, não um sistema: não há banco de dados nem persistência, e todos os
dados exibidos são fictícios.

- **Arquivo único** (`index.html`), autocontido: sem build, sem bibliotecas externas.
- **Tema claro e escuro.**
- **Acessibilidade** com meta WCAG 2.2 AA.

---

## Como abrir

- **Online:** use o link [Abrir a demonstração](https://valura-health.github.io/eficare-demo/).
- **Localmente:** clone o repositório e abra o `index.html` no navegador. Não é preciso
  instalar nada.

---

## Telas

A navegação lateral agrupa treze telas em quatro blocos:

| Bloco | Telas |
|---|---|
| **Operação** | Painel · Ingestão de documentos · Catálogo (matriz ABC×XYZ) · Ressuprimento · Risco de validade · Tabelas e preços |
| **Assistente** | Efi, o assistente conversacional |
| **Antecipação** | Sentinela, a antecipação de riscos |
| **Decisão** | Recebimento · Plano de compra sob verba · Negociação · FMEA · Relatórios |

> **Plano de compra** é a única tela que tenta falar com uma API. Ela consulta
> `http://127.0.0.1:8000/saude` (quando aberta via `file://` ou GitHub Pages) e, se não houver
> resposta, usa o conjunto de demonstração e sinaliza isso no cabeçalho. Sem API local, tudo
> funciona normalmente com dados fictícios.

---

## ⚠️ Todos os dados são fictícios

Nenhum número, item, fornecedor, operadora, prescritor ou pessoa neste protótipo corresponde a
dado real de qualquer instituição. Os nomes de operadoras são genéricos de propósito
(*"Cooperativa Médica Regional"*, *"Autogestão Industrial"*), e os valores servem apenas para
demonstrar o comportamento da interface.

---

## Princípios de design demonstrados

| Princípio | O que significa | Onde aparece |
|---|---|---|
| **Nenhum número sem procedência** | Todo dado mostra de onde veio e quando | Carimbo de fonte e data do espelho em cada bloco |
| **Régua de preço** | O preço pago é lido em contexto, não isolado | Valor posicionado entre o piso de mercado e o teto legal |
| **Tarja ABC×VEN** | Criticidade visível sem abrir o item | Faixa colorida na borda de cada item (V = vital, E = essencial, N = não essencial), inspirada no vocabulário da farmácia hospitalar |
| **Matriz de estratégia** | A classificação do item define quanto esforço de gestão ele merece | Nove células ABC×XYZ agrupadas em três regimes de controle |
| **Privacidade por padrão** | Dados de pessoas ficam ocultos até haver motivo | Prescritores pseudonimizados; revelação só mediante justificativa |

---

## Licença

Software proprietário. © ValuraHealth. Todos os direitos reservados. Veja [LICENSE](LICENSE).

Você pode visualizar a demonstração livremente. Reproduzir, adaptar ou reutilizar o código ou o
design não é permitido.
