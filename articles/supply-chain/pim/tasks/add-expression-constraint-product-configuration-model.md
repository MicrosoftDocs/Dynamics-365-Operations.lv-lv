--- 
title: "Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim"
description: "Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi. Tajā parādīts, kā varat noteikt, ka skaļrunim nepieciešama stūru aizsardzība, ja lietotājs ir atlasījis metāla priekšējo režģi. Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.


## <a name="create-an-expression-constraint"></a>Izteiksmes ierobežojuma izveide
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa modelis.  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Izvērsiet sadaļu Ierobežojumi.
6. Noklikšķiniet uz Pievienot.
7. Noklikšķiniet uz Izveidot.
8. Laukā Nosaukums ierakstiet kādu vērtību.

## <a name="enter-expression"></a>Ievadīt izteiksmi
1. Noklikšķiniet uz Rediģēt izteiksmi.
    * Šajā posmā atbloķējot lietotāja interfeisu uzdevuma ierakstīšanu, varat izmantot IntelliSense un simbolu sarakstu, lai izveidotu ierobežojumu izteiksmi.  
2. Laukā ConstraintBody ievadiet "Nozīmē[FrontGrill=="Metāls", CornerProtection]".
    * Šī izteiksmes loģika nosaka: ja priekšējais režģis ir metāls, tad jāatlasa stūru aizsardzības opcija.  
3. Noklikšķiniet uz Pārbaudīt.
    * Apstiprināšanas funkcija apstrādā ierobežojuma izteiksmi un pārbauda sintakses kļūdas.  
4. Noklikšķiniet uz Aizvērt.
5. Noklikšķiniet uz OK.


