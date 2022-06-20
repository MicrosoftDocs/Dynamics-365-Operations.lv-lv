---
title: Darbs ar moduļiem
description: Šajā rakstā aprakstīts, kā un kad izmantot moduļus Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c393f1e619647795a5ae8da3a78500c1678da9f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860196"
---
# <a name="work-with-modules"></a>Darbs ar moduļiem

[!include [banner](includes/banner.md)]

Šajā rakstā aprakstīts, kā un kad izmantot moduļus Microsoft Dynamics 365 Commerce.

Moduļi ir loģiski veidošanas bloki, kas veido lapas struktūru, un tiem ir dažādi mērķi un tvērumi. Daži moduļi ir augsta līmeņa konteineri, un to vienīgais mērķis ir aizturēt un organizēt citus moduļus (pakārtotos moduļus). Citiem moduļiem, piemēram, vienkāršam attēla novietojuma modulim, ir ļoti specifisks mērķis. Citi moduļi, piemēram, karuseļa modulis, atrodas kaut kur starp šīm divām kategorijām.

Pēc noklusējuma jūsu Dynamics 365 Commerce vietnē ir ietverta moduļu bibliotēka, kas ļauj jums sasniegt pamata e-komercijas scenārijus. Jums ir jābūt iespējai izveidot vispārīgu e-komercijas vietni, vienkārši izmantojot šos moduļus. Tomēr, iespējams, vēlēsities arī pielāgot šos moduļus vai izveidot jaunus, pielāgotus moduļus specifiskām vajadzībām. Ja vēlaties izveidot pielāgotus moduļus, ir pieejams moduļa dizaina programmatūras izstrādes komplekts (SDK), lai palīdzētu jums izveidot pielāgotu moduļu bibliotēku.

## <a name="container-modules-and-slots"></a>Konteineru moduļi un sloti

Kā jau minēts iepriekš, daži moduļi ir paredzēti pakārtotu moduļu aizturēšanai. Šie moduļi ir pazīstami kā *konteineri*, un tie atļauj ligzdotu moduļu hierarhijas. Konteineru moduļi ietver *slotus*. Sloti tiek izmantoti, lai apstrādātu konteinerā esošo pakārtoto moduļu izkārtojumu un nolūku. Piemērs ir pamata lapas konteinera modulis (augšējā līmeņa modulis jebkurai lapai), kas nosaka vairākus nozīmīgus slotus.

- Galvenes slots
- Apakšgalvenes slots
- Galvenais slots
- Kājenes slots
- Apakškājenes slots

Moduļa izstrādātājs definē šos slotus un nosaka, kurus un cik daudz pakārtotos moduļus var ievietot tieši tajā. Piemēram, galvenes slots var atbalstīt tikai vienu **Virsraksta moduļa** veidu, turpretī pamatteksta slots var atbalstīt neierobežotu moduļu skaitu jebkuram veidam (izņemot citas lapas konteinera moduļus).

Autorēšanas rīkos lapas autoriem nav jāzina iepriekš, kuri moduļi var un kuri nevar tikti ievietoti katrā slotā. Kad lapu autori atlasa slotu un pēc tam mēģina atlasīt moduli, lai to pievienotu, viņi redz filtrētu moduļu veidu skatu, kas tiek atbalstīts šim slotam.

## <a name="content-modules"></a>Satura moduļi

Satura moduļos ir ietverti satura un multivides elementi, piemēram, teksts (piemēram, virsraksti, rindkopas un saites) vai līdzekļu atsauces (piemēram, attēli, video un PDF faili). Tipiskiem satura moduļu tipiem ir satura bloks, teksta bloks un promo reklāmkarogu moduļi. Šo trīs tipu moduļos var būt teksts vai multivide, un tiem nav nepieciešami pakārtotie moduļi, lai radītu kaut ko redzamu lapā.

Lielākā daļa parasto, ikdienas lapu un satura autorēšanas aktivitāšu ietver satura moduļus, galvenokārt tāpēc, ka šie moduļi definē faktisko saturu, kas tiek atveidots to pamata konteinera moduļos. Ir pieejami daudzi satura moduļi, un šie moduļi parasti ir pēdējie, ko pievienosiet ligzdoto moduļu lapas hierarhijai.

