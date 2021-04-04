---
title: Ārvalstu valūtas pārvērtēšana bankas kontiem
description: Šajā tēmā ir sniegta informācija par ārvalstu valūtas pārvērtēšanu bankas kontiem.
author: panolte
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86d62d5d281eaf243b61d2d86591257f758d5d3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264981"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a>Ārvalstu valūtas pārvērtēšana bankas kontiem

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a>Ārvalstu valūtas summu pārvērtēšana bankas kontu transakcijām

> [!IMPORTANT]
> Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Polijā.

Varat pārvērtēt ārvalstu valūtas summas bankas transakcijas. Pēc tam varat izveidot pārskatu, lai skatītu bankas transakcijas, kurām ir ārvalstu valūtas pārvērtēšanas korekcijas.

1. Atlasiet vienumu **Skaidras naudas un bankas pārvaldība** &gt; **Periodiskie uzdevumi** &gt; **Banka — Valūtas maiņas korekcija (FIFO un LIFO)**.
2. Laukā **Datumā** ievadiet pārvērtēšanas beigu datumu. Aprēķinos tiek iekļautas tikai transakcijas, kuru datums ir pirms norādītā datuma.
3. Atlasiet **Iekļaujamie ieraksti** &gt; **Filtrēt** &gt; **Pievienot**, lai pievienotu bankas kontu. Ja nenorādīsit bankas kontu, tiek pārvērtētas visas bankas kontu summas.
4. Atlasiet **Labi**, lai aizvērtu vaicājuma lapu.
5. Lapā **Ārvalstu valūtas pārvērtēšana** atzīmējiet izvēles rūtiņu **Pārrēķins**, lai pārvērtētu ārvalstu valūtas summas par visiem atvērtajiem periodiem.

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a>Pārskata izveide, lai skatītu bankas transakcijas, kurām ir ārvalstu valūtas pārvērtēšanas korekcijas

> [!IMPORTANT]
> Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Polijā.

1. Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Pieprasījumi un pārskati** &gt; **Pārskats “Banka — Valūtas maiņas korekcija”**.
2. Atlasiet vienumu **Iekļaujamie ieraksti** &gt; **Filtrēt**, lai atrastu vienu vai vairākus bankas kontus, par kuriem skatīt informāciju.
3. Neobligāti: laukā **Bankas konts** atlasiet bankas kontu. Atstājot šo lauku tukšu, pārskatā tiek iekļauta bankas transakciju informācija par visiem bankas kontiem.
4. Atlasiet **Labi**, lai izveidotu pārskatu. 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a>Valūtas maiņas kursa korekciju aprēķins bankas konta transakcijām

> [!IMPORTANT]
> Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Čehijas Republikā, Igaunijā, Lietuvā vai Latvijā.

Ir jāpārvērtē un jākoriģē banku konti, ja pastāv maiņas kursu atšķirība starp uzskaites valūtu un pārskata valūtu. Šis uzdevums palīdz jums aprēķināt pareizo bilanci gan uzskaites valūtā, gan pārskata valūtā bankas kontos.

1. Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Iestatīšana** &gt; **Skaidras naudas un bankas pārvaldības parametri**.
2. Cilnes **Numuru sērijas** laukā **Atsauce** atlasiet numuru sēriju atsaucei **Banka — Valūtas maiņas korekcija**.
3. Aizvērt lapu.
4. Atlasiet **Virsgrāmata** &gt; **Iestatīšana** &gt; **Valūta** &gt; **Valūtas maiņas kursi**. Lapā **Valūtas maiņas kursi** var definēt maiņas kursu starp divām valūtām vai valūtu pāri.
5. Kad esat beidzis, aizveriet lapu.
6. Atlasiet **Virsgrāmata** &gt; **Iestatīšana** &gt; **Virsgrāmata**. Laukos **Nerealizētā peļņa** un **Nerealizētie zaudējumi** atlasiet galveno kontu, kurā tiek grāmatoti maiņas kursi.
7. Aizvērt lapu.
8. Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Periodiskie uzdevumi** &gt; **Ārvalstu valūtas pārvērtēšana**.
9. Laukā **Datumā** atlasiet pārvērtēšanas datumu vai korekcijas datumu.
10. Laukā **No valūtas** atlasiet pašreizējās valūtas kodu. Laukā **Uz valūtu** atlasiet valūtu, kura jākoriģē.
11. Atlasiet **Iekļaujamie ieraksti** &gt; **Filtrēt**, lai atrastu bankas kontu, un pēc tam atlasiet **Labi**.
12. Lapā **Ārvalstu valūtas pārvērtēšana** atlasiet **Labi**. Bankas kontu darījumu korekcija atlasītajā datumā tiek aprēķināta.

> [!NOTE]
> Virsgrāmatā var skatīt divas atsevišķas transakcijas: uzskaites valūtai un pārskata valūtai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]