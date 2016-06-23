# HEAD

Uma lista de tudo que pode ir no `<head>` do seu documento

## Table of Contents

- [Mínimo Recomendado](#minimo-recomendado)
- [Elementos](#elementos)
- [Meta](#meta)
  - [Meta: Não Recomendado](#meta-nao-recomendado)
- [Link](#link)
  - [Link: Not Recommended](#link-not-recommended)
  - [Favicons](#favicons)
- [Social](#social)
  - [Facebook / Open Graph](#facebook--open-graph)
  - [Facebook / Instant Articles](#facebook--instant-articles)
  - [Twitter](#twitter)
  - [Google+ / Schema.org](#google--schemaorg)
  - [OEmbed](#oembed)
- [Browsers / Platforms](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Apple Safari](#apple-safari)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
  - [Microsoft Internet Explorer: Legacy, Do Not Use!](#microsoft-internet-explorer-legacy-do-not-use)
- [Browsers (Chinese)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App Links](#app-links)
- [Notes](#notes)
  - [Performance](#performance)
- [Other Resources](#other-resources)
- [Related Projects](#related-projects)
- [Other Formats](#other-formats)
- [Translations](#translations)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

## Mínimo Recomendado

Essas são as tags essenciais para websites básicos, minimalistas:

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!-- As 3 tags meta acima *devem* vir primeiro no head; qualquer outro conteúdo deve vir *após* essas tags -->
<title>Título da página</title>
```

## Elementos

``` html
<!-- Título do Documento -->
<title>Título da Página</title>

<!-- URL Base para todas as URLs relativas contidas no documento -->
<base href="https://example.com/page.html">

<!-- CSS Externo -->
<link rel="stylesheet" href="styles.css">

<!-- CSS Inline -->
<style>
  /* ... */
</style>

<!-- JavaScript -->
<script src="script.js"></script>
```

## Meta

``` html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- As 3 tags meta acima *devem* vir primeiro no head; qualquer outro conteúdo deve vir *após* essas tags -->

<!-- Permite controlar de onde os recursos são carregados -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
<!-- Coloque o mais pra cima no documento tanto quanto possível -->
<!-- Só se aplica para o conteúdo após esta tag -->

<!-- Nome da aplicação web (só deve ser usado se o website for usado como um app) -->
<meta name="application-name" content="Nome da Aplicação">

<!-- Descrição pequena da página (limitada a 150 caracteres) -->
<!-- Em *algumas* situações esta descrição é exibida como parte dos resultados de busca. -->
<meta name="description" content="Uma descrição da página">

<!-- Controla o comportamento dos motores de busca (crawling e indexação) -->
<meta name="robots" content="index,follow,noodp"><!-- Todos os motores de busca -->
<meta name="googlebot" content="index,follow"><!-- Específico do Google -->

<!-- Fala para o Google não exibir o campo de busca -->
<meta name="google" content="nositelinkssearchbox">

<!-- Fala para o Google não exibir traduções para esta página -->
<meta name="google" content="notranslate">

<!-- Verifica propriedade para o Google Search Console -->
<meta name="google-site-verification" content="verification_token">

<!-- Usado para nomear o software utilizado para construir o website (por ex: WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Pequena descrição do assunto do seu site -->
<meta name="subject" content="assunto do seu site">

<!-- Frase resumida descrevendo o propósito do seu site -->
<meta name="abstract" content="">

<!-- Descreve o tópico do seu website -->
<meta name="topic" content="">

<!-- Breve sumário da companhia ou propósito do website -->
<meta name="summary" content="">

<!-- Uma tag obsoleta que faz o mesmo que a meta tag keywords -->
<meta name="classification" content="business">

<!-- Nome de domínio ou endereço web completo -->
<meta name="url" content="https://example.com/">

<!-- Faz o mesmo que URL, mais velho e não suportado -->
<meta name="identifier-URL" content="https://example.com/">

<meta name="directory" content="submission">

<!-- Tem a mesma função que a tag keywords -->
<meta name="category" content="">

<!-- Especifica que seu site deve aparecer em todos os países e idiomas -->
<meta name="coverage" content="Worldwide">

<!-- Faz o mesmo que a tag coverage -->
<meta name="distribution" content="Global">

<!-- Especifica a faixa etária da audiência do site baseado no seu conteúdo -->
<meta name="rating" content="General">

<!-- Permite controlar como a informação sobre o referrer é passada -->
<meta name="referrer" content="never">

<!-- Desabilita a detecção e formatação automática de possíveis números de telefone -->
<meta name="format-detection" content="telephone=no">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="país[-estado]"><!-- Código do país (ISO 3166-1): obrigatório, código do estado (ISO 3166-2): opcional; ex. content="BR" / content="BR-RJ" -->
<meta name="geo.placename" content="cidade/país"><!-- ex. content="Rio de Janeiro" -->
```

- [Meta tags que o Google entende](https://support.google.com/webmasters/answer/79812?hl=en)
- [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- [ICBM na Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- [Geotagging ba Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

### Meta: Não Recomendado
A seguir as tags meta que não tem o uso recomendadas:

```html
<!-- Usado para declarar o idioma do documento, mas não tão bem suportado. Melhor usar <html lang=""> -->
<meta name="language" content="pt">

<!-- Google desconsidera & Bing considera como um indicador de spam -->
<meta name="keywords" content="palavras,chave,separadas,com,vírgulas,e,sem,espaços">

<!-- Não há evidência de utilização pelos serviços de busca atuais -->
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">

<!-- É uma maneira muito fácil de bots de spam conseguir endereços de email -->
<meta name="reply-to" content="email@exemplo.com.br">

<!-- É melhor usar <link rel="author"> ou um arquivo humans.txt -->
<meta name="author" content="nome, email@exemplo.com.br">
<meta name="designer" content="">
<meta name="owner" content="">

<!-- Diz para os motores de busca revisitarem a página após um certo período. Isto não é mais utilizado porque a maioria dos motores de busca atualmente utilizam intervalos aleatórios para verificar mudanças no conteúdo. -->
<meta name="revisit-after" content="7 days">

<!-- Envia o usuário para uma nova URL após um certo período de tempo -->
<!-- O W3C recomenda que essa tag não seja usada. O Google recomenda usar um redirecionamento de servidor 301. -->
<meta http-equiv="refresh" content="300; url=https://exemplo.com.br/">

<!-- Controle de Cache -->
<!-- É melhor configurar o controle de cache do lado do servidor -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## Link

``` html
<!-- Helps prevent duplicate content issues -->
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">

<!-- Used to be included before the icon link, but is deprecated and no longer is used -->
<link rel="shortlink" href="https://example.com/?p=42">

<!-- Links to an AMP HTML version of the current document -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Points to a CSS stylesheet -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Links to a JSON file that specifies "installation" credentials for web applications -->
<link rel="manifest" href="manifest.json">

<!-- Links to the author of the document -->
<link rel="author" href="humans.txt">

<!-- Refers to a copyright statement that applies to the links context -->
<link rel="copyright" href="copyright.html">

<!-- Gives a reference to a location in your document that may be in another language -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Gives information about an author or another person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Links to a document that contains an archive link to the current document -->
<link rel="archives" href="https://example.com/2003/05/" title="May 2003">

<!-- Links to top level resource in an hierarchical structure -->
<link rel="index" href="https://example.com/" title="DeWitt Clinton">

<!-- Gives the starting point of the document -->
<link rel="start" href="https://example.com/photos/pattern_recognition_1_about/" title="Pattern Recognition 1">

<!-- Leads to the preceding resource of the sequence the current document is in -->
<link rel="prev" href="https://example.com/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/" title="OpenSearch and OpenID? A sure way to get my attention.">

<!-- Gives a self reference - useful when the document has multiple possible references -->
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">

<!-- The first, next, previous, and last documents in a series of documents, respectively -->
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="previous" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">

<!-- Used when using a 3rd party service to maintain a blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forms an automated comment when another wordpress blog links to your wordpress blog or post -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Notifies a url when you link to it on your site -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Loads in an external HTML file into the current HTML file -->
<link rel="import" href="component.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="subresource" href="styles.css">
<link rel="preload" href="image.png">
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

### Link: Not Recommended
Below are the link relations which are not recommended for use:

```html
<link rel="shortcut icon" href="path/to/favicon.ico">
```

### Favicons

``` html
<!-- For IE 10 and below -->
<!-- No link, just place a file called favicon.ico in the root directory -->

<!-- For IE 11, Chrome, Firefox, Safari, Opera -->
<link rel="icon" href="path/to/favicon-16.png" sizes="16x16" type="image/png">
<link rel="icon" href="path/to/favicon-32.png" sizes="32x32" type="image/png">
<link rel="icon" href="path/to/favicon-48.png" sizes="48x48" type="image/png">
<link rel="icon" href="path/to/favicon-62.png" sizes="62x62" type="image/png">
<link rel="icon" href="path/to/favicon-192.png" sizes="192x192" type="image/png">
<!-- More info: https://bitsofco.de/all-about-favicons-and-touch-icons/ -->
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)

## Social

### Facebook / Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
<!-- Facebook: https://developers.facebook.com/docs/sharing/webmasters#markup -->
<!-- Open Graph: http://ogp.me/ -->
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

### Facebook / Instant Articles

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="http://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Instant Articles: Creating Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Instant Articles: Format Reference](https://developers.facebook.com/docs/instant-articles/reference)

### Twitter

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<!-- More info: https://dev.twitter.com/cards/getting-started -->
<!-- Validate: https://dev.twitter.com/docs/cards/validation/validator -->
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://dev.twitter.com/docs/cards/validation/validator)

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- [oEmbed format](http://oembed.com/)

## Browsers / Platforms

### Apple iOS

``` html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Add to Home Screen -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Touch Icons -->
<link rel="apple-touch-icon" href="path/to/apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="path/to/apple-touch-icon-precomposed.png">
<!-- In most cases, one 180×180px touch icon in the head is enough -->
<!-- If you use art-direction and/or want to have different content for each device, you can add more touch icons -->

<!-- Startup Image -->
<link rel="apple-touch-startup-image" href="path/to/startup.png">

<!-- More info: https://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html -->
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- Pinned Site -->
<link rel="mask-icon" href="path/to/icon.svg" color="red">
```

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- Add to homescreen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->
```

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" value="notranslate">
```

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta http-equiv="cleartype" content="on">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Disable link highlighting on IE 10 on Windows Phone (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Pinned sites (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Contoso Pinned Site Caption">
<meta name="msapplication-tooltip" content="Example Tooltip Text">
<meta name="msapplication-starturl" content="/">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">

<meta name="msapplication-allowDomainApiCalls" content="true">
<meta name="msapplication-allowDomainMetaTags" content="true">
<meta name="msapplication-badge" content="frequency=30; polling-uri=http://example.com/id45453245/polling.xml">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile">
<meta name="msapplication-square150x150logo" content="path/to/logo.png">
<meta name="msapplication-square310x310logo" content="path/to/largelogo.png">
<meta name="msapplication-square70x70logo" content="path/to/tinylogo.png">
<meta name="msapplication-wide310x150logo" content="path/to/widelogo.png">
<meta name="msapplication-task" content="name=Check Order Status;action-uri=./orderStatus.aspx?src=IE9;icon-uri=./favicon.ico">
<meta name="msapplication-task-seperator" content="1">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="path/to/tileimage.jpg">
<meta name="msapplication-window" content="width=1024;height=768">
```

### Microsoft Internet Explorer: Legacy, Do Not Use!

``` html
<!-- Disable the image toolbar when you mouse over images in IE 6 (https://msdn.microsoft.com/en-us/library/ms532986(v=vs.85).aspx) -->
<meta http-equiv="imagetoolbar" content="no">

<!-- Disable Windows theming to form inputs/buttons (https://support.microsoft.com/en-us/kb/322240) -->
<meta name="MSThemeCompatible" content="no">

<!-- Disable a feature that only appeared on IE 6 beta (https://stackoverflow.com/q/2167301) -->
<meta name="MSSmartTagsPreventParsing" content="true">

<!-- Interpage Transitions (https://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx) -->
<meta http-equiv="Page-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Page-Exit" content="revealtrans(duration=3,transition=12)">
<meta http-equiv="Site-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Site-Exit" content="revealtrans(duration=3,transition=12)">
```

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- Web Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
<!-- More info: http://applinks.org/documentation/ -->
```

- [App Links Docs](http://applinks.org/documentation/)

## Browsers (Chinese)

### 360 Browser

``` html
<!-- select rendering engine in order -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- Display this page in fullscreen -->
<meta name="x5-fullscreen" content="true">
<!-- Page will be displayed in "application mode"(fullscreen,etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

``` html
<!-- Locks the screen into the specified orientation -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- Display this page in fullscreen -->
<meta name="full-screen" content="yes">
<!-- UC browser will display images even if in "text mode" -->
<meta name="imagemode" content="force">
<!-- Page will be displayed in "application mode"(fullscreen,forbiding gesture, etc.) -->
<meta name="browsermode" content="application">
<!-- Disabled the UC browser's "night mode" in this page -->
<meta name="nightmode" content="disable">
<!-- Simplify the page to reduce data transfer -->
<meta name="layoutmode" content="fitscreen">
<!-- Disable the UC browser's feature of "scaling font up when there are many words in this page" -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

## Notes

### Performance
Moving the `href` attribute to the beginning of an element improves compression when GZIP is enabled, because the `href` attribute is used in `a`, `base` and `link` tags.

Example:

``` html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

## Other Resources

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

## Related Projects

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

## Other Formats

- [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

## Translations

- [Japanese](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- [Russian/Русский](https://github.com/Konfuze/HEAD)

## Contributing

Open an issue or a pull request to suggest changes or additions.

Please follow these steps for pull requests:
- Modify only one tag, or one related set of tags at a time
- Use double quotes on attributes
- Don't include a trailing slash in self-closing elements — the HTML5 spec says they're optional
- Consider including a link to documentation that supports your change

### Contributors

Check out all the super awesome [contributors](https://github.com/joshbuchea/HEAD/graphs/contributors).

## Author

**[Josh Buchea](http://joshbuchea.com/)**

## License

[CC0 License](LICENSE)

![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")
