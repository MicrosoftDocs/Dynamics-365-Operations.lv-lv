---
title: "ES ieraksta sertifikāti"
description: "Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) ierakstu sertifikātiem."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 415e8ec91f3968883cb4e7ece10d8a26782bac1b
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="eu-entry-certificates"></a>ES ievešanas sertifikāti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) ierakstu sertifikātiem.

Eiropas Savienības (ES) ieraksta sertifikātam varat veikt šādus uzdevumus:

-   Izveidot un izsniegt ES ieraksta sertifikātu kopā ar pavadzīmi vai debitora rēķinu par preču vai pakalpojumu piegādi uz ES valstīm/reģioniem.
-   Saņemt ES ieraksta sertifikātu, ko parakstījis ES debitors.
-   Augšupielādēt parakstīto ES ieraksta sertifikātu, kas ir saņemts no debitora vai no trešās puses, kura ir atbildīga par krājumu piegādi debitoram.
-   Piesaistīt augšupielādēto ES ieraksta sertifikātu debitora rēķinam.
-   Atjaunināt augšupielādētā ES ieraksta sertifikāta statusu.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Priekšnosacījums</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valsts/reģions</td>
<td>Juridiskās personas primārajai adresei ir jāatrodas ES dalībvalstī.</td>
</tr>
<tr class="even">
<td>Saistītie iestatīšanas uzdevumi</td>
<td><ul>
<li>Lapā <strong>Debitoru moduļa parametri</strong> atzīmējiet opcijas <strong>Iespējot ieraksta sertifikāta pārvaldību</strong> un <strong>Iespējot ieraksta sertifikāta izsniegšanu</strong>.</li>
<li>Lapā <strong>Debitori</strong>, kopsavilkuma cilnē <strong>Rēķins un piegāde</strong> atzīmējiet opciju <strong>Nepieciešams ieraksta sertifikāts</strong> , lai norādītu, ka ES ieraksta sertifikāts šim debitoram ir obligāts. Atzīmējiet opciju <strong>Izsniegt ieraksta sertifikātu</strong>, lai debitoram izdotu juridiskās personas ES ieraksta sertifikātu.</li>
<li>Lapā <strong>Debitoru moduļa parametri</strong> atzīmējiet numuru secības kodu atsaucei <strong>Ieraksta sertifikāts</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Saistītās transakcijas</td>
<td><ul>
<li>Izveidojiet debitora kontu.</li>
<li>Izveidojiet pārdošanas pasūtījumu.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>ES ieraksta sertifikāta izveidošana, reģistrēšana un augšupielādēšana
ES ieraksta sertifikātu var izveidot automātiski vai manuāli. ES ieraksta sertifikāts tiek izveidots un izdrukāts automātiski, kad pavadzīmi vai rēķinu debitoram grāmatojat, izmantojot lapu **Pavadzīmes grāmatošana** vai **Rēķina grāmatošana**. Lai ES ieraksta sertifikātu izveidotu vai atkārtoti drukātu manuāli, izmantojiet lapu **Rēķinu žurnāls**. Turklāt varat izmantot lapu **Ierakstu sertifikātu žurnāls**, lai ievadītu detalizētu informāciju par ES ieraksta sertifikātu, ko izsniedza trešā puse.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>ES ieraksta sertifikātu automātiska vai manuāla izveidošana

ES ieraksta sertifikātu varat izveidot automātiski, izmantojot pavadzīmi lapā **Visi pārdošanas pasūtījumi** vai izmantojot rēķinu lapā **Pārdošanas pasūtījums**. Lai ES ieraksta sertifikātu izveidotu manuāli, varat lietot rēķinu lapā **Rēķinu žurnāls**. Taču pirms ES ieraksta sertifikāta manuālas izveidošanas ir jāmaina rēķina sertifikācijas statuss.

### <a name="registering-an-eu-entry-certificate"></a>ES ieraksta sertifikāta reģistrēšana

Ja ir nepieciešama reģistrēšana, varat izmantot lapu **Ierakstu sertifikātu žurnāls**, lai reģistrētu ES ieraksta sertifikātu, ko izsniedza trešā puse.

### <a name="uploading-a-received-eu-entry-certificate"></a>Saņemta ES ieraksta sertifikāta augšupielādēšana

Izmantojiet lapu **Pielikumi**, lai augšupielādētu saņemtu ES ieraksta sertifikātu, ko parakstījis ES debitors. Kad sertifikāts ir augšupielādēts, varat to saistīt ar rēķinu kā pierādījumu, ka krājumi tika piegādāti. Šāds pierādījums ir nepieciešams, ja jums ir jāizsniedz rēķins, kas neietver pievienotās vērtības nodokli (PVN), un tas tiek izmantots arī auditēšanas laikā.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Nav obligāti: sertifikāta statusa atjaunināšana un rēķina statusa drukāšana

Ieraksta sertifikācijas statusu un debitora rēķina drukāšanas statusu varat atjaunināt, izmantojot lapu **Rēķinu žurnāls**.

## <a name="technical-information-for-system-administrators"></a>Tehniskā informācija sistēmas administratoriem
Ja nevarat piekļūt lapām, kas tiek izmantotas šī uzdevuma izpildīšanai, sazinieties ar sistēmas administratoru un sniedziet nākamajā tabulā redzamo informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Priekšnosacījums</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Drošības lomas un pienākumi</td>
<td>Lai iestatītu un izveidotu ES ieraksta sertifikātu krājumiem vai pakalpojumiem, jums ir jābūt tādas drošības lomas dalībniekam, kurā ietverti tālāk norādītie pienākumi.
<ul>
<li><strong>Debitoru parādu darbinieks</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Klientu apkalpošanas pārstāvis</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Pārdošanas darbinieks</strong> (TradeSalesClerk)</li>
<li><strong>Nosūtīšanas darbinieks</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>






