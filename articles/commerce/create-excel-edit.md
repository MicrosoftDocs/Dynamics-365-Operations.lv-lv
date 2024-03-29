---
title: Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus
description: Šajā rakstā ir aprakstīts, kā izveidot Excel darbgrāmatu, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: 93e0053c38c9595cab59947e4b65b0b4aa966380
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270214"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot Excel darbgrāmatu, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.

## <a name="overview"></a>Pārskats

Ir pieejama iepriekš definēta Excel veidne, kurai klienti var piekļūt no dažādām sistēmas daļām un kuru var izmantot, lai rediģētu un auditētu mazumtirdzniecības darījumus. Tomēr klienti šim nolūkam var arī izveidot pielāgotu Excel darbgrāmatu.

## <a name="create-and-configure-an-excel-workbook"></a>Excel darbgrāmatas izveide un konfigurēšana

Lai izveidotu un konfigurētu Excel darbgrāmatu un varētu rediģēt mazumtirdzniecības darījumus, veiciet tālāk norādītās darbības.

1. Atveriet programmu Excel un izveidojiet tukšu darbgrāmatu.
1. Cilnē **Ievietot** atlasiet **Manas pievienojumprogrammas**.
1. Labajā rūtī atlasiet saiti **Pievienot servera informāciju**.
1. Ievadiet servera vietrādi URL un pēc tam atlasiet **Labi**.
1. Ja saņemat kļūdas ziņojumu “Nav atrasta neviena sīkprogrammas reģistrācija”, veiciet tālāk norādītās darbības, lai atrisinātu problēmu.

    1. Programmā Commerce dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Office programmu parametri**.
    1. Kopsavilkuma cilnē **Programmas parametri** atlasiet **Inicializēt programmas parametrus**.
    1. Apstiprinājuma ziņojuma lodziņā atlasiet **Labi**.
    1. Kopsavilkuma cilnē **Reģistrētās sīkprogrammas** atlasiet **Inicializēt sīkprogrammu reģistrāciju**.
    1. Atkārtojiet trīs iepriekšējās darbības pēc nepieciešamības.

1. Atlasiet **Noformējums** un pēc tam atlasiet **Pievienot tabulu**.
1. Pamatojoties uz modificējamajiem datiem, atlasiet elementus, kas jāpievieno Excel darbgrāmatai rediģēšanai. Izmantojiet tālāk esošo tabulu kā atsauci.

    | Darījuma veids | Izmantojamie datu elementi |
    |------------------|----------------------|
    | Darījumi, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, tiešsaistes pasūtījumi, asinhroni debitoru pasūtījumi, asinhroni debitoru piedāvājumi | Darījums (auditējams), pārdošanas darījums (auditējams), maksājumu darījumi (auditējami), nodokļu darījumi (auditējami), atlaižu darījumi (auditējami), maksas darījumi (auditējami) |
    | Noguldījums bankā | Darījums (auditējams), norēķinu darījumi noguldījumiem bankā (auditējami) |
    | Noguldījums seifā | Darījums (auditējams), norēķinu darījumi noguldījumiem seifā (auditējami) |
    | Norēķinu uzskaite | Darījums (auditējams), norēķinu uzskaites darījumi (auditējami) |
    | Ienākumi, izdevumi | Darījums (auditējams), ienākumu/izdevumu darījumi (auditējami), maksājumu darījumi (auditējami) |
    | Sākuma summas norādīšana, norēķinu noņemšana, mainīgā ievade, izdodamā atlikuma norēķini, rēķinu apmaksa, debitora depozīts | Darījums (auditējams), maksājumu darījumi (auditējami) |

    > [!NOTE]
    > Ir svarīgi katrai Excel darbgrāmatai pievienot tikai vienu datu elementu. Turklāt visi lauki, kas atzīmēti ar atslēgas simbolu, ir jāpievieno atbilstošajai darbgrāmatai.

1. Pēc darbgrāmatas konfigurēšanas lietojiet pieprasītos filtrus. Noteikti izmantojiet tos pašus filtrus visām faila darblapām. Izvairieties no ļoti lielu datu apjomu ielādēšanas Excel failā. Pretējā gadījumā var tikt ietekmēta veiktspēja, un programmas Excel un jūsu sistēmas darbība var palēnināties. Kā faila filtrus iesakām vienmēr izmantot elementus “Uzņēmums” un “Pārskata numurs” vai “Darījuma numurs”.
1. Pēc filtru konfigurēšanas atlasiet **Atsvaidzināt**, lai ielādētu datus.
1. Rediģējiet vajadzīgos datus un pēc tam publicējiet tos. Ja poga **Publicēt** nav pieejama, iespējams, daži galvenie lauki netika pievienoti Excel darbgrāmatai.

## <a name="additional-resources"></a>Papildu resursi

[Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana](edit-cash-trans.md)

[Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana](edit-order-trans.md)

[Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana](edit-financial-dim.md)

[Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
