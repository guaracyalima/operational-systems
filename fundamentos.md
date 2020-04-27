# Fundamentos de sistemas operacionais

## Referências:

- Sistemas Operacionais modernos modernos - Tanenbaum

- Fundamentos de sistemas operacionais - Silberschatz

### Definições
- Camada de software localizada ligeiramente acima do hardware, tendo com uma das atribuições controlá-los.

- Protege os aplicativos de terem que entender caracteristicas de hardware

- Usuá interagem atraz de uma interface, seja ela uma `CLI` (Command Line User Interface), `GUI` (Graphical user interface) ou `MUI` (Manual User Interface - ex.: tela touch)

- Progrmas em modo usuario não podem ser classificados como sendo sistema operacional

### Modos de acesso
|Forma de separação de privilegios|

- Modo usuario => Não consegue acessar diretamente ao hardware (interagem com o modo nucleo)

- Modo Núcleo (supervisor ou kernel) => Possui instruções com privilegios de acesso ao hardware, bem como instruções que não o acessam diretamente

A comunicação entre modo usuário com o modo nuclo é chamada de `system call` ou `chamadas de sistema`

### Fundamentos de SO

- System Call => É o mecanismo usado por um programa em modo usuário para solicitar recursos ao SO via API

- O sistema operacional deve resolver as chamadas direcionadas a ele

- Interrupção de software (Traps || Exceptions) => É utilizada para permitir que um programa em modo usuario passe para oara o modo núcleo e o seu controle para o SO.( o SO para o que está fazendo para dar atenção á solicitação)

- Interface (hardware) => Consiste em um evento onde um dispositivo (hardware) solicita a intervenção do processado eo tratamento pelo SO

- Interrupções permitem o paralelismo nos SO

### SO como maquina estendida

- Ocultar o hardware ( o SO deve ocultar o hardware oferecendo aos aplicativos abstrações claras e simples)


### SO como gerenciador de recursos

- Deve manter o controle sobre quem está usando qual recurso e, atender as requisições dos recursos

- Gerenciar e proteger a memória, os deispositivos de I/O e demais recursos

- Controlar a multiplexação (partila ou compartilhamento) de recursos no tempo e no espaço


## Classificação de SO

### Quanto a quantidade de usuários:

- Monousuário
- Multiusuário

### Quantidade de tarefas:
- Monotarefa (monoprogramção) => Executa apenas uma tarefa por vez
- Multitarefa (multiprogramação) => são executadas concerentemente mais de uma tarefa por vez. Dá suporte á multiplexação


### Quantidade de processadores ou nucleos:

- Monoprocessado
- Multiprocessados => São executadas concorrentemente e/ou simultaneamente (mais de uma tarefa por vez)

## Forma que as aplicações são escalonadas

### Em lote (batch)
- Primeiros sistemas multiprogramados que permitiam sequenciamento automático de tarefas
- Não é realizada a interação do usuário com a aplicação (somente consigo informações ao final do processamento de todo o lote)
- Oferece tempos de resposta longos
- Tem por finalidade uso intensivo de CPU

### Em tempo compartilhado - time-sharing
- Variante da multiprogramação que trabalha com fatias de tempos
- Faz a alternancia de uso da CPU para varias tarefas

### Tempo real - real time
- Existem requisitos rígidos de tempo ( normalmente ambientes críticos onde existe alta disponibilidade)
