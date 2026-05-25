# 🔥 Caminho do Fogo

**Plataforma de gestão de ocorrências para brigadistas de incêndio**

🔗 [Ver projeto ao vivo](https://caminhodofogo.vercel.app)

---

## Sobre o projeto

Caminho do Fogo é uma ferramenta de gestão operacional para brigadas de combate a incêndio. A plataforma permite visualizar ocorrências em mapa, registrar e acompanhar ações de campo, e consultar o histórico de incêndios detectados.  
---

## O problema

O projeto já estava em andamento quando entrei. Havia decisões tomadas, um desenvolvedor trabalhando, e telas sendo implementadas, mas o resultado final raramente correspondia ao que havia sido desenhado.

Fiz diversas telas com handoff muito detalhado: anotações de espaçamento, de cor, de posições, especificações de componente, guias de estilo inline. Mesmo assim, a implementação retornava inconsistente. Ficava me perguntando o que mais poderia fazer, já que não eram telas complexas, mas cada interpretação gerava uma nova divergência.

O estalo veio quando testei o **Figma Make**, a ferramenta de IA do próprio Figma que gera código HTML diretamente a partir dos designs. O desenvolvedor começou a usar esse HTML como referência de implementação e a precisão melhorou significativamente. A estrutura já estava lá; ele não precisava mais interpretar, só adaptar.

Com esse novo caminho em vista, decidi recuar e olhar para o projeto de forma mais ampla. Fiz uma análise de usabilidade e de interface do que havia sido construído até então, e a conclusão foi clara: antes de continuar entregando telas, o produto precisava de uma base sólida. Refiz o style guide do zero, tipografia, cores, espaçamentos, componentes, para que o time tivesse uma referência única e consistente.

A partir daí, as entregas mudaram de natureza. Com o style guide definido e o fluxo Figma \+ Claude estabelecido, passei a entregar as telas diretamente em HTML, navegáveis, com estados reais, prontas para implementar. Mais rápido e com muito mais fidelidade ao que havia sido projetado.

---

## Telas

| Tela | Descrição |
| :---- | :---- |
| `index.html` | Dashboard com visão geral e painel de camadas |
| `mapa.html` | Mapa interativo com marcadores de ocorrência e toolbar |
| `acoes.html` | Lista de ações com filtros, paginação e status |
| `detalhes-acao.html` | Detalhe de uma ação individual |
| `incendios.html` | Histórico de incêndios detectados |

---

## Stack e processo

O fluxo que emergiu desse aprendizado foi **Figma → Claude → GitHub → Vercel**, sem uso de frameworks JavaScript ou dependências externas.

- **Design:** Figma (sistema visual, tokens, componentes)  
- **Implementação:** HTML \+ CSS \+ JavaScript vanilla  
- **IA como par de desenvolvimento:** Claude (geração e refinamento de código, ajustes de componentes, resolução de bugs)  
- **Versionamento:** GitHub  
- **Deploy:** Vercel (CI/CD automático via push)

O papel do Claude nesse fluxo não foi só gerar código, mas sim tornar viável que uma designer conduzisse a implementação com autonomia. Cada decisão visual tomada no Figma era traduzida diretamente em código, refinada em conversa, e validada visualmente antes de ir para o repositório. O desenvolvedor recebia telas prontas para referenciar ou adaptar, em vez de interpretar especificações estáticas.

---

## Funcionalidades implementadas

- Navegação lateral colapsável  
- Toolbar interativa no mapa com ações de zoom, busca por coordenada e importação de camadas  
- Modal de "Exibição de dados" com sistema de camadas  
- Painel de ações com filtros por data, status e tipo  
- Paginação funcional na listagem de ações  
- Dropdowns com posicionamento dinâmico via JavaScript  
- Tags de status com variantes de cor  
- Tela de detalhe com acesso via ícone na listagem

---

## Aprendizados

- Trabalhar com IA como par de desenvolvimento acelera drasticamente o ciclo design → código, mas exige que o designer saiba **dirigir**, ou seja, identificar o que está errado, descrever o comportamento esperado, validar o resultado.  
- CSS vanilla com variáveis bem definidas se comporta como um Design System leve e suficiente para projetos dessa escala.  
- O GitHub como parte do fluxo de design e muda a forma de pensar em versões e iterações.

---

## Sobre a autora

**Victoria Nogueira** — Product Designer explorando o ponto de encontro entre sistemas de design, código e IA como ferramenta criativa.

[LinkedIn](https://linkedin.com/in/victorianogueiram) · [GitHub](https://github.com/victorianogueiram)  
