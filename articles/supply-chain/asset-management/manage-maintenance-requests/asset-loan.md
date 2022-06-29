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
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015759"
---
# <a name="asset-loans"></a>Līdzekļu patapinājumi

[!include [banner](../../includes/banner.md)]

 

Ja jūsu uzņēmums saņem līdzekļus remonta vai uzturēšanas darbiem no iekšējām atrašanās vietām vai debitoriem, un, ja jūs īslaicīgi patapināt līdzekļus šīm atrašanās vietām vai debitoriem, Līdzekļu pārvaldība var izsekot līdzekļu patapinājumus.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Reģistrēt līdzekļu patapinājumus uzturēšanas pieprasījumā

1. Atlasiet Līdzekļu **pārvaldības uzturēšanas** \> **pieprasījumus visiem** \> **uzturēšanas pieprasījumiem vai** Aktīvajai **uzturēšanai pieprasījumus.**
2. Atlasiet uzturēšanas pieprasījumu, lai reģistrētu līdzekļa patapinājumu un pēc tam atlasiet **Rediģēt.**
3. Lapā **Pieprasījums** atlasiet **Nosūtīt patapinājuma līdzekli**.
4. Atlasiet līdzekli un ievadiet plānoto atgriešanas datumu.
5. Atlasiet **Labi**.

> [!NOTE]
> - Varat nosūtīt patapinājuma līdzekli tikai tad, ja ir pieejams tā paša līdzekļu tipa aktīvs.
> - Līdzeklim, kuru patapināt, ir jābūt līdzekļa dzīves cikla statusam, kas ļauj to izmantot kā patapinājuma līdzekli, piemēram, **InStorage**. Kad līdzekļa patapinājums ir reģistrēts, līdzekļa dzīves cikla statuss automātiski tiek atjaunināts uz, piemēram, **OnLoan**.

Lai apskatītu visu to pamatlīdzekļu sarakstu, ko esat patapinājuši citām atrašanās vietām vai klientiem, **atlasiet Pamatlīdzekļu vadības** \> **Pamatlīdzekļu** \> **patapinājumus Visus līdzekļu patapinājumus.** Ja līdzeklim ir atzīmēta izvēles rūtiņa **Pabeigts**, līdzeklis ir reģistrēts kā atgriezts jūsu uzņēmumam.

![Uzturēšanas pieprasījumu pārvaldība.](media/06-manage-maintenance-requests.png)

Lapā **Aktīvie līdzekļu patapinājumi** varat skatīt visu to patapinājuma līdzekļu sarakstu, kas vēl nav atgriezti jūsu uzņēmumam.

## <a name="register-loan-assets-as-returned"></a>Reģistrēt patapinājuma līdzekļus kā atgrieztus

1. Izvēlieties **Aktīvu pārvaldības Aktīvu** \> **patapinājumu** \> **Aktīvie aktīvu patapinājuma līdzekļi.**
2. Atlasiet līdzekļa patapinājumu, lai reģistrētu kā atgrieztu, un pēc tam atlasiet **Atgriezt līdzekļa patapinājumu**.
3. Laukā **Atgriezts** ievadiet datumu un laiku.
4. Atlasiet **Labi**.
5. Atsvaidziniet saraksta **Aktīvie līdzekļu patapinājumi** lapu un pievērsiet uzmanību, ka līdzekļa patapinājums vairs nav redzams sarakstā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]