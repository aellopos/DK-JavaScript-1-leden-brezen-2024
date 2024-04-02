# Práce s poli
## Pole v divadle
Cvičení provádějte ve vašem JavaScript souboru.

1. Vytvořte pole celých čísel, například počty diváků na několika po sobě jdoucích divadelních představeních. Použijte metodu `push` a přidejte do pole počet diváků na novém představení.
1. Vytvořte pole desetinných čísel, například zaplněnost divadla v několika po sobě jdoucích představeních. Poté pomocí metody `pop` odstraňte poslední hodnotu v poli.
1. Vytvořte pole řetězců, například seznam názvů několika divadelních představení, která divadlo hraje. Uložte toto pole do proměnné `plays`. Uložte do jiné proměnné druhou položku tohoto pole.
1. Uložte do proměnné `reviews` pole hodnocení, které obdržela divadelní hra _Plyšáci na útěku_ v různých recenzních časopisech. Hodnocení je vždy objekt obsahující název recenzního časopisu jako řetězec a samotné hodnocení jako číslo mezi 1 až 10.

<details>
<summary><b>Řešení</b></summary>

```js
const spectators = [77, 43, 15, 99, 30];
spectators.push(12);

const theatre = [13.5, 12.7, 11.2, 12.3, 15.1];
theatre.pop();

const plays = [
  'Pýcha a předsudek ',
  'Maryša',
  'Kauza pražské kavárny',
  'Kdo je tady ředitel?',
];
let second = plays[1];

const reviews = [
  { magazine: 'Slovenka', rating: 10 },
  { magazine: 'Zivot', rating: 8 },
  { magazine: 'Divadelní Luk', rating: 9 },
  { magazine: 'Makarony', rating: 1 },
];
```

</details>

## Práce s indexy
Cvičení provádějte ve vašem JavaScript souboru.

1.  Napište funkci `first`, která jako svůj parametr přijme pole a vrátí první prvek tohoto pole. Pokud pole bude prázdné, funkce vrátí `undefined`. Funkci otestujte s několika různými poli. Například:

    ```js
    first([3, 2, 1]); // ⟶ 3
    first([]); // ⟶ undefined
    ```

1.  Napište funkci `last`, která jako svůj parametr přijme pole a vrátí poslední prvek tohoto pole. Pokud pole bude prázdné, funkce vrátí `undefined`. Funkci otestujte s několika různými poli. Například:

    ```js
    last([3, 2, 1]); // ⟶ 1
    last([]); // ⟶ undefined
    ```

1.  Napište funkci `middle`, která jako svůj parametr přijme pole a vrátí prvek uprostřed tohoto pole. Pokud pole bude prázdné, funkce vrátí `undefined`. Pokud pole bude obsahovat sudý počet prvků, vrátí funkce prvek vlevo od středu. Funkci otestujte s několika různými poli. Například:

    ```js
    middle([3, 2, 1]); // ⟶ 2
    middle([3, 2, 1, 0]); // ⟶ 2
    middle([]); // ⟶ undefined
    ```

1.  Napište funkci `middleMean`, která jako svůj parametr přijme pole a vrátí prvek uprostřed tohoto pole. Pokud pole bude prázdné, funkce vrátí `undefined`. Pokud pole bude obsahovat sudý počet prvků, vrátí funkce průměr dvou prvků uprostřed. Funkci otestujte s několika různými poli. Například:

    ```js
    middleMean([3, 2, 1]); // ⟶ 2
    middleMean([3, 2, 1, 0]); // ⟶ 1.5
    middleMean([]); // ⟶ undefined
    ```

1.  Napište funkci `insert`, která jako první parametr přijme pole a jako druhý parametr nějakou hodnotu. Funkce zkontroluje, zda pole již obsahuje tuto hodnotu. Pokud ano, vrátí `false`. Pokud ne, vloží hodnotu na konec pole a vrátí `true`. Funkci otestujte s několika různými poli. Například:

    ```js
    insert([3, 2, 1], 4); // ⟶ true
    insert([3, 2, 1], 3); // ⟶ false
    ```


