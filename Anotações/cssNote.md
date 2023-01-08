# Cascata 
O browser escolhe qual regra ira aplicar , caso haja muitas regras para o mesmo elemento 

### Origem de estilo
inline > tag style > tag link


### Especificidade
No css existe ordem de prioridades com valores para se considerar ( piority pokemon)

0- Universal selector , combinators e negation pseudo-class( :not() )
1- Element type selectors e pseudo-elements ( :before, ::after )
10- classes e attributes selectors ( [type:radio])
100- ID Selector 
1000- inline 

### Regra !important
* Cuidado , evite o uso
* Não é considerado uma boa prática
* Quebra o fluxo natural da cascata

# At-Rules

* Está relacionado ao comportamento CSS
* começa com  o sinal  de " @ " seguido do identificador e valor

### Exemplos Comuns     
- @import        // Incluir um CSS exertno
- @media        // regras condicionais para dispositivos
- @fon-face    //fontes externas
- @keyframes  // Animation
 Exemplos :
'''css
 @import "http://local.com/style.css""

@media (min-width:500px) {
    }
    @font-face {

    }
    @keyframes nameofanimation {
        }

# Shorthand 

é uma junção de propriedades mais resumidas e legível

>''' css
/* Propriedades do background */
background-color: #000;
background-image: url;
background-repeat: no-repeat;
background-position: center;

>/* Background Shorthand */
background: #000 url(images/bg.gif) no-repeat center ;


>/* Font propriedades */
font-family: Arial , sans-serif;
font-weight: bold;
font-style: italic;
font-size:.8em;
line-height: 1.2;

/* font shorthand */
font italic Bold .8em/1.2 Arial , sans-serif

 **Detalhes**
* não irá considerar propriedades anteriores 
* valores não especificados irão assumir o valor padrão 
* geralmente , a ordem descrita não importa , mas , se houver muitas propriedades com valores semelhantes , poderemos encontrar problemas

**Propriedades que aceitam shorthand**

animation, background , border , border-bottom , border-color etc

# Vendor  Predixes
São coisas que permitem que browsers adiocionem features a fim de colocar em uso alguma novidade que vemos no CSS.

Exemplos:

> p {
	-webkit-background-clip: text; /*Chrome, Safari, iOS e Android*/
	-moz-background-clip: text; /* Mozilla (Firefox) */
	-ms-background-clip: text; /* Internet Explorer ou Edge*/
	-o-background-clip: text; /* Opera */

Você também pode consultar se a feature pode ser utilizada através dos sites:

https://ireade.github.io/which-vendor-prefix

https://caniuse.com

# Funções
Em programação, funções são reconhecidas por causar um reaproveitamento de código.
Exemplos de funções do CSS:

rgb()
hsl()
url()
calc()
Dentro dos parêntesis são passados argumentos

Link da documentação do MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions


# Box Sizing 

Por padrão o navegador vai calcular o tamanho da caixa pelo content-box e vai somar com os outros boxes, por exemplo  abaixo 
```
div {
height: 100px;
width: 100px ;
border: 1px solid  red;
margin: 10%;
padding : 0 20px;
} 
```
 a caixa vai ficar com uma largura de 140px. Para que isso não aconteça, é possível mudar qual vai ser a referência para o calculo do tamanho da caixa adicionando a propriedade box-sizing: border-box;.

Normalmente usa-se o código abaixo como forma de "resetar" o box-sizing que vem por padrão nos navegadores.

```
* {
     box-sizing: border-box;
}
```
# Display block-inline
O display: block e o display: inline são dois valores da propriedade CSS "display" que determinam como um elemento é exibido na página.

O display: block faz com que um elemento se comporte como um elemento de bloco, ou seja, ocupa todo o espaço disponível na largura do seu container e empurra para a próxima linha abaixo . Alguns exemplos de elementos que são exibidos como bloco por padrão são divs, h1-h6, p, table, etc.

Já o display: inline faz com que um elemento se comporte como um elemento de inline, ou seja, ocupa somente o espaço necessário para o seu conteúdo e não quebra para a próxima linha. Alguns exemplos de elementos que são exibidos como inline por padrão são spans, a, strong, etc.

---
**block**
* ocupa toda a linha , colocando o proximo elemento abaixo desse
* width e height sao respeitados
* padding , margin , border  irão funcionar normalmente .

**inline**
* elemento ao lado do outro
* widh e height não funcionam 
* somente valores horizontais de margin , padding e border  funcionam

```
exemplos :
block: <p> <div> <section> todos os headings <h1>
inline: <a> <strong> <span> <em>
 ```
# Margin

# Padding

# Border


# Cores

**Tipos de cores** 

* background-color (para caixas)
* color (para textos)
* border-color (para caixas)

**Valores**
podemos definir valores por :
* hexadecimal #33cc33
* palavras chave(blue,red,green,yellow)
* funções (rgb , hsl , hsla ,rgba)


# Page Layout
- Tables
- Floats e clear
- Frameworks e grid systems
- Flexbox
- Grid

### Posicionamento 
position pode ser  **static | relative | absolute | fixed**

Position controla onde , na pagina , o elemento irá ficar ,alterando o fluxo normal dos  elementos.

* O fluxo normal dos elementos é ficar um abaixo do outro, a não ser no caso de elementos inline, que ficam um ao lado do outro.


* Por padrão os elementos são **static**. Isso significa que os elementos irão seguir o fluxo normal do HTML.

* O position indica onde o elemento vai ser posicionado na página. Ao usar o position podemos adicionar outras propriedades como top, right, bottom, left e z-index, que vão determinar o posicionamento final do elemento.

* Quando o position é **relative** os elementos são deslocados do seu posicionamento normal, mas sem afetar o posicionamento de outros elementos da página.

* O position  **absolute** faz com que o elemento seja  deslocado saindo do fluxo normal. O elemento de position absolute é posicionado em relação ao seu parent element mais próximo. Se esse elemento "pai" não existir, ele será posicionando em relação ao bloco contendo a raiz do elemento.

* Quando aplicado o position **fixed** é como se criasse um elemento flutuante que fica fixo na página, independente do scrolling feito.


###  Element stacking
É o empilhamento de elementos. Podemos usar o z-index para determinar a ordem da posição do elemento. Quanto maior o z-index, mais "acima" vai aparecer o elemento.


### Flexbox

Nos permite posicionar os elementos dentro da caixa
Controle em uma dimensão (horizontal ou vertical)
Alinhamento, direcionamento, ordenar e tamanhos
> div.parent {
	display: flex;
    flex-direction: column;
}
* obs : pegar sempre o conteiner pai(não sei se está certo isso)

**Flex-direction**
Qual a direção do flex: horizontal ou vertical
row | column

**Alinhamento**
justify-content
align-items


### Grid
**(estudar mais sobre)**
* Posicionamento  dos elementos dentro da caixa
* Posicionamento horizontal e vertical ao mesmo tempo
* Pode ser flexível ou fixo
* cria espaço para os elementos filhos habitarem 

### Grid ou Flexbox 
Qual usar e quando usar ( tenho q rever isos aki)

# 


