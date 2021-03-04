---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433224"
---
# <a name="get-started-with-planning-optimization"></a>Darba sākšana ar plānošanas optimizāciju

[!include [banner](../../includes/banner.md)]

Kā [iepriekš paziņots](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), ir ieplānota plānošanas optimizācija, kas aizstātu esošo iebūvēto vispārējās plānošanas programmu.

Ja pašlaik izmantojat iebūvēto vispārējās plānošanas programmu, jums tūlīt jāsāk plānot migrāciju uz plānošanas optimizāciju. Ir svarīgi nekavējoties sākt migrācijas procesu, jo, kad tiek ieviests nolietojums, jūsu darbības var tikt ietekmētas. Lai izvairītos no problēmām pēdējā brīdī, kad tiek ieviests nolietojums, mēs iesakām pabeigt migrāciju pirms 2020. gada 1. decembra. 

Plānošanas optimizācijas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Supply Chain Management iebūvētajā plānošanas programmā. Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām. Pašlaik plānošanas optimizācijas funkcionalitāte Dynamics Lifecycle Services (LCS) netiek ieslēgta pēc noklusējuma, tāpēc jums ir iespēja veikt novērtēšanu pirms šī līdzekļa ieslēgšanas.

> [!NOTE]
> Jums jāpieprasa migrācijas izņēmumu plānošanas optimizācijā, ja vispārējās plānošanas process neiekļauj ražošanu (vispārējās plānošanas ģenerētus plānotos ražošanas pasūtījumus), un jums nepieciešama iebūvētā vispārējās plānošanas programmas versija, kas jaunāka par versiju 10.0.15. Sākot ar versiju 10.0.16, kļūda vidēs tiks parādīta, kad tiek palaista iebūvētā vispārējā plānošana bez plānoto ražošanas pasūtījumu ģenerēšanas. Plānošanas optimizācija ir jāizmanto visiem jaunajiem izvietojumiem, kas vispārējās plānošanas laikā neģenerē plānotos ražošanas pasūtījumus. Īpašnieki, kam pieder esošās vides, kurās darbojas iebūvētā vispārējās plānošanas programma bez plānoto ražošanas pasūtījumu ģenerēšanas, saņems e-pastu ar sīkāku informāciju par izņēmuma procesu. Iesakām jums strādāt ar partneri, lai novērtētu un plānotu migrāciju uz plānošanas optimizāciju.

Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus. Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Pieejamība
Plānošanas optimizācija pašlaik ir pieejama šādās Azure ģeogrāfiskās vietās: Amerikas Savienotās Valstis, Kanāda, Eiropa, Apvienotā Karaliste un Austrālija. Ja mēģināsit instalēt pievienojumprogrammu no cita ģeogrāfiskā reģiona, tad LCS rādīs ziņojumu, ka šī ģeogrāfiskā vērtība netiek atbalstīta.

Ņemiet vērā, ka plānošanas optimizācija neatbalsta Dynamics 365 Supply Chain Management lokālās izvietošanas.

### <a name="licensing"></a>Licencēšana

Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.

### <a name="install-the-add-in"></a>Pievienojumprogrammas instalēšana

Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management. Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).

> [!NOTE]
> Plānošanas optimizācijas prasība ir ar LCS iespējota augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku. Ja mēģināsit instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta, un tā būs jāatceļ.

1. Piesakieties LCS un atveriet vēlamo vidi.
1. Doties **Pilna detalizēta informācija**.
1. Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.
1. Atlasiet **Instalēt jaunu pievienojumprogrammu**.
1. Atlasiet **Plānošanas optimizācija**.
1. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.
1. Atlasiet **Instalēt**.
1. Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.
1. Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina). Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.

Plānošanas optimizācijas papildinājuma instalēšanas galvenais nolūks ir savienot pakalpojumu un vidi. Tāpēc jums ir jāinstalē pievienojumprogramma atsevišķi katrai videi, kurā izmantosiet plānošanas optimizāciju neatkarīgi no tā, kāds kods tiek pārvietots starp vidēm.

### <a name="planning-optimization-integration"></a>Plānošanas optimizācijas integrēšana

Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.

#### <a name="connection-status"></a>Savienojuma statuss

Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu. Nākamajā tabulā ir parādītas iespējamās vērtības.

| Savienojuma statuss | Apraksts | Vai var izmantot plānošanas optimizāciju? |
|---|---|---|
| Savienojums izveidots | Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management. | Jā |
| Savienojuma iespējošana | Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Savienojums pārtraukts | Nav savienojuma ar plānošanas optimizācijas pakalpojumu. Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā. | Nē |
| Savienojuma atspējošana | Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts. | Nē |
| Statusa iegūšana | Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma. | Nē |

#### <a name="the-use-planning-optimization-option"></a>Iespēja Plānošanas optimizācijas izmantošana

Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:

- **Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.
- **Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.

> [!NOTE]
> Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.

### <a name="integration-with-the-setup"></a>Integrēšana ar iestatījumu

Ja plānošanas optimizācija ir ieslēgta, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu. Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.

## <a name="additional-resources"></a>Papildu resursi

[Priekšskatījuma noteikumi un nosacījumi](https://go.microsoft.com/fwlink/?linkid=2015274)

[Plānošanas optimizācijas apskats](planning-optimization-overview.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]