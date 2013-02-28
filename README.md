# Szablon jekyll-bloga

Dostosowany do konfiguracji serwera *Sigma* szablon
jekyll-bloga.


## Instalacja szablonu

Klikamy w ikonkę **fork** i natępnie klonujemy sforkowanego bloga
na swoje konto na serwerze *Sigma*.

Cała procedura może wyglądać tak:
<pre>git clone git@github.com:⟨twój login na <b>githubie</b>⟩/jblog.git blog
cd blog
</pre>


## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.md

na przykład:

    2013-02-29-jekyll-howto.md

Po napisaniu posta generujemy statyczną wersję bloga wykonując
z katalogu z blogiem, czyli z katalogu **blog/** polecenie:

    jekyll --server PORT # testowanie, localhost:PORT

Jeśli wszystko jest OK, to wdrażamy bloga na Sigmę:

    rake deploy          # uaktualnić DESTINATION

Po wykonaniu polecenia blog jest dostępny tutaj:

<pre>http://sigma.ug.edu.pl/~⟨twój login na <b>sigmie</b>⟩/blog
</pre>


## Korzystamy z rozszerzeń

Jak? Opisane jest to w [jekyll_ext](http://github.com/rfelix/jekyll_ext).


# Ściąga z Git-a

Kilka użytecznych poleceń…

## Tracking branches

Po sforkowaniu projektu, na przykład
[emacs starter kit](https://github.com/technomancy/emacs-starter-kit)
którego autorem jest *technomancy*, klonujemy repozytorium
projektu na swój komputer:

    git clone git@github.com:wbzyl/emacs-starter-kit.git

Jak nakazują dobre obyczaje, dodajemy oryginalne repozytorium
do swojego jako *remote*:

    git remote add technomancy git://github.com/technomancy/emacs-starter-kit.git

i od razu ściągamy oryginał:

    git fetch technomancy

Po jakimś czasie zauważamy, że technomancy dodał nową gałąź **v2**:

    origin/HEAD -> origin/master
    origin/master
    technomancy/master
    technomancy/v2

Oczywiście, natychmiast chcielibyśmy sprawdzić jak działa v2.
Najwygodniej będzie dodać do swojego repozytorium nową gałąź
na którą będziemy pobierać nowe wersje **v2** z repozytorium technomancy.

W tym celu tworzymy tzw. *tracking branch*:

    git checkout --track technomancy/v2
    git checkout -b v2.x --track technomancy/v2 # lub tak, zmieniamy nazwę gałęzi na v2.x

Teraz polecenie:

    git branch -a
      master
    * v2
      remotes/origin/HEAD -> origin/master
      remotes/origin/master
      remotes/technomancy/master
      remotes/technomancy/v2

pokazuje, że faktycznie jesteśmy jesteśmy na nowej gałęzi.

Różnice w kodzie między gałęziami można sprawdzić bez tworzenia
nowej gałęzi:

    git diff master..technomancy/master
