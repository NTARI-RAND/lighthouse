> Tradução comunitária (rascunho) — Política NTARI P2-002, Transmissão Multilíngue Global (Global Multilingual Broadcast). Fonte: lighthouse-weight-tiers.md (original em inglês, snapshot de 2026-10-05). Rascunho comunitário assistido por máquina, pendente de revisão por mantenedor regional conforme P2-002 §3.1. As especificações técnicas centrais permanecem em inglês conforme §2.2.
>
> Notou algum erro nesta tradução? Correções de tradução são contribuições
> valiosas e muito bem-vindas: faça um fork do repositório e abra um pull
> request em https://github.com/NTARI-RAND/lighthouse.

> O original em inglês é normativo. Esta tradução é oferecida para leitura, não para interpretação: onde divergir de `lighthouse-weight-tiers.md`, prevalece o inglês. As palavras-chave normativas (MUST, MUST NOT, SHOULD, SHOULD NOT, MAY), os nomes de campos, os rótulos e os identificadores são mantidos em inglês porque constituem o contrato de conformidade.

# Níveis de Peso do Lighthouse — Rascunho de Especificação

Vinculado à Janus-Facing Architecture. Um nível é um **fato estrutural sobre corroboração**, nunca um veredicto sobre a verdade. Os níveis são contados em **unidades de hubs independentes**: o hub, não a conta, é a unidade de contagem, com a independência lida estruturalmente e os hubs sob controle comum excluídos. As definições de nível são **política, não mecanismo** — elas vivem como dados de política diffáveis e são comprometidas no registro testemunhado com entradas de changelog em linguagem simples, de modo que a pergunta "quais regras de nível estavam em vigor quando isto foi renderizado?" sempre tem uma resposta testemunhada. Toda renderização que mostra um nível carrega um recibo: quais replicações, quais hubs, qual distribuição de concordância, qual versão da política de níveis. Alegações de conhecimento e suas replicações são **relações tipadas**, distintas dos sinais de comércio e de adjudicação; nenhum leitor pode confundi-las.

---

## T0 — Ancorado

Uma alegação de conhecimento existe no registro testemunhado como uma tripla vinculada — **alegação de fato, procedimento, resultado** — comprometida por um proponente em situação regular, em um hub, sob a disciplina ordinária da camada de registro: append-only, testemunhado de forma independente, monotônico. A âncora compromete **apenas fatos estruturais e referências**: hashes de conteúdo dos três artefatos, um tipo de alegação, um identificador de versão do procedimento, um carimbo de tempo, uma referência pseudônima do proponente, uma referência do hub. Os próprios artefatos — o procedimento escrito, os dados — entram no commons de contribuição AGPL, endereçados por conteúdo e servidos pelos hubs; o ledger guarda os hashes.

- A ancoragem é condicionada pelo pacto: a situação (standing) decide **se** uma conta pode ancorar, nunca quanto nem com que visibilidade.
- A existência é o piso, nunca evidência. Um leitor pode inferir que esta alegação, com este procedimento, existia neste momento, vinda de uma conta então em situação regular. Um leitor NÃO pode inferir revisão, plausibilidade ou verdade.
- Toda âncora deve responder por si. Qualquer pessoa pode ancorar uma contestação que a referencie; o silêncio do proponente acumula dwell — um fato legível, nunca um fato autoadjudicado.
- Um artefato que se torna irrecuperável não apaga a âncora; a alegação é renderizada como artefato-escuro (artifact-dark), outro fato legível.
- Uma violação posterior do pacto por um proponente **anota suas âncoras, nunca as apaga**. Um fabricador pode ter dito algo verdadeiro; as replicações de suas alegações sustentam-se em seu próprio registro.

Superfície de manipulação: emissão em massa. Defesa: T0 não dimensiona nada, toda âncora é uma exposição que responde por si sob o pacto, e um hub pode limitar a taxa de ancoragem como política local e publicada.

## T1 — Citado

Outras âncoras referenciam a alegação. Citações são **arestas tipadas** — estende, usa-procedimento, disputa, menciona — e os tipos de aresta são dados de política. A citação renderiza o **grafo de descoberta**: é assim que as alegações são encontradas, navegadas e contestadas entre hubs.

- Contagens de citação MUST NOT entrar no peso, no ranking para recompensa ou na elegibilidade — **permanentemente**, e não enquanto se espera algo. Citações são, e continuarão sendo, quase gratuitas de emitir; um sinal que não custa nada não pode pesar nada.
- Uma aresta *disputa* é de primeira classe e é renderizada ao lado de *estende*. O grafo nunca se compensa em saldo líquido.
- As superfícies de descoberta MUST renderizar a proveniência — quem cita, a partir de qual hub — para que um anel de citações seja legível como uma forma. A varredura do limpo-demais lê subgrafos fechados como material de sinalização; uma sinalização é insumo de contestação, nunca remoção.

Um leitor pode inferir atenção e conectividade. Um leitor NÃO pode inferir corroboração. A citação encontra alegações; nunca as confirma.

## T2 — Replicado no próprio hub

Uma conta diferente da do proponente, registrada no **próprio hub do proponente**, executou uma versão específica do procedimento e ancorou uma **replicação**: referência da versão do procedimento, o hash de seu próprio resultado e sua **declaração de concordância** — consistente, inconsistente ou inconclusiva —, que é sua própria alegação, que deve responder por si e é contestável como qualquer âncora.

- Todas as replicações no mesmo hub **colapsam em uma única unidade-hub**, independentemente do número de contas. O colapso é a defesa contra Sybil: contas-fantoche não compram nada, e a métrica se sustenta sem qualquer detecção de controlador.
- As contas do próprio proponente são excluídas; onde o controle comum de contas é estruturalmente visível, ele também é excluído — mas é a regra do colapso, não a detecção, que sustenta a garantia.
- T2 contribui com estrutura e renderização, nunca com elegibilidade. Sua função é a de rampa de acesso: prova que o procedimento é **executável por mãos que não as de seu autor**, e traz à tona defeitos procedimentais a baixo custo, antes que se gaste esforço entre hubs.

Um leitor pode inferir executabilidade e interesse local. Um leitor NÃO pode inferir confirmação independente — um hub compartilhado significa equipamento compartilhado, gravidade social compartilhada, pontos cegos compartilhados.

## T3 — Replicado entre hubs

Existem replicações ancoradas vindas de hubs **estruturalmente independentes** do hub do proponente. O nível carrega uma contagem em unidades-hub — o número de hubs independentes distintos com pelo menos uma replicação ancorada — mantida **por categoria de concordância**: "consistente em quatro hubs, inconsistente em um" é entregue exatamente assim, permanentemente. Esta é a regra de não fazer médias aplicada ao conhecimento.

- A independência é lida estruturalmente no nível do hub: controle distinto par a par. Operador comum, controlador comum, matriz administrativa compartilhada — excluídos. **As dez filiais de um sistema de bibliotecas de condado são uma única unidade.**
- A relação de testemunho não é uma relação de controle. Hubs que contra-assinam os checkpoints uns dos outros permanecem corroboradores independentes; do contrário, parceiros de federação jamais poderiam corroborar uns aos outros, e redes pequenas seriam estranguladas ao nascer.
- Um hub só é uma unidade contável enquanto seu próprio registro for honestamente testemunhado — duas ou mais testemunhas independentes, nenhuma delas sendo chaves do próprio hub. As replicações de um hub novo correm sob o **rótulo provisório** (stand-in) até que seu testemunho seja real: reconhecimento escalonado, exatamente como na camada de governança.
- A replicação real se dispersa. Uma concordância perfeita demais entre hubs supostamente independentes é, ela própria, material de sinalização para a varredura — a assinatura do wash trade traduzida para o conhecimento.
- Uma inconsistência sem resposta acumula dwell sobre a alegação original — legível, nunca um rebaixamento automático.

Superfície de manipulação: hubs emitidos, já que a AGPL significa que qualquer um pode colocar um no ar. Defesa: o status de unidade é conquistado estruturalmente — registro testemunhado, exclusão por controle, rótulo provisório até a federação —, de modo que um hub falso custa o que custa um hub real.

## T4 — Atestado

Um hub ancora, sob sua própria chave institucional, uma **atestação de ocorrência**: esta versão do procedimento foi executada nestas instalações, nesta data, nesta sessão, por esta referência de conta. **Ocorrência, nunca verdade** — o hub atesta o evento que ele hospedou diretamente, não a descoberta. O resultado do replicador e sua declaração de concordância permanecem uma âncora própria, separada e vinculada.

- Uma atestação falsa é uma violação do pacto pelo próprio hub — adjudicável, lida como estrutura, alimentando a leitura de conduta do operador que governa a situação do hub. A atestação tem força porque a reputação de uma instituição está por trás dela.
- Contada em unidades-hub como no T3: muitas execuções atestadas em um mesmo hub são uma única unidade. O número de execuções é renderizado como detalhe e não dimensiona nada.
- **A atestação é um serviço, nunca uma permissão.** Um hub pode recusar-se a hospedar ou atestar qualquer procedimento — agendamento, supervisão e o dever de cuidado ordinário são política local e publicada do hub —, e uma alegação recusada não perde nada em outros lugares: ela é ancorada no T0, percorre o grafo no T1 e é corroborada entre hubs no T3. O cuidado ordinário do local faz o trabalho de segurança sem que nenhum centro se torne uma autoridade de verdade ou de conteúdo.
- Um hub MUST NOT atestar execuções feitas por contas sob seu próprio controle — seu operador, sua equipe agindo como o hub. O vínculo empregatício é uma relação de controle neste nível; uma unidade autoatestada é a raposa contando as galinhas: ela conta zero e carrega o rótulo.
- O custo de emissão do nível é **corpos e tardes** — linear em hubs, sem economias de escala. Essa linearidade, e não qualquer verificação de identidade, é a economia de Sybil.

Um leitor pode inferir que instituições independentes apostaram sua reputação na ocorrência do evento. Um leitor NÃO pode inferir que o resultado está correto — apenas que falsificá-lo agora custa a instituições reais tardes reais, multiplicadas.

---

## Disciplinas que vinculam todos os níveis

- **Vinculação de versão.** Uma replicação vincula-se à versão do procedimento que executou. Um procedimento refinado é uma nova âncora que cita a antiga; o peso acumula-se por versão, com a cadeia visível. Do contrário, o peso se acumula na v1 enquanto a v2 é discretamente entregue por baixo dela.
- **Concordância é dado; violação é conduta.** Uma replicação inconsistente é um fato de concordância, não uma acusação, e nunca é encaminhada como alegação de dano. Somente conduta — fabricação, deturpação do que foi executado, uma atestação falsa — entra no pipeline de alegações do pacto. **Discordância nunca é violação.** Manter os dois canais separados é o que impede que alegações de dano se tornem a arma da disputa científica.
- **Elegibilidade, nunca dimensionamento.** O status de nível determina se uma alegação é elegível para o influxo econômico; o limiar — T3 ou acima, ou apenas T4 na virada da chave — é política governada, não definição de nível. O dimensionamento do pagamento pertence à troca real que ele financia, que carrega a fricção comercial que os níveis não podem carregar.
- **Nenhuma renderização colapsada.** Nenhuma pontuação única, nenhuma estrela, nenhum selo de "verificado". Um nível é renderizado com seu recibo: as replicações, os hubs, a distribuição de concordância, a versão de política em vigor.

## Pedidos a recusar ou sinalizar

- *"Mostre a pontuação geral da alegação."* → Reconstrói a média que o pacto proíbe. Entregue a distribuição.
- *"Impulsione o ranking pela contagem de citações."* → T1 não dimensiona nada, permanentemente.
- *"Deixe o hub atestar as execuções de sua própria equipe."* → Autoatestação vestindo uma chave institucional.
- *"Deixe os hubs cobrarem por posicionamento mais rápido ou em nível mais alto."* → Reputação vendida. O agendamento de atestações é política do hub; a posição no nível nunca pode ser comprada.
- *"Rebaixe automaticamente diante de uma replicação inconsistente."* → Concordância é dado. Renderize-a; nunca a adjudique por relógio ou por contagem.
- *"Marque a alegação como verificada no T4."* → A autoridade de verdade em um casaco mais bonito. Ocorrência, nunca verdade.
- *"Incorpore a reputação comercial ao peso do conhecimento."* → Confunde relações tipadas. Um bom comerciante não é, por isso, um bom proponente.

## Resíduo nomeado

Exclusão geográfica: comunidades sem hub participante não podem alcançar T4 e só alcançam T3 por meio de registro distante — uma lacuna a ser contornada por design (dias itinerantes de atestação, arranjos com hubs parceiros), nunca aceita em silêncio. Partida a frio: contagens de hubs escassas no início significam corroboração escassa; os rótulos provisórios carregam a honestidade até que a federação se adense. Anéis de conluio de humanos reais atravessando hubs continuam possíveis a custo linear; são fraude — território do pacto —, e cada instância adjudicada é uma violação que nunca se dissolve em média.
