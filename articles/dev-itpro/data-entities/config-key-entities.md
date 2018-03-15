---
title: "Konfigurācijas atslēgas un datu elementi"
description: "Šajā tēmā ir aprakstītas attiecības starp konfigurācijas atslēgām un datu elementiem programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: f9ea932b48d57baad4b4ab66069191ebd7cbbd6c
ms.contentlocale: lv-lv
ms.lasthandoff: 02/27/2018

---

# <a name="configuration-keys-and-data-entities"></a>Konfigurācijas atslēgas un datu elementi

[!include[banner](../includes/banner.md)]

Pirms izmantojat datu elementus datu importēšanai vai eksportēšanai, vispirms ieteicams noteikt konfigurācijas atslēgu ietekmi uz tiem datu elementiem, ko plānojat lietot. 

Lai uzzinātu vairāk par konfigurācijas atslēgām programmā Finance and Operations, skatiet rakstu [Pārskats par licenču kodiem un konfigurācijas atslēgām](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Konfigurācijas atslēgu piešķires
Konfigurācijas atslēgas var piešķirt vienam vai visiem tālāk norādītajiem artefaktiem.
-   Datu elementi
-   Tabulas, kas lietotas kā datu avoti
-   Tabulas lauki
-   Datu elementu lauki

Tālāk esošajā tabulā sniegts kopsavilkums par to, kā konfigurācijas atslēgu vērtības dažādos artefaktos, kas ir objekta pamatā, maina paredzēto objekta uzvedību.

| Konfigurācijas atslēgas iestatījums datu elementā | Konfigurācijas atslēgas iestatījums tabulā | Konfigurācijas atslēgas iestatījums tabulas laukā | Konfigurācijas atslēga datu elementa laukā | Paredzētā uzvedība                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------|-----------------------------|-----------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deaktivizēts                          | Nav novērtēts               | Nav novērtēts                     | Nav novērtēts                   | Ja būs deaktivizēta datu elementa konfigurācijas atslēga, datu elements nebūs funkcionāls. Nav svarīgi, vai konfigurācijas atslēgas pamata tabulās un laukos ir aktivizētas vai deaktivizētas.                                                                                                                                                                                                                                                                                                                                          |
| Aktivizēts                           | Deaktivizēts                    | Nav novērtēts                     | Nav novērtēts                   | Ja ir aktivizēta datu elementa konfigurācijas atslēga, datu pārvaldības platforma pārbauda konfigurācijas atslēgu katrā no pamata tabulām. Ja būs deaktivizēta tabulas konfigurācijas atslēga, šī tabula nebūs pieejama datu elementā funkcionālai lietošanai. Ja ir deaktivizēta tabulas konfigurācijas atslēga, tabulas un datu elementa konfigurācijas atslēgas iestatījumi netiek novērtēti. Ja elementa primārajai tabulai būs deaktivizēta tās konfigurācijas atslēga, sistēma rīkosies tā, it kā elementa konfigurācijas atslēga būtu deaktivizēta. |
| Aktivizēts                           | Aktivizēts                     | Deaktivizēts                          | Nav novērtēts                   | Ja būs aktivizēta datu elementa konfigurācijas atslēga un būs aktivizētas pamata tabulu konfigurācijas atslēgas, datu pārvaldības platforma pārbaudīs konfigurācijas atslēgas tabulu laukos. Ja būs deaktivizēta lauka konfigurācijas atslēga, šis lauks nebūs pieejams datu elementā funkcionālai lietošanai pat tad, ja atbilstošajam datu elementa laukam būs aktivizēta konfigurācijas atslēga.                                                                                                                                   |
| Aktivizēts                           | Aktivizēts                     | Aktivizēts                           | Deaktivizēts                        | Ja konfigurācijas atslēga būs aktivizēta visos citos līmeņos, bet elementa lauka konfigurācijas atslēga nebūs aktivizēta, šis lauks nebūs pieejams lietošanai datu elementā.                                                                                                                                                                                                                                                                                                                                                                          |

> [!NOTE]
> Ja elementam cits elements darbojas kā datu avots, iepriekš aprakstītā semantika tiek lietota rekursīvā veidā.

### <a name="entity-list-refresh"></a>Elementu saraksta atsvaidzināšana
Kad ir atsvaidzināts elementu saraksts, datu pārvaldības platforma veido konfigurācijas atslēgas metadatus izpildlaika lietošanai. Šie metadati tiek veidoti, izmantojot iepriekš aprakstīto loģiku. Pirms darbu un elementu izmantošanas datu pārvaldības platformā ir ļoti ieteicams nogaidīt, kamēr ir pabeigta elementu saraksta atsvaidzināšana. Pretējā gadījumā, iespējams, konfigurācijas atslēgas metadati nebūs atjaunināti un tiks iegūti negaidīti rezultāti. Kad tiek atsvaidzināts elementu saraksts, elementu saraksta lapā tiek parādīts tālāk norādītais ziņojums.

![Elementu saraksta atsvaidzināšana](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Datu elementu saraksta lapa
Datu pārvaldības darbvietā esošajā datu elementu saraksta lapā ir parādīti elementu konfigurācijas atslēgu iestatījumi. Sāciet darbu šajā lapā, lai izprastu, kā konfigurācijas atslēgas ietekmē datu elementu.
Šī informācija tiek parādīta, izmantojot metadatus, kas veidoti elementu atsvaidzināšanas laikā. Konfigurācijas atslēgas kolonnā parādīts ar datu elementu saistītās konfigurācijas atslēgas nosaukums. Ja šī kolonna ir tukša, tas nozīmē, ka ar datu elementu nav saistīta neviena konfigurācijas atslēga. Konfigurācijas atslēgas statusa kolonnā parādīts konfigurācijas atslēgas statuss. Ja tajā ir ievietota atzīme, tas nozīmē, ka šī atslēga ir aktivizēta. Ja tā ir tukša, tas nozīmē, ka atslēga ir deaktivizēta vai arī nav nevienas saistītas atslēgas.

![Elementu saraksta lapa](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Mērķa lauki
Nākamā darbība ir detalizēti aplūkot datu elementu, lai skatītu konfigurācijas atslēgu ietekmi uz tabulām un laukiem. Datu elementa mērķa lauku formā parādīta konfigurācijas atslēga un atslēgas statusa informācija saistītajām tabulām un laukiem datu elementā.  Ja pašam datu elementam ir deaktivizēta tā konfigurācijas atslēga, tiek parādīts brīdinājuma ziņojums ar informāciju par to, ka šī elementa mērķa lauku formā esošās tabulas un lauki nebūs pieejami neatkarīgi no to konfigurācijas atslēgas statusa.

![Mērķa lauki](./media/Target_fields_1.png)

### <a name="child-entities"></a>Bērnelementi 
Noteiktiem elementiem citi elementi darbojas kā datu avoti vai arī tie ir salikti datu elementi — šo elementu konfigurācijas atslēgas informācija ir parādīta formā Bērnelementi. Lietojiet šo formu līdzīgi kā iepriekš aprakstīto elementu saraksta lapu. Arī bērnelementu mērķa lauku formas uzvedība ir līdzīga iepriekš aprakstītajai.

![Mērķa lauki](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Datu elementu lietošana
Kad ir iegūta pilnīga izpratne par konfigurācijas atslēgu ietekmi uz datu elementiem, ko vēlaties lietot, varat izmantot datu elementus, pievienojot tos datu projektiem. 

### <a name="run-time-validations-for-configuration-keys"></a>Izpildes laika pārbaudes konfigurācijas atslēgām
Izmantojot elementu saraksta atsvaidzināšanas laikā veidotos konfigurācijas atslēgas metadatus, tālāk norādītajos gadījumos tiek veiktas izpildes laika pārbaudes.

-   Kad darbam tiek pievienots datu elements

-   Kad lietotājs elementu sarakstā noklikšķina uz Validēt

-   Kad lietotājs datu projektā ielādē datu pakotni

-   Kad lietotājs datu projektā ielādē veidni

-   Kad tiek ielādēts esošs datu projekts

-   Kad datu projektā tiek ielādēta veidne

-   Pirms eksportēšanas/importēšanas darba izpildes (pakešuzdevuma, darba, kas nav pakešuzdevums, periodiska, OData darba)

-   Kad lietotājs izveido kartējumu

-   Kad lietotājs kartē laukus kartēšanas lietotāja interfeisā

-   Kad lietotājs pievieno tikai importējamus laukus


### <a name="managing-configuration-key-changes"></a>Konfigurācijas atslēgas izmaiņu pārvaldība
Ikreiz, kad atjaunināt konfigurācijas atslēgas elementa, tabulas vai lauka līmenī, ir jāatsvaidzina elementu saraksts datu pārvaldības platformā. Šis process nodrošina, ka platforma paņem jaunākos konfigurācijas atslēgas iestatījumus. Kamēr nebūs atsvaidzināts elementu saraksts, elementu saraksta lapā tiks rādīts tālāk norādītais brīdinājums. Atjauninātās konfigurācijas atslēgas izmaiņas stāsies spēkā nekavējoties pēc elementu saraksta atsvaidzināšanas. Ieteicams validēt esošos datus projektus un darbus, lai nodrošinātu, ka pēc konfigurācijas atslēgu izmaiņu stāšanās spēkā tie darbojas, kā paredzēts.

![Mērķa lauki](./media/Target_fields_3.png)


