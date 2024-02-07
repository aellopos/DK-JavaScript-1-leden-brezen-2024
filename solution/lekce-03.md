# Příklady - Vstup a výstup

## Očkování

Představte si, že vyrábíte registrační systém na očkování proti COVID-19. U každého registrovaného chceme evidovat jméno a věk.

1. Vytvořte webovou stránku, která se uživatele zeptá nejdříve na jméno a poté na věk. Tyto hodnoty si uložte do smysluplně pojmenovaných proměnných. Nezpomeňte věk převést na číslo.
1. Poté, co uživatel zadá všechny údaje, vypište do stránky odstavec s obsahem ve tvaru
   ```
   Květoslav Voňavý, věk: 67
   ```


<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není :)

</details>

## Výplata jako stránka

1. Vytvořte webovou stránku, která uživatele požádá o jeho hodinovou sazbu v korunách a spočítá jeho hrubou mzdu za předpokladu, že pracuje 8 hodin denně 21 dní v měsíci. Do stránky vypište výsledek zabalený do nějaké přívětivé formulace. Dbejte na to, abyste korektně převedli uživatelem zadanou hodnotu na číslo.
1. Nechte uživatele zadat nejen hodinovou sazbu, ale také počet hodin a dní v měsíci. Opět dejte pozor na správnou konverzi.

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není :)

</details>

# Příklady - Objekty

## Realitka

Mějme následující objekt představující inzerát na stránkách nějaké realitní kanceláře.

```js
const apartment = {
  type: 'rent',
  disposition: '3+1',
  area: {
    floorage: 100,
    balcony: 2,
    units: 'sqm',
  },
  city: 'Prague',
  district: 'Old Town',
  price: {
    rent: 28000,
    fees: {
      water: 1000,
      energy: 2500,
      services: 560,
    },
    currency: 'czk',
  },
  ownership: 'personal',
  condition: 'renovated',
  status: 'free',
  floor: 3,
};
```

Vytvořte webovou stránku s JavaScriptem, zkopírujte si tento kód do vašeho programu a vyřešte následující úkoly.

1. Pomocí tečkové notace vypište do stránky dispozici bytu.
1. Vypište do stránky čistý nájem bez poplatků.
1. Vypište do stránky celý objekt představující výměru bytu.
1. Do separátních proměnných uložte město a městskou část. Vypište je do stránky.
1. Změnte stav inzerátu z `'free'` na `'taken'`.

<details>
<summary><b>Řešení</b></summary>


Tady zatím nic není :)

</details>

## Knihovna

1. V JavaScriptovém programu vytvořte objekt představující jednu knihu v knihovně. Uvažte, jaké vlastnosti může taková kniha mít. Rozhodně budeme chtít název, autora a počet stran. Přidejte do objektu alespoň tři další vlastnosti tak, aby obsahovaly čísla, řetězce i vnořený objekt.
1. Vytvořte alespoň jednu další knihu se stejnými vlastnostmi ale jinými hodnotami.`


<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není :)

</details>

## Očkování – objekty

Pokračujme v našem registračním systému na očkováni. Zatím se umíme uživatele zeptat na jméno a věk.

1. Vytvořte objekt `person`, do kterého vložte uživatelem zadané údaje. Objekt bude mít následující strukturu
   ```js
   {
     name: 'Květoslav Voňavý',
     age: 67,
   }
   ```
1. Přidejte do objektu `person` údaj o tom, v jakém jazyce si uživatel přeje komunikovat. Zjistěte jej z objektu `window`.
1. Poté, co uživatel zadá všechny údaje, vypište do stránky objekt `person` se všemi jeho vlastnostmi v nějakém hezkém formátu a zkontrolujte, že obsahuje správné informace.


<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není :)

</details>