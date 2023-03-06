# Web Semantica


A web semântica é uma forma de adicionar significado ao conteúdo da web, utilizando a linguagem HTML. A intenção é tornar a estrutura da página mais clara e organizada, facilitando a compreensão tanto para humanos quanto para ferramentas e aplicativos que acessam a página. Além disso, a web semântica também é importante para a acessibilidade e para otimização de mecanismos de busca, pois permite que o conteúdo seja apresentado de forma clara e correta para os visitantes da página e seja mais facilmente encontrado na web.

**Dicas de como escrever um HTML Semantico**

* Utilize as tags semânticas corretas: escolha as tags certas para marcar seu conteúdo, como ``<header>, <nav>, <main>, <section>, <article>, <aside> e <footer>.``

* Mantenha a estrutura simples e clara: use uma estrutura simples e clara para organizar seu conteúdo, evitando aninhar tags desnecessariamente.

* Utilize atributos de linguagem: adicione o atributo "lang" à tag ``<html>`` para especificar a linguagem do conteúdo da página.

* Especifique o tipo de conteúdo: adicione o atributo "type" às tags ``<style> e <script>`` para especificar o tipo de conteúdo que estão incluindo.

* Use descrições claras para os links: forneça descrições claras para os links com a tag ``<a>`` e o atributo "title".

* Adicione legendas a tabelas: adicione uma legenda às tabelas usando a tag ``<caption>`` para torná-las mais acessíveis.

* Forneça descrições para imagens: forneça descrições para as imagens usando a tag ``<img>`` e o atributo "alt".

* Valide seu HTML: valide seu HTML usando ferramentas online gratuitas para garantir que esteja escrito corretamente.





# Atributos 

No HTML um atributo  é um valor que pode ser atribuido a um elemento para fornecer informações adicionais sobre o elemento ou para modificar seu comportamento.
Alguns dos atributos mais comuns em HTML incluem:


* **class:** usado para definir uma ou mais classes CSS para um elemento.
* **id:** usado para definir um identificador único para um elemento.
* **src:** usado para especificar a URL de um recurso (como uma imagem) que deve ser incorporado no documento.
* **href:** usado para especificar a URL de um recurso que deve ser vinculaod a partir do elemento (como um link para outra página).
* **alt:** usado para fornecer um texto alternativo para um recurso incorporado (como uma imagem) que pode não ser exibido corretamente.
* **title:** usado para fornecer um texto de dica de ferramenta para um elemento que aparece quando o usuário passa o mouse sobre ele.
* **style:** usado para definir estilos CSS inline para um elemento.
* **target:** usado para especificar o destino do link (como "_blank" para abrir o link em uma nova janela).
* **type:** usado para especificar o tipo de um elemento (como "text" para um campo de entrada de texto).
* **value:** usado para definir o valor de um elemento (como o valor de um campo de entrada de texto).








# Tags
Algumas das tags HTML básicas incluem:

``<html>``: Define o início e o fim da estrutura de uma página da web.

``<head>``: Contém informações sobre a página, como o título, metadados e links para folhas de estilo.

``<title>``: Define o título da página, que é exibido na guia do navegador.

``<body>``: Contém o conteúdo visível da página, incluindo texto, imagens, links e outros elementos.

``<h1>`` a ``<h6>``: Define os títulos de seção, onde `<h1>` é o título principal e ``<h6>`` é o título menor.

``<p>``: Define um parágrafo de texto.

``<a>``: Define um link para outra página da web ou para um recurso externo.

``<img>``: Insere uma imagem na página.

``<ul>``: Cria uma lista não ordenada, usando os elementos `<li>` para definir cada item na lista.

``<ol>``: Cria uma lista ordenada, usando os elementos ``<li>`` para definir cada item na lista.

# Tabelas 
Tabelas em HTML são usadas para exibir dados em forma de linhas e colunas. As tabelas são compostas por células, 
que são definidas por elementos <td> ou <th> (para células de cabeçalho). As células são organizaads em linhas com o elemento <tr>,
que é colocado dentro do elemento <table>


<table>
  <tr>
    <th>Cabeçalho 1</th>
    <th>Cabeçalho 2</th>
  </tr>
  <tr>
    <td>Dado 1</td>
    <td>Dado 2</td>
  </tr>
  <tr>
    <td>Dado 3</td>
    <td>Dado 4</td>
  </tr>
