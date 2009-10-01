# Szablon jekyll-bloga 

Dostosowany do konfiguracji serwera *Sigma* szablon bloga.
Statyczne strony bloga generujemy za pomocą programu *jekyll*.


## Instalacja

Klikamy w ikonkę **fork** i natępnie klonujemy sforkowanego bloga
na swoje konto na serwerze *Sigma*:

<pre>git clone git://github.com/⟨twój login na <b>githubie</b>⟩/jblog.git ⟨nazwa wykładu⟩
</pre>

Na przykład, dla wykładu „Środowisko programisty” ⟨nazwa wykładu⟩ to `sp`.


## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.markdown

na przykład:

    2009-06-12-jekyll-howto.markdown

Po napisaniu posta generujemy statyczną wersję bloga wykonując z
katalogu z blogiem, takie polecenie:

    jekyll ~/public_html/sp

Po wykonaniu polecenia blog jest dostępny pod URI:

<pre>http://sigma.inf.ug.edu.pl/~⟨twój login na <b>sigmie</b>⟩/sp/
</pre>
