---
title: Līdzekļu patapinājumi
description: Šajā rakstā ir aprakstīts, kā reģistrēt patapinājuma pamatlīdzekļus Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ced5ec174fe1885273241be5f9fd48b7947129af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846276"
---
# <a name="asset-loans"></a>Līdzekļu patapinājumi

[!include [banner](../../includes/banner.md)]

 

Ja jūsu uzņēmums saņem līdzekļus remonta vai uzturēšanas darbiem no iekšējām atrašanās vietām vai debitoriem, un, ja jūs īslaicīgi patapināt līdzekļus šīm atrašanās vietām vai debitoriem, Līdzekļu pārvaldība var izsekot līdzekļu patapinājumus.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Reģistrēt līdzekļu patapinājumus uzturēšanas pieprasījumā

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.
2. Atlasiet uzturēšanas pieprasījumu, lai reģistrētu līdzekļa patapinājumu un pēc tam atlasiet **Rediģēt.**
3. Lapā **Pieprasījums** atlasiet **Nosūtīt patapinājuma līdzekli**.
4. Atlasiet līdzekli un ievadiet plānoto atgriešanas datumu.
5. Atlasiet **Labi**.

> [!NOTE]
> - Varat nosūtīt patapinājuma līdzekli tikai tad, ja ir pieejams tā paša līdzekļu tipa aktīvs.
> - Līdzeklim, kuru patapināt, ir jābūt līdzekļa dzīves cikla statusam, kas ļauj to izmantot kā patapinājuma līdzekli, piemēram, **InStorage**. Kad līdzekļa patapinājums ir reģistrēts, līdzekļa dzīves cikla statuss automātiski tiek atjaunināts uz, piemēram, **OnLoan**.

Lai skatītu sarakstu ar visiem līdzekļiem, kurus esat patapinājis citai atrašanās vietai vai debitoriem, atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļa patapinājums** \> **Visi līdzekļu patapinājumi**. Ja līdzeklim ir atzīmēta izvēles rūtiņa **Pabeigts**, līdzeklis ir reģistrēts kā atgriezts jūsu uzņēmumam.

![Uzturēšanas pieprasījumu pārvaldība.](media/06-manage-maintenance-requests.png)

Lapā **Aktīvie līdzekļu patapinājumi** varat skatīt visu to patapinājuma līdzekļu sarakstu, kas vēl nav atgriezti jūsu uzņēmumam.

## <a name="register-loan-assets-as-returned"></a>Reģistrēt patapinājuma līdzekļus kā atgrieztus

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļa patapinājums** \> **Aktīvie līdzekļu patapinājumi**.
2. Atlasiet līdzekļa patapinājumu, lai reģistrētu kā atgrieztu, un pēc tam atlasiet **Atgriezt līdzekļa patapinājumu**.
3. Laukā **Atgriezts** ievadiet datumu un laiku.
4. Atlasiet **Labi**.
5. Atsvaidziniet saraksta **Aktīvie līdzekļu patapinājumi** lapu un pievērsiet uzmanību, ka līdzekļa patapinājums vairs nav redzams sarakstā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]