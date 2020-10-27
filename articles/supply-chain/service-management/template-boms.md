---
title: Veidnes MK
description: Veidnes materiālu komplekti (MK) nodrošina standartizētu komponentu sarakstu tiem pakalpojumu objektiem, kas tiek apkalpoti regulāri.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985772"
---
# <a name="template-boms"></a>Veidnes MK    

[!include [banner](../includes/banner.md)]


Veidnes materiālu komplekti (MK) jums nodrošina standartizētu komponentu sarakstu tiem pakalpojumu objektiem, kas tiek apkalpoti regulāri. Komponenti, kas ir uzskaitīti veidnes MK, pārstāv pakalpojumu objekta atsevišķos apakškomponentus. Pakalpojumu objektam lietojot veidnes MK, varat reģistrēt apakškomponentus, kas ir aizstāti šim pakalpojumu objektam.

Lai pielietotu veidnes MK pakalpojumu līgumam vai pakalpojumu pasūtījumam, pievienojiet to pakalpojumu objektu attiecībām.


> [!NOTE]
> <P>Katram pakalpojumu objektam varat lietot tikai vienu veidnes MK.</P>

## <a name="create-a-template-bom"></a>Veidnes MK izveidošana

Nākamajā tabulā ir informācija par dažādajām metodēm, kuras varat izmantot, lai izveidotu veidnes MK.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Metode</p></th>
<th><p>Apraksts</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Ražošana</p></td>
<td><p>Šis veidnes MK ir balstīts uz ražošanas pasūtījumu. Šī opcija ir piemērojama tikai tad, ja darbojaties ražošanas vidē. Šīs metodes priekšrocība ir tā, ka jums ir pašreizējs, detalizēts saraksts ar sastāvdaļām, kas aizvieto krājumu.</p></td>
</tr>
<tr class="even">
<td><p>Krājuma MK</p></td>
<td><p>Veidnes MK ir balstīts uz krājuma MK. Krājuma MK, atšķirībā no ražošanas MK, ir statisks saraksts ar komponentiem, kas veido kādu krājumu.</p></td>
</tr>
<tr class="odd">
<td><p>Pastāvoša veidne</p></td>
<td><p>Veidne ir balstīta uz pastāvošu veidnes MK.</p></td>
</tr>
<tr class="even">
<td><p>Manuāli</p></td>
<td><p>Ja jūs zināt, kuras rezerves daļas parasti tiek aizvietotas kādā pakalpojumu objektā, savu veidnes MK varat izveidot manuāli. Šī metode noder, lai nodrošinātu, ka veidnē ietvertie komponenti ataino faktiskās vajadzības jūsu darba vietā.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Veidnes MK lietošana pakalpojumu līgumam vai pakalpojumu pasūtījumam

Veidnes MK varat lietot kādam pakalpojumu līgumam, pakalpojumu pasūtījumam vai abiem. Pakalpojumu līgums parasti sedz ilgtermiņa attiecības ar klientu. Pakalpojumu materiālu komplektā (MK) ierakstītā aizvietojumu vēsture ir pakalpojumu līgumam noderīgi dati.

Veidnes materiālu komplektu (MK) varat lietot arī pakalpojumu pasūtījumam, lai ierakstītu pakalpojumu objektam izpildīto pakalpojumu vēsturi.

## <a name="copy-the-history-of-a-service-bom"></a>Pakalpojumu MK vēstures kopēšana

Pakalpojumu MK rindas vēsturi varat kopēt no viena pakalpojumu līguma uz citu pakalpojumu līgumu. Kopējot pakalpojumu vēsturi starp pakalpojumu līgumiem, varat saglabāt ierakstu par kāda krājuma aizvietošanu.

**Piemērs**

Jūs esat iestatījis trīs gadu ilgu pakalpojumu līgumu klienta mašīnai. Šajā laikā klients pierod pie uzņēmuma sniegtajiem labajiem pakalpojumiem. Tādēļ pēc līguma beigām klients vēlas iestatīt jaunu. Tagad jūs varat vienoties par uzņēmumam izdevīgāku līgumu. Tā kā ieraksti par aizvietotajiem komponentiem var noderēt arī turpmāk, šī pakalpojumu MK vēsturi jūs kopējat uz jauno līgumu.

## <a name="modify-the-template-bom"></a>Veidnes MK modificēšana

Ja kāds veidnes MK nav pievienots nevienam pakalpojumu objektam, tajā varat modificēt vai dzēst rindas. Pēc veidnes MK pievienošanas kādam pakalpojumu objektam varat modificēt tikai MK lokālo versiju. Ja vēlaties dublēt veidnes MK lokālās versijas iestatījumus, jūs varat izveidot jaunu veidnes MK, kas balstās uz lokālo versiju. Plašāku informāciju skatiet tēmā [Pakalpojumu MK modificēšana](modify-service-bom.md).

Ja aizvietojat kādu materiālu komplektā (MK) ietvertu krājumu, šo aizvietošanu varat iereģistrēt MK veidotāja MK rindā. Ja vēlaties, aizvietošanas objektam varat izveidot pakalpojumu pasūtījuma rindu. Ja izveidojat pakalpojumu pasūtījuma rindu, varat izrakstīt rēķinu par aizvietošanas krājumu. Ja aizvietošanai neizveidojat pakalpojumu pasūtījuma rindu, aizvietošanas reģistrācija tiek paturēta, lai varētu izsekot pakalpojumu objekta vēsturi.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>MK rindas informācijas rādīšanas veida mainīšana

Varat mainīt veidu, kā visiem veidņu un pakalpojumu MK tiek rādīta MK rindas informācija. Šīs izmaiņas attiecas uz visiem veidņu MK un pakalpojumu MK. Tostarp arī tādiem, kas ir pievienoti pakalpojumu objektiem.

## <a name="set-up-number-sequences-for-template-boms"></a>Veidņu MK numuru sēriju iestatīšana

Lai izmantotu veidņu MK, ir jāiestata divas numuru sērijas. Iestatiet vienu numuru sēriju veidnes materiālu komplektam (MK) un vienu — MK vēstures rindas numuram.


> [!NOTE]
> <P>Numuru sērijas tiek izmantotas, lai piešķirtu identifikatorus ierakstiem, kam tie ir nepieciešami. Lai numuru sēriju varētu piešķirt veidnes MK vai MK vēstures rindas numuram, ir jāiestata numuru sēriju kodi.</P>


## <a name="set-up-number-sequences"></a>Numuru sēriju iestatīšana

1.  Saraksta lapā **Numuru sērijas** izveidojiet numuru sērijas veidņu materiālu komplektu (MK) un MK vēstures rindu numuram. 

2.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.

3.  Noklikšķiniet uz **Numuru sērijas** un pēc tam atlasiet kādu numuru sērijas kodu numuru sēriju atsaucēm, kuras izveidojāt formā **Numuru sērijas**.

4.  Aizveriet formu, lai saglabātu izmaiņas.


> [!NOTE]
> <P>MK vēstures rindas numuru sistēma izmanto, lai transakcijas MK vēsturē saistītu ar pakalpojumu līgumu vai pakalpojumu pasūtījumu. Šis numurs netiek rādīts lietotāja interfeisā.</P>



## <a name="see-also"></a>Skatiet arī

[Veidnes MK izveide](create-template-bom.md)

[Veidņu MK pārvaldīšana objektu attiecībās.](manage-template-boms-on-object-relations.md)

[Pakalpojuma MK modificēšana](modify-service-bom.md)

 


