---
title: Automātiskā apstiprināšana ar Plānošanas optimizācijas rīku
description: Šajā tēmā skaidrots, kā izmantot automātiskās apstiprināšanas ar Plānošanas optimizācijas rīku.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: e412ccbc7c44d41e0a70ef8b5436901e01c671e6
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383692"
---
# <a name="auto-firming-with-planning-optimization"></a>Automātiskā apstiprināšana ar Plānošanas optimizācijas rīku

[!include [banner](../../includes/banner.md)]

Automātiskā apstiprināšana ļauj apstiprināt (t.i., izlaist) plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa. Kad plānotie pasūtījumi ir apstiprināti, tie tiek pārveidoti par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem. Kad tiek izmantots Plānošanas optimizācijas rīks, plānotie pasūtījumi tiek apstiprināti vispārējās plānošanas izpildes laikā, kad pasūtījuma datums (tas ir, sākuma datums) ir laika periods apstiprināšanai.

> [!NOTE]
> Plānotā pirkšanas pasūtījuma automātisko apstiprināšanu var veikt tikai tad, ja krājums ir saistīts ar kreditoru.

## <a name="turn-on-auto-firming"></a>Automātiskās apstiprināšanas ieslēgšana

Lai ieslēgtu automātisko apstiprināšanu, veiciet tālāk minētās darbības.

1. Darbvietā **Līdzekļu pārvaldība** cilnē **Jauns** sarakstā atlasiet **Automātiskā apstiprināšana Plānošanas optimizācijai**. Ja šī funkcija netiek parādīta cilnē **Jauns**, skatiet cilnēs **Neiespējotās** un **Visas**.
1. Atlasiet **Iespējot tagad**. Pēc izvēles atlasiet **Grafiks** un pēc tam atlasiet laiku, kad vēlaties ieslēgt līdzekli.

## <a name="set-up-the-firming-time-fence"></a>Iestatiet apstiprināšanas noteikšanas periodu

Apstiprināšanas periods tiek aprēķināts uz priekšu, sākot no vispārējās plānošanas datuma. To nosaka ievadīto dienu skaits. Apstiprināšanas laika ierobežojumu var kontrolēt šādos veidos:

- Lai definētu noklusējuma apstiprināšanas laika ierobežojumu nodrošinājuma grupai, dodieties uz **Vispārējā plānošana**\>**Iestatījumi**\>**Nodrošinājums**\>**Nodrošinājuma grupas** un atlasiet nodrošinājuma grupu. Pēc tam no kopsavilkuma cilnes **Citi** laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.
- Lai pārrakstītu apstiprināšanas laika periodu, kas noteikts nodrošinājuma grupai noteiktam krājumam, dodieties uz **Produkta informācijas pārvaldība** \> **Izlaistās preces**, pēc tam no darbības rūts atlasiet **Plāns** un pēc tam atlasiet **Krājumu nodrošinājums**. Pēc tam cilnē **Vispārīgi** atlasiet **Ignorēt laika periodu** un laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.
- Lai pārrakstītu apstiprināšanas laika periodu, kas ir definēts nodrošinājuma grupai un krājumu nodrošinājumam noteiktam vispārējam plānam, dodieties uz **Vispārējā plānošana**\>**Iestatījumi**\>**Vispārējie plāni** un atlasiet vispārējo plānu. Pēc tam kopsavilkuma cilnē  **Periods dienās** lauciņu **Iesaldēt** uzstādiet uz **Jā** un ievadiet dienu skaitu.

Ja ir ieslēgta automātiskā apstiprināšana vispārējai plānošanai, kas izmanto Plānošanas optimizāciju, automātiskās apstiprināšanas process tiek veikts saskaņā ar automātiskās apstiprināšanas iestatījumiem. Ja automātiskā apstiprināšana nav ieslēgta vai ja plānošana tiek sākta no lapas **Tīkla prasības**, automātiskās apstiprināšanas process tiek izlaists.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Plānošanas optimizācija pret iebūvēto Supply Chain Management plānošanas programmu

Plānošanas optimizāciju un plānošanas programmu, kas ir iebūvēta Microsoft Dynamics 365 Supply Chain Management, var izmantot, lai automātiski apstiprinātu plānotos pasūtījumus. Taču pastāv dažas svarīgas atšķirības. Piemēram, tā kā Plānošanas optimizācija izmanto pasūtījuma datumu (t.i., sākuma datumu), lai noteiktu, kurus plānotos pasūtījumus apstiprināt, iebūvētā Supply Chain Management plānošanas programma izmanto prasības datumu (t.i., beigu datumu). Lūk, kopsavilkums par atšķirībām.

**Plānošanas optimizācija**

- Automātiskā apstiprināšana ir balstīta uz pasūtījuma datumu (sākuma datumu).
- Tā kā pasūtījuma datums (sākuma datums) aktivizē apstiprināšanu, jums nav jāapsver izpildes laiks kā daļa no apstiprināšanas laika ierobežojuma.
- Ja vēlaties apstiprināt visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt vienai nedēļai.

**Iebūvēta Supply Chain Management plānošanas programma**

- Automātiskā apstiprināšana ir balstīta uz prasības datumu (beigu datuma).
- Lai palīdzētu nodrošināt, ka pasūtījumi ir apstiprināti noteiktā laikā, apstiprināšanas laika periodam jābūt ilgākam par izpildes laiku.
- Ja vēlaties apstiprināt visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt izpildes laikam plus viena nedēļa.
