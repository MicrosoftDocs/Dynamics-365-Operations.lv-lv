---
title: Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Microsoft Dynamics 365 Finance risinājumam.
author: NickSelin
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 165f2c981b550f8a6fd4d2ce08763e6fa3c8b6e7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750110"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Microsoft Dynamics 365 Finance.

## <a name="overview"></a>Kopsavilkums

Elektronisko pārskatu izveide (ER) ir programma, kas nodrošina ar likumu noteikto un valstij raksturīgo elektronisko dokumentu atbalstu. Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu. Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu (EP) veidošanu](general-electronic-reporting.md).

- Izveidot elektroniskā dokumenta veidni:

    - Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:

        - Pamata dati, piemēram, datu tabulas, datu ieraksti un klases.
        - Procesam specifiskie rekvizīti, piemēram, izpildes datums un laiks, laika josla.
        - Lietotāja ievadītie parametri, ko lietotājs norāda izpildes laikā.

    - Definēt nepieciešamos dokumenta elementus un to topoloģiju, lai norādītu galīgā dokumenta formātu.
    - Konfigurēt vēlamo datu plūsmu no atlasītajiem datu avotiem definētajiem dokumenta elementiem (izmantojot datu avota saistījumus dokumenta formāta komponentiem) un norādīt procesa kontroles loģiku.

- Padarīt veidni pieejamu, lai to varētu izmantot citās instancēs:

    - Pārveidot dokumenta veidni, kas izveidota programmā Dynamics AX, par ER konfigurāciju un eksportēt konfigurāciju no pašreizējās programmas instances kā XML pakotni, kuru var glabāt lokāli vai LCS.
    - Pārveidot ER konfigurāciju par programmas dokumenta veidni.
    - Importēt XML pakotni, kas tiek glabāta lokāli vai LCS pašreizējā instancē.

- Pielāgot elektroniskā dokumenta veidni:

    - Pārnest veidni no LCS uz pašreizējo instanci kā ER konfigurāciju.
    - Izveidot ER konfigurācijas pielāgotu versiju un saglabāt atsauci uz tās bāzes versiju.

- Integrēt veidni noteiktā biznesa procesā, lai tā būtu pieejama programmā:

    - Konfigurēt iestatījumus, lai programma sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā. Piemēram, ietveriet atsauci uz ER konfigurāciju noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.

- Izmantot veidni noteiktā biznesa procesā:

    - Izpildīt ER konfigurāciju konkrētā biznesa procesā. Piemēram, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu, ja ir atlasīta maksājumu metode ar atsauci uz ER konfigurāciju.

## <a name="concepts"></a>Koncepcijas
Ar ER konfigurācijas dzīves ciklu ir saistītas tālāk norādītās lomas un saistītās darbības.

| Loma                                       | Aktivitātes                                                      | Apraksts |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektronisko pārskatu veidošanas funkcionālais konsultants | Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).           | Biznesa procesos iesaistīta persona, kura izstrādā ER domēnam specifiskos datu modeļu, izstrādā nepieciešamās elektronisko dokumentu veidnes un atbilstoši tās saista. |
| Elektroniskā pārskata izstrādātājs             | Izveidojiet un pārvaldiet datu modeļu kartējumus.                          | Dynamics AX speciālists, kurš atlasa nepieciešamos Finance datu avotus un saista tos ar ER domēnam specifiskiem datu modeļiem. |
| Uzskaites supervizors                      | Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem. | Piemēram, loma **Uzskaites supervizors**, kas sniedz iespēju ER konfigurācijas iestatījumus izmantot noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu. |
| Kreditoriem maksājamo rēķinu darbinieks            | Izmantot ER artefaktus noteiktā biznesa procesā.                | Piemēram, loma **Kreditoriem maksājamo rēķinu darbinieks**, kas sniedz iespēju ģenerēt rēķinu apstrādes elektroniskos maksājumu ziņojumus, pamatojoties uz ER formātu, kas ir konfigurēts noteiktai maksājumu metodei. |

## <a name="er-configuration-development-lifecycle"></a>ER konfigurācijas izstrādes dzīves cikls
Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķā Finance and Operations instancē:

- Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un instances izmantošanas veiktspējai.
- Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo ieejas punkti un reģistrēts uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

Izstrādes vidē izstrādātās ER konfigurācijas var augšupielādēt testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale). Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus. Visbeidzot apstiprinātās ER konfigurācijas var augšupielādēt LCS, kur tās var koplietot ar pakalpojumu abonentiem, vai ražošanas vidē iekšējai lietošanai, kā tas ir redzams tālāk esošajā attēlā.

![ER konfigurācijas dzīves cikls](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]