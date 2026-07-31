> Tradução comunitária (rascunho) — Política NTARI P2-002, Transmissão Multilíngue Global (Global Multilingual Broadcast). Fonte: lighthouse-seed.md (original em inglês, snapshot de 2026-07-29). Rascunho comunitário assistido por máquina, pendente de revisão por mantenedor regional conforme P2-002 §3.1. As especificações técnicas centrais permanecem em inglês conforme §2.2.
>
> Notou algum erro nesta tradução? Correções de tradução são contribuições
> valiosas e muito bem-vindas: faça um fork do repositório e abra um pull
> request em https://github.com/NTARI-RAND/lighthouse.

# A Rede Lighthouse — Documento Semente

**Uma aplicação da Janus-Facing Architecture: um commons de conhecimento testemunhado, sustentado por hubs cívicos.**

Network Theory Applied Research Institute

Este documento está integralmente vinculado à Janus-Facing Architecture (JFA). Ele nomeia papéis e mecanismos, nunca o software que os preenche; toda invariante da arquitetura-mãe vincula aqui sem reafirmação, e onde este documento e a JFA divergirem, ou este documento é corrigido ou a JFA é emendada às claras. Seu companheiro normativo é **lighthouse-weight-tiers.md**, a especificação completa dos níveis; este documento resume os níveis e não os duplica — um espelho é uma segunda fonte de verdade, que já nasce em deriva.

**Vocabulário, mapeado para os papéis da JFA.** Um **hub** é uma instituição cívica — uma biblioteca, uma escola ou qualquer organização que execute o software — reunindo dois papéis da JFA em um único pacote implantável: o **orquestrador** (o papel de coordenador/operador da JFA: o aplicativo voltado aos membros, o log append-only do próprio hub, seus deveres de adjudicação) e a **testemunha** (que contra-assina os checkpoints de *outros* hubs). **LBTAS** é a escala de avaliação do pacto — voltada a revelar danos, derivada de Leveson; sua expansão está pendente de definição (problema em aberto 2). Uma **âncora** é o compromisso de fatos estruturais e hashes no registro testemunhado. Uma **atestação** é a alegação assinada de um hub de que uma execução ocorreu fisicamente em suas instalações — ocorrência, nunca verdade. Uma **unidade-hub** é a unidade de contagem de corroboração: o hub, nunca a conta. Um **rótulo provisório** (stand-in) marca qualquer garantia operando abaixo de seu piso estrutural.

---

## Parte I — o que é o Lighthouse

O Lighthouse é um commons de conhecimento no qual fatos empíricos são capturados **junto com os procedimentos que os testam**, vindos de proponentes de formação acadêmica e não acadêmica igualmente, ancorados a um registro testemunhado por meio de hubs locais onde o público pode discutir, replicar e contestar em comunidade. Ele instancia a Parte VI da JFA: um registro testemunhado pode ancorar qualquer alegação empírica ou comercial; ancorada, uma alegação torna-se citável, e o pacto avalia o proponente da mesma forma que avalia um parceiro comercial. Os mesmos trilhos que tornam o comércio confiável tornam o conhecimento confiável.

O nome é a disciplina. Um farol não certifica uma rota segura; ele torna o perigo visível e deixa a navegação a cargo do navio. O Lighthouse ilumina alegações — seus procedimentos, suas replicações, suas disputas, a reputação de seus proponentes — e nunca emite um veredicto sobre a verdade. Sinalizar, nunca sentenciar; ancorar, nunca certificar.

O que ele não deve se tornar, herdado literalmente: uma agência de classificação da verdade, um mercado de anúncios onde a visibilidade é comprada, um monopólio de credenciamento. A descoberta permanece federada, citada e contestável.

## Parte II — o modelo de alegações

O objeto atômico de conhecimento é uma tripla vinculada: **alegação de fato, procedimento, resultado**, ancorada como alegação, nunca afirmada como fato.

