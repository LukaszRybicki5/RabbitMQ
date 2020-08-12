Witam,

Aby sprawdzić działanie programu proponuje pobrać zawartość, wypakowac na pulpit foldery z paczki Folders_To_Desktop,
a następnie włączyć MessageReceiver i MessageSender.

Opis Zadania

Zadanie polega na stworzeniu aplikacji, która cyklicznie będzie odczytywała pliki CVS ze wskazanych, wielu, lokalizacji. Kolumny w plikach CSV nie są znane. Zakładamy, że pierwszy wiersz zawiera nagłówek – nazwę kolumny.

Dane z pliku CSV powinny zostać odczytane i poprawnie rozpoznane – liczby, booleany, itd. 

Każdy wiersz powinien zostać przekształcony na JSON i wysłany do RabbitMQ.
Nazwa pliku determinuje routing key po stronie RabbitMQ.

Program powinien być w maksymalnym stopniu konfigurowalny. Parametry które na pewno powinny się pojawić w pliku properties:
Lista katalogów które monitorujemy

Interwał co jaki monitorujemy
Filtr rozszerzeń (csv, tsv)
Separator jakim oddzielane są kolumny.
Parametry połączenia do RabbitMQ
Ilość wierszy z pliku na jedną wiadomość w RabbitMQ (batch size)-
