---
title: Duālā ieraksta iestatīšana no Lifecycle Services
description: Šajā rakstā ir izskaidrots, kā iestatīt duālo rakstīšanas savienojumu no pakalpojumiem Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 5cccba580d23c3a0e9aed62f76a305926a58585f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879809"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Duālā ieraksta iestatīšana no Lifecycle Services

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir izskaidrots, kā iespējot duālo rakstiet no Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Klientiem ir jāveic Power Platform integrācija, kā aprakstīts šādās tēmās:

- Ja vēl neizmantojat un vēlaties Microsoft Power Platform izvērst finanšu un operāciju vides, pievienojot platformas iespējas, [Power Platform skatiet integrāciju — iespējot vides izvietošanas laikā](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Ja jums jau ir Dataverse un Power Platform vides, un vēlaties tās savienot ar finanšu un operāciju vidēm, skatiet [Power Platform integrāciju - iespējojiet pēc vides izvietošanas](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Duālās rakstīšanas iestatīšana jaunām vai esošām Dataverse vidēm

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

8. Kad saistīšana ir pabeigta, tiek parādīta hipersaite. Izmantojiet saiti, lai pieteiktos dubultās rakstīšanas administrācijas apgabalā Finanšu un operāciju vidē. No turienes varat iestatīt elementu kartējumus.

## <a name="linking-mismatch"></a>Saistīšanas neatbilstība

Ir iespējams, ka jūsu dubultās rakstīšanas vide ir saistīta ar Dataverse instanci, kamēr LCS nav iestatīts Power Platform integrācijai. Šī saistīšanas neatbilstība var izraisīt neparedzētu uzvedību. Ir ieteicams, lai LCS vides dati atbilstu datiem, kas ir saistīti ar duālo rakstiet, lai vienu un to pašu savienojumu varētu izmantot biznesa notikumi, virtuālās tabulas un pievienojumprogrammas.

Ja jūsu videi ir saistīšanas neatbilstība, LCS parāda brīdinājumu, kas ir līdzīgs šādam piemēram jūsu vides informācijas lapā: "Microsoft ir noteikusi, ka jūsu vide ir saistīta, izmantojot Duālo Power Platform rakstiet ar citu adresātu, nekā norādīts Integrācijā, kas nav ieteicama."

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integrācijas saite ir neatbilstoša.":::

Ja saņemat šo brīdinājumu, mēģiniet kādu no šiem risinājumiem:

- Ja jūsu LCS vide Power Platform nekad nav tikusi iestatīta integrācijai, varat izveidot savienojumu ar instanci, Dataverse kas ir konfigurēta duālā rakstīšana, izpildot šajā rakstā sniegtos norādījumus.
- Ja LCS Power Platform vide jau ir iestatīta integrācijai, jums ir jāatsaista dubultā rakstīšana un atkārtoti to jāpievieno tai, ko norāda LCS, izmantojot [Scenārijs: Atiestatīt vai mainīt saistīšanu](relink-environments.md#scenario-reset-or-change-linking).

Iepriekš bija pieejama manuāla atbalsta biļetes opcija, bet tas bija pirms iepriekš minētā 1. opcijas.  Korporācija Microsoft vairs neatbalsta pieprasījumu manuālu atkārtotu saistīšanu, izmantojot atbalsta biļeti.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
