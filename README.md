# miniguia-estudos-notebooklm
Notebook Lm  utilizado para estudos na plataforma dio.me

Contexto e Objetivos:
  - Para este NotebooLM o tema escolhido foi sobre construção de testes automatizados utilizando a ferramenta Playwright. Este aplicativo será utilizado para estudos, pesquisas e até consultas em momentos em que é necessário acessar a documentação sem a necessidade de ficar procurando em diversas fontes pela internet sobre este framework que vem dominando o mercado de trabalho.
------------------------------------------------------------------------------------
Curadoria de Fontes
        Fontes de Texto:
          - https://playwright.dev/
          - https://playwright.dev/docs/intro
          -  https://playwright.dev/docs/writing-tests
          -  https://playwright.dev/docs/codegen-intro
          -  https://playwright.dev/docs/running-tests
          

        Fontes de Vídeo:
          -  https://www.youtube.com/watch?v=rAec3mZFhF0&t=109s
          -  https://www.youtube.com/watch?v=Rp2y-uotumE&t=2613s

-----------------------------------------------------------------------------------
Engenharia de Prompts e "Cicatrizes":
  prompt:   
  Como um analista de testes Senior, especialista em SDET, automações de testes e especialista nas melhores práticas de Testes de software,  a partir de agora responda as minhas perguntas consultando as fontes inseridas neste notebookLM. As respostas deverão ser exibidas em tópicos  e explicadas detalhadamente  com o objetivo de facilitar o entendimento sobre a ferramenta Playwright.

  prompt: 
  Gostaria de saber como faço a instalação do playwright no meu computador, ele não tem nenhum  ambiente de desenvolvimento estruturado. Como posso instalar e já iniciar os meus testes?

  prompt:
  Como um especialista, me  mostre como editar o arquivo de configuração do playwright e a pasta qual ele se localiza  por padrão no projeto criado após a instalação dos pré requisitos do playwright.**
  -------------------------------------------------------------------------------------
  Miniguia de Estudo (Entrega Final):

        1. Resumos Estruturados do Playwright
      O Playwright é definido como uma ferramenta de automação robusta, unificada e projetada para as necessidades da web moderna
      . Abaixo, os pilares fundamentais:
      Arquitetura e Suporte Multi-navegador: Diferente de outras ferramentas, o Playwright utiliza uma única API para controlar os motores Chromium, Firefox e WebKit
      . Ele gerencia seus próprios binários, garantindo que os testes funcionem de forma idêntica em Windows, Linux e macOS, sem depender dos navegadores instalados no sistema do usuário
      .
      Confiabilidade e Performance: A ferramenta elimina a intermitência (flakiness) através do auto-waiting (espera automática para que elementos estejam acionáveis) e asserções de "web-first", que tentam novamente até que a condição seja atendida
      . Além disso, sua performance é destacada por ser significativamente superior a concorrentes, permitindo execuções extremamente rápidas e paralelas por padrão
      .
      Isolamento Total: Cada teste é executado em um Browser Context exclusivo, o que equivale a um perfil de navegador novo e isolado
      . Isso evita a contaminação entre testes com custo de processamento quase zero, permitindo simular estados de autenticação de forma eficiente
      .
      Padrões de Projeto (POM): A implementação do Page Object Model (POM) é recomendada para manter o código limpo e sustentável
      . Este padrão separa os locatários de elementos e as ações em classes específicas para cada página, facilitando manutenções futuras: se um elemento mudar, a alteração é feita em um único lugar
      .
      
      --------------------------------------------------------------------------------
      2. Glossário de Conceitos Principais
      Auto-waiting: Recurso que aguarda automaticamente que um elemento esteja visível, estável e habilitado antes de realizar uma ação (como clique ou preenchimento)
      .
      Browser Context: Um ambiente isolado dentro de uma instância do navegador, funcionando como uma sessão privada que garante que um teste não interfira em outro
      .
      Codegen (Test Generator): Ferramenta que abre uma janela de navegador, grava as ações do usuário e gera automaticamente o código de teste correspondente
      .
      Headless Mode: Execução de testes em segundo plano, sem abrir a interface gráfica do navegador, o que economiza recursos e acelera o processo
      .
      Locators (Localizadores): A forma como o Playwright identifica elementos na página; ele prioriza métodos resilientes baseados em papéis de acessibilidade (como getByRole) em vez de seletores CSS frágeis
      .
      POM (Page Object Model): Padrão de design que cria uma classe para cada página da aplicação, encapsulando a lógica de interação e os seletores
      .
      Trace Viewer: Ferramenta de depuração que fornece uma linha do tempo completa do teste, incluindo snapshots do DOM, logs de rede e capturas de tela para cada etapa
      .
      UI Mode: Interface gráfica avançada para executar e depurar testes, permitindo o "time travel" para visualizar o estado da aplicação antes e depois de cada comando
      .
      
      --------------------------------------------------------------------------------
      3. Conjunto de Prompts para Revisões Futuras
      Estes prompts podem ser utilizados em novas consultas para aprofundar ou revisar o conteúdo:
      Prompt de Configuração Inicial: "Explique detalhadamente o processo de inicialização de um projeto Playwright via terminal e quais são os componentes principais do arquivo playwright.config.js criado."
      Prompt de Refatoração (POM): "Como posso converter um script de teste gerado pelo Codegen para o padrão Page Object Model, visando melhorar a manutenibilidade do código?"
      Prompt de Estratégias de Locatários: "Quais são as melhores práticas para a criação de localizadores resilientes no Playwright e por que devo preferir getByRole em vez de seletores CSS?"
      Prompt de Depuração: "Descreva como utilizar o UI Mode e o Trace Viewer para investigar um teste que falhou durante a execução em um pipeline de CI."
      Prompt de Execução Avançada: "Como configurar o Playwright para rodar testes em paralelo apenas em um navegador específico (como WebKit) e gerar um relatório HTML detalhado?"
        