</table>
  
  
  
  
# DataList

* Lista de valores como sugestão a uma tag ``<input>``
* Valores sugestivos e não obrigatorios 
* Usuario poderao selecionar um dos valores , ou colocar um valor diferente da sugestão .

       <input
       type="text"
       list="saladadefruta"
       placeholder="Escolha uma Fruta"/>
        <datalist id="saladadefruta">
           <option>maçã</option>
           <option>banana</option>
           <option>nektarina</option>
           <option>graviola</option>
           <option>uva</option>
        </datalist>
        
        
  

# Formulario

**As principais tags para formulário são:**  

`<form>`  têm como função iniciar o formulário

`<input>` têm como função definir um campo de texto

`<button>`  têm como função definir um botão

`<textarea>`  têm como função também, definir um campo para o formulário, mas diferentemente, tem como principal característica conter preenchimentos e textos grandes

`<label>`  têm como função definir define uma legenda ou nome para um campo de texto ou controle do formulário

`<legend>`  têm como função definir um título para um conjunto de campo

`<option>`  têm como função definir uma lista de opções dentro de um "drop-down"

`<fieldset>`  têm como função definir um grupo de campos

`<select>`  têm como função definir uma lista selecionável ou conhecida como "drop-down"

`<output>`  têm como função definir elementos de saída para o formulário

`<optgroup>`  têm como função definir um grupo de opções


**Tipos de inputs usados**

`<input type="button">`  é usado em formulários HTML para criar um botão que não envia dados para o servidor. Em vez disso, é usado para executar scripts JavaScript na página, geralmente para realizar tarefas como mostrar ou ocultar elementos da página, mudar o estilo da página ou realizar cálculos.

`<input type="checkbox">` Cria uma caixa de seleção que pode ser marcada ou desmarcada pelo usuário.

`<input type="color">`Cria um campo de entrada que permite ao usuário selecionar uma cor.

`<input type="date">` Cria um campo de entrada para seleção de data, geralmente com um calendário embutido para seleção de data.

`<input type="datetime-local">`Cria um campo de entrada para seleção de data e hora sem considerar a Time Zone.

`<input type="email">`Cria um campo de entrada para endereços de e-mail, que pode ser validado para garantir que o valor digitado seja um endereço de e-mail válido.

`<input type="file">` Cria um campo de entrada que permite ao usuário selecionar um arquivo de seu computador para ser enviado ao servidor.

`<input type="hidden">`Cria um campo de entrada que não é exibido na página e é usado para enviar dados que não precisam ser exibidos para o usuário.

`<input type="image">` é um tipo especial de botão de entrada que permite que você envie uma imagem como parte de um formulário HTML.

`<input type="month">`Cria um campo de entrada para seleção de mês.

`<input type="number">`Cria um campo de entrada para números.

`<input type="password">` Cria um campo de entrada para senhas, onde os caracteres digitados são ocultos atrás de caracteres de substituição (geralmente asteriscos ou pontos).

`<input type="radio">`Cria um botão de rádio que pode ser selecionado pelo usuário.

`<input type="range">`Cria um campo de entrada para seleção de um valor dentro de um intervalo es

`<input type="reset">` é usado em formulários HTML para limpar os valores dos campos de entrada.

`<input type="search">` Cria um campo de entrada para buscas, com características visuais e funcionais específicas para buscas.

`<input type="submit">`  é usado em formulários HTML para enviar os dados do formulário para o servidor. Quando o usuário clica no botão "Enviar", todos os valores dos campos de entrada no formulário são enviados para o servidor para serem processados.

`<input type="tel">`  é usado em formulários HTML para coletar informações de telefone de um usuário. 

`<input type="text">`  é o tipo mais básico de campo de entrada em um formulário HTML. Ele permite que o usuário insira qualquer texto em uma caixa de texto.

`<input type="time">` Cria um campo de entrada para seleção de hora.

`<input type="url">` Cria um campo de entrada para URLs, que pode ser validado para garantir que o valor digitado seja uma URL válida.

`<input type ="textarea">`Cria uma área de texto multilinha para entrada de texto.

`<input type="week">` Cria um campo de entrada para seleção de semana.




  
  
  


