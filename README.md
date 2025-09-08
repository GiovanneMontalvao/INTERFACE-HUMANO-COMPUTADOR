# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **DETECÇÃO DE MACACOS-PREGO POR VISÃO COMPUTACIONAL A PARTIR DE VÍDEOS EM AMBIENTES NÃO-CONTROLADOS** sob orientação do Professor **Reinaldo Bianchi** e desenvolvido pelos seguintes alunos:

- Diego Meira Jardim da Silva
- Giovanne Delghingaro Montalvão

## Resumo

Desenvolveremos um sistema automatizado, baseado em aprendizado profundo, para classificar a presença de macacos-prego (Sapajus spp.) em vídeos de ambientes não controlados. Além de criar uma interface gráfica para os usuários poderem escolher os vídeos que querem que sejam analisados.

## Introdução
 
- O sistema desenvolvido tem como propósito automatizar a detecção de macacos-prego em vídeos de armadilhas fotográficas, utilizando técnicas de aprendizado profundo. Ele oferece benefícios como a redução do tempo necessário para análise manual, maior precisão na identificação, padronização dos resultados e apoio direto às ações de monitoramento e conservação ambiental.
- A aplicação busca resolver o problema do grande volume de dados gerados por armadilhas fotográficas, que tornam inviável a revisão manual completa. Além disso, oferece uma solução não invasiva para o monitoramento da fauna em ambientes complexos como florestas tropicais.
- O sistema permite o processamento automático de vídeos, extraindo frames e detectando macacos-prego por meio de redes neurais convolucionais. Entre suas funcionalidades estão a exibição de bounding boxes nas detecções, geração de relatórios de ocorrência, possibilidade de ajuste do nível de confiança, exportação de dados e uma interface simples para upload e visualização dos resultados.
- Como tecnologias, iremos utilizar para desevolvimento a linguagem de programação Python e, como modelo de visão computacionao, YOLOv8s.
- O sistema será utilizado por pesquisadores, ONGs e instituições voltadas à conservação da biodiversidade. Os usuários poderão carregar vídeos obtidos em armadilhas fotográficas e obter automaticamente detecções de macacos-prego. O ambiente de uso inclui tanto laboratórios e centros de pesquisa, onde há computadores com maior capacidade de processamento, quanto aplicações em campo, onde a análise pode ser feita em equipamentos mais simples.

## Publico Alvo
- O produto é direcionado a pesquisadores em biologia da conservação, ONGs ambientais, universidades e órgãos de gestão de áreas protegidas.
- Esse público se caracteriza por atuar principalmente em regiões de florestas tropicais da América do Sul, onde os macacos-prego estão presentes. Demograficamente, inclui profissionais e estudantes de nível superior e pós-graduação. Comportamentalmente, trata-se de um grupo engajado em pesquisa científica, preservação ambiental e uso de tecnologias inovadoras. Psicograficamente, são pessoas motivadas pela conservação da biodiversidade e pela eficiência no manejo de dados.

## Análise de concorrência

1. Entre os principais concorrentes e softwares utilizados pelo público-alvo estão ferramentas de detecção automática de fauna em imagens de armadilhas fotográficas, como Wildlife Insights, TrapTagger e modelos genéricos de visão computacional como YOLO pré-treinados em bases amplas (COCO, ImageNet).
2. Os principais concorrentes são o Wildlife Insights, plataforma global de análise em nuvem; o TrapTagger, voltado à anotação colaborativa; e modelos genéricos como YOLOv5 e Faster R-CNN, amplamente usados em visão computacional.
3. O Wildlife Insights é escalável, mas depende de internet e possui custos. O TrapTagger é simples e colaborativo, porém lento. Já os modelos genéricos têm boa acurácia em contextos controlados, mas sofrem perda de desempenho em florestas tropicais.
4. Essas ferramentas oferecem interfaces acessíveis, mas muitas vezes exigem conexão com servidores externos ou não permitem ajustes finos para espécies locais. A experiência do usuário pode ser comprometida pela dependência de internet em áreas de campo e pela baixa flexibilidade de adaptação aos dados regionais.
5. Plataformas como Wildlife Insights trabalham em modelo freemium ou mediante parcerias institucionais, enquanto ferramentas colaborativas como TrapTagger são gratuitas, mas limitadas. Modelos de deep learning genéricos são gratuitos, porém exigem alto custo computacional em hardware.
6. Estudos apontam que usuários dessas plataformas reconhecem os benefícios da automação, mas reclamam da dependência de infraestrutura tecnológica, da baixa adaptabilidade a diferentes espécies e da falta de suporte local em contextos de conservação na América do Sul.
7. Há uma tendência crescente de especialização de modelos para habitats e espécies específicas, além da busca por soluções mais leves e acessíveis para uso em campo. Outro padrão observado é a integração entre IA e monitoramento participativo, com envolvimento de ONGs e comunidades locais.
8. As soluções existentes são úteis em cenários amplos, mas não atendem bem ao monitoramento de primatas neotropicais. Faltam flexibilidade, robustez em ambientes complexos e adaptação a espécies locais.
9. Entre os pontos fortes estão a escalabilidade, a colaboração comunitária e a base técnica consolidada. Recomenda-se que o sistema proposto seja especializado, robusto em campo e de fácil uso, além de permitir execução offline e adaptação a outras espécies.

### Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  #### Personas Primárias

   - Mariana Alves, 42 anos, pesquisadora em Biologia da Conservação – "Preciso de precisão e rapidez para não perder tempo com triagens manuais"
        - Mariana é pesquisadora em um instituto na Amazônia e coordena projetos de monitoramento da fauna em áreas protegidas. Ela lida com milhares de vídeos de armadilhas fotográficas e precisa de resultados confiáveis para publicar artigos científicos e apoiar políticas de conservação. Busca reduzir o tempo gasto em análises manuais e ter relatórios padronizados para embasar decisões.

<img width="315" height="315" alt="image" src="https://github.com/user-attachments/assets/65fce8b2-ef72-4dba-a8d5-78f2fb77fa1f" />

   
   - Lucas Ferreira, 28 anos, analista de ONG Ambiental – "Quanto mais acessível a tecnologia, mais impacto podemos gerar em campo"
        - Lucas trabalha em uma ONG que realiza monitoramento participativo de fauna junto a comunidades locais. Muitas vezes atua em áreas sem internet, o que exige ferramentas que funcionem offline. Precisa de uma solução simples e acessível para rodar em notebooks comuns, sem depender de grandes servidores. Valoriza tecnologias que aproximam ciência e comunidades em prol da conservação.

<img width="315" height="315" alt="image" src="https://github.com/user-attachments/assets/23918d55-b9b5-4647-8b9a-58cbf4b4303f" />

   
   - Camila Rodrigues, 31 anos, mestranda em Ecologia – "Preciso de uma interface clara para testar hipóteses no meu projeto"
        - Camila desenvolve dissertação sobre comportamento de primatas em fragmentos florestais. Ela deseja utilizar vídeos de armadilhas fotográficas para extrair informações quantitativas sobre presença e comportamento dos macacos-prego. Precisa de uma interface gráfica intuitiva, que permita carregar vídeos, ajustar níveis de confiança e exportar dados de forma organizada.

<img width="315" height="315" alt="image" src="https://github.com/user-attachments/assets/82a69e4e-802b-46c3-b3b6-67249031c5f5" />


  #### Personas Secundárias
    
   - João Pedro Martins, 23 anos, estudante de Ciência da Computação desenvolvendo seu Trabalho de Conclusão de Curso – "Quero aplicar IA em um problema real de conservação"
        - João Pedro está no último semestre de Ciência da Computação e decidiu aplicar visão computacional em um tema de impacto social e ambiental. Ele busca usar o sistema como base para aprender mais sobre aprendizado profundo e aplicar modelos como YOLO em problemas reais. Tem bom domínio de programação em Python, mas pouca experiência prática com ecologia e comportamento animal.

<img width="315" height="315" alt="image" src="https://github.com/user-attachments/assets/c4a6fe8e-8d96-4b39-b21d-a66eccd201e0" />


### Mapa de empatia

![Mapa de empatia](empatia.png)

## Personas Primárias
- Mariana Alves, 42 anos
  - O que o usuário vê: Laboratórios, armadilhas fotográficas, grandes volumes de vídeos no computador. Outros pesquisadores e alunos trabalhando em análises manuais demoradas. Relatórios científicos que dependem de muito esforço humano.
  - O que o usuário ouve: Conversas de colegas sobre a dificuldade em lidar com tantos dados. Demandas de instituições de conservação por relatórios rápidos e confiáveis. Críticas sobre erros ou atrasos na análise manual.
  - O que o usuário diz e faz: Reclama do tempo perdido em triagens manuais. Procura constantemente novas ferramentas para automatizar processos. Orienta alunos e cobra produtividade científica.
  - O que o usuário pensa e sente: Sente frustração com a lentidão do processo manual. Tem expectativa de que um sistema de IA traga precisão e economia de tempo. Acredita que a tecnologia pode acelerar avanços em conservação.
  - Dores: Volume excessivo de vídeos para analisar. Dificuldade em encontrar ferramentas adaptadas ao contexto de florestas tropicais. Pressão por resultados científicos rápidos.
  - Ganhos: Economia de tempo na análise. Relatórios padronizados e confiáveis. Apoio direto às suas pesquisas e publicações.

