---
title: Inženierzinātnes izmaiņu pārvaldības apskats (satur video)
description: Šajā tēmā sniegts pārskats par tehnoloģisko izmaiņu pārvaldību, kas palīdz plānot un pārvaldīt preču versiju izveidi un pārvaldīt produktu dzīves ciklus un tehnikas izmaiņas.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e9dc692061cec830f487e01a79075eda835bac23
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937664"
---
# <a name="engineering-change-management-overview"></a>Tehnoloģisko izmaiņu pārvaldības pārskats

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Līdzekļa kopsavilkums

Šodienas ražotājiem ir nepieciešama stingra preču datu pārvaldība, versiju kontrole un inženiertehnisko izmaiņu pārvaldība, lai izdotos veiksmīgai preču dzīves cikla sašaurināšanai, paaugstinātām kvalitātes un drošības prasībām un lielākai uzmanībai par preču drošību.

Inženierzinātnes izmaiņu pārvaldība preču datu pārvaldības procesam atved struktūru un nozari, kā arī sniedz iespēju precēm definēt, izlaist un pārskatīt kontrolētā veidā, ko atbalsta darbplūsmas. Izmantojot preču versijas un inženierzinātnes izmaiņu pārvaldību, varat dokumentēt, novērtēt produkta ietekmi un pielietot inženierzinātnes izmaiņas visā produkta dzīves ciklā.

Tehnikas izmaiņu pārvaldība, kas palīdz plānot un pārvaldīt preču versiju izveidi un pārvaldīt produktu dzīves ciklus un tehnikas izmaiņas. Šeit ir saraksts ar tās galvenajām iezīmēm:

