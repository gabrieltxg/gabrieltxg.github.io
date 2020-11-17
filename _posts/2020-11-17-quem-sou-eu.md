---
layout: post
title: "Sobre mim e sobre o que eu faço"
author: "Gabriel"
categories: 
tags: [caos]
image: chirikov_401_x0_1000.png
---

Alô! 

Meu chamo Gabriel, sou formado em Astronomia e faço mestrado na mesma área no IAG-USP. Minha pesquisa se baseia no estudo de sistemas dinâmicos não lineares, métodos de detecção de caos e análise de estabilidade dinâmica através de cálculos sobre difusão caótica. 

Uma vez que me trabalho desde a graduação era puramente teórico e computacional, tenho feito desde lá um intenso uso de ferramentas de programação, principalmente em Python. No entanto, antes do mestrado trabalhei intensamente com análise de dados no setor público, onde aprendi a usar fora da faculdade muito do que aprendi nela. Neste trabalho meu interesse em ciência e engenharia de dados cresceu neste trabalho e hoje faço projetos paralelos ao meu projeto de mestrado, nas horas livres, bem como sigo estudando métodos e algoritmos.

Meu interesse, no entanto, não se limita à minha pesquisa acadêmica e aos conhecimentos que adquiri no trabalho. Meu apetite por matemática e pela física é generalizado. tenho um grande interesse por ecologia teórica e por redes de interação como sistemas dinâmicos. Para além da academia, gosto de literatura --- principalmente russa e japonesa --- e música da ásia central, além de conhecer e estudar alguns idiomas (no momento tô lutando pra dominar o alemão, espero que logrando êxito).

### Mas e a imagem ali em cima?

Ah! sobre a imagem do topo, fiz ela para o meu TCC, onde iniciei estudos sobre fenômenos caóticos. Sistemas dinâmicos não lineares --- ou sistemas caóticos --- são aqueles que, por definição, contém sensibilidade às condições iniciais do sistema e/ou a um parâmetro de controle. No caso da imagem acima, o que eu fiz foi trabalhar com o sistema discreto definido pelo físico soviético Boris Chirikov em 1969 e chamado Mapa Padrão:

$$x_{i+1} = x_{i} + K \sin (y_{i+1}), \\ y_{i+1} = y_{i} + x_{i}.$$

Eu fiz 1000 iterações das equações acima para 401 condições iniciais $x_{0}$ e 401 de $y_{0}$, de modo que obtive, ao final 160.801 trajetórias diferentes. O Parâmetro de controle $K$ utilizado foi $K=1.3$. 

Em seguida, fiz uma análise de cada uma das 160.801 trajetórias diferentes de modo a saber se elas são regulares --- tem períodos e trajetórias previsíveis --- ou se elas são caóticas --- ou seja, instáveis, irregulares e com baixa previsibilidade. A ferramente que eu utilizei para realizar essa análise foi o __Fast Lyapunov Indicator, (FLI)__, desenvolvido por Fouchard et al (2000). O FLI se baseia na análise da divergência exponencial da trajetória com relação às suas condições iniciais --- intimamente relacionado com o Expoente de Lyapunov, clássica ferramenta para análise de fenômenos caóticos. O FLi é definido como 

$$\dot{\vec{v}}(t) = Df(x, y,...)\vec{v}(t),$$

onde $v(t)$ é um vetor tangente inicial qualquer e $Df(x, y,...)$ é a matriz jacobiana do sistema de equações que rege a dinâmica do sistema.

Assim, a imagem representa um __mapa dinâmico__ deste sistema e indica quais condições iniciais são regulares --- zonas mais claras --- e quais são caóticas --- quais são mais escuras.
