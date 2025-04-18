## Storytelling e cenário atual

A FindMyStuff surgiu com o propósito de transformar a experiência de compra online, atuando como um marketplace inteligente e centrado no cliente, que conecta vendedores e consumidores de forma fluida, segura e eficiente. Desde o início da operação, foi desenvolvida uma aplicação central robusta e monolítica, que por muito tempo atendeu bem às necessidades do negócio. Essa plataforma sustentava todas as operações digitais com estabilidade e confiabilidade — desde a gestão de vendedores e produtos até o checkout e o atendimento ao cliente.

Com o crescimento da base de usuários e a entrada de novos parceiros e lojistas, a complexidade da operação aumentou significativamente. A FindMyStuff expandiu seus times de tecnologia, investindo em mais profissionais para acelerar a entrega de funcionalidades e manter a competitividade em um mercado cada vez mais dinâmico. No entanto, o que parecia um caminho natural revelou uma limitação estrutural importante.

A arquitetura monolítica da aplicação passou a ser um entrave. Cada nova funcionalidade exigia mudanças em uma base de código extensa e altamente acoplada, tornando o desenvolvimento lento, arriscado e custoso. Como resultado, o time-to-market aumentou consideravelmente, prejudicando a capacidade da empresa de responder com agilidade às demandas dos lojistas, consumidores e parceiros.

Enquanto isso, outros marketplaces que apostaram em arquiteturas modernas, modulares e escaláveis passaram a ganhar vantagem competitiva, lançando novos recursos com muito mais rapidez e flexibilidade.

Hoje, a FindMyStuff se encontra em um ponto de inflexão: é fundamental repensar sua estrutura tecnológica para acompanhá-la na próxima fase de crescimento. A modernização da arquitetura não é mais uma opção — é um passo estratégico essencial para retomar a agilidade, fomentar inovação, garantir escalabilidade e assegurar a sustentabilidade da operação no longo prazo.


## O que esperamos aprender com esse projeto? 

Com este projeto, esperamos aprender como modernizar de forma eficaz uma arquitetura legada, migrando de um modelo monolítico para uma estrutura mais modular, escalável e alinhada com as melhores práticas de desenvolvimento de software. Além de entender como alinhar a evolução tecnológica com os objetivos estratégicos da empresa, garantindo que a transformação digital realmente gere valor para os clientes e para o negócio, bem como entender como planejar e executar a decomposição dos domínios da aplicação monolítica em micro-serviços, fazendo uso do Strangler Pattern.


#### 


## Que perguntas precisamos que sejam respondidas?



1. **Como está estruturada a arquitetura AS IS do sistema?**
2. **Quais são os requisitos não funcionais atuais da aplicação?**

    (Ex: RTO, RPO, SLA, TPS, tempo de resposta, disponibilidade, escalabilidade, segurança) — Eles são documentados? Estão sendo atendidos?

3. **Qual é a expectativa de crescimento no uso da aplicação nos próximos 3 a 5 anos?**

    (Ex: aumento de usuários, transações por segundo, volume de dados, integrações com parceiros)

4. **Quais padrões e tecnologias de arquitetura distribuída o time já domina?**

    (Ex: microsserviços, eventos, filas, containers, Kubernetes, mensageria, APIs REST/GraphQL) — O time tem familiaridade prática com eles?

5. **Qual domínio do sistema sofre mais com as limitações da arquitetura atual? **E onde a rigidez tecnológica impacta diretamente os resultados do negócio?
6. **Os times de desenvolvimento estão organizados por domínios de negócio?**

    (Ex: modelo ágil, squads independentes, ownership de serviços) — Como é o nível de autonomia técnica?

7. **Quais partes do sistema são candidatas viáveis para extração ou refatoração? **Há blocos que já estão prontos para serem modularizados ou desacoplados?
8. **Quem é o sponsor do projeto e quais stakeholders estão envolvidos? **
9. Quais áreas serão impactadas diretamente pela mudança e precisam estar alinhadas desde o início?
10. **Existe um orçamento definido para a modernização da arquitetura?**
11. **Qual é o prazo esperado para entrega da nova arquitetura ou suas primeiras fases?**
12. **Quais ferramentas e práticas de observabilidade serão necessárias?**

    (Ex: monitoramento, tracing distribuído, alertas, dashboards, logs estruturados) — O que já está em uso e o que precisa ser incorporado?

13. **Quais as métricas de sucesso que o cliente avalia serem as principais para o projeto? (OKR, KPIs)**
14. **Existe alguma funcionalidade que está no roadmap de evolução da aplicação e que deverá ser implantada de imediato?**


## Riscos do projeto


##### Definição errônea do problema e dos requisitos

Caso o projeto tenha feito um levantamento errado, nossa arquitetura baseline está comprometida e pode afetar a solução que vamos propor.


##### Mudança de objetivos da empresa

Caso o board da empresa mude seu direcionamento estratégico, o projeto pode se tornar inviável.


##### Orçamento

O uso de ferramentas e técnicas voltadas para a arquitetura de microsserviços tendem a ter um custo alto. Dimensionar uma volumetria irreal pode incorrer em custos não vantajosos. É preciso estar atento para que o ROI do projeto seja sempre positivo.


##### Conhecimento técnico

O time de desenvolvimento pode não ter o conhecimento necessário para migrar a aplicação para microsserviços. Causando atrasos e falhas na entrega.


##### Mudança de consumo do cliente 

O cliente pode alterar o seu padrão de consumo reduzindo os seus gastos no e-commerce.


## Plano de aprendizado do projeto


<table>
  <tr>
   <td>Semana
   </td>
   <td>Atividade
   </td>
   <td>Entregável
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Kickoff interno: alinhar objetivos e abordagem
   </td>
   <td>Roteiro do discovery, definição de papéis
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Preparar materiais: checklist, templates, mapas
   </td>
   <td>Formulários, mapa de perguntas, templates de documentação
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Workshop de visão geral e arquitetura AS IS
   </td>
   <td>Diagrama atual
   </td>
  </tr>
  <tr>
   <td>2-3
   </td>
   <td>Entrevistas com tech leads e analistas sobre requisito não-funcionais
   </td>
   <td>Matriz de requisitos e métricas (RTO, SLA, etc)
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Reunião com áreas de negócio para entender a expectativa de crescimento
   </td>
   <td>Projeção de uso e crescimento (usuários, dados, transações)
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Workshop técnico com o time para mapear maturidade e tecnologias
   </td>
   <td>Avaliação de domínio técnico
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Identificação de gargalos por domínio e viabilidade de refatoração
   </td>
   <td>Lista de domínios impactados e oportunidades de extração
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Mapeamento de stakeholders, sponsors e restrições
   </td>
   <td>Quadro de stakeholders, orçamento e restrições
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>Identificação de métricas de sucesso (KPIs/OKRs) e prioridades de curto prazo
   </td>
   <td>Lista de métricas e demandas críticas no roadmap
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Análise de logs, métricas de uso e observabilidade atual
   </td>
   <td>Diagnóstico técnico com pain points
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Validação cruzada de dependências e pontos de acoplamento
   </td>
   <td>Mapa de dependências e riscos
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>Benchmark interno de ferramentas de observabilidade
   </td>
   <td>Recomendação de stack técnica
   </td>
  </tr>
</table>





## Plano de redução de riscos


##### **Definição errônea do problema e dos requisitos** 

1. **Sessões de design discovery com todos os stakeholders** **para termos uma visão do problema de diversas perspectivas**: validaremos hipóteses e protótipos com o time de negócio, tecnologia e operacional. Também propomos o estabelecimento de checkpoints formais para validar a estratégia adotada conforme o projeto evolui.		


