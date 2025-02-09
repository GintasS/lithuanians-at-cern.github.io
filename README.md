<h1 align="center" style="display: block; font-size: 2.5em; font-weight: bold; margin-block-start: 1em; margin-block-end: 1em;">
  <br /><br /><strong>lithuanians-at-cern.github.io</strong>
</h1>

## Įvadas


<a href="https://lithuanians-at-cern.github.io/" target="_blank">lithuanians-at-cern.github.io</a> yra Lietuvių bendruomenės CERN puslapis. Jis yra sukurtas su su Jekyll, Bootstrap 4 ir GitHub pages. Puslapis nėra fancy, bet jis yra skirtas perteikti esminę informacija lietuviams, pradedančiams savo kelionę CERN'e.

## Table of contents

- [Paleidimas](#paleidimas)
- [Struktūra](#struktura)
- [DUK](#duk)

## Paleidimas

Paleidimo instrukcijos yra <a href="https://nicolas-van.github.io/bootstrap-4-github-pages/" target="_blank">čia</a>.

## Struktūra

| Folderis/Failas    | Informacija |
| -------- | ------- |
| _includes_  | Saugomi pernaudojami .html failai kiekvienam puslapiui (footer, head, header). |
| _layouts_ | Saugomi .html failai, aprašantys puslapio struktūrą.     |
| _sass_    | Saugomi konfigūraciniai bootstrap failai (sukompiliuota bootstrap biblioteka, galima customazinti).    |
| assets    | Saugomi statiniai failai, kaip nuotraukos ar css ir .js.   |
| _config.xml    | Jekyll configuracija |
| update_bootstrap.sh | Scriptas turėtų upgradinti bootstrap versija |
| _sass/_variables.scss | Failas, skirtas keisti pagrindinius bootstrap elementus |


## DUK

### Kaip pridėti naują puslapį (kaip "pranešimai")?

1. Pagrindiniame kataloge sukuriate .MD arba .html failą "puslapio_pavadinimas.md" ar "puslapio_pavadinimas.html".
2. Atliekate reikiamus pakeitimus naujai sukurtame faile.
3. Pridėti puslapį į navbar ```_includes/header.html```:

    ```
    <li class="nav-item">
      <a class="nav-link" style="color:white;" href="{{ "/puslapio_pavadinimas" | relative_url }}">puslapio_pavadinimas</a>
    </li>
    ```    
4. Jūs turite naują puslapį :)

### Kaip galima pridėti naujų klausimų-atsakymų į DUK?

Tai yra visai paprastas procesas:

1. Atsidarote ```index.html``` failą.
2. Pasirenkate tinkamą vietą (kaip pvz ```<div class="collapse" id="collapseGeneralQuestions">``` - bendrinių klausimų div elementas).
3. Nukopijuojate esamą **card** elementą arba įkeliate šitą:

    ```
    <div class="card">
      <div class="card-header p-2" id="heading1">
          <h5 class="mb-0">
              <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapse1" aria-expanded="true" aria-controls="collapse1">
                Klausimas
              </button>
            </h5>
      </div>

      <div id="collapse1" class="collapse" aria-labelledby="heading1" data-parent="#faqExample">
          <div class="card-body">
            Atsakymas
          </div>
      </div>
    </div>  
    ```
4. Pakeičiate Klausimo ir Atsakymo vietą. 
5. Taip pat pakeičiate skaičiukus prie ```id="heading1"```, ```data-target="#collapse1"```, ```id="collapse1"```, ```aria-labelledby="heading1"``` į kitą skaičiuką kurio nėra, pvz 50.

  Šie skaičiukai yra naudojami sulinkinti cardą (```<div class="card-header p-2">```) su turiniu (```<div id="collapse1" class="collapse"```).

6. Išsaugojate ```index.html``` failą.

### Kaip buvo sukurtas puslapis?

Puslapis buvo paiimtas iš atvirojo kodo <a href="https://github.com/nicolas-van/bootstrap-4-github-pages" target="_blank">repozitorijos</a>.


<!-- markdownlint-enable -->
