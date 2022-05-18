---
title: Nomas grāmatošanas tipi
description: Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6c06f68aebe7ed1ccc944793591202a9a221c42b
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720144"
---
# <a name="lease-posting-types"></a>Nomas grāmatošanas tipi

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.

## <a name="lease-asset"></a>Nomas līdzeklis

Šis konts ir saistīts ar lietošanas tiesību (right-of-use — ROU) līdzekli. Šis konts tiek debetēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem nomas uzskaites standartiem, uzskaites standartu kodifikācijas tēmu 842 (ASC 842) un starptautisko finanšu pārskatu standartu 16 (SFPS 16). Mainītai nomai šis konts var būt debetēts vai kreditēts atkarībā no tā, vai maiņa palielina vai samazina nomas saistības.

**Žurnāla ierakstu piemēri**: sākotnējā atzīšana<br>
**Debets**: nomas līdzeklis XXX<br>
**Kredīts**: nomas saistības XXX

## <a name="lease-liability"></a>Nomas saistības

Konts ir saistīts ar nomas saistībām, kas rodas, kad maksājumiem tiek piemērota atlaide saskaņā ar jaunajiem IFRS 16 un ASC 842 standartiem. Šis konts tiek kreditēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem standartiem. Tas tiek debetēts nomas maksājumiem un kreditēts procentu uzkrājumiem.

**Žurnāla ierakstu piemēri**: sākotnējā atzīšana<br>
**Debets**: nomas līdzeklis XXX<br>
**Kredīts**: nomas saistības XXX

**Žurnāla ierakstu piemērs**: procentu uzkrājumi<br>
**Debets**: procentu izdevumi XXX<br>
**Kredīts**: nomas saistības XXX

**Žurnāla ierakstu piemērs**: nomas maksājums<br>
**Debets**: nomas saistības XXX<br>
**Kredīts**: kreditora maksājums/nomas maksājums XXX

## <a name="short-term-lease-liability"></a>Īstermiņa nomas saistības

Konts ir saistīts ar īstermiņa nomas saistībām, kur tiek grāmatots īstermiņa nomas saistību pārklasificēšanas žurnāla ieraksts. Šis konts tiek kreditēts īstermiņa saistībām no amortizācijas grafika mēneša pēdējā dienā. Tomēr tā pati summa tiek debetēta nākamā mēneša pirmajā dienā.

**Žurnāla ierakstu piemērs**: īstermiņa nomas saistību pārklasificēšana<br>
**Debets**: nomas saistības XXX<br>
**Kredīts**: īstermiņa nomas saistības XXX<br>
**Debets**: īstermiņa nomas saistības XXX<br>
**Kredīts**: nomas saistības XXX

## <a name="depreciation-expense"></a>Nolietojuma izmaksas

Konts ir saistīts ar izdevumiem, kas ir saistīti ar LLT līdzekļa amortizāciju saskaņā ar IFRS 16, ASC 842 un finanšu nomu saskaņā ar SGS 17 un ASC 840. Šis konts tiek debetēts, ja LLT līdzeklis tiek nolietots katru mēnesi.

**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi<br>
**Debets**: nolietojuma izdevumi XXX<br>
**Kredīts**: uzkrātais nolietojums XXX

## <a name="gainloss-on-lease-modification"></a>Peļņa/zaudējumi no nomas modifikācijas

Konts ir saistīts ar jebkuriem guvumiem vai zaudējumiem, kas rodas no nomas modifikācijām. Nomas modifikācijas laikā var rasties guvums, ja modifikācija samazina nomas saistības par summu, kas pārsniedz LLT līdzekļa uzskaites vērtību.

Piemēram, nomai ir pašreizējās $ 150 000 nomas saistības uzskaites vērtība un $ 100 000 LLT aktīva uzskaites vērtība. Noma tiek modificēta, un šī modifikācija veido jaunu nākotnes minimālo nomas maksājumu (PVFMLP) $ 40 000 apmērā aktuālo vērtību. Tāpēc nomas saistības tiks debetētas ar $ 110 000 ($ 150 000 – $ 40 000). Tā kā LLT līdzeklis ir tikai $ 100 000, $ 110 000 samazinājums samazina pamatlīdzekli zemāk par 0 (nulli). Tāpēc uzskaites vadlīnijas nosaka, ka atlikums ir jārezervē peļņas kontā. Šādā gadījumā galīgais žurnāla ieraksts būs debets nomas saistību apmaksai par $ 110 000, kredīts nomas līdzeklim $ 100 000 apmērā un kredīts peļņas kontā $ 10 000.

