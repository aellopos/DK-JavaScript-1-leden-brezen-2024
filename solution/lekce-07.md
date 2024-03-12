# Cvičení: Procvičování funkcí

## E-mail, pozdravy

Vytvořte si repozitář ze šablony [cviceni-email](https://github.com/aellopos/cviceni-email/tree/main) se stránkou obsahující šablonu jednoduchého e-mailu.

Každý e-mail je třeba zakončit zdvořilým pozdravem.

1. V souboru `index.js` vytvořte funkci bez parametrů s názvem `goodbye`. Tato funkce vloží do odstavce s třídou `email__closing` rozloučení „Na shledanou“.
1. Zavolejte funkci `goodbye()` na konci souboru `index.js`. Ověřte, že se na zobrazené stránce správně změnil pozdrav na konci e-mailu.
1. Končit e-mail jen slovy „Na shledanou“ je nezdvořilé. Přidejte proto do funkce `goodbye` parametr představující jméno pisatele e-mailu. Funkce do posledního odstavce vloží koncový pozdrav i se jménem. Příklad použití:

   ```js
   goodbye('Pavel Ovesný');
   ```

   Ve stránce bude

   > S pozdravem Pavel Ovesný

<details>
<summary><b>Řešení</b></summary>

Obsah souboru `index.js`:

```js
const goodbye = (name) => {
  const closingElement = document.querySelector('.email__closing');
  closingElement.textContent = `Na shledanou ${name}`;
};

goodbye('tě pic');
```

</details>

## E-mail, tělo

Pokračujte na stránce z přechozího příkladu.

1. Do souboru `index.js` přidejte funkci `fillSubject` s jedním parametrem `subject`. Tato funkce ze stránky vybere DOM element představující předmět e-mailu a nastaví jeho obsah na řetězec, který přišel v parametru.
1. Zavolejte funkci na konci souboru `index.js` a vykoušejte si nastavit předmět e-mailu na nějaký smysluplný text.
1. Napište funkci `fillBody` s jedním parametrem `body`, která ze stránky vybere DOM element představující tělo e-mailu a nastaví jeho obsah dle hodnoty parametru.
1. Zavolejte funkci na konci souboru `index.js` a ověřte, že v zobrazené stránce správně změní tělo e-mailu.
1. Z předchozího cvičení nám zůstala funkce `goodbye`. Do funkce `fillBody` přidejte další parametr s názvem `name`. Tento parametr bude představovat jméno odesílatele. Funkce vyplní tělo e-mailu a do elementu `email__closing` vloží pozdrav, který vyrobí pomocí volání funkce `goodbye`.

<details>
<summary><b>Řešení</b></summary>

Obsah souboru `index.js`:

```js
const goodbye = (name) => {
  return 'S pozdravem ' + name;
};

const fillSubject = (subject) => {
  document.querySelector('.email__subject').textContent = subject;
};

const fillBody = (body, name) => {
  const bodyElm = document.querySelector('.email__body');
  bodyElm.innerHTML += body;
  const closingElm = document.querySelector('.email__closing');
  closingElm.textContent = goodbye(name);
};

fillSubject('Nepřišly gumičky');
fillBody(
  'Nepřišly gumičky. A co na to počítač? Mlčí. No tak to je konec. Všecko vylejt.',
  'referent Kubrt'
);
```

</details>

## Převod měny


Napište funkci `convertToCZK`, která převede částku zadanou v cízí měně na české koruny. Funkce bude podporovat následující měny a kurzy.

| Měna           | Kód | Kurz   |
| -------------- | --- | ------ |
| Euro           | EUR | 24.47  |
| Britská libra  | GBP | 28.09  |
| Americký dolar | USD | 24.81  |
| Bitcoin        | BTC | 478637 |

Výslednou částku zakrouhlete na celé koruny. Příklad použití:

```js
document.body.innerHTML += convertToCZK(25, 'EUR');
```

Pokud funkce jako parametr dostane neznámý kód měny, vrátí jako výsledek `null`. Otestujte funkci výpisem výsledku do stránky.

<details>
<summary><b>Řešení</b></summary>

```js
const convertToCZK = (amount, currency) => {
  let rate;

  if (currency === 'EUR') {
    rate = 24.47;
  } else if (currency === 'GBP') {
    rate = 28.09;
  } else if (currency === 'USD') {
    rate = 24.81;
  } else if (currency === 'BTC') {
    rate = 478637;
  } else {
    return null;
  }

  return Math.round(rate * amount);
};

document.body.innerHTML += `100 € je ${convertToCZK(100, 'EUR')} Kč<br>`;
document.body.innerHTML += `£ 100 je ${convertToCZK(100, 'GBP')} Kč<br>`;
document.body.innerHTML += `$ 100 je ${convertToCZK(100, 'USD')} Kč<br>`;
document.body.innerHTML += `100 bitcoinů je ${convertToCZK(100, 'BTC')} Kč<br>`;
```


</details>

# Cvičení: Porozumění kódu + další

## Porozumění kódu

Přečtěte si následující úryvky kódu a u každého řekněte, co program vypíše do stránky aniž byste program spouštěli.

Úryvek 1:
```js
const name = 'Mississippi';

if (name.length > 5) {
  const name = 'Missi';
  document.body.innerHTML += `<p>${name}</p>`;
}

document.body.innerHTML += `<p>${name}</p>`;
```

Úryvek 2:
```js
const name = 'Franta';

const greet = (name) => {
  const name = 'Pepa';
  document.body.innerHTML += `<p>${name}</p>`;
};

greet('Jožin');
```

Úryvek 3:
```js
const age = 25;

if (age > 21) {
  const price = 100;
} else if (age > 15) {
  const price = 50;
} else {
  const price = 0;
}

document.body.innerHTML += `<p>${price}</p>`;
```

## Výplňořez

1. Napište funkci `fillcut`, která jako svůj první parametr `str` očekává řetězec a jako druhý parametr `len` kladné celé číslo. Úkolem funkce je oříznout nebo prodloužit zadaný řetězec tak, aby měl délku přesně `len`.
   - Pokud je vstupní řetězec delší než `len`, tak funkce odřízne jeho konec a vrátí výsledek.
   - Pokud je vstupní řetězec kratší než `len`, tak jej doplní od začátku znakem tečky a vrátí výsledek.
   - Pokud je vstupní řetězec dlouhý přesně `len`, funkce jej vrátí beze změny.

Příklad použití:

```js
document.body.innerHTML += fillcut('petr', 8) + '<br>'; // vypíše „....petr“
document.body.innerHTML += fillcut('petr', 3) + '<br>'; // vypíše „pet“
document.body.innerHTML += fillcut('petr', 4) + '<br>'; // vypíše „petr“
```

<details>
<summary><b>Řešení</b></summary>

```js
const fillcut = (str, len) => {
  if (str.length > len) {
    return str.slice(0, len);
  } else if (str.length < len) {
    return str.padStart(len, '.');
  } else {
    return str;
  }
};
```

</details>