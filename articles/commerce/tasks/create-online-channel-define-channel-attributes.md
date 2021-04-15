---
title: Izveidot tiešsaistes kanālu un definēt kanāla atribūtus
description: Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798517"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Izveidot tiešsaistes kanālu un definēt kanāla atribūtus

[!include [banner](../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai. Lai izveidotu jaunu tiešsaistes kanālu, vispirms ir jāizveido organizācijas hierarhija. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.


## <a name="create-a-new-online-channel"></a>Izveidot jaunu tiešsaistes kanālu
1. Dodieties uz Mazumtirdzniecība un tirdzniecība > Kanāli > Tiešsaistes veikali.
2. Klikšķiniet Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
5. Laukā Noliktavas laika josla atlasiet atbilstošo opciju.
6. Laukā Noklusējuma debitors ievadiet vai atlasiet vērtību.
7. Laukā Debitoru adrešu grāmata ievadiet vai atlasiet vērtību.
8. Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.
9. Laukā Maksājuma metode ievadiet vai atlasiet vērtību.
10. Laukā E-pasta paziņojumu profils ievadiet vai atlasiet vērtību.
11. Izvērsiet sadaļu Finanšu dimensijas.
12. Laukā Biznesa vienība ievadiet vai atlasiet vērtību.
    * Tādā pašā veidā iestatiet vērtību visām pārējām noklusējuma dimensijām.  
13. Noklikšķiniet uz Saglabāt.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Tiešsaistes kanāla pievienošana organizācijas hierarhijai
1. Aizvērt lapu.
2. Dodieties uz Organizācijas administrēšana > Organizācijas > Organizāciju hierarhijas.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Noklikšķiniet uz Skatīt.
5. Noklikšķiniet uz Rediģēt.
    * Varat atlasīt jebkuru hierarhijas mezglu, kam vēlaties pievienot jaunu kanālu.  
6. Klikšķiniet Ievietot.
7. Noklikšķiniet uz Tirdzniecības kanāls.
8. Noklikšķiniet uz Labi.
9. Noklikšķiniet uz Publicēt, lai atvērtu nolaižamo dialoglodziņu.
10. Laukā Spēkā stāšanās datums ievadiet datumu un laiku.
11. Noklikšķiniet uz Publicēt.

## <a name="configure-orders-for-near-real-time-notification"></a>Pasūtījumu konfigurēšana gandrīz reāllaika paziņojumam
1. Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Centrālā biroja iestatīšana > Parametri > Tirdzniecības parametri.
2. Vienumam “Izmantot reāllaika pakalpojumu e-komercijas pasūtījuma izveidei” iestatiet uz “Jā”.
3. Palaidiet sadales grafiku 1070, lai sinhronizētu izmaiņas ar kanālu datu bāzi. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]