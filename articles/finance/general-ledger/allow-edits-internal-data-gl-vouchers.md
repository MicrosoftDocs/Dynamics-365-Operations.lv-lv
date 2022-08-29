---
title: Atļaut virsgrāmatas dokumentu iekšējo datu rediģēšanu
description: Šajā rakstā ir sniegta informācija, kā rediģēt Virsgrāmatas dokumentu iekšējos datus.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220719"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Atļaut virsgrāmatas dokumentu iekšējo datu rediģēšanu

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Grāmatojot grāmatvedības ierakstus Virsgrāmatā, lauks **Apraksts** bieži tiek izmantots, lai glabātu iekšējās piezīmes vai dokumentāciju. Ja informācija nav pareiza, tā var radīt sajukumus un apgrūtināt perioda beigu slēgšanu. Šis līdzeklis ļauj grāmatvedības pārvaldniekam vai uzskaites supervizoram **labot** kļūdas, rediģējot virsgrāmatas grāmatoto dokumentu lauku Apraksts.

Virsgrāmatā grāmatoto dokumentu izmaiņas ir ierobežotas ar datiem, kas pēc rakstura ir iekšēji. Šī funkcija nekad neļaus jums labot tādus datus kā summas, grāmatošanas datumus, Virsgrāmatas kontus un darbības valūtu. Šo datu izmaiņas ietekmēs finanšu pārskatu ārējos pārskatus un tās jāveic tikai ar jaunu Virsgrāmatas dokumentu palīdzību.

> [!NOTE]
> Dynamics 365 finanšu versijai 10.0.29 šis līdzeklis ir ierobežots **ar labojumiem laukā** Apraksts.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Rediģēt Virsgrāmatas dokumentu iekšējos datus

Pirms Virsgrāmatas dokumentu rediģēšanas **ir jāiespējo funkcija Atļaut rediģēšanu virsgrāmatas dokumentu iekšējos** **datos līdzekļu pārvaldības darbvietā**.
Kad funkcija ir aktivizēta, grāmatvedības vadītāja vai uzskaites supervizora lomai ir jāpiešķir lietotājs, kurš rediģēs grāmatotos dokumentus. Atļaujas var pievienot arī citām lomām, pielāgojot drošības lomas.

Rediģēšanas process ir atļauts tikai no dokumentu darbību lapas.

1. Dodieties uz **Virsgrāmatas** > **vaicājumiem un pārskatiem** > **Dokumentu darbības**.
2. **Dialoglodziņā SysQuery** ievadiet meklēšanas kritērijus, lai atlasītu dokumentus.
3. Atlasiet dokumenta rindas, kuras vēlaties labot, un pēc tam atlasiet Labot dokumenta **rediģēšanas** > **iekšējos dokumenta datus**.

    [![Dokumentu darbību lapa](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Lapā Labot **iekšējos dokumenta datus** katrai atlasītajai rindai tiek rādīti šādi dati:
  
  - Virsgrāmatas konts
  - Konta nosaukums
  - Dokuments
  - Pašreizējais apraksts
  - Jauns apraksts

    [![Žurnāla dokuments.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Var rediģēt **tikai** lauku Jauns apraksts. Pēc noklusējuma vērtība atbilst vērtībai pašreizējā apraksta **laukā**, lai varētu ātri izlabot nelielas kļūdas aprakstā.

4. Modificējiet **lauku Jauns** apraksts katrā rindā vai dzēsiet aprakstu no katras rindas.

   Vai arī, ja vairākas rindas jāatjaunina ar vienu un to pašu vērtību, rīkojieties šādi:

      1. Atlasiet rediģējamās rindas un pēc tam atlasiet Lielapjoma **atjaunināšana atlasītos ierakstus**.
      2. Laukā **Labot lauku** atlasiet lauku rediģēšanai. Pašlaik uzmeklēšana ietver tikai lauku **Jauns** apraksts.
      3. Laukā **Jauna** vērtība ievadiet jaunu aprakstu.
      4. Atlasiet **Atjaunināt**. Visi atlasītie ieraksti tiek atjaunināti ar jaunu vērtību.

      [![Veikt atlasīto ierakstu lielapjoma atjaunināšanas dialoglodziņu.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Laukā **Rediģēšanas iemesls** ievadiet piezīmi, lai paskaidrotu, kāpēc labošana tika veikta. Šī piezīme tiek parādīta dokumenta **rediģēšanas lapas Audita pierakstos**.

   Vienā dokumentā var veikt vairākus rediģējumus, un katra rediģēšana tiks izsekota.

## <a name="audit-trail-of-voucher-edits"></a>Dokumenta rediģējumu auditācijas pieraksti

Auditācijas pieraksti tiek uzturēti īpaši, lai izsekotu izmaiņas, kas veiktas, izmantojot šo funkciju. Dokumentu audita pārbaudes variet piekļūt diviem veidiem:

  - Dodieties uz **Virsgrāmatas** > **vaicājumiem un pārskatiem** > **Dokumentu darbības**. Dokumenta uzziņu **lapā atlasiet** Labot **dokumentu** > **audita pārbaudes dokumentu rediģēšanu**. Auditācijas pieraksti tiek rādīti tikai atlasītajam dokumenta ierakstam. 
   
    Šādā veidā atverot vaicājumu, varat fokusties uz visiem labojumiem, kas tika veikti vienam dokumenta ierakstam.
  
  - Dodieties uz** Virsgrāmatu** > **dokumentu** > **rediģēšanas periodisko uzdevumu audita pārbaudes.** Dialoglodziņā ievadiet kritērijus, lai norādītu dokumentus, kuriem vēlaties apskatīt rediģēšanas pierakstus. Lai apskatītu visu dokumentu audita pārbaudes, atstājiet kritērijus tukšus un atlasiet **Labi**. 
    
    Atverot šādu vaicājumu, varat filtrēt rediģējumus, kas veikti konkrētā datumā vai noteiktam lietotājam.

Redi **?ēšanas lapas auditācijas** pieraksti parāda sekojošo informāciju:

- **Izveides datums un laiks** – rediģēšanas datums un laiks.
- **Rediģēšanas iemesls** – pamatojums, kāpēc lietotājs ievadīja rediģēšanai.
- **Veidojis** – Lietotājs, kurš veicis rediģēšanu.

Lai apskatītu katra audita pieraksta detaļas, detalizētu informāciju par Izveidoto **datumu un laika** vērtību. Skata **rediģētā dokumenta rekvizītu lapa** parāda to pašu informāciju, kas oriģinālajai labošanas lapai, ieskaitot iepriekšējo aprakstu un atjaunināto aprakstu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
