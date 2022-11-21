---
title: Darba sākšana ar vispārējo plānošanu
description: Šajā rakstā ir paskaidrots, kā sākt izmantot vispārējās plānošanas funkcionalitāti sadaļā Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780307"
---
# <a name="get-started-with-master-planning"></a>Darba sākšana ar vispārējo plānošanu

[!include [banner](../../includes/banner.md)]

Vispārējo plānošanu programmatūrā Supply Chain Management nodrošina ārējs pakalpojums, ko sauc par plānošanas optimizācijas pievienojumprogrammu Dynamics 365 Supply Chain Management. Šajā tēmā ir paskaidrots, kā iegūt un iestatīt šo pakalpojumu.

## <a name="availability"></a>Pieejamība

Plānošanas optimizācija pašlaik ir pieejama šādās Azure ģeogrāfiskajās atrašanās vietās: ASV, Kanāda, Brazīlija, Eiropa, Francija, Apvienotā Karaliste, Norvēģija, Šveice, Austrālija, Āzijas un Klusā okeāna reģions, Japāna un Indija. Ja mēģināsit instalēt pievienojumprogrammu no cita ģeogrāfiskā reģiona, tad LCS rādīs ziņojumu, ka šī ģeogrāfiskā vērtība netiek atbalstīta. Papildinformāciju par Azure ģeogrāfiskām vietām un saistītiem reģioniem skatiet sadaļā [Azure ģeogrāfiskās vietas](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Ņemiet vērā, ka plānošanas optimizācija neatbalsta Dynamics 365 Supply Chain Management lokālās izvietošanas.

## <a name="licensing"></a>Licencēšana

Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.

## <a name="install-and-enable-planning-optimization"></a>Instalēt un iespējot plānošanas optimizāciju

Lai izmantotu plānošanas optimizāciju, pārliecinieties, vai visi sistēmas priekšnosacījumi ir savā vietā, un pēc tam iespējojiet tās licences atslēgu un instalējiet plānošanas optimizācijas pievienojumprogrammu Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat instalēt plānošanas optimizēšanas pievienojumprogrammu, ir jāievieš šādi priekšnosacījumi:

- Supply Chain Management ir jāpalaiž ar LCS iespējotu 2. līmeņa vai augstākas pieejamības vidi, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku. Ja mēģināsit instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta, un tā būs jāatceļ.

- Jūsu sistēmā jābūt iestatītai Power Platform integrācijai. Papildinformāciju skatiet sadaļā [Microsoft Power Platform Integrācija ar Finance and Operations programmām](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Iespējot plānošanas optimizācijas licenci

Lai izmantotu plānošanas optimizāciju, ir jāiespējo tās konfigurācijas atslēga. Lai to izdarītu:

1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Cilnē **Konfigurācijas atslēgas** atzīmējiet izvēles rūtiņu **plānošanas optimizācijai**.
1. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Instalēt un iespējot plānošanas optimizācijas pievienojumprogrammu

Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).

Lai instalētu plānošanas optimizācijas pievienojumprogrammu:

1. Piesakieties LCS un atveriet vēlamo vidi.
1. Doties **Pilna detalizēta informācija**.
1. Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.
1. Atlasiet **Instalēt jaunu pievienojumprogrammu**.
1. Atlasiet **Plānošanas optimizācija**.
1. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.
1. Atlasiet **Instalēt**.
1. Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.
1. Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina). Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.

Plānošanas optimizācijas pievienojumprogrammas instalēšanas galvenais nolūks ir savienot pakalpojumu un vidi. Tāpēc jums ir jāinstalē pievienojumprogramma atsevišķi katrai videi, kurā izmantosiet plānošanas optimizāciju neatkarīgi no tā, kāds kods tiek pārvietots starp vidēm.

## <a name="integrate-planning-optimization-with-your-system"></a>Integrējiet plānošanas optimizāciju savā sistēmu

Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.

### <a name="connection-status"></a>Savienojuma statuss

Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu. Nākamajā tabulā ir parādītas iespējamās vērtības.

| Savienojuma statuss | Apraksts | Vai var izmantot plānošanas optimizāciju? |
|---|---|---|
| Savienojums izveidots | Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management. | Jā |
| Savienojuma iespējošana | Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Savienojums pārtraukts | Nav savienojuma ar plānošanas optimizācijas pakalpojumu. Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā rakstā. | Nē |
| Savienojuma atspējošana | Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Statusa iegūšana | Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma. | Nē |

### <a name="the-use-planning-optimization-option"></a>Iespēja Plānošanas optimizācijas izmantošana

Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:

- **Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.
- **Nē** — novecojusi vispārējās plānošanas programma tiek izmantota vispārējai plānošanai.

Šis iestatījums attiecas uz visām juridiskajām personām (uzņēmumiem). Plānošanas optimizāciju nav iespējams izmantot dažās juridiskajās personās, bet novecojušo vispārējās plānošanas programmu — citās juridiskajās personās.

> [!NOTE]
> Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti novecojušajai vispārējās plānošanas programmai, tiek aktivizēti, kamēr opcija Izmantot plānošanas optimizāciju **ir iestatīta** uz **Jā**, šīs opcijas neizdosies.

### <a name="integration-with-the-setup"></a>Integrēšana ar iestatījumu

Ja plānošanas optimizācija ir ieslēgta, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu. Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
