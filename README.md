# Projeto Computacional 1 — Pac-Man

## Descrição

Este projeto consiste no desenvolvimento de uma versão simplificada do jogo **Pac-Man**, utilizando Python e a biblioteca Pygame.

O projeto implementa um sistema básico de movimentação do personagem em um mapa formado por nós (`Node`), permitindo que o Pac-Man se movimente entre diferentes pontos do mapa de acordo com as teclas direcionais pressionadas pelo jogador.

A estrutura do projeto foi desenvolvida utilizando conceitos de **Programação Orientada a Objetos (POO)**, separando responsabilidades entre classes e módulos.

## Justificativa

O projeto foi desenvolvido com o objetivo de aplicar, de maneira prática, conceitos de Programação Orientada a Objetos e programação de jogos.

A implementação de um jogo simples permite trabalhar com conceitos como:

* Criação e utilização de classes e objetos;
* Atributos e métodos;
* Métodos especiais do Python;
* Organização do código em diferentes módulos;
* Representação de posições utilizando vetores;
* Movimentação baseada em tempo;
* Tratamento de eventos do teclado;
* Estruturas de dados para representar conexões entre diferentes pontos do mapa.

Além disso, o projeto permite compreender como diferentes objetos podem trabalhar juntos para formar um sistema maior.

## Funcionalidades

O projeto possui as seguintes funcionalidades:

* Criação de uma janela utilizando Pygame;
* Representação de um mapa através de nós conectados;
* Criação do personagem Pac-Man;
* Movimentação do Pac-Man através das teclas direcionais;
* Verificação de movimentos válidos;
* Identificação do próximo nó de destino;
* Detecção de quando o Pac-Man alcança ou ultrapassa seu destino;
* Possibilidade de inverter a direção do personagem;
* Renderização dos nós, conexões e personagem na tela;
* Controle da movimentação utilizando `delta time`, tornando o movimento independente da quantidade de frames por segundo.

## Temas abordados

Durante o desenvolvimento do projeto foram abordados os seguintes conceitos:

### Programação Orientada a Objetos

* Classes;
* Objetos;
* Construtores (`__init__`);
* Atributos;
* Métodos;
* Relacionamento entre objetos;
* Organização de responsabilidades entre classes.

### Python

* Variáveis e constantes;
* Dicionários;
* Listas;
* Condicionais;
* Laços de repetição;
* Importação de módulos;
* Métodos especiais (`dunder methods`);
* Operadores personalizados através de métodos como `__add__`, `__sub__`, `__mul__` e `__eq__`.

### Matemática e vetores

A classe `Vector2` é utilizada para representar posições e direções no espaço bidimensional.

Também é utilizado o conceito de **magnitude ao quadrado** (`magnitudeSquared`), calculado através de:

```text
x² + y²
```

Essa operação permite comparar distâncias sem a necessidade de calcular a raiz quadrada, sendo útil para verificar se o Pac-Man chegou ou ultrapassou determinado ponto.

### Desenvolvimento de jogos

* Game loop;
* Atualização por frame;
* `delta time`;
* Entrada do teclado;
* Renderização;
* Coordenadas 2D;
* Movimentação de personagens.

## Tecnologias

As principais tecnologias utilizadas no desenvolvimento foram:

* **Python 3**
* **Pygame**
* **Git**
* **GitHub**

## Bibliotecas

### Pygame

O projeto utiliza a biblioteca **Pygame** para criar a janela do jogo, desenhar os elementos na tela, receber eventos do teclado e controlar o tempo entre os frames.

```python
import pygame
```

### Math

A biblioteca padrão `math` do Python é utilizada principalmente para operações matemáticas relacionadas aos vetores, como o cálculo de raiz quadrada utilizado na magnitude.

```python
import math
```

## Estrutura do projeto

O projeto está dividido em diferentes arquivos, com cada módulo possuindo uma responsabilidade específica:

```text
poo-projeto-computacional-1/
│
├── constants.py
├── vector.py
├── nodes.py
├── pacman.py
├── run.py
└── README.md
```

### `constants.py`

Contém constantes utilizadas pelo projeto, como:

* Dimensões da tela;
* Dimensões dos tiles;
* Cores;
* Direções de movimentação.

### `vector.py`

Implementa a classe `Vector2`, responsável pela representação de vetores bidimensionais.

A classe permite realizar operações matemáticas como:

```python
vetor1 + vetor2
vetor1 - vetor2
vetor * numero
vetor / numero
```

Além disso, possui métodos para calcular a magnitude, obter a magnitude ao quadrado e converter o vetor para outros formatos.

### `nodes.py`

Implementa os nós utilizados para representar o mapa.

Cada `Node` possui uma posição e pode possuir vizinhos nas quatro direções:

```text
UP
DOWN
LEFT
RIGHT
```

A classe `NodeGroup` é responsável por armazenar e organizar os nós do mapa.

### `pacman.py`

Implementa o personagem Pac-Man.

A classe controla:

* Posição;
* Direção;
* Velocidade;
* Nó atual;
* Nó de destino;
* Movimentação;
* Entrada do teclado;
* Verificação de direção;
* Detecção de chegada ao destino.

### `run.py`

É o ponto de entrada da aplicação.

Responsável por:

* Inicializar o Pygame;
* Criar a janela;
* Criar o mapa;
* Criar o Pac-Man;
* Executar o game loop;
* Atualizar o estado do jogo;
* Processar eventos;
* Renderizar os elementos.

## Distribuição das Tarefas

| Integrante             | Tarefas                                                    |
| ---------------------- | ---------------------------------------------------------- |
| [Daniel Esmeraldo & João Peixoto] | Implementação da classe `Vector2` e operações matemáticas  |
| [Daniel Esmeraldo & João Peixoto] | Implementação dos nós e estrutura do mapa                  |
| [Daniel Esmeraldo & João Peixoto] | Implementação da classe `Pacman` e sistema de movimentação |
| [Daniel Esmeraldo & João Peixoto] | Implementação do `GameController`, integração e testes     |

## Referência

O desenvolvimento da lógica de movimentação e da estrutura utilizada no projeto teve como referência o material disponível no **Pacman Code**:

**Pacman Code:** https://pacmancode.com/

O site apresenta materiais relacionados à implementação de um jogo inspirado em Pac-Man, incluindo conceitos de movimentação, vetores, nós e organização da lógica do jogo.

## Como executar

Primeiramente, é necessário possuir o Python 3 instalado.

Depois, instale o Pygame:

```bash
pip install pygame
```

Clone o repositório:

```bash
git clone https://github.com/Dan1Ems/poo-projeto-computacional-1.git
```

Entre na pasta do projeto:

```bash
cd poo-projeto-computacional-1
```

Execute o programa:

```bash
python run.py
```

## Conclusão

O projeto possibilitou a aplicação prática dos conceitos de Programação Orientada a Objetos em um sistema interativo.

A divisão do programa em classes como `Vector2`, `Node`, `NodeGroup`, `Pacman` e `GameController` permite organizar melhor o código e separar as diferentes responsabilidades do jogo.

Além dos conceitos de POO, o projeto também possibilitou o aprendizado de conceitos relacionados ao desenvolvimento de jogos, como movimentação, vetores, entrada de teclado, renderização e controle de tempo.
