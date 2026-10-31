# MPK Studio — iOS PWA prototype

Aplikacja webowa instalowana na ekranie iPhone'a. Zawiera dotykową klawiaturę 25-klawiszową, 8 padów, lokalny syntezator Web Audio, prosty sekwencer 16 kroków i ekran mapowania kontrolerów MIDI.

## Uruchomienie
1. Rozpakuj ZIP na komputerze.
2. Uruchom lokalny serwer HTTPS (np. `npx serve .`; do testów localhost działa bez HTTPS).
3. Otwórz adres aplikacji w Safari na iPhonie.
4. W Safari wybierz Udostępnij → Do ekranu początkowego.

Możesz też opublikować zawartość katalogu na hostingu HTTPS. Po pierwszym uruchomieniu zasoby są cache'owane do pracy offline.

## Ważne ograniczenia prototypu
- To PWA, nie natywna aplikacja z App Store.
- Dźwięk generowany jest lokalnie przez Web Audio; nie ma jeszcze sampli ani pełnego silnika instrumentów.
- Web MIDI zależy od wsparcia przeglądarki iOS oraz dostępności urządzenia. Przycisk MIDI Connect wykrywa API, ale na iOS może być niedostępny. W takim przypadku aplikacja nadal działa jako instrument dotykowy.
- MIDI Editor konfiguruje mapowanie wysyłane przez tę aplikację; nie zapisuje presetów bezpośrednio do firmware AKAI.
- Arpeggiator jest na razie przełącznikiem interfejsu — pełna logika arpeggiatora jest kolejnym etapem.

## Bezpieczeństwo i prywatność
Brak konta, backendu i telemetrii. Konfiguracja jest zapisywana lokalnie w localStorage.
