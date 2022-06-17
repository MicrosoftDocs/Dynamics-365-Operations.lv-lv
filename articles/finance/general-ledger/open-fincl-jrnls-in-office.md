---
title: Finanšu žurnālu veidņu atvēršana sistēmā Office
description: Šajā rakstā aprakstītas problēmas, kas var rasties, veidojot pielāgotus finanšu žurnālus, izmantojot Microsoft Excel veidni.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896352"
---
# <a name="open-financial-journal-templates-in-office"></a>Finanšu žurnālu veidņu atvēršana sistēmā Office

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstītas problēmas, kas var rasties, veidojot pielāgotus finanšu žurnālus, izmantojot Microsoft Excel veidni.

## <a name="symptom"></a>Simptoms

Jūs izveidojāt pielāgotu Excel veidni finanšu žurnāliem, bet tā neparādās izvēlnē **Atvērt rindas programmā Excel**. Vai arī tā parādās izvēlnē, tiek atvērta cita veidne, bet, kad to atlasāt.

## <a name="resolution"></a>Novēršana

Noklusējuma funkcionalitāte Atvērt programmā Excel izmanto pašreizējās lapas saknes datu avotu (tabulu), lai noteiktu, kuras Office veidnes vai datu elementi tiek parādīti kā opcijas izvēlnē **Atvērt programmā Excel**. Šī darbība nav ideāla pieredze finanšu žurnāliem, jo finanšu žurnāli izmanto tās pašas tabulas (LedgerJournalTable un LedgerJournalTrans) kā daudzu citu žurnālu tipu saknes datu avotu.

Finanšu žurnāliem funkcionalitāte Atvērt rindas programmā Excel ir paredzēta, lai parādītu veidnes, kas ir paredzētas žurnālam, kurā pašlaik strādājat, piemēram, virsgrāmatas žurnāla vai maksājumu žurnāla kontekstā. Piemēram, veidne, ko ir paredzēts izmantot ar kreditoru maksājumu žurnālu, tiks izveidota, lai ieviestu jūsu primāro kontu kā kreditoru kontu.

Ja vēlaties paaugstināt veidni tā, lai tā būtu pieejama izvēlnēs **Atvērt rindas programmā Excel** un **Atvērt programmā Excel** vienkārša izstrādātāja pieredze ir ieviest **LedgerIJournalExcelTemplate** interfeisu un paplašināt **DocuTemplateRegistrationBase** klasi. Daudzi šīs pieejas piemēri ir ieviesti sistēmā. Viens piemērs, ko var izmantot atsaucei, ir Virsgrāmatas Žurnālam (vai ikdienas žurnālam) izveidotais **LedgerDailyJournalExcelTemplate** interfeiss.

Kad veidnei ir ieviests **LedgerIJournalExcelTemplate** interfeiss, izvēlnē **Atvērt rindas programmā Excel** veidnes tiks filtrētas pēc jūsu žurnāla tipa, kā arī tiks rādītas tikai šim žurnālam pieejamās veidnes. Interfeiss nodrošina arī validācijas metodi, kas nodrošina, ka veidni nevar atvērt žurnālam, ja tā neatbilst konta tipa prasībām. Piemēram, varat norādīt, ka konta tipam jābūt **Kreditors** vai **Virsgrāmata**.

Lai iegūtu papildinformāciju par šo funkcionalitāti, skatiet rakstu [Veidņu pievienošana izvēlnei Atvērt rindas programmā Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
