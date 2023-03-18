# 📟 Čo treba Logovať/čo je vhodné Logovať?
1.	Udalosti typu Autentifikácia/Prihlasovanie 
2.	Udalosti Riadenia prístupu
3.	Udalosti typu Upload súborov a dát
4.	Udalosti Validácie vstupov
5.	Udalosti typu obmedzenia
6.	Udalosti typu Podozrivé/Nebezpečné Správanie 
7.	Zmeny prístupov a oprávnení
8.	Zmeny Citlivé/Osobne údaje 
9.	Sekvenčné chyby/Chyby, ktoré vzniknú za behu
10.	Chyby manažovania relácií (Sessions)
11.	Systémové udalosti
12.	Manažovanie používateľov

## Logovacie Úrovne (Logging Levels)
![logss](https://user-images.githubusercontent.com/24510943/226104456-27c5969e-4841-4802-9bec-122f72869d61.png)
**1. OFF** - Nnajvyššia možnú úroveň a je určený na vypnutie logovania. Nebudú sa zaznamenávať žiadne správy.   
**2. FATAL** - Veľmi závažné chybové udalosti, ktoré pravdepodobne povedú k prerušeniu aplikácie. Chyby servera, ktoré bránia spusteniu aplikácie.  
**3. ERROR** - Chybové udalosti, ktoré môžu aplikácii naďalej umožniť bežať. Chyby, ktoré  môžu umožniť obnovenie. Táto úroveň zahŕňa aj fatálne správy.  
**4. WARN** -  Potenciálne škodlivé situácie. Udalosti, ktoré môžu viesť k chybe. Táto úroveň zahŕňa aj chybové a fatálne správy.  
**5. INFO** - Informačné správy, ktoré zvýrazňujú priebeh aplikácie na vysoko granulárnej úrovni. Zahŕňa aj varovania, chyby a fatálne správy.  
**6. DEBUG** - Informačné udalosti s drobnou granularitou, ktoré sú najužitočnejšie na ladenie aplikácie. zahŕňa aj správy Info, Varovanie, Chyba a Závažné správy.  
**7. TRACE** - Označuje jemnejšie informačné udalosti ako DEBUG. Zaznamenáva všetky správy, ktoré zachytávajú typický tok cez aplikáciu. Táto úroveň zahŕňa správy ladenia, informácií, varovania, chýb a závažných správ. Zaznamenáva všetky správy (rovnako ako Trace).  
**8. ALL** - Najnižšia možnú úroveň a je určený na zapnutie všetkých protokolov.  

![atd49gel95khv4dyt7kn](https://user-images.githubusercontent.com/24510943/226108439-e9867e2f-3f31-46c6-aff9-cd0cddfce560.png)

```java
// Log4j API Level Class
public final static int OFF_INT = Integer.MAX_VALUE;
public final static int FATAL_INT = 50000;
public final static int ERROR_INT = 40000;
public final static int WARN_INT  = 30000;
public final static int INFO_INT  = 20000;
public final static int DEBUG_INT = 10000;
public static final int TRACE_INT = 5000; 
public final static int ALL_INT = Integer.MIN_VALUE; 
```

![BOUAq](https://user-images.githubusercontent.com/24510943/226104471-97ce6bcf-67a2-4bb5-bdb1-cec67b2da154.png)  

### Príklady Logovania Úrovne Upozornenia (Log/Logger.Warn)
```java
log.warn("Používateľský účet na ABC je zakázaný službou XYZ. {}.", email);
logger.warn("Ubehol časový limit čakania na dokončenie úloh úpravy.");
log.warn("Duplicitný email/účet pre používateľa {}.", email);
log.warn("Zlyhanie overenia správy pre {}.", email);
log.warn("Nie je možné načítať manažéra požiadaviek medzi vláknami '{}' kvôli {}", clazz, e.toString());
logger.warn("Súbor [Ext] sa nenašiel: " + cesta);
logger.warn(String.format("Vyskytla sa výnimka pri vrátení transakcie s vypršaným časovým limitom %s", txId), e); 
```

## 📕 Zdroje a inšpirácia 
A. [Logging Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html)  
B. [Ultimate Guide to Logging](https://www.loggly.com/ultimate-guide/java-logging-basics/)  
C. [How To Do Logging In Java](https://www.marcobehler.com/guides/java-logging)  
D. [Java Logging Overview](https://docs.oracle.com/javase/10/core/java-logging-overview.htm#JSCOR-GUID-B83B652C-17EA-48D9-93D2-563AE1FF8EDA)  
E. [Konfigurácia Logovania Log4j](https://techdocs.broadcom.com/us/en/ca-mainframe-software/traditional-management/web-viewer/14-0/installing/configure-logging.html)
F. [Logovacia Trieda Level Log4j](https://logging.apache.org/log4j/1.2/apidocs/org/apache/log4j/Level.html)