##### **Mudança de objetivos da empresa**



1. **Alinhamento Estratégico Contínuo com Roadmap Flexível: **Manter o board informado com relatórios regulares e demonstrações de progresso, destacando o valor gerado em cada fase. Planejar entregas modulares, como APIs independentes, que criem valor por si mesmas, permitindo a continuidade do projeto mesmo com mudanças de foco estratégico.
2. **Governança Adaptativa:** Criar uma estrutura de governança ágil que permita ajustes rápidos e pausas, evitando acoplamentos rígidos e facilitando redirecionamentos com impacto mínimo.


##### **Orçamento**



1. **Monitoramento de uso: **com ferramentas de observabilidade bem estabelecidas,

    coletamos dados de tráfego, uso e carga dos nossos serviços. 

2. **Estabeleceremos KPIs de sucesso para cada métrica de uso**: as métricas serão

    vinculadas ao custo do projeto. Dessa forma, temos como medir se o ROI está positivo


    e criar estratégias e ADRs com base nesta informação.



##### **Conhecimento técnico**



1. **Capacitação Estruturada:** Criar um plano de capacitação contínua que inclua workshops, certificações, pares com especialistas e bootcamps internos focados em microsserviços, eventos, mensageria e DevOps.
2. **Transição Progressiva:** Iniciar a migração com equipes pequenas e escopos bem definidos, enquanto parte da equipe mantém a operação do sistema monolítico, evitando sobrecarga e uma curva de aprendizado excessiva.


##### **Mudança de consumo do cliente**



1. **Análise de Comportamento em Tempo Real**: Utilizar ferramentas de observabilidade para detectar rapidamente mudanças nos padrões de consumo, como queda de acesso em categorias e abandono de carrinho.
2. **Arquitetura Orientada a Experimentação:** Facilitar a realização de A/B testing, personalização e análises por região e perfil, permitindo ajustes ágeis do produto conforme o comportamento do cliente.


## Partes interessadas



* **Os executivos da FindMyStuff** que poderão melhorar a experiência do cliente, aumentando receita e o CLV.
* **Time técnico da FindMyStuff** que poderão trabalhar com tecnologias modernas e dedicar mais tempo à inovação, do que fazendo troubleshooting do ambiente.
* **Clientes **que terão melhor experiência ao usar a plataforma


## Benefícios: o que eles esperam ganhar?

A **FindMyStuff **espera:



* Retomar a agilidade na disponibilização de novas funcionalidades na aplicação, melhorando o time-to-market
* Fomentar a inovação no processo de criação de novos serviços, ajudando a empresa a se manter na vanguarda tecnológica neste segmento
* Garantir a escalabilidade e disponibilidade da aplicação
* Assegurar a sustentabilidade do negócio no longo prazo, sempre focando em entregar uma melhor experiência para o cliente


## Público alvo

A **FindMyStuff**, como um marketplace abrangente, atinge um público-alvo diversificado, abrangendo desde indivíduos até pequenas/médias empresas. Aqui estão os principais segmentos:



* **Consumidores Individuais:**
    * Pessoas que buscam uma ampla variedade de produtos, desde itens de uso diário até produtos especializados.
    * Compradores que valorizam a conveniência de comprar online e a variedade de vendedores.
    * Consumidores que buscam preços competitivos e promoções.
* **Pequenos e Médios Empresários:**
    * Vendedores que utilizam a plataforma para alcançar um público maior e expandir seus negócios online.
    * Empreendedores que buscam uma plataforma de e-commerce com ferramentas e serviços para gerenciar suas vendas.

Em uma análise apresentada pelo time executivo, hoje as gerações mais presentes na plataforma são:



* **Geração Z:** é o grupo que mais cresce no marketplace, com destaque para a compra de celulares e itens tecnológicos.
* **Millennials e Geração X:** compõem grande parte da audiência, com os Millennials sendo responsáveis por mais da metade do faturamento.


