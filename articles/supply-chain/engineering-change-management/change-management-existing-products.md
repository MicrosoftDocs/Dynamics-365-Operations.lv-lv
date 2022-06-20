---
title: Izmaiņu pārvaldības iespējošana esošajām precēm
description: Šajā rakstā skaidrots, kā iespējot izmaiņu pārvaldību esošajiem produktiem. Tas apraksta arī gadījumus, kad jūsu spēja iespējot izmaiņu pārvaldību ir ierobežota.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9f99529abebdf5490f158c6f0a7be4519449e9f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893473"
---
# <a name="enable-change-management-on-existing-products"></a>Izmaiņu pārvaldības iespējošana esošajām precēm

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā iespējot izmaiņu pārvaldību esošajiem produktiem. Tas apraksta arī gadījumus, kad jūsu spēja iespējot izmaiņu pārvaldību ir ierobežota.

Kad iespējojat izmaiņu pārvaldību esošai precei, varat izveidot šīs preces versijas un izsekot izmaiņas, kas tai veiktas visā tās dzīves laikā. Tāpēc šīs izmaiņas var izsekot, izmantojot izmaiņu pasūtījumus. Lai iespējotu izmaiņu pārvaldību, atbilstošās preces ir jāpārvērš par *tehnoloģiju krājumiem* (sauktiem arī par inženierzinātnes produktiem). Inženierzinātnes preces ir preces, kas ir versija un tiek pārvaldītas, izmantojot izmaiņu pārvaldību. Vednis ir nodrošināts, lai tas vadītu jūs caur pārvēršanas procesu.

## <a name="turn-this-feature-on-or-off"></a>Ieslēgt vai izslēgt šo līdzekli

Šajā rakstā aprakstītajai funkcionalitātei ir nepieciešams, lai *jūsu* *sistēmai* būtu ieslēgta gan inženierzinātnes izmaiņu pārvaldība, gan Iespējot esošo preču izmaiņu pārvaldību. Papildinformāciju par to, kā ieslēgt vai izslēgt šos līdzekļus, skatiet inženierzinātnes [izmaiņu pārvaldības pārskatā](product-engineering-overview.md).

## <a name="restrictions-and-limitations"></a>Aizliegumi un ierobežojumi

Ne visus preču tipus var konvertēt uz visiem citiem tipiem. Pastāv šādi ierobežojumi un ierobežojumi:

- Konvertējot preci par tehnoloģiju preci, tā paliek kā *prece*. Tā nekļūst par *preces šablonu*.
- Konvertējot preču šablonu, kam ir noteikta dimensiju kopa, šīs dimensijas tiek uzturētas pēc izmaiņu beigām. Piemēram, konvertējot preces šablonu, kam ir lieluma dimensija, lieluma dimensija tiks paturēta.

Tāpēc, ja jums ir atšķirīga prece, to var mainīt tikai uz tehnikas preci, kas neizseko preces dimensiju darījumos (t.i., versijas dimensija netiek izmantota). Papildinformāciju par šīm problēmām skatiet pārējās šī raksta sadaļās.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Sagatavošanās pārvēršanai, izveidojot visas nepieciešamās tehnoloģiju preču kategorijas

*Inženierzinātnes produktu kategorija* ir jāpiešķir katrai tehnikas precei. Šī piešķire tiks izpildīta, palaižot vedni **Pārvērst par inženierzinātnes preci**. *Pirms* šo preču pārveidošanas visām atbilstošām standarta precēm jābūt inženierzinātnes produktu kategorijām.

Inženierzinātnes preču kategorija sniedz pamatu inženierzinātnes produkta izveidošanai, un tā izveido noklusēto vērtību un politiku kopu. Inženiertehniskie atribūti un to noklusējuma vērtības (kā definēts inženierzinātnes kategorijai) tiek piemēroti arī rezultātā iegūtajam inženiertehniskajam produktam. Varat pēc vajadzības rediģēt atribūtu vērtības un/vai pievienot papildu inženiertehniskos atribūtus rezultātā iegūtajam produktam.

