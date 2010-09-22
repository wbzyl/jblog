# Szablon jekyll-bloga 

Dostosowany do konfiguracji serwera *Sigma* szablon bloga.
Statyczne strony bloga generujemy za pomocą programu *jekyll*.


## Instalacja

Klikamy w ikonkę **fork** i natępnie klonujemy sforkowanego bloga
na swoje konto na serwerze *Sigma*. Klona umieszczamy w katalogu
*public_git*, który musimy wcześniej utworzyć.

Cała procedura może wyglądać tak:

<pre>mkdir -p ~/public_git/
cd ~/public_git/
git clone git@github.com:⟨twój login na <b>githubie</b>⟩/jblog.git sp
</pre>

gdzie nazwa katalogu *sp* to skrót (modulo polskie literki)
od nazwy wykładu „Środowisko programisty”.


## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.markdown

na przykład:

    2009-06-12-jekyll-howto.markdown

Po napisaniu posta generujemy statyczną wersję bloga wykonując z
katalogu z blogiem, czyli z katalogu **~/public_git/sp/** polecenie:

    jekyll ~/public_html/blog

Po wykonaniu polecenia blog jest dostępny pod URI:

<pre>http://sigma.inf.ug.edu.pl/~⟨twój login na <b>sigmie</b>⟩/blog
</pre>

## Kończymy instalację

W *jBlogu* jest kilka napisów, które pewnie należy wymienić,
na przykład, w pliku *index.html* znajdziemy:

    title: Mój_Blog

w plikach *_layouts/default.html* i :*_layouts/index.html*

    <meta name="author" content="Imię Nazwisko" />.
    ...
 
w pliku *atom.xml*:

    <title>Imię Nazwisko</title>
    <link href="http://sigma.inf.ug.edu.pl/~login_na_sigmie/atom.xml" rel="self"/>
    ...

Oczywiście można też przygotowac samemu logo. Ale przygotowanie
fajnego logo może nieco potrwać. Dlatego ta wersja ma logo tekstowe.

Aby je zmienić wystarczy zamienić tekst logo w elemencie *a* w plikach
*default.html* oraz *index.html*

    <div id="logo" class="push-1 span-7">
      <a href="/blog/">MÓJ@BLOG</a>
    </div>

## Korzystamy z rozszerzeń

Jak? Opisane jest to w [jekyll_ext](http://github.com/rfelix/jekyll_ext).


## Gałąź *svg*
    
Zawiera wersję jBloga, która używa grafiki z logo.
Logo to wykonałem w programie *inkscape*. 

Plik *images/logo.svg* w formacie *SVG* zawiera 
nazwę mojego bloga *WB@jBlog*.

W pliku *SVG* literki składane są fontem *OTF*
[Cyklop](http://nowacki.strefa.pl/cyklop.html). Komputerową
wersję tego fontu przygotował Janusz M. Nowacki.


## Krótka instrukcja JTZ z zarządzania gałęziami

Zaczynamy od utworzenia gałęzi i przejścia na nią:

    git checkout -b nologo

Sprawdzamy, czy jesteśmy na nowej gałęzi:

    git branch
    master
    * nologo

Gwiazdka `*` przy *nologo* pokazuje, że tak.

Dodajemy do arkusza stylów font wykorzystany w pliku png z logo:

    @font-face {
      font-family: "Cyklop";
      src: url(fonts/Cyklop-Italic.otf) format("opentype");
      font-style: italic;
    }

Przegladarka skorzysta z tego fontu o ile obsługuje *web fonts*.

Po tych i kilku innych poprawkach w kodzie wykonujemy polecenie:

    git status

i jeśli wszystko jest OK, to:

    git add .
    git commit -m "gotowy kod z logo tekstowym"

Pozostaje tylko przesłać gałąź *nologo* na *github.com*:

    git push origin nologo

### Jak sklonować gałąź *nologo*

Od wersji 1.6.2 Gita klonujemy zdalną gałąź używając opcji *--track*
polecenia *git-checkout*:

    git checkout --track origin/nologo

Oto rezultat:

    git branch -a
      master
    * nologo
      remotes/origin/HEAD -> origin/master
      remotes/origin/master
      remotes/origin/nologo
