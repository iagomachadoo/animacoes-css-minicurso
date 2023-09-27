# Animacoes CSS - Minicurso

## Tipos de animações 

- [Artigo](https://desenvolvimentoparaweb.com/ux/motion-ui-principios-tipos-animacao-interface/#:~:text=Colocando%20tudo%20isso%20em%20conjunto,%3A%20Funcional%2C%20Material%20e%20Encantador.)

- É possível categorizar animações de interfaces em 3 tipo:
    - Funcional 
        - Otimiza a experiência

        - Guia a atenção

        - Feedback + Preparação

    - Material 
        - Modelos consistentes de UI

        - Relações espaciais entre telas e elementos

    - Encantador
        - Humanidade e diversão

        - Algo único e memorável

        - Entretenimento + relacionamento

## Preliminares - transform e transition
- A propriedade Transform
    - Essa propriedade em CSS é usada para aplicar transformações 2D ou 3D a elementos HTML

    - Ela permite que você altere a posição, rotação, escala e inclinação de um elemento sem afetar o layout do documento

    - As transformações aplicadas usando a propriedade transform não alteram o fluxo normal dos elementos na página, o que é útil para criar animações e efeitos visuais sem interferir no layout

    - A propriedade transform pode aceitar várias funções de transformação como valores.

    - Podemos encadear várias dessas funções em uma mesma propriedade, contudo, devemos ter cuidado na hora de sobrescrever propriedades com multiplas funções. Para isso, é necessário reescrever as demais funções que não foram alteradas
        -   ```
                // Errado
                .box{
                    transform: translateX(100px) scale(2) rotate(90deg);
                    transform: translateX(200px);
                }

                // Correto
                .box{
                    transform: translateX(100px) scale(2) rotate(90deg);
                    transform: translateX(200px) scale(2) rotate(90deg);
                }
            ```

- A propriedade Transition
    - É usada para criar animações suaves entre diferentes estados de um elemento quando ocorre uma mudança em suas propriedades. Essa propriedade permite controlar a transição de propriedades CSS, como cor, tamanho, posição e outros, de um estado para outro de forma gradual e controlada. Isso cria uma experiência mais agradável e visualmente atraente para os usuários.

    - Consiste em 4 valores principais
        - Propriedades a serem transitadas

        - Duração da transição

        - Função de temporização (timing function)

        - Atraso (delay)

## Keyframe
- As regras @keyframe são usadas para definir animações personalizadas e controladas que podem ser aplicadas a elementos HTML.

- Elas permitem criar animações suaves ao longo do tempo, especificando como as propriedades CSS de um elemento devem mudar em diferentes estágios da animação.

- Sintaxe 
    -   ```
            @keyframes nome-da-animacao {
                /* Definições de animação */
            }

        ```

- Exemplo 
    -   ```
            @keyframes moverDireita {
                from {
                    transform: translateX(0);
                }
                to {
                    transform: translateX(100px);
                }
            }

            elemento {
                animation: nome-da-animacao duração-totalsegundos opcoes-de-animacao;
            }
        ```