Tālāk esošajā attēlā ir parādīts, kā moduļi tiek ligzdoti pamata konteineru moduļa slotos.

![Ligzdošanas moduļi.](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moduļu pievienošana vai noņemšana

Šīs procedūras apraksta, kā pievienot un noņemt moduļus.

### <a name="add-a-module"></a>Moduļa pievienošana

Lai lapas slotam vai konteineram pievienotu moduli, veiciet tālāk minētās darbības.

1. Kreisajā struktūras rūtī vai tieši galvenajās kanvās atlasiet konteineru vai slotu, kuram var pievienot pakārtoto moduli.

    > [!NOTE]
    > Moduļa veidotājs nosaka moduļu tipu sarakstu, ko var pievienot konkrētam moduļa slotam. Veidnes autori tad var precizēt atļautās moduļa opcijas, lai palīdzētu nodrošināt saskanīgu meklēšanas programmas optimizāciju (SEO) un autorēšanas efektivitāti visām lapām, kas izveidotas no noteiktas veidnes. Kad pievienojat moduli slotam, **Pievienot moduli** dialoglodziņš tiek automātiski filtrēts, lai tiktu rādīti tikai moduļi, kas tiek atbalstīti atlasītajā konteinerā vai slotā. Šis atļauto moduļu sarakstu nosaka lapas veidne vai konteinera moduļa definīcija.

1. Ja izmantojat struktūras rūti, atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam un pēc tam atlasiet **Pievienot moduli**. Ja vadīklas izmantojat tieši kanvās, atlasiet plusa zīmi (**+**) tukšā slotā vai blakus pašlaik atlasītajam modulim un pēc tam atlasiet **Pievienot moduli**.

    > [!NOTE]
    > Ja konteiners vai slots neatbalsta jaunus pakārtotos moduļus, opcija **Pievienot moduli** nav pieejama.

1. Dialoglodziņā **Pievienot moduli** meklējiet moduli, ko pievienot lapai.

    > [!TIP]
    > **Satura bloks** ir labs moduļa tips iesācējiem, ar ko strādāt.

1. Atlasiet **Labi**, lai atlasīto moduli pievienotu atlasītajam konteineram vai slotam jūsu lapā.

### <a name="remove-a-module"></a>Moduļa noņemšana

Lai no lapas slota vai konteinera noņemtu moduli, veiciet tālāk minētās darbības.

1. Struktūras rūtī pa kreisi izvēlieties daudzpunktes (**...**) pogu, kas atrodas blakus moduļa nosaukumam, lai noņemtu, un pēc tam atlasiet Miskastes simbolu. Alternatīvi galvenajā kanvā var izvēlēties miskastes simbolu, kas atrodas atlasītajā moduļa rīkjoslā.
1. Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt moduli, atlasiet **Labi**.

## <a name="move-a-module-to-a-new-position"></a>Centrālā moduļa pārvietošana jaunā pozīcijā

Lai pārvietotu moduli uz jaunu pozīciju jūsu lapā, izmantojiet jebkuru no šīm metodēm.

### <a name="move-a-module-using-the-outline-pane"></a>Moduļa pārvietošana, izmantojot struktūras rūti

Lai moduli pārvietotu, izmantojot struktūras rūti, veiciet šādas darbības.

1. Atlasiet un turiet moduli, ko vēlaties pārvietot struktūras rūtī, pēc tam velciet moduli uz jaunu pozīciju struktūrā. Zilā rinda struktūrskatā un kanvās norāda, kur modulis var tikt novietots.
1. Izlaidiet moduli, lai to nomestu jaunajā pozīcijā.

### <a name="move-a-module-directly-within-the-canvas"></a>Moduļa pārvietošana tieši kanvas ietvaros

Lai moduli pārvietotu tieši kanvās, veiciet šādas darbības.

1. Atlasiet moduli, kuru vēlaties pārvietot uz kanvām. 
1. Moduļa rīkjoslā izvēlieties augšupvērstu vai lejupvērstu bultiņas simbolu un pēc tam velciet bultiņu uz jaunu pozīciju lapā. Zilā rinda kanvās un struktūrskatā norāda, kur modulis var tikt novietots. Ja moduli nevar pārvietot uz augšu vai uz leju, šis bultiņas simbols tiks pelēkots. 
1. Izlaidiet moduli, lai to nomestu jaunajā pozīcijā.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Moduļa pārvietošana, izmantojot daudzpunktes izvēlni

Lai moduli pārvietotu, izmantojot daudzpunktes izvēlni, veiciet šādas darbības.

1. Atlasiet moduli vai nu struktūrskatā, vai kanvās.
1. Atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam vai nu struktūras rūtī, vai atlasītā moduļa rīkjoslā kanvās.
1. Ja moduli var pārvietot uz augšu vai uz leju konteinerā vai slotā, būs redzamas opcijas **Pārvietot uz augšu** vai **Pārvietot uz leju**. Atlasiet vēlamo pārvietošanas opciju, lai pārvietotu moduli uz augšu vai uz leju attiecībā pret pārējiem moduļiem.

## <a name="configure-modules"></a>Moduļu konfigurēšana

Šīs procedūras apraksta, kā konfigurēt un satura un konteinera moduļus.

### <a name="configure-a-content-module"></a>Satura moduļa konfigurēšana

Lai konfigurētu satura moduli lapā, rīkojieties, kā norādīts tālāk.

1. Struktūras rūtī pa kreisi izvērsiet koku un atlasiet jebkuru satura moduļa tipu (piemēram, **Satura bloks**). Alternatīvi jūs varat atlasīt moduli galvenajās kanvās.
1. Moduļa rekvizītu rūtī, kas atrodas labajā pusē, ievadiet rekvizītus visām vēlamajām moduļa vadīklām.
1. Komandjoslā atlasiet **Saglabāt**. Tas arī atsvaidzinās priekšskatījuma pamatni.

### <a name="edit-module-text-properties"></a>Rediģēt moduļa teksta rekvizītus

Moduļa teksta rekvizīti, kas nav tikai lasāmi, var tikt rediģēti tieši kanvās.

Lai rediģētu moduļa teksta rekvizītus, rīkojieties šādi.

1. Atlasiet kanvu teksta vadīklu, pēc tam novietojiet kursoru vietā, kur vēlaties rediģēt tekstu.
1. Ievadiet satura tekstu.
1. Atlasiet jebkur ārpus teksta satura, lai turpinātu cita satura rediģēšanu.

### <a name="inline-image-selection"></a>Iekļautā attēla atlase

Moduļa attēli, kas nav tikai lasāmi, var tikt mainīti tieši no kanvām.

Lai izvēlētos jaunu attēlu satura modulim, rīkojieties, kā norādīts tālāk.

1. Kanvās veiciet dubultklikšķi uz attēla. Tiks izsaukts multivides uztvērēja logs.
1. Meklējiet un atlasiet jaunu attēlu, kuru vēlaties izmantot, un pēc tam atlasiet **Labi**. Jaunais attēls tagad tiek atveidots kanvā.

### <a name="configure-a-container-module"></a>Konteinera moduļa konfigurēšana

Lai konfigurētu konteinera moduli lapā, rīkojieties, kā norādīts tālāk.

1. Lapā atlasiet konteinera moduli (piemēram, karuselis vai plūstošā konteinera modulis).
1. Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.
1. Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus vai nu konteinera nosaukumam, vai kādam no tajā esošo slotu nosaukumiem, un pēc tam atlasiet **Pievienot moduli**. Pēc tam pievienojiet pakārtotos moduļus atlasītajam konteineram. Papildinformāciju skatiet iepriekšējā [šī raksta](#add-a-module) sadaļā Darbs ar moduļiem.
1. Ja vairāki pakārtotie moduļi eksistē kā pamata konteinerā esoši līdzīgie moduļi, varat mainīt to parādīšanas secību pamata konteinerā. Atlasiet moduļa daudzpunktes pogu un pēc tam izmantojiet pogas ar augšup un lejup vērstām bultiņām.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar veidnēm](work-with-templates.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Konteinera moduļa pievienošana lapā](add-container-module.md)

[Darbs ar publicēšanas grupām](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
