--- 
title: "Konfigurācijas noformēšana datu importēšanai no ārējā faila CSV formātā (ER)"
description: "Izmantojiet šo procedūru, lai noformētu elektronisko pārskatu veidošanas (ER) konfigurācijas datu importēšanai programmā Dynamics 365 for Finance and Operations no ārējā faila CSV formātā."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f6bfa9f7c0638b0eaacf1a49bcd7d84ffab3acbf
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---
# <a name="design-a-configuration-to-import-data-from-an-external-file-in-csv-format-er"></a>Konfigurācijas noformēšana datu importēšanai no ārējā faila CSV formātā (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai noformētu elektronisko pārskatu veidošanas (ER) konfigurācijas datu importēšanai programmā Dynamics 365 for Finance and Operations no ārējā faila CSV formātā. Šīs procedūras ietvaros jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam “Litware, Inc.”. Lai izpildītu šīs darbības, vispirms ir jāizpilda procedūra “ER Konfigurācijas nodrošinātāja izveide un atzīmēšana ar aktīvu statusu”. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot USMF datu kopu. 

Ir jāveic arī tālāk norādīto failu lokāla lejupielāde un saglabāšana: (https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Procesu var konfigurēt, lai ārējie faili XML, TXT vai CSV formātā tiek importēti uz tabulām programmā Dynamics 365 for Finance and Operations. Vispirms ir jāizveido abstrakts datu modelis importēto datu atspoguļošanai; no biznesa skatu punkta — šim nolūkam tiek izveidota ER datu modeļa konfigurācija. Pēc tam definējiet importētā faila struktūru, kas kartē uz izveidoto datu modeli, kā veidu, lai pārnestu datus no faila uz abstrakto datu modeli, — šim nolūkam tiek izveidota ER formāta konfigurācija. Pēc tam ER datu modeļa konfigurācija ir jāpaplašina ar jaunu modeļa kartējumu, kas apraksta veidu, kādā dati no importētā faila un saglabātie dati no abstraktā datu modeļa tiek lietoti, lai atjauninātu programmas tabulas vai datu elementus.  
    * Tālāk minēto soļu aprakstā ir norādīts, kā ārēji izsekotas kreditoru transakcijas tiek importētas no ārējā CSV faila izmantošanai vēlāk kreditora nodokļa 1099 nosegšanas formās.   
    * Pārliecinieties, ka konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Lietojiet filtru “1099 Maksājumu modelis”. Ja jau esat izpildījis procedūru “ER Izveidot nepieciešamās konfigurācijas datu importēšanai no ārējā faila elektronisko pārskatu veidošanai” un konfigurācija “1099 Maksājumus modelis” ir pieejama konfigurāciju kokā, izlaidiet visas darbības nākamajā apakšuzdevumā.   

## <a name="add-a-new-er-model-configuration"></a>Pievienot jaunu ER modeļa konfigurāciju
1. Tā vietā, lai veidotu jaunu modeli, kas atbalsta datu importēšanu, ielādējiet iepriekš lejupielādēto failu 1099model.xml. Šajā failā ir kreditoru transakciju pielāgotais datu modelis. Šis datu modelis jau ir kartēts uz nepieciešamajiem datu komponentiem.  
2. Noklikšķiniet uz Mainīt.
3. Noklikšķiniet uz Ielādēt no XML faila.
4. Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099model.xml.  
5. Noklikšķiniet uz OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Pievienot jaunu ER formāta konfigurāciju, kas atbalsta datu importēšanu
1. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis”.
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Jauns ievadiet “Uz datu modeli 1099 Maksājumu modelis balstīts formāts”.
4. Laukā Atbalsta datu importēšanu atlasiet vērtību Jā.
5. Nospiediet taustiņu ESC, lai aizvērtu šo lapu.
    * Tā vietā, lai veidotu jaunu ER formātu, kas atbalsta datu importēšanu, ielādējiet iepriekš lejupielādēto failu 1099formatcsv.xml. Šajā failā ir nepieciešamais ER formāts, kas definē ienākošā CSV faila struktūru, un šīs struktūras kartējums uz kreditoru transakciju datu modeli.   
6. Noklikšķiniet uz Mainīt.
7. Noklikšķiniet uz Ielādēt no XML faila.
    * Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099formatcsv.xml.  
8. Noklikšķiniet uz OK.
9. Koka struktūrā izvērsiet zaru “1099 Maksājumu modelis”.
10. Kokā atlasiet “1099 Maksājumu modelis\Kreditoru transakciju importēšanai (CSV)”.

## <a name="review-format-settings"></a>Pārskatīt formāta iestatījumus
1. Noklikšķiniet uz Veidotājs.
2. Noklikšķiniet uz Izvērst/sakļaut.
3. Ieslēdziet opciju “Rādīt detalizēti”.
    * Izveidotais formāts pārstāv paredzamo ārējā faila struktūru CSV formātā.  
4. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība”.
    * Elementam Sakne, kura tips ir SEQUENCE, laukā “Īpašas rakstzīmes” ir atlasīta opcija “Jauna rinda — Windows (CR LF)”. Pamatojoties uz šo iestatījumu, katra rinda parsēšanas failā ir jāuzskata par atsevišķu ierakstu.   
5. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..*”.
    * Elementam Sakne\Rinda, kura tips ir SEQUENCE, laukā “Daudzkārtīgums” ir atlasīta opcija “Viens — daudzi”. Pamatojoties uz šo iestatījumu, parsēšanas failā būs norādīta vismaz viena rinda.   
6. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums”.
    * Ņemiet vērā, ka elements Sakne\Rinda\Tipi, kura tips ir CASE, ir pievienots kā secības Sakne\Rinda ligzdotais elements. Tā kā šis CASE elements satur 3 ligzdotus secības elementus, šī iestatījuma gadījumā tiek pieņemts, ka paredzama 3 dažādu rindas tipu atbilstība parsēšanas failā.   
7. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Virsraksts: Secība 1..1”.
    * Elements Sakne\Rinda\Tipi\Virsraksts, kura tips ir SEQUENCE, satur ligzdotu STRING elementu, kura vērtība ir definēta kā fiksēta virknes vērtība. Šī secība parsēs parsēšanas faila virsraksta rindu.   
8. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Ieraksts: Secība 1..1 (,)”.
    * Elements Sakne\Rinda\Tipi\Ieraksts, kura tips ir SEQUENCE, ir konfigurēts, lai parsētu transakcijas rindas. Ņemiet vērā, ka rakstzīmju opcija “Pielāgots norobežotājs” ir konfigurēta kā komats. Tas nozīmē, ka komats tiks izmantots kā lauku atdalītājs šādam rindas tipam parsēšanas failā.   
    * Ņemiet vērā, ka vairāki ligzdoti elementi, kuriem ir dažādi datu tipi, ir pievienoti elementam Sakne\Rinda\Tipi\Ieraksts, lai parsētu transakcijas rindas kā atdalītus laukus. Ņemiet vērā, ka opcija “Piedāvājuma pieteikums” ir konfigurēta kā “Nav”. Tas nozīmē, ka parsēšanas failā visi šī tipa lauki tiks uzskatīti par tādiem, kam nav apvilkto rakstzīmju.   
9. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Ieraksts: Secība 1..1 (,)\TransactionDate: DateTime”.
    * Piemēram, elements Sakne\Rinda\Tipi\Ieraksts\TransactionDate, kura tips ir DATETIME, ir konfigurēts, lai izgūtu transakcijas datuma un laika vērtību no parsēšanas faila formātā “M/d/gggg”.   
10. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Ieraksts: Secība 1..1 (,)\CountryCode: Virkne 0..1”.
    * Ņemiet vērā, ka elements Sakne\Rinda\Tipi\Ieraksts\CountryCode, kura tips ir STRING, ir konfigurēts tā, ka tam laukā “Daudzkārtīgums” ir atlasīta opcija “Nulle — viens”. Šis iestatījums paredz, ka lauka CountryCode vērtība parsēšanas rindā nav obligāta.   
11. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Ieraksts: Secība 1..1 (,)\Piezīme: Secība 1..1 (,)”.
    * Ņemiet vērā, ka elements Sakne\Rinda\Tipi\Ieraksts\Piezīme, kura tips ir SEQUENCE, ir konfigurēts tā, ka tam laukā “Piedāvājuma pieteikums” ir atlasīta opcija “Visi” un ka laukā “Pēdiņa” ir atlasīta dubulto pēdiņu rakstzīme. Tas nozīmē, ka visi šī rindu tipa lauki parsēšanas failā (ko raksturo ligzdotie elementi: Teksts, kura tips ir STRING) tiks uzskatīti par tādiem, kas ir iekļauti dubulto pēdiņu rakstzīmēs.  
12. Kokā atlasiet “Ienākošs: Fails\Sakne: Secība\Rinda: Secība 1..* \Tipi: Gadījums\Neparsēts: Secība 1..1 ”.
    * Elements Sakne\Rinda\Tipi\Neparsēts, kura tips ir SEQUENCE, ir konfigurēts, lai parsētu transakcijas rindas attiecībā uz struktūru, kura neatbilst iepriekš aprakstītajai struktūrai pamatelementā CASE.   

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Pārskatīt iestatījumu formāta kartējumam uz datu modeli
1. Noklikšķiniet uz Kartēt formātu uz modeli.
    * Modeļa kartējums “Kartēšana uz modeli no CSV formāta” raksturo datu pārsūtīšanas datu plūsmu no ienākošā CSV faila uz datu modeli.   
2. Noklikšķiniet uz Veidotājs.
3. Kokā izvērsiet "format".
    * Ņemiet vērā, ka izveidotais formāts šeit tiek radīts kā datu avota komponents.  
4. Kokā izvērsiet "formāts\Ienākošs: Fails(Ienākošs)".
5. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)”.
6. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)”.
7. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)\Tipi: Gadījums(Tipi)”.
8. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)\Tipi: Gadījums(Tipi)\Ieraksts: Secība 1..1 (,)(Ieraksts)”.
9. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)\Tipi: Gadījums(Tipi)\Ieraksts: Secība 1..1 (,)(Ieraksts)\Dati”.
10. Kokā izvērsiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)\Tipi: Gadījums(Tipi)\Ieraksts: Secība 1..1 (,)(Ieraksts)\Dati\CountryCode: Virkne 0..1 (CountryCode)”.
11. Kokā atlasiet “formāts\Ienākošs: Fails(Ienākošs)\Sakne: Secība(Sakne)\Rinda: Secība 1..* (Rinda)\Tipi: Gadījums(Tipi)\Ieraksts: Secība 1..1 (,)(Ieraksts)\Dati\TransactionDate: DateTime(TransactionDate)”.
    * Ņemiet vērā, ka obligātie un neobligātie formāta elementi, piemēram, TransactionDate un CountryCode, izskatās atšķirīgi iepriekš definētajā datu avota komponentā “formāts”.   
