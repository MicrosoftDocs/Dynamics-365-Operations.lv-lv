---
title: "Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana"
description: "Šajā tēmā ir aprakstīts, kā pārvaldīt Microsoft Dynamics 365 for Operations risinājuma elektronisko pārskatu (ER) konfigurāciju dzīves ciklu."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cecbb5bd57aa24a942d10241bd83e4c1996a3805
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā pārvaldīt Microsoft Dynamics 365 for Operations risinājuma elektronisko pārskatu (ER) konfigurāciju dzīves ciklu.

<a name="overview"></a>Pārskats
--------

Elektronisko atskaišu veidošana (ER) ir programma, kas atbalsta obligāti vajadzīgus un valsts noteiktus elektroniskos dokumentus programmā Microsoft Dynamics 365 for Operations. Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu. Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu veidošanu](general-electronic-reporting.md).

-   Izveidot elektroniskā dokumenta veidni:
    -   Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:
        -   Pamata Dynamics 365 for Operations dati, piemēram, datu tabulas, datu ieraksti un klases.
        -   Procesam specifiskie rekvizīti, piemēram, izpildes datums un laiks, laika josla.
        -   Lietotāja ievadītie parametri, ko lietotājs norāda izpildes laikā.
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
    -   Konfigurēt iestatījumus, lai Dynamics 365 for Operations sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā. Piemēram, ietveriet atsauci uz ER konfigurāciju noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.
-   Izmantot veidni noteiktā biznesa procesā:
    -   Izpildīt ER konfigurāciju konkrētā biznesa procesā. Piemēram, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu, ja ir atlasīta maksājumu metode ar atsauci uz ER konfigurāciju.

## <a name="concepts"></a>Koncepcijas
Ar ER konfigurācijas dzīves ciklu ir saistītas tālāk norādītās lomas un saistītās darbības.

| Loma                                       | Aktivitātes                                                      | apraksts                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronisko pārskatu veidošanas funkcionālais konsultants | Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).           | Biznesa procesos iesaistīta persona, kura izstrādā ER domēnam specifiskos datu modeļu, izstrādā nepieciešamās elektronisko dokumentu veidnes un atbilstoši tās saista.                                                                           |
| Elektroniskā pārskata izstrādātājs             | Izveidojiet un pārvaldiet datu modeļu kartējumus.                          | Dynamics 365 for Operations speciālists, kurš atlasa nepieciešamos Dynamics 365 for Operations datu avotus un saista tos ar ER domēnam specifiskiem datu modeļiem.                                                                 |
| Uzskaites supervizors                      | Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem. | Piemēram, loma **Uzskaites supervizors**, kas sniedz iespēju ER konfigurācijas iestatījumus izmantot noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu. |
| Kreditoriem maksājamo rēķinu darbinieks            | Izmantot ER artefaktus noteiktā biznesa procesā.                | Piemēram, loma **Kreditoriem maksājamo rēķinu darbinieks**, kas sniedz iespēju ģenerēt rēķinu apstrādes elektroniskos maksājumu ziņojumus, pamatojoties uz ER formātu, kas ir konfigurēts noteiktai maksājumu metodei.           |

## <a name="er-configuration-development-lifecycle"></a>ER konfigurācijas izstrādes dzīves cikls
Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķā Dynamics 365 for Operations instancē:

-   Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un Dynamics 365 for Operations instances izmantošanas veiktspējai.
-   Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo Dynamics 365 for Operations ieejas punkti un reģistrēts uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

Izstrādes vidē izstrādātās ER konfigurācijas var augšupielādēt testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale). Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus. Visbeidzot apstiprinātās ER konfigurācijas var augšupielādēt LCS, kur tās var koplietot ar pakalpojumu abonentiem, vai ražošanas vidē iekšējai lietošanai, kā tas ir redzams tālāk esošajā attēlā. ![ER konfigurācijas dzīves cikls](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)