## Počítání oveček
Vytvořte JavaScriptový program, který vepíše do stránky ovčí příběh pro děti na dobrou noc. Výsledkem by měl být text počítající ovečky.

1. Vytvořte si nový projekt - index.html a script.js. Soubory propojte.

1. Využijte následujících dvacet jmen oveček:

   ```js
   const ovciJmena = [
     'Bětuška',
     'Cína',
     'Dolly',
     'Heidy',
     'Líza',
     'Belinda',
     'Celia',
     'Elvíra',
     'Karla',
     'Otýlie',
     'Škraboška',
     'Kopretinka',
     'Berta',
     'Růženka',
     'Bobinka',
     'Žofka',
     'Dášenka',
     'Vlnka',
     'Květuše',
     'Pampeliška',
   ];
   ```

1. Pomocí metody `forEach` do stránky vepište deset za sebou jdoucích vět v následující podobě:

   > Ovečka Bětuška jako 1. přeskočila přes plot. Ovečka Cína jako 2. přeskočila přes plot. Ovečka Dolly jako 3. přeskočila přes plot…
<details>
<summary><b>Řešení</b></summary>

```js
ovciJmena.forEach((jmeno, index) => {
  document.body.textContent += `Ovečka ${jmeno} jako ${
    index + 1
  }. přeskočila přes plot. `;
});
```

</details>


# Metody forEach a map
## Jednohubky pro `map`

Založte si JavaScriptový program a do něj vložte následující data:

```js
const cisla = [7, 1, 4, 5, 2, 9, 3, 6, 8];
const zvirata = [
  'pes',
  'kočka',
  'králík',
  'had',
  'andulka',
  'morče',
  'krkavec',
];
const napoje = [
  { nazev: 'Pivo', cena: 12, skladem: true },
  { nazev: 'Rum', cena: 120, skladem: false },
  { nazev: 'Víno', cena: 85, skladem: true },
  { nazev: 'Whisky', cena: 450, skladem: true },
  { nazev: 'Vodka', cena: 280, skladem: false },
  { nazev: 'Becherovka', cena: 210, skladem: true },
  { nazev: 'Kofola', cena: 40, skladem: true },
  { nazev: 'Voda', cena: 15, skladem: false },
];
```

Pomocí metody `map` vždy vytvořte pole dle zadání a vypište jej pro kontrolu do konzole (použijte `console.log`).

1. Vytvořte nové pole, které bude obsahovat všechna čísla z pole `cisla` vynásobená dvěma.
1. Vytvořte nové pole, které bude obsahovat délky všech řetězců z pole `zvirata`.
1. Vytvořte nové pole, které bude obsahovat pouze názvy všech nápojů z pole `napoje`.
1. Vytvořte nové pole, které bude obsahovat pouze název nápoje z pole `napoje`, pokud je nápoj skladem, v opačném případě bude obsahovat řetězec `Není skladem`.

<details>
<summary><b>Řešení</b></summary>

```js
const kratDva = cisla.map((cislo) => cislo * 2);
console.log(kratDva);

const delky = zvirata.map((zvire) => zvire.length);
console.log(delky);

const nazvy = napoje.map((napoj) => napoj.nazev);
console.log(nazvy);

const skladem = napoje.map((napoj) => {
  if (napoj.skladem) {
    return napoj.nazev;
  } else {
    return 'Není skladem';
  }
});
```


</details>

## Nezaplacené objednávky
Pracujete na velkém e-shopu a vaším úkolem je z nezaplacených objednávek vybrat všechny identifikátory a e-maily zákazníků pro zpracování dalšími systémy.