## Objetivos: O que eles estão tentando realizar?



1. **Melhorar o Time-to-Market:** Reduzir o tempo necessário para implementar novas funcionalidades e atualizações, garantindo que a empresa permaneça competitiva no mercado de e-commerce.
2. **Modernização da Arquitetura de Sistemas: **Migrar sua aplicação monolítica para uma arquitetura de microsserviços, visando melhorar a agilidade e a escalabilidade do sistema.
3. **Redução de custos operacionais: **Implementar uma infraestrutura que proporciona escalabilidade elástica, ajustando os custos operacionais conforme a demanda real do tráfego.


## Preocupações: qual o pior que pode acontecer?



1. **Prejuízo financeiro na transição**: se a solução impedir o cliente de realizar os pedidos de alguma forma, o faturamento da empresa é diretamente impactado.
2. **Perda de confiabilidade**: um serviço com funcionamento intermitente impacta negativamente a imagem que o cliente tem sobre a empresa.
3. **Trazer os problemas da arquitetura atual**: se a nova arquitetura continuar com problemas de acoplamento entre os domínios, o time-to-market pode piorar drasticamente e novos problemas podem surgir. 
4. **Crise econômica:** crises e outras ameaças externas podem inviabilizar a conclusão do projeto, parando a migração na metade.


## Diagrama de arquitetura


##### Arquitetura AS-IS

![alt_text](images/image1.png "image_tooltip")


![alt_text](images/image2.png "image_tooltip")



##### Arquitetura TO-BE

![alt_text](images/image3.png "image_tooltip")



## Descrição dos componentes


##### Camada de Apresentação (Front-End e Acesso Externo)



* **Web UI SPA **e **BackOffice Web UI (SSR)**: interfaces do cliente e da equipe interna.
* **API Gateways (E-commerce e Mobile)**: roteiam requisições, aplicam regras de segurança e controle de acesso.
* **Segurança**: inclui HTTPS, DNS, WAF, CDN, autorizações personalizadas e proteção contra DDoS.


##### Camada de Domínio (Microsserviços)

Microsserviços independentes, responsáveis por funcionalidades específicas: **Pedidos** (Criar, Obter, Alterar, Pagar, Rastrear);  **Carrinho; Catálogo de Produtos; Entrega; Pagamento; Conta; Fidelidade; Estoque; Promoção; Recomendação; Notificações**

Cada serviço tem seus próprios adaptadores (DB, REST, mensageria).


##### Comunicação Assíncrona (Event-Driven)



* **Event Topics**: tópicos para publicação e consumo de eventos.
* **Filas e Sagas**: coordenação de fluxos distribuídos (ex: pagar ou cancelar pedido).
* **CDC / Outbox Pattern**: captura de mudanças no banco e publicação confiável de eventos.


##### Persistência de Dados



* **Bancos de dados**: SQL para o monolito e NoSQL para os micro serviços.
* **Outbox Table e BinLog**: suporte ao CDC e consistência eventual.


##### Integrações com Terceiros



* **Paguei** (pagamento), **Entrega Rápida**, **SES (e-mail)**, **SNS (SMS)**.
* Integrações feitas via adaptadores REST e mensageria.


##### Infraestrutura e DevOps



* **CI/CD Pipeline**: Git, builds, testes, deploys automatizados.
* **Service Mesh**: comunicação segura e observável entre microsserviços.
* **Observabilidade**: logs, métricas, tracing, dashboards.
* **Secret Vault e Image Repository**: segurança e versionamento de containers.


##### Sistema Legado (Monólito)

Parte da lógica de negócio ainda reside no monólito, em processo de migração gradual via **Strangler Pattern**.


## Requisitos da arquitetura



