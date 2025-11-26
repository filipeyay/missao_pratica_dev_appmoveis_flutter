# Missão Prática Desenvolvimento Aplicativos Moveis Flutter

Trabalho da faculdade.

---

## 1. Objetivo da Prática

O objetivo central desta atividade foi executar os fundamentos do desenvolvimento mobile com o framework Flutter, focando na construção declarativa de interfaces de usuário. A prática focou na demonstração da utilização de Widgets estruturais (**MaterialApp**, **Scaffold**), de layout (**Row**, **Column**, **Stack**) e de rolagem (**ListView**).

O objetivo foi aplicar esses conceitos de forma integrada para desenvolver a interface visual do aplicativo "**Explore Mundo**", uma agência de viagens, garantindo responsividade e organização de código através da composição de widgets.

## 2. Análise Crítica da Missão Prática

A implementação do aplicativo da Agência de Viagens "Explore Mundo" exigiu a adoção de uma abordagem declarativa e baseada na composição do Flutter. O desenvolvimento seguiu um roteiro lógico para transformar requisitos visuais em código funcional:

- **Decomposição do Layout:** A primeira etapa foi a análise visual do design proposto, dividindo a tela em elementos básicos (linhas, colunas e blocos de texto). Identificou-se a necessidade de uma estrutura vertical principal contendo quatro seções distintas: imagem, título, botões e descrição textual.
- **Construção "Bottom-Up":** Adotou-se a estratégia de construir os componentes menores primeiro para depois integrá-los à estrutura maior.
- **Seção de Título:** Utilizou-se `Row` e `Column` aninhados. O uso do widget `Expanded` foi crucial aqui para garantir que o texto ocupasse o espaço disponível sem gerar _overflow_, empurrando o ícone de avaliação para a extremidade.
- **Reusabilidade (DRY):** Na seção de botões, implementou-se um método auxiliar (`_buildButtonColumn`) para gerar as colunas de ícones e textos. Isso demonstrou a capacidade do Flutter de tratar UI como código, facilitando a manutenção e evitando repetição desnecessária.
- **Gerenciamento de Assets:** A integração da imagem local exigiu a configuração do `pubspec.yaml` e o uso do `BoxFit.cover` para garantir que a imagem se adaptasse ao container sem distorção.
- **Responsividade e Rolagem:** A etapa final envolveu a substituição da `Column` principal por um `ListView`. Essa decisão técnica foi fundamental para garantir que o aplicativo fosse funcional em dispositivos com telas menores, permitindo a rolagem do conteúdo e evitando erros de renderização por falta de espaço vertical.

Essa abordagem prática demonstrou como a hierarquia de widgets do Flutter permite criar layouts complexos e responsivos de maneira eficiente e modular.
