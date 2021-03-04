---
title: Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem
description: Šajā tēmā sniegts pārskats par to, kā sertifikāti tiek izmantoti mazumtirdzniecības veikalos.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 75edc1b683c4ea6c2bac8e509e6f6da8c56c5e6a
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665252"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Pārskats

Šajā tēmā sniegts pārskats par sertifikātu profiliem, kas ir pieejami Microsoft Dynamics 365 Commerce. Šī funkcionalitāte paplašina līdzekli [Mazumtirdzniecības kanālu noslēpumu pārvaldība](../dev-itpro/manage-secrets.md), pievienojot atbalstu lokālajiem sertifikātiem.

Lai gan pārdošanas punkts (POS) darbojas bezsaistes režīmā, tas nevar piekļūt sertifikātiem, kas tiek glabāti galvenajā glabātuvē. Tā vietā ir jāizmanto lokāls sertifikāts. Tālāk ir norādītas atbalstītās iespējas:

- Lokālo sertifikātu izmantošana galvenās glabātuves rezerves scenārijos
- Lokālo sertifikātu izmantošana bez galvenās glabātuves (piemēram, lokālajā instalācijā)
- Pakāpeniska sertifikātu atjaunināšana, kur daži veikali un termināli izmanto jauno sertifikāta versiju, bet citi veikali un termināli turpina izmantot iepriekšējo versiju

Sertifikātu profilu funkcionalitāte ļauj norādīt noklusējuma sertifikātu un iestatīt kārtību, kādā tiek meklēti sertifikāti tajā pašā sertifikāta profilā. Šī funkcionalitāte arī nodrošina līdzīgu iestatīšanas pieeju lokālajiem sertifikātiem un Key Vault sertifikātiem. Varat pievienot uzņēmumam raksturīgos iestatījumus sertifikātiem, bet unikālu starpuzņēmumu identifikatoru katram sertifikātam var izmantot Commerce kanālos.

### <a name="scenarios"></a>Scenāriji

Sertifikātu profilu funkcionalitāte atbalsta šādus scenārijus pakalpojuma Commerce kanālos:

- Lokāla sertifikāta izmantošana galvenās glabātuves rezerves scenārijos. Šie ir daži rezerves scenāriju piemēri:

    - Galvenās glabātuves krātuve nav pieejama.
    - Sertifikāts nav atrodams galvenās glabātuves krātuvē.
    - POS darbojas bezsaistes režīmā.

- Lokālo sertifikātu izmantošana tos neuzglabājot galvenajā glabātuvē (piemēram, lokālajā instalācijā).
- Pakāpeniska sertifikātu atjaunināšana, kur sertifikāta jaunā versija tiek izmantota tikai veikalos vai terminālos, kur jaunā versija jau ir pieejama.
- Viena un tā paša sertifikāta izmantošana vairākos uzņēmumos.

## <a name="set-up-certificate-profiles"></a>Sertifikātu profilu iestatīšana

Šajā procedūrā ir aprakstīts, kā iestatīt sertifikātu profilus. Pirms sertifikātu profilu izmantošanas pakalpojuma Commerce kanālos, veiciet tālāk norādītās darbības, lai konfigurētu iestatījumus.

1. Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem**.
2. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sertifikātu profili**.
3. Izveidojiet ierakstu un iestatiet tā laukus **Sertifikāta profils**, **Nosaukums** un **Apraksts**.

    > [!NOTE]
    > Sertifikāta profils ir unikāls sertifikāta identifikators visos uzņēmumos un Commerce komponentos.

3. Cilnē **Juridiskās personas** pievienojiet rindu un atlasiet juridisko personu (uzņēmumu), kam tiks izmantots pašreizējais sertifikāta profils. Ja sertifikāta profils tiks izmantots vairākām juridiskajām personām, atkārtojiet šo darbību, lai pievienotu rindu katrai juridiskajai personai.
4. Atlasiet **Iestatījumi**, lai atvērtu lapu **Sertifikāta profila iestatījumi**, kurā varat ievadīt uzņēmumam raksturīgos sertifikāta profila iestatījumus.

### <a name="certificate-profile-settings"></a>Sertifikāta profila iestatījumi

Atlasot **Iestatījumi** sertifikāta profila rindām, tiek parādīta lapa **Sertifikāta profila iestatījumi**. Šajā lapā varat norādīt, kurus sertifikātus var izmantot, kad pašreizējais sertifikāta profils tiek izsaukts Commerce kanālos. Varat arī norādīt kārtību, kādā ir jāmeklē sertifikāti.

> [!NOTE]
> Lauks **Prioritāte** tiek iestatīts automātiski. Vērtība **1** norāda augstāko prioritāti. Kad lapā **Sertifikāta profila iestatījumi** tiek pievienota jauna rinda, tās prioritāte tiek iestatīta uz skaitli, kas ir lielāks par iepriekšējās rindas prioritāti. Lai mainītu konkrētas rindas prioritāti, atlasiet rindu un pēc tam atlasiet **Pārvietot uz augšu**, lai palielinātu prioritāti, vai **Pārvietot uz leju**, lai samazinātu prioritāti.

Kad lapā **Sertifikāta profila iestatījumi** pievienojat jaunu rindu, iestatiet šādus laukus:

- **Atrašanās vietas tips** – atlasiet atrašanās vietu, kur sertifikāts ir saglabāts. Šim laukam ir divas iespējamās vērtības: **Lokāls sertifikāts** un **Key Vault**.
- **Key Vault sertifikāts** – šis lauks ir obligāts, ja lauks **Atrašanās vietas tips** tiek iestatīts uz **Key Vault**. Izmantojiet to, lai norādītu Key Vault sertifikāta noslēpumu.

    > [!NOTE]
    > Pirms sertifikātu profilos izmantot Key Vault sertifikātu, pārliecinieties, vai esat augšupielādējis sertifikātu galvenās glabātuves krātuvē, un izpildiet norādījumus sadaļā [Azure Key Vault klienta iestatīšana](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Veikala nosaukums** – šis lauks ir neobligāts, un tas ir pieejams tikai iestatot lauku **Atrašanās vietas tips** uz **Lokāls sertifikāts**. Izmantojiet to, lai norādītu noklusējuma veikala nosaukumu, kas jāizmanto lokālo sertifikātu meklēšanai.
- **Veikala atrašanās vieta** – šis lauks ir neobligāts, un tas ir pieejams tikai iestatot lauku **Atrašanās vietas tips** uz **Lokāls sertifikāts**. Izmantojiet to, lai norādītu noklusējuma veikala atrašanās vietu, kas jāizmanto lokālo sertifikātu meklēšanai.

    > [!NOTE]
    > Noklusējuma veikala nosaukums un veikala atrašanās vieta tiek pievienota, lai vienkāršotu lokālo sertifikātu meklēšanas procesu Commerce Runtime. X509StoreProvider satur sarakstu ar mapēm, kur tiek glabāti sertifikāti. Ja noklusējuma veikala nosaukums un noklusējuma veikala atrašanās vieta nav norādīta, X509StoreProvider mēģina atrast sertifikātu citās saraksta mapēs.

- **Īssavilkums** – šis lauks ir obligāts, un tas ir pieejams tikai iestatot lauku **Atrašanās vietas tips** uz **Lokāls sertifikāts**. Izmantojiet to, lai norādītu sertifikāta īssavilkumu.
- **Komentāri** – šis lauks ir neobligāts, un tas ļauj lietotājiem ievadīt piezīmes.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Darbplūsma: sertifikātu meklēšana Commerce Runtime

Šī ir pamata darbplūsma, kas tiek izmantota, meklējot sertifikātu, kad sertifikāta profils tiek izsaukts Commerce Runtime.

1. Sistēma nosaka, vai sertifikāta profilā ir uzņēmumam raksturīgie iestatījumi pašreizējai juridiskajai personai.
1. Sistēma mēģina atrast sertifikātu, izmantojot vērtības, kas norādītas lapas **Sertifikāta profila iestatījumi** rindai, kur lauks **Prioritāte** ir iestatīts uz **1**.

    - Ja lauks **Atrašanās vietas tips** ir iestatīts uz **Key Vault**, tad lauka **Key Vault sertifikāta noslēpums** vērtība tiek izmantota, lai meklētu sertifikātu lapā **Galvenās glabātuves parametri**. Pēc tam sertifikāts tiek meklēts galvenās glabātuves krātuvē.
    - Ja lauks **Atrašanās vietas tips** ir iestatīts uz **Lokāls sertifikāts**, tad X509StoreProvider vispirms meklē sertifikātu, izmantojot noklusējuma veikala nosaukumu un veikala atrašanās vietu, ja šie parametri ir norādīti. Pēc tam tas meklē visās citās mapēs, kas atrodas mapju sarakstā.

1. Ja sertifikāts netiek atrasts, process tiek atkārtots ar rindu, kurā lauks **Prioritāte** ir iestatīts uz **2**, un tā tālāk.

> [!NOTE]
> Sertifikāts netiek atrasts, ja sertifikāta profilam nav iestatījumu pašreizējai juridiskajai personai, vai ja sertifikāta meklēšana ir neveiksmīga visām rindām lapā **Sertifikāta profila iestatījumi**.

#### <a name="caching-the-results-of-certificate-searches"></a>Sertifikātu meklēšanas rezultātu kešdarbe

Sertifikātu meklēšanas rezultāti tiek saglabāti kešatmiņā. Kešatmiņas noklusējuma derīguma termiņš ir viena stunda. Tomēr šo termiņu var pielāgot un iestatīt uz maksimālo 24 stundu vērtību.

### <a name="gradual-update"></a>Pakāpeniska atjaunināšana

Ja tiek ieviesta jauna sertifikāta versija, ko nevar atjaunināt visos veikalos vienlaicīgi, sertifikātu profilu funkcionalitāte ļauj sertifikātu atjaunināt pakāpeniski.

1. Atrodiet sertifikāta profilu un rindu, kas jāatjaunina, un pēc tam atlasiet **Iestatījumi**.
1. Pievienojiet rindu un norādiet iestatījumus, kas saistīti ar jaunāko sertifikāta versiju.
1. Palieliniet jaunās rindas **Prioritāte** vērtību. Izmantojiet pogu **Pārvietot uz augšu**, lai pārvietotu rindu tā, lai tā būtu virs tā paša sertifikāta iepriekšējās versijas rindas.

> [!NOTE]
> Vispirms jaunā sertifikāta versija tiks izsaukta Commerce Runtime. Ja sertifikāts vēl nav atjaunināts noteiktā veikalā vai noteiktā terminālī, tiks izsaukta iepriekšējā versija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]