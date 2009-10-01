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
git clone git://github.com/⟨twój login na <b>githubie</b>⟩/jblog.git sp
</pre>

gdzie nazwa katalogu *sp* to skrót od „Środowiska programisty”.


## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.markdown

na przykład:

    2009-06-12-jekyll-howto.markdown

Po napisaniu posta generujemy statyczną wersję bloga wykonując z
katalogu z blogiem, czyli z katalogu **~/public_git/sp/** polecenie:

    jekyll ~/public_html/sp

Po wykonaniu polecenia blog jest dostępny pod URI:

<pre>http://sigma.inf.ug.edu.pl/~⟨twój login na <b>sigmie</b>⟩/sp/
</pre>
