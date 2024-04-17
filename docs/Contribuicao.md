# Como contribuir?

Esse markdown serve para verificar como contribuir 

## Git workflow

O modelo que vamos seguir se baseia em duas branches principais, a "main" e "development", além das ramificações secundárias para features ou correções de bugs. Essa estrutura torna mais claro o ciclo de vida do desenvolvimento, desde a criação de novas funcionalidades até a implantação de versões estáveis.

### Diagrama do git flow

![02_Feature_branches.svg](docs/img/gitflow.jpeg)

#### Fluxo de Desenvolvimento

Primeiramente, **cada nova mudança deve ser desenvolvida em uma branch exclusiva**, o que facilita o gerenciamento de mudanças e a colaboração da equipe.

Uma vez que a mudança está pronta para ser incorporada ao projeto, um "Merge Request" (MR) deve ser aberto para a branch "development". Isso permite que a equipe revise a alteração, compartilhe feedback e assegure a aderência aos padrões de qualidade e ao objetivo do projeto.

Após a aprovação e testes bem-sucedidos em um ambiente de teste ou "stage", a alteração está pronta para ser mesclada na branch "development". Somente após ter sido testada e aprovada nesse ambiente que um commit de "development" para "main" deve ser realizado. Essa abordagem ajuda a manter a branch "main" como uma representação estável e confiável do código do projeto, garantindo que apenas as alterações devidamente validadas sejam incorporadas à versão principal.

#### Nomeclatura de branches

A nomeclatura de branches que segue o padrão **"tipo-da-mudança/descrição"** é uma abordagem estruturada e informativa para gerenciar branches em repositórios de controle de versão, especialmente no contexto de commits convencionais. Essa convenção de nomenclatura utiliza tokens derivados dos tipos de mudanças definidos no padrão de commits convencionais para categorizar as branches de forma clara e compreensível.

A estrutura **"tipo-da-mudança/nome-descritivo"** pode ser desdobrada da seguinte maneira:

1. **Tipo da Mudança (Token)**: O tipo da mudança é um token que descreve a natureza da alteração que está sendo realizada na branch. Esses tokens são extraídos dos tipos descritos no Conventional Commits, e estão descritos na seção `Politica de Commits.`

2. **descrição**: É uma breve descrição que esclarece o propósito da branch de forma clara e concisa. Deve explicar o que está sendo desenvolvido na branch, para que outras pessoas da equipe possam entender facilmente a sua finalidade.

Por exemplo, se você estiver criando uma branch para adicionar um novo recurso de pesquisa em um projeto de software, a nomeclatura pode seguir o formato "feat/relatorio-mobilizacao" ou "feat/busca." Isso torna evidente que a branch se destina à implementação de um novo recurso de pesquisa.

## Politica de Commits

A nossa política de commits adota o padrão Conventional Commits como diretriz fundamental para o registro de alterações no nosso código. Este padrão incentiva a clareza e consistência nas mensagens de commit, facilitando a compreensão e rastreamento das mudanças ao longo do tempo.

Padrão de commit

### **prefixo(sufixo): descrição**

**Exemplo**:

```markdown
docs(dag-notificacao-proposta): documentação inicial da dag de envio de mensagem de novas propostas.
```

### Prefixo

- **feat**: Utilizado para novas funcionalidades ou adições ao código. Feat de features.
- **fix**: Usado para correções de bugs.
- **chore**: Geralmente associado a tarefas de manutenção, ajustes de configuração ou outras atividades não relacionadas a funcionalidades ou bugs.
- **docs**: Reservado para alterações na documentação.
- **refactor**: Utilizado quando há refatoração de código sem alterar comportamento externo.
- **test**: Associado a adições ou modificações nos testes.
- **build**: Relacionado a mudanças no sistema de build ou dependências.
- **ci**: Envolvendo ajustes ou melhorias em configurações de integração contínua.
- **perf**: Usado para melhorias de desempenho.
- **revert**: Utilizado para reverter uma alteração anterior.

### Sufixo

No sufixo, deve estar em parentese aonde que está sendo feita a mudança, seguido de dois pontos e sua mensagem.

## Revisão e qualidade do código

Para manter a qualidade do código, adotamos uma série de medidas automatizadas e de padrão de código.

## Todo código deve ter seu arquivo de testes e deve passar na análise estática do Mypy.
    - ***Justificativa:*** Incorporar testes unitários e análise estática com o MyPy é crucial para assegurar a robustez do código. O MyPy, ao realizar verificações estáticas de tipo, ajuda a identificar potenciais bugs antes que o código entre em produção, aumentando a confiança na qualidade do software.
