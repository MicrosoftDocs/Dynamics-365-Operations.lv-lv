---
title: Pamatlīdzekļa sadalīšana
description: Šajā rakstā ir izskaidrots, kā sadalīt vienas pamatlīdzekļu grāmatas procentus jaunā pamatlīdzekļu grāmatā.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880793"
---
# <a name="split-a-fixed-asset"></a>Pamatlīdzekļa sadalīšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā sadalīt vienas pamatlīdzekļu grāmatas procentus jaunā pamatlīdzekļu grāmatā. 

## <a name="create-a-new-fixed-asset"></a>Izveidojiet jaunu pamatlīdzekli

1. Navigācijas rūtī dodieties uz **Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.
2. Atlasiet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**. Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.
4. Laukā **Nosaukums** ievadiet vērtību.
5. Aizveriet formu.

## <a name="split-a-fixed-asset"></a>Pamatlīdzekļa sadalīšana

Pirms pilnībā nolietotā līdzekļa sadalīšanas, līdzekļa grāmatas statuss ir manuāli jāmaina no **Slēgts** uz **Atvērts**. Šī darbība ir nepieciešama, jo grāmatas statusam jābūt **Atvērts**, ja ir jāgrāmato līdzekļu darbības (piemēram, izslēgšanas pārdošanai). Ir jāieslēdz arī parametrs **Vairāku darījumu atļaušana vienā dokumentā** lapas **Virsgrāmatas parametri** cilnē **Vispārīgi**. Pēc tam, kad līdzekļu grāmatošanas statuss ir mainīts un ir atļauti vairāki darījumi vienā dokumentā, veiciet tālāk norādītās darbības, lai sadalītu līdzekli.

1. Sarakstā atrodiet un atlasiet sadalāmā pamatlīdzekļa saiti.
2. Atlasiet **Grāmatas**. Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.
3. Atlasiet **Funkcijas**.
4. Atlasiet **Pamatlīdzekļa sadalīšana**.
5. Laukā **Uz pamatlīdzekli**, ievadiet vai atlasiet kādu vērtību.
6. Laukā **Uz grāmatu** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
7. Ievadiet datumu laukā **Transakcijas datums**.
8. Ievadiet skaitli laukā **Procenti**.
9. Laukā **Žurnāla nosaukums**, ievadiet vai atlasiet kādu vērtību.
10. Atlasiet **Labi**.

## <a name="post-the-journal-transaction"></a>Žurnāla transakcijas grāmatošana

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls**.
2. Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.
3. Atlasiet **Rindas**.

    - Pārbaudiet izveidotās žurnāla rindas.
    - Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.
    - Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.

4. Atlasiet **Grāmatot**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
