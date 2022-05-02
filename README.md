# ☕ VAVA-JAVA
* Vývoj Aplikácií s Viacvrstvovou Architektúrou (VAVA) 
* Slovenská technická univerzita v Bratislave Fakulta Informatiky a Informačných Technológií STU FIIT 2022
* Prednášajúci: PhDr. Ing. Mgr. et Mgr. et Mgr. et Mgr. Miroslav Reiter, DiS., MBA, MPA, MSC, DBA, Ing. Paed. IGIP
* Kontakt: riaditel@it-academy.sk
* Komunikácia: Skype
* Verzia Javy/JDK: Java SE JDK 11
* Preferované IDE: Netbeans 12 (alebo podľa preferencií Eclipse/IntelliJ IDEA)

## Organizácia predmetu
**Prednášky**: Každý štvrtok 18:00-19:40  
**Cvičenia**: Každý utorok **formou konzultácii**
1. skupina od 17:00
2. skupina od 19:00

Osobitné **konzultácie**: **Piatok 13:00-14:00**

## 🔥 Sylabus/Čo nás čaká a neminie...
1. Úvod do Javy
1. Štruktúra platformy
1. Vývojové technológie
1. Kolekcie
1. Logovanie
1. Lokalizácia
1. XML, NIO2
1. Regulárne výrazy
1. Modularita
1. JDBC
1. Bezpečnosť
1. Prehľad JEE a .NET

## 👨‍🏫 Výsledky vzdelávania
* Získať prehľad o platforme Java (Java Standard Edition), jej architektúre, štruktúre a vlastnostiach
* Zdokonaliť sa vo vývoji programov pre platformu Java (Java Standard Edition)
* Naučiť sa tvoriť desktopové GUI aplikácie vo SWING/JavaFX
* Nadobudnúť zručnosti vo využívaní vybraných rozhraní a rozširujúcich knižníc platformy Java (Standard Edition)
* Pripraviť sa na neskorší vývoj rozsiahlych viacvrstvových enterprise aplikácií
* Zasadenie Java v kontexte JEE a .NET technológií

## Stručná osnova predmetu:
1. Štruktúra platformy Java
2. Java vývojové technológie a štandardy
3. Vybrané kapitoly/detaily Java Standard Edition API (napr. Collections, Logging, Localization, XML, I/O, Regular Expressions)
4. Modularita, JDBC, Bezpečnosť
5. Prehľad JEE a .NET technológií

