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
<img width="500" height="350" alt="image" src="https://github.com/user-attachments/assets/7aa0a5ca-0785-4ece-b459-2fa4dd8237e9" />

2. Os principais concorrentes são o Wildlife Insights, plataforma global de análise em nuvem; o TrapTagger, voltado à anotação colaborativa; e modelos genéricos como YOLOv5 e Faster R-CNN, amplamente usados em visão computacional.
<img width="500" height="350" alt="image" src="https://github.com/user-attachments/assets/96edb4be-b5d8-47ec-9a2b-6fdcbcf17d05" />

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
- Lucas Ferreira leva seu notebook para comunidades locais onde a ONG atua e carrega os vídeos coletados em campo. Ele abre o programa e, mesmo sem conexão à internet, o sistema começa a identificar automaticamente os macacos-prego. Durante a análise, Lucas mostra os resultados para os moradores, aproximando ciência e comunidade. Ao final, exporta relatórios simples e acessíveis para compartilhar com a equipe da ONG.
- Camila Rodrigues organiza os vídeos das armadilhas fotográficas para sua pesquisa de mestrado e abre o programa no laboratório. Ela ajusta os parâmetros de confiança da detecção para refinar os resultados e acompanha as marcações feitas pelo sistema em tempo real. Após a análise, exporta os dados quantitativos já organizados em tabelas, que serão usados para testar hipóteses sobre o comportamento dos macacos-prego em diferentes fragmentos florestais.

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

## Questões para Refinamento de cenários

### Mariana Alves

1. Por que Mariana precisa automatizar a detecção de macacos-prego em vídeos de floresta nativa?  
2. Que resultados ela espera do sistema (identificação de espécie, tempo economizado, precisão mínima)?  
3. Quais metadados são necessários para treinar e validar o modelo (rótulos de espécie, localização, horário)?  
4. Em quais ambientes e servidores o sistema será executado?  
5. Qual qualidade mínima dos vídeos (resolução, iluminação) que ela consegue obter no campo?  
6. Que ferramentas acadêmicas já fazem parte do fluxo de trabalho dela?  
7. Quais são os prazos e pressões de entrega de resultados?  
8. Quem carrega e anota os vídeos para análise?  
9. Quem valida as detecções e quem é notificado dos resultados?  
10. Como ela ajusta parâmetros de modelo e configurações de detecção?  
11. Que modos de execução (local, nuvem, em lote) ela precisa?  
12. Como ela avalia a confiabilidade dos resultados e documenta para relatórios?

---

### Lucas Ferreira

1. Por que Lucas precisa acelerar a triagem de vídeos em campo e escritório?  
2. Qual nível de confiabilidade ele exige para suporte a decisões urgentes?  
3. Que metadados (GPS, hora) são essenciais para as análises de campo?  
4. Quais dispositivos e recursos ele utiliza em campo (smartphone, laptop com bateria limitada)?  
5. Como lidar com conexão de internet intermitente ou inexistente?  
6. Quais condições ambientais afetam a qualidade dos vídeos (chuva, neblina)?  
7. Quem faz o upload e coleta os vídeos e qual o nível técnico da equipe?  
8. Quem consome as informações geradas e precisa ser alertado de espécies críticas?  
9. Que estratégias de pré-seleção ou análise alternativa ele explora?  
10. Quais modos de processamento (local vs. remoto) e como ele decide entre eles?  
11. Que falhas podem ocorrer em campo e como ele contorna?  
12. Como ele valida a precisão em campo e reporta os resultados?

---

## Camila Rodrigues

1. Por que Camila precisa de uma ferramenta intuitiva para extrair padrões de ocorrência?  
2. Quais hipóteses ela testa com a detecção automática?  
3. Que atributos de saída (número de aparições, períodos de atividade) são gerados?  
4. Que interfaces gráficas ou notebooks ela prefere?  
5. Qual qualidade dos vídeos coletados e restrições de formato?  
6. Quais prazos de defesa e submissão ela enfrenta?  
7. Quem importa e anota vídeos e revisa os resultados?  
8. Que estratégias de visualização de dados ela quer aplicar?  
9. Como define filtros de qualidade e sensibilidade do modelo?  
10. Quais modos de execução (script, GUI) atendem melhor seu uso?  
11. Que problemas técnicos podem surgir e como contorná-los?  
12. Como ela valida métricas (recall, precisão) e documenta para a dissertação?

---

### João Pedro Martins

1. Por que João Pedro quer aplicar IA na detecção de macacos-prego?  
2. Que aprendizado prático (Python, TensorFlow, pipeline CI/CD) ele busca com o projeto?  
3. Que saídas técnicas (modelos treinados, documentação de código) são geradas?  
4. Em quais máquinas (desktop da universidade, servidor de GPU) ele testa o sistema?  
5. Que ferramentas de desenvolvimento (VS Code, Git, Docker) já estão instaladas?  
6. Como ele lida com limites de memória e processamento?  
7. Quem submete pull requests ou issues no repositório de código?  
8. Que decisões de arquitetura (microserviços vs. monolito) ele precisa tomar?  
9. Em que ordem cria testes unitários, documenta a API e implementa a detecção?  
10. Quais modos (debug vs. produção) ele implementa?  
11. Quais falhas técnicas devem ser previstas e como tratá-las?  
12. Como ele verifica performance e documenta benchmarks para o portfólio?

## Cenários de Problema com Referência às Perguntas

