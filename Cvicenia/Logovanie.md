# 📟 Čo treba Logovať/Čo je vhodné Logovať?
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

## Ukážky Logov z aplikácií
### Gantt Project (Java Freeware)
![logy](https://user-images.githubusercontent.com/24510943/228639920-5a6129d3-f96a-4d17-80c0-f12e07ab6d25.png)
```log
C:\Users\Administrator\ganttproject.log

GanttProject 3.2.3230
Settings file:
	location: C:\Users\Administrator\.ganttproject
	size:4664
	is readable: true
java.class.path: eclipsito.jar;C:\Program Files (x86)\GanttProject-3.2
java.home: C:\Program Files (x86)\GanttProject-3.2\runtime
java.ext.dirs: null
java.io.tmpdir: C:\Users\ADMINI~1\AppData\Local\Temp\
java.runtime.version: 11.0.13+8-LTS
java.vendor: BellSoft
java.vm.name: OpenJDK 64-Bit Server VM
java.vm.vendor: BellSoft
java.vm.version: 11.0.13+8-LTS
os.arch: amd64
os.name: Windows 10
os.version: 10.0
sun.java.command: com.bardsoftware.eclipsito.Launch --verbosity 1 --version-dirs plugins;~/.ganttproject.d/updates --app net.sourceforge.ganttproject.GanttProject
user.country: SK
user.dir: C:\Program Files (x86)\GanttProject-3.2
user.home: C:\Users\Administrator
user.language: sk
user.timezone: Europe/Prague

mar 29, 2023 6:56:18 PM biz.ganttproject.LoggerImpl debug
FINE: Creating main frame...
mar 29, 2023 6:56:18 PM biz.ganttproject.LoggerImpl debug
FINE: 1. loading look'n'feels
mar 29, 2023 6:56:18 PM biz.ganttproject.LoggerImpl debug
FINE: 2. loading options
mar 29, 2023 6:56:19 PM biz.ganttproject.LoggerImpl debug
FINE: 3. creating menus...
mar 29, 2023 6:56:19 PM biz.ganttproject.LoggerImpl debug
FINE: 4. creating views...
mar 29, 2023 6:56:20 PM biz.ganttproject.LoggerImpl debug
FINE: 5. calculating size and packing...
mar 29, 2023 6:56:20 PM biz.ganttproject.LoggerImpl debug
FINE: 6. changing language ...
mar 29, 2023 6:56:20 PM biz.ganttproject.LoggerImpl debug
FINE: 7. first attempt to restore bounds
mar 29, 2023 6:56:20 PM biz.ganttproject.LoggerImpl debug
FINE: 8. finalizing...
mar 29, 2023 6:56:21 PM net.sourceforge.ganttproject.GPLogger log
INFO: Deleting old auto-save files
```
### JDownloader (Java Freeware)
![29 03 2023 20_58_45-JDownloader 2](https://user-images.githubusercontent.com/24510943/228641476-7715699c-da36-4b68-9919-a00131064748.png)
```log
------------------------Thread: 1:Log.L.log-----------------------
--ID:1TS:1679745735388-25.3.2023 13:02:15 -  [org.appwork.loggingv3.LogV3(info)] -> Application Root: C:\Users\Administrator\AppData\Local\JDownloader 2.0
--ID:1TS:1679745735423-25.3.2023 13:02:15 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Prefer (merged) JSon Storage from File: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.jdownloader.update.lastchance.LastChanceConfig.json
--ID:1TS:1679745736560-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Prefer (merged) JSon Storage from File: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.jdownloader.updatev2.UpdateSettings.json
--ID:1TS:1679745736604-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Load JSon Storage from Classpath url: jar:file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/JDownloader.jar!/cfg/updateclient/Setup.json
--ID:1TS:1679745736605-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Prefer (merged) JSon Storage from File: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\updateclient\Setup.json
--ID:1TS:1679745736606-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.appwork.updatesys.client.Setup|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\updateclient\Setup
------------------------Thread: 21:Log.L.log-----------------------
--ID:21TS:1679745736623-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Prefer (merged) JSon Storage from File: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.jdownloader.settings.InternetConnectionSettings.json
--ID:21TS:1679745736623-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.jdownloader.updatev2.InternetConnectionSettings|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.jdownloader.settings.InternetConnectionSettings
--ID:21TS:1679745736645-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> Load JSon Storage from Classpath url: jar:file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/JDownloader.jar!/cfg/updateclient/HttpSettings.json
--ID:21TS:1679745736646-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\updateclient\HttpSettings.json
--ID:21TS:1679745736646-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.appwork.updatesys.client.defaultimpl.http.UpdateHttpClientOptions|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\updateclient\HttpSettings
--ID:21TS:1679745736654-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\ProxySelector.json
--ID:21TS:1679745736655-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.appwork.updatesys.client.defaultimpl.http.ProxySelectorSettings|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\ProxySelector
--ID:21TS:1679745736658-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Read Config(File): C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\ProxySelector.proxies.json
--ID:21TS:1679745736683-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Read Config(URL): jar:file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/JDownloader.jar!/cfg/updateclient/Setup.updateservers.json
--ID:21TS:1679745736687-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JD\extensions.json
--ID:21TS:1679745736687-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.appwork.updatesys.client.extensions.ExtensionsStorage|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JD\extensions
--ID:21TS:1679745736691-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Read Config(File): C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JD\extensions.installed.json
--ID:21TS:1679745736691-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Read Config(File): C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JD\extensions.requestedinstalls.json
--ID:21TS:1679745736701-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.appwork.updatesys.client.tracker.TrackConfig.json
--ID:21TS:1679745736706-25.3.2023 13:02:16 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JDU\extensions.json
--ID:21TS:1679745736706-25.3.2023 13:02:16 -  [org.appwork.loggingv3.LogV3(finer)] -> Init StorageHandler for Interface:org.appwork.updatesys.client.extensions.ExtensionsStorage|Path:C:\Users\Administrator\AppData\Local\JDownloader 2.0\update\versioninfo\JDU\extensions
------------------------Thread: 23:Log.L.log-----------------------
--ID:23TS:1679745752838-25.3.2023 13:02:32 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/jdownloader/updatev2/UpdaterTranslation.sk.lng/null
--ID:23TS:1679745752839-25.3.2023 13:02:32 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/jdownloader/updatev2/UpdaterTranslation.en.lng/null
--ID:23TS:1679745752901-25.3.2023 13:02:32 -  [org.appwork.loggingv3.LogV3(finer)] -> Read Config(File): C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\org.jdownloader.settings.InternetConnectionSettings.customproxylist.json
------------------------Thread: 28:Log.L.log-----------------------
--ID:28TS:1679745752985-25.3.2023 13:02:32 -  [org.appwork.storage.JsonKeyValueStorage(<init>)] -> CFG File does not exist: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\laf\JDDefaultLookAndFeel.json
--ID:28TS:1679745753074-25.3.2023 13:02:33 -  [org.appwork.loggingv3.LogV3(info)] -> LaF init: org.jdownloader.gui.laf.jddefault.JDDefaultLookAndFeel
--ID:28TS:1679745753094-25.3.2023 13:02:33 -  [org.appwork.utils.logging2.extmanager.ExtLogManager(getLogger)] -> Ignored: de.javasoft.plaf.synthetica.SyntheticaLookAndFeel
--ID:28TS:1679745753102-25.3.2023 13:02:33 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/appwork/swing/synthetica/LanguageFileSetup.sk.lng/null
--ID:28TS:1679745753103-25.3.2023 13:02:33 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/appwork/swing/synthetica/LanguageFileSetup.en.lng/null
--ID:28TS:1679745753116-25.3.2023 13:02:33 -  [org.jdownloader.gui.laf.jddefault.JDDefaultLookAndFeel(load)] -> Custom LAF XML: C:\Users\Administrator\AppData\Local\JDownloader 2.0\cfg\laf\JDDefaultLookAndFeel.xml
--ID:28TS:1679745753337-25.3.2023 13:02:33 -  [org.appwork.utils.logging2.extmanager.ExtLogManager(getLogger)] -> Ignored: de.javasoft.plaf.synthetica.painter.ImagePainter
--ID:28TS:1679745753647-25.3.2023 13:02:33 -  [org.appwork.loggingv3.LogV3(info)] -> LAF Init duration: 573ms
------------------------Thread: 23:Log.L.log-----------------------
--ID:23TS:1679745755277-25.3.2023 13:02:35 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/appwork/utils/locale/AWUTranslation.sk.lng/null
--ID:23TS:1679745755277-25.3.2023 13:02:35 -  [org.appwork.loggingv3.LogV3(finer)] -> Load Translation file:/C:/Users/Administrator/AppData/Local/JDownloader%202.0/translations/org/appwork/utils/locale/AWUTranslation.en.lng/null
------------------------Thread: 1:Log.L.log-----------------------
--ID:1TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.loggingv3.LogV3(info)] -> No Vetos
--ID:1TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.loggingv3.LogV3(info)] -> Fire onShutDownEvents:0
--ID:1TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.loggingv3.LogV3(info)] -> Create ExitThread
```
```log
------------------------Thread: 1:org.appwork.shutdown.ShutdownController.log-----------------------
--ID:1TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> Request Shutdown: org.jdownloader.updatev2.ForcedShutdown@13167f4
--ID:1TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> Wait for ShutdownThread:Thread[ShutdownThread:1679745773234|org.jdownloader.updatev2.ForcedShutdown@13167f4,5,main]|waitDuration:0
------------------------Thread: 37:org.appwork.shutdown.ShutdownController.log-----------------------
--ID:37TS:1679745773234-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> Exit Now(Controller): Code: 0
--ID:37TS:1679745773235-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> [1/9|Priority: 10000]ShutdownController: start item->org.appwork.shutdown.ShutdownRunableEvent Priority: 10000
--ID:37TS:1679745773237-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> [1/9|Priority: 10000]ShutdownController: item ended after->2
--ID:37TS:1679745773237-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> [Done:1/9]
--ID:37TS:1679745773237-25.3.2023 13:02:53 -  [org.appwork.shutdown.ShutdownController(log)] -> [2/9|Priority: 10000]ShutdownController: start item->flushing logs to disk
```

### muCommander (Java Freeware)
![29 03 2023 21_06_29-C__Users_Administrator_ - muCommander](https://user-images.githubusercontent.com/24510943/228642422-0476b12c-4c55-4d59-8b63-41d96a0f5a58.png)
```log
[2023-03-29 21:05:44.618] FINE FolderChangeMonitor.java#windowGainedFocus,323 com.mucommander.core.FolderChangeMonitor@532e1065: setting forceRefresh as MainFrame gained focus
[2023-03-29 21:05:44.830] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:05:44.831] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:05:52.868] FINEST FocusDialog.java#windowActivated,228 requesting focus on initial focus component
[2023-03-29 21:05:52.869] FINEST FocusDialog.java#windowActivated,236 requestFocusInWindow failed, calling requestFocus
[2023-03-29 21:05:52.928] FINE FocusRequester.java#run,102 focus requested on javax.swing.JButton
[2023-03-29 21:05:55.554] FINE FolderChangeMonitor.java#windowGainedFocus,323 com.mucommander.core.FolderChangeMonitor@532e1065: setting forceRefresh as MainFrame gained focus
[2023-03-29 21:05:55.724] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:05:55.724] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:05:57.643] FINEST CredentialsManager.java#authenticateImplicit,348 called, fileURL=https://github.com/mucommander/mucommander/issues/new/ containsCredentials=false
[2023-03-29 21:05:57.644] FINEST CredentialsManager.java#findMatches,383 returning matches=[]
[2023-03-29 21:05:57.644] FINEST CredentialsManager.java#findMatches,383 returning matches=[]
[2023-03-29 21:05:57.663] FINE AbstractProcess.java#startMonitoring,90 Starting process merged output monitor...
[2023-03-29 21:05:58.145] FINE ProcessOutputMonitor.java#run,115 Process output stream emptied, closing
[2023-03-29 21:06:06.915] FINE FolderChangeMonitor.java#windowGainedFocus,323 com.mucommander.core.FolderChangeMonitor@532e1065: setting forceRefresh as MainFrame gained focus
[2023-03-29 21:06:06.939] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:06:06.939] FINE ModificationDateBasedMonitoredFile.java#isChanged,42 isChanged = false
[2023-03-29 21:06:09.812] FINEST FocusDialog.java#windowActivated,228 requesting focus on initial focus component
[2023-03-29 21:06:09.813] FINEST FocusDialog.java#windowActivated,236 requestFocusInWindow failed, calling requestFocus
[2023-03-29 21:06:09.897] FINE FocusRequester.java#run,102 focus requested on javax.swing.JButton
```

### Xiaomi Mi Home (Freeware)
```log
SmartHome 0:[DEBUG]-11-29 00:44:47.980 check developer execute, onFail failed to connect to de.api.io.mi.com/35.157.42.148 (port 443) from /192.168.100.2 (port 45652) after 20000ms
SmartHome 0:[DEBUG]-11-29 01:23:48.733 check developer execute, onFail failed to connect to de.api.io.mi.com/18.194.154.249 (port 443) from /192.168.100.2 (port 41478) after 20000ms
SmartHome 0:[DEBUG]-11-29 02:31:18.869 check developer execute, onSuccess net Result: isCache = false,code = 0, response = {"code":0,"message":"ok","result":false}
SmartHome 0:[DEBUG]-11-29 03:19:12.410 check developer execute, onSuccess net Result: isCache = false,code = 0, response = {"code":0,"message":"ok","result":false}
SmartHome 0:[DEBUG]-11-29 09:10:21.945 check developer execute, onFail failed to connect to de.api.io.mi.com/35.157.42.148 (port 443) from /192.168.100.2 (port 49830) after 20000ms
SmartHome 0:[DEBUG]-11-29 09:36:24.145 check developer execute, onFail failed to connect to de.api.io.mi.com/35.157.42.148 (port 443) from /192.168.100.2 (port 50316) after 20000ms
SmartHome 0:[DEBUG]-11-29 10:02:26.372 check developer execute, onFail failed to connect to de.api.io.mi.com/18.194.154.249 (port 443) from /192.168.100.2 (port 46138) after 20000ms
```
```log
SmartHome 0:[DEBUG]-11-30 19:19:45.099 RPC: error code is success
SmartHome 107:[DEBUG]-11-30 19:19:45.277 RPC: error code is success
SmartHome 971:[DEBUG]-11-30 19:19:46.159 RPC: error code is success
SmartHome 19968:[DEBUG]-11-30 19:20:05.156 RPC: error code is success
SmartHome 266216:[DEBUG]-11-30 19:24:11.387 RPC: error code is success
```
### Minecraft (Java)
![latest-log-selectall](https://user-images.githubusercontent.com/24510943/228642946-e9a2b429-0642-48c2-a657-1ef3c4bac2f8.png)

## 📕 Zdroje a inšpirácia 
A. [Logging Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html)  
B. [Ultimate Guide to Logging](https://www.loggly.com/ultimate-guide/java-logging-basics/)  
C. [How To Do Logging In Java](https://www.marcobehler.com/guides/java-logging)  
D. [Java Logging Overview](https://docs.oracle.com/javase/10/core/java-logging-overview.htm#JSCOR-GUID-B83B652C-17EA-48D9-93D2-563AE1FF8EDA)  
E. [Konfigurácia Logovania Log4j](https://techdocs.broadcom.com/us/en/ca-mainframe-software/traditional-management/web-viewer/14-0/installing/configure-logging.html)
F. [Logovacia Trieda Level Log4j](https://logging.apache.org/log4j/1.2/apidocs/org/apache/log4j/Level.html)
