plik cat.c - backdoor
Za każdym razem, jak użytkownik wpisuje polecenie "cat /plik", backdoor zapisuje wyświetlony tekst w pliku /tmp/skradzony_cat.txt, który tworzy się samodzielnie, jeśli pliku nie ma.
Bit SUID umożliwia wyświetlenie zawartości plików, które mogą byc otwarte tylko z poziomu użytkownika root.
plik /tmp/skradzony_cat.txt można wysyłać prostym skryptem bash na przykład na server zdalny. Jesli użytkownik zobaczył zawartość jakiegoś systemowego pliku, na przykład /etc/shadow, zawartośc pliku będzie na pliku tekstowym, ktory będzie wysłany na serwer, dalej uzywając atak siłowy można odnaleźć jawne hasła i włamać się do systemu. Ale to jest poza zakresami naszego zadania :)