- Lucas Ferreira, 28 anos
  - O que o usuário vê: Comunidades locais em campo, áreas remotas sem infraestrutura tecnológica, equipamentos simples como notebooks comuns e armadilhas fotográficas. Relatórios de difícil interpretação por parte das comunidades.
  - O que o usuário ouve: Demandas por resultados acessíveis vindas de líderes comunitários. Conversas sobre limitações de internet e recursos. Discussões sobre a importância de levar ciência de forma clara para populações locais.
  - O que o usuário diz e faz: Afirma a necessidade de tecnologias acessíveis e práticas. Cobra ferramentas que funcionem offline. Apresenta resultados simplificados para comunidades, tentando aproximar ciência e conservação.
  - O que o usuário pensa e sente: Sente que soluções complexas distanciam a ciência das pessoas. Acredita que simplicidade e acessibilidade ampliam o impacto. Valoriza resultados que possam ser aplicados diretamente em campo.
  - Dores: Falta de internet nas áreas de atuação. Necessidade de equipamentos de alto desempenho que não estão disponíveis. Barreiras na comunicação entre ciência e comunidades.
  - Ganhos: Uso de ferramentas offline em notebooks comuns. Relatórios acessíveis e simplificados. Maior impacto social e ambiental ao aproximar ciência e comunidades.

- Camila Rodrigues, 31 anos
  - O que o usuário vê: Laboratórios acadêmicos, vídeos longos de armadilhas fotográficas, tabelas de dados pouco organizadas. Professores e colegas discutindo hipóteses de pesquisa e cobrando resultados estruturados.
  - O que o usuário ouve: Orientações do orientador sobre a necessidade de análises quantitativas confiáveis. Comentários de colegas sobre a dificuldade de extrair dados de comportamento animal manualmente.
  - O que o usuário diz e faz: Expressa a necessidade de ferramentas com interface clara. Testa diferentes softwares de análise de vídeo. Cobra organização e eficiência para alinhar os dados com sua pesquisa de mestrado.
  - O que o usuário pensa e sente: Sente insegurança diante do excesso de dados e da limitação de ferramentas. Acredita que uma interface gráfica simples pode facilitar sua análise e dar mais confiança aos resultados.
  - Dores: Processos manuais demorados. Falta de ferramentas específicas para extrair dados comportamentais. Dificuldade em exportar informações de forma organizada.
  - Ganhos: Interface intuitiva que permite testar hipóteses com facilidade. Ajuste de níveis de confiança para personalizar análises. Exportação de dados prontos para uso em dissertações e artigos.
 ## Persona Secundária
- João Pedro Martins, 23 anos
  - O que o usuário vê: Ambiente acadêmico de laboratório de computação. Professores, colegas e ferramentas de visão computacional como YOLO, PyTorch e TensorFlow. Exemplos de TCCs anteriores com temas aplicados.
  - O que o usuário ouve: Professores incentivando a aplicar IA em problemas reais. Colegas comentando sobre as dificuldades em conseguir datasets confiáveis. Discussões sobre prazos e banca de TCC.
  - O que o usuário diz e faz: Fala sobre a vontade de aplicar IA em conservação ambiental. Pesquisa artigos, códigos e datasets para treinar modelos. Passa horas testando scripts e ajustando hiperparâmetros.
  - O que o usuário pensa e sente: Sente ansiedade por causa dos prazos do TCC. Tem expectativa de que seu projeto seja útil de verdade e não só teórico. Se sente motivado quando consegue resultados que funcionam em dados reais.
  - Dores: Dificuldade em conseguir vídeos anotados para treinar modelos. Falta de experiência em ecologia para interpretar resultados. Limitação de hardware para treinar redes neurais.
  - Ganhos: Aprender na prática sobre IA aplicada a problemas reais. Um TCC relevante, com impacto positivo no meio ambiente. Possibilidade de abrir portas para pesquisas futuras ou empregos na área.

