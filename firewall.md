**Firewall**

- Filtrowanie po źródłowym i docelowym IP, protokole IP, źródłowym i docelowym porcie dla ruchu TCP i UDP
- Limitowanie jednoczesnych połączeń
- Wykrywanie systemów operacyjnych z użyciem p0f (advanced passive OS fingerprinting) w celach filtracji ruchu
- Możliwość logowania (lub nie) ruchu odpowiadającego każdej z reguł
- Elastyczna polityka routingu możliwa przez wybór bramy dla reguły (load balancing, redundancja, multi WAN i inne)
- Aliasy pozwalające na zgrupowanie adresów IP, sieci i portów – bardzo ułatwia i porządkuje pracę administratorów
- Przezroczysty firewall warstwy drugiej – mostkowanie interfejsów i filtrowanie ruchu między nimi, nawet bez wykorzystywania IP
- Scrubbing – „normalizacja&quot; pakietów, pozwala na składanie pofragmentowanych pakietów w locie, zabezpieczając niektóre systemy operacyjne przed różnymi formami ataków, odrzuca pakiety TCP z nieprawidłową kombinacją flag
  - domyślnie włączone w pfSense
  - istnieje możliwość wyłączenia w razie potrzeby – funkcjonalność może powodować problemy z niektórymi połączeniami NFS
- Wyłączenie filtrowania – możliwość wyłączenia firewalla w pełni, kiedy tylko tego potrzebujesz'
![](http://net-masters.pl/wp-content/uploads/2015/12/pfSense-WAN-Rules-01.png)
***Tablica stanów***

Większość firewalli nie posiada lub ma bardzo ubogą możliwość kontroli tablicy stanów. pfSense ma wiele udogodnień umożliwiających drobnostkową kontrolę tablicy stanów – jest to zasługa systemu FreeBSD, na której bazuje pfSense.

- Regulowany rozmiar tablicy stanów – domyślny rozmiar tablicy dobierany jest automatycznie proporcjonalnie do wielkości pamięci RAM zainstalowanej w systemie, jednak może zostać zwiększona w locie do wybranego rozmiaru. Każdy stan zajmuje około 1KB w pamięci RAM.
- Podstawy do tworzenia reguł:
  - limitowanie jednoczesnych połączeń
  - limitowanie stanów per host
  - limitowanie nowych połączeń na sekundę
  - definiowanie czasu trwania stanu
  - definiowanie rodzaju stanu
- Rodzaje stanów – pfSense oferuje wiele opcji dla obsługi stanów:
  - Keep state – działa z wszystkimi protokołami. Domyślne dla wszystkich reguł
  - Sloppy state – działa z wszystkimi protokołami. Mniej restrykcyjny, użyteczny przy asymetrycznym routingu
  - Synproxy state – działa jako proxy dla przychodzących połączeń TCP, chroniąc serwery przed podsłuchami TCP SYN
  - None – nie przetrzymuje żadnych stanów dla ruchu sieciowego
- Optymalizacja tablicy stanów – pfSense oferuje 4 opcje dla optymalizacji:
  - Normal – domyślny algorytm
gh latency – pomocne dla łączy z dużym opóźnieniem, jak np. łącza satelitarne – wydłuża czas trwania połączeń
Aggressive – zakańcza połączenia znacznie szybciej, efektywniej używa zasoby, jednak może wystąpić odrzucanie spodziewanych połączeń
Conservative – stara się zapobiegać odrzucaniu spodziewanych połączeń kosztem zwiększonego zużycia CPU i pamięci RAM
