---
title: Pamatlīdzekļu transakciju grāmatošana grāmatošanas līmeņos
description: Šajā rakstā ir sniegts pārskats par pamatlīdzekļu transakciju grāmatošanas līmeņa funkcionalitāti.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493676"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Pamatlīdzekļu transakciju grāmatošana grāmatošanas līmeņos

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par pamatlīdzekļu transakciju grāmatošanas līmeņa funkcionalitāti.

Pamatlīdzeklis bieži tiek nolietots dažādos veidos dažādiem nolūkiem. Nolietojums nodokļu nolūkiem tiek aprēķināts, izmantojot pašreizējos nodokļu nosacījumus, lai sasniegtu visaugstāko iespējamo nolietojumu pirms nodokļiem, bet nolietojums pārskata nolūkos tiek aprēķināts atbilstīgi uzskaites noteikumiem un standartiem. Dažādi nolietojuma veidi tiek aprēķināti un ierakstīti atsevišķi grāmatošanas līmeņos.

Katra pamatlīdzeklim piesaistītā grāmata ir iestatīta noteiktam grāmatošanas līmenim, kuram ir vispārējā nolietojuma mērķis. Ir desmit grāmatošanas līmeņi: Pašreizējais, Operācijas, Nodokļi un septiņi līmeņi, kuru tips ir Pielāgots. Jūs varat arī atslēgt grāmatas grāmatošanu virsgrāmatā, iestatot laukam Grāmatot virsgrāmatā opciju Nē. Pēc tam laukam Grāmatošanas līmenis tiek automātiski iestatīta opcija Nav. Parasti grāmatas, kas netiek grāmatotas Virsgrāmatā, tiek izmantotas nodokļu pārskatu veidošanai. Šī pieeja sniedz papildu pielāgojamības iespējas pamatlīdzekļu grāmatas vēsturisko transakciju dzēšanai, jo tās nav iekļautas Virsgrāmatā.

Pamatlīdzekļu žurnāli tiek definēti, izmantojot lapu Žurnālu nosaukumi sadaļā Virsgrāmata > Žurnāla iestatījumi > Žurnālu nosaukumi. Katrs žurnāls, kur varat grāmatot nolietojumu, tiek definēts pēc žurnāla nosaukuma tikai vienā grāmatošanas līmenī. Grāmatošanas līmeni žurnālā nevar mainīt. Šis ierobežojums palīdz nodrošināt, ka katra grāmatošanas līmeņa darbības atrodas atsevišķi. Katram grāmatošanas līmenim jāizveido vismaz viens žurnāla nosaukums. Ja izmantojat grāmatas, kas netiek grāmatotas Virsgrāmatā, ir jāizveido arī žurnāls, kura grāmatošanas līmenim ir iestatīta opcija Nav.

Varat norādīt virsgrāmatas kontus pamatlīdzekļu darbībām lapā Pamatlīdzekļu grāmatošanas metodes. Katrai grāmatošanas metodei jāatlasa atbilstīgs darbības tips un grāmata un pēc tam jāpiešķir virsgrāmatas konti. Iestatiet grāmatošanas metodes ierakstu katrai grāmatai, kas tiek grāmatota virsgrāmatā.

Pamatlīdzekli var ievadīt dokumentos, kuri atbalsta tikai **pašreizējo** grāmatošanas līmeni, piemēram, **Pirkšanas pasūtījums**, **Gaidošs kreditora rēķins**, **Pārdošanas pasūtījums** vai **Brīva teksta rēķins**. Atlasot pamatlīdzekļa ID jebkurā no šiem dokumentiem, līdzekļu grāmata tiek filtrēta grāmatā ar **pašreizējo** grāmatošanas līmeni un tiek aizpildīta automātiski grāmatošanas laikā, kad sistēma pārbauda, vai pamatlīdzekļu grāmatošanas līmenis ir **Pašreizējais**. Ja šo pārbaudi nevarēs pabeigt, grāmatošanas process tiks apturēts. 

> [!NOTE] 
> Izmantojot atvasinātās grāmatas, varat vienlaikus grāmatot transakcijas dažādos grāmatošanas līmeņos. Primārās grāmatas darbības tiek izveidotas žurnālā vai avota dokumentā, kura grāmatošanas līmenis atbilst grāmatas grāmatošanas līmenim. Grāmatošanas laikā atvasinātās grāmatas darbības tiks grāmatotas atbilstīgajos grāmatošanas līmeņos. 


Papildinformāciju skatiet [Atvasinātās grāmatas](derived-books.md) un [Grāmatošana, izmantojot atvasinātās grāmatas](post-derived-value-models.md).



