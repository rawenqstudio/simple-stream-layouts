# 🎥 Simple Stream Layouts

**Simple Stream Layouts** to przeglądarkowe narzędzie dla streamerów, mające na celu łatwo i szybko podzielić się swoimi kamerkami oraz równie łatwo i szybko ustawić je na swoim streamie.

---

## ✨ Główne Funkcje

* 🚀 **Ultra Low Latency (ULL):** Tryb wyłączający wygładzanie ruchu (Jitter Buffer) w przeglądarce, pozwalający osiągnąć opóźnienia rzędu 50-100 ms (Glass-to-Glass). Dodatkowo wbudowany mechanizm **Auto-Catchup** automatycznie niweluje mikro-opóźnienia.
* 👥 **Architektura Multi-Viewer:** Główny panel Reżysera działa jako serwer sygnałowy. Pozwala to na podłączenie wielu niezależnych odbiorników (np. główny OBS, podgląd dla grafika, podgląd dla tłumacza).
* 🎛️ **Wirtualny Stół Montażowy (Free Mode):** Swobodne zarządzanie układem kamer w czasie rzeczywistym. 
  * Przeciągaj i upuszczaj (Drag & Drop) kamery w przestrzeni 16:9.
  * Zmieniaj rozmiar zachowując proporcje lub przycinaj (Crop) przy użyciu klawisza `SHIFT`.
  * Magnetyzm (Snapping) do krawędzi innych okien ułatwia perfekcyjne ułożenie.
* 📐 **Inteligentne Układy (Presets):** Gotowe ułożenia kamer: Pełna Siatka (Auto-Grid skalujący się od 1 do 12 gości), Paski boczne/górne, Split (rozdzielenie na boki) oraz profesjonalny układ **Center Stage** (jeden główny mówca na środku, reszta po bokach).
* 🎮 **Zintegrowany Moduł Gier:** Wbudowana gra "Czółko" (Heads Up). Reżyser rozdaje hasła, które jako nakładki (overlays) przyklejają się w OBS bezpośrednio do kamer gości. System automatycznie ukrywa hasło przed zgadującym.
* 🎥 **Zdalne PTZ (Pan-Tilt-Zoom):** Goście mogą wykadrować swój obraz (zbliżenie, przesunięcie lewo/prawo/góra/dół) na swoich urządzeniach, a matematyka CSS bezstratnie przeliczy i zaaplikuje ten kadr bezpośrednio w OBS.
* 📊 **Monitorowanie Jakości (Health Stats):** Reżyser widzi w czasie rzeczywistym bitrate, packet loss i rozdzielczość każdego gościa.
* 🎚️ **Zarządzanie Audio:** Rozdzielony sygnał A/V (omijający opóźnienia miksera OBS) oraz zdalne wyciszanie mikrofonów gości z panelu Reżysera.

---

## 🚀 Jak zacząć? (Szybki Start)

1. Wrzuć pliki na dowolny hosting obsługujący HTTPS (np. **GitHub Pages**).
2. Otwórz `index.html` i kliknij **+ Utwórz Studio**.
3. Otwórz **Panel Reżysera** (`director.html`) – *musi być otwarty przez cały czas trwania transmisji!*
4. Skopiuj Link do OBS i wklej go jako **Źródło Przeglądarki w swoim OBS Studio**. Pamiętaj o odznaczeniu opcji "Kontroluj dźwięk przez OBS" dla zachowania zerowego opóźnienia.
5. Wyślij linki Gościom. Gdy wejdą na stronę i wybiorą sprzęt, automatycznie pojawią się w OBS i w panelu Reżysera.

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

Jeśli to narzędzie ułatwiło Ci produkcję i zaoszczędziło czas (oraz pieniądze na komercyjnych rozwiązaniach), rozważ wsparcie twórcy! Dziękuję za każdą kawę! ❤️

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=for-the-badge)](https://www.paypal.com/paypalme/rawen90)
