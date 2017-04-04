---
title: "Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana"
description: "Šajā tēmā aprakstīts, kā pārvaldīt elektroniskās ziņošanas (ER) konfigurācija Microsoft Dynamics 365 darbības risinājumu lifecycle."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana

Šajā tēmā aprakstīts, kā pārvaldīt elektroniskās ziņošanas (ER) konfigurācija Microsoft Dynamics 365 darbības risinājumu lifecycle.

<a name="overview"></a>Pārskats
--------

Elektronisko atskaišu veidošana (ER) ir programma, kas atbalsta obligāti vajadzīgus un valsts noteiktus elektroniskos dokumentus programmā Microsoft Dynamics 365 for Operations. Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu. Lai iegūtu sīkāku informāciju, skatiet [elektronisko atskaišu pārskatu](general-electronic-reporting.md).

-   Izveidot elektroniskā dokumenta veidni:
    -   Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:
        -   Pamatā esošo dinamiku 365 darbības datus, piemēram, datu tabulas, datu subjekti un klases.
        -   Procesu raksturīgie rekvizīti, piemēram, izpildes datumu, laiku un laika joslu.
        -   Lietotāja ievades parametrus, noteicis galalietotājam izpildlaikā.
    -   Definēt nepieciešamos dokumenta elementus un to topoloģiju, lai norādītu galīgā dokumenta formātu.
    -   Konfigurēt vēlamo datu plūsmu no atlasītajiem datu avotiem definētajiem dokumenta elementiem (izmantojot datu avota saistījumus dokumenta formāta komponentiem) un norādīt procesa kontroles loģiku.
-   Padarīt veidni pieejamu, lai to varētu izmantot citās Dynamics 365 for Operations instancēs:
    -   Pārveidot dokumenta veidni, kas izveidota programmā Dynamics 365 for Operations, par ER konfigurāciju un eksportēt konfigurāciju no pašreizējās Dynamics 365 for Operations instances kā XML pakotni, kuru var glabāt lokāli vai LCS.
    -   Pārveidot ER konfigurāciju par Dynamics 365 for Operations dokumenta veidni.
    -   Importēt XML pakotni, kas tiek glabāta lokāli vai LCS pašreizējā Dynamics 365 for Operations instancē.
-   Pielāgot elektroniskā dokumenta veidni:
    -   Pārnest veidni no LCS uz pašreizējo Dynamics 365 for Operations instanci kā ER konfigurāciju.
    -   Izveidot ER konfigurācijas pielāgotu versiju un saglabāt atsauci uz tās bāzes versiju.
-   Integrēt veidni noteiktā biznesa procesā, lai tā būtu pieejama programmā Dynamics 365 for Operations:
    -   Konfigurēt iestatījumus, lai Dynamics 365 for Operations sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā. Piemēram, atsaukties uz īpašu kontu kreditoru maksājumu metodi radīt elektronisko maksājuma ziņojumu apstrādes rēķinus ER konfigurāciju.
-   Izmantot veidni noteiktā biznesa procesā:
    -   Darboties ER konfigurācijas noteiktām biznesa procesu. Piemēram, lai ģenerētu elektronisko maksājuma ziņojumu apstrādei rēķinos, maksājuma metode, kas satur norādes uz Traumpunktu konfigurācijas tiek atzīmēta.

## <a name="concepts"></a>Koncepcijas
Šādas lomas un saistītas darbības ir saistītas ar ER konfigurācijas lifecycle.

| Loma                                       | Aktivitātes                                                      | apraksts                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronisko pārskatu veidošanas funkcionālais konsultants | Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).           | Komersants, kas izstrādā ER domēna-īpašu datu modeļi, noformē nepieciešamo elektronisko dokumentu veidnes, un saista tos attiecīgi.                                                                           |
| Elektroniskā pārskata izstrādātājs             | Izveidojiet un pārvaldiet datu modeļu kartējumus.                          | Dynamics 365 par operāciju speciālists, kurš izvēlas nepieciešamo dinamiku 365 operācijas datu avotiem un saista tos ER domēna-īpašu datu modeļi.                                                                 |
| Uzskaites supervizors                      | Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem. | Piemēram, **grāmatvedības vadītājs** lomu, kas ļauj ER konfigurācijas iestatījumus, lai noteiktu kontu kreditoru maksājumu metodi izmantot, lai ģenerētu elektronisko maksājuma ziņojumu apstrādes rēķinus. |
| Kreditoriem maksājamo rēķinu darbinieks            | Izmantot ER artefaktus noteiktā biznesa procesā.                | Piemēram, **kontus kreditoru maksājumi ierēdnis** lomu, kas ļauj elektronisko maksājumu ziņojumi atrodami apstrādes rēķinus, pamatojoties uz ER formātā, kas ir konfigurēts izmantošanai ar noteiktu maksājumu metodi.           |

## <a name="er-configuration-development-lifecycle"></a>ER konfigurācijas izstrādes dzīves cikls
Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķā Dynamics 365 for Operations instancē:

-   Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un Dynamics 365 for Operations instances izmantošanas veiktspējai.
-   Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo Dynamics 365 for Operations ieejas punkti un reģistrēts uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

ER sastāvi, kas ir paredzētas šajā izstrādes vidē var augšupielādēt testa vides konfigurācija novērtēšanai (pienācīgu procesu integrācija, rezultāti un izpildes pareizību) un kvalitātes nodrošināšanu, piemēram, pareizību lomu orientētu piekļuves tiesības un pienākumu sadalījumu. Šim nolūkam var izmantot līdzekļus, kas ļauj ER konfigurācijas datu apmaiņas. Visbeidzot, pierādīta ER sastāvi var augšupielādēt LCS, kur viņi var dalīties ar pakalpojumu abonentiem, vai ražošanas vides iekšējai lietošanai, piemēram, kā parādīts sekojošajā attēlā. ![ER konfigurācijas lifecycle](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)


