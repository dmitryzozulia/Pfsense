![](https://habrastorage.org/getpro/habr/post_images/1f8/03c/f40/1f803cf40067b629be332b8c8d09fba2.png)
# Pfsense
Instalacja, instrukcja, konfiguracja podstawowa
**PfSense**
PfSense to system operacyjny, który powstał na bazie FreeBSD. W kontekście pełnienia ról sieciowych jest to ogromna zaleta – zarówno FreeBSD, jak i inne systemy z rodziny BSD są bowiem rozwijane właśnie z myślą o usługach sieciowych. Szczególny nacisk położono na stabilność działania oraz bezpieczeństwo. Dobrze skonfigurowany system będzie działał bez problemów przez długie lata, a ewentualne przestoje najczęściej będą wynikać z problemów sprzętowych.Trzeba przyznać, że twórcy pfSense bardzo celnie wybrali fundament dla swoich dalszych prac.

Użyte w nazwie systemu litery „pf&quot; zdradzają użycie oprogramowanie Packet Filter – znanego z OpenBSD narzędzia do filtrowania ruchu i realizowania funkcji NAT oraz QoS. To nie jest jedyny mechanizm zaczerpnięty z OpenBSD. Kolejny to protokół CARP (Common Address Redundancy Protocol) służący do budowania rozwiązań sieciowych odpornych na awarie sprzętowe. Za pomocą tego protokołu można połączyć ze sobą dwa firewalle lub więcej. Gdy urządzenie aktywne ulegnie awarii, drugi firewall przejmie jego funkcje, zachowując jednocześnie identyczną konfigurację, jaką wcześniej miał aktywny firewall (tę bardzo ciekawą funkcję opiszemy szerzej w dalszej części artykułu). Wśród pakietów dostępnych do instalacji znajduje się też całe mnóstwo narzędzi realizujących funkcje sieciowe i diagnostyczne, a wywodzących się z OpenBSD.

Podobnie jak wiele innych systemów operacyjnych przeznaczonych do serwowania usług sieciowych pfSense ma graficzny interfejs użytkownika. Wykorzystywany jest on do konfiguracji poszczególnych usług sieciowych, monitoringu, nadzorowania stanu pracy serwera oraz szybkiego instalowania nowych funkcji. Niemal wszystkie czynności można wykonać bez konieczności wpisywania komend powłoki systemowej, choć ta jest dostępna i oferuje nieco większe możliwości.

**&gt; PODSTAWOWE FUNKCJE PFSENSE**

Jedną z funkcji, jaką może pełnić pfSense, jest firewall. Filtrowanie ruchu sieciowego odbywa się z wykorzystaniem reguł oraz przy użyciu dodatkowych, często ciekawych, mechanizmów. Należy do nich m.in. p0f – narzędzie wykorzystywane przez pfSense do rozpoznawania systemu operacyjnego urządzenia generującego w danej chwili ruch sieciowy.

### [Instalacja PFsense](instalacja_pfsense.md)
### [Firewall](firewall.md)