---

### Mariana Alves

Mariana Alves:  
A pesquisadora Mariana Alves atua em um ambiente acadêmico e de conservação, lidando diariamente com grandes quantidades de vídeos coletados em áreas de floresta nativa [1]. Seu contexto é marcado pela pressão por resultados rápidos e precisos, tanto para publicações científicas quanto para relatórios institucionais [7]. A sobrecarga com análises manuais motiva a busca por ferramentas automatizadas que auxiliem na identificação confiável de macacos-prego, reduzindo o tempo gasto em triagens e garantindo uma precisão mínima aceitável para validação científica [2]. Para isso, ela depende de metadados como rótulos de espécie, localização e horário, fundamentais no treinamento e validação dos modelos de detecção [3].

O sistema deve ser executado em laboratórios de pesquisa, em computadores institucionais ou servidores locais [4], e precisa se adaptar à qualidade variável dos vídeos coletados em campo, que muitas vezes apresentam limitações de resolução e iluminação [5]. Mariana já utiliza ferramentas acadêmicas em seu fluxo de trabalho, como softwares estatísticos e de análise de dados [6], e busca integrar a solução a esse ecossistema. Os prazos curtos de entrega de relatórios aumentam a pressão, fazendo com que alunos e técnicos participem do carregamento e anotação dos vídeos para análise [8], enquanto a validação final das detecções e notificações de resultados fica sob sua responsabilidade [9].

Além disso, Mariana precisa de flexibilidade para ajustar parâmetros do modelo e configurações de detecção de acordo com o contexto da pesquisa [10], podendo executar o sistema localmente, em nuvem ou em lotes de vídeos extensos [11]. Por fim, avalia a confiabilidade dos resultados comparando com observações manuais e documenta todas as análises em relatórios padronizados, garantindo transparência e reprodutibilidade científica [12].

---

### Lucas Ferreira

Lucas Ferreira:  
Lucas Ferreira atua como analista em uma ONG ambiental que realiza monitoramento participativo de fauna em parceria com comunidades locais. Ele precisa acelerar a triagem de vídeos tanto em campo quanto no escritório, já que o volume de dados coletados é muito alto para ser revisado manualmente [1]. Por lidar com decisões urgentes relacionadas à conservação, exige um nível de confiabilidade elevado, mesmo que em alguns casos os resultados sirvam apenas como alerta preliminar [2]. Para que as análises façam sentido, é essencial o uso de metadados básicos como GPS e horário de captura, que ajudam a contextualizar os registros de espécies [3].

No campo, Lucas utiliza principalmente smartphones e laptops simples, muitas vezes com bateria limitada, o que exige soluções leves e otimizadas [4]. Outro desafio é a conexão de internet intermitente ou inexistente em áreas remotas, o que torna fundamental que o sistema funcione de modo totalmente offline [5]. Além disso, condições ambientais como chuva, neblina e baixa iluminação comprometem a qualidade dos vídeos e aumentam a dificuldade das detecções [6].

A coleta e upload dos vídeos normalmente são feitos por técnicos e voluntários com nível técnico variado, o que demanda uma interface simples e intuitiva [7]. As informações processadas precisam ser consumidas rapidamente por gestores e equipes de campo, especialmente quando espécies críticas são detectadas [8]. Para contornar limitações, Lucas explora estratégias de pré-seleção de vídeos e análises alternativas que reduzam a sobrecarga de dados [9]. Ele pode decidir entre processamento local em notebooks ou remoto em servidores, dependendo da urgência e da infraestrutura disponível [10].

Entre as falhas possíveis estão problemas de energia, arquivos corrompidos e interrupções inesperadas, que ele contorna com backups e execuções em etapas menores [11]. Por fim, Lucas valida a precisão das análises cruzando os resultados com observações de campo e reporta as informações de forma clara para a equipe e parceiros da ONG, garantindo que o trabalho tenha impacto direto nas ações de conservação [12].

---

### Camila Rodrigues

Camila Rodrigues:  
Camila Rodrigues é mestranda em Ecologia e precisa de uma ferramenta intuitiva que facilite a extração de padrões de ocorrência de macacos-prego em vídeos, sem exigir conhecimentos avançados em programação [1]. Suas hipóteses de pesquisa envolvem testar relações entre presença dos animais e fatores ambientais, além de identificar variações no comportamento em diferentes fragmentos florestais [2]. Para isso, o sistema deve gerar atributos de saída como número de aparições, períodos de atividade e frequência relativa em determinados locais [3]. Ela prefere utilizar interfaces gráficas claras e organizadas, mas também tem familiaridade com notebooks acadêmicos que possibilitam maior flexibilidade na análise [4].

Os vídeos coletados em campo apresentam qualidade variável, com diferentes resoluções e formatos, o que exige que o sistema seja capaz de lidar com tais restrições [5]. Camila enfrenta prazos rígidos de defesa e submissão de artigos científicos, o que aumenta sua dependência de ferramentas que economizem tempo [6]. Normalmente, alunos auxiliares ajudam a importar e anotar vídeos, mas a revisão dos resultados fica sob responsabilidade da própria pesquisadora [7]. Ela também deseja aplicar estratégias de visualização de dados, como gráficos de frequência temporal e mapas de calor de atividade [8].

