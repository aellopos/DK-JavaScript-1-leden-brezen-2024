# Vícestránkové aplikace
## Počasí
Podobných postupem jako jsme na lekci tvořili aplikaci _Zprávičky_ zkuste vytvořit vlastní aplikaci, která bude zobrazovat počasí na aktální týden.

1. Forkem si vytvořte kopii [tohoto repozitáře](https://github.com/aellopos/cviceni-pocasi). Najdete v něm soubor s daty pro počasí na jeden týden.
1. V naší aplikaci budeme chtít vytvořit dvě stránky podle popisu dále. Zatím je nemusíme nijak horlivě stylovat, stačí nám zatím základní zobrazení dat.
1. Hlavní stránka bude `index.html` s přehledem počasí na sedm dní v týdnou, pondělí až pátek. Každý den bude zobrazen jako karta s názvem dne, teplotou a stavem typu zataženo, déšť, sníh, atd. Pro tuto stránku si vytvořte samostatný soubor `index.js` a naplňte HTML obsahem podle dodaných dat.
1. Po rozkliknutí karty na hlavní stránce se uživatel dostane na stránku `detail.html` s detailním přehledem počasí na daný den. Odkaz bude vypadat například `detail.html?den=pondeli`. Na stránce se zobrazí název dne, teploty ráno, odpoledne a večer, stav jako zataženo, déšť apod., vlhkost, tlak a slovní popis počasí.


# Ladění
## Recitály

U všech následujících úryvků kódů vytvořte technický popis jejich fungování a zároveň zkuste odhadnout záměr daného kódu. Obě dvě části si skutečně napište například do textového souboru.

1.  ```js
    const average = (a, b) => {
      return (a + b) / 2;
    };
    ```
1.  ```js
    const titleElement = document.querySelector('.title');
    titleElement.textContent = 'Nadpis';
    ```
1.  ```js
    let time = 0;
    setTimeout(() => {
      time += 1;
      console.log('time', time);
    }, 1000);
    ```
1.  ```js
    buttonOk.addEventListener('click', () => {
      document.body.innerHTML = '<p>Everything OK</p>';
    });
    ```
1.  ```js
    document.addEventListener('keyup', (event) => {
      if (event.code === 'KeyP') {
        console.log('paused');
      }
    });
    ```

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není :) 

</details>

