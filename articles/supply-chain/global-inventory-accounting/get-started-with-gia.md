---
title: Darba sākšana ar Globālo krājumu uzskaiti
description: Šajā rakstā ir aprakstīts, kā uzsākt darbu ar globālo krājumu uzskaiti.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 493e0be8ab56abc2a3253876107b7f4fefabf4ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891094"
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

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a> Kā iegūt globālā krājuma uzskaites pievienojumprogrammu

> [!IMPORTANT]
> Lai izmantotu Globālo krājumu uzskaiti, ir jābūt LCS iespējotai augstas pieejamības videi (nevis OneBox videi). Turklāt jāizmanto Supply Chain Management versiju 10.0.19 vai jaunāku.

### <a name="supply-chain-management-version-10019-to-10026"></a>Piegādes ķēdes pārvaldības versija no 10.0.19 līdz 10.0.26

Lai instalētu Globālo krājumu uzskaiti Piegādes ķēdes pārvaldības versijai 10.0.19 uz 10.0.26, [sāciet ar pievienojumprogrammas instalēšanu](#install). Pēc tam nosūtiet savu LCS vides ID un uzņēmuma nosaukumu, sūtīt e-pasta ziņojumu uz globālo [krājumu uzskaites grupu](mailto:GlobalInvAccount@microsoft.com). Komanda nosūtīs jums sekojuma e-pastu, kas satur jūsu Globālā krājuma uzskaites pakalpojuma galapunktus.

### <a name="supply-chain-management-version-10027-and-later"></a>Piegādes ķēdes pārvaldības versija 10.0.27 un jaunāka

Lai instalētu Globālo krājumu uzskaiti Piegādes ķēdes pārvaldības versijai 10.0.27 un jaunākai versijai, [tikai instalējiet pievienojumprogrammu](#install). Šīm Piegādes ķēžu pārvaldības versijām globālie krājumu uzskaites pakalpojuma galapunkti tiks iestatīti automātiski, tādēļ jums tos nav nepieciešams atrast manuāli. Ja pievienojumprogrammas iestatīšanas laikā rodas problēmas, lūdzu, sazinieties ar globālo [krājumu uzskaites grupu](mailto:GlobalInvAccount@microsoft.com).

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
1. Atlasiet **Piešķirt lomu** un pēc tam atlasiet *Sistēmas administrators*. Ja ir loma ar nosaukumu Lietotājs *Common Data Service*, atlasiet to.
1. Atkārtojiet iepriekšējās darbības, bet iestatiet lauku **Pieteikuma ID** uz *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Ja jūsu Dataverse instalācijas noklusējuma valoda nav angļu valoda, veiciet šādas darbības.

1. Pārejiet uz **Papildu iestatījums \> Administrēšana \> Valodas**.
1. Atlasiet *Angļu* (*ValodasKods=1033*) un pēc tam atlasiet **Lietot**.

## <a name="install-the-add-in"></a><a name="install"></a>Pievienojumprogrammas instalēšana

Izpildiet šīs darbības, lai instalētu pievienojumprogrammu, kuru var izmantot Globālajai krājumu uzskaitei.

1. Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).
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
1. Cilnē Visi **meklējiet** līdzekli ar nosaukumu (Priekšskatījums) Globālo *krājumu uzskaite*.
1. Atlasiet **Iespējot tagad**.
1. Dodieties uz sadaļu **Globālā krājumu uzskaite \> Iestatīšana \> Globālās krājumu uzskaites parametri \> Integrācijas parametri**.
1. Atkarībā no tā, kuru Piegādes ķēžu pārvaldības versiju jūs izmantojat, veiciet vienu no šīm darbībām:
    - **Piegādes ķēdes pārvaldības versija 10.0.19 līdz 10.0.26**: **·** **datu** pakalpojuma galapunkta un globālā krājuma uzskaites galapunkta laukos ievadiet URL, kas tika sūtīti jums pa e-pastu [no globālās krājumu uzskaites komandas (](#sign-up) skatiet arī Kā iegūt globālās krājumu uzskaites pievienojumprogrammu).
    - **Piegādes ķēdes pārvaldības versija 10.0.27 un jaunāka**: jums nav jāievada galapunkti, tāpēc varat izlaist šo soli.

Globālā krājumu uzskaite tagad ir gatava lietošanai.
