---
title: Funkcionālo novietojumu veidi
description: Šajā tēmā aprakstīts, kā izveidot funkcionālo novietojumu veidus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 708c27dbf568ca8bea6ec0b775afac9b80759581
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837733"
---
# <a name="functional-location-types"></a>Funkcionālo novietojumu veidi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā aprakstīts, kā izveidot funkcionālo novietojumu veidus Līdzekļu pārvaldībā. Funkcionālo novietojumu veidus izmanto, lai pārvaldītu prasības funkcionālajiem novietojumiem, tostarp to, kā līdzekļi tiek uzstādīti funkcionālajā novietojumā. Var iestatīt līdzekļu veidus, uzturēšanas plānus, funkcionālā novietojuma atribūtus un līdzekļu atribūtu prasības, kas jāizmanto funkcionālā novietojumā, kurš izmanto konkrētu funkcionālā novietojuma veidu. Veidojot funkcionālo novietojumu, funkcionālā novietojuma veids ir obligāts.

>[!NOTE] 
>Lai strādātu ar funkcionālajiem novietojumiem, ir jāizveido noklusējuma funkcionālais novietojums, kas tiks izmantots tikai jaunu līdzekļu izveides nolūkā. Šim noklusējuma funkcionālajam novietojumam ieteicams izveidot noklusējuma funkcionālā novietojuma veidu, kas ir patiešām vienkāršs un ļauj uzstādīt vairākus līdzekļus noklusējuma funkcionālajā novietojumā. Papildinformāciju par funkcionālo novietojumu iestatīšanu skatiet [Izveidot funkcionālos novietojumus](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Noklusējuma funkcionālā novietojuma veida izveide

Šajā procedūrā ir parādīts, kā izveidot noklusējuma funkcionālā novietojuma veidu, kas jāizmanto noklusējuma funkcionālajam novietojumam.

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Funkcionālie novietojumi** > **Funkcionālo novietojumu veidi**.
2. Atlasiet **Jauns**, lai izveidotu funkcionālā novietojuma veidu.
3. Ievietojiet funkcionālā novietojuma veida ID laukā **Funkcionālā novietojuma veids**, piemēram, "Noklusējums", un nosaukumu laukā **Nosaukums**.
4. Atlasiet dzīves cikla modeli laukā **Funkcionālā novietojuma dzīves cikla modelis**.
5. Atlasiet "Jā" uz pārslēgšanas pogas **Vairāki līdzekļi**, lai atļautu uzstādīt vairākus līdzekļus funkcionālajā novietojumā (noklusējuma funkcionālais novietojums), izmantojot šo veidu.

Tagad ir izveidots noklusējuma funkcionālā novietojuma veids, kas jāizmanto tikai noklusējuma funkcionālajā novietojumā. Jūs nedrīkstat pievienot papildu prasības vai ierobežojumus šim noklusējuma funkcionālā novietojuma veidam.


## <a name="create-functional-location-types"></a>Funkcionālo novietojumu veidu izveide

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Funkcionālie novietojumi** > **Funkcionālo novietojumu veidi**.
2. Atlasiet **Jauns**, lai izveidotu funkcionālā novietojuma veidu.
3. Ievietojiet funkcionālā novietojuma veida ID laukā **Funkcionālā novietojuma veids**, piemēram, "Noklusējums", un nosaukumu laukā **Nosaukums**.
4. Atlasiet dzīves cikla modeli laukā **Funkcionālā novietojuma dzīves cikla modelis**. Plašāku informāciju par funkcionālā novietojuma dzīves cikla stāvokļiem un dzīves cikla modeļiem skatiet sadaļā [Funkcionālo novietojumu dzīves cikla stāvokļi](../setup-for-functional-locations/functional-location-stages.md).
5. Atlasiet "Jā" uz pārslēgšanas pogas **Vairāki līdzekļi**, ja vajadzētu būt iespējamam uzstādīt vairākus līdzekļus funkcionālajā novietojumā, izmantojot šo funkcionālā novietojuma veidu. Ja atlasīsit "Nē", varat instalēt tikai *vienu* līdzekli funkcionālajā novietojumā, izmantojot šo funkcionālā novietojuma veidu.
6. Atlasiet "Jā" uz pārslēgšanas pogas **Atjaunināt līdzekļa dimensij**, ja vēlaties, lai līdzekļi, kas uzstādīti šī veida funkcionālajā novietojumā, automātiski izmantotu ar funkcionālo novietojumu saistītās finanšu dimensijas. Tas nozīmē, ka, ja maināt finanšu dimensijas veidlapā [Izveidot funkcionālo novietojumu](../functional-locations/create-functional-locations.md) un funkcionālais novietojums izmanto funkcionālā novietojuma veidu ar šo pārslēgšanas pogu iestatītu uz "Jā", finanšu dimensijas tiek automātiski atjauninātas visiem līdzekļiem, kas uzstādīti šajā funkcionālajā novietojumā.
7. Lauks **Līdzekļa veids** tiek izmantots, ja vēlaties automātiski izveidot *vienu* līdzekli funkcionālajam novietojumam ar tādu pašu ID un nosaukumu kā funkcionālajam novietojumam, kuru veidojat. Piemēram, tas var būt būtiski, ja veidojat statisku funkcionālo novietojumu, piemēram, ēku vai konveijeru. Šādā gadījumā atlasiet līdzekļa veidu, kuru vēlaties izmantot automātiski izveidotam līdzeklim. Atcerieties, ka gadījumā, ja veicat atlasi šajā laukā, pārslēgšanas pogai **Vairāki līdzekļi** jābūt iestatītai uz "Nē".
8. Kopsavilkuma cilnē **Līdzekļu veidi** atlasiet līdzekļu veidus, kas ir saistīti ar funkcionālā novietojuma veidu. Atlasiet **Pievienot rindu** un atlasiet līdzekļu veidus. Ja šeit pievienojat līdzekļu veidus, funkcionālā novietojumā var uzstādīt tikai tos līdzekļus, kas izmanto šo funkcionālā novietojuma veidu. Ja kopsavilkuma cilnē **Līdzekļu veidi** nav atlasīts neviens līdzekļu veids, var uzstādīt visus līdzekļu veidus.
9. Kopsavilkuma cilnē **Uzturēšanas plāni** atlasiet uzturēšanas plānus, kas automātiski jāiestata jaunos funkcionālos novietojumos, izmantojot šo funkcionālā novietojuma veidu. Atlasiet **Pievienot rindu** un atlasiet uzturēšanas plānus. Ja šeit pievienojat uzturēšanas plānus, funkcionālajā novietojumā var izmantot tikai šos plānus, izmantojot šo funkcionālā novietojuma veidu.
10. Kopsavilkuma cilnē **Līdzekļa atribūtu prasības** iestatiet līdzekļa atribūtus, kas automātiski jāiestata jaunos funkcionālos novietojumos, izmantojot šo funkcionālā novietojuma veidu. Atlasiet **Pievienot rindu** un atlasiet atribūtu. Šīs atribūtu prasības darbojas kā vadlīnijas. Tās nav validētas attiecībā uz līdzeklim iestatītiem atribūtiem (**Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi** > atlasiet līdzekli saraksta lapā > cilne **Vispārīgi** > poga **Atribūti** ). Atribūtu prasības tiek parādītas, instalējot līdzekļus funkcionālajos novietojumos.
11. Kopsavilkuma cilnē **Atļautie veidi** atlasiet funkcionālo novietojumu veidus, kuriem jābūt derīgiem pakārtotiem funkcionālā novietojuma veidiem, kas saistīti ar vecākelementa funkcionālā novietojuma veidu, kurš izmanto atlasīto funkcionālā novietojuma veidu.
12. Kopsavilkuma cilnē **Atribūti** atlasiet funkcionālā novietojuma atribūtus, kas automātiski jāiestata jaunos funkcionālos novietojumos, izmantojot šo funkcionālā novietojuma veidu. Atlasiet **Pievienot rindu** un atlasiet atribūtu.


>[!NOTE] 
>Kopsavilkuma cilnē **Vispārīgi** varat iegūt pārskatu par līdzekļu veidu skaitu, uzturēšanas plāniem, līdzekļu atribūtu prasībām, atļautajiem veidiem, atribūtiem un funkcionālajiem novietojumiem, kas iestatītas funkcionālā novietojuma veidā. Laukā **Funkcionālie novietojumi** ir norādīts to funkcionālo novietojumu skaits, kuri izmanto funkcionālā novietojuma veidu. Varat izmantot pogu **Kopēt**, lai kopētu iestatījumus no funkcionālā novietojuma veida uz atlasīto funkcionālā novietojuma veidu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]