1. Vycházejte ze šablony na GitHubu [cviceni-nezaplacene-objednavky](https://github.com/aellopos/cviceni-nezaplacene-objednavky).

1. Upravte soubor `app.js` tak, aby nachystal dvě nová pole `identifikatory` a `emaily`.

   1. Pole `const identifikatory = []`a `const emaily = []` jsou již předpřipravené. Upravte části za rovnítky. Využijte metodu `map` na poli `nezaplaceneObjednavky`.

   1. Zařiďte, aby v prvním poli `identifikatory` byly pouze čísla, jednotlivá `id` z původního pole `nezaplaceneObjednavky`. Představte si, že čísla bude zpracovávat skladový systém, který je potřebuje přesně v této podobě.

   1. V druhém poli by měly být pouze řetězce, jména s e-maily zákazníků ve formátu `Jméno <jmeno@server.cz>`, aby se daly snadno zpracovat e-mailovým serverem.

1. Poslední dva předchystané řádky nijak neupravujte. Představte si, že místo nich bude jednou kód, který předá vámi vytvořená pole dalším systémům.

   ```js
   processEmails(emaily);
   processIdentifiers(identifikatory);
   ```


<details>
<summary><b>Řešení</b></summary>

```js
console.log('Funguju!')

const nezaplaceneObjednavky = [
	{
		id: 159753246,
		polozky: [
			{ nazev: 'knihy', mnozstvi: 5, cena: 200 },
			{ nazev: 'pero', mnozstvi: 1, cena: 50 },
			{ nazev: 'sešity', mnozstvi: 3, cena: 100 },
		],
		datum: '2023-04-07',
		uzivatel: {
			jmeno: 'Tomáš',
			email: 'tomas@volny.cz',
		},
	},
	{
		id: 456123789,
		polozky: [
			{ nazev: 'notebook', mnozstvi: 1, cena: 12000 },
			{ nazev: 'myš', mnozstvi: 1, cena: 400 },
			{ nazev: 'klávesnice', mnozstvi: 1, cena: 800 },
			{ nazev: 'sluchátka', mnozstvi: 1, cena: 1500 },
		],
		datum: '2023-04-08',
		uzivatel: {
			jmeno: 'Markéta',
			email: 'marketa@seznam.cz',
		},
	},
	{
		id: 987654321,
		polozky: [
			{ nazev: 'plavky', mnozstvi: 1, cena: 400 },
			{ nazev: 'papuče', mnozstvi: 1, cena: 100 },
			{ nazev: 'ručník', mnozstvi: 2, cena: 150 },
		],
		datum: '2023-04-09',
		uzivatel: {
			jmeno: 'Johanka',
			email: 'johanka@gmail.com',
		},
	},
	{
		id: 123456789,
		polozky: [
			{ nazev: 'tričko', mnozstvi: 2, cena: 250 },
			{ nazev: 'džíny', mnozstvi: 1, cena: 600 },
			{ nazev: 'boty', mnozstvi: 1, cena: 800 },
			{ nazev: 'pásek', mnozstvi: 1, cena: 100 },
		],
		datum: '2023-04-10',
		uzivatel: {
			jmeno: 'Jane',
			email: 'jane@outlook.com',
		},
	},
	{
		id: 852963741,
		polozky: [
			{ nazev: 'míč', mnozstvi: 1, cena: 300 },
			{ nazev: 'brankářské rukavice', mnozstvi: 1, cena: 800 },
			{ nazev: 'tréninkové dresy', mnozstvi: 10, cena: 500 },
			{ nazev: 'plíškový medvídek', mnozstvi: 1, cena: 150 },
		],
		datum: '2023-04-04',
		uzivatel: {
			jmeno: 'Ruda',
			email: 'ruda@email.cz',
		},
	},
	{
		id: 753951824,
		polozky: [
			{ nazev: 'matrace', mnozstvi: 1, cena: 5000 },
			{ nazev: 'polštář', mnozstvi: 2, cena: 300 },
			{ nazev: 'povlečení', mnozstvi: 1, cena: 800 },
		],
		datum: '2023-04-06',
		uzivatel: {
			jmeno: 'Novákovi',
			email: 'novakovi@seznam.cz',
		},
	},
]

const processEmails = (emails) => {
	document.querySelector('#emaily').textContent = emails.join(', ')
}

const processIdentifiers = (identifiers) => {
	document.querySelector('#identifikatory').textContent = identifiers.join(', ')
}

const identifikatory = nezaplaceneObjednavky.map((objednavka) => {
	return objednavka.id
})

const emaily = nezaplaceneObjednavky.map((objednavka) => {
	return `${objednavka.uzivatel.jmeno} <${objednavka.uzivatel.email}>`
})

processEmails(emaily)
processIdentifiers(identifikatory)
```


</details>

   