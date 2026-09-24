# Relatório - Coelinhos do Brasil

> [!CAUTION]
> - Lembre-se que você <ins>**não pode utilizar ferramentas de IA para
>   escrever este relatório**</ins>

## Dados do aluno

- **Cartão UFRGS**: 588403
- **Nome**: Vítor Santana Feijó

## Passos que eu segui para resolver o problema especificado (em formato de *"prompt"*)

> [!IMPORTANT]
> - Coloque aqui todas as informações necessárias para que alguém
>   (pessoa ou ferramenta de IA) possa reproduzir os seus passos para
>   solucionar o problema
> - Escreva em formato imperativo, como se fosse um *prompt* com as
>   instruções a serem seguidas na solução do problema
> - Seja objetivo e conciso: quanto *menos palavras* você utilizar,
>   melhor
> - Seja técnico e use terminologia adequada: assuma que quem irá ler
>   os seus passos possui conhecimento de Ciência da Computação e
>   Computação Gráfica
> - Caso você queira incluir informações "longas" (como algum *prompt*
>   grande usado com alguma ferramenta de IA), crie arquivos à parte e
>   adicione links no texto (por exemplo, crie o arquivo `PROMPTS.md`
>   e adicione um link markdown `[os prompts detalhados estão
>   aqui](PROMPTS.md)`)
> - Novamente, lembre-se que você *não pode utilizar ferramentas
>   de IA para escrever este relatório*


[os prompts detalhados estão aqui](PROMPTS.md)

1. Faça o coelho realizar transformações para que as coordenadas em Y(salto) mude em relação ao tempo entre um intervalo de 0 até 0.8.
`
bunny_y = 0.4f * (1.0f + sin(jump_velocity * jump_time));
`
2. Faça o coelho realizar transformações para que as coordenadas em Z(tilt durante o salto) mude em relação ao tempo entre um intervalo de -0.35 até 0.35.
`
bunny_tilt = 0.35f * cos(jump_velocity * jump_time);
`
3. Faça o coelho realizar transformações para que as coordenadas em Y mude em relação ao tempo que mude o seu ângulo da direção frontal do coelho.
`
float heading = -angle + 3.141592f / 2.0f;
`
4. Faça 8 coelhos azuis ficarem andando em um circulo azul, 14 amarelos andando em um formato de losango fora do círculo e 24 verdes andando em forma de retangulo fora do retangulo. Todos mantendo as transformações anteriores.

5. Achate a bola em y(e diminua o tamanho geral da bola) e faça ela se mover junto com os coelhos.

6. Arrume as constantes para que fique igual a do video

## Principais dificuldades encontradas durante o desenvolvimento (formato livre)

- O começo foi mais desafiador pelo pouco entendimento da biblioteca opengl
- O mudar o ângulo fronta do coelho para que ele fique "olhando para frente".


## Você acha que conseguiu resolver o problema de forma adequada?

Acredito que sim, o meu trabalho está bastante semelhante ao video.

## Se você quiser compartilhar mais alguma coisa, coloque aqui:



## Se você possui alguma sugestão para o professor sobre esta atividade, coloque aqui:


