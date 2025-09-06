# 🎮 PokéParty 🥳

## Sobre o app:

Como neste ano comemoro uma idade bastante emblemática da minha vida, ~~30~~ 20 anos, resolvi planejar (com antecedência para não poder desistir quando chegar o dia) uma festa com a temática de um dos meus jogos favoritos: Pokémon.

Convidei meus amigos para uma festa na qual eles tem que confirmar a presença e, de quebra, me informar qual a cor de roupa irão & o Pokémon que inspirou a escolha.

Infelizmente, por conta do pouco tempo entre a ideia e a data, não consegui desenvolver nem um site para isso, então tive que usar uma planilha. Porém, nesta disciplina, irei desenvolver a ideia e criar, de fato, um app para esse registro de presença e escolhas dos convidados.

O app mostrará, de imediato, uma lista de todos que já confirmaram presença;

Também deve permitir que os convidades confirmem seu nome e confirmem um pokémon de sua escolha para a caracterização da festa.

O detalhe é que: ninguém pode repetir o pokémon do outro (afinal existem 1025 pokémons) então eu precisava que, além do nome, todos pudessem visualizar as escolhas de pokémons que já foram feitas para não repetir.

Após a confirmação, o nome e o pokémon aparecem na lista juntamente com uma imagem do pokémon escolhido - apenas para título de ilustração mesmo, tornar mais dinâmico.

Possíveis funcionalidades adicionais/futuras: poder clicar em cada pokémon já selecionado e ser levado à pokédex oficial da franquia, falando sobre aquele pokémon.

## Funcionalidades:

Organizar funcionalidades a serem implementadas, atualizadas a cada Checkpoint

- [ ] 1. Visualizar confirmações anteriores;
- [ ] 2. Poder realizar a confirmação de presença;
- [ ] 3. Poder realizar a escolha do Pokémon;
- [ ] 4. Caso o Pokémon já tenha sido escolhido, o sistema não registra a presença e solicita que a escolha de Pokémon seja mudada;
- [ ] 5. Após a confirmação, o usuário visualiza seu nome e escolha de Pokémon na lista.
        
## 🖼️ Protótipos de tela: 

[Figma - com protótipo navegável](https://www.figma.com/design/LHuHm5ywInZrjJENh0Nezo/Pok%C3%A9Party?node-id=3-41429&t=Psyi8FBeSv6wkiwN-1)

## 🏦 Modelagem do banco: 

1. O banco de dados utilizado será do tipo relacional, composto por uma única tabela chamada Convidados. Esta escolha se dá pelo fato de ser relativamente simples (em teoria) de se conseguir o que se espera de uma lista assim.
2. Esta tabela armazena os dados necessários para gerenciar as confirmações de presença e a escolha de pokémons dos convidados da festa.

Entidade: Convidado
Atributos:

    id (inteiro, chave primária, autoincremento)
    nome (texto, obrigatório)
    pokemon (texto, obrigatório, único)
    presenca (booleano, obrigatório)

Exemplo de tabela:
| id | nome  | pokemon | presenca | data_confirmacao       |
|----|-------|----------|----------|------------------------|
| 1  | Ash   | Pikachu | true     | 2025-09-06 14:00:00    |
| 2  | Misty | Psyduck | true     | 2025-09-06 14:05:00    |



---

<!-- Projetar a modelagem do banco de dados (seja local ou remoto) e incluir um link para visualização pública no Readme.md

Se o banco for relacional, apresente um diagrama entidade relacionamento representando as tabelas, relações e atributos;

Se o banco for NoSQL, apresente os Schemas dos dados gerados, acessados ou manipulados pelo app;

Se não houver persistência de dados local e o banco for completamente remoto, como uma API manipulada pelo App, envie a modelagem do banco de dados remoto (ou a parcela manipulada pelo App, caso o contexto total seja muito abrangente);

Dica: você pode usar a ferramenta https://app.diagrams.net/ (antigo draw.io) para produzir essas modelagens e gerar um link de visualização pública. Alternativamente, você pode usar outra ferramenta de sua preferência, exportar como imagem e incluir no próprio Readme usando a tag de imagem do markdown ou ainda hospedar no Google Drive, com link público.

-->

## 🏃 Planejamento de sprints: 

Incluir um cronograma de sprints a realizar até a conclusão do App. 

Planeje cada requisito a ser implementado, elabore uma previsão (em semanas) de quanto tempo levará para desenvolver cada recurso.

Quanto mais detalhado e realista for o seu planejamento, melhor será a avaliação neste requisito.

### Sprint 0: Planejamento (1 semana)
- Criação do repositório inicial
- Estudo das técnicas a serem utilizadas
- Definifição da estrutura do app
- Prototipagem no Figma
###### Entregáveis:
- README.md
- Protótipos iniciais no Figma

### Sprint 1: Funcionalidades básicas e estrutura (1 semana)
- Criação da tela inicial
- Cadastro de convidados
- Estruturação de lista de confirmação visível assim que acessar o app
###### Entregáveis:
- Lista de confirmação
- App básico

### Sprint 2: Confirmação de presença + escolha de Pokémon (2 semanas)
- Campo para confirmar presença
- Campo para confirmar pokémon
- Implementação de regra para impedir escolha repetida de pokémon
###### Entregáveis:
- Fluxo completo de confirmação (presença + pokémon)
- Validação da escolha
- Atualização de lista

### Sprint 3: Visualização detalhada e imagens (1 semana)
- Exibição da imagem do Pokémon escolhido ao lado do nome do convidado
- Feedback visual após confirmação
- Melhorias contínuas na interface
###### Entregáveis:
- Lista com imagens de pokémons
- Feedback para usuários - de confirmação ou de erro

### Sprint 4: Persistência de dados e banco (2 semanas)
- Implementação de banco de dados (decidir com antecedência se será local ou remoto)
- Integração com API (se necessário)
- Testes de persistência de dados
###### Entregáveis:
- Dados persistidos corretamente
- App recuperando dados do banco para iniciar

### Sprint 5: Ideias futuras e refinamento (1 semana)
- Adicionar link para pokédex oficial ao clicar no pokémon escolhido
- Refinamento de UI/UX
- Realização de testes
- Documentação final

###### Entregáveis:
- App completo
- Documentação revisada

#### Cronograma resumido
| Sprint        | Duração   | Entregas                          |
|---------------|-----------|---------------------------------------------|
| Sprint 0      | 1 semana  | Protótipo, modelagem banco                  |
| Sprint 1      | 1 semana  | Estrutura básica, lista convidados          |
| Sprint 2      | 2 semanas | Confirmação presença, escolha Pokémon       |
| Sprint 3      | 1 semana  | Imagem Pokémon, feedback visual             |
| Sprint 4      | 2 semanas | Persistência de dados, backend/API          |
| Sprint 5      | 1 semana  | Refino, Pokédex, documentação               |
