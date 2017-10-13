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
