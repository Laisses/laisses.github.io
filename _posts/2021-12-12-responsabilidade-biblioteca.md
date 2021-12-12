---
layout: post
title: Tu te tornas eternamente responsável pela biblioteca que instalas
date: 2021-12-12
---

Ontem eu finalizei mais um curso da minha formação. Nesse projeto diversas bibliotecas foram instaladas para "facilitar a nossa vida", com direito a posts sobre as vantagens e links para bibliotecas famosas. Mas o que eu queria saber é: e qual é o custo?

<!--more-->

Essa questão me incomoda desde a primeira vez que eu usei o Bootstrap em um curso de front-end. Não há dúvida de que essa é uma ferramenta muito útil e versátil, mas ela é necessária para uma estilização simples? Bem... não. Talvez valha a pena se familiarizar e aprender a usar porque nunca se sabe o que vamos encontrar pela frente, mas usar essa biblioteca quando o objetivo é justamente aprender HTML e CSS me soa como oportunidade perdida.

A segunda biblioteca que eu encontrei foi a Moment.js, e aquele sentimento de oportunidade perdida voltou. Mas dessa vez eu fiz diferente, e fui aprender como tratar datas na mão. Foi demorado, devagar, sofrido, por vezes desesperador e cansativo, e também foi extremamente recompensador. Não só por conseguir, o que implica (é claro) na dancinha da vitória, mas também porque existe valor na evolução da aprendizagem. É um processo que envolve descobrir como pesquisar, filtrar respostas, ler documentação (e reler, e reler, e reler e depois procurar um site que explique a documentação), pedir ajuda e se comunicar. E isso não tem curso que ensine.

Foi com essa bagagem e com essa mentalidade que eu cheguei ao curso que motivou esse post. Dessa vez no back-end, fazendo a minha primeira API. Especificamente, uma API REST no Node.js com Express. Nesse curso novos conceitos foram apresentados, como: `package.json`, `package-lock.json`, `dependencies`, `devDependencies`, modules e etc. E nesse curso foram utilizados o express, nodemon, MySQL, consign e moment. Eu não usei moment nem consign, a primeira eu já expliquei o porquê, e a segunda porque eu não entendi para que serve e o meu programa funcionou sem usar. Mas mesmo não usando bibliotecas que eu julguei não serem necessárias, alguma coisa continuou me incomodando. Depois de uns dias de reflexão eu percebi que me aborrecia o uso aparentemente indiscriminado e a falta de discussão sobre vantagens e desvantagens, porque tem desvantagem.... Certamente deve... né?  

O fato é que existe um custo. Não exatamente da natureza que eu imaginei, mas lá está ele. A verdade é que a minha hipótese de programadora iniciante é que deveria ter algo a ver com performance. Como tudo que eu fiz até hoje é minúsculo, quando eu olhei o `package-lock` pela primeira vez e vi 85 bilhões de dependências eu achei que qualquer coisa extra que eu colocasse ali ia ser demais. Não era esse o problema, e eu descobri que é tudo sobre dependências, e as dependências das dependências. Porque se uma dessas para de funcionar, tudo para de funcionar, e aí quem conserta? Eu? Para responder essa dúvida eu me deparei com um ninho de vespas! Pelo título do post dá para saber qual é a minha opinião sobre o assunto. Mas vamos lá falar sobre qual é a treta.

O negócio é o seguinte: existe uma discussão sobre quem é, ou quem deveria ser o mantenedor de softwares de código aberto, e nós temos uma cultura que diz que o criador é o responsável. Muitas pessoas escolhem esse caminho porque gostam do projeto que construíram e querem continuar relevantes, e tudo bem isso. O problema é que a comunidade passa a exigir muito, e os desenvolvedores que atendem à essa comunidade vem relatando episódios de burnout e depressão. Esse foi inclusive o caso do Tim Wood, que escreveu a moment, e [deixou o projeto em 2016][moment] para cuidar da sua saúde mental depois de ter depressão relacionada ao trabalho.

Eu li mais alguns artigos de pessoas contando suas histórias de burnout em comunidades de código aberto e como a [demanda para entregar softwares cada vez com mais rapidez][burnout] e o [ambiente tóxico][ambiente-toxico] proveniente de interações negativas são os grandes responsáveis. Inclusive, eu achei [uma pesquisa][pesquisa] que teve por objetivo encontrar, entender e mitigar interações danosas nas comunidades de código aberto, fazendo um paralelo direto entre estresse e burnout e não só o alto nível de demandas, mas também do tom em que essas demandas são feitas.

O que eu penso sobre isso é que o fato de alguém ter feito uma biblioteca útil que você quer usar te dá exatamente zero direito de exigir o que for de quem fez. Sabe, a pessoa fez esse projeto porque ela quis, e ela não te deve nada. E mesmo que a motivação e o objetivo tenham sido de alcançar visibilidade e crescer (o que eu nem acho que seja o caso em comunidades de código aberto), é a prerrogativa dessa pessoa fazer só o que ela quiser, inclusive deletar tudo em um belo dia ensolarado de domingo.

A responsabilidade de dar conta do problemão que isso vai causar é sua. Afinal, a escolha de depender desse código foi sua, esse é o risco. Eu acho razoável concluir que quando eu instalo uma dependência que possui mais 30 dependências encadeadas, eu me torno responsável por todas as trinta e uma.

Pense no seguinte cenário: Uma pessoa decide investir no mercado imobiliário e compra uma casa para alugar. Daí um tempo o inquilino (ou a imobiliária) liga para avisar que a casa está sem energia porque a instalação elétrica estava cheia de gambiarras e o eletricista declarou que toda a fiação do imóvel deve ser trocada. Essa pessoa vai fazer o quê? Dizer que o problema é do dono anterior? Não existe terceirização da culpa. Ela escolheu comprar essa casa e quando fez isso a comprou no estado em que estava. E o inquilino não poderia ligar menos para quem fez o que e como, ele só quer o conserto.

No fim das contas, seja na casa do exemplo acima ou na nossa aplicação, os problemas estruturais são nossa responsabilidade. Quando se escolhe se usa ou não essa biblioteca ou aquela ferramenta, deve-se pensar também no potencial trabalho que essa escolha pode gerar versus os benefícios. Esse é o custo.

## Referências

1. [`moment().endOf('term')`][moment]
2. [What you need to know about burnout in open source communities - Why is burnout so prevalent in open source communities, and what can we do about it?][burnout]
3. [Leaving Toxic Open Source Communities - Exploring the cultural shame of leaving and tips for finding healthy communities.][ambiente-toxico]
4. [Stress and Burnout in Open Source: Toward Finding, Understanding, and Mitigating Unhealthy Interactions][pesquisa]

[moment]: https://medium.com/@timrwood/moment-endof-term-522d8965689
[burnout]: https://opensource.com/article/19/11/burnout-open-source-communities
[ambiente-toxico]: https://modelviewculture.com/pieces/leaving-toxic-open-source-communities
[pesquisa]: https://www.cs.cmu.edu/afs/cs.cmu.edu/Web/People/ckaestne/pdf/icsenier20.pdf