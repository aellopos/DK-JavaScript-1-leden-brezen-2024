# Příklady

## Házení kostkou

Vymyslete, jak použít funkci `Math.random` a různé zaokrouhlovací funkce probírané v této lekci k simulování hodu klasickou šestistěnnou kostkou. S použitím vhodných funkcí sestavte výraz, který vygeneruje náhodné celé číslo **mezi 1 a 6**.

Zamyslete se nad tím, zda vámi vytvořený výraz generuje všechna čísla skutečně se stejnou pravděpodobností. Vemte v úvahu, že funkce `Math.random` generuje náhodná čísla mezi 0 (včetně) a 1 (vyjma). Je tedy malinká pravěpodobnost, že **občas padne přesně číslo 0**. Naopak **číslo 1 padnout nemůže**.

<details>
<summary><b>Řešení</b></summary>

```js
1 + Math.floor(Math.random() * 6);
```

</details>

## Příjem divadla

1. Jeden lístek do divadla :i[Pěst na oko] stojí **12 euro**. Spočítejte měsíční příjem divadla ze vstupného, přichází-li průměrně **174 návštěvníků** na jedno představení a divadlo hraje **15 představení** měsíčně. Uložte výsledek do proměnné `prijem`.
1. Hodnotu proměnné `prijem` vypište do stránky.
1. Divadlo se rozhodlo prodávat studentské vstupné ve výši **65 %** plného vstupného. Jak se změní měsíční příjem divadla pokud víme, že **40 %** návštěvníků jsou studenti?
1. Vypište do stránky i příjem divadla se započítanou slevou pro studenty.


<details>
<summary><b>Řešení</b></summary>

```js
const plnaCena = 12;
const pocetNavstevnikuNaPredstaveni = 174;
const pocetPredstaveniZaMesic = 15;
const prijem =
  plnaCena * pocetNavstevnikuNaPredstaveni * pocetPredstaveniZaMesic;
document.body.innerHTML = '<p>Příjem divadla: ' + prijem + ' Kč</p>';

const studentskaCena = 0.65 * plnaCena;
const studenti = 0.4;
const prijmySeStudenty =
  (plnaCena * (1 - studenti) + studentskaCena * studenti) *
  pocetNavstevnikuNaPredstaveni *
  pocetPredstaveniZaMesic;
document.body.innerHTML +=
  '<p>Příjem divadla se slevou pro studenty: ' + prijmySeStudenty + ' Kč</p>';
```

</details>

