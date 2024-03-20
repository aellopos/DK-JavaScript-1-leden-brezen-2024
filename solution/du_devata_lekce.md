# Úkol 07

## Newsletter, kontrola

Pokračujte v příkladu Newsletter z lekce. V tomto cvičení zařidíme, aby uživatel při zadávání e-mailu dostal zpětnou vazbu, pokud zadává neplatný vstup.

1. V CSS si vytvořte třídu, která dělá výrazný červený rámeček kolem textového políčka.
1. Přidejte na textové políčko posluchač události `input`.
1. Během toho, jak uživatel píše, kontrolujte, jestli náhodou políčko není prázdné. V takovém případě na políčko přidejte třídu s červeným rámečkem. Pokud je vstup v pořádku, rámeček odeberte.
1. Zobrazte červený rámeček i v případě, že zadaný e-mail neobsahuje zavináč. K tomu můžete použít metodu `indexOf` nebo [`includes`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes).