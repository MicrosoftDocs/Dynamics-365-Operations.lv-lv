---
title: Darba sākšana ar Globālo krājumu uzskaiti
description: Šajā tēmā ir aprakstīts, kā sākt darbu ar Globālo krājumu uzskaiti.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f5b3c013996253de75cd85c4bcfc52ed159e8f9d
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860513"
---
# <a name="get-started-with-global-inventory-accounting"></a>Darba sākšana ar Globālo krājumu uzskaiti

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Globālā krājumu uzskaite ļauj veikt vairāku krājumu uzskaites Globālās krājumu uzskaites virsgrāmatās, kas iestatītas. Katru Globālās krājumu uzskaites virsgrāmatu jāsaista ar *konvenciju*. Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:

- Izmaksu objekts
- Ievades mērījumu bāze
- Izmaksu plūsmas pieņēmums
- Izmaksu elements

> [!NOTE]
> Pat pēc tam, kad esat ieslēdzis Globālo krājumu uzskaiti, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.

Globālā krājumu uzskaite ir pievienojumprogramma. Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS). Varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.

Globālā krājumu uzskaite šobrīd neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Supply Chain Management. Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Kā iegūt Globālās krājuma uzskaites publisku priekšskatījumu

> [!IMPORTANT]
> Lai izmantotu Globālo krājumu uzskaiti, ir jābūt LCS iespējotai augstas pieejamības videi (nevis OneBox videi). Turklāt jāizmanto Supply Chain Management versiju 10.0.19 vai jaunāku.

Lai pieteiktos Globālās krājumu uzskaites publiskajam priekšskatījumam, nosūtiet savu LCS vides ID pa e-pastu [Globālās krājumu uzskaites grupai](mailto:GlobalInvAccount@microsoft.com). Pēc programmas apstiprināšanas grupa nosūtīs jums e-pasta ziņojumu, kas ietvers Globālās krājumu uzskaites beta atslēgu un jūsu pakalpojuma galapunktus. Pēc beta atslēgas saņemšanas varat [instalēt pievienojumprogrammu](#install).

## <a name="licensing"></a>Licencēšana

Globālā krājumu uzskaite ir licencēta kopā ar krājumu uzskaites standarta līdzekļiem, kas ir pieejami Supply Chain Management. Jums nav jāiegādājas papildu licence, lai izmantotu Globālo krājumu uzskaiti.

## <a name="prerequisites"></a>Priekšnosacījumi

### <a name="set-up-microsoft-power-platform-integration"></a>Iestatiet integrāciju ar Microsoft Power Platform

Pirms iespējot pievienojumprogrammas funkcionalitāti, jums jāintegrē ar Microsoft Power Platform, veicot šādas darbības.

1. Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.
1. Doties **Pilna detalizēta informācija**.
1. Sadaļā **Power Platform integrācija** atlasiet **Iestatīšana**.
1. Dialoglodziņā **Power Platform vides iestatīšana** atzīmējiet izvēles rūtiņu un pēc tam atlasiet **Iestatīšana**. Parasti iestatīšana ilgst no 60 līdz 90 minūtēm.
1. Kad Microsoft Power Platform vides iestatīšana ir pabeigta, lapa parāda jūsu vides nosaukumu. Turklāt sadaļā **Power Platform Integrācija** ir parādīts paziņojums "Power Platform vides iestatīšana ir pabeigta." Globālajai krājumu uzskaitei nav nepieciešama dubultās rakstīšanas programma.

Papildinformāciju skatiet rakstā [Iestatīt pēc vides izvietošanas](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>Iestatīt Dataverse

Pirms Dataverse iestatīšanas, pievienojiet nomniekam Globālās krājumu uzskaites pakalpojumu principus, izpildot šīs darbības.

1. Instalējiet Azure AD moduli Windows PowerShell v2, kā aprakstīts [Pakalpojuma Azure Active Directory instalēšana PowerShell grafikam](/powershell/azure/active-directory/install-adv2).
1. Izpildiet šādu PowerShell komandu.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Pēc tam izveidojiet programmas lietotājus Globālajā krājumu uzskaitē programmā Dataverse, veicot šādas darbības.

1. Atveriet Dataverse vides URL.
1. Dodieties uz **Papildu iestatījumi \> Sistēma \> Drošība \> Lietotāji** un izveidojiet programmas lietotāju. Izmantojiet lauku **Skats**, lai mainītu lapas skatu uz *Programmas lietotāji*.
1. Atlasiet **Jauns**.
1. Iestatiet lauku **Programmas ID** uz *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Atlasiet **Piešķirt lomu** un pēc tam atlasiet *Sistēmas administrators*. Ja ir loma ar nosaukumu *Common Data Service Lietotājs*, atlasiet to arī.
1. Atkārtojiet iepriekšējās darbības, bet iestatiet lauku **Pieteikuma ID** uz *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Ja jūsu Dataverse instalācijas noklusējuma valoda nav angļu valoda, veiciet šādas darbības.

1. Pārejiet uz **Papildu iestatījums \> Administrēšana \> Valodas**.
1. Atlasiet *Angļu* (*ValodasKods=1033*) un pēc tam atlasiet **Lietot**.

## <a name="install-the-add-in"></a><a name="install"></a>Pievienojumprogrammas instalēšana

Izpildiet šīs darbības, lai instalētu pievienojumprogrammu, kuru var izmantot Globālajai krājumu uzskaitei.

1. [Parakstīties](#sign-up) Globālās krājuma uzskaites publiskam priekšskatījumam.
1. Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).
1. Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.
1. Atlasiet plus zīmi (**+**).
1. Laukā **Kods** ievadiet savu papildinājuma beta atslēgu Globālajai krājuma uzskaitei. (Kad pierakstījieties, jums vajadzētu saņemt beta atslēgu ar e-pasta ziņojumu.)
1. Atlasiet **Atbloķēt**.
1. Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.
1. Doties **Pilna detalizēta informācija**.
1. Dodieties uz **Power Platform integrāciju** un atlasiet **Iestatīšana**.
1. Dialoglodziņā **Power Platform vides iestatīšana** atzīmējiet izvēles rūtiņu un pēc tam atlasiet **Iestatīšana**. Parasti iestatīšana ilgst no 60 līdz 90 minūtēm.
1. Kad Microsoft Power Platform vides iestatīšana ir pabeigta, kopsavilkuma cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
1. Atlasiet **Globālā krājumu uzskaite**.
1. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.
1. Atlasiet **Instalēt**.
1. Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēta Globālā krājumu uzskaite. Pēc dažām minūtēm statusam jāmainās no *Instalē* uz *Instalēts*. (Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī Globālā krājumu uzskaite ir gatava lietošanai.

## <a name="set-up-the-integration"></a>Iestatiet integrēšanu

Veiciet šīs darbības, lai iestatītu integrāciju starp Globālo krājumu uzskaiti un Supply Chain Management.

1. Pierakstieties Supply Chain Management.
1. Dodieties uz **Sistēmas administrēšana \> Līdzekļu pārvaldība**.
1. Atlasiet **Pārbaudīt atjauninājumus**.
1. Cilnē **Viss** meklējiet līdzekli ar nosaukumu *Globāla krājumu uzskaite*.
1. Atlasiet **Iespējot tagad**.
1. Dodieties uz sadaļu **Globālā krājumu uzskaite \> Iestatīšana \> Globālās krājumu uzskaites parametri \> Integrācijas parametri**.
1. Laukos **Datu pakalpojuma galapunkts** un **Globālās krājumu uzskaites galapunkts** ievadiet vietrāžus URL no e-pasta ziņojuma, ko Globālās krājumu uzskaites grupa nosūtīja, kad pierakstījieties priekšskatījumā.

Globālā krājumu uzskaite tagad ir gatava lietošanai.
