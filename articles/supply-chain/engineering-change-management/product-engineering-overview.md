---
title: Inženierzinātnes izmaiņu pārvaldības apskats (satur video)
description: Šajā rakstā ir sniegts pārskats par inženierzinātnes izmaiņu pārvaldību, kas palīdz plānot un pārvaldīt preču versiju vadību, kā arī pārvaldīt preces dzīves cikla un inženierzinātnes izmaiņas.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a27548fff9728c74814fb92438da1d0c17b5e2b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067398"
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

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Iepriekšējais video ([mainīt pārvaldības iespējas Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ir iekļauts finanšu [un operāciju iespējas, kas](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) pieejamas YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošana sistēmā

Pirms izmantot inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu, kā aprakstīts *Inženierzinātnes izmaiņu pārvaldības* inženierzinātnes izmaiņu pārvaldības funkciju un tā konfigurācijas atslēgu. Ja vēlaties arī izsekot versiju dimensijai produktiem transakcijās (neobligāti), ir arī jāiespējo gan līdzeklis *Produkta versiju dimensija*, gan tā konfigurēšanas atslēga. Pēc tam, kad šie priekšnosacījumi ir pēc vajadzības iestatīti, varēsit arī iespējot neobligātos līdzekļus inženiertehnisko izmaiņu pārvaldībai.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Ieslēgt vai izslēgt galvenās inženierzinātnes izmaiņu pārvaldības funkcijas

Lai ieslēgtu vai izslēgtu galvenās inženierzinātnes izmaiņu pārvaldības funkcijas, izpildiet šīs darbības. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25 *inženierzinātnes* izmaiņu pārvaldības līdzeklis ir ieslēgts pēc noklusējuma.

1. Atvēriet darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Pārbaudīt, vai nav atjauninājumu.
1. Ja nepieciešams, mainiet *vai izslēdziet* līdzekli ar nosaukumu Inženierzinātnes izmaiņu pārvaldība.
1. Ja vēlaties izsekot preču versijas dimensiju darbībās (nav obligāti), grieziet līdzekli, kura nosaukums ir *Preces dimensijas versija*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Ieslēgt vai izslēgt nepieciešamās konfigurācijas atslēgas

Tad ieslēdziet konfigurācijas atslēgas, veicot šādas darbības. Tie netiek ieslēgti pēc noklusējuma.

1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Izvērst zaru **Tirdzniecība**.
1. Iespējojiet vai deaktivizējiet galvenās funkcijas konfigurācijas atslēgu, izmantojot izvēles **rūtiņu Inženierzinātnes izmaiņu** pārvaldība.
1. Izvērsiet **Inženiertehnisko izmaiņu pārvaldība** zaru un atzīmējiet vai notīriet šādas izvēles rūtiņas pēc vajadzības (atkarībā no funkcijām, ko vēlaties izmantot):

    - **Atribūtu meklēšana** - atzīmējiet šo izvēles rūtiņu, lai iespējotu [atribūtu meklēšanas līdzekli](engineering-attributes-and-search.md). Ieteicams iespējot šo funkciju, taču, ja to neizmantosit, to var notīrīt.
    - **Izmaiņu pārvaldība procesa ražošanai** - atzīmējiet šo izvēles rūtiņu, ja vēlaties izmantot Inženiertehnisko izmaiņu pārvaldības līdzekļus, lai pārvaldītu izmaiņas procesa ražošanas formulās. Ja formulas nav jāpārvalda, šo izvēles rūtiņu var notīrīt. Papildinformāciju skatiet [pPrvaldīt izmaiņas formulās un to sastāvdaļās](manage-formula-changes.md).

1. Ja arī vēlaties izmantot versijas dimensiju, atzīmējiet izvēles rūtiņu **Preces dimensija – versija**. (Šī izvēles rūtiņa atrodas tālāk sarakstā, nevis ligzdots zem **Inženierzinātnes izmaiņu pārvaldības** zars.) Ja šī funkcija nav nepieciešama, varat notīrīt šo izvēles rūtiņu.
1. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Lai nodrošinātu, ka konfigurācijas atslēgas ir pareizi atjauninātas, lai atspoguļotu izmaiņas, datu bāze ir jāsinhronizē. Atkarībā no tā, pie kāda tipa vides jūs strādājat, veiciet vienu no tālāk minētajiem soļiem:
    - **1. pakāpes (izstrādes) vidēm**: atveriet projektu programmā Microsoft Visual Studio un pēc tam atlasiet **Dynamics 365 Sinhronizēt \> datu bāzes sinhronizāciju \>**.
    - **2. pakāpes (un augstākām) vidēm**: datu bāze automātiski tiek sinhronizēta pēc vides izvietošanas uzturēšanas režīmā un ārpus tā, tādēļ varat izlaist šo darbību.

### <a name="turn-on-additional-engineering-change-management-features"></a>Papildu inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošana sistēmā

Pēc pamata inženiertehnisko izmaiņu pārvaldības līdzekļu iespējošanas un to konfigurācijas atslēgu iespējošanas, līdzekļa pārvaldībai tiek pievienotas dažas papildu neobligātas inženiertehnisko izmaiņu pārvaldības iespējas. Katrs no šiem līdzekļiem ir uzskaitīts modulī **Inženiertehnisko izmaiņu pārvaldība**. Tālāk sniegtajā tabulā ir aprakstīti visi neobligātie līdzekļi un saites uz papildinformāciju. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25 visi šie līdzekļi ir ieslēgti pēc noklusējuma, bet joprojām varat izvēlēties izslēgt tos.

| Līdzekļa nosaukums līdzekļu pārvaldībā | Apraksts | Līdzekļa statuss |
|---|---|---|
| Izmaiņu pārvaldības iespējošana esošajām precēm | <p>Šis līdzeklis ļauj konvertēt esošās preces inženiertehniskajās precēs, lai varat sākt to pārvaldību, izmantojot inženiertehnisko izmaiņu pārvaldību.</p><p>Papildinformācija: [Izmaiņu pārvaldības iespējošana esošām precēm](change-management-existing-products.md).</p> |
| Tehniskie paziņojumi ražotājiem | <p>Kad tiek nomainīta preces inženiertehnika, ir svarīgi par šīm izmaiņām informēt ražošanas daļu. Tādējādi ražošanas darbinieki var veikt atbilstošo darbību, piemēram, aizstāt komponenti, mainīt pavadzīmi (BOM) vai maršrutu. Šis līdzeklis ļauj ziņot ražošanas daļai par izmaiņām ražotajos produktos.</p><p>Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).</p> |
| Uzlabota atribūtu pārmantošana tehnisko izmaiņu pārvaldībai | <p>Šis līdzeklis vienkāršo pabeigto preču vai starpproduktu atribūtus. Kad šis līdzeklis ir iespējots, ir vieglāk identificēt visus atribūtus, kuri ietilpst elementā, un varat atlasīt tos atribūtus, kurus vajadzētu izplatīt no šī elementa uz tā vecākelementu. Šis līdzeklis noder, ja, piemēram, viens pabeigtā produkta komponents ir trausls, toksisks vai uzliesmojošs, jo jūs varat viegli identificēt trauslo, toksisko vai uzliesmojošo atribūtu un izplatīt to uz pabeigto preci.</p><p>Papildinformāciju skatiet rakstā [Inženiertehniskie atribūti un inženiertehnisko atribūtu meklēšana](engineering-attributes-and-search.md).</p> |
| Preces gatavības pārbaudes | <p>Šis līdzeklis ļauj iestatīt gatavības pārbaudes standarta (ne-tehniskajām) precēm. Lietojiet preču gatavības pārbaudes, lai pārliecinātos, ka katra prece ir pilnībā definēta un ka visas vajadzīgās politikas tiek konfigurētas, pirms prece ir padarīta pieejama un izmantota transakcijās. Atspējojot šo līdzekli pēc tā lietošanas kādu laiku, tiks dzēstas visas esošās standarta preču gatavības pārbaudes.</p><p>Papildinformāciju skatiet sadaļā [Produktu gatavība](product-readiness.md).</p> |
| Pārvaldīt izmaiņas formulās un to komponentos | <p>Šis līdzeklis ļauj izsekot izmaiņām formulu sastāvdaļās, līdzproduktos un blakusproduktos.</p><p>Papildinformāciju skatiet [pPrvaldīt izmaiņas formulās un to sastāvdaļās](manage-formula-changes.md).</p> |
| Tehnisko preču variantu ģenerēšana | <p>Šis līdzeklis ļauj ģenerēt tehnisko produktu variantus, pamatojoties pieejamajās dimensiju vērtībās.</p><p>Papildu informāciju skatiet rakstā [Variantu ģenerēšana inženierijas precēm](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

