---
title: Bāzes izmaiņas ICMS-DIF nodokļa aprēķinos precēm no piegādātājiem citās valstīs
description: Šajā rakstā ir aprakstīta ICMS-DIF nodokļu tipa aprēķinu konfigurācija, kad finanšu dokuments tiek saņemts Plkst. Mk (RS) vai São Papildmaksas (SP) stāvoklī.
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868267"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Bāzes izmaiņas ICMS-DIF nodokļa aprēķinos precēm no piegādātājiem citās valstīs

Šajā rakstā ir aprakstīta ICMS-DIF **nodokļu tipa aprēķinu konfigurācija, kad finanšu dokuments tiek saņemts** Plkst. Mk (RS) vai São Papildmaksas (SP) stāvoklī.

Atbilstoši valsts likuma definīcijai, Imposto sobre Circulação de Mercadorias e Serviços (ICMS), kas tiek apkopota, jāatbilst šim noteikumam:

*ICMS* apkopot = ([(*Operācijas* summa - *ICMS no* avota) ÷ (1 – *ICMS %* iekšējais)] × *ICMS %* iekšējais) – *ICMS summa no avota*

## <a name="example"></a>Paraugs

Brazīlijas uzņēmums RS stāvoklī saņem finanšu dokumentu pirkšanai no kreditora SP stāvoklī. Uzņēmumam jāsavāc ICMS procentuālā starpība starp RS stāvokli (18 procenti) un SP stāvokli (12 procenti). Tomēr bāze jāaprēķina saskaņā ar iepriekšējo noteikumu.

- **Operācijas summa:** 1 000,00 Brazīlijas reāls (R$ 1000,00)
- **ICMS starpstate:** R$ 120,00
- **ICMS procenti RS stāvoklī:** 18 procenti
- **ICMS apkopošanai RS stāvoklī:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Novēršana

Lai aprēķinātu diferenciāālu ICMS (ICMS-DIF) saskaņā ar RS statusa nosacījumiem, PVN kodi un PVN grupa jāiestata šādā veidā:

1. Izveidojiet PVN kodu, lai saņemtu 12 procentu ICMS (citam štatam). Šis kods tiek izmantots, lai reģistrētu kreditora nodokļu saņemamo summu.
2. Izveidojiet PVN kodu, lai savāktu ICMS-DIF. Lai definētu 18 procentu un 12 procentu starpību, šim PVN kodam procentuālajai summai jābūt 18 procenti (savam štatam). Iestatiet nodokļa tipu kā **ICMS-DIF**. Šis PVN kods aprēķina parametros jādefinē šādi:

    - Laukā **Izcelsme atlasiet bruto** summas **procentus**.
    - Aprēķina bāzes **laukā** atlasiet neto **summu katrai rindai** vai rēķina **bilances neto summu**.
    - Nosakiet taksācijas kodu tā, lai tam finanšu vērtība būtu **3**. Šādā veidā korekcijas darbība tiks automātiski izveidota, kad ir iespējots **finanšu** grāmatu modulis.
    - PVN grupas konfigurācijā atlasiet opciju **Izmantot** **nodokli ICMS-DIF** PVN kodam.