- O ledger registra apenas fatos estruturais e referências — hashes de conteúdo dos três artefatos, tipo da alegação, identificador de versão do procedimento, carimbo de tempo, referência pseudônima do proponente, referência do hub. **Nenhuma PII no commons**, jamais.
- Os próprios artefatos — texto do procedimento, dados — entram no commons de contribuição AGPL, endereçados por conteúdo, servidos pelos hubs. A proveniência é entrada = saída; uma contribuição não pode ser retomada.
- Alegações de conhecimento, replicações e suas disputas são **relações tipadas**, distintas dos sinais de comércio e de adjudicação. Nenhum leitor pode colapsá-las.
- Replicações vinculam-se à **versão do procedimento** que executaram. Um refinamento é uma nova âncora que cita a antiga; a reputação acumula-se por versão, com a cadeia visível.
- Toda âncora deve responder por si; contestações são arestas de primeira classe; o silêncio de um proponente acumula dwell — legível, nunca autoadjudicado. Um artefato que se torna irrecuperável é renderizado como artefato-escuro (artifact-dark); a âncora nunca se apaga.

## Parte III — o pacto aplicado

O LBTAS avalia **proponentes, nunca alegações**. Uma alegação só acumula reputação por meio da estrutura de corroboração da Parte V; uma pessoa só acumula reputação por meio de conduta.

- A distribuição completa é entregue, nunca uma média; a avaliação mais baixa é a própria violação. Uma fabricação nunca se dissolve em um volume confortável de bom trabalho.
- **Concordância é dado; violação é conduta.** Uma replicação inconsistente é um fato de concordância — consistente, inconsistente, inconclusiva — nunca uma acusação, e nunca é encaminhada como alegação de dano. Somente conduta entra no pipeline do pacto: fabricação, deturpação do que foi executado, uma atestação falsa. **Discordância nunca é violação.** Essa separação de canais é o que impede que alegações de dano se tornem a arma da disputa científica.
- O pacto é simétrico: toda alegação é contestável, arquivamentos anotam, e uma violação posterior anota as âncoras de um proponente sem apagá-las — um fabricador pode ter dito algo verdadeiro, e as replicações de suas alegações sustentam-se em seu próprio registro.
- Nenhuma autoridade de verdade em lugar algum: nenhum "verificado como verdadeiro" de qualquer hub, qualquer centro, qualquer varredura, qualquer modelo. Um auxílio de leitura por máquina explica; nunca certifica.

## Parte IV — a arquitetura de hubs

Um pacote, dois papéis, duas chaves, **sempre apontadas para fora**.

- Todo hub executa o orquestrador e a testemunha, mas **nenhuma instituição testemunha o próprio log**. Os checkpoints da Biblioteca A são contra-assinados pela Escola B e pela Biblioteca C; A retribui o favor nos deles. As chaves de testemunha são distintas par a par e nunca são as do próprio operador — um orquestrador-testemunha fundido em uma única instituição é o operador que atesta a si mesmo, exatamente o que a camada de registro existe para impedir.
- Uma alegação de dano contra um hub **é protocolada na testemunha de um hub vizinho**, a montante, com o operador ausente do nascimento da alegação contra si. Onde quer que dois hubs se federem, a lacuna de liveness do protocolo de registro se fecha.
- **Piso de lançamento: dois hubs independentes.** Um piloto de hub único só é conforme sob o rótulo provisório; ele não pode se apresentar como federação.
- **Espaço, nunca portão.** O registro e o mercado vivem no protocolo, abaixo do aplicativo de qualquer hub. Um membro recusado ou maltratado na Biblioteca A entra no aplicativo da Escola B com reputação e liquidez intactas. Essa portabilidade — não a boa vontade de qualquer hub — é o que faz dos hubs espaços, e não porteiros.
- A independência entre hubs é lida estruturalmente: controle distinto par a par, excluídos operador comum, controlador comum e matriz administrativa compartilhada. **As dez filiais de um sistema de bibliotecas de condado são uma única unidade.** A relação de testemunho *não* é uma relação de controle — hubs que contra-assinam os logs uns dos outros permanecem corroboradores independentes, ou pequenas federações seriam estranguladas ao nascer.
- Mercado-alvo: bibliotecas e escolas, com membros acessando o aplicativo móvel ou web de seu hub. Sob a AGPL-3.0, qualquer instituição pode entrar no mercado de orquestração do commons de conhecimento; o copyleft somado à escada de legibilidade mantém esse mercado contestável, e não meramente aberto.

## Parte V — níveis de peso, por referência

