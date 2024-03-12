# Cvičení: Funkce jako argumenty
## Hesla

Vytvořte si repozitář ze šablony [cviceni-hesla](https://github.com/Czechitas-podklady-WEB/cviceni-hesla) se stránkou, která obsahuje tři různé funkce na generování hesel. Každá funkce vygeneruje heslo zadané délky s určitou bezpečnostní silou. Kód funkcí zkoumat nemusíte, obsahuje věci, které jsme zatím neprobírali.

Příklad samostatného použití jednotlivých funkcí:

```js
weakPassword(5); // → '01234'
```

```js
mediumPassword(8); // → '48140525'
```

```js
strongPassword(6); // → 'azc7mw'
```

Napište funkci `createAccount`, která se bude tvářit, že zakládá nový uživatelský účet. Funkce bude mít **dva parametry** `user` a `generatePassword`. **První bude uživatelské jméno** a **druhý bude funkce**, pomocí které se má vygenerovat heslo pro tento účet. Funkce `createAccount` **vrátí řetězec**, který bude obsahovat jméno uživatele a heslo vygenerované voláním funkce `generatePassword`. Funkci `generatePassword` při volání předejte **číslo 9** jako délku hesla.

Na konci javascriptového kódu vyzkoušejte založit více různých účtů s různými typy hesel. Například:

```js
document.body.innerHTML += `
	<p>${createAccount('Míša', weakPassword)}</p>
	<p>${createAccount('Řízek', mediumPassword)}</p>
	<p>${createAccount('Mápodčepicí', strongPassword)}</p>
`;
```

by mělo vepsat do stránky něco jako:

```text
Uživatel Míša s heslem 012345678
Uživatel Řízek s heslem 074031827
Uživatel Mápodčepicí s heslem mwwf9epts
```

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není

</details>

## E-mail podruhé

Pojďme dále rozvinout cvičení s [vyplňováním e-mailu](https://github.com/aellopos/cviceni-email/tree/main) z předchozí lekce.

1. Vytvořte si repozitář ze šablony [cviceni-email-podruhe](https://github.com/aellopos/cviceni-email-podruhe).
1. Všimněte si funkce `goodbye`, která generuje pozdrav na konec e-mailu. Přidejte alespoň dvě další funkce, kde každá generuje k zadanému jménu jiný typ pozdravu. Například `formalGoodbye` pro velmi formální pozdravy jako „S uctivou poklonou…“, nebo naopak `rudeGoodbye` typu „Se měj…“, pokud se chcete rozloučit nevybíravě.
1. Upravte funkci `fillBody` tak, aby brala třetí parametr `goodbyeFunction` představující funkci, pomocí které se má vygenerovat závěrečný pozdrav. Vyzkoušejte zavolat funkci `fillBody` postupně s každou z vašich zdravících funkcí a ověřte, že vše správně funguje.

#### Ukázka použití

```js
fillSubject('Obchodní sdělení');
fillBody(
  'Kupte mycí prostředek, který vám vytře zrak, se slevou 50 %.',
  'Jan Čistý',
  formalGoodbye
);
```

nebo

```js
fillSubject('Pozvánka na oslavu narozenin');
fillBody('Zítra oslava. 18:00 ve Starý hospodě.', 'Patrik Veselý', rudeGoodbye);
```

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není

</details>

# Cvičení: Události
## Objednavka

Vytvoříme jednoduchou stránku s objednávacím tlačítkem.

1. Založte HTML stránku s jedním tlačítkem
   ```html
   <button id="button-order">Objednat</button>
   ```
1. Doplňte do stránky JavaScriptový program, který zařídí, že po stisknutí tlačítka se do stránky za tlačítko vypíše odstavec:
   ```html
   <p>Objednáno</p>
   ```
1. Upravte program tak, že text se nevypíše do stránky, ale zobrazí se na samotném tlačítku.

[ukázka řešení](../images/ukazka.gif)

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není

</details>

## Kontrola dosupnosti
Vyjděte z řešení předchozího příkladu, kdy se objednává při kliknutí na tlačítko.

1. Zařiďte úpravou přímo **v HTML souboru**, aby při načtení stránky tlačítko obsahovalo zprávu _Kontroluji dostupnost…_
1. Přidejte do stránky zpoždění pomocí funkce `setTimeout`, která zařídí, že **8 vteřin** po načtení stránky se zpráva na tlačítku změní na _Objednat_.
1. Tlačítka mají speciální HTML atribut s názvem `disabled`. Pokud je tento atribut přítomen, na tlačítko se nedá kliknout. Přidejte tento **atribut do HTML** kódu tlačítka, aby tlačítko bylo při načtení stránky nedostupné/neklikatelné. Až **po uplynutí časovače jej zpřístupněte** nastavením vlastnosti `disabled` v JavaScriptu na `false`.

[ukázka řešení](../images/ukazka2.gif)

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není

</details>

## Zarovka

Vytvořte si repozitář ze šablony [cviceni-zarovka](https://github.com/aellopos/cviceni-zarovka) se stránkou, která zobrazuje obyčejnou žárovku.

1. Pomocí JavaScriptu zařiďte, aby se při stisknutí libovolné klávesy na stránce přidala k elementu žárovky CSS třída `bulb--on`. Žárovka by se takto měla rozsvítit.
1. Vylepšete program tak, aby na následné stisknutí libovolné klávesy žárovka opět zhasnula. Opakovaným mačkáním kláves ji tak můžeme rozsvěcovat a zhasínat.

[ukázka řešení](../images/zarovka.gif)

<details>
<summary><b>Řešení</b></summary>

Tady zatím nic není

</details>
