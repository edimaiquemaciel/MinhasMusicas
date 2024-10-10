# Minhas Músicas e Podcasts

Este projeto em Java permite gerenciar músicas e podcasts, contando suas reproduções, curtidas e classificações. O sistema também identifica quais são os áudios mais apreciados e classifica-os como "sucesso absoluto" ou "preferido por todos".

## Funcionalidades

- **Música**: 
  - Armazenar título, cantor, álbum, e gênero.
  - Registrar reproduções e curtidas.
  - Atribuir uma classificação baseada no número de curtidas.
  
- **Podcast**: 
  - Armazenar título, apresentador e descrição.
  - Registrar reproduções e curtidas.
  - Atribuir uma classificação baseada no número de curtidas.

- **Minhas Preferidas**:
  - Identificar áudios (músicas ou podcasts) que possuem classificação alta.
  - Exibir mensagem indicando se um áudio é um sucesso ou preferido.

## Estrutura do Projeto

O projeto está organizado em pacotes e classes da seguinte maneira:

### Pacote: `br.com.alura.minhasmusicas.principal`

- **Classe `Principal`**:
  - Ponto de entrada do programa. Cria e simula reproduções e curtidas de uma música e um podcast.
  - Chama a classe `MinhasPreferidas` para verificar quais são os áudios com alta classificação.

### Pacote: `br.com.alura.minhasmusicas.modelos`

- **Classe `Audio`**:
  - Classe base para músicas e podcasts.
  - Contém os métodos para reproduzir, curtir e calcular a classificação geral de um áudio.

- **Classe `Musica`**:
  - Extende `Audio` e adiciona atributos específicos, como álbum, cantor e gênero.
  - Define uma regra personalizada para a classificação da música, baseada nas curtidas.

- **Classe `Podcast`**:
  - Extende `Audio` e adiciona atributos como apresentador e descrição.
  - Define uma regra de classificação para podcasts, diferente da regra para músicas.

- **Classe `MinhasPreferidas`**:
  - Avalia se um áudio é considerado um "sucesso absoluto" ou "preferido por todos" com base na sua classificação.
  
## Exemplo de Execução

Após a execução do programa, a saída será algo assim:

```
Forever também é um dos que todo mundo está curtindo
BolhaDev é considerado sucesso absoluto e preferido por todos
```

Isso significa que a música "Forever" é apreciada, mas não atingiu o status de "sucesso absoluto", enquanto o podcast "BolhaDev" foi altamente curtido e considerado um sucesso.

## Como Rodar o Projeto

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/edimaiquemaciel/MinhasMusicas.git
   ```

2. **Compile e execute** o arquivo `Principal.java` na sua IDE favorita ou via linha de comando.

## Estrutura do Código

```bash
src/
├── br/com/alura/minhasmusicas/modelos/
│   ├── Audio.java
│   ├── Musica.java
│   ├── Podcast.java
│   └── MinhasPreferidas.java
└── br/com/alura/minhasmusicas/principal/
    └── Principal.java
```

## Tecnologias Utilizadas

- **Java 11** ou superior

## Melhorias Futuras

- Implementar persistência de dados para salvar as músicas e podcasts em um banco de dados.
- Criar uma interface gráfica para facilitar a navegação e gestão dos áudios.
- Adicionar a possibilidade de remover músicas e podcasts da lista de preferidos.

## Licença

Este projeto está licenciado sob os termos da licença MIT. Para mais informações, veja o arquivo [LICENSE](LICENSE).
