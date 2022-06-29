---
title: Pakalpojumu pasūtījumu manuālā izveide
description: Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1764d97d4492e7b982a5d2c9f7e7f1c15380be1d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014856"
---
# <a name="create-service-orders-manually"></a>Pakalpojumu pasūtījumu manuālā izveide    

[!include [banner](../includes/banner.md)]


Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**. Pakalpojumu pasūtījumu varat veidot arī no projekta.

> [!TIP]
> <P>Varat izmantot automatizētos pakalpojumu pasūtījumu izveides procesus. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Pakalpojumu pasūtījuma manuāla izveide no pakalpojumu līguma

1.  Atlasiet **Pakalpojumu pārvaldības** \> **pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Izvēlieties pakalpojumu līgumu un izveidojiet jaunu pakalpojumu līgumu.

3.  Atlasiet cilni **Piegāde** un grupā **Izveidot** atlasiet **Plānotie pakalpojumu pasūtījumi**, lai atvērtu veidlapu **Pakalpojumu pasūtījumu izveide**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Pakalpojumu pasūtījuma manuāla izveide pakalpojumu pasūtījumu formā

1.  Atlasiet **Pakalpojumu pārvaldības pakalpojumu** \> **pasūtījumus** \> **Pakalpojumu pasūtījumi.**

2.  Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma pasūtījumu.

3.  Pakalpojumu pasūtījumam izveidojiet pakalpojumu pasūtījuma rindas.

> [!NOTE]
> <P>Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam. Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</P>

## <a name="create-a-service-order-from-a-project"></a>Pakalpojumu pasūtījuma izveide no projekta

1.  Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.

2.  Veidlapas **Projekti** **Darbību rūtī** cilnē **Pārvaldīt** noklikšķiniet uz \> **Pakalpojums** \> **Pakalpojumu pasūtījumi**.

3.  Izpildiet iepriekš norādītās darbības, lai manuāli izveidotu pakalpojumu pasūtījumu veidlapā **Pakalpojumu pasūtījumi**. Laukā **Projekta ID** tiek parādīta projekta atsauce.

> [!NOTE]
> <P>Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam. Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Pakalpojumu pasūtījuma izveide no veidlapas Pārdošanas pasūtījumi

Varat izveidot pakalpojumu pasūtījumu no veidlapas **Pārdošanas pasūtījumi**, izmantojot vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.

1.  Dodieties uz **Pārdošana un mārketings** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.

2.  Atveriet attiecīgo pārdošanas pasūtījumu.

3.  Cilnē **Pārdošanas pasūtījums** noklikšķiniet uz vienuma **Pakalpojuma pasūtījums**, lai palaistu vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.

4.  Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Atlasīt pakalpojumu pasūtījuma līgumu** veiciet šādas darbības:
    
      - Izmantojiet lauku **Pakalpojuma līgums**, lai atlasītu pakalpojuma līgumu ar kuru ir jāsaista jaunais pakalpojuma pasūtījums.
    
      - Pēc izvēles: izmantojiet lauku **Projekta ID**, lai saistītu šo pakalpojuma pasūtījumu ar konkrētu projektu.

5.  Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Pakalpojuma pasūtījuma izveide** veiciet šādas darbības:
    
      - Laukā **Ieteicamais pakalpojuma laiks** ievadiet pakalpojuma izsaukuma sākuma datumu un laiku.
    
      - Pēc izvēles: modificējiet tekstu laukā **Apraksts**. Pēc noklusējuma šajā laukā ir iepriekšējā lapā atlasītā pakalpojuma līguma apraksts.
    
      - Laukā **Atbildīgā persona** atlasiet par līgumu atbildīgā darbinieka ID un, ja ziniet, kurš tas ir, — klienta iecienītākā tehniķa ID, kurš būs atbildīgs par pakalpojuma izsaukumu.
    
      - Laukā **Kontaktpersonas ID** atlasiet klienta uzņēmuma kontaktpersonu, ar kuru ir jāsazinās saistībā ar šo pakalpojuma pasūtījumu.

6.  Atlasiet **Tālāk \>** un pēc tam atlasiet **Pabeigt**.


## <a name="see-also"></a>Skatiet arī

[Pakalpojumu pasūtījumi](service-orders.md)

[Automātiska pakalpojumu pasūtījumu izveide](create-service-orders-automatically.md)

[Pakalpojumu pasūtījumu izveidošana (klases forma)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]