* **Escalabilidade**: esta plataforma de e-commerce é a principal fonte de renda da empresa e deve suportar demandas de crescimento do negócio, seja estas demandas planejadas (como campanhas promocionais), quanto demandas geradas por fatores externos onde a **FindMyStuff **não tem controle sobre o evento.
* **Performance**: Como o foco da FindMyStuff é garantir uma melhor experiência para seus clientes, garantir a performance das transações executadas na plataforma é fundamental para garantir uma boa experiência.
* **Segurança**: A segurança da informação sempre foi nossa prioridade. Lidamos com dados sensíveis e não podemos nos dar ao luxo de termos os dados dos nossos clientes comprometidos. 
* **Agilidade**: Precisamos melhorar nosso time-to-market para lançar novas funcionalidades e continuar inovando em nosso segmento. Para tal, agilidade na entrega de novos produtos usando conceitos ágeis, continuous integration, continuous deployment e delivery e os padrões modernos adotados nos ajudará a atingir este objetivo.
* **Disponibilidade**: Cada segundo que a plataforma fica indisponível é uma venda que deixamos de fazer e um cliente/parceiro infeliz e não podemos aceitar isso. Por isso, garantir a disponibilidade da nossa plataforma é crucial para o sucesso do nosso negócio.


## Sobre o que o diagrama ajuda a raciocinar/pensar?



1. **Estrutura e Interconexões:** Ilustra como os componentes do sistema se interconectam e interagem, facilitando a compreensão do fluxo de dados.
2. **Escalabilidade e Flexibilidade:** Permite visualizar como a arquitetura pode ser escalada e adaptada para atender necessidades futuras.
3. **Identificação de Dependências:** Ajuda a identificar dependências entre componentes, avaliando os impactos de alterações.
4. **​​Oportunidades de Melhoria:** Facilita a identificação de pontos críticos e otimizações possíveis.
5. **Estratégias de Implementação:** Apoia a formulação de estratégias para uma transição eficiente para microsserviços.




## Padrões essenciais de arquitetura



1. **Microsserviços: **Adotamos uma estratégia de microsserviços para desacoplar responsabilidades, permitindo escalabilidade flexível e adaptável.
2. **CQRS: **Este padrão facilita a implementação de event-sourcing entre os microsserviços e a aplicação legada, aumentando a confiabilidade e independência dos componentes.
3. **EDA: **Uma solução orientada a eventos é valiosa em processos prolongados, como o processamento de pedidos, permitindo que etapas sejam executadas sob demanda sem reservar recursos desnecessários.
4. **Service Mesh:** O service mesh é crucial para gerenciar a comunicação entre microsserviços, oferecendo monitoramento de requisições, regras de autenticação e autorização, e padrões de resiliência, como retries, circuit breakers e timeouts.
5. **API Gateway: **O API Gateway centraliza o ponto de saída para diversos serviços, simplificando o gerenciamento e unificando as interações, garantindo eficiência no processamento de solicitações.
6. **Hexagonal: **Este padrão de arquitetura proporciona uma visualização clara das dependências de cada serviço, assegurando que o fluxo da aplicação (entrada e saída síncrona e assíncrona, domínios, etc.) esteja explícito.


## Padrões ocultos



1. **DDD: **A aplicação, inclusive legada, está orientada a domínio, facilitando a aplicação de princípios do Strangler Pattern
2. **BFF: **Existem componentes na arquitetura para adaptar a apresentação dos dados com base na plataforma e origem do cliente. 
3. **Strangler Pattern: **Para chegar na arquitetura final, a arquitetura deverá ser quebrada em pequenas entregas realizando a migração de forma concisa e focando no que entregará maior valor ao cliente.


## 


## Metamodelo

O metamodelo definido para nossa arquitetura é estruturado em cinco pilares principais. Esse metamodelo orienta o design e desenvolvimento da arquitetura, assegurando a eficácia e integração de todos os pilares: 



1. **Microsserviços: **Unidades autônomas que encapsulam responsabilidades específicas, promovendo desacoplamento e escalabilidade flexível.
2. **Observabilidade: **Capacidade de monitorar e entender o desempenho dos microsserviços, utilizando métricas, logs e rastreamentos para rápida identificação de problemas e ajuste das operações.
3. **Latência:** Tempo de resposta das interações entre serviços, com foco em sua minimização para garantir uma experiência de usuário eficiente em processos críticos.
4. **Autorização e Autenticação**: Regras de segurança que garantem acesso seguro, identificando usuários e serviços (autenticação) e definindo permissões de acesso (autorização).
5. **Mensageria: **Sistema de comunicação assíncrona entre microsserviços, que facilita a troca de dados, aumenta a resiliência e permite a escalabilidade do sistema.


## Entendimento da arquitetura: pode ser discernido no diagrama único?

Não. Para detalhar todas as estruturas, suas dependências e operações, será necessário criar diagramas com diferentes objetivos, como descrever os processos do SAGA, fluxo de autenticação/autorização, e pipeline de dados.


## Consolidação do diagrama: o diagrama está completo?

**	**Não. Apesar do diagrama principal apresentar os componentes e a estrutura de nossa solução, para se ter uma visão geral é necessário analisar outros diagramas de diferentes perspectivas relacionadas a essa arquitetura, como arquitetura de tecnologia e de dados.


## 


## Simplificação: poderia ser simplificado e ainda assim ser eficaz?

Existem alguns pontos que poderiam ser simplificados, como o acoplamento do micro serviço de criação de pedidos e o de busca de pedidos. Essa abordagem seria eficaz, mas não eficiente caso a demanda aumentasse substancialmente, uma vez que uma das funcionalidades poderia sofrer com alta latência devido a volumetria dos serviços.

O banco de dados de pedidos poderia continuar dentro do banco de dados do monólito sendo uma abordagem mais simples, porém não seria eficiente e estaria não compliance com o pattern de micro-serviços.


## Discussões: houve alguma discussão importante que como equipe?



1. Qual estratégia devemos usar para que o monolito acesse os dados de pedido, que agora são gerados pelo novo microsserviço
2. Teremos um microsserviço (API) dedicado para a leitura de pedidos ou essa funcionalidade será acoplada no mesmo serviço de criação de pedidos?
3. Haveria a necessidade de utilizar mais de um api gateway (para uso externo e uso do backoffice)?


## Decisões: Que decisões a equipe teve dificuldade para tomar?



1. Entendemos que seria ideal termos um data lake para que todas as aplicações possam acessar dados históricos. Tivemos que desistir da ideia para focar numa solução mais simples, rápida e de baixo custo para esta fase do projeto.
2. Tivemos dificuldade de escolher entre bancos de dados SQL e NoSQL para o microsserviço de pedidos. No final escolhemos NoSQL para garantir que os schemas sejam maleáveis.


## 


## Incertezas: que decisões foram tomadas sob incerteza?



1. Não era claro se todas as tabelas auxiliares fariam sentido de serem replicadas via CDC para o banco de pedidos. Mesmo incertos, decidimos por não transmiti-las e usar strings para status e outras enumerações. 
2. Não tínhamos detalhes sobre a frequência e quantidade de resultados que os módulos de recomendação precisavam. Mesmo assim, decidimos que o serviços e busca de pedidos limitaria a busca com base na data do pedido.


## Desistências: houve algum ponto de decisão sem retorno ou que a equipe desistiu?

	Não, como iniciamos o brainstorm com a premissa de que a solução deve ser a mais simples e rápida de implementar possível, nos protegemos contra decisões que não fossem estratégicas nesta fase do projeto.




## Arquitetura C4Model

##### Nível Contexto

![alt_text](images/image4.png "image_tooltip")



##### Nível Container

![alt_text](images/image5.png "image_tooltip")



##### Nível Componente

![alt_text](images/image6.png "image_tooltip")


![alt_text](images/image7.png "image_tooltip")

