# 🎥 Simple Stream Layouts

> **Błyskawiczne studio P2P do streamingu grupowego. Jeden link dla wszystkich, zero konfiguracji, pełna kontrola nad sceną w OBS.**

[![WebRTC](https://img.shields.io/badge/WebRTC-P2P%20Mesh-38bdf8?style=for-the-badge&logo=webrtc&logoColor=white)](https://webrtc.org/)
[![JavaScript](https://img.shields.io/badge/Vanilla-JavaScript%20ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/)
[![PeerJS](https://img.shields.io/badge/Signaling-PeerJS-8b5cf6?style=for-the-badge)](https://peerjs.com/)
[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=for-the-badge)](https://www.paypal.com/paypalme/rawen90)

---

## 💡 Dlaczego Simple Stream Layouts?

Głównym problemem podczas wspólnych streamów (np. z gier wieloosobowych, podcastów czy talk-show) przy użyciu standardowych narzędzi (np. VDO.Ninja) jest konieczność generowania dziesiątek osobnych linków i mozolnego wklejania każdego źródła z osobna do OBS-a.

**Simple Stream Layouts rozwiązuje ten problem:**
* Wszyscy streamerzy i goście dołączają do **jednego wspólnego pokoju za pomocą jednego linku**.
* Do OBS-a wklejasz **tylko jedno źródło przeglądarki (1920x1080)**, które automatycznie układa wszystkie kamery.
* **Pełna niezależność:** Reżyser może centralnie sterować układem kamer ze swojego panelu **LUB** każdy ze streamerów może za pomocą funkcji *„Interakcja”* w swoim OBS-ie ułożyć kamery po swojemu, z automatycznie wyciętym własnym obrazem i dźwiękiem (**Mix-Minus**).

---

## ✨ Kluczowe Funkcje

### 🎬 1. Dwa Równoległe Tryby Pracy
* **Tryb Reżysera (`director.html`):** Realizator ma pełną kontrolę nad streamem – jednym kliknięciem przełącza gotowe sceny (*Siatka, Lewo, Prawo, Góra, Dół, Split, Center Stage*) lub dowolnie przestawia kamery na Wirtualnym Stole Montażowym.
* **Tryb Niezależnego OBS-a (`&local=1`):** Każdy streamer w ekipie może ignorować komendy Reżysera i w oknie interakcji OBS-a ułożyć kamery według własnych potrzeb (np. w boczny pasek obok okna gry).

### 🔓 2. Wirtualny Stół Montażowy (Free Mode)
* **Swobodne przesuwanie i skalowanie w czasie rzeczywistym:** Dowolne kadrowanie sceny bezpośrednio z poziomu Reżyserki lub okna interakcji OBS.
* **Magnetyczne przyciąganie (Snap & Guidelines):** Czerwone linie pomocnicze ułatwiające idealne wyrównanie krawędzi kafelków (klawisz `ALT` wyłącza przyciąganie).
* **Swobodny Crop:** Skalowanie narożnikiem z klawiszem `SHIFT` pozwala na dowolne przycinanie proporcji kadru.
* **Blokada układu (Layout Lock):** Zabezpieczenie stołu montażowego przed przypadkowym przesunięciem podczas transmisji.

### 📐 3. Inteligentna obsługa kamer 4:3 i 16:9
* Automatyczne wykrywanie formatu kamery gościa – brak ucinania kadru czy zniekształceń.
* **Przyciski szybkiego dopasowania (`↔ W` / `↕ H`):** Błyskawiczne zrównanie kafelka 4:3 z szerokością (320 px) lub wysokością (180 px) sąsiadujących kamer 16:9.

### 🔇 4. Inteligentny Mix-Minus (`&exclude=`)
* Domyślnie w podglądzie gościa/streamera jego własna kamera i mikrofon są **całkowicie ukrywane i wyciszane**, co eliminuje echo i zapobiega dublowaniu własnej kamery na streamie.
* Możliwość wykluczania wielu osób jednocześnie po przecinku (np. `&exclude=Marek,Ania,Piotr`).

### ⚡ 5. Wydajność i Ultra-Low Latency (ULL)
* **Topologia WebRTC Mesh:** Bezpośrednie połączenia P2P o minimalnym opóźnieniu.
* **Zerowy Jitter Buffer:** Wymuszenie zerowego buforowania (`playoutDelayHint = 0`) dla natychmiastowej synchronizacji audio/video.
* **Pętla Auto-Catchup:** Monitorowanie opóźnień w czasie rzeczywistym – jeśli pojawi się lag (>200 ms), OBS delikatnie przyspiesza odtwarzanie (1.05x), a przy dużym zacięciu (>2 s) wykonuje natychmiastowy bezszwowy refresh bufora.
* **Unlock Bitrate:** Opcja wymuszenia wysokiego bitrate'u (6 Mbps) z flagą `contentHint = 'motion'`.

### 🔄 6. Płynny Hot-Swap i Kadrowanie PTZ
* Gość może w dowolnym momencie transmisji zmienić kamerę, mikrofon lub format (16:9 / 4:3) **bez rozłączania i bez przeładowywania strony**.
* Suwaki kadrowania PTZ (Zoom cyfrowy, Poziom, Pion) po stronie gościa przesyłane na żywo do OBS-a.

### 🎮 7. Moduł Gier (Czółko / Heads-Up)
* Wbudowane narzędzie do teleturniejów i gier towarzyskich na żywo.
* Reżyser jednym kliknięciem losuje lub wpisuje hasła, które pojawiają się w OBS-ie w formie kart nad głowami graczy.
* **Anti-Cheat:** Gracz zgadujący ma w swoim podglądzie ukryte własne hasło!
* Tryb testowy: Skrót `Ctrl + Shift + F` dodający sztucznych uczestników (demo boty) do testowania scen.

### 🎨 8. Minimalistyczny Design *Dark Slate Studio*
* **Kinowe podpisy (Ambient Text Overlay):** Czysta, elegancka typografia z subtelną winietą cienia u dołu kadru – 100% czytelności na każdym tle bez zasłaniania obrazu.
* Płynne animacje i szklany interfejs (*Glassmorphism*).

---

## 🚀 Szybki Start (Krok po Kroku)

1. Otwórz stronę główną **`index.html`** i kliknij **`+ Utwórz Nowe Studio`**.
2. **Krok 1 (Reżyser):** Otwórz *Panel Reżysera* – to Twoje centrum dowodzenia realizacją.
3. **Krok 2 (Goście):** Skopiuj *Link dla Gości* i wyślij go znajomym. Goście wpisują swoje imię, ustawiają kadr i klikają *Dołącz*.
4. **Krok 3 (OBS i Podglądy):**
   * **Główny ekran transmisji:** Skopiuj *Źródło OBS / Ekran Gry* ze strony głównej i wklej w OBS Studio jako **Browser Source (1920x1080)**.
   * **Podglądy dla uczestników:** Po kliknięciu *„Dołącz do studia”* w panelu gościa automatycznie generują się gotowe, spersonalizowane przyciski kopiowania linku podglądu:
     * **Własny Podgląd (Niezależny):** link z automatycznym Mix-Minus (wycięta własna kamera i audio) oraz włączonym lokalnym menu sterowania w oknie interakcji.
     * **Podgląd Live Reżysera (Tryb gry):** link z podglądem na żywo całej sceny i automatycznie ukrytym własnym hasłem do gry (Anti-Cheat).

---

## ⚙️ Parametry URL (Kompendium)

Możesz ręcznie dostosować działanie każdego linku podglądu w OBS, dopisując poniższe parametry w adresie URL:

| Parametr | Zastosowanie | Przykład |
| :--- | :--- | :--- |
| `room` | Unikalny identyfikator pokoju / studia | `?room=goodiez7` |
| `local=1` | **Tryb Niezależnego OBS-a:** Ignoruje realizację Reżysera i włącza lokalne menu sterowania w oknie interakcji OBS | `&local=1` |
| `exclude` | **Mix-Minus:** Całkowicie ukrywa i wycisza podane osoby (oddzielone przecinkami) | `&exclude=Marek,Ania` |

---

## 🛠️ Technologie

* **Frontend:** HTML5, CSS3 (CSS Grid, Flexbox, Custom Transforms, Glassmorphism)
* **Język:** Vanilla JavaScript (ES6+, bez zewnętrznych frameworków)
* **Transmisja Audio/Video:** WebRTC (RTCPeerConnection, MediaStream API)
* **Sygnalizacja P2P:** PeerJS (DataChannels, Mesh Orchestration)

---

## ☕ Wsparcie i Twórcy

Projekt stworzony przez: **from xrawenq for Goodiez**

Jeśli to narzędzie ułatwiło Ci organizację streamów, rozwiązało problem z konfiguracją wielu kamer i zaoszczędziło Twój czas, rozważ wsparcie projektu! Dziękuję za każdą postawioną kawę! ❤️

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=for-the-badge)](https://www.paypal.com/paypalme/rawen90)
