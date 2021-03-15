---
title: Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management
description: Šajā tēmā ir paskaidrots, kā izdot elektronisko rēķinus programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104409"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir paskaidrots, kā izdot elektronisko rēķinus programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.


## <a name="feature-activation"></a>Līdzekļu aktivizēšana

Lai sāktu elektronisko rēķinu izdošanu, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu, jāaktivizē funkcionalitātes atsauce programmās Finance un Supply Chain Management.

Katra funkcionalitātes atsauce atbilst noteiktai elektronisko rēķinu izrakstīšanas funkcijai, kas atbilst valsts/reģiona elektronisko rēķinu izrakstīšanas prasībām.

Šajā tabulā ir parādīts saraksts ar funkcionalitātes atsaucēm, ko atbalsta elektronisko rēķinu izrakstīšanas pievienojumprogramma.

| Līdzekļa atsauce | Vārds, uzvārds                                              | Valsts/reģions |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e Federal — Brazīlijas elektroniskais rēķins       | Brazīlija         |
| BR-00095          | NFS-e Brazīlijas elektroniskie rēķini               | Brazīlija         |
| DK-00001          | E-rēķini publiskajam sektoram (OIOUBL) - DK    | Dānija        |
| EG-00008          | E-rēķinu izrakstīšana Ēģiptei                             | Ēģipte          |
| ES-00025          | Elektroniskais rēķins publiskajam sektoram           | Spānija          |
| EUR-00023         | Eiropas Savienības e-rēķini publiskajam sektoram       | Eiropa         |
| ITA-00036         | IT - E-rēķinu izrakstīšana publiskajam sektoram (FatturaPA) | Itālija          |
| MX-00010          | E-rēķinu izrakstīšana CFDI                                  | Meksika         |
| MX-00016          | E-rēķinu izrakstīšana CFDI — atcelšanas process           | Meksika         |

Gadījumos, kad ir mantojuma elektronisko rēķinu izrakstīšanas funkcija, tiek atbalstīta valsts lokalizāciju tvērums, funkcionalitātes atsauces aktivizēšana ļauj izdot elektroniskos rēķinus, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu, un izslēdz iepriekšējo funkciju.

## <a name="submit-electronic-documents"></a>Iesniegt elektroniskos dokumentus

Elektronisko dokumentu iesniegšanas process ir viens saziņas punkts starp Finance un Supply Chain Management un Elektronisko rēķinu izrakstīšanas pievienojumprogrammu. Katra iesniegšanas notikuma laikā sakaru plūsma ir abos virzienos:

- **No Finance un Supply Chain Management uz Elektronisko rēķinu izrakstīšanas pievienojumprogrammu** - Finance un Supply Chain Management sūta abstraktos rēķinus elektronisko rēķinu pievienojumprogrammai. Pēc vajadzības tie nosūta arī mainīgo saturus, kas tika konfigurēti, kā daļa no elektronisko rēķinu izrakstīšanas funkcijām.
- **No Elektronisko rēķinu izrakstīšanas pievienojumprogrammas uz Finance un Supply Chain Management** – atkarībā no elektronisko rēķinu izrakstīšanas funkcijas, Finance un Supply Chain Management saņem atjauninājumus no Elektronisko rēķinu izrakstīšanas pievienojumprogrammas par iepriekš iesniegto rēķinu apstrādes rezultātiem. Tie saņem arī mainīgo saturus, kas tika konfigurēti, kā daļa no elektronisko rēķinu izrakstīšanas funkcijām.

Lai iesniegtu elektroniskos dokumentus Elektronisko rēķinu izrakstīšanas pievienojumprogrammai, Finance un Supply Chain Management dodieties uz **Organizācijas administrēšana &gt; Periodiskie &gt; Elektroniskie dokumenti &gt; Iesniegt elektroniskos dokumentus**.

Sākums ir grāmatots rēķins. Šis rēķins var būt no dažādiem nosaukumiem, piemēram, pārdošanas pasūtījumiem, projekta rēķiniem vai brīva teksta rēķiniem.

Iesniegšanas procesu var palaist manuāli vai fonā.

