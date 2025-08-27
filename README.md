# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **DETECÇÃO DE MACACOS-PREGO POR VISÃO COMPUTACIONAL A PARTIR DE VÍDEOS EM AMBIENTES NÃO-CONTROLADOS** sob orientação do Professor **Rafael Testa** e desenvolvido pelos seguintes alunos:

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
   
   - Lucas Ferreira, 28 anos, analista de ONG Ambiental – "Quanto mais acessível a tecnologia, mais impacto podemos gerar em campo"
        - Lucas trabalha em uma ONG que realiza monitoramento participativo de fauna junto a comunidades locais. Muitas vezes atua em áreas sem internet, o que exige ferramentas que funcionem offline. Precisa de uma solução simples e acessível para rodar em notebooks comuns, sem depender de grandes servidores. Valoriza tecnologias que aproximam ciência e comunidades em prol da conservação.
   
   - Camila Rodrigues, 31 anos, mestranda em Ecologia – "Preciso de uma interface clara para testar hipóteses no meu projeto"
        - Camila desenvolve dissertação sobre comportamento de primatas em fragmentos florestais. Ela deseja utilizar vídeos de armadilhas fotográficas para extrair informações quantitativas sobre presença e comportamento dos macacos-prego. Precisa de uma interface gráfica intuitiva, que permita carregar vídeos, ajustar níveis de confiança e exportar dados de forma organizada.

  #### Personas Secundárias
   
   - Pedro Almeida, 27 anos, voluntário ambiental – "Quero ajudar mesmo sem ser especialista"
        - Pedro participa de projetos de conservação como voluntário. Embora não tenha formação em biologia, auxilia na coleta de vídeos em campo e deseja colaborar com a equipe técnica. Para isso, busca ferramentas fáceis de usar, que não exijam conhecimentos avançados, mas que permitam contribuir de forma efetiva no monitoramento da fauna.
    
   - João Pedro Martins, 23 anos, estudante de Ciência da Computação desenvolvendo seu Trabalho de Conclusão de Curso – "Quero aplicar IA em um problema real de conservação"
        - João Pedro está no último semestre de Ciência da Computação e decidiu aplicar visão computacional em um tema de impacto social e ambiental. Ele busca usar o sistema como base para aprender mais sobre aprendizado profundo e aplicar modelos como YOLO em problemas reais. Tem bom domínio de programação em Python, mas pouca experiência prática com ecologia e comportamento animal.

### Mapa de empatia

![Mapa de empatia](empatia.png)

## Persona Primária
- Mariana Alves, 42 anos
  - O que o usuário vê: Laboratórios, armadilhas fotográficas, grandes volumes de vídeos no computador. Outros pesquisadores e alunos trabalhando em análises manuais demoradas. Relatórios científicos que dependem de muito esforço humano.
  - O que o usuário ouve: Conversas de colegas sobre a dificuldade em lidar com tantos dados. Demandas de instituições de conservação por relatórios rápidos e confiáveis. Críticas sobre erros ou atrasos na análise manual.
  - O que o usuário diz e faz: Reclama do tempo perdido em triagens manuais. Procura constantemente novas ferramentas para automatizar processos. Orienta alunos e cobra produtividade científica.
  - O que o usuário pensa e sente: Sente frustração com a lentidão do processo manual. Tem expectativa de que um sistema de IA traga precisão e economia de tempo. Acredita que a tecnologia pode acelerar avanços em conservação.
  - Dores: Volume excessivo de vídeos para analisar. Dificuldade em encontrar ferramentas adaptadas ao contexto de florestas tropicais. Pressão por resultados científicos rápidos.
  - Ganhos: Economia de tempo na análise. Relatórios padronizados e confiáveis. Apoio direto às suas pesquisas e publicações.
 
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
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


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
