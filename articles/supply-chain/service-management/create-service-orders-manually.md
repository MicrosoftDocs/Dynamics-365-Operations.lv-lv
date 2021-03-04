---
title: Pakalpojumu pasūtījumu manuālā izveide
description: Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51cfdb94a368df9e7082af3c768c79df44000342
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432805"
---
# <a name="create-service-orders-manually"></a>Pakalpojumu pasūtījumu manuālā izveide    

[!include [banner](../includes/banner.md)]


Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**. Pakalpojumu pasūtījumu varat veidot arī no projekta.

> [!TIP]
> <P>Varat izmantot automatizētos pakalpojumu pasūtījumu izveides procesus. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Pakalpojumu pasūtījuma manuāla izveide no pakalpojumu līguma

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Izvēlieties pakalpojumu līgumu un izveidojiet jaunu pakalpojumu līgumu.

3.  Noklikšķiniet uz cilnes **Piegāde** un grupā **Izveidot** noklikšķiniet uz **Plānotie pakalpojumu pasūtījumi**, lai atvērtu veidlapu **Pakalpojumu pasūtījumu izveide**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Pakalpojumu pasūtījuma manuāla izveide pakalpojumu pasūtījumu formā

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.

2.  Nospiediet Ctrl+N, lai veidotu jaunu pakalpojumu pasūtījumu.

3.  Pakalpojumu pasūtījumam izveidojiet pakalpojumu pasūtījuma rindas.

> [!NOTE]
> <P>Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam. Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</P>

## <a name="create-a-service-order-from-a-project"></a>Pakalpojumu pasūtījuma izveide no projekta

1.  Noklikšķiniet uz **Projektu pārvaldība un uzskaite** \> **Vispārīgi** \> **Projekti** \> **Visi projekti**.

2.  Veidlapas **Projekti** **Darbību rūtī** cilnē **Pārvaldība** noklikšķiniet uz \> **Pakalpojums** \> **Pakalpojumu pasūtījumi**.

3.  Izpildiet iepriekš norādītās darbības, lai manuāli izveidotu pakalpojumu pasūtījumu veidlapā **Pakalpojumu pasūtījumi**. Laukā **Projekta ID** tiek parādīta projekta atsauce.

> [!NOTE]
> <P>Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam. Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Pakalpojumu pasūtījuma izveide no veidlapas Pārdošanas pasūtījumi

Varat izveidot pakalpojumu pasūtījumu no veidlapas **Pārdošanas pasūtījumi**, izmantojot vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.

2.  Atveriet attiecīgo pārdošanas pasūtījumu.

3.  Cilnē **Pārdošanas pasūtījums** noklikšķiniet uz vienuma **Pakalpojuma pasūtījums**, lai palaistu vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.

4.  Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Atlasīt pakalpojumu pasūtījuma līgumu** veiciet tālākminētās darbības.
    
      - Izmantojiet lauku **Pakalpojuma līgums**, lai atlasītu pakalpojuma līgumu ar kuru ir jāsaista jaunais pakalpojuma pasūtījums.
    
      - Pēc izvēles: izmantojiet lauku **Projekta ID**, lai saistītu šo pakalpojuma pasūtījumu ar konkrētu projektu.

5.  Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Pakalpojuma pasūtījuma izveide** veiciet tālākminētās darbības.
    
      - Laukā **Ieteicamais pakalpojuma laiks** ievadiet pakalpojuma izsaukuma sākuma datumu un laiku.
    
      - Pēc izvēles: modificējiet tekstu laukā **Apraksts**. Pēc noklusējuma šajā laukā ir iepriekšējā lapā atlasītā pakalpojuma līguma apraksts.
    
      - Laukā **Atbildīgā persona** atlasiet par līgumu atbildīgā darbinieka ID un, ja ziniet, kurš tas ir, — klienta iecienītākā tehniķa ID, kurš būs atbildīgs par pakalpojuma izsaukumu.
    
      - Laukā **Kontaktpersonas ID** atlasiet klienta uzņēmuma kontaktpersonu, ar kuru ir jāsazinās saistībā ar šo pakalpojuma pasūtījumu.

6.  Noklikšķiniet uz **Tālāk \>** un pēc tam uz **Pabeigt**.


## <a name="see-also"></a>Skatiet arī

[Pakalpojuma pasūtījumi](service-orders.md)

[Automātiska pakalpojuma pasūtījumu izveide](create-service-orders-automatically.md)

[Pakalpojumu pasūtījumu izveidošana (klases forma)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]