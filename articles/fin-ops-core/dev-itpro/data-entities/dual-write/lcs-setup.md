---
title: Duālā ieraksta iestatīšana no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt duālo rakstīšanas savienojumu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781396"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Duālā ieraksta iestatīšana no Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā skaidrots, kā iespējot duālo rakstīšanu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Jums jāpabeidz Power Platform integrēšana atbilstoši aprakstam šādās tēmās:

+ [Power Platform integrācija - Iespējot vides izvietošanas laikā](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform integrācija - Iespējot pēc vides izvietošanas](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

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

## <a name="linking-mismatch"></a>Saistīšanas neatbilstība

Ir iespējams, ka jūsu LCS vide ir saistīta ar vienu Dataverse instanci, kamēr duālās rakstīšanas vide ir saistīta ar citu Dataverse instanci. Šī saistīšanas neatbilstība var izraisīt neparedzētu uzvedību, un tā var beigt datu nosūtīšanu uz nepareizo vidi. Ieteicamā vide, kas tiek izmantota duālajā rakstībā, ir tā, kas ir izveidota kā daļa no Power Platform integrācijas, un ilgtermiņa, tas būs vienīgais veids, kā izveidot saiti starp vidēm.

Ja jūsu videi ir saistīšanas neatbilstība, LCS parāda brīdinājumu jūsu vides informācijas lapā, kas ir līdzīga "Microsoft ir noteikusi, ka jūsu vide ir saistīta, izmantojot duālo rakstiet ar citu adresātu, nevis to, kas ir norādīts Power Platform integrācijā, kas nav ieteicama":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integrācijas saite ir neatbilstoša.":::

Ja saskaraties ar šo kļūdu, pastāv divas opcijas, kas pamatotas uz jūsu vajadzībām:

+ [Atsaistīt un atkārtoti saistīt dubultās rakstīšanas vides (Atiestatīt vai mainīt saistīšanu)](relink-environments.md#scenario-reset-or-change-linking), kā norādīts LCS vides informācijas lapā. Šī ir ideālā opcija, jo to varat palaist bez Microsoft atbalsta.  
+ Ja vēlaties saglabāt saiti duālās rakstīšanas ierakstā, varat lūgt Microsoft Atbalsta dienestu palīdzību mainīt Power Platform integrāciju, lai izmantotu esošo Dataverse vidi, kā dokumentēts iepriekšējā sadaļā.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
