# DOM Programming

## Node attributes

* nodeName

  返回节点名称
  
      document.nodeName //document
  
* nodeType

  返回节点常良值
  
      document.nodeType //9
      document.querySelector('a').nodeType == 1 //判断是否是需要的节点
  
* ownerDocument

  ownerDocument属性返回当前节点所在的顶层文档对象，即document对象。
  
      div.ownerDocument // document
      
* nextSibling

  nextsibling返回紧跟在当前节点后面的第一个同级节点。如果没有则返回null。注意，该属性还包括文本节点和评论节点。因此如果当前节点后面有空格，该属性会返回一个文本节点，内容为空格。
  
* previousSibling

  previoussibling属性返回当前节点前面的第一个同级节点。如果当前节点前面没有同级节点，则返回null。
  
* parentNode

  parentNode属性返回当前节点的父节点。对于一个节点来说，它的父节点只可能是三种类型：element节点、document节点和documentfragment节点。对于document节点和documentfragment节点，它们的父节点都是null。另外，对于那些生成后还没插入DOM树的节点，父节点也是null。
  
* parentElement

  parentElement属性返回当前节点的父Element节点。如果当前节点没有父节点，或者父节点类型不是Element节点，则返回null。在IE浏览器中，只有Element节点才有该属性，其他浏览器则是所有类型的节点都有该属性。
  
      dom.parentElement.style.color = 'blue';
      
* textContent

  返回当前节点和它的所有后代节点的文本内容。
  
      <div>Hello <span>World</span></div>
      var divDom = document.querySelector('div')
      divDom.textContent; // Hello World
      divDom.textContent = "<p>Welcome<p>" //&lt ;Welcome&gt ; //转义
      
* nodeValue

  nodeValue属性返回或设置当前节点的值，格式为字符串。但是，该属性只对Text节点、Comment节点、XML文档的CDATA节点有效，其他类型的节点一律返回null。
  
* childNodes

  childNodes属性返回一个NodeList集合，成员包括当前节点的所有子节点。如果当前节点不包括任何子节点，则返回一个空的NodeList集合。由于NodeList对象是一个动态集合，一旦子节点发生变化，立刻会反映在返回结果之中。
  
* firstNode
 
  firstNode属性返回当前节点的第一个子节点，如果当前节点没有子节点，则返回null。注意，除了HTML元素子节点，该属性还包括文本节点和评论节点。

* lastNode

  lastChild属性返回当前节点的最后一个子节点，如果当前节点没有子节点，则返回null。
  
* baseURI

  baseURI属性返回一个字符串，由当前网页的协议、域名和所在的目录组成，表示当前网页的绝对路径。如果无法取到这个值，则返回null。浏览器根据这个属性，计算网页上的相对路径的URL。该属性为只读。
  
## Node methods

* appendChild()

  appendChild方法接受一个节点对象作为参数，将其作为最后一个子节点，插入当前节点。如果参数节点是文档中现有的其他节点，appendChild方法会将其从原来的位置，移动到新位置。
  
      var p = document.createElement('p');
      document.body.appendChild(p);
      
* hasChildNodes()

  返回一个布尔值，表示当前节点是否有子节点。
  
      if ( document.body.hasChildNodes() ) {
        //不是空文档
      }

* cloneNode()
* insertBefore()
* removeChild()
* replaceChild()
* contains()
* compareDocumentPosition()
* isEqualNode()
* normalize()

## NodeList Interface

## HTMLCollection Interface

## ParentNode Interface

## ChildNode Interface

## HTML Element

* dataset attribute
* tabindex attribute
* page position related attributes
* style attributes
* Element object methods
* table element
