impress.js
============

É uma estrutura de apresentação baseada no poder de transformações CSS3 e
transições em navegadores modernos e inspirado pela ideia por trás prezi.com.

**AVISO**

impress.js não pode ajudá-lo se você não tem nada de interessante para dizer;)


COMO USAR
---------------

[Use a fonte](http://github.com/bartaz/impress.js/blob/master/index.html), Boa Sorte ;)

Se você não tem idéia do que quero dizer com isso, ou você acabou de clicar nesse link acima e esta
muito confuso com todos esses personagens estranhos que foram exibidos na tela,
é um sinal, que impress.js não é para você.

Desculpa.

Felizmente, existem algumas caras no GitHub que ficaram bastante animados com a idéia de construir
ferramentas de edição para impress.js. Vamos esperar que eles consigam fazê-lo.



EXEMPLOS E OUTROS RECURSOS DE APRENDIZAGEM
---------------------------------------

### Oficial demo

[impress.js demo](http://impress.github.io/impress.js/) by [@bartaz](http://twitter.com/bartaz)

### Exemplos e demos

Mais exemplos e demos podem ser encontradas no [Examples and demos wiki page](http://github.com/bartaz/impress.js/wiki/Examples-and-demos).

Sinta-se livre para adicionar suas próprias apresentações de exemplo (para websites).

### Outros tutoriais e recursos de aprendizagem

Se você quer aprender ainda mais, há um [list of tutorials and other learning resources](https://github.com/bartaz/impress.js/wiki/impress.js-tutorials-and-other-learning-resources)
on the wiki, too.

There is also a book available about [Building impressive presentations with impress.js](http://www.packtpub.com/building-impressive-presentations-with-impressjs/book) by Rakhitha Nimesh Ratnayake.


WANT TO CONTRIBUTE?
---------------------

If you've found a bug or have a great idea for new feature let me know by [adding your suggestion]
(http://github.com/bartaz/impress.js/issues/new) to [issues list](https://github.com/bartaz/impress.js/issues).

If you have fixed a bug or implemented a feature that you'd like to share, send your pull request against [dev branch]
(http://github.com/bartaz/impress.js/tree/dev). But remember that I only accept code that fits my vision of impress.js
and my coding standards - so make sure you are open for discussion :)

**Note:** The team has changed, so there will be many changes in the upcoming versions.
If you need informations about versions, check the [changelog](CHANGELOG.md).


ABOUT THE NAME
----------------

impress.js name in [courtesy of @skuzniak](http://twitter.com/skuzniak/status/143627215165333504).

It's an (un)fortunate coincidence that a Open/LibreOffice presentation tool is called Impress ;)


BROWSER SUPPORT
-----------------

### TL;DR;

Currently impress.js works fine in latest Chrome/Chromium browser, Safari 5.1 and Firefox 10.
With addition of some HTML5 polyfills (see below for details) it should work in Internet Explorer 10, 11 and Edge.
It doesn't work in Opera, as it doesn't support CSS 3D transforms.

If you find impress.js working on other browsers, feel free to tell us and we'll update this documentation.

As a presentation tool it was not developed with mobile browsers in mind, but some tablets are good
enough to run it, so it should work quite well on iPad (iOS 5, or iOS 4 with HTML5 polyfills) and 
Blackberry Playbook. Inform us of any bug and we will try to fix this.

### Still interested? Read more...

Additionally for the animations to run smoothly it's required to have hardware
acceleration support in your browser. This depends on the browser, your operating
system and even kind of graphic hardware you have in your machine.

For browsers not supporting CSS3 3D transforms impress.js adds `impress-not-supported`
class on `#impress` element, so fallback styles can be applied to make all the content accessible.


### Even more explanation and technical stuff

Let's put this straight -- wide browser support was (and is) not on top of my priority list for
impress.js. It's built on top of fresh technologies that just start to appear in the browsers
and I'd like to rather look forward and develop for the future than being slowed down by the past.

But it's not "hard-coded" for any particular browser or engine. If any browser in future will
support features required to run impress.js, it will just begin to work there without changes in
the code.

From technical point of view all the positioning of presentation elements in 3D requires CSS 3D
transforms support. Transitions between presentation steps are based on CSS transitions.
So these two features are required by impress.js to display presentation correctly.

Unfortunately the support for CSS 3D transforms and transitions is not enough for animations to
run smoothly. If the browser doesn't support hardware acceleration or the graphic card is not 
good enough the transitions will be laggy.

Additionally the code of impress.js relies on APIs proposed in HTML5 specification, including
`classList` and `dataset` APIs. If they are not available in the browser, impress.js will not work.

Fortunately, as these are JavaScript APIs there are polyfill libraries that patch older browsers
with these APIs.

For example IE10 is said to support CSS 3D transforms and transitions, but it doesn't have `classList`
nor `dataset` APIs implemented at the moment. So including polyfill libraries *should* help IE10
with running impress.js.


### And few more details about mobile support

Mobile browsers are currently not supported. Even Android browsers that support CSS 3D transforms are
forced into fallback view at this point.

Fortunately some tablets seem to have good enough hardware support and browsers to handle it.
Currently impress.js presentations should work on iPad and Blackberry Playbook.

In theory iPhone should also be able to run it (as it runs the same software as iPad), but I haven't
found a good way to handle its small screen.

Also note that iOS supports `classList` and `dataset` APIs starting with version 5, so iOS 4.X and older
requires polyfills to work.

Copyright 2011-2016 Bartek Szopka - Released under the MIT [License](LICENSE)
