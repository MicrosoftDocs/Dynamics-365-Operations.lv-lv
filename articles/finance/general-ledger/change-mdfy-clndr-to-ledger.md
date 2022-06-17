---
title: Virsgrāmatas kalendāra maiņa vai atkārtota piešķiršana
description: Šajā rakstā skaidrots, kā mainīt virsgrāmatai pašreiz piešķirto kalendāru un kā virsgrāmatai piešķirt jaunu kalendāru.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 751954e0dc5f682b99ab7fe349cd505dc9da7858
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848611"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Virsgrāmatas kalendāra maiņa vai atkārtota piešķiršana

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā mainīt virsgrāmatai pašreiz piešķirto kalendāru un kā virsgrāmatai piešķirt jaunu kalendāru.

## <a name="issue"></a>Problēma

Dažkārt uzņēmumiem ir jāmaina esošais kalendārs, kas ir piešķirts virsgrāmatai, vai jāpiešķir jauns kalendārs.

## <a name="resolution"></a>Novēršana

Pastāv divi virsgrāmatas kalendāra maiņas vai atkārtotas piešķiršanas scenāriji. Pirmais scenārijs ir saistīts ar esoša kalendāra, kas jau ir piešķirts virsgrāmatai, maiņu. Otrais scenārijs ietver jauna kalendāra izveidi un tā piešķiršanu virsgrāmatai. Abas izmaiņas var veikt jebkurā laikā, pat pēc transakciju iegrāmatošanas virsgrāmatā.

### <a name="change-an-existing-fiscal-calendar"></a>Esoša finanšu kalendāra maiņa

Lai mainītu esošu kalendāru, kas ir piešķirts jūsu virsgrāmatai, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata** un atlasiet finanšu kalendāra saiti, lai atvērtu lapu **Virsgrāmatas kalendāri**.

Pastāv ierobežojumi izmaiņām, kuras var veikt kalendārā. Piemēram, varat mainīt gada *periodu* sākuma un beigu datumus, bet kalendārā nevar mainīt *gada* sākuma un beigu datumus.

Lai mainītu periodus gadā, atlasiet atbilstošo kalendāru un gadu. Vispirms izmantojiet pogu **Dzēst periodu**, lai dzēstu dažus vai visus esošos darba periodus. Varat dzēst visus darbības periodus, izņemot pirmo. Pēc tam izmantojiet pogu **Sadalīt periodu**, lai atlikušo periodu vai periodus sadalītu jaunos periodos, ievadot nākamā perioda atbilstošo sākuma datumu.

Pēc periodu maiņas kalendārā katrai juridiskajai personai (uzņēmumam), kam kalendārs ir piešķirts, jāpalaiž process **Pārrēķināt virsgrāmatas periodus**. Lai gan nav brīdinājuma ziņojuma, kas atgādinātu par nepieciešamību pabeigt šo darbību, pārrēķina procesā ir nepieciešams atjaunināt periodu, kas ir piešķirts katrai virsgrāmatā iegrāmatotajai transakcijai. Lai izpildītu pārrēķināšanas procesu, katra uzņēmuma lapā **Virsgrāmatas iestatīšana** atlasiet **Pārrēķināt virsgrāmatas periodus**.

Ja pārrēķina process netiks izpildīts, transakciju bilances apgrozījuma bilancē vai finanšu pārskatos var būt nepareizi iekļautas periodos. Šādā gadījumā bilances var labot jebkurā laikā, palaižot pārrēķināšanas procesu.

### <a name="assign-a-new-fiscal-calendar"></a>Jauna finanšu kalendāra piešķiršana

Lai piešķirtu jaunu finanšu kalendāru, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata** un atlasiet **Rediģēt**, lai lapa **Virsgrāmata** pārietu rediģēšanas režīmā. Pēc tam laukā **Finanšu kalendārs** atlasiet jaunu finanšu kalendāru.

Pēc virsgrāmatas finanšu kalendāra maiņas ir jāizpilda darbība **Pārrēķināt virsgrāmatas periodus**. Kad piešķirat virsgrāmatai jaunu finanšu kalendāru, ziņojums atgādina par nepieciešamību pabeigt šo darbību. Kaut arī ziņojums šķietami norāda, ka pārrēķina process ir neobligāts, tā nav taisnība. Jāatjaunina periods, kas piešķirts katrai virsgrāmatā iegrāmatotai transakcijai. Lai izpildītu pārrēķināšanas procesu, lapā **Virsgrāmatas iestatīšana** atlasiet **Pārrēķināt virsgrāmatas periodus**.

Ja pārrēķina process netiks izpildīts, transakciju bilances apgrozījuma bilancē vai finanšu pārskatos var būt nepareizi iekļautas periodos. Šādā gadījumā bilances var labot jebkurā laikā, palaižot pārrēķināšanas procesu.