O texto normativo vive na especificação companheira. A forma: **T0 Ancorado** (a existência é o piso, nunca evidência) → **T1 Citado** (renderiza o grafo de descoberta; contagens de citação não dimensionam nada, permanentemente) → **T2 Replicado no próprio hub** (executabilidade; todas as replicações no mesmo hub colapsam em uma unidade-hub) → **T3 Replicado entre hubs** (corroboração contada em unidades de hubs independentes, mantida por categoria de concordância — "consistente em quatro hubs, inconsistente em um" é entregue exatamente assim) → **T4 Atestado** (a chave institucional de um hub aposta sua reputação na *ocorrência, nunca na verdade*; o custo de emissão é corpos e tardes, linear).

Quatro disciplinas vinculam todos os níveis: vinculação de versão; concordância-é-dado-violação-é-conduta; **elegibilidade, nunca dimensionamento** — o status de nível determina se uma alegação pode entrar no influxo econômico, e nunca dimensiona um pagamento; e nenhuma renderização colapsada — sem pontuação, sem estrelas, sem selo de verificado, cada nível entregue com seu recibo.

## Parte VI — a postura diante de Sybil

Gerenciado até deixar de compensar, nunca resolvido: as duas ferramentas que poderiam resolvê-lo — uma autoridade global de identidade e um muro de compra — são as duas coisas que a arquitetura recusa. Quatro movimentos:

1. **A corroboração conta hubs, não contas.** Exclusão por mesmo controlador em todos os níveis; dez contas-fantoche em uma biblioteca colapsam no valor estrutural de um único hub.
2. **Presença física é o custo por unidade.** A atestação faz o nível mais forte custar corpos e tardes, linearmente, sem economias de escala — a desonestidade precificada acima de seu rendimento, não impedida.
3. **A varredura do limpo-demais.** Subgrafos fechados de citação, anéis de admiração mútua e concordância suspeitamente sem dispersão entre hubs "independentes" são material de sinalização — uma sinalização contestável, nunca uma remoção, porque falsos positivos recaem sobre pequenas comunidades de nicho honestas, e o local natural de contestação é o próprio salão do hub.
4. **Recompensas sequenciadas atrás da chave.** No lançamento, o peso não dimensiona nada: sem ranking, sem influxo. O grafo acumula-se no registro testemunhado — anéis construídos cedo são esforço desperdiçado e permanentemente visíveis à varredura retroativa. O peso então é ligado como uma mudança de política governada e testemunhada, apenas para os níveis entre hubs e atestado. Sybil antes do peso de citação, satisfeito por ordenação, não por perfeição.

Resíduo nomeado: um humano que genuinamente frequenta N hubs (o custo linear é a defesa); anéis de conluio de humanos reais atravessando hubs (fraude — território do pacto, cada instância adjudicada uma violação que nunca se dissolve em média); o alcance de nível de membros remotos (problema em aberto 3); escassez de corroboração na partida a frio (os rótulos provisórios carregam a honestidade).

## Parte VII — o influxo econômico

Conhecimento ancorado e corroborado torna-se insumo de P&D para produtos e serviços nas economias JFA — o rendimento de um cultivar, o modo de falha de uma ferramenta, a curva de custo de um método, fluindo do commons para a troca real.

- O status de nível determina a **elegibilidade** para o influxo; o limiar — T3 ou acima, ou apenas T4 na virada da chave — é política governada e testemunhada, não definição de nível. O dimensionamento do pagamento pertence à troca real que ele financia, que carrega a fricção comercial que os níveis não podem carregar.
- **Nenhum posicionamento pago, jamais.** As alegações de um fornecedor sobre seus próprios produtos são ancoradas, replicadas e disputadas como as de qualquer um; o pacto e a varredura as policiam, nunca uma taxa de listagem.
- As invariantes da economia JFA vinculam por inteiro: a unidade ganha, nunca comprada; não resgatável; denominação não é resgate; e uma leitura regulatória concluída antes de qualquer fase de crédito.

## Parte VIII — ordem de desenvolvimento

Construa de baixo para cima; a ordem é o argumento. Cada estágio é entregue com seus rótulos provisórios honestos.

