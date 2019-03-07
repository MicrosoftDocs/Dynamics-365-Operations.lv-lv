---
title: ER konfigurāciju noformēšana ienākošo dokumentu parsēšanai
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai parsētu ienākošu elektronisku dokumentu.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e5f826afa141c0851a963b33e40c58513e60a07
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "326105"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>ER konfigurāciju noformēšana ienākošo dokumentu parsēšanai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai parsētu ienākošu elektronisku dokumentu. Šajā procedūrā jūs importēsiet nepieciešamās ER konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam, izmantojot tās, parsēsiet ienākošos elektroniskos dokumentus. Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. 

Šīs darbības var veikt, izmantojot jebkuru datu kopu. Pirms sākat, lejupielādējiet un saglabājiet failus, kas ir uzskaitīti tēmā Ienākošo dokumentu parsēšana, lai atjauninātu programmas datus (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents). Minētie faili ir: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
    * Lai demonstrētu ienākošo elektronisko dokumentu parsēšanas XML formātā iespējas, tiks izmantots šāds scenārijs: ERP lietojumprogramma (Dynamics 365 for Finance and Operations) pieprasa datus no tīmekļa pakalpojuma (piemēram, http://efsta.org/ finanšu pakalpojuma EFSTA) un parsē ienākošās atbildes, lai attiecīgi atjauninātu lietojumprogrammas datus. Visefektīvākajai parsēšanai tiek izmantots viens ER formāts, neraugoties uz paredzamo ienākošo dokumentu XML formātā atšķirīgo struktūru.   

## <a name="import-and-review-er-configurations"></a>ER konfigurāciju importēšana un pārskatīšana
Importējiet ER modeļa konfigurāciju, kura satur parauga datu modeli, kas paredzēts ienākošā faila informācijas glabāšanai.  
1. Noklikšķiniet uz Mainīt.
2. Noklikšķiniet uz Ielādēt no XML faila.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu EFSTA model.xml.  
3. Noklikšķiniet uz OK.
4. Kokā atlasiet “EFSTA modelis”.
5. Noklikšķiniet uz Veidotājs.
    * Pārskatiet importētā datu modeļa struktūru. Ņemiet vērā, ka enumType uzskaitījums ir definēts, lai atpazītu tālāk norādītos pakalpojumu atbilžu veidus: iegūt apstiprinājumu par transakcijas iesniegšanu, iegūt informāciju par pēdējo iesniegto transakciju un atpazīt neatbalstītus atbilžu veidus.   
6. Kokā izvērsiet “Atbilde”.
    * Ņemiet vērā, ka saknes vienums “Atbilde” ir definēts, lai norādītu, kāda veida dati jāņem no atbalstīto pakalpojumu atbildēm, lai attiecīgi atjauninātu pieteikumu datus.   
7. Aizvērt lapu.
    * Jūs importēsit ER formāta konfigurāciju, kas norāda, kā ienākošie dokumenti tiks parsēti datu uzglabāšanai ER datu modelī.   
8. Noklikšķiniet uz Mainīt.
9. Noklikšķiniet uz Ielādēt no XML faila.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu EFSTA format.xml.  
10. Noklikšķiniet uz OK.
11. Kokā izvērsiet “EFSTA modelis”.
12. Kokā atlasiet “EFSTA model\EFSTA format”.
13. Noklikšķiniet uz Veidotājs.
14. Noklikšķiniet uz Izvērst/sakļaut.
    * Ņemiet vērā, ka formāta elements CASE tiek izmantots kā saknes elements un satur trīs ligzdotos elementus FILE, kas nozīmē to, ka šis formāts ir paredzēts, lai parsētu vairāku formātu ienākošos failus.  
15. Kokā atlasiet “Atbildes\Transakcijas izpilde\TraC”.
    * Ņemiet vērā, ka atbilde par iesniegto transakciju sākas ar saknes elementu “TraC”.   
16. Kokā atlasiet “Atbildes\Pēdējais transakcijas pieprasījums\Tra”.
    * Ņemiet vērā, ka atbilde par pēdējo iesniegto transakciju sākas ar saknes elementu “Tra”.   
17. Kokā atlasiet “Atbildes\Neparedzēta atbilde\Teksts”.
    * Trešais elements FILE ar ligzdoto elementu TEXT ir pievienots, lai atpazītu citus atbilžu tipus, kuri atšķiras no iepriekš minētajiem.   
18. Noklikšķiniet uz Kartēt formātu uz modeli.
    * Šis modeļa kartējums satur datu plūsmas definīciju, lai saglabātu detalizētu informāciju par parsēto ienākošo dokumentu, izmantojot datu modeļa vienumus.  
19. Noklikšķiniet uz Veidotājs.
20. Kokā izvērsiet "format".
21. Kokā izvērsiet “formāts\Atbildes: Gadījums(Atbildes)”.
    * Pārskatiet datu avota “format” struktūru. Ņemiet vērā, ka visi trīs atbilžu tipi tiek piedāvāti atsevišķi.   
22. Kokā atlasiet “formāts\Atbildes: Gadījums(Atbildes)\aType”.
    * Datu avota vienums “aType” ir pievienots, lai norādītu atbildes tipu, un ir piesaistīts datu modeļa vienumam “Veids”.  
23. Noklikšķiniet uz cilnes Validācijas.
24. Kokā atlasiet “Tips = format.Responses.aType”.
    * Ņemiet vērā, ka ER pārbaude ir konfigurēta, lai informētu lietotāju par situāciju, kad atbildes struktūra neatbilst apstiprinājumam par transakcijas iesniegšanu vai informācijai par pēdējo iesniegto transakciju (neatbalstīts atbildes gadījums).   
25. Aizvērt lapu.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Palaist ER formāta modeļa kartējumu, kas konfigurēts ienākošo failu parsēšanai
Jūs palaidīsit izveidoto modeļa kartējumu testēšanas nolūkos, lai redzētu, kā konfigurētais ER formāts parsēs ienākošās pakalpojumu atbildes. Šajā solī tiek izmantoti dažādi XML faili, lai simulētu dažāda tipa tīmekļa pakalpojumu atbildes.   
1. Atveriet failu Response1.xml XML lasītājā, piemēram, tīmekļa pārlūkprogrammā. Ņemiet vērā, ka šis fails satur apstiprinājuma informāciju par pabeigtu transakciju (“TraC” ir saknes elements).   
2. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Response1.xml.  
3. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka atbildes tips ir pareizi atpazīts un parsēts (ERModelEnumDataSourceHandler#EFSTA model#enumType#C nozīmē transakcijas pabeigšanas gadījumu).   
    * Atveriet failu Response2.xml XML lasītājā. Ņemiet vērā, ka šis fails satur informāciju par pēdējo iesniegto transakciju (“Tra” ir saknes elements).   
4. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Response2.xml.  
5. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka atbildes tips ir pareizi atpazīts un parsēts (ERModelEnumDataSourceHandler#EFSTA model#enumType#R nozīmē sistēmas restartēšanas gadījumu).   
    * Atveriet failu Response3.xml XML lasītājā. Ņemiet vērā, ka šis fails sākas ar TraZ saknes vienumu un ka šī struktūra nav konfigurēta, izmantojot ER formātu.   
6. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Response3.xml.  
7. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka atbildes tips ir pareizi atpazīts kā neatbalstīts (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Informācijas žurnālā ir reģistrēts atbilstošais ziņojums (saskaņā ar ER pārbaudes iestatījumu), un lielākā daļa datu modeļa nav aizpildīta.   
    * Atveriet failu Response4.xml XML lasītājā. Ņemiet vērā, ka šī faila struktūra ir gandrīz tāda pati kā veiksmīgi parsētam failam Response1.xml, izņemot saknes elementa “TraC” ligzdotu elementu secību.   
8. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Response4.xml.  
9. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka atbildes tips ir pareizi atpazīts kā neatbalstīts (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)). Informācijas žurnālā ir reģistrēts atbilstošais ziņojums, un lielākā daļa datu modeļa nav aizpildīta. Tas skaidrojams ar to, ka šī ER formāta pašreizējais iestatījums paredz noteiktu ienākošā faila saknes vienuma ligzdoto elementu secību.   
10. Aizvērt lapu.
11. Kokā atlasiet “Atbildes\Transakcijas izpilde\TraC”.
12. Laukā Ligzdoto elementu parsēšanas kārtība atlasiet “Jebkura”.
    * Atlasiet iestatījumu Jebkura laukā “Ligzdoto elementu parsēšanas kārtība”, lai atļautu jebkuru ligzdoto elementu secību šim saknes XML vienumam.  
13. Noklikšķiniet uz Saglabāt.
14. Noklikšķiniet uz Kartēt formātu uz modeli.
15. Noklikšķiniet uz Palaist.
    * Noklikšķiniet uz Pārlūkot un atlasiet failu Response4.xml.  
16. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka tagad atbildes tips ir pareizi atpazīts kā līdzvērtīgs failam Response1.xml.  

