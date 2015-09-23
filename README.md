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
* previousSibling
* parentNode
* parentElement
* textContent
* nodeValue
* childNodes
* firstNode
* lastNode
* baseURI


## Node methods

* appendChild()
* hasChildNodes()
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
