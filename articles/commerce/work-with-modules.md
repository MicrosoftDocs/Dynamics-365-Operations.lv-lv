---
title: Darbs ar moduļiem
description: Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914798"
---
# <a name="work-with-modules"></a>Darbs ar moduļiem

Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Pārskats

Moduļi ir loģiski veidošanas bloki, kas veido lapas struktūru, un tiem ir dažādi mērķi un tvērumi. Daži moduļi ir augsta līmeņa konteineri, un to vienīgais mērķis ir aizturēt un organizēt citus moduļus (pakārtotos moduļus). Citiem moduļiem, piemēram, vienkāršam attēla novietojuma modulim, ir ļoti specifisks mērķis. Citi moduļi, piemēram, karuseļa modulis, atrodas kaut kur starp šīm divām kategorijām.

Pēc noklusējuma jūsu Dynamics 365 Commerce vietnē ir ietverta sākuma komplekta moduļa bibliotēka, kas ļauj jums sasniegt pamata e-komercijas scenārijus. Jums ir jābūt iespējai izveidot vispārīgu e-komercijas vietni, vienkārši izmantojot šos moduļus. Tomēr, iespējams, vēlēsities arī pielāgot šos moduļus vai izveidot jaunus, pielāgotus moduļus specifiskām vajadzībām. Ja vēlaties izveidot pielāgotus moduļus, ir pieejams moduļa dizaina programmatūras izstrādes komplekts (SDK), lai palīdzētu jums izveidot pielāgotu moduļu bibliotēku.

## <a name="container-modules-and-slots"></a>Konteineru moduļi un sloti

Kā jau minēts iepriekš, daži moduļi ir paredzēti pakārtotu moduļu aizturēšanai. Šie moduļi ir pazīstami kā *konteineri*, un tie atļauj ligzdotu moduļu hierarhijas. Konteineru moduļi ietver *slotus*. Sloti tiek izmantoti, lai apstrādātu konteinerā esošo pakārtoto moduļu izkārtojumu un nolūku. Piemērs ir pamata lapas konteinera modulis (augšējā līmeņa modulis jebkurai lapai), kas nosaka vairākus nozīmīgus slotus.

- Galvenes slots
- Pamatteksta slots
- Kājenes slots

Moduļa izstrādātājs definē šos slotus un nosaka, kurus un cik daudz pakārtotos moduļus var ievietot tieši tajā. Piemēram, galvenes slots var atbalstīt tikai vienu **Virsraksta moduļa** veidu, turpretī pamatteksta slots var atbalstīt neierobežotu moduļu skaitu jebkuram veidam (izņemot citas lapas konteinera moduļus).

Autorēšanas rīkos lapas autoriem nav jāzina iepriekš, kuri moduļi var un kuri nevar tikti ievietoti katrā slotā. Kad lapu autori atlasa slotu un pēc tam mēģina atlasīt moduli, lai to pievienotu, viņi redz filtrētu moduļu veidu skatu, kas tiek atbalstīts šim slotam.

## <a name="content-modules"></a>Satura moduļi

Satura moduļos ir ietverti satura un multivides elementi, piemēram, teksts (piemēram, virsraksti, rindkopas un saites) vai līdzekļu atsauces (piemēram, attēli, video un PDF faili). Tipisku satura moduļu tipu piemēri ir **Centrālais** ,**Līdzekļa** un **Reklāmkarogs**. Šo trīs tipu moduļos var būt teksts vai multivide, un tiem nav nepieciešami pakārtotie moduļi, lai radītu kaut ko redzamu lapā.

Lielākā daļa parasto, ikdienas lapu un satura autorēšanas aktivitāšu ietver satura moduļus, galvenokārt tāpēc, ka šie moduļi definē faktisko saturu, kas tiek atveidots to pamata konteinera moduļos. Ir pieejami daudzi satura moduļi, un šie moduļi parasti ir pēdējie, ko pievienosiet ligzdoto moduļu lapas hierarhijai.

Tālāk esošajā attēlā ir parādīts, kā moduļi tiek ligzdoti pamata konteineru moduļa slotos.