- **Manuāla izpilde** - manuālai izpildei jums ir jāizmanto **Filtra** opcija, lai definētu iesniedzamo dokumentu diapazonu. **Filtru** lapā varat konfigurēt savu vaicājumu, lai atlasītu iesniedzamos iegrāmatotos rēķinus. Kad atlase ir veikta, manuāli jāsāk apstrādes izpilde un jāgaida, kamēr tā beidzas. Kad apstrāde ir pabeigta, ziņojums darbību centrā rāda elektronisko dokumentu skaitu, kas ir veiksmīgi iesniegti.
- **Fona izpilde** – fona izpilde tiek veikta bez pieteikšanās pieprasījuma vai arī saglabājiet iesniegšanas dialoglodziņu atvērtu. Varat plānot procesu, lai palaistu un noteiktu izpildes biežumu.

## <a name="view-the-submission-logs"></a>Skatīt iesniegšanas žurnālus

Pakalpojumos Finance un Supply Chain Management jūs varat izmantot iesniegšanas žurnālus, lai aplūkotu iesniegšanas procesa rezultātus Elektronisko rēķinu izrakstīšanas pievienojumprogrammā. Dodieties uz **Organizācijas administrēšana &gt; Periodiski &gt; Elektroniskie dokumenti &gt; Elektronisko dokumentu iesniegšana** un pēc tam laukā **Dokumenta tips** atlasiet vērtību, lai filtrētu rēķinu tipu, ko rāda žurnāli.

Pastāv trīs iespējamie iesniegšanas statusi:

- **Plānots** - Elektronisko rēķinu izrakstīšanas pievienojumprogramma saņemta no Finance un Supply Chain Management, kā arī notiek elektronisko rēķinu izrakstīšanas līdzekļa apstrāde.
- **Pabeigts** – Elektronisko rēķinu izrakstīšanas pievienojumprogramma veiksmīgi apstrādāja elektronisko rēķinu izrakstīšanas funkciju, it kā tā būtu konfigurēta tās palaišanai.
- **Neizdevās** - Elektronisko rēķinu izrakstīšanas pievienojumprogramma konstatēja kļūdu, vai tā tika apturēta ar izņēmumu Elektronisko rēķinu izrakstīšanas funkcijas apstrādes laikā.

> [!IMPORTANT]
> Iesniegšanas statuss attiecas uz apstrādes statusu, ko Elektronisko rēķinu izrakstīšanas pievienojumprogramma veic uz elektronisko rēķinu izrakstīšanas līdzekli. Tam nav atsauces uz elektroniskā rēķina beigu statusu.
>
> Piemēram, ja ārējā tīmekļa pakalpojumā ir jāiesniedz elektroniskais rēķins apstiprināšanai, iesniegšanas statuss varētu būt **Pabeigts**, bet elektroniskā rēķina statuss varētu būt **Noraidīts**. Šajā gadījumā Elektronisko rēķinu izrakstīšanas pievienojumprogramma veiksmīgi apstrādāja elektronisko rēķinu izrakstīšanas funkciju, it kā tā būtu konfigurēta tās apstrādei. Tomēr elektroniskais rēķins tika noraidīts, jo tas neatbilst kritērijiem, ar kuriem tīmekļa pakalpojums tika izveidots rēķina apstiprināšanai.

Iesniegšanas žurnālos ir iekļautas šādas papildu funkcijas:

- **Papildinformācija par iesniegšanu** – skatīt detalizētu informāciju par galveno iesniegšanu. Vizualizēšana parāda pilnīgu izpildes žurnālu darbībām, kas ir konfigurētas elektronisko rēķinu izrakstīšanas līdzeklī. Tas arī ļauj lietotājiem lejupielādēt failus, kas tiek izveidoti apstrādes laikā. Scenārijos, kuros rēķinu jāapstiprina ārējam tīmekļa pakalpojumam, tas ļauj lietotājiem skatīt rēķina statusu.
- **Saistītās iesniegšanas** - skatīt detalizētu informāciju par pakārtotajām iesniegšanām.
- **Atcelt iesniegšanas** – šī funkcija iespējo īpašu iesniegšanas procesu scenārijos, kuros elektroniskais rēķins jāapstiprina ārējam tīmekļa pakalpojumam. Tas sniedz norādījumus Elektronisko rēķinu izrakstīšanas pakalpojumam nosūtīt īpašu ziņojumu, kas paredzēts apstiprināta elektroniskā rēķina statusa atcelšanai tīmekļa pakalpojuma datu bāzē.
- **Atkārtoti iesniegt dokumentu** - atkārtoti iesniedziet elektronisko dokumentu, kas jau ir iesniegts elektronisko rēķinu izrakstīšanas pievienojumprogrammā. **Iesniegšanas informācijas** lapā tiek izveidots pilnīgi jauns žurnāls.
- **Sūtīt saistīto iesniegumu**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]