- Produktu versijas
- Uzlabota preču izlaides funkcionalitāte, kas ļauj uzturēt preču pamatdatus vienā juridiskā personā (tehniskajā uzņēmumā) un publicēt pilnībā konfigurēto izlaisto preci citām juridiskajām personām
- Nosacījumi, lai apstiprinātu, ka pieprasītā informācija tiek ievadīta pirms produkta versijas aktivizēšanas (gatavības pārbaudes)
- Uzlabota preču dzīves cikla pārvaldība, izmantojot detalizēti sadalītu kontroli, kad izlaisto preci var izmantot īpašos biznesa procesos
- Tehnikas izmaiņu pieprasījumi, ko atbalsta darbplūsmas
- Tehnikas izmaiņu pasūtījumi, ko atbalsta darbplūsmas

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Iepriekšējais video ([Izmaiņu pārvaldības iespējas sistēmā Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas pieejams YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošana sistēmā

Pirms izmantot inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu, kā aprakstīts *Inženierzinātnes izmaiņu pārvaldības* inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu. Ja vēlaties arī izsekot versiju dimensijai produktiem transakcijās (neobligāti), ir arī jāiespējo gan līdzeklis *Produkta versiju dimensija*, gan tā konfigurēšanas atslēga. Pēc tam, kad šie priekšnosacījumi ir pēc vajadzības iestatīti, varēsit arī iespējot neobligātos līdzekļus inženiertehnisko izmaiņu pārvaldībai.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Pamata inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošana sistēmā

Vispirms, ieslēdziet šīs funkcijas, veicot šādas darbības.

1. Atvēriet darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Pārbaudīt, vai nav atjauninājumu.
1. Ieslēdziet līdzekli, kura nosaukums ir *Tehnikas izmaiņu pārvaldība*.
1. Pēc tam, ja vēlaties to izmantot, iespējojiet arī funkciju ar nosaukumu *Preces dimensijas versija*.

### <a name="turn-on-the-required-configuration-keys"></a>Vajadzīgo konfigurācijas atslēgu iespējošana

Tad ieslēdziet konfigurācijas atslēgas, veicot šādas darbības.

1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Izvērst zaru **Tirdzniecība**.
1. Iespējojiet galvenos līdzekļu konfigurācijas atslēgu, atzīmējot izvēles rūtiņu **Inženiertehnisko izmaiņu pārvaldība**.
1. Izvērsiet **Inženiertehnisko izmaiņu pārvaldība** zaru un atzīmējiet vai notīriet šādas izvēles rūtiņas pēc vajadzības (atkarībā no funkcijām, ko vēlaties izmantot):

    - **Atribūtu meklēšana** - atzīmējiet šo izvēles rūtiņu, lai iespējotu [atribūtu meklēšanas līdzekli](engineering-attributes-and-search.md). Ieteicams iespējot šo funkciju, taču, ja to neizmantosit, to var notīrīt.
    - **Izmaiņu pārvaldība procesa ražošanai** - atzīmējiet šo izvēles rūtiņu, ja vēlaties izmantot Inženiertehnisko izmaiņu pārvaldības līdzekļus, lai pārvaldītu izmaiņas procesa ražošanas formulās. Ja formulas nav jāpārvalda, šo izvēles rūtiņu var notīrīt. Papildinformāciju skatiet [pPrvaldīt izmaiņas formulās un to sastāvdaļās](manage-formula-changes.md).

1. Ja arī vēlaties izmantot versijas dimensiju, atzīmējiet izvēles rūtiņu **Preces dimensija – versija**. (Šī izvēles rūtiņa atrodas tālāk sarakstā, nevis ligzdota zem **Inženiertehnisko izmaiņu pārvaldība** zara.)
1. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Sākot no 2022. gada aprīļa, licences atslēgas gan **Inženierzinātnes izmaiņu pārvaldībai**, gan **Preces dimensijai - versija** tiks aktivizētas pēc noklusējuma visām jaunajām instalācijām, bet, ja nepieciešams, tās joprojām būs iespējams deaktivizēt.

### <a name="turn-on-additional-engineering-change-management-features"></a>Papildu inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošana sistēmā

Pēc pamata inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošanas un to konfigurācijas atslēgu iespējošanas, līdzekļa pārvaldībai tiek pievienotas dažas papildu neobligātas inženiertehnisko izmaiņu pārvaldības iespējas. Katrs no šiem līdzekļiem ir uzskaitīts modulī **Inženiertehnisko izmaiņu pārvaldība**. Tālāk sniegtajā tabulā ir aprakstīti visi neobligātie līdzekļi un saites uz papildinformāciju.

| Līdzekļa nosaukums līdzekļu pārvaldībā | Apraksts |
|---|---|
| Izmaiņu pārvaldības iespējošana esošajām precēm | <p>Šis līdzeklis ļauj konvertēt esošās preces inženiertehniskajās precēs, lai varat sākt to pārvaldību, izmantojot inženiertehnisko izmaiņu pārvaldību.</p><p>Papildinformācija: [Izmaiņu pārvaldības iespējošana esošām precēm](change-management-existing-products.md).</p> |
| Tehniskie paziņojumi ražotājiem | <p>Kad tiek nomainīta preces inženiertehnika, ir svarīgi par šīm izmaiņām informēt ražošanas daļu. Tādējādi ražošanas darbinieki var veikt atbilstošo darbību, piemēram, aizstāt komponenti, mainīt pavadzīmi (BOM) vai maršrutu. Šis līdzeklis ļauj ziņot ražošanas daļai par izmaiņām ražotajos produktos.</p><p>Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).</p> |
| Uzlabota atribūtu pārmantošana tehnisko izmaiņu pārvaldībai | <p>Šis līdzeklis vienkāršo pabeigto preču vai starpproduktu atribūtus. Kad šis līdzeklis ir iespējots, ir vieglāk identificēt visus atribūtus, kuri ietilpst elementā, un varat atlasīt tos atribūtus, kurus vajadzētu izplatīt no šī elementa uz tā vecākelementu. Šis līdzeklis noder, ja, piemēram, viens pabeigtā produkta komponents ir trausls, toksisks vai uzliesmojošs, jo jūs varat viegli identificēt trauslo, toksisko vai uzliesmojošo atribūtu un izplatīt to uz pabeigto preci.</p><p>Papildinformāciju skatiet rakstā [Inženiertehniskie atribūti un inženiertehnisko atribūtu meklēšana](engineering-attributes-and-search.md).</p> |
| Preces gatavības pārbaudes | <p>Šis līdzeklis ļauj iestatīt gatavības pārbaudes standarta (ne-tehniskajām) precēm. Lietojiet preču gatavības pārbaudes, lai pārliecinātos, ka katra prece ir pilnībā definēta un ka visas vajadzīgās politikas tiek konfigurētas, pirms prece ir padarīta pieejama un izmantota transakcijās. Atspējojot šo līdzekli pēc tā lietošanas kādu laiku, tiks dzēstas visas esošās standarta preču gatavības pārbaudes.</p><p>Papildinformāciju skatiet sadaļā [Produktu gatavība](product-readiness.md).</p> |
| Pārvaldīt izmaiņas formulās un to komponentos | <p>Šis līdzeklis ļauj izsekot izmaiņām formulu sastāvdaļās, līdzproduktos un blakusproduktos.</p><p>Papildinformāciju skatiet [pPrvaldīt izmaiņas formulās un to sastāvdaļās](manage-formula-changes.md).</p> |
| Tehnisko preču variantu ģenerēšana | <p>Šis līdzeklis ļauj ģenerēt tehnisko produktu variantus, pamatojoties pieejamajās dimensiju vērtībās.</p><p>Papildu informāciju skatiet rakstā [Variantu ģenerēšana inženierijas precēm](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
