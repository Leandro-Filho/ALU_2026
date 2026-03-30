# Projeto Março - 2026 Engenharia de Computação

## Sobre o Projeto

Este projeto foi desenvolvido como um trabalho prático para a aula de programação do Inteli (Instituto de Tecnologia e Liderança). O objetivo foi projetar e construir do zero uma Unidade Lógica Aritmética (ALU) de 8 bits, compreendendo na prática como o "cérebro" de um computador processa operações matemáticas e lógicas no nível de hardware (portas lógicas, flip-flops e roteamento de bits).

---

## Como Funciona (Resumo da Arquitetura)

O fluxo de dados funciona da seguinte maneira:

### Entradas
O circuito recebe dados de duas fontes principais:
- Um pino externo (**N**)
- O próprio registrador **Acumulador (AC)**

### Processamento Paralelo
Os dados entram simultaneamente em todos os blocos de operação construídos bit a bit no projeto.

As operações disponíveis são:

#### Aritméticas
- Somador/Subtrator (com tratamento de Overflow)
- Multiplicador
- Divisor

#### Deslocamentos (Shifts)
- Shift Left
- Shift Right  
*(Deslocamento físico de fios, equivalente a multiplicar ou dividir por 2)*

#### Lógicas
- NAND
- XOR  
*(operações bit a bit)*

### Seleção (MUX)
Um multiplexador principal, controlado por um sinal de **Opcode de 3 bits**, escolhe qual das respostas paralelas será utilizada.

### Armazenamento (Registradores AC e MQ)
- O resultado da operação escolhida é salvo no registrador principal **AC** a cada pulso de **Clock**.
- Para operações que excedem 8 bits (como:
  - bits mais significativos da multiplicação  
  - quociente da divisão  
), o circuito utiliza um registrador auxiliar chamado **MQ**.
- Isso evita perda de dados.

Os registradores foram construídos do zero utilizando **Flip-Flops tipo D**.

---

## Como Abrir e Executar

Para acessar os arquivos `.dig`, você deve ter a ferramenta simuladora de circuitos **Digital.jar** (H. Neemann) em seu computador.

### Passos para execução

1. Certifique-se de ter o **Java** instalado.
2. Abra o executável `Digital.jar`.
3. No menu:
   - Clique em **Arquivo > Abrir**
   - Navegue até a pasta onde você clonou este projeto
   - Abra um dos arquivos `.dig`

---

## Como posso ver funcionando?

Acesse esse seguinte link e será levado ao vídeo: [Ir para o Vídeo](https://www.youtube.com/watch?v=wWu-E5x5PjM).