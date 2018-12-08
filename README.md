# lithuanians-at-cern.github.io
[lithuanians-at-cern.github.io](https://lithuanians-at-cern.github.io/)

## Instrukcija

Nepatingime ir naudojame *webp*, jpg seniai nusipelnęs keliauti į istorijos
šiukšlyną.


## Lokalus development'as
Isidiekit docker'į. Tada:

```bash
git clone git@github.com:lithuanians-at-cern/lithuanians-at-cern.github.io.git
cd lithuanians-at-cern.github.io

# paleidziam dockeri ir prisijungiam prie terminalo
docker run -it -p 4000:4000 -v $(pwd):/site jekyll/jekyll  /bin/bash   # leisti su `sudo` jei truksta teisiu
cd /site    # mountpointas i musu puslapio src
bundle install  # sudiegiam dependency
jekyll serve      # paleidziam serveri 

```

### Naudingos nuorodos
* [Temos dokumentacija](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
* [Pavyzdžiai](https://github.com/mmistakes/minimal-mistakes/tree/gh-pages-3.1.6)

### Turinio pridėjimas
* Naujienos (Postai):
	* Pagal pavyzdį `_posts` direktorijoje sukuriamas kitas failas. 
* Puslapis:
	* Pagal pavyzdį `_pages` direktorijoje sukuriamas failas.
	* Tam, kad jis būtų pasiekimas iš puslapio, `_data/navigation.yml` reikia pridėti įrašą apie jį.
* Juodraščiai laikomi `_draft` direktorijoje.
* `index.html` yra titulinis puslapis 

## TODO 
* Puslapis
* Turinys
	* DUK
	* Stažuotės
	* Kontaktai
