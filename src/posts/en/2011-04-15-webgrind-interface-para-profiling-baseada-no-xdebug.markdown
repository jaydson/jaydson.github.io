---
comments: true
date: 2011-04-15 12:42:47
layout: post
slug: webgrind-interface-para-profiling-baseada-no-xdebug
title: Webgrind - Interface para Profiling baseada no Xdebug
categories:NetBeans,Xdebug
---

O [**Xdebug Profiler**](http://www.xdebug.org) é uma ferramenta poderosa que nos permite analisar o código PHP a procura de gargalos(!), ou até mesmo determinados trechos onde possa existir lentidão na aplicação.
Normalmente usamos algum cliente para ler as informações geradas pelo Xdebug, como por exemplo o [KCacheGrind](http://kcachegrind.sf.net/).


O que venho compartilhar hoje é uma excelente ferramenta, o [WebGrind](https://github.com/jokkedk/webgrind), desenvolvida pelo [Joakim Nygard](https://github.com/jokkedk).
O que gostei foi a simplicidade. [Baixe](https://github.com/jokkedk/webgrind) > Descompacte > Coloque no servidor.
Pronto, feito isso basta acessar, iniciar o debugger e acessar a aplicação.<!-- more -->

Obviamente é necessário ter o [Xdebug instalado](http://www.xdebug.org/docs/install) e configurado, mas isso nao é  um bicho de 7 cabeças.

Notem em cima a direita:
654 different functions called in 109 milliseconds
O WebGrind mostra o total de chamadas de funções, e o tempo total em milisegundos.
Além disso, cada função exibe quais arquivos foram usados.

Bom, testem ai e vejam o que mais é possivel.


Profiler