## Contexto de uso

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
  - Laboratórios de pesquisa com computadores para análise de vídeos e relatórios.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
  - Social: Colaboração entre biólogos, cientistas da computação, estudantes e voluntários.
  - Econômico: Recursos financeiros limitados, necessidade de soluções de baixo custo.
  - Cultural: Conservação da biodiversidade e ao uso de tecnologia pra melhorar o monitoramento da fauna, valorizando tanto o conhecimento científico quanto o local.
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
  - Os vídeos que serão analisados.
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?
  - Pesquisadores ou técnicos acabam de voltar do campo com os vídeos e precisam analisá‑los.


## Jornada do usuário
 
- Mariana Alves recebe os vídeos das armadilhas fotográficas do campo e, quando chega no laboratório, abre o programa pra começar a análise. Em seguida, o sistema inicia a separar os trechos onde aparece um macaco‑prego, mesmo sem internet. Enquanto o programa roda, ela acompanha as detecções na tela em tempo real. Quando termina, o sistema mostra um painel com os resultados e gera relatórios prontos pra usar.

## Qualidade de uso

- Usabilidade:
  - A usabilidade do sistema é fundamental, pois ele deve permitir que pesquisadores e voluntários analisem os vídeos de forma simples, rápida e eficiente, mesmo sem conhecimento técnico avançado. O produto facilita o aprendizado, oferece resultados claros em tempo real e garante a geração de relatórios prontos para uso, reduzindo o esforço necessário e aumentando a satisfação do usuário.
- Experiência de usuário:
  - A experiência do usuário é marcada pela praticidade e confiança, já que o sistema analisa automaticamente os vídeos e apresenta os resultados de forma clara e visual. O usuário acompanha as detecções em tempo real e recebe relatórios prontos, o que gera satisfação, reduz esforço e agiliza o trabalho de pesquisa.
- Acessibilidade:
  - O sistema é simples, intuitivo e não exige conhecimentos técnicos avançados, permitindo que qualquer pesquisador utilize com facilidade.
- Comunicabilidade:
  - As informações são transmitidas de forma clara, com resultados visuais e relatórios objetivos que facilitam a compreensão e a tomada de decisões.  

## Cenário de Problema
- Mariana Alves:
  - A pesquisadora Mariana atua em um ambiente acadêmico e de conservação, onde lida diariamente com grandes quantidades de vídeos coletados em áreas de floresta nativa. Seu contexto é marcado pela pressão por resultados rápidos e precisos, necessários para publicações científicas e relatórios institucionais. A sobrecarga com análises manuais motiva a busca por ferramentas automatizadas que auxiliem na identificação confiável de espécies, permitindo otimizar o tempo e focar em interpretações científicas.
- Lucas Ferreira:
  - O analista de ONG Lucas trabalha em campo e em escritórios de organizações ambientais, em um cenário de recursos limitados e conectividade instável. Sua rotina exige soluções práticas e acessíveis que reduzam o tempo de triagem de imagens e vídeos, garantindo informações ágeis para embasar decisões de conservação e ações de proteção de áreas ameaçadas. Ele precisa de ferramentas que funcionem bem em condições adversas e que sejam simples de utilizar, mesmo por equipes não técnicas.
- Camila Rodrigues:
  - A estudante de pós-graduação Camila está inserida em um contexto de pesquisa acadêmica aplicada, onde os vídeos coletados servem como base para validar hipóteses e produzir conhecimento científico. Ela necessita de métodos que permitam extrair informações de forma intuitiva e confiável, já que dedica grande parte do tempo à análise de dados para compreender padrões de comportamento e ocorrência dos macacos-prego. O uso de tecnologias de IA surge como um diferencial para reduzir esforços manuais e acelerar o desenvolvimento de sua dissertação.
- João Pedro Martins:
  - O estudante de computação João Pedro vive um contexto acadêmico e de inovação tecnológica, onde busca aplicar seus conhecimentos em programação e inteligência artificial a problemas reais. Ele encontra na detecção de macacos-prego uma oportunidade de aprendizado prático e de impacto social, contribuindo diretamente para a conservação da biodiversidade. Seu ambiente é de constante experimentação e testes, em que a motivação vem tanto do desafio técnico quanto da possibilidade de apoiar iniciativas ambientais relevantes. 

<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
## Coleta de dados

## Modelo de tarefas

## Design

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel)
#### Avaliação heurística

### Prtotipação em médio nível (Figma)
#### Avaliação heurística

### Prtotipação em alto nível (React)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
