---
title: Analītisku atskaišu izmantošana programmā Attract
description: Šajā tēmā ir aprakstīti analītiskie pārskati par darbā pieņemšanas procesa ieskatiem programmā Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461906"
---
# <a name="use-analytic-reports-in-attract"></a>Analītisku atskaišu izmantošana programmā Attract

[!include [banner](includes/banner.md)]

Analītiskie pārskati programmā Microsoft Dynamics 365 Talent: Attract nodrošina standarta komplektācijā (out-of-the-box — OOTB) iekļautu risinājumu darbā pieņemšanas procesa ieskatiem. Pieejamās funkcijas:

- **Darba analīze** — noklikšķiniet uz cilnes **Analīze** darba ietvaros, lai skatītu darba kandidātu rādītājus.
- **Analīzes centrmezgls:** — kreisajā navigācijas sadaļā noklikšķiniet uz **Analīze**, lai skatītu apkopotos rādītājus par visiem darbiem.
- **Lietotājam raksturīga drošība** — piekļuvi pārskatiem kontrolē Attract [loma](security-attract.md) un darba dalībnieka loma.
- **Šķērsfiltrēšana:** — lai skatītu citus rādītājus, kas filtrēti pēc atlasītajiem datiem, pārskatā noklikšķiniet uz vizuālajiem elementiem.

>[!NOTE] 
>- Šis līdzeklis pašreiz ir [priekšskatījumā](access-preview-feature.md). Lai to izmēģinātu, jums ir nepieciešams [**Visaptverošais darbā pieņemšanas papildinājums**](attract-comprehensive-hiring.md).
>- Visi publiskie priekšskatījuma pārskati tiek rādīti angļu valodā.
>- Pārskatu atsvaidzināšanas biežums: ik pēc 3 stundām. Pēdējais atsvaidzināšanas laiks (vietējā laika joslā) atrodas pārskata sākumā. Atsvaidzināšanas laiki ir aptuveni un mainās atkarībā no datu apjoma un resursu noslodzes jūsu reģionā.

## <a name="job-analytics"></a>Darba analīze

Pārskati Darba analīze ir atsevišķas vakances darbā pieņemšanas procesa momentuzņēmums.  Galvenie rādītāji:

- Aktīvie kandidāti pēc posma
- Kandidāta avots
- Kandidāta tips (iekšējs vai ārējs)

## <a name="analytics-hub"></a>Analīzes centrmezgls

Pārskatos Analīzes centrmezgls tiek apkopoti dažādu darbu dati, lai atklātu darbā pieņemšanas procesā esošās tendences. Programmā Attract ir iekļauti divi OOTB pārskati: Konveijera apkopojums un Piltuves analīze.

### <a name="pipeline-summary"></a>Konveijera apkopojums

Konveijera kopsavilkuma pārskatā tiek apkopoti dati par vakantām darba vietām. Galvenie rādītāji:

- Kandidāti visos darbos pēc posma
- Kandidāta avots
- Vakantās darba vietas pēc darba stāža līmeņa

### <a name="funnel-analysis"></a>Piltuves analīze

Piltuves analīzes pārskatā tiek apkopoti dati par darba vietām, kas ir slēgtas kā aizpildītas. Galvenie rādītāji:

- Laiks līdz pieņemšanai darbā
- Konvertēšanas rādītāji (uzvirzot kursoru)
- Piedāvājuma pieņemšanas koeficients

Piezīme. Lai visprecīzāķ noteikti laiku līdz pieņemšanai darbā, ir ieteicams izmantot līdzekli [Piedāvājumu pārvaldība](offer-setup.md), kas ir pieejams kā daļa no Visaptverošā darbā pieņemšanas papildinājuma.

>[!TIP] 
>Lai iegūtu papildu informāciju, mēģiniet virzīt kursoru virs vizuālajiem elementiem. Piemēram, virzot kursoru virs sadaļas **Aktīvie kandidāti** vizuālajiem materiāliem, tiek parādīts vidējais dienu skaits atsevišķā posmā. Analizējot šo informāciju, var gūt būtiskus ieskatus, lai samazinātu laiku līdz nolīgšanai un ļautu personāla atlases darbiniekiem koncentrēties uz veidiem, kā samazināt katram posmam veltīto laiku.

## <a name="user-specific-security"></a>Lietotājam raksturīga drošība

Programmas Attract pārskati ir pieejami Administrators, Lasīt visu, Personāla atlases darbinieks un Par pieņemšanu darbā atbildīgais vadītājs [lomām.](security-attract.md) Nepiešķirtajiem lietotājiem nav piekļuves nevienai analīzes pārskatu lapai (Darba analīze vai Analīzes centrmezgls).

Pārskatos Darba analīze tiek rādīti dati atlasītajam darbam. Pārskatos Analīzes centrmezgls tiek apkopoti dati par visiem darbiem, ko lietotājs var skatīt. Lietotājiem, kas lapā Darbi var skatīt gan Mani darbi, gan Visi darbi, pārskatos Analīzes centrmezgls ir pieejami šie paši skati.

## <a name="cross-filter"></a>Šķērsfiltrēšana

Viena no Power BI izcilajām īpašībām ir visu pārskata lapā esošo vizuālo elementu savstarpējā saistība. Ja atlasīsit datu punktu uz kāda vizuālā elementa, visi pārējie vizuālie elementi lapā, kurā ir šīs datu izmaiņas, pamatojoties uz šo atlasi. Uzziniet vairāk un aplūkojiet piemēru sadaļā [Kā vizuālie elementi veic šķērsfiltrēšanu Power BI pārskatā](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Eksportēt programmā Excel

Lai skatītu pārskata datus programmā Excel, varat noklikšķināt uz izvēlnes opcijas (trīs punkti) uz vizuālā elementa un atlasīt opciju **Eksportēt pamata datus**. Eksportētie dati tiks eksportēti kā filtrēti, respektējot lietotāja atļaujas programmā Attract. Papildinformāciju skatiet sadaļā [Datu eksportēšana no vizualizācijas](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
