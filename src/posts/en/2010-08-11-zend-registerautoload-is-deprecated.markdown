---
comments: true
date: 2010-08-11 23:07:59
layout: post
slug: zend-registerautoload-is-deprecated
title: Zend - registerAutoload is deprecated
wordpress_id: 614
categories:PHP,Zend
---
Após atualizar a versão do [Zend Framework](http://framework.zend.com/) tive problema com o registerAutoload.
Isso porque desde a versão 1.8 o Zend_Loader::registerAutoload está obsoleto.
Meu  código  estava mais ou menos assim:

[php]
include('Zend/Loader.php');
Zend_Loader::registerAutoload();
[/php]

Para solucionar o problema basta usar o [Zend_Loader_Autoloader](http://framework.zend.com/manual/en/zend.loader.autoloader.html).
Em minha implementação apenas o trecho abaixo resolveu o problema:

[php]
include('Zend/Loader/Autoloader.php');
$autoloader = Zend_Loader_Autoloader::getInstance();
[/php]
