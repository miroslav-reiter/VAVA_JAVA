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

## Logovacie Úrovne (logging Levels)
OFF - Nnajvyššia možnú úroveň a je určený na vypnutie logovania
FATAL - Veľmi závažné chybové udalosti, ktoré pravdepodobne povedú k prerušeniu aplikácie
ERROR - Chybové udalosti, ktoré môžu aplikácii naďalej umožniť bežať
WARN -  Potenciálne škodlivé situácie
INFO - Informačné správy, ktoré zvýrazňujú priebeh aplikácie na vysoko granulárnej úrovni
DEBUG - Informačné udalosti s drobnou granularitou, ktoré sú najužitočnejšie na ladenie aplikácie
TRACE - Označuje jemnejšie informačné udalosti ako DEBUG
ALL - Najnižšia možnú úroveň a je určený na zapnutie všetkých protokolov

![logss](https://user-images.githubusercontent.com/24510943/226104456-27c5969e-4841-4802-9bec-122f72869d61.png)

![BOUAq](https://user-images.githubusercontent.com/24510943/226104471-97ce6bcf-67a2-4bb5-bdb1-cec67b2da154.png)

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

https://logging.apache.org/log4j/1.2/apidocs/org/apache/log4j/Level.html

## 📕 Zdroje a inšpirácia 
A. [Logging Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html)  
B. [Ultimate Guide to Logging](https://www.loggly.com/ultimate-guide/java-logging-basics/)  
C. [How To Do Logging In Java](https://www.marcobehler.com/guides/java-logging)  
D. [Java Logging Overview](https://docs.oracle.com/javase/10/core/java-logging-overview.htm#JSCOR-GUID-B83B652C-17EA-48D9-93D2-563AE1FF8EDA)  
