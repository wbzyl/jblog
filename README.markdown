# Szablon jekyll-ibloga 

Dostosowany do konfiguracji serwera *Sigma* szablon bloga.
Statyczne strony bloga generujemy za pomocą programu *jekyll*.

## Instalacja

Klikamy w ikonkę **fork** i natępnie klonujemy sforkowanego bloga
na swoje konto na serwerze *Sigma*:

<pre>git clone git://github.com/<i>twój login na <b>githubie</b></i>/iblog.git <i>nazwa wykładu</i>
</pre>

Na przykład, dla wykładu „Środowisko programisty” polecenie może wyglądać tak:

    git clone git://github.com/wbzyl/iblog.git sp

## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_post`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.markdown

na przykład:

    2009-06-12-jekyll-howto.markdown

Po napisaniu posta generujemy statyczną wersję bloga wykonując z
katalogu z blogiem, na przykład, takie polecenie:

    jekyll ~/public_html/sp

Po wykonaniu polecenia blog jest dostępny pod URI:

<pre>http://sigma.inf.ug.edu.pl/~<i>twój login na <b>sigmie</b></i>/sp/
</pre>