**Žurnāla ierakstu piemērs**: nomas modifikācija<br>
**Debets**: nomas saistības XXX<br>
**Kredīts**: nomas līdzeklis XXX<br>
**Kredīts**: peļņa XXX

## <a name="accumulated-depreciation"></a>Uzkrātais nolietojums

Konts ir saistīts ar LLT līdzekļa kontrāro līdzekļu kontu. Šis konts tiek kreditēts, kad tiek grāmatoti nolietojuma izdevumi.

**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi<br>
**Debets**: nolietojuma izdevumi XXX<br>
**Kredīts**: uzkrātais nolietojums XXX

## <a name="variable-payment"></a>Mainīgais maksājums

Konts ir saistīts ar mainīgiem nomas maksājumiem, kas tiek ražoti ar indeksa pārvērtēšanu saskaņā ar ASC 842, ASC 840 un SGS 17 nomu. Nomas maksājumu grafikā mainīgie maksājumi ir ietverti kolonnā **Mainīgais maksājums**. Šis konts tiek debetēts, ja rēķins tiek veidots, pamatojoties uz maksājumu grafika rindu, kas ietver mainīgo maksājumu.

**Žurnāla ierakstu piemērs**: nomas maksājums<br>
**Debets**: nomas saistības XXX<br>
**Debets**: mainīgais maksājums XXX<br>
**Kredīts**: kreditora maksājums/nomas maksājums XXX

## <a name="deferred-rent-asset-liability"></a>Atliktās nomas maksas līdzeklis (saistības)

Šis konts ir saistīts ar atlikto nomas masas līdzekli vai saistībām, ko sagatavoja atliktās nomas maksas apstrādes noma. Šis konts tiek debetēts, ja rēķins ir grāmatots ar atliktu nomas maksas apstrādes nomu, ja nomas maksājuma summa ir lielāka par perioda taisnvirziena nomas izdevumiem. Tas tiek kreditēts, ja nomas maksa ir mazāka par perioda taisnvirziena nomas izdevumiem.

**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)<br>
**Debets**: nomas izdevumi XXX<br>
**Kredīts**: atliktās nomas maksas saistības XXX<br>
**Kredīts**: kreditora maksājums/nomas maksājums XXX

## <a name="lease-expense"></a>Nomas izdevumi

Konts ir saistīts ar nomas izdevumiem, ja noma tiek klasificēta kā atlikta nomas maksas apstrādes noma. Šis konts tiek debetēts, ja rēķins ir grāmatots ar atlikto nomasas maksas apstrādes nomu.

**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)<br>
**Debets**: nomas izdevumi XXX<br>
**Kredīts**: atliktās nomas maksas saistības XXX<br>
**Kredīts**: kreditora maksājums/nomas maksājums XXX

## <a name="impairment-expense"></a>Vērtības samazinājuma izdevumi

Konts tiek iegrāmatots, ja noma ir samazinājusies. Šis konts tiek debetēts, bet LLT līdzekļu konts tiek tieši kreditēts.

**Žurnāla ierakstu piemērs**: nomas maksājums<br>
**Debets**: vērtības samazinājuma izdevumi XXX<br>
**Kredīts**: LLT līdzeklis XXX

## <a name="lease-payment"></a>Nomas maksājums

Konts tiek iegrāmatots, ja parametrs **Maksāt kreditoram** ir izslēgts. Tiek kreditēts šis konts, nevis kreditori, ja parametrs ir izslēgts.

**Žurnāla ierakstu piemērs**: nomas maksājums<br>
**Debets**: nomas saistības XXX<br>
**Kredīts**: nomas maksājums XXX

## <a name="expense-type-postings"></a>Izdevumu tipa grāmatojumi

Katram izdevumu tipam atlasītais konts tiek debetēts, ja tiek ģenerēts maksājums par šo izdevumu tipu. Piemēram, konts, kas ir norādīts izmaksu tipam **Apdrošināšana**, tiek debetēts ikreiz, kad tiek izveidots rēķins vai maksājumu žurnāla ieraksts no izpildes izmaksu grafika apdrošināšanas izdevumiem.

**Žurnāla ierakstu piemērs**: apdrošināšanas maksājums<br>
**Debets**: apdrošināšanas izdevumu tipa konts XXX<br>
**Kredīts**: korespondējošais konts XXX

> [!NOTE]
> Korespondējošais konts tiek atlasīts nomas līmenī rindās, kas attiecas uz izpildes izmaksu maksājumu grafiku. Šo korespondējošo kontu var saistīt ar kreditoru vai ar Virsgrāmatas kontu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
