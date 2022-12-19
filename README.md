# Smart Dom

## Instrukcja na Windows:
1. Pobierz Oracle VM VirtualBox i plik vdi z https://www.home-assistant.io/installation/windows/ 
2. Wykonaj krok *HYPERVISOR SPECIFIC CONFIGURATION* z instrukcji powyżej.
3. Po uruchomieniu VM załóż konto na HA.
4. Włącz Advanced Mode (ikonka użytkownika po lewej -> Advanced Mode).
5. Pobierz Add-ons (Settings -> Add-ons): File editor oraz Samba share.
6. Używając Samba share skopiuj pliki house.png oraz zawartość repo https://github.com/mk-maddin/dummy-HA:
6.1. house.png do przykładowo *\\\192.168.1.111\config\www\lovelace* (folder www/lovelace należało utworzyć)
6.2. folder dummy z repo do *\\\192.168.1.111\config\custom_components* (folder custom_components należało utworzyć)
6.3. zrestartuj system (Developer Tools -> Restart)
7. Przekopiuj zawartość configuration.yaml do /config/configuration.yaml w HA (File editor -> /config/configuration.yaml). Zapisz i w Developer Tools zrestartuj system.
8. Utwórz nowy dashboard (Settings -> Dashboards -> Add dashboard). Otwórz utworzony dashboard, kliknij trzy kropki u góry z prawej strony i wybierz Edit Dashboard, potem Start with an empty dashboard i Take control.
9. W nowym dashboardzie kliknij Add cart i wybierz Picture Elements. Do środka konfiguracji wklej zawartość pliku picture_element.yaml i zapisz.
10. W górnym menu dashboardu kliknij na ołówek obok nazwy zakładki (pewnie Home) i w View type wybierz Panel (1 card). Zapisz.
