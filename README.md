# 🎥 Simple Stream Layouts

**Simple Stream Layouts** to przeglądarkowe narzędzie dla streamerów, mające na celu łatwo i szybko podzielić się swoimi kamerkami oraz równie szybko i wygodnie ustawić je na swoim streamie.

Główną zaletą mojego rozwiązania w porównaniu do wykorzystywanego przez większość streamerów dzielenia się pojedyńczymi linkami do obs ninja i wklejaniem każdego z nich z osobna do obsa jest to, że każdy z streamerów/użytkowników, który chce podzielić się swoją kamerką dołącza do jednego pokoju za pomocą tego samego linku, a po dołączeniu każdy z użytkowników ma możliwość niezależnego od innych ułożenia obrazów z kamer za pomocą 'interakcji' w obsie.

---

## 🚀 Jak zacząć? (Szybki Start)

1. Stwórz Pokój.
2. W pierwszej kolejności otwórz **Panel Reżysera** (Panel ten musi być otwarty cały czas).
3. Wyślij linki Gościom. Gdy wejdą na stronę i wybiorą sprzęt, automatycznie pojawią się w OBS i w panelu Reżysera.

### Niezależny podgląd dla ekipy (Tryb Lokalny)
Jeśli Twój współpracownik potrzebuje własnego układu kamer w OBS (ignorującego polecenia Reżysera), wystarczy, że do swojego linku OBS doda parametr `&local=1`. Po kliknięciu prawym przyciskiem myszy na źródło w OBS i wybraniu "Interakcja", zyska dostęp do lokalnego menu sterowania.

---

## 🛠 Technologie
* **HTML5 / CSS3** (CSS Grid, Flexbox, CSS Transforms)
* **Vanilla JavaScript** (ES6+)
* **WebRTC** (Natywne API dla Audio/Video)
* **PeerJS** (Warstwa sygnalizacyjna do zestawiania połączeń P2P)
* **STUN / TURN Servers** (Wsparcie dla trudnych sieci komórkowych/LTE poprzez projekt OpenRelay)

---

## ☕ Wsparcie i Twórcy

Projekt stworzony przez: **from xrawenq for Goodiez**

Jeśli to narzędzie ułatwiło Ci pracę i zaoszczędziło czas, rozważ wsparcie twórcy! Dziękuję za każdą kawę! ❤️

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=for-the-badge)](https://www.paypal.com/paypalme/rawen90)