Para refinar suas análises, define filtros de qualidade e ajusta a sensibilidade do modelo conforme o contexto experimental [9]. Modos de execução tanto por interface gráfica (GUI) quanto por scripts são relevantes, dependendo da etapa do trabalho — a GUI para triagens rápidas e scripts para análises reprodutíveis [10]. Entre os problemas técnicos mais comuns estão incompatibilidades de formato de vídeo e limitações de hardware, que ela contorna convertendo arquivos e utilizando versões reduzidas de dados [11]. Por fim, Camila valida métricas como recall e precisão, documentando os resultados de forma padronizada para sua dissertação e publicações científicas [12].

---

### João Pedro Martins

João Pedro Martins:  
O estudante de computação João Pedro vive um contexto acadêmico e de inovação tecnológica, onde busca aplicar seus conhecimentos em programação e inteligência artificial a problemas reais[1][2]. Ele encontra na detecção de macacos-prego uma oportunidade de aprendizado prático e de impacto social, contribuindo diretamente para a conservação da biodiversidade[3]. Seu ambiente é de constante experimentação e testes, em que a motivação vem tanto do desafio técnico quanto da possibilidade de apoiar iniciativas ambientais relevantes[4][5][8].

---

# Análise de Tarefas
## HTA

### 1. Carregar vídeo
O usuário seleciona o arquivo no computador e realiza o upload para o sistema iniciar a análise.
<img width="684" height="426" alt="image" src="https://github.com/user-attachments/assets/9d55867b-9774-4e9f-a891-62f644a33780" />

### 2. Ajustar parâmetros de análise
O pesquisador pode configurar a confiança mínima e a taxa de frames a processar para equilibrar precisão e desempenho.

<img width="579" height="350" alt="image" src="https://github.com/user-attachments/assets/afbb944c-7c2b-45eb-a85a-820baf31c61c" />

### 3. Executar processamento automático
O sistema processa os vídeos usando IA, destacando os trechos relevantes e mostrando as detecções.
<img width="561" height="349" alt="image" src="https://github.com/user-attachments/assets/ac78f88f-587e-484f-9f92-da7289d67261" />

### 4. Validar resultados
O usuário revisa os resultados, podendo ajustar parâmetros e repetir a análise se necessário.
<img width="553" height="349" alt="image" src="https://github.com/user-attachments/assets/2f13c57f-5d9f-43d5-9f97-303b76166506" />

### 5. Gerar relatórios
Ao final, o sistema gera saídas organizadas para pesquisa e documentação científica.
<img width="598" height="353" alt="image" src="https://github.com/user-attachments/assets/99d3fbc6-fedc-4fd9-80e7-df8ff0ed3a12" />

## GOMS

### GOMS – Goals, Operators, Methods, Selection Rules
- GOAL 0: Obter relatório automatizado de presença de macacos-prego
  - GOAL 1: Carregar vídeo
    - METHOD 1.A: Selecionar arquivo pelo explorador de arquivos
    - RULE: O sistema deve permitir seleção de arquivo somente em formatos de vídeo suportados. Se o usuário tentar carregar arquivo inválido, exibir aviso e bloquear o carregamento.
      - OP. 1.A.1: Clicar em “Carregar vídeo”
      - OP. 1.A.2: Navegar até pasta do vídeo
      - OP. 1.A.3: Selecionar arquivo e confirmar

  - GOAL 2: Ajustar parâmetros de detecção
    - METHOD 2.A: Usar sliders na interface
    - RULE: Se usuário não domina ajustes → manter padrão automático
      - OP. 2.A.1: Arrastar barra de confiança
      - OP. 2.A.2: Selecionar taxa de frames


  - GOAL 3: Rodar análise
    - METHOD 3.A: Pressionar botão “Iniciar análise”
    - RULE: O botão “Iniciar análise” deve ficar desabilitado enquanto nenhum vídeo válido estiver carregado ou se os parâmetros estiverem fora do intervalo aceitável.
      - OP. 3.A.1: Sistema processa vídeo e mostra detecções

  - GOAL 4: Exportar resultados
    - METHOD 4.A: Gerar PDF automático
    - RULE: Se o relatório é para artigo científico, o sistema deve gerar PDF formatado automaticamente com visualização prévia
    - METHOD 4.B: Exportar tabela CSV
    - RULE: Se relatório é para artigo científico → usar PDF; se para dados brutos → usar CSV

## CTT
<img width="1084" height="358" alt="image" src="https://github.com/user-attachments/assets/e194fc50-f1d6-4770-aa0e-a6f76efcec55" />

<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->

## Prototipação no Papel
### Tela 1 (inicial)
<img width="850" height="500" alt="image" src="https://github.com/user-attachments/assets/a28a8a67-9906-4869-84e3-cbb84e647a8c" />

### Tela 2 (Detecção)
<img width="850" height="500" alt="image" src="https://github.com/user-attachments/assets/5050b029-1483-46bc-941d-fd244c59b645" />

### Tela 3 (Relatórios)
<img width="850" height="500" alt="image" src="https://github.com/user-attachments/assets/23a24630-ecf6-4371-82b0-b02b3799fb18" />

## Coleta de dados

### O quê coletar
  - Perfil do usuário (formação, experiência com tecnologia e com pesquisa em biodiversidade).
  - Necessidades e dificuldades na análise manual de vídeos.
  - Expectativas quanto à precisão, tempo de processamento e formato dos relatórios.
  - Contexto de uso (laboratórios, campo, limitações de internet e hardware).