1. **Estágio 0 — o registro federado.** Piloto de dois hubs: logs append-only por hub, checkpoints monotônicos com testemunho cruzado, provas de consistência, protocolo-no-vizinho. Esta é a construção de maior alavancagem da própria JFA (problema em aberto 2) vestindo as roupas do Lighthouse; nada acima dela é lido honestamente até que seja real.
2. **Estágio 1 — ancoragem e descoberta.** T0 e T1: a tripla de alegação, o grafo de citações tipado, o serviço de artefatos a partir do commons AGPL. Sem dimensionar nada.
3. **Estágio 2 — replicação e concordância.** T2 e T3: contagem por unidade-hub, distribuições de concordância, renderização de dwell. Recibos e regras-como-dados-de-política-diffáveis são entregues *aqui*, como recursos de lançamento — legibilidade é um entregável da construção, não polimento.
4. **Estágio 3 — atestação.** T4: chaves institucionais dos hubs, disciplina de ocorrência, a regra de exclusão de funcionários, atestação falsa alimentando a leitura de conduta do operador.
5. **Estágio 4 — a chave do influxo.** Somente após a leitura regulatória e somente para os níveis entre hubs e atestado, como uma mudança de política governada e testemunhada.

## Parte IX — problemas em aberto

1. **A interface de exame do registro não está desenhada.** Membros examinando o registro pelo aplicativo de seu hub herdam a escada de legibilidade inteira — decisões que se explicam no ponto de uso, regras vivendo como dados diffáveis, versões de política testemunhadas, auxílios de leitura por máquina que nunca se tornam oráculos. Esta é a próxima conversa de design, e ela é nomeada aqui em vez de contornada.
2. **O LBTAS aguarda sua definição.** Este documento o trata como a escala de avaliação do pacto voltada a revelar danos, derivada de Leveson; a expansão e qualquer adaptação específica do Lighthouse aos níveis da escala estão por escrever.
3. **Exclusão geográfica.** Uma comunidade sem hub participante não pode alcançar T4 e só alcança T3 por meio de registro distante. Dias itinerantes de atestação e arranjos com hubs parceiros são soluções de contorno candidatas; a aceitação silenciosa não é.
4. **Captura de hub além da varredura.** Instituições reais podem conluiar-se; a resposta é adjudicação mais a leitura de conduta do operador, ambas dependentes de a federação ser real — este problema repousa sobre o Estágio 0 exatamente como o problema 4 da JFA repousa sobre seu problema 2.
5. **Tudo na Parte VII da JFA vincula aqui.** Os problemas 2, 4, 7 e 8 em especial. O design hub-como-testemunha do Lighthouse é uma alavanca proposta para o problema 8 — instituições cívicas como testemunhas longevas, publicamente responsabilizáveis e mutuamente independentes — a ser provada em implantação, não presumida.

## O padrão

Um sistema só é Lighthouse se todos os sete valerem; falhando um, é outro software vestindo o vocabulário.

1. Alegações são ancoradas como alegações; nenhum centro, varredura, hub ou modelo detém veredicto sobre a verdade.
2. Hubs são espaços, nunca portões: o registro e o mercado vivem abaixo do aplicativo de qualquer hub, e um membro deixa um hub por outro com reputação e liquidez intactas.
3. Nenhuma instituição testemunha o próprio log; dois hubs independentes são o piso da federação, e qualquer coisa menor carrega o rótulo provisório.
4. A corroboração é contada em unidades de hubs independentes, nunca em contas; contagens de citação não dimensionam nada, permanentemente.
5. Distribuições são entregues inteiras — concordância ao lado de volume, dano ao lado de elogio — nunca uma pontuação colapsada ou um selo de verificado, e toda renderização carrega seu recibo.
6. Concordância é dado e violação é conduta; discordância nunca é violação.
7. O peso determina elegibilidade e nunca dimensiona pagamento; toda recompensa fica atrás de uma chave governada e testemunhada, sequenciada Sybil-primeiro.

---

Durante a implementação, o protocolo de tensão está em vigor: ao notar uma restrição sendo reenquadrada por conveniência, um substituto sendo entregue sem rótulo, ou um problema em aberto sendo contornado — pare, nomeie a tensão, anexe-a à invariante ou ao problema e proponha o movimento conforme mínimo. Traga-a à superfície; não a absorva.

*Este documento é documentação livre sob o commons AGPL-3.0 do projeto; ele foi feito para ser lido, reimplementado e contestado.*
