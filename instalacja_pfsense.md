**Instalacja** może zostać przeprowadzona np. w następujące sposoby:

1. Z live CD with Installer
  - Wykorzystać do instalacji  **Live CD with Installer** , które może zostać pobrane ze strony pfSense -  [pfSense Download Mirrors](https://www.pfsense.org/download/mirror.php?section=downloads#mirrors)
  - Pobrany plik iso ma zostać nagrany na płytę CD i z niej uruchomiony system.
2. Z live CD with Installer na kluczu USB
  - Wykorzystać do instalacji **Live CD with Installer (on USB Memstick)**, które może zostać pobrane ze strony pfSense. Jako &quot;console&quot; wybrać  **VGA**  -  [pfSense Download Mirrors](https://www.pfsense.org/download/mirror.php?section=downloads#mirrors)
  - Zapisać na pendrive plik iso i uruchomić z nim system. 

**Procedura Instalacji:**

- Po wciśnięciu klawisza _Enter_ rozpoczyna się instalacja w trybie Default Multi-User.

 ![](https://pp.userapi.com/c639429/v639429722/4b917/5Wu3v0hoehg.jpg)

- Konfiguracja konsoli, wykorzystywane są ustawienia domyślne.

 ![](https://pp.userapi.com/c639620/v639620722/59388/9ehCvnvB_Kk.jpg)

- Dla początkujących użytkowników zalecana jest opcja &quot;Quick/Easy Install&quot;.

 ![](https://pp.userapi.com/c639620/v639620722/59398/tW7UW9k83oI.jpg)

- Wyświetlane jest ostrzeżenie. że dysk zostanie sformatowany. Przez co dane na dysku ulegną utracie.

 ![](https://pp.userapi.com/c639620/v639620722/593a0/CS-bvuYxkcY.jpg)

- W razie potrzeby może zostać dostosowana konfiguracja jądra.

 ![](https://pp.userapi.com/c639620/v639620722/593a8/NFYd9_Sbzl8.jpg)

- Po skopiowaniu danych system jest restartowany, po czym przeprowadzana jest konfiguracja interfejsów.

 ![](https://pp.userapi.com/c639620/v639620529/4ee9b/raYIxCt7ODs.jpg)

- Konfiguracja VLAN-ów.

 ![](https://pp.userapi.com/c639620/v639620529/4eea3/fNRJv_bD9GQ.jpg)
 
- Wybór karty sieciowej dla interfejsu WAN.

 ![](https://pp.userapi.com/c639620/v639620529/4eeab/LhJ04UpTINY.jpg)

- W tym przykładzie igb1 jest deklarowany jako interfejs WAN.

 ![](https://pp.userapi.com/c639620/v639620529/4eeb3/g7UIQbdH8_c.jpg)
 
- Wybór karty sieciowej interfejsu LAN. W tym przykładzie deklarowana jest karta sieciowa igb0.

 ![](https://pp.userapi.com/c639620/v639620529/4eebb/x8JkWsjhCXE.jpg)

- Zatwierdzenie konfiguracji interfejsów WAN i LAN.

 ![](https://pp.userapi.com/c639620/v639620529/4eec3/yYYJyx5xwjs.jpg)
 
- Shell pfSense oferuje kilka opcji konfiguracyjnych.

 ![](https://pp.userapi.com/c639620/v639620529/4eecb/iZKaUztAWI4.jpg)
 
- Kreator jest pomocny w konfiguracji najważniejszych ustawień.

 ![](https://pp.userapi.com/c639620/v639620529/4eed3/pp3jYqLou8c.jpg)

- Tutaj podawana jest nazwa hosta, domena i serwer DNS.

 ![](https://pp.userapi.com/c639620/v639620529/4eedc/hqdJo569hf4.jpg)
 
- W razie potrzeby może zostać zmieniony serwer czasu.

 ![](https://pp.userapi.com/c639620/v639620529/4eee5/3ECJ2D2F3-A.jpg)
 
- Maska konfiguracyjna interfejsu WAN.

 ![](https://pp.userapi.com/c639620/v639620529/4eef6/w1Q8I3hbJtc.jpg)
 
- Najlepiej, aby zaraz zmienić domyślne hasło.

 ![](https://pp.userapi.com/c639620/v639620529/4eeff/72tEr-4meVw.jpg)

- Kreator jest zakończony.

 ![](https://pp.userapi.com/c639620/v639620529/4ef08/0v2jrFmoyQ4.jpg)

- Dashboard udostępnia dobry przegląd aktualnego stanu.

 ![](https://pp.userapi.com/c639620/v639620529/4ef11/YVLpUDc_2SU.jpg)
 
**Informacja jest pobrana ze strony internetowej: https://www.thomas-krenn.com/pl/wiki/Instalacja_firewalla_open_source_pfSense**
