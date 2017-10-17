### Instalacja PFsense ###
Instalacja PFsense na wirtualną maszynę, w którą pakiety z sieci internet będą wchodzić najpierw, a późnej już na fizyczny komputer, wtedy można wykorzystać wszystkie możliwości Pfsense.

- Najpierw mamy ściągnąć plik dla instalacji ze strony internetowej: https://www.pfsense.org/download/
![](https://pp.userapi.com/c639222/v639222640/4e6e7/loBfxpjMBJg.jpg)

- Mamy wyciągąć plik "iso" z archiwu "gz"

- Konfiguracja maszyny wirtualnej:
![](https://pp.userapi.com/c840222/v840222640/34a54/OhWc1eNUPzc.jpg)
![](https://pp.userapi.com/c637324/v637324640/50f87/cPCSuDbz3TM.jpg)
![](https://pp.userapi.com/c637324/v637324640/50f91/XBvQ8ECPRJU.jpg)
![](https://pp.userapi.com/c637324/v637324640/50f9b/MPz5ZhtFJNM.jpg)

- Konfiguracja sieci w wirtualnej maszynie

![](https://pp.userapi.com/c637324/v637324640/50fae/0x-l2OToWRM.jpg)
![](https://pp.userapi.com/c637324/v637324640/50fb8/E76TN4I-3mk.jpg)

- Konfiguracja sieci w systemie Windows(nie będzie dostępu od internetu do konca konfiguracji)
 
  - Wyłaczamy wszystko opróc VirtualBox driver(dla fizycznego) 
 
  ![](https://pp.userapi.com/c637324/v637324640/50fd3/vbvizjL2a7k.jpg)
 
  - Włączamy wszystko i konfigurujemy ipv4 w taki sposób
 
  ![](https://pp.userapi.com/c637324/v637324640/50fe5/cpeFYKuDFWY.jpg)
  ![](https://pp.userapi.com/c637324/v637324640/50fee/e8dY6WHVSl4.jpg)

- Teraz można urochomić wirtualną maszyne i dalej pójdzie instalacja PFsense. Po instalacji maszyna będzie zresetowana, i wtedy mamy wyćiągnąć dysk z wirtualnego napędu.

![](https://pp.userapi.com/c637324/v637324422/4fcac/pyW3BeLKN8w.jpg)
![](https://pp.userapi.com/c637324/v637324422/4fcbe/0PaQkDnTXus.jpg)

- Po właczeniu maszyny mamy skonfigurować interface LAN (jest pod numerem 2). Ip: 192.168.56.2, przez maskę /24.

![](https://pp.userapi.com/c637324/v637324422/4fd67/-zPcVK2GOZY.jpg)

- Teraz można wejść przez przegłądarkę internetową na adres https://192.168.56.2/ i zobaczyć webowy interfejs PFsense. Login: admin, Hasło: PFsense

![](https://pp.userapi.com/c637324/v637324422/4fd6f/q-NUFIC54Jo.jpg)

- Można wprowadzić DNS server

![](https://pp.userapi.com/c637324/v637324422/4fd77/1OW_LYJaYUw.jpg)

- Tutaj mamy wybrać adres statyczny lub dynamiczny, ja mam dynamiczny dla tego wybieram DHCP

![](https://pp.userapi.com/c637324/v637324422/4fd7f/zv45sZwr1w8.jpg)

- Konfiguracja lan

![](https://pp.userapi.com/c637324/v637324422/4fdb4/TLKeiLtdh1Y.jpg)

- Teraz jest można zmienić hasło

![](https://pp.userapi.com/c637324/v637324422/4fdbc/cv1kC6DMapc.jpg)

- Instalacja jest zakończona 

![](https://pp.userapi.com/c637324/v637324422/4fdc4/R5N5Q8NgsX8.jpg)

### Podstawowa konfiguracja firewallu PFsense ###
Na początku są wyłączone wszytkie porty i wszystkie protokoły sieci internet.
- Włączamy http i port 80

![](https://pp.userapi.com/c841638/v841638139/2839c/PMw4cMRGO1Q.jpg)

- Włączamy https i port 443

![](https://pp.userapi.com/c841638/v841638139/283a6/Qm6U6083aas.jpg)

- Włączamy DNS i port 53

![](https://pp.userapi.com/c841638/v841638139/283b0/6adKZHW0g0k.jpg)

Tak wygłąda tabela firewalla 

![](https://pp.userapi.com/c841638/v841638139/28366/ePq7JWgHaxs.jpg)
