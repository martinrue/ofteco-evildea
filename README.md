# Ofteco: Evildea

An analysis of the Esperanto YouTuber Evildea's usage of Esperanto. This file was generated using [ofteco](https://github.com/martinrue/ofteco).

Analizo de la uzado de Esperanto de la Esperanto-Jutubisto Evildea. Tiu ĉi dosiero estis kreita de [ofteco](https://github.com/martinrue/ofteco).

## Results

[https://martinrue.com/ofteco-evildea](https://martinrue.com/ofteco-evildea).

## Input

The video IDs used in this analysis were extracted from the YouTube search results DOM via the following query:

La identigiloj de filmetoj, kiuj estis uzitaj en tiu ĉi analizo, estis prenita de la serĉrezultoj de Jutubo per la sekva kodo:

```
$('#byline > a')
  .filter(function() {
    return $(this).text() === 'Evildea';
  })
  .map(function() {
    return $(this).closest('#dismissable')
                  .find('ytd-thumbnail a')
                  .attr('href')
                  .split('v=')[1]
                  .split('&t=')[0];
  })
  .each((i, id) => console.log(id));
```