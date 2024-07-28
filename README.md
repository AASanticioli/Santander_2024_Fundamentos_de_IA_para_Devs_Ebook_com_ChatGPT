# Santander 2024 - Fundamentos de IA para Devs

Este repositório contém o ebook "Kotlin vs Java", criado para a disciplina __*"Criando um Ebook com ChatGPT & MidJourney"*__  do Bootcamnp __*"Santander 2024 - Fundamentos de IA para Devs"*__. Este ebook foi desenvolvido utilizando a ferramenta de IA Copilot da Microsoft, demonstrando como essa tecnologias pode ser aplicada na criação de conteúdo técnico.

## Resumo do Ebook

### Kotlin vs Java

O ebook "Kotlin vs Java" explora as principais diferenças e semelhanças entre essas duas linguagens de programação populares. Ele aborda aspectos como:

- **Sintaxe e Estrutura**: Comparação das estruturas básicas de código e sintaxe.
- **Desempenho**: Análise de desempenho em diferentes cenários de uso.
- **Interoperabilidade**: Como Kotlin e Java podem ser usados juntos em projetos.
- **Ferramentas e Suporte**: Disponibilidade de ferramentas e suporte da comunidade para cada linguagem.
- **Casos de Uso**: Exemplos de situações em que cada linguagem é mais adequada.

O objetivo do ebook é fornecer uma visão clara e objetiva para desenvolvedores que estão considerando qual linguagem adotar para seus projetos.

## Comandos utilizados para a criação do conteúdo no Copilot
1. Solicitação de análise do possível título do ebook
```
Aja como um especialista em marketing e publicidade, e faça considerações a respeito do título “Kotlin ou Java: considerações ao Iniciar o backend de um novo projeto” para um ebook, apresentando quais as percepções e reações que o público alvo (desenvolvedor backend júnior que esteja aprendendo java) possa ter.
```


2. Solicitação de criação de conteúdo
```
Faça um texto para ebook, com foco em desenvolvimento de backend com Kotlin e Spring, listando as principais diferenças entre ele e o desenvolvimento backend com Java e Spring, apresentando desde a estrutura de código - baseada nas premissas do livro  "Get Your Hands Dirty on Clean Architecture" de Tom Hombergs - até os testes,  passando pela declaração das bibliotecas do arquivo "build.gradle.kts" e os comentários pertinentes à arquitetura e à injeção de dependência. 

{REGRAS}
> Explique sempre de uma maneira simples
> Explique, em forma de notas de rodapé, cada termo técnico apresentado, considerando que o público são Desenvolvedores Juniores.
> Utilize como exemplo um ecommerce simples, com os seguintes módulos gradle: core, product, customer, order
> Considere que cada módulo será executado em seu próprio container Docker, ou seja, um arquivo Dockerfile por módulo gradle e um arquivo compose.yml para todo o projeto.
> Considerar uma pasta chamada "docker" que contenha os arquivos "postgresql.dockerfile" e "redis.dockerfile" para conter as declarações de container docker do banco de dados Postgfres e do banco de cache Redis. 
> Apresente os exemplos de código de maneira evolutiva, começando com o básico e evoluindo até chegar à versão final do código.  
> Utilize TDD, ou seja, antes de cada exemplo kotlin, apresente o código do caso de teste que realizará  o teste unitário do exemplo.
> Mantenha uma linguagem ubíqua
> Sempre apresentar os códigos em Kotlin primeiro e depois o mesmo código em java, descrevendo um comparativo entre os dois logo abaixo. 
> Sempre relacione os exemplos a cada parte da aplicação, apresentando qual é a arquitetura envolvida e o porquê de se utilizar essa abordagem.
> Siga o seguinte roteiro:
- Capítulo 01: apresentar uma introdução sobre kotlin, apresentando dados estatísticos de seu uso em backend dos últimos 5 anos - tanto com Spring quanto com ktor -, comparando com os mesmos dados do uso de java no backend no mesmo período.
- Capítulo 02: apresentar a estrutura de pastas proposta no livro "Get Your Hands Dirty on Clean Architecture" 2ª edição de Tom Hombergs para cada um dos módulos, explicando os pontos fortes e fracos dessa arquitetura, além de suas indicações e contraindicações. 
- Capítulo 03: considerando que o leitor já conheça docker, explicar as vantagens e desvantagens do uso de containeres docker no contexto de aplicações backend kotlin e java, explicando também o uso de Docker Compose em ambiente de desenvolvimento e de Kubernbetes em ambiente de produção. 
- Capítulo 04: Explicar o que é Gradle e como ele deve ser configurado para o aplicativo que iremos construir. Apresente todos os arquivos gradle de configuração do projeto, destacando a diferença entre as declarações do projeto kotlin para o projeto java. 
- Capítulo 05: Apresentar o conceito de domínio do DDD, relacionando o conceito ao porquê de se distribuir a aplicação pelos módulos gradle do projeto. Utilizando o módulo de ":product" como exemplo, apresente o código de declaração das entidades de domínio ("br.dev.santi.product.application.domain.entity"), dos serviços de domínio ("br.dev.santi.product.application.domain.service"), além das declarações das portas de entrada ("br.dev.santi.product.application.port.inn") e de saída ("br.dev.santi.product.application.port.out")
- Capítulo 07: Explicar o que é uma camada de persistência. Explicar JPA. Explicar flyway e como utilizá-lo em cada módulo da aplicação de forma independente. Apresentar os arquivos de configuração do flyway bem como as entidades para o módulo ":product", considerando que as entidades estão localizadas em "br.dev.santi.product.adapter.out.persistence.entity" e as configurações do flyway em "br.dev.santi.product.adapter.out.persistence.config". Apresentar o código dos mapeadores (mappers) que farão a conversão de entidades de domínio para entidades de persistência e vice-versa.
```
A solicitação excedeu o tamanho possível do prompt, então foi necessário realizar outro prompt:
```
Seguindo as mesmas regras, acrescente:
- Capítulo 06: Apresentar o conceito de Adaptadores da arquitetura hexagonal e como Tom Hombergs utiliza esse conceito em sua arquitetura. Apresentar como esse modelo é utilizado em aplicações kotlin com Spring e Java com Spring. 
- Capítulo 08: Apresentar os conceitos de Restfull. Apresetnar como o Spring lida com Rest. Apresentar como implementar os adaptadores de entrada web via API Rest com kotlin/spring e java/spring, considerando que o código se localiza em "br.dev.santi.product.adapter.inn.web" e que há arquivos separados para RestController, RequestBody (data class) e Response (data class).
```

## Lições aprendidas
1. A solicitação do conteúdo foi realizada dentro das regras do prompt, isso não ficou legal. Quando for gerar novamente, o ideal é fornecer as regras em um prompt inicial e depois solicitar capítulo por capítulo, refinando seu conteúdo.
2. O Midjourney apresentado no curso não aceita mais solicitações de período de teste (trial).
3. Testei outras ferramentas de geração de imagens por AI, mas as elas possuem restrições quanto ao uso de logos das linguagens de programação, mesmo quando as donas das patentes permitem seu uso para esse tipo de material. 
