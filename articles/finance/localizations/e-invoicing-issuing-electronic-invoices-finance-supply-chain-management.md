---
title: Elektronisko rēķinu izsniegšana pakalpojumā Finance un Supply Chain Management
description: Šajā rakstā skaidrots, kā izsniegt elektroniskos rēķinus Microsoft Dynamics 365 Finanšu un elektronisko Dynamics 365 Supply Chain Management rēķinu izrakstīšanai.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 465aea4eda3cbb023f7e222ba51553654131c0c7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864184"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektronisko rēķinu izsniegšana pakalpojumā Finance un Supply Chain Management

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā izsniegt elektroniskos rēķinus Microsoft Dynamics 365 Finanšu un elektronisko Dynamics 365 Supply Chain Management rēķinu izrakstīšanai.


## <a name="feature-activation"></a>Līdzekļu aktivizēšana

Lai izsniegtu elektronisko rēķinu, izmantojot Elektronisko rēķinu izrakstīšanu, jāaktivizē līdzeklis programmās Finance un Supply Chain Management.

Katrs līdzeklis atbilst noteiktai elektronisko rēķinu izrakstīšanas funkcijai, kas atbilst valsts/reģiona elektronisko rēķinu izrakstīšanas prasībām.

Tabulā zemāk ir parādīts saraksts ar līdzekļiem, ko Elektronisko rēķinu izrakstīšana var atbalstīt.

| Nosaukums/vārds, uzvārds                                              | Valsts/reģions |
|---------------------------------------------------|----------------|
|Austrijas elektroniskais rēķins                        |Austrija         |
|Beļģijas elektroniskais rēķins                         |Beļģija         |
|NF-e Federal — Brazīlijas elektroniskais rēķins       |Brazīlija          |
|NFS-e — Brazīlijas pakalpojumu (pilsētas) elektroniskais rēķins|Brazīlija          |
|Dānijas elektroniskais rēķins                          |Dānija         |
|Ēģiptes elektroniskais rēķins                        |Ēģipte           |
|Igaunijas elektroniskais rēķins                        |Igaunija         |
|Somijas elektroniskais rēķins                         |Somija         |
|Francijas elektroniskais rēķins                          |Francija          |
|Vācijas elektroniskais rēķins                          |Vācija         |
|PEPPOL — globāls elektroniskais rēķins                 |Globāls          |
|Itālijas elektroniskais rēķins                         |Itālija           |
|CFDI — Meksikas elektroniskais rēķins                  |Meksika          |
|Nīderlandes elektroniskais rēķins                           |Nīderlande     |
|Norvēģijas elektroniskais rēķins                       |Norvēģija          |
|Spānijas elektroniskais rēķins                         |Spānija           |

Kad ir mantojuma Elektronisko rēķinu izrakstīšanas līdzeklis, kas tiek atbalstīts valsts/reģiona lokalizāciju tvērumā, viena no šo līdzekļu aktivizēšana izslēdz mantojuma līdzekli un iespējo elektroniskos rēķinu izsniegšanu, izmantojot Elektronisko rēķinu izrakstīšanu.

> [!IMPORTANT]
> Pēc Elektronisko rēķinu izrakstīšanas integrācijas funkcijas iespējošanas jaunā Elektronisko rēķinu izrakstīšanas pieredze pēc noklusējuma tiek izslēgta. Varat izmantot šo līdzekļu koncepciju, lai izvēles veidā iespējotu jaunu pieredzi juridiskām personām, izmantojot valstij/reģionam specifisku funkcionalitāti. Opcija **Globāli** kontrolē jauno pieredzi pārējiem apgabaliem/reģioniem, kas nav īpaši norādīti tabulā.

## <a name="submit-electronic-documents"></a>Iesniegt elektroniskos dokumentus

Elektronisko dokumentu iesniegšanas process ir viens saziņas punkts starp Finance un Supply Chain Management un Elektronisko rēķinu izrakstīšanu. Katra iesniegšanas notikuma laikā sakaru plūsma ir abos virzienos:

- **No Finance un Supply Chain Management uz Elektronisko rēķinu izrakstīšanu** - Finance un Supply Chain Management sūta abstraktos rēķinus elektronisko rēķinu izrakstīšanai. Pēc vajadzības tie nosūta arī mainīgo saturus, kas tika konfigurēti, kā daļa no elektronisko rēķinu izrakstīšanas funkcijām.
- **No Elektronisko rēķinu izrakstīšanas uz Finance un Supply Chain Management** – atkarībā no elektronisko rēķinu izrakstīšanas funkcijas, Finance un Supply Chain Management saņem atjauninājumus no Elektronisko rēķinu izrakstīšanas par iepriekš iesniegto rēķinu apstrādes rezultātiem. Tie saņem arī mainīgo saturus, kas tika konfigurēti, kā daļa no elektronisko rēķinu izrakstīšanas funkcijām.

Lai iesniegtu elektroniskos dokumentus Elektronisko rēķinu izrakstīšanai, Finance un Supply Chain Management dodieties uz **Organizācijas administrēšana &gt; Periodiskie &gt; Elektroniskie dokumenti &gt; Iesniegt elektroniskos dokumentus**.

