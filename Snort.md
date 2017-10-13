**Snort** jest znanym open source IDS/IPS, który jest zintegrowany z kilkoma dystrybucjami zapory IPfire np., Endian i PfSense. W tym samouczku, naszym celem jest instalacja, Konfiguracja Snorta i zasady na PfSense firewall. Snort potrzebuje zapory filtr (pf) pakietów, które oferują IPS, który jest również dostępny w tej dystrybucji.
 Wszystkie oprogramowanie Pfsense firewall są dostępne w podmenu pakiety . Przejdź do System menu i wybierz pakiety z rozwijanego menu listy.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/packages1.png)
 Kliknij zakładkę dostępne pakiety dla różnych kategorii oprogramowania.
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/availablepackage.png)
 Dostępne pakiety pokazuje następujące sub menu Opcje. Snort jest narzędziem zabezpieczeń open source, w związku z tym kliknij menu zabezpieczeń do listy dół dostępne pakiety instalacyjne na PfSense.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/availablepackage-options.png)
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/icon-snort.png?resize=513%2C150)
 Instalacja nowego pakietu na Pfsense , wymaga potwierdzenia od administratora zapory, który znajduje się poniżej.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/confirm.png)
 Instalacja Snorta
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-installation-1.png)
 **Konfiguracja Snorta**
 Po udanej informacje programu snort na Pfsense, Teraz musimy skonfigurować Snorta na interfejsie LAN do portu skanowania wykrywania. Snort jest dostępna w menu usługi po instalacji.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-in-services-menu.png)
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/services-all-menu.png)
 Snort, albo działać na interfejs sieci LAN lub WAN PFSense. W związku z tym musimy stworzyć sieci lan i wan interfejsów
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-interfac-setting.png)
 Poniżej przedstawiono ustawienia interfejsu LAN. Mamy zaznaczone opcje IPS jak blok przestępców i zabić ich Państwa
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-interface-setting-lan.png)
 Interfejs dodany dla sieci LAN i obecnie, że snort nie działa na nim. Kliknij na krzyż (X) przycisk, aby rozpocząć Snort ids usługi na interfejsie LAN.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-interface-added.png)
 Jak pokazano w następujących snort migawka jest uruchomiony na interfejsie LAN.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-interface-running.png)
 Poniższy ekran pojawia się po kliknięciu na ustawienia menu dla instalacji reguły snort globalne.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-rules-under-global-setting.png)
 Zaloguj się na stronie internetowej snort i generuje Onikcode do pobrania “Snort VRT” zasady.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/oinkcode.png)
 Kliknij na Oinkcode po lewej stronie, aby uzyskać Oinkcode.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/oinkcode-code.png)
 Ponownie przejdź do menu Ustawienia globalne i wpisz Oinkcode aby pobrać reguły Snort VRT.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/enter-oinkcode-on-snort-setting.png)
 Teraz przejdź do menu aktualizacji, aby sprawdzić stan różnych reguł. Kliknij przycisk Aktualizacja, aby pobrać lub zaktualizować reguły snort na Pfsense.
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/updates-menu.png)
 Kliknij przycisk Aktualizuj, aby zainstalować zasady na Snorta. Reguły aktualizacji krok pokazywany jest w poniżej rysunek. Mamy zainstalowane snort Wspólnoty, VRT, pojawiających się zagrożeń zasady.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/updates-rules.png)
 Przed przejściem do następnego menu programu snort, ponownie kliknij na karcie interfejsy Snort i wybierz LAN do edycji.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/lan-interface.png)
 Po kliknięciu na przycisk Edytuj, Wybierz opcję Kategorie LAN dla reguły snort. Wybierz pożądane reguły z tej kompleksowej listy dla interfejsu sieci LAN.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/snort-rules.png)
 Po instalacji reguły snort na Pfsense, Następna opcja jest menu alerty
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/alerts.png)
 Snort z packet filter (filtr) daje możliwość blokowania złośliwego IP. Zablokowany IP pojawi się na poniższych zrzutach ekranu.
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/blocked.png)
 Jest to bardzo często w sieci administrator zapewnia białe listy IP. Domyślnie lokalne sieci LAN jest zwykle na liście przechodzą.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/pass-list.png)
 Pomiń menu jest wyświetlany w następujących migawka. Umożliwia blokowanie fałszywych alarmów.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/suppress.png)
 Lista adresów ip złośliwe mogą być ładowane na Pfsense w konfiguracja Snorta. Ruch przychodzący z adresów ip, przechowywane w na liście zostaną uznane za szkodliwe.
 ![](https://i2.wp.com/websetnet.com/wp-content/uploads/2015/12/ip-list1.png)
 Ustawienie dla podpisów identyfikatora (SID) z reguły snort jest zarządzany przy użyciu tego menu.
 ![](https://i0.wp.com/websetnet.com/wp-content/uploads/2015/12/sid-mgmt.png)
 Ustawienie odpowiednich logowania zarządzania są wyświetlane w menu.
 ![](https://i1.wp.com/websetnet.com/wp-content/uploads/2015/12/log-management1.png)
 
 
 
 
 
 