### De quem coletar
  - Pesquisadores em biologia da conservação.
  - Analistas de ONGs ambientais.
  - Estudantes de graduação e pós-graduação que utilizam armadilhas fotográficas.
  - Voluntários que apoiam na coleta de vídeos em campo.

### Ferramenta de coleta 1: Entrevistas semiestruturadas
- Aplicar entrevistas diretas com pesquisadores e analistas para compreender fluxos de trabalho, expectativas e dores no processo de análise manual.
- https://docs.google.com/forms/d/e/1FAIpQLSfZrrq_-NfbNGAO497ap6I9EhPsqOuGPozMW2mywfHzl6af7A/viewform?usp=header
  

### Ferramenta de coleta 2: Questionários online
- Enviar questionários padronizados para um público maior (estudantes e voluntários), coletando informações rápidas sobre uso de tecnologia e necessidades de interface.
- https://docs.google.com/forms/d/e/1FAIpQLSfs7E9kJ7AejVE4HzPGKwOsa9dSuY1-Ww9z0aSumbGP_MyC1w/viewform?usp=dialog
    
### Ferramenta de coleta 3: Observação em campo / estudos de campo
- Acompanhar usuários no processo de coleta e análise de vídeos, observando limitações práticas (internet, bateria, iluminação) e como lidam com os dados antes da análise automatizada.

### Aspectos éticos
- Consentimento livre e esclarecido.
- Garantia de anonimato e confidencialidade dos dados.
- Participação voluntária com possibilidade de desistir a qualquer momento.

# Ciclo de Vida de Usabilidade
## Características da Plataforma

### Descrição de software e hardware
| **Item**     | **Descrição**                                                                                                                                                                                                                                                                                                                   |
| ------------ | -------------------------------------------------- |
| **Hardware** | **PC1:** Ryzen 7 5700x (8 núcleos / 16 threads / 3.4 GHz), RAM: 32 GB, GPU: RTX 4060 (8 GB VRAM) <br> **PC2:** Ryzen 9 5900x (12 núcleos / 24 threads / 3.3 GHz), RAM: 32 GB, GPU: RTX 4070 Ti (12 GB VRAM) <br> **PC3:** Notebook i7 (10ª geração), 16 GB RAM, GPU dedicada GTX 1660 (6 GB VRAM) – usado em análises de campo. |
| **Software** | **Interface (UI):** customTkinter <br> **Linguagem:** Python 3.10 <br> **Bibliotecas principais:** YOLOv8 (Ultralytics), OpenCV, TensorFlow 2.19.0, customTkinter, pandas, numpy. <br> **Sistema Operacional:** compatível com Windows e Linux.     |

### Capacidades da plataforma
| **Capacidade**                             | **Justificativa**                                                                                          |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| Suporte a vídeos em alta resolução (≥720p) | Necessário para garantir detecções mais precisas de macacos-prego em ambientes de floresta.                |
| Execução offline                           | Essencial para uso em campo, onde o acesso à internet é limitado ou inexistente.                           |
| Placa de vídeo dedicada                    | Fundamental para aceleração de inferência e redução do tempo de análise.                                   |
| Exportação automática de relatórios        | Facilita o uso acadêmico e institucional, gerando documentos prontos para publicação ou relatório técnico. |

### Restrições da plataforma
| **Restrição**                                    | **Justificativa**                                                                                                            |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Dependência de hardware intermediário            | O processamento de vídeo e IA exige desempenho acima de notebooks básicos, especialmente para longas gravações.              |
| Qualidade mínima de vídeo (720p, boa iluminação) | Baixa iluminação ou ruídos visuais comprometem o reconhecimento de animais e aumentam falsos positivos.                      |
| Tempo de processamento dependente da GPU         | Quanto maior o número de vídeos e resolução, maior o tempo de inferência; otimizações são necessárias para análises em lote. |

## Princípios Gerais do Projeto
| **Princípio**            | **Descrição no contexto do projeto**                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| **Simplicidade**         | A interface contém apenas as funções essenciais: carregar vídeo, iniciar análise, visualizar resultados e exportar relatórios. |
| **Consistência**         | Ícones, termos e fluxos são padronizados (ex.: “Iniciar análise”, “Exportar PDF”).                                             |
| **Feedback imediato**    | O sistema mostra o progresso e as detecções em tempo real.                                                                     |
| **Prevenção de erros**   | Mensagens de confirmação antes de reprocessar vídeos ou excluir dados.                                                         |
| **Flexibilidade**        | Ajuste de parâmetros de confiança e taxa de frames acessível a todos os perfis de usuário.                                     |
| **Eficiência e rapidez** | O modelo YOLOv8s garante detecção precisa em tempo reduzido.                                                                   |
| **Apoio à aprendizagem** | Interface autoexplicativa, com feedback visual e textual para guiar o usuário.                                                 |

## Metas de Usabilidade
| **Metas**                  | **Porcentagem** | **Justificativa**                                                                                                              |
| -------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Facilidade de uso**      | **40%**         | A interface deve ser intuitiva e simples, permitindo que pesquisadores e voluntários operem o sistema sem treinamento técnico. |
| **Precisão da detecção**   | **30%**         | A identificação automática dos macacos-prego deve ser confiável para evitar erros em relatórios científicos.                   |
| **Tempo de processamento** | **20%**         | A análise deve ocorrer de forma rápida, reduzindo significativamente o tempo em relação à triagem manual.                      |
| **Interface responsiva**   | **10%**         | A interface deve se adaptar bem a diferentes tamanhos de tela e manter o desempenho em equipamentos de campo.                  |