![Ligzdošanas moduļi](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moduļu pievienošana vai noņemšana

Šīs procedūras apraksta, kā pievienot un noņemt moduļus.

### <a name="add-a-module"></a>Moduļa pievienošana

Lai lapas slotam vai konteineram pievienotu moduli, veiciet tālāk minētās darbības.

1. Kreisajā struktūras rūtī atlasiet konteineru vai slotu, kuram var pievienot pakārtoto moduli.

    > [!NOTE]
    > Moduļa veidotājs nosaka moduļu tipu sarakstu, ko var pievienot konkrētam moduļa slotam. Veidnes autori tad var precizēt atļautās moduļa opcijas, lai palīdzētu nodrošināt saskanīgu meklēšanas programmas optimizāciju (SEO) un autorēšanas efektivitāti visām lapu lapām, kas izveidotas no noteiktas veidnes.

1. Atlasiet daudzpunktes pogu (**...**) modulim un pēc tam atlasiet **Pievienot moduli**. Tiek parādīts dialoglodziņš **Pievienot moduli**. Šis dialoglodziņš tiek automātiski filtrēts, lai tiktu rādīti tikai moduļi, kas tiek atbalstīti atlasītajā konteinerā vai slotā. Moduļu sarakstu nosaka lapas veidne vai konteinera moduļa definīcija.

    > [!NOTE]
    > Ja konteiners vai slots neatbalsta jaunus pakārtotos moduļus, opcija **Pievienot moduli** nav pieejama.

1. Dialoglodziņā meklējiet un atlasiet moduli, ko pievienot lapai.

    > [!TIP]
    > **Funkcija** un **Centrālais** ir labi moduļu veidi iesācējiem.

1. Atlasiet **Labi**, lai atlasīto moduli pievienotu atlasītajam konteineram vai slotam jūsu lapā.

### <a name="remove-a-module"></a>Moduļa noņemšana

Lai no lapas slota vai konteinera noņemtu moduli, veiciet tālāk minētās darbības.

1. Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus moduļa nosaukumam, lai noņemtu, un pēc tam atlasiet pogu Miskaste.
1. Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt moduli, atlasiet **Labi**.

## <a name="configure-modules"></a>Moduļu konfigurēšana

Šīs procedūras apraksta, kā konfigurēt un satura un konteinera moduļus.

### <a name="configure-a-content-module"></a>Satura moduļa konfigurēšana

Lai konfigurētu satura moduli lapā, rīkojieties, kā norādīts tālāk.

1. Struktūras rūtī pa kreisi atlasiet satura moduļa tipu (piemēram, **Līdzekļa**, **Centrālais** vai **Reklāmkarogs**).
1. Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.
1. Ja rekvizītu rūtij ir sadaļa **Datu konfigurācija**, atlasiet to, lai to izvērstu. Citādi pārejiet uz 5. darbību.
1. Ja tur ir poga **Pievienot datu avotu**, atlasiet to un pēc tam atlasiet pievienojamos satura vienumus.
1. Ievadiet iestatījumus visām nepieciešamajām vai vēlamajām moduļa vadīklām.
1. Atlasiet **Saglabāt**.

### <a name="configure-a-container-module"></a>Konteinera moduļa konfigurēšana

Lai konfigurētu konteinera moduli lapā, rīkojieties, kā norādīts tālāk.

1. Lapā atlasiet konteinera moduli (piemēram, karuselis vai plūstošā konteinera modulis).
1. Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.
1. Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus vai nu konteinera nosaukumam, vai kādam no tajā esošo slotu nosaukumiem, un pēc tam atlasiet **Pievienot moduli**. Pēc tam pievienojiet pakārtotos moduļus atlasītajam konteineram. Plašāku informāciju skatiet procedūru [Moduļa pievienošana](#add-a-module) iepriekš šajā tēmā.
1. Ja vairāki pakārtotie moduļi eksistē kā pamata konteinerā esoši brāļi, varat mainīt to parādīšanas secību pamata konteinerā. Atlasiet moduļa daudzpunktes pogu un pēc tam izmantojiet pogas ar augšup un lejup vērstām bultiņām.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar veidnēm](work-with-templates.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Konteinera moduļa pievienošana lapā](add-container-module.md)

[Satura izvietojuma moduļu pievienošana lapā](add-content-placement-modules.md)

[Darbs ar publicēšanas grupām](publish-groups.md)