Sākums ir grāmatots rēķins. Šis rēķins var būt no dažādiem nosaukumiem, piemēram, pārdošanas pasūtījumiem, projekta rēķiniem vai brīva teksta rēķiniem.

Iesniegšanas procesu var palaist manuāli vai fonā.

- **Manuāla izpilde** - manuālai izpildei jums ir jāizmanto **Filtra** opcija, lai definētu iesniedzamo dokumentu diapazonu. **Filtru** lapā varat konfigurēt savu vaicājumu, lai atlasītu iesniedzamos iegrāmatotos rēķinus. Kad atlase ir veikta, manuāli jāsāk apstrādes izpilde un jāgaida, kamēr tā beidzas. Kad apstrāde ir pabeigta, ziņojums darbību centrā rāda elektronisko dokumentu skaitu, kas ir veiksmīgi iesniegti.
- **Fona izpilde** – fona izpilde tiek veikta bez pieteikšanās pieprasījuma vai arī saglabājiet iesniegšanas dialoglodziņu atvērtu. Varat plānot procesu, lai palaistu un noteiktu izpildes biežumu.

## <a name="view-the-submission-logs"></a>Skatīt iesniegšanas žurnālus

Pakalpojumos Finance un Supply Chain Management jūs varat izmantot iesniegšanas žurnālus, lai aplūkotu iesniegšanas procesa rezultātus Elektronisko rēķinu izrakstīšanā. Dodieties uz **Organizācijas administrēšana &gt; Periodiski &gt; Elektroniskie dokumenti &gt; Elektronisko dokumentu iesniegšana** un pēc tam laukā **Dokumenta tips** atlasiet vērtību, lai filtrētu rēķinu tipu, ko rāda žurnāli.

Pastāv trīs iespējamie iesniegšanas statusi:

- **Plānots** - Elektronisko rēķinu izrakstīšana saņemta no Finance un Supply Chain Management, kā arī notiek elektronisko rēķinu izrakstīšanas līdzekļa apstrāde.
- **Pabeigts** – Elektronisko rēķinu izrakstīšana veiksmīgi apstrādāja elektronisko rēķinu izrakstīšanas funkciju, it kā tā būtu konfigurēta tās palaišanai.
- **Neizdevās** - Elektronisko rēķinu izrakstīšana konstatēja kļūdu, vai tā tika apturēta ar izņēmumu Elektronisko rēķinu izrakstīšanas funkcijas apstrādes laikā.

> [!IMPORTANT]
> Iesniegšanas statuss attiecas uz apstrādes statusu, ko Elektronisko rēķinu izrakstīšana veic uz elektronisko rēķinu izrakstīšanas līdzekli. Tam nav atsauces uz elektroniskā rēķina beigu statusu.
>
> Piemēram, ja ārējā tīmekļa pakalpojumā ir jāiesniedz elektroniskais rēķins apstiprināšanai, iesniegšanas statuss varētu būt **Pabeigts**, bet elektroniskā rēķina statuss varētu būt **Noraidīts**. Šajā gadījumā Elektronisko rēķinu izrakstīšana veiksmīgi apstrādāja elektronisko rēķinu izrakstīšanas funkciju, it kā tā būtu konfigurēta tās apstrādei. Tomēr elektroniskais rēķins tika noraidīts, jo tas neatbilst kritērijiem, ar kuriem tīmekļa pakalpojums tika izveidots rēķina apstiprināšanai.

Iesniegšanas žurnālos ir iekļautas šādas papildu funkcijas:

- **Papildinformācija par iesniegšanu** – skatīt detalizētu informāciju par galveno iesniegšanu. Vizualizēšana parāda pilnīgu izpildes žurnālu darbībām, kas ir konfigurētas elektronisko rēķinu izrakstīšanas līdzeklī. Tas arī ļauj lietotājiem lejupielādēt failus, kas tiek izveidoti apstrādes laikā. Scenārijos, kuros rēķinu jāapstiprina ārējam tīmekļa pakalpojumam, tas ļauj lietotājiem skatīt rēķina statusu.
- **Saistītās iesniegšanas** - skatīt detalizētu informāciju par pakārtotajām iesniegšanām.
- **Atcelt iesniegšanas** – šī funkcija iespējo īpašu iesniegšanas procesu scenārijos, kuros elektroniskais rēķins jāapstiprina ārējam tīmekļa pakalpojumam. Tas sniedz norādījumus Elektronisko rēķinu izrakstīšanai nosūtīt īpašu ziņojumu, kas paredzēts apstiprināta elektroniskā rēķina statusa atcelšanai tīmekļa pakalpojuma datu bāzē.
- **Atkārtoti iesniegt dokumentu** - atkārtoti iesniedziet elektronisko dokumentu, kas jau ir iesniegts elektronisko rēķinu izrakstīšanā. Lapā **Iesniegšanas informācijas** tiek izveidots jauns žurnāls.
- **Sūtīt saistīto iesniegumu**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
