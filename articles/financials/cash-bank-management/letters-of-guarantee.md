---
title: "Garantijas vēstules"
description: "Šajā rakstā ir sniegta informācija par garantijas vēstulēm. Garantijas vēstulē banka piekrīt personai maksāt noteiktu naudas summu, ja kāds no bankas klientiem nepilda maksājumu vai saistības attiecībā pret šo personu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c3d61bbfdd6a304a7bd2edd81e51e556a4955dce
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="letters-of-guarantee"></a>Garantijas vēstules

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par garantijas vēstulēm. Garantijas vēstulē banka piekrīt personai maksāt noteiktu naudas summu, ja kāds no bankas klientiem nepilda maksājumu vai saistības attiecībā pret šo personu. 

Garantijas vēstule ir bankas (garantētājs) apņemšanās samaksāt noteiktu naudas summu kādai personai (saņēmējs), ja bankas klients (maksātājs) veic maksājumu vai izpilda pienākumu attiecībā uz saņēmēju. Garantijas vēstules nav nododamas. Tās attiecas tikai uz saņēmēju, kurš ir nosaukts līgumā. Maksātājs var pieprasīt palielināt vai samazināt garantijas vēstules summu saskaņā ar līguma nosacījumiem. 

Lai likvidētu garantijas vēstuli, saņēmējam jāiesniedz sākotnējā garantijas vēstule un jāinformē banka par maksātāja saistību nepildīšanu pirms termiņa beigu datuma. Pēc tam banka saņēmēja kontā iemaksā summu saskaņā ar garantijas vēstules nosacījumiem. Banka rezervē procentus no maksājamas summas kā peļņu. Procentu apmērs tiek norunāts un norādīts līguma nosacījumos. 

Varat izveidot kodu, lai izsekotu garantijas vēstules mērķi. Varat arī norādīt iemeslus, kas var būt saistīti ar garantijas vēstuli, ja vēstule tiek atcelta. Mērķu kodus un bankas iemeslus var skatīt lapā **Maksājuma mērķu kodi** un **Bankas iemesli**. 

Var izmantot lapu **Garantijas vēstule**, lai veiktu šos uzdevumus:

-   izveidot pareizus virsgrāmatas ierakstus un veiktu korekcijas manuālai ievadei;
-   reģistrēt visas skaidras un bezskaidras naudas transakcijas un izsekot garantijas vēstuļu bilances;
-   reģistrēt un izsekot statusu un garantijas vēstuļu derīguma termiņu;
-   ģenerēt atskaiti, kurā norādītas bankas, kas ir garantijas vēstuļu turētājas.

Tālāk tabulā ir aprakstītas darbības, ko var veikt garantijas vēstulei.

| Darbība              | Mērķis                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Iesniegt bankā      | Iesniegt bankai garantijas vēstules izsniegšanas pieprasījumu.                                                                       |
| Saņemt no bankas   | Kad banka piekrīt izpildīt pieprasījumu, paņemt garantijas vēstuli no bankas.                            |
| Nodot saņēmējam | Kad saņemat no bankas garantijas vēstuli, nodot garantijas vēstuli saņēmējam.              |
| Palielināt vērtību      | Ja saņēmējs un maksātājs tam piekrīt, palielināt monetāro vērtību.                                                  |
| Samazināt vērtību      | Ja saņēmējs un maksātājs tam piekrīt, samazināt monetāro vērtību.                                                  |
| Paplašināt              | Kad garantijas vēstuli nododat saņēmējam, pagarināt derīguma termiņu, ja tas ir nepieciešams. |
| Atcelt              | Ja garantijas vēstules mērķis vairs nav spēkā, varat izbeigt līgumu.                  |
| Likvidēt           | Kad saņēmējs nodod garantijas vēstuli bankai, garantijas vēstulē norādītā naudas summa tiek izmaksāta.                      |


Lai iegūtu papildu informāciju, skatiet šādas tēmas:

[Garantijas vēstules darījums](tasks/letter-guarantee-transaction.md)

[Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili](tasks/set-up-bank-facilities-posting-profiles.md)



