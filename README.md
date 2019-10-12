# WARNING: This repository is no longer maintained :warning:

> This repository will not be updated. The repository will be kept available in read-only mode.

# ProcessWire Textformatter Normalize UTF8

Textformatter Normalize UTF8 uses a lightweight PHP class [(Patchwork UTF-8)](https://github.com/tchwork/utf8).

## Use it if ..

1. If you check the page with the [W3C HTML5 validator](http://validator.w3.org/), you'll maybe get the following warning:
   
   ```Text run is not in Unicode Normalization Form C.```
   
2. If you notice strange output in some browsers (bold letters, shifted characters, ..).

## What it does

> In Unicode it is possible to produce the same text with different sequences of characters.
> For example, take the Hungarian word világ. The fourth letter could be stored in memory as a precomposed U+00E1 LATIN SMALL LETTER A WITH ACUTE (a single character) or as a decomposed sequence of U+0061 LATIN SMALL LETTER A followed by U+0301 COMBINING ACUTE ACCENT (two characters).
> 
> világ = világ
>
> The Unicode Standard allows either of these alternatives, but requires that both be treated as identical. To improve efficiency, an application will usually normalize text before performing searches or comparisons. Normalization, in this case, means converting the text to use all precomposed or all decomposed characters.
>
> There are four normalization forms specified by the Unicode Standard: NFC, NFD, NFKC and NFKD. The C stands for (pre-)composed, and the D for decomposed. The K stands for compatibility. To improve interoperability, the W3C recommends the use of NFC normalized text on the Web.
>
> -- <cite>[W3C](http://www.w3.org/International/questions/qa-html-css-normalization)</cite>
