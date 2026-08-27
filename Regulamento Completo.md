
# Desafio Olho na Caixa

**Quantas frutas realmente chegaram?**

*Desafio aberto aos alunos da UFBA e promovido pela Solutis AI Center & LabS*

> 🤝 Ativação da parceria com a LIAO, Liga de IA e Otimização (UFBA)

| | |
|---|---|
| 💰 Prêmio | R$ 3.000 a R$ 5.000 |
| 📅 Prazo final | 21/09/2026, 23h59 |
| 🚀 Publicação | 22/08/2026 |

**[Quero participar](#inscrição-e-envio)** · **[Ver o que entregar](#o-que-entregar)**

---

## A história


![Ilustracao](assets/ilustracao-historia.png)

*Na cozinha da escola, um celular comum e visão computacional respondem, "em segundos", quanto realmente chegou naquela caixa.*

Terça-feira, 7h40. O caminhão do fornecedor para na frente da escola. Descem quatorze caixas.

O contrato diz o que deveria ter dentro delas: 380 unidades de tangerina, 240 unidades de banana, 25 kg de tomate, 12 kg de cenoura. Para saber se chegou, alguém teria que contar 380 tangerinas, uma por uma, em cima da pia. E depois contar 240 bananas. E depois pesar o tomate, sem balança, ou com uma balança de cozinha que não aguenta a caixa inteira.

Ninguém faz isso. Não por descuido: **porque não cabe.** O entregador está com o motor ligado e mais seis escolas na rota. O café das 8h não pode atrasar. A única pessoa disponível para receber é a mesma que está preparando a refeição, e ela tem talvez um minuto por caixa.

Então acontece o que sempre acontece: olha-se as caixas por cima, parece certo, assina.

A conferência só tem valor se acontecer naquele instante, com o entregador ainda parado ali: é o único momento em que dá para recusar a caixa e devolver. 
Depois que o caminhão vira a esquina, uma falta virou perda, porém ainda faz sentido uma auditoria sobre o que foi entregue. Afinal multiplique por centenas de escolas, cinco vezes por semana, o ano letivo inteiro.

> O desafio é responder o mais rápido possível, idealmente em menos de um minuto, e no ato do recebimento: quanto realmente chegou dentro dessas caixas?

## Os quatro itens do desafio

A lista de hortifruti do contrato mistura itens medidos por **unidade** e por **peso (kg)**. Quatro itens são o grupo obrigatório, e sua solução precisa atender **pelo menos 2 dos 4**. Atender mais de dois, e cobrir um de cada natureza, conta a favor na avaliação.

| Item | Conferência | O que ele testa |
|---|---|---|
| **Banana** | por unidade | chega em pencas, mas o contrato conta unidades: exige lidar com o aglomerado e a conversão de penca para unidade |
| **Tangerina** | por unidade | esférica, a granel, empilhada em camadas: só a camada de cima é visível |
| **Tomate** | por peso (kg) | muitas peças pequenas, caixa densa, peso alto para o volume |
| **Cenoura** | por peso (kg) | forma alongada que se entrelaça: volume aparente engana, com muitos vazios entre peças |

Soluções que se generalizem para outros itens da lista sem retrabalho (laranja, maçã, batata, repolho) também contam ponto.

## Premissas: as regras do mundo real

Estas restrições descrevem a escola como ela é, não como gostaríamos que fosse.

**1. Sem hardware específico**

Sem câmera fixa, sem esteira, sem sensor. **Exceção: balanças comuns** (5 a 25 kg, doméstica ou de feira), permitidas, mas sem integração digital. O peso entra por foto do display ou digitado em formulário. Uma caixa cheia pode passar de 25 kg, e resolver isso (pesagem em partes, tara da caixa vazia etc.) faz parte do desafio. Estimar peso por imagem, sem depender de balança, vale ponto extra.

**2. Só celular comum**

Fotos e vídeos com o aparelho que a equipe já tem em mão, sem tripé ou acessório. Captura guiada por app, com jornadas diferentes por tipo de item, é permitida e incentivada. Assuma aparelho de entrada, câmera comum e rede instável.

**3. Qualquer tecnologia de visão**

YOLO e similares, modelos multimodais (Google, OpenAI, Anthropic), modelos próprios ou combinações. Nenhuma abordagem é privilegiada: vale o resultado.

**4. Mudar o processo é permitido**

O processo atual é manual e sem padrão. Apoiar a caixa em um lugar específico, transferir conteúdo em etapas, folha impressa no enquadramento, dois ângulos, pesar em duas partes: tudo é jogo. Limite único: a captura deve caber em menos de um minuto por caixa, com uma pessoa só, sem treinamento longo e com o mínimo de fricção.

## As três dimensões da solução

Toda submissão precisa apresentar explicitamente sua abordagem nas três dimensões abaixo. Uma solução que brilha em uma e ignora as outras não compete.

**1. Processo de captura**
Como a informação entra: foto, vídeo, sequência, ordem dos passos, tempo, o que o app pede para enquadrar, o que acontece com luz ruim. Se exige checagem ou devolução, descreva e argumente a baixa fricção.

**2. Evidências da abordagem**
Quais sinais chegam ao número (geometria, camadas, contagem de eventos, peso médio, referência de escala, leitura de display, resposta de modelo multimodal) e o que fica registrado para revisão posterior.

**3. PoC / protótipo funcional**
Protótipo que recebe a captura real e devolve a contagem ou a medição automatizada, não uma maquete de telas nem um slide de arquitetura. App, web ou notebook com interface simples. Precisa rodar na frente da banca sobre material que a banca pode escolher.

## Como será avaliado

| Critério | Peso |
|---|---:|
| Acurácia medida nos itens atendidos | 35 |
| Processo de captura: fricção baixa, viável na cozinha, à prova de erro do usuário | 20 |
| PoC funcional: roda de verdade, usável por quem não é técnico | 20 |
| Evidências: adequação dos sinais usados e clareza do registro | 15 |
| Clareza e reprodutibilidade, incluindo o método de cálculo da margem de erro | 10 |
| **Pontuação base (soma dos critérios acima)** | **100** |

A pontuação base vai até 100 pontos. Os pontos extras da seção abaixo somam até 15 pontos adicionais, elevando a pontuação máxima possível para 115 pontos.

## Margem de erro

**Obrigatória.** Sua entrega precisa dizer qual é a margem de erro da solução para cada item atendido e como ela foi calculada: quantos lotes ou caixas testados, qual era a quantidade real de cada um e como você obteve esse valor real, e qual métrica usou (erro percentual médio, maior erro observado, desvio, etc.).

> Uma solução com 12% de erro bem medido e bem explicado vale mais do que uma que promete "alta precisão" sem demonstrar. Margem de erro não declarada, ou sem método, derruba a nota de acurácia.

**Declarar incerteza a cada conferência é opcional:** uma faixa ("entre 360 e 395 unidades") ou nível de confiança conta a favor, mas não é exigência.

| Item e situação | Erro aceitável por lote (referência) |
|---|---|
| Banana (unidade, chega em penca) | ≤ 5% |
| Tangerina (unidade, a granel) | ≤ 10% |
| Tomate e cenoura (kg), com balança comum | ≤ 3% |
| Tomate e cenoura (kg), sem balança, estimado por imagem | ≤ 10% |

Metas não são eliminatórias, orientam a nota de acurácia.

## Pontos extras

Cada item atendido abaixo soma **3 pontos extras** à pontuação base, no limite de **15 pontos adicionais** (5 itens, 3 pontos cada).

| Ponto extra | Pontos |
|---|---:|
| Estimar peso por imagem sem depender de balança | +3 |
| Tratar explicitamente os casos em que a solução não deve responder (luz insuficiente, enquadramento ruim, item não identificado) | +3 |
| Tempo total por caixa abaixo de 1 minuto | +3 |
| Custo por conferência declarado, quando houver uso de API paga | +3 |
| Generalizar para outros itens da lista sem retrabalho | +3 |

## Prazo e premiação

- **27/08/2026**: Publicação do desafio
- **Durante os 30 dias**: Canal de dúvidas aberto e kit de apoio disponível
- **02/10/2026, 23h59**: Prazo final único para todas as submissões
- **A definir**: Avaliação da banca e anúncio do vencedor

A Solutis premiará o autor da melhor solução apresentada, que atenda aos requisitos do desafio, com valor **entre R$ 3.000,00 e R$ 5.000,00**. O vencedor e o valor exato serão definidos pela banca avaliadora indicada pela Solutis, exclusivamente pela qualidade e completude da solução.

| Faixa de pontuação | Valor do prêmio |
|---|---|
| Mínimo entregável: atende aos requisitos obrigatórios do desafio (pelo menos 2 dos 4 itens, PoC funcional e margem de erro dentro das metas de referência, sem pontos extras) | **R$ 3.000,00** |
| Pontuação máxima possível: 100 pontos da avaliação, mais os 15 pontos extras, totalizando 115 pontos | **R$ 5.000,00** |

Soluções entre esses dois extremos recebem valor proporcional à pontuação total, a critério da banca avaliadora.

## O que entregar

1. **Pacote da solução:** código, instruções de execução e dependências, de forma que a banca consiga rodar (link do repositório GitHub)
2. **Documento de até 6 páginas:** as três dimensões, decisões técnicas, margem de erro de cada item com método de cálculo, e limites conhecidos
3. **Vídeo de até 5 minutos:** o protótipo funcionando sobre material real
4. **Material de captura utilizado:** fotos, vídeos e pesagens usados para medir a acurácia, com a quantidade real de cada lote e como foi apurada

## Kit de apoio fornecido pela Solutis

- Planilha de itens de hortifruti com a unidade de conferência de cada produto
- Fotos e vídeos de referência
- Canal de dúvidas durante todo o período do desafio

📦 Repositório do kit de apoio (template de submissão, planilha e instruções): [github.com/marx-correia/desafio-olho-na-caixa](https://github.com/marx-correia/desafio-olho-na-caixa)

## Regras e observações

**Participação:** restrita a alunos regularmente matriculados na UFBA (graduação ou pós-graduação), individualmente ou em equipe. A LIAO - Liga de Inteligência Artificial e Otimização, é incentivada pela parceria, mas o desafio NÃO está restrito apenas aos alunos membros da Liga.

**Propriedade intelectual:** você mantém a autoria da sua solução e concede à Solutis licença de uso não exclusiva do material submetido, para avaliação e demonstração deste desafio e compartilhamento de conhecimento.

**Privacidade e LGPD:** vale lembrar que o ambiente é uma escola. Portanto rostos de adultos ou crianças que apareçam no material devem ser desfocados/anonimizados. A solução não deve depender de reconhecimento de pessoas para funcionar.

## Inscrição e envio

Preencha o formulário de inscrição para receber acesso ao canal de dúvidas e incrementos ao kit de apoio. A submissão final (repositório, documento, vídeo e material de captura) é feita pelo mesmo formulário de envio final.

**[Preencher o formulário de inscrição](https://forms.cloud.microsoft/r/m6qLkbRGDw)**

**[Submissão de proposta de solução](https://forms.cloud.microsoft/r/WNb1hATgch)**


## Dúvidas frequentes

**Preciso de uma base gigante de dados anotados?**
Não. Trinta dias não dão para isso, e o desafio não assume isso. Criatividade no processo de captura costuma valer mais que volume de dados.

**Posso usar balança?**
Sim, comum, de 5 a 25 kg, sem integração com o sistema: o peso entra por foto do display ou digitado em formulário. Uma caixa cheia pode passar da capacidade, e resolver isso faz parte do desafio.

**Posso usar API paga de modelo multimodal?**
Pode. Só declare o custo estimado por conferência: uma rede de escolas não sustenta reais por caixa.

**Posso mudar o jeito como a caixa é recebida?**
Pode, desde que a mudança seja de baixa fricção e você defenda por quê. É uma das partes mais interessantes do desafio.

**Preciso acertar exatamente?**
Não. Precisa errar pouco, medir quanto erra e explicar como mediu.

---

Solutis AI Center & Solutis LabS · Desafio Olho na Caixa · 2026
Ativação da parceria com a LIAO, Liga de Inteligência Artificial e Otimização (UFBA)