12. Kokā izvērsiet "Transactions = '$both'".
    * Ņemiet vērā, ka elementi formātā, kas definē importētā faila struktūru, ir saistīti ar datu modeļa elementiem. Atkarībā no šīm saistībām importētā CSV faila saturs izpildlaikā tiks saglabāts esošajā datu modelī. Pievērsiet uzmanību elementa CountryRegion saistījumam. Ienākošajos failos, kam nav norādīta valsts koda vērtība, datu modelī visiem transakcijas elementiem valsts kods pēc noklusējuma tiks aizpildīts kā “ASV”.   
13. Ieslēdziet opciju “Rādīt detalizēti”.
14. Noklikšķiniet uz cilnes Validācijas.
15. Noklikšķiniet uz Meklēt.
16. Laukā Atrast ierakstiet “kreditors”.
17. Noklikšķiniet uz Atrast nākamo.
    * Šajā formāta kartējumā var būt lietotāja definēta loģika validēt importēto datu precizitāti no biznesa skatu punkta. Piemēram, pamatojoties uz iestatījumu, jebkurai importējamā faila rindai, kuras struktūra neatbilst nedz virsraksta rindas, nedz transakcijas rindas struktūrai, informācijas žurnālā tiek ģenerēts brīdinājuma ziņojums, kas lietotāju informē par šo gadījumu un norāda transakcijas kārtas numuru failā.   
18. Aizvērt lapu.

## <a name="run-the-format-mapping"></a>Formāta kartēšanas palaišana
Testēšanas nolūkos izpildiet formāta kartēšanu, izmantojot iepriekš lejupielādēto failu 1099entriescsv.csv. Ģenerētajā izvadē tiks norādīti dati, kuri tiks importēti no atlasītā CSV faila un reālajā importēšanā aizpildīti pielāgotajā datu modelī.   
1. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099entriescsv.csv.  
2. Noklikšķiniet uz OK.
    * Ņemiet vērā brīdinājuma ziņojumus par rindām, kas nav pieņemtas. 4. rindā ir ienākumu vērtība, kas ir norādīta nepieņemamā formātā, savukārt 7. rindā nav transakcijas piezīmes teksta dubultās pēdiņas.   
    * Pārskatiet izvadi XML formātā, kas parāda no atlasītā faila importētos un uz datu modeli pārnestos datus. Ņemiet vērā, ka tika apstrādātas visas 7 importētā CSV faila rindas. Datus saturošo lauku virsraksta 1. rinda tika izlaista, 4 transakcijas tika pareizi parsētas un 2 transakcijas tika atpazītas kā nederīgas.   
3. Aizvērt lapu.
4. Aizvērt lapu.