Tehniskajai preces kategorijai jāatbilst piešķiramajam projektam. Piemēram, preces tipam un dimensiju grupai jāsakrīt gan ar preci, gan ar tās inženierzinātnes preču kategoriju. Papildinformāciju skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

> [!IMPORTANT]
> Vednis **Pārvērst par inženierzinātnes preci** var pārveidot preces tikai par inženierzinātnes precēm, kur versija darbībās nav izsekota. Tāpēc opciju **Izsekot versiju darbībās** ir jāiestata uz *Nē* tehnoloģiju preču kategorijām, kuras izveidojat, lai konvertētu esošās preces.

Papildinformāciju par tehnisko produktu kategoriju izveidi skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Palaist vedni Pārvērst par tehnisko preci

Vednis **Pārvērst par tehnoloģisku preci** palīdz pārvērst vienu vai vairākas esošas preces par tehnikas precēm. Tā pārvērš preces par tehnoloģiju precēm (versiju precēm), kur versija nav izsekota darījumos (t.i., versijas dimensija netiek izmantota). Pēc pārvēršanas pabeigšanas varat pārvaldīt preces, izmantojot inženierzinātnes izmaiņu pārvaldību.

Pārveidošana ir pastāvīga. Tādēļ jūs to nevarēsit atsaukt vēlāk. 

Katra pārveidotā inženierzinātnes prece turpinās būt izlaista tajā pašā kompānijā, kurā tika izlaista sākotnējā prece. Tomēr inženierzinātnes materiālu komplekts (MK) un maršruti netiks automātiski nodoti šiem uzņēmumiem.

Izpildiet šīs darbības, lai **palaistu pārvērstu tehnoloģiju preču** vedni un pārvērstu preci par tehnoloģiju preci.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atzīmējiet izvēles rūtiņu katrai dimensijai, ko vēlaties pārvērst.
1. Darbības rūtī, cilnē **Inženieris**, kas atrodas grupā **Tehnisko izmaiņu pārvaldība**, atlasiet **Pārvērst par tehnoloģisku preci**, lai apskatītu produkta versijas.
1. Vedņa pirmā lapa ir **Sveiciena** lapa. Ja jums vēl nav zināms pārvēršanas process, rūpīgi izlasiet informāciju par šo lapu. Kad esat gatavs publicēt, atlasiet **Tālāk**.
1. Lapā **Atlasīt konvertējamās preces detalizētu informāciju** tiek parādīta katra prece, ko atlasījāt pirms vedņa atvēršanas. Pārbaudīt sarakstu. Izmantojiet rīkjoslas pogas **Jauns** and **Dzēst**, lai pievienotu un noņemtu produktus pēc nepieciešamības.
1. Izmantojiet tālāk norādītos laukus, kas atrodas režģa augšpusē, lai piešķirtu noklusējuma vērtības katrai uzskaitītajām precei. (Pēc pārvēršanas pabeigšanas šīs vērtības var mainīt atsevišķiem produktiem.) Noklusējuma vērtības netiks piešķirtas precēm, kurās atbilstošā vērtība jau ir piešķirta.

    - **Noklusējuma inženierzinātnes kategorija** - atlasiet sākotnējo tehnoloģiju preču kategoriju, ko piešķirt katrai uzskaitītajai precei. Atlasītā kategorija tiks lietota tikai precēm, kuras ir saderīgas ar to.
    - **Noklusējuma versija** - ievadiet sākotnējo produkta versiju, ko piešķirt katrai uzskaitītajai precei. Katrai inženierzinātnes precei ir vismaz viena tehnoloģiju versija.
    - **Noklusējuma dzīves cikla stāvoklis** – atlasiet sākotnējo preces dzīves cikla stāvokli, ko piešķirt katrai uzskaitītajām precei.
    - **Pašreizējais MK būs daļa no tehniskais produkta** - atzīmējiet šo izvēles rūtiņu, ja pašreizējais MK katrai uzskaitītai precei ir jāizmanto kā tehniskās preces MK.

    Plašāku informāciju par preču iestatījumiem skatiet nākamo darbību.

