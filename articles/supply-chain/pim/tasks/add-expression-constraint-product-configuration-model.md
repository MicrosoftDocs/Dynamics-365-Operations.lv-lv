---
title: Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ac010b96892450c8d37bb08f967ecf4491b4b5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148013"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim

[!include [banner](../../includes/banner.md)]

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

