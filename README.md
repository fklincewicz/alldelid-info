# AllDelid

## Opis i cel aplikacji

AllDelid jest wewnętrzną aplikacją firmy, używaną wyłącznie do obsługi własnego konta Allegro. Aplikacja pobiera polskie zamówienia klientów i przygotowuje na ich podstawie dokumenty ZK w Subiekcie GT.

## Zakres funkcjonalny

Aplikacja:

- pobiera zdarzenia oraz szczegóły zamówień Allegro,
- przetwarza zamówienia z adresem dostawy w Polsce,
- identyfikuje pozycje zamówienia na podstawie SKU,
- tworzy dokumenty ZK w Subiekcie GT,
- zabezpiecza przed ponownym utworzeniem tego samego dokumentu,
- może zmienić status realizacji zamówienia na PROCESSING.

Aplikacja nie zarządza ofertami Allegro i nie jest udostępniana innym sprzedawcom.

## Połączenie z Allegro

AllDelid korzysta z OAuth Device Authorization Flow. Użytkownik rozpoczyna połączenie w aplikacji, otwiera stronę autoryzacyjną Allegro i zatwierdza dostęp na swoim koncie. Redirect URL nie jest wykorzystywany.

## Wykorzystywane uprawnienia Allegro API

| Scope | Zastosowanie |
|---|---|
| `allegro:api:profile:read` | Identyfikacja konta połączonego z aplikacją |
| `allegro:api:orders:read` | Pobieranie zdarzeń, zamówień, danych dostawy i pozycji zamówienia |
| `allegro:api:orders:write` | Zmiana statusu realizacji zamówienia na PROCESSING |

## Bezpieczeństwo

Client Secret, access token i refresh token są przechowywane lokalnie i chronione mechanizmem Windows DPAPI. Dane robocze aplikacji są przechowywane lokalnie w bazie SQLite. Aplikacja nie przechowuje hasła użytkownika do Allegro.

## Kontakt

Adres e-mail: WPISZ_TUTAJ_FIRMOWY_EMAIL