## Cenário de Interação
### Cenário

Cenário de problema: Detecção automatizada de macacos-prego (Sapajus spp.) em vídeos de armadilhas fotográficas para pesquisas de conservação da fauna.

Atores: Mariana Alves (pesquisadora), Lucas Ferreira (analista ambiental), Camila Rodrigues (mestranda em Ecologia). 

Durante o processo de monitoramento da fauna em áreas de floresta nativa, pesquisadores e técnicos coletam centenas de vídeos por meio de armadilhas fotográficas [1]. Ao retornar ao laboratório, Mariana Alves, pesquisadora principal, inicia o sistema de detecção automatizada. Ela carrega as pastas com os vídeos e define os parâmetros de confiança do modelo [2]. O sistema começa o processamento, detectando a presença de macacos-prego em tempo real e exibindo caixas delimitadoras sobre cada detecção [3].

Enquanto o sistema roda, Lucas Ferreira, analista de uma ONG parceira, utiliza sua versão offline em campo para processar vídeos recentes coletados por comunidades locais [4]. Ele acompanha as notificações de detecções e exporta relatórios compactos com coordenadas GPS e horários de ocorrência [5]. A versão offline permite que o trabalho continue mesmo sem acesso à internet, garantindo decisões rápidas em ações de conservação.

No laboratório, Camila Rodrigues, mestranda em Ecologia, carrega os resultados processados e realiza análises comparativas. Ela ajusta a sensibilidade do modelo para refinar o reconhecimento e aplica filtros de tempo e local para extrair padrões de atividade [6]. O sistema gera automaticamente gráficos e tabelas com frequência de aparições, além de permitir exportação dos resultados para CSV e PDF [7].

Durante o uso, o sistema detecta vídeos com iluminação insuficiente e emite alertas, sugerindo correção automática de brilho e contraste [8]. Também notifica os usuários sobre arquivos corrompidos ou vídeos duplicados [9]. Após o processamento, um relatório consolidado é gerado e enviado automaticamente a todos os colaboradores do projeto [10].

A equipe revisa os resultados e valida manualmente amostras com baixa confiança. O sistema registra as revisões, atualiza os metadados e armazena o dataset final no servidor institucional [11]. Por fim, um aviso é enviado aos responsáveis por campo e laboratório, confirmando a conclusão da análise e a disponibilidade dos relatórios [12].

Concluída a validação do dataset, o sistema envia uma notificação automática para Mariana e para todos os participantes envolvidos, confirmando que seus vídeos foram oficialmente incluídos no dataset final e que os resultados podem ser utilizados para análises e publicações [13].

### Perguntas de cenário

1. Quem pode/deve iniciar o processo de análise e cadastro dos vídeos no sistema?
2. Quando e onde os vídeos são processados e armazenados (laboratório ou campo)?
3. Quem fornece os dados de vídeo e metadados de localização ao sistema?
4. Quais informações (frames, horários, coordenadas, nível de confiança) devem ser armazenadas nos resultados finais?
5. Quantas análises podem ser executadas simultaneamente e em quais modos (local, offline ou em nuvem)?
6. Quem pode supervisionar e validar os resultados das detecções?
7. Que informações são necessárias para cadastrar uma nova coleta de vídeos no sistema?
8. Como o sistema processa, exibe e atualiza as detecções durante a execução?
9. De quem depende a aprovação e validação final dos resultados?
10. Que alertas e feedbacks o sistema deve emitir para indicar problemas (iluminação, arquivos corrompidos, baixa confiança)?
11. Como o sistema pode ajustar automaticamente parâmetros de detecção e qualidade de imagem?
12. Em que pontos a interação entre usuários e sistema pode ser mais eficiente?
13. Quem precisa ser notificado da conclusão das análises e da geração dos relatórios?

### Design Centrado na Comunicação

| **Tópico > Subtópico (diálogo)** | **Falas e Signos** |
| -------------------------------- | ------------------ |
| **Carregar vídeos**              | **U:** Quero carregar os vídeos das armadilhas fotográficas para análise. <br> **D:** Certo. Deseja selecionar os arquivos de uma pasta local ou de um dispositivo externo? <br> **U:** De uma pasta local. <br> **D:** Arquivos importados com sucesso. Foram encontrados 24 vídeos válidos.                                                       |
| **Configurar análise**           | **U:** Quero ajustar a sensibilidade da detecção. <br> **D:** Qual nível de confiança deseja aplicar? (baixa, média ou alta) <br> **U:** Alta, para evitar falsos positivos. <br> **D:** Configuração salva. Detecção configurada para confiança ≥ 0.85.                                                                                            |
| **Iniciar processamento**        | **U:** Pode começar a análise dos vídeos? <br> **D:** Claro. A análise será executada em modo offline. Deseja visualizar as detecções em tempo real? <br> **U:** Sim, quero acompanhar. <br> **D:** Iniciando... Exibindo quadros processados e detecções de macacos-prego destacadas.                                                              |
| **Acompanhar resultados**        | **U:** Quantas detecções já foram feitas? <br> **D:** Até agora, 37 detecções em 12 vídeos. Confiabilidade média: 91%. <br> **U:** Algum vídeo apresentou problema? <br> **D:** Um vídeo foi ignorado por baixa iluminação. Deseja aplicar correção automática de brilho? <br> **U:** Sim. <br> **D:** Correção aplicada, vídeo reinserido na fila. |
| **Gerar relatório**              | **U:** Quero gerar um relatório com as ocorrências detectadas. <br> **D:** Deseja incluir gráficos de horários e frequência? <br> **U:** Sim, inclua tudo. <br> **D:** Relatório gerado com sucesso. Arquivo salvo em formato PDF e CSV.                                                                                                            |
| **Exportar dados**               | **U:** Preciso exportar os resultados para o banco de dados da pesquisa. <br> **D:** Selecione o formato desejado (CSV, JSON ou Excel). <br> **U:** CSV. <br> **D:** Exportação concluída. Os dados estão prontos para upload institucional.                                                                                                        |
| **Encerrar sessão**              | **U:** Quero encerrar o programa. <br> **D:** Deseja salvar as configurações atuais como padrão para futuras análises? <br> **U:** Sim, salve como “Análise Alta Confiança”. <br> **D:** Perfil salvo e sessão encerrada com sucesso.                                                                                                               |

### Mapa de Objetivos

| **Tipo de Objetivo**      | **Formulação**                                                                                                                                             |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Final**                 | Contribuir para a conservação da fauna e a pesquisa científica por meio da automação na detecção de macacos-prego em vídeos de armadilhas fotográficas.    |
| **Instrumental**          | Automatizar o processo de análise de vídeos para reduzir o tempo de triagem e aumentar a precisão na identificação das espécies.                           |
| **Instrumental Direto**   | Utilizar o sistema para carregar vídeos, processar as imagens, visualizar as detecções e gerar relatórios de ocorrência.                                   |
| **Instrumental Indireto** | Oferecer uma interface intuitiva, funcionamento offline e compatibilidade com hardware de campo para facilitar o uso por pesquisadores, estudantes e ONGs. |


### Esquema Conceitual de Signos

**Analisar vídeos (A)** – funcionalidade de processamento e detecção de macacos-prego

| signo | origem | observações |
|--------|---------|--------------|
| vídeos carregados | domínio | indica a quantidade de vídeos importados para análise; quanto mais vídeos, maior a robustez do dataset |
| nível de confiança | domínio | representa o parâmetro de sensibilidade do modelo; valores altos reduzem falsos positivos |
| detecções realizadas | domínio | indica o número de ocorrências de macacos-prego detectadas até o momento |
| vídeos com problema | domínio | mostra vídeos com falhas, baixa iluminação ou corrompidos, sinalizando rupturas na comunicação |
| correção aplicada | domínio | indica que ajustes automáticos (como brilho e contraste) foram realizados com sucesso |
| relatório gerado | domínio | representa o fechamento do processo de análise e consolidação dos resultados |
| exportação concluída | domínio | mostra que os dados foram enviados para o repositório institucional ou salvos em arquivo |
| sessão encerrada | domínio | indica o término do processo e salvamento das configurações personalizadas |

---

**Gerar relatório (R)** – funcionalidade de síntese e exportação de resultados

| signo | origem | observações |
|--------|---------|--------------|
| resumo de detecções | domínio | apresenta estatísticas consolidadas (número de detecções, confiabilidade média, vídeos processados) |
| gráficos de atividade | domínio | representa visualmente padrões de ocorrência temporal e espacial dos macacos-prego |
| exportar formato | domínio | permite escolher entre CSV, JSON ou PDF conforme a necessidade da pesquisa |
| relatório final salvo | domínio | indica que o arquivo foi criado e armazenado com sucesso no sistema |

---

**Validar resultados (V)** – funcionalidade de revisão e confirmação de detecções

| signo | origem | observações |
|--------|---------|--------------|
| amostras revisadas | domínio | representa a quantidade de vídeos analisados manualmente para validar o modelo |
| baixa confiança | domínio | sinaliza detecções incertas que precisam de revisão humana |
| metadados atualizados | domínio | indica que os dados corrigidos foram incorporados ao dataset final |
| validação concluída | domínio | mostra que o processo foi encerrado e os resultados estão prontos para publicação |


## Molic

### Sistema total
<img width="589" height="806" alt="image" src="https://github.com/user-attachments/assets/da7aaa6e-5a4e-4e9e-a2c6-64904a61b1f4" />

## Figma

### Tela inicial
<img width="1204" height="826" alt="image" src="https://github.com/user-attachments/assets/b74a1175-bdde-4642-b7c8-e9c4518d489b" />

### Tela de detecção
<img width="1209" height="888" alt="image" src="https://github.com/user-attachments/assets/f33f598e-93fc-4050-ad91-49f263797bdd" />
<img width="1208" height="890" alt="image" src="https://github.com/user-attachments/assets/4c080a93-44f4-467a-8d0f-7a201705deb2" />

### Tela de Relatórios
<img width="1206" height="889" alt="image" src="https://github.com/user-attachments/assets/f0751873-8f1b-4ec4-a579-a2faec96ea53" />

## Planejamento da Avaliação

### Planejamento de Usabilidade

