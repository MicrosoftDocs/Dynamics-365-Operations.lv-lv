---
title: "Elektronisko atskaišu veidošanas konfigurācijas dzīves cikla pārvaldīšana"
description: "Šajā tēmā ir aprakstīts, kā pārvaldīt Microsoft Dynamics 365 for Finance and Operations risinājuma elektronisko pārskatu (ER) konfigurāciju dzīves ciklu."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 35288f5c2edfa8a340f963a5c7216041765a58b4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Pārvaldīt elektronisko pārskatu veidošanas konfigurācijas dzīves ciklu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā pārvaldīt Microsoft Dynamics 365 for Finance and Operations risinājuma elektronisko pārskatu (ER) konfigurāciju dzīves ciklu.

<a name="overview"></a>Apskats
--------

Elektronisko pārskatu veidošana (Electronic reporting — ER) ir programma, kas programmatūrā Microsoft Dynamics 365 for Finance and Operations atbalsta ar likumu noteiktos un valstij specifiskos elektroniskos dokumentus. Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu. Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu veidošanu](general-electronic-reporting.md).

-   Izveidot elektroniskā dokumenta veidni:
    -   Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:
        -   Pamata Finance and Operations dati, piemēram, datu tabulas, datu ieraksti un klases.
        -   Procesam specifiskie rekvizīti, piemēram, izpildes datums un laiks, laika josla.
        -   Lietotāja ievadītie parametri, ko lietotājs norāda izpildes laikā.
    -   Definēt nepieciešamos dokumenta elementus un to topoloģiju, lai norādītu galīgā dokumenta formātu.
    -   Konfigurēt vēlamo datu plūsmu no atlasītajiem datu avotiem definētajiem dokumenta elementiem (izmantojot datu avota saistījumus dokumenta formāta komponentiem) un norādīt procesa kontroles loģiku.
-   Padarīt veidni pieejamu, lai to varētu izmantot citās Finance and Operations instancēs:
    -   Programmā Finance and Operations izveidotu dokumenta veidni pārveidot par ER konfigurāciju un konfigurāciju no pašreizējās Finance and Operations eksportēt kā XML pakotni, kuru var glabāt lokāli vai pakalpojumā LCS.
    -   ER konfigurāciju pārveidot par Finance and Operations dokumenta veidni.
    -   XML pakotni, kas tiek glabāta lokāli vai pakalpojumā LCS, importēt pašreizējā Finance and Operations instancē.
-   Pielāgot elektroniskā dokumenta veidni:
    -   Veidni no LCS uz pārnest uz pašreizējo Finance and Operations instanci kā ER konfigurāciju.
    -   Izveidot ER konfigurācijas pielāgotu versiju un saglabāt atsauci uz tās bāzes versiju.
-   Integrēt veidni noteiktā biznesa procesā, lai tā būtu pieejama programmā Finance and Operations:
    -   Konfigurēt iestatījumus, lai Finance and Operations sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā. Piemēram, ietveriet atsauci uz ER konfigurāciju noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.
-   Izmantot veidni noteiktā biznesa procesā:
    -   Izpildīt ER konfigurāciju konkrētā biznesa procesā. Piemēram, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu, ja ir atlasīta maksājumu metode ar atsauci uz ER konfigurāciju.

## <a name="concepts"></a>Koncepcijas
Ar ER konfigurācijas dzīves ciklu ir saistītas tālāk norādītās lomas un saistītās darbības.

| Loma                                       | Aktivitātes                                                      | Apraksts                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronisko pārskatu veidošanas funkcionālais konsultants | Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).           | Biznesa procesos iesaistīta persona, kura izstrādā ER domēnam specifiskos datu modeļu, izstrādā nepieciešamās elektronisko dokumentu veidnes un atbilstoši tās saista.                                                                           |
| Elektroniskā pārskata izstrādātājs             | Izveidojiet un pārvaldiet datu modeļu kartējumus.                          | Finance and Operations speciālists, kurš atlasa nepieciešamos Finance and Operations datu avotus un saista tos ar ER domēnam specifiskiem datu modeļiem.                                                                 |
| Uzskaites supervizors                      | Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem. | Piemēram, loma **Uzskaites supervizors**, kas sniedz iespēju ER konfigurācijas iestatījumus izmantot noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu. |
| Kreditoriem maksājamo rēķinu darbinieks            | Izmantot ER artefaktus noteiktā biznesa procesā.                | Piemēram, loma **Kreditoriem maksājamo rēķinu darbinieks**, kas sniedz iespēju ģenerēt rēķinu apstrādes elektroniskos maksājumu ziņojumus, pamatojoties uz ER formātu, kas ir konfigurēts noteiktai maksājumu metodei.           |

## <a name="er-configuration-development-lifecycle"></a>ER konfigurācijas izstrādes dzīves cikls
Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķu Finance and Operations instanci.

-   Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un Finance and Operations instances veiktspējai.
-   Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo Finance and Operations ieejas punkti un reģistrētais uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

Izstrādes vidē izstrādātās ER konfigurācijas var augšupielādēt testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale). Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus. Visbeidzot apstiprinātās ER konfigurācijas var augšupielādēt LCS, kur tās var koplietot ar pakalpojumu abonentiem, vai ražošanas vidē iekšējai lietošanai, kā tas ir redzams tālāk esošajā attēlā. ![ER konfigurācijas dzīves cikls](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)




