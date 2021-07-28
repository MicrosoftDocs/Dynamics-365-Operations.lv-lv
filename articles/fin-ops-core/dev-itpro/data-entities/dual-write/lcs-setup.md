---
title: Duālā ieraksta iestatīšana no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt duālo rakstīšanas savienojumu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e604e1491bbafa041fa3f52ad0f8b454c63d47de
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359367"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Duālā ieraksta iestatīšana no Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā skaidrots, kā iespējot duālo rakstīšanu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Jums jāpabeidz Power Platform integrēšana atbilstoši aprakstam šādās tēmās:

+ [Power Platform integrācija - Iespējot vides izvietošanas laikā](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform integrācija - Iestatīt pēc vides izvietošanas](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Iestatīt duālo rakstīšanu jaunajām Dataverse vidēm

Veiciet šos soļus, lai iestatītu duālo rakstīšanu no LCS **Vides informācijas** lapas:

1. Lapā **Vides informācija** izvērsiet **Power Platform integrācijas** sadaļu.

2. Atlasiet **Duālās rakstīšanas programmas** pogu.

    ![Power Platform integrēšana.](media/powerplat_integration_step2.png)

3. Pārskatiet noteikumus un nosacījumus un atzīmējiet **Konfigurēt**.

4. Lai turpinātu, atlasiet **Labi**.

5. Jūs varat pārraudzīt progresu, periodiski atsvaidzinot vides informācijas lapu. Uzstādīšanai parasti nepieciešamas 30 minūtes vai mazāk.  

6. Kad uzstādīšana ir pabeigta, ziņojums jūs informēs, vai process bija veiksmīgs vai ja tajā radās kļūme. Ja iestatīšana neizdevās, tiek parādīts saistītais kļūdas ziņojums. Kļūdas jālabo pirms pārcelšanās uz nākamo darbību.

7. Atlasiet **Saite uz Power Platform vidi**, lai izveidotu saiti starp Dataverse un pašreizējās vides datu bāzēm. Tas parasti aizņem mazāk kā 5 minūtes.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Saite uz Power Platform vidi.":::

8. Kad saistīšana ir pabeigta, tiek parādīta hipersaite. Izmantojiet saiti, lai pieteiktos duālās rakstīšanas administrācijas apgabalā Finance and Operations vidē. No turienes varat iestatīt elementu kartējumus.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Iestatīt duālo rakstīšanu jau esošai Dataverse videi

Lai esošajai Dataverse videi iestatītu duālo rakstīšanu, ir jāizveido Microsoft [atbalsta biļete](../../lifecycle-services/lcs-support.md). Biļetē ir jāietver:

+ Jūsu Finance and Operations vides ID.
+ Jūsu vides nosaukums no Lifecycle Services.
+ Dataverse organizācijas ID vai Power Platform vides ID no Power Platform administrēšanas centra. Jūsu biļetē pieprasiet, lai ID tiktu izmantots Power Platform integrācijai.

> [!NOTE]
> Jūs nevarat atsaistīt vides, izmantojot portālu LCS. Lai noņemtu saiti videi, atveriet **Datu integrācijas** darbvietu Finance and Operations vidē un pēc tam atlasiet **Noņemt saiti**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
