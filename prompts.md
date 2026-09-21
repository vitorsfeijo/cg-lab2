# Prompts da conversa

Ferramenta de IA utilizada: ChatGPT luna 5.6

1. como faço a camera olahr mais longe? far plane ser mais longe

Resumo: O `farplane` foi explicado como o limite de renderizacao distante, usando valores mais negativos como `-100.0f`. Para afastar a camera, deve-se aumentar `g_CameraDistance`.

2. como eu faço para fazer um coelho se movimentar no plano?

Resumo: O coelho do meio passou a se mover em uma trajetoria circular no plano XZ usando `cos`, `sin` e `glfwGetTime()`.

3. daria para aumentar o tamanho do plano? ou é melhor diminuir o tamanho dos coelhos?

Resumo: Foi explicado que aumentar o plano e preferivel para preservar o tamanho dos coelhos. O plano foi escalado para `8.0f` e depois ampliado durante a conversa.

4. tem como aumentar a velocidade com qual o scroll aproxima e desaproxima a camera?

Resumo: O fator do zoom no `ScrollCallback` foi aumentado de `0.1f` para `0.3f` e depois ajustado pelo usuario para `1.8f`.

5. g_CameraDistance -= 0.9f*yoffset; pq assim ta dando erro?

Resumo: A expressao era valida em C++, e o erro foi identificado como um falso diagnostico do editor. A conversao explicita `static_cast<float>(0.9 * yoffset)` foi sugerida.

6. da pra colocar os coelhos verde e amarelo parados no canto do plano? eu aumentei bastante ele para ficar como no video

Resumo: Os coelhos verde e amarelo foram colocados em posicoes fixas nos cantos, enquanto o azul continuou se movimentando. Depois, o usuario alterou o plano para escala `20.0f`.

7. consegue tirar a bola?

Resumo: A esfera foi removida da renderizacao, do carregamento do modelo e das definicoes que ficaram sem uso.

8. como eu posso fazer o coelho azul além de ficar em circulos ele ficar subindo e descendo?

Resumo: Foi adicionada uma oscilacao vertical usando `bunny_y = 0.4f * (1.0f + sin(time))`, mantendo X e Z para o movimento circular.

9. como eu faço para fazer ele pular mais rapido?

Resumo: A frequencia do pulo foi aumentada trocando `sin(time)` por `sin(3.0f * time)`.

10. como eu faço para o coelho azul se inclinar para frente enquanto esta subindo e se inclinar para tras enquanto desce do pulo? ele tem q ficar na posição neutra(reto) quando estiver no chão

Resumo: A inclinacao passou a usar `cos` para acompanhar a fase do pulo e fica zerada quando o coelho esta no chao. A amplitude usada foi de aproximadamente `0.35` radianos.

11. como aumenta o raio que o coelho faz o circulo?

Resumo: O raio foi identificado como o multiplicador de `cos` e `sin` na posicao X/Z. Alterar `1.5f`, por exemplo para `5.0f`, aumenta o circulo.

12. eu queria q o coelho girasse para que ele sempre esteja "olhando para frente" enquanto faz o circulo"

Resumo: Foi adicionada uma rotacao horizontal baseada no angulo da trajetoria, usando `Matrix_Rotate_Y(bunny_heading)`.

13. como eu mudo onde é a frente dele?

Resumo: A frente do modelo pode ser corrigida somando um deslocamento ao angulo, por exemplo `bunny_heading = -time + pi` para girar 180 graus.

14. a ideia do video é fazer varios desses coelhos representarem a bandeira do brasil, 8 coelhos azuis ficam girando no centro representando o circulo azul, 14 amarelos ficam girando em um formato de triangulo e 24 verdes ficam em formato de retangulo. mas todos os coelhos tem as transformações de pulo e tilt e de olhar pra "frente"(bunny_heading = -time + 3.141592f / 2.0f; // gira 90 graus)

Resumo: A cena foi ampliada para 46 coelhos: 8 azuis, 14 amarelos e 24 verdes, com salto, inclinacao e orientacao individual.

15. todos os coelhos ficam "andando", os azuis em circulo, os amarelos em um losango(eu tinha errado e falado triangulo), e os verdes no retangulo

Resumo: Os azuis passaram a percorrer o circulo, os amarelos o perimetro de um losango e os verdes o perimetro de um retangulo, todos com movimento continuo.

16. esta quase perfeito, mas eu queria que eles ficassem mais "proximos", o como eu mudo as dimensões do circulo, do losango e do retangulo? eu queria q as variaveis tivessem comentarios doq elas significam e oq elas mudam para que eu possa entender melhor e fazer modificações no codigo

Resumo: As dimensoes foram aproximadas e os parametros receberam comentarios: `circle_radius`, vertices do losango e vertices do retangulo. Tambem foram nomeadas as velocidades e quantidades de coelhos.

17. como eu mudo onde que a camera "nasce"?

Resumo: A posicao inicial da camera e controlada por `g_CameraTheta`, `g_CameraPhi` e `g_CameraDistance`. O ponto observado e definido por `camera_lookat_l`.

18. voce consegue fazer um arquivo chamado prompts.md com todos os prompts que eu te dei nessa conversa em ordem?

Resumo: Foi criado este arquivo com os prompts da conversa em ordem cronologica.