## ☕ YouTube video záznamy z prednášok a cvičení Playlist
[YouTube kanál IT Academy](https://www.youtube.com/watch?v=0aV5g2rQCl8&list=PLIu_ZdHo7Pk8VkVfUW06vbZGtzxF9GR24)

## 🥇 Podmienky na absolvovanie predmetu
* **70 %** formou **tímovej práce** v podobe **projektu**, implementácie a jednoduchej dokumentácie prototypu postaveného na vybraných technológiách JAVA a JEE 
* **30 % skúška** podobná **oficiálnej Oracle Java certifikačnej skúške OCP (Oracle Certified Professional) Java SE 11 Developer 1Z0-819**, alebo absolvovanie **oficiálnej** **certifikačnej skúšky OCP 1Z0-819**: https://education.oracle.com/oracle-certified-professional-java-se-11-developer/trackp_OCPJAV11

## 🔥 Hodnotenia, tímový projekt
### Vlastný projekt (do 11. cvičenia) – 70 bodov
Vytvoríte **tímy o 5 členoch**  
V tíme je **1 vedúci**, každá skupina si ho demokraticky zvolí alebo sa sám diktátorsky zvolí  

A. **Projektový zámer** a predstavenie tímu s rozdelením úloh a rôl (**RACI matica**) – 10 bodov – (do 5. cvičenia)  
B. **Program**, **video prezentácia** a **dokumentácia vrátane UML, EA diagramov** – 60 bodov – (do 11. cvičenia)

✔️ **Odovzdávané UML diagramy** (core funkcionalita a triedy v projekte) v dokumentácii:
1. prípadov použitia (use case)
2. aktivít (activity)
3. tried (class)
4. balíčkov (package)
5. sekvenčný (sequence)

#### 💡 Námety na projekty
1. [JDownloader v2](https://jdownloader.org/)
1. [muCommander v2](https://www.mucommander.com/)
1. [Plánovač Kurzov a Skúšok](https://home.pearsonvue.com/) vid. prílohy
1. [Slovensko.sk Schránky v2](https://www.slovensko.sk/sk/titulna-stranka) vid. prílohy

Vlastný projekt **musí obsahovať** veci z odprednášaných tém a mať: 
1. **Kolekcie** (treba vybrať **vhodné dátové štruktúry** podľa povahy/architektúry projektu)
1. **Logovanie** (Logovanie biznis logiky aplikácie + Logovanie Exceptions/Errors)
1. **Lokalizácia** (Preklady a lokalizácia ENG a SK)
1. **XML** (Použitá 1 vybraná XML technológia, spracovanie/parsovanie XML dokumentov, import/export do XML, SAX, DOM, StAX, JAXB, XStream, Jackson XML, XPATH, XQUERY)
1. **Regulárne výrazy** (Vyhľadávanie s prepínačmi, filtrovanie)
1. **JDBC** (Pripojenie na vybranú databázu [Derby](https://db.apache.org/derby/docs/10.4/devguide/cdevdvlp40653.html)/[MySQL](https://dev.mysql.com/downloads/connector/j/)/[PostgreSQL](https://jdbc.postgresql.org/)/[SQLite](https://www.sqlitetutorial.net/sqlite-java/sqlite-jdbc-driver/)/[Oracle Database](https://www.oracle.com/database/technologies/appdev/jdbc-downloads.html), ukladanie dát do DB), môžu sa použiť aj NoSQL databázy za predpokladu, že použijete **JDBC** napr. [MongoDB](https://www.mongodb.com/docs/datalake/tutorial/jdbc-driver/) 
1. **Ošetrenie/validácia vstupov** + bezpečnosť (Ochrana voči základným SQL injekciám)
1. **GUI** aplikácia (Swing, JavaFX, Vaadin), nie Android aplikácia 
2. Aplikácia by mala byť navrhnutá pre 3 **rôznych používateľov/aktérov** napr. admin, power/super user, používateľ (user)
3. **Dátové zložky** musia byť **zapúzdrené** (všetky private)

V projekte treba dodržovať odporúčané postupy (best practices) a konvencie. Využiť objektovo orientované princípy a techniky bez zbytočných duplicít kódu (DRY). Treba myslieť na **príjemné používateľské rozhranie** na jednej strane a na druhej na dobrý **návrh** a **štruktúru**.

Pri projekte sa odovzdávajú **zdrojové kódy** a **projektový súbor** spolu so **spustiteľným JAR súborom (+ knižnice/moduly)** a **dokumentáciou** v miestach odovzdania AIS. Dátum a čas odovzdania si študenti a tímy sledujú sami v AISe a sú povinní ho rešpektovať. V prípade neodovzdania projektu do stanoveného času a dátumu sa projekt hodnotí 0 bodmi. Vedúci tímu + jeden z členov tímu nahrá tieto súbory do AISu. Rovnako každý tím nahrá všetky súbory do svojho verejného repozitára na GitHub/Gitlab/Bitbucket, aby bol k dispozícii iným tímom v skupine na hodnotenie. Projektové zadanie aj výsledný projekt a jeho projektovú dokumentáciu odovzdávate ako 1 samostatný PDF dokument, v ktorom je všetko, nie porozdelované po súboroch.

Ďalej tím pripraví **video** (15-20 minút), kde odprezentuje svoje zadanie. **Do popisu v miestach odovzdania zašle odkaz na YouTube/Vimeo video**. **Video musí byť verejne dostupné cez odkaz** v popise miesta odovzdania. V prípade nedostupnosti odkazu na video či nefunkčnosti aplikácie sa projekt hodnotí 0 bodmi.

Najprv vo videu ukážete a demonštrujete, ako sa váš program používa a či má ošetrené vstupy, nepadá, out of memory. V druhej časti otvoríte kód a vysvetlíte dôležité časti logiky. Každý člen tímu vysvetľuje svoju časť, ktorú mal na starosti. V prípade, že použijete súbory a zdrojové kódy z internetu je povinné uvádzať všetky použité zdroje. Študent musí rozumieť každému riadku daného kódu a orientovať sa v ňom.

Video ma odpovedať na otázky: 
1. Ako funguje aplikácia? 
2. Aká je biznis a aplikačná logika/vrstva SW?
3. Aká je architektúra SW a použité návrhové vzory?
4. Aké komponenty ste použili a prečo?
5. Čo ste sa pri tom naučili? 
6. Čo vám robilo problémy (vrásky na tvári)? Ako ste sa s tým vysporiadali?

Berte to ako priateľský rozhovor s potenciálnym technologickým investorom alebo zákazníkom, ktorý je technologicky orientovaný.

Video bude súčasťou dokumentácie a **projekty sa budú prezentovať a hodnotiť aj priamo na cvičeniach vo forme súťaže medzi jednotlivými tímami.** Každý študent hodnotí aj iné projekty v rámci svojej skupiny (kvalita/prevedenie/realizácia/splnenie požiadaviek/GUI) do pripraveného dotazníka na hodnotenie. Študent tak môže ovplyvniť výsledné bodové hodnotenie za projekty v rozsahu (0-15 % hodnotenia, samozrejme v rámci povoleného počtu 60 bodov za projekt). **Konečné slovo má pri rozhodovaní a prideľovaní bodov vyučujúci**. Najúspešnejšie tímy a projekty môžu získať od Google malé darčeky/Swag.  

## 📰 Odporúčane zdroje, knihy, príprava na skúšku
### 📚 Základné knihy:
1. BLOCH, J. Effective Java. Boston: Addison - Wesley, 2nd edition, 2008. ISBN 03-213-566-8-3
1. NAFTALIN, M. -- WADLER, P. Java Generics and Collections. Sebastopol, USA: O'Reilly Media, 1st edition, 2006. 286 s. ISBN 05-965-277-5-6
1. GAMMA, E. -- HELM, R. -- JOHNSON, R. -- VLISSIDES, J. Design Patterns. Elements of Reusable Object-Oriented Software. Boston : Addison Wesley, 1994. 395 s. ISBN 0-201-63361-2
1. SIERA, K. Head First Java. O'Reilly. 2005. 688 s. ISBN 9780596009205
1. FREEMAN, E. Head First Design Patterns. O'Reilly.  2020. 672 s. ISBN 9781492078005

### 💼 Príprava na skúšku, certifikačnú skúšku OCP:
1. BOAYRSKY, J. OCP Oracle Certified Professional Java SE 11 Developer Complete Study Guide. 2020. John Wiley. 1032 s. ISBN 1119619130
2. BOAYRSKY, J. OCP Oracle Certified Professional Java SE 11 Developer Practice Tests. John Wiley. 2021. 608 s. ISBN 1119696135
3. BOAYRSKY, J. OCP Oracle Certified Professional Java SE 8 Programmer II Study Guide Exam 1Z0-809. Sybex
4. Oracle Certified Professional, Java SE 11 Developer Certification Overview https://education.oracle.com/oracle-certified-professional-java-se-11-developer/trackp_OCPJAV11

### 🌐 Elektronické zdroje:
1. Oracle Java Dokumentácia: Java Platform, Standard Edition 11 API Specification, 2021, https://docs.oracle.com/en/java/javase/11/docs/api/
1. Oracle Blog java https://blogs.oracle.com/java/
1. Dzone Java Spotlight https://dzone.com/java-jdk-development-tutorials-tools-news