1. Pārskatiet katru režģī norādīto preci un novērtējiet, kā arī uz to attiecas piešķirtās noklusējuma vērtības. Katrai rindai pārskatiet šādu informāciju un iestatiet jebkurus atbilstošos laukus:

    - **Preces numurs** – preces numurs.
    - **Preces nosaukums** – preces nosaukums.
    - **Tehnoloģiskā kategorija** — atlasiet tehnoloģisko preču kategoriju, kurai prece piederēs pēc tās pārvēršanas. Katrai precei jau ir jābūt atbilstošai kategorijai, kā paskaidrots šī raksta iepriekšējā sadaļā. Kategorija ir jāpiešķir katrai precei.
    - **Versija** - ievadiet sākotnējo produkta versiju, ko piešķirt katrai uzskaitītajai precei. Piemēram, varat atlasīt numuru, kas iekļaujas numuru sērijā, ko kategorija jau lieto. Katra tehniskā versija saglabā šai versijai raksturīgos tehniskos datus. Papildinformāciju skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).
    - **Preces dzīves cikla stāvoklis** — atlasiet preces dzīves cikla stāvokli, kurā precei ir jābūt pēc tās pārvēršanas. Preces dzīves cikla stāvoklis ļauj kontrolēt, kuras darbības ir atļautas dotajā tehnoloģiju versijā. Papildinformāciju skatiet šeit: [Produktu dzīves cikla stāvokļi un darījumi](product-lifecycle-state-transactions.md).
    - **Ir MK** - atzīmēta izvēles rūtiņa norāda, ka precei ir MK. Šīs izvēles rūtiņas iestatījums var palīdzēt jums izlemt, kā iestatīt **Pašreizējo MK, kas būs daļa no inženierzinātnes preces** izvēles rūtiņu.
    - **Pašreizējais MK būs daļa no tehniskais produkta** - atzīmējiet šo izvēles rūtiņu, ja pašreizējais MK katrai uzskaitītai precei ir jāizmanto kā tehniskās preces MK. Tad šo MK pārvaldīs inženierzinātnes izmaiņu pārvaldība. Ja precei nav MK vai vēlaties manuāli izveidot MK pārveidotai precei vēlāk, notīriet šo izvēles rūtiņu.
    - **Ir kļūdas** – atzīmēta izvēles rūtiņa norāda, ka preces iestatījumos ir viena vai vairākas kļūdas. Piemēram, preces tips vai dimensiju grupa var neatbilst kategorijai. Preces, kurām ir kļūdas, tiks izlaistas, un tās netiks pārvērstas.

1. Kad esat beidzis, rīkjoslā atlasiet **Pārbaudīt**, lai pārbaudītu preces iestatījumus. Katrai rindai izvēles rūtiņa **Ir kļūdas** tiks atjaunināta, lai norādītu preces statusu. Pielāgojiet vērtības, līdz katras preces iestatījumos nav kļūdu.
1. Ja visas preces ir pareizi iestatītas, atlasiet **Tālāk**, lai turpinātu.
1. Lapā **Apstiprināt atlasi** tiek rādīts to preču skaits, kuru iestatījumos nav kļūdu un tādēļ ir gatavas pārvēršanai. Tajā ir norādīts arī to preču skaits, kas tiks izlaistas kļūdu dēļ. Lai palaistu pārvēršanu kā pakešuzdevumu, iestatiet opciju **Palaist pakešuzdevumā** uz *Jā*.
1. Atlasiet **Pabeigt**, lai lietotu iestatījumus un sāktu preču pārvēršanu par tehnikas precēm.

> [!NOTE]
> Ja sistēma ir iestatīta manuāli pieņemt preces, pirms tās tiek izlaistas, katra konvertētā prece ir jāpieņem, atbilstošos uzņēmumos izmantojot lapu **Atvērt preču laidienus**. Papildinformāciju skatiet sadaļā [Pārskatīt un akceptēt produktu, pirms to izlaidīsiet vietējā uzņēmumā](engineering-scenarios.md#accept).