| Etapa | Planejamento aplicado ao projeto de detecção de macacos-prego |
|-------|----------------------------------------------------------------|
| **D** | Avaliar a apropriação da tecnologia por pesquisadores e ONGs.<br>Verificar se a interface permite análise eficiente de vídeos em campo e laboratório. |
| **E**| - Os usuários conseguiram carregar e analisar vídeos sem ajuda?<br>- A interface foi compreendida sem treinamento prévio?<br>- Os relatórios gerados foram úteis para tomada de decisão?<br>- O sistema funcionou bem em ambientes offline?<br>- Houve sugestões de melhoria ou dificuldades recorrentes? |
| **C** | - Avaliação heurística (baseada em Nielsen)<br>- Testes com usuários reais (pesquisadores, analistas de ONG, mestrandos)<br>- Questionários pré e pós-teste<br>- Observação direta e coleta de métricas |
| **I**| - Sessões presenciais e remotas com vídeos reais de armadilhas fotográficas<br>- Equipamentos com e sem GPU<br>- Participantes com diferentes níveis de familiaridade com IA e visão computacional |
| **D**| - Garantir anonimato dos participantes<br>- Permitir pausas, saída livre e conforto durante a sessão<br>- Termo de consentimento assinado<br>- Nenhum dado sensível será armazenado |
| **E** | - Consolidar problemas de usabilidade por frequência e gravidade<br>- Identificar heurísticas violadas<br>- Gerar recomendações de redesign<br>- Validar melhorias com nova rodada de testes |


---

### Lista de Instrumentos
   1) Termo de consentimento  
   2) Questionários  
   3) Tabela de Observação  
   4) Formulário de avaliação Heuristica.


## Avaliação de IHC através de inspeção HEURÍSTICA

### Tabela 1 - Conjunto de heurísticas de Nielsen (1994)

| 1. | Visibilidade do status do sistema: |
| :---- | :---- |
| O sistema deve sempre manter os usuários informados sobre o que está acontecendo através de feedback apropriado, em um tempo razoável. | **3** - Ausência de barra de progresso durante processamento. |
| 2. | Compatibilidade entre sistema e mundo real: |
| O sistema deve utilizar a linguagem do usuário, com palavras, frases e conceitos familiares para ele, ao invés de termos específicos de sistemas. Seguir convenções do mundo real, fazendo com que a informação apareça em uma ordem lógica e natural. | **2** - Termos técnicos (ex.: "YOLOv8s", "confidence threshold") exibidos sem explicação ou glossário. |
| 3. | Controle e liberdade para o usuário: |
| Estão relacionados à situação em que os usuários frequentemente escolhem as funções do sistema por engano e então necessitam de "uma saída de emergência” claramente definida para sair do estado não desejado sem ter que percorrer um longo diálogo, ou seja, é necessário suporte a *undo* e *redo*. | **3** - Ausência de botão "Cancelar" para interromper análise em andamento. |
| 4. | Consistência e padrões: |
| Referem-se ao fato de que os usuários não deveriam ter acesso a diferentes situações, palavras ou ações representando a mesma coisa. A interface deve ter convenções não-ambíguas. | **2** - Terminologia inconsistente ("Salvar", "Gravar", "Exportar") usada alternadamente. |
| 5. | Prevenção de erros: |
| Os erros são as principais fontes de frustração, ineficiência e ineficácia durante a utilização do sistema. | **4** - Upload aceita formatos não suportados ou arquivos corrompidos sem validação. |
| 6. | Reconhecimento em lugar de lembrança: |
| Tornar objetos, ações, opções visíveis e coerentes. O usuário não deve ter que lembrar informações de uma parte do diálogo para outra. Instruções para o uso do sistema devem estar visíveis ou facilmente acessíveis. | **2** - Falta de legendas e tooltips para bounding boxes, filtros e controles avançados. |
| 7. | Flexibilidade e eficiência de uso: |
| A ineficiência nas tarefas pode reduzir a eficácia do usuário e causar-lhes frustração. O sistema deve ser adequado tanto para usuários inexperientes quanto para usuários experientes. | **2** - Ausência de processamento em lote, presets e atalhos de teclado para usuários avançados. |
| 8. | Projeto minimalista e estético: |
| Os diálogos não devem conter informações irrelevantes ou raramente necessárias. Cada unidade extra de informação em um diálogo compete com unidades relevantes e diminui sua visibilidade relativa. | **1** - Tela de Relatórios com excesso de opções e texto sem hierarquia visual clara. |
| 9. | Auxiliar os usuários a reconhecer, diagnosticar e recuperar erros: |
| Mensagens de erro devem ser expressas em linguagem natural (sem códigos), indicando precisamente o erro e sugerindo uma solução. | **4** - Mensagens de erro genéricas sem orientação. |
| 10. | Ajuda e documentação: |
| Mesmo que seja melhor que o sistema possa ser usado sem documentação, pode ser necessário fornecer ajuda e documentação. Tais informações devem ser fáceis de encontrar, ser centradas na tarefa do usuário, listar passos concretos a serem seguidos e não ser muito grandes. A ajuda deve estar facilmente acessível e on-line. | **2** - Ajuda limitada ao manual curto integrado; falta de tutoriais rápidos, walkthroughs e exemplos contextuais.

---

### Tabela 2 - Grau de severidade dos problemas de usabilidade

| Nível | Descrição |
|---:|---|
| 0 | Sem importância; não afeta operação |
| 1 | Cosmético; baixa prioridade |
| 2 | Simples; corrigível em baixa prioridade |
| 3 | Grave; alta prioridade de correção |
| 4 | Catastrófico; corrigir antes do lançamento |

---

| Heurística atendida | Exemplo (tela/elemento) | Justificativa |
|---|---:|---|
| Compatibilidade com o mundo real | Tela de Detecção; metadados do vídeo (timestamp; GPS; nome do arquivo) visíveis | Usa termos e informações familiares aos pesquisadores; mapeia dados do mundo real para a interface |
| Reconhecimento em lugar de lembrança | Tela Inicial; painel "Histórico de Análises" com últimos thresholds e presets visíveis | Permite reutilizar parâmetros sem memorizar; reduz carga cognitiva e acelera tarefas recorrentes |


## Método de Avaliação de Usabilidade baseado em Observação do Usuário

### Lista de tarefas que o usuário deve cumprir
- Tarefa 1: Carregar uma imagem no sistema (botão ou drag-and-drop)
- Tarefa 2: Selecionar uma imagem do histórico para visualizar resultados
- Tarefa 3: Interpretar os resultados exibidos (detecção e score)
- Tarefa 4: Clicar em Iniciar Detecção e verificar atualização dos resultados
- Tarefa 5: Gerar relatório da detecção e confirmar entrada na tabela de relatórios
- Tarefa 6: Clicar em Visualizar para abrir a imagem do animal detectado.
- Tarefa 7: Voltar à tela inicial e fechar o sistema corretamente


### Formulário de perfil do usuário

### Avaliação de cada Tarefa — Usuário 1

| Tarefa | Grau de Sucesso | Total de Erros cometidos | Tipos de Erros | Tempo Necessário | Grau de Satisfação |
|---|---:|---:|---|---:|---|
| Tarefa 1: Carregar uma imagem no sistema | Sucesso Total | 0 | — | 18s | Sem Confusão |
| Tarefa 2: Selecionar uma imagem do histórico | Sucesso Total | 0 | — | 10s | Sem Confusão |
| Tarefa 3: Interpretar os resultados exibidos | Sucesso Parcial | 1 | Interpretação (score confuso) | 35s | Confusão Leve |
| Tarefa 4: Clicar em Iniciar Detecção e verificar atualização | Sucesso Parcial | 1 | Feedback ausente durante processamento | 50s | Confusão Moderada |
| Tarefa 5: Gerar relatório e confirmar na tabela | Sucesso Parcial | 1 | Sistema (atraso na listagem) | 65s | Confusão Moderada |
| Tarefa 6: Visualizar animal detectado | Sucesso Total | 0 | — | 22s | Sem Confusão |
| Tarefa 7: Voltar à tela inicial e fechar o sistema | Sucesso Total | 0 | — | 8s | Sem Confusão |

### Avaliação de cada Tarefa — Usuário 2

| Tarefa | Grau de Sucesso | Total de Erros cometidos | Tipos de Erros | Tempo Necessário | Grau de Satisfação |
|---|---:|---:|---|---:|---|
| Tarefa 1: Carregar uma imagem no sistema | Sucesso Parcial | 1 | Upload não exibiu preview imediatamente | 40s | Confusão Moderada |
| Tarefa 2: Selecionar uma imagem do histórico | Sucesso Parcial | 1 | Navegação (miniaturas pequenas) | 30s | Confusão Moderada |
| Tarefa 3: Interpretar os resultados exibidos | Falha | 2 | Interpretação; termos técnicos sem explicação | 75s | Confusão Alta |
| Tarefa 4: Clicar em Iniciar Detecção e verificar atualização | Falha | 2 | Sem feedback; usuário não soube se processo rodou | 120s | Frustração Alta |
| Tarefa 5: Gerar relatório e confirmar na tabela | Falha | 2 | Não encontrou botão; relatório não apareceu | 90s | Frustração Alta |
| Tarefa 6: Visualizar animal detectado | Falha | 1 | Link de visualização não óbvio | 60s | Confusão Alta |
| Tarefa 7: Voltar à tela inicial e fechar o sistema | Sucesso Parcial | 1 | Menu confuso para retornar | 25s | Confusão Moderada |

### Respostas do Formulário do Usuário:
<img width="855" height="593" alt="image" src="https://github.com/user-attachments/assets/6419bf96-88e0-4064-81cd-19b624e094b4" />
<img width="855" height="721" alt="image" src="https://github.com/user-attachments/assets/b39c34ca-fc23-4042-847a-27330f47f3ed" />
<img width="855" height="591" alt="image" src="https://github.com/user-attachments/assets/ff7b577f-1a6a-4e85-8114-dae5fcf3f7c8" />
<img width="855" height="598" alt="image" src="https://github.com/user-attachments/assets/978504e2-6ea7-4188-82f4-d9d42368dfb8" />
<img width="855" height="720" alt="image" src="https://github.com/user-attachments/assets/25ddbffd-2613-4d0c-b088-95a8371365f8" />

### Conclusão da avaliação por observação do usuário:

#### Usuário 1
- Completou a maioria das tarefas sem grandes problemas. Encontrou alguns incômodos, como a imagem nem sempre aparecer logo após o envio, ausência de aviso claro durante o processamento e demora na atualização da lista de resultados. Isso não impediu a conclusão, mas deixou a experiência menos confiável e mais lenta.

#### Usuário 2
- Teve mais dificuldade. Não entendeu bem os números que indicam a confiança do sistema, as miniaturas do histórico eram pequenas e faltaram mensagens claras enquanto o sistema trabalhava. Esses pontos a impediram de completar tarefas importantes e reduziram a utilidade para triagem de imagens de campo.

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
