# 🎥 Simple Stream Layouts

**Simple Stream Layouts** to przeglądarkowe narzędzie dla streamerów, mające na celu łatwo i szybko podzielić się swoimi kamerkami oraz równie szybko i wygodnie ustawić je na swoim streamie.

Główną zaletą mojego rozwiązania w porównaniu do wykorzystywanego przez większość streamerów dzielenia się pojedyńczymi linkami do obs ninja i wklejaniem każdego z nich z osobna do obsa jest to, że każdy z streamerów/użytkowników, który chce podzielić się swoją kamerką dołącza do jednego pokoju za pomocą tego samego linku, a po dołączeniu każdy z nich ma możliwość niezależnego ułożenia obrazów z kamer za pomocą 'interakcji' w obsie.

---

## 🚀 Jak zacząć? (Szybki Start)

Narzędzie posiada dwa tryby pracy, które mogą pracować jednocześnie: Tryb Reżysera oraz Tryb niezależnego Obsa.

1. Tryb Reżysera.
W tym trybie to Reżyser steruje widokiem układu kamer widocznych w obsie.

2. Tryb niezależnego Obsa.
W tym trybie to każdy z uczestników steruje widokiem układu kamer widocznych w swoim obsie za pomocą 'interakcji'. W tym trybie domyślnie każdy z niezależnych obsów ma wyłączone wyświetlanie własnej kamerki, tak aby nie dublowała się z tą, którą już posiada na streamie i steruje kamerkami tylko pozostałych uczestników pokoju.

Uczestnik może wybrać do którego z trybów chce dołączyć po dołączeniu do pokoju.

### Dodatkowe informacje

Niezależny podgląd dla ekipy (Tryb Lokalny). Jeśli Twój współpracownik potrzebuje własnego układu kamer w OBS (ignorującego polecenia Reżysera), wystarczy, że do swojego linku OBS doda parametr `&local=1`. Po kliknięciu prawym przyciskiem myszy na źródło w OBS i wybraniu "Włącz interakcję", zyska dostęp do lokalnego menu sterowania.

Domyślnie w trybie niezależnego obsa Twoja kamerka jest wyłączona. Jeśli chcesz aby Twoja kamerka również była widoczna w widoku Twojego obsa lub chcesz usunąć z widoku Twojego obsa innych użytkowników, to możesz tego dokonać dokonując zmian w wklejonym linku w obsie i parametrze '&exclude=', albo go całkowicie usuwając, jeśli chcesz mieć kamerki wszystkich uczestników, albo dodając po przecinku, przykładowo exclude=Marek,Ania,Piotr innych uczestników pokoju.

---

## 🛠 Technologie
* **HTML5 / CSS3** (CSS Grid, Flexbox, CSS Transforms)
* **Vanilla JavaScript** (ES6+)
* **WebRTC** (Natywne API dla Audio/Video)
* **PeerJS** (Warstwa sygnalizacyjna do zestawiania połączeń P2P)

---

## ☕ Wsparcie i Twórcy

Projekt stworzony przez: **from xrawenq for Goodiez**

Jeśli to narzędzie ułatwiło Ci pracę i zaoszczędziło czas, rozważ wsparcie twórcy! Dziękuję za każdą kawę! ❤️

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=for-the-badge)](https://www.paypal.com/paypalme/rawen90)
