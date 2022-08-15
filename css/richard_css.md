css richard:
> aqui vai ter meus css

pseudo-classes:
> -elementos tem um estado atual em css.
> -ex de pseudo-classe de estado que já usou antes: hover
> link    -define tempo e estilo de transição entre os estados, não funciona  em  tudo.
> link    -link ainda não visitado
> visited  -link visitado.
> focus   -barra de "escrever" na box/input/check
> disabled -atributo que pode ser usado para desabilitar no html e no css para mostrar o que acontece.
> enabled -o de cima mas para ativado.
> checked -já conhece.
> first-child -seleciona somente o ultimo filho de uma tag
> last-child-seleciona  o ultimo.
> required -???
pseudo-classe not():
> ao usar not(id/classe) vc pode selecionar tudo exceto o que tiver no not.
> ex para pseudo-classe: input(:not(:checkd) + p {x} , isso significa quando checked não estiver ativo, acontecerá x
pseudo-classe mth-child()?
>usada para selecionar x irmãos de um conjunto.
>ex: ul  li:nth-child(2){y} fz y no child de índice 2, pode selecionar pares com even e impar que é odd.
> ex2: se colocar 3n vai selecionar a cada 3.
> 3x3: 3n+5 começa do 5, seleciona ele e a cada 3.
>
visual code: 
> se vc usar uma tag e digitar *x vai multiplicar ela por x, ex: <li>*3
pseudo-elements:
::      - é a mesma coisa do : pq o navegador já corrige, na documentação tem 2.
after   - insere um item depois do indicado, precisa de content="" . ex: ul li:: after{content:"-"}, isso insere - depois dos li
> first-letter - te permite modificar a primeira letra de algo.
> first-line  - te permite modificar a primeira linha.
> selection   - te permite modificar o que acontece quando vc selecionar com o mouse.
> placeholder - nome pré-setado em caixas de texto e afins.
especificidade do css:
>são 3 coisas:
> id    classe, atributos e pseudo-classes    elementos e pseudo-elementos
> fica (x,x,x)
> ex:
> #p fica (1,0,0)
> .p fica (0,1,0)
> #p.p fica (1,1,0)
> p#p.p fica (1,1,1)
> #b p#p.p fica (2,1,1)
> body#b p#p.p fica ()
> body#b.bclass p#p.p fica (2,2,2)
> body div ul li a fica (0,0,5)
> quanto maior mais os numeros mais dificil sobrescrever, se tiver dificil ainda dá para ir na tag do html e mudar o style. mas não se faz isso.
> !important força o navegador a aplicar o que está sendo dito. se tiver 2 desses quem desempata é a especificidade.

> regra geral de prioridade: especificidade → style → important


