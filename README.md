# Smart Dom

## Instrukcja na Windows:
1. Pobierz Oracle VM VirtualBox i plik vdi z https://www.home-assistant.io/installation/windows/ 
2. Wykonaj krok *HYPERVISOR SPECIFIC CONFIGURATION* z instrukcji powyżej.
3. Po uruchomieniu VM załóż konto na HA ( http://homeassistant.local:8123 )
4. Włącz Advanced Mode (ikonka użytkownika po lewej -> Advanced Mode).
5. Pobierz i uruchom Add-ons (Settings -> Add-ons -> Add-on store): File editor (+ Show in sidebar) oraz Samba share (+ username i password w Configuration).
6. Pobierz repo https://github.com/iantrich/config-template-card i zbuduj plik js (npm install --force && npm run build).
7. Używając Samba share skopiuj pliki house.png itd. oraz zawartość repo https://github.com/mk-maddin/dummy-HA i zbudowany plik config-template-card.js:
 - zgodnie z dokumentacją wejdź w *\\\192.168.1.111* (url wzięty z okna powitalnego po uruchomeniu HA System information -> IPv4) w File Explorer i zaloguj się używając danych z Configuration
 - house.png i inne obrazki do przykładowo *\\\192.168.1.111\config\www\lovelace* (folder www/lovelace należało utworzyć) 
 - folder dummy z repo do *\\\192.168.1.111\config\custom_components* (folder custom_components należało utworzyć)
 - config-template-card.js do *\\\192.168.1.111\config*
 - zrestartuj system (Developer Tools -> Restart)
8. Przekopiuj zawartość configuration.yaml do /config/configuration.yaml w HA (File editor -> /config/configuration.yaml). Zapisz i w Developer Tools zrestartuj system.
9. Utwórz nowy dashboard (Settings -> Dashboards -> Add dashboard). Otwórz utworzony dashboard, kliknij trzy kropki u góry z prawej strony i wybierz Edit Dashboard, potem Start with an empty dashboard i Take control.
10. W nowym dashboardzie kliknij trzy kropki u góry z prawej strony i wybierz Edit Dashboard. Ponownie kliknij w krzy kropki u góry z prawej strony i Manage resources  -> Add resource -> url: /local/config-template-card.js -> Create.
12. W nowym dashboardzie kliknij Add cart i wybierz Picture Elements. Do środka konfiguracji wklej zawartość pliku picture_element.yaml i zapisz.
13. W górnym menu dashboardu kliknij na ołówek obok nazwy zakładki (pewnie Home) i w View type wybierz Panel (1 card). Zapisz.
