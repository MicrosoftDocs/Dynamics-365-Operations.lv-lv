---
title: Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim
description: Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859c25fd361063d4c5a8544c4b488adfab4238e6cc079fa96efe1c71777779e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730326"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā preces konfigurācijas modelim var pievienot jaunu ierobežojuma izteiksmi. Tajā parādīts, kā varat noteikt, ka skaļrunim nepieciešama stūru aizsardzība, ja lietotājs ir atlasījis metāla priekšējo režģi. Procedūrai tiek izmantots augstas kvalitātes skaļruņa komponents demonstrācijas uzņēmumā USMF.

## <a name="create-an-expression-constraint"></a>Izteiksmes ierobežojuma izveide

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa modelis.  
4. Sarakstā atlasiet saiti atlasītajā rindā.
5. Izvērsiet sadaļu **Ierobežojumi**.
6. Atlasiet **Pievienot**.
7. Atlasiet **Izveidot**.
8. Laukā **Nosaukums** ierakstiet kādu vērtību.

## <a name="enter-expression"></a>Ievadīt izteiksmi

1. Atlasiet **Rediģēt izteiksmi**.
    * Šajā posmā atbloķējot lietotāja interfeisu uzdevuma ierakstīšanu, varat izmantot IntelliSense un simbolu sarakstu, lai izveidotu ierobežojumu izteiksmi.  
2. Laukā **ConstraintBody** ievadiet "Nozīmē[FrontGrill=="Metāls", CornerProtection]".
    * Šī izteiksmes loģika nosaka: ja priekšējais režģis ir metāls, tad jāatlasa stūru aizsardzības opcija.  
3. Atlasiet **Pārbaudīt**.
    * Apstiprināšanas funkcija apstrādā ierobežojuma izteiksmi un pārbauda sintakses kļūdas.  
4. Atlasiet **Aizvērt**.
5. Atlasiet **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]