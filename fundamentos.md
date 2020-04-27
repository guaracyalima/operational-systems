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
