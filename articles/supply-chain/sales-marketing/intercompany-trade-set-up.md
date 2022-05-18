---
title: Starpuzņēmumu tirdzniecības iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt starpuzņēmumu tirdzniecību
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5080267568f4d0626d2c727efb533295e7d8e397
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669409"
---
# <a name="set-up-intercompany-trade"></a>Starpuzņēmumu tirdzniecības iestatīšana

[!include [banner](../../includes/banner.md)]

Lai ļautu programmai Microsoft Dynamics 365 Supply Chain Management vadīt starpuzņēmumu tirdzniecību, ir jāiestata iespēja, ka debitori un kreditori vada starpuzņēmumu. Jāiestata arī Kreditoru parādi, Debitoru parādi, Sagāde un avoti, Pārdošana un mārketings.

## <a name="before-you-set-up-intercompany-trade"></a>Pirms starpuzņēmumu tirdzniecības iestatīšanas

Pirms starpuzņēmumu tirdzniecības iestatīšanas ir jāizlemj, kuri no klientiem ir starpuzņēmuma klienti un kuri no kreditoriem ir starpuzņēmuma kreditori. Ir jāizlemj, kurus no jūsu citiem Microsoft Dynamics 365 Supply Chain Management uzņēmumu kontiem un kuru tirdzniecības politiku izmantot starpuzņēmuma tirdzniecības saitei ar atsevišķu starpuzņēmuma klientu vai kreditoru.

It īpaši iesakām, lai jūs un jūsu organizācija zinātu starpuzņēmumu parametrus.

- Apspriediet uzstādīšanu ar vadītājiem, kas ir atbildīgi par starpuzņēmumu tirdzniecību katrā juridiskajā personā.
- Iestatiet atbilstošās vērtības katrai juridiskajai personai.

## <a name="set-up-trading-relations"></a>Tirdzniecības attiecību iestatīšana

Lai iestatītu starpuzņēmumu tirdzniecību debitoriem un kreditoriem, rīkojieties šādi.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Izvēlieties debitora kontu.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Norādiet starpuzņēmumu iestatījuma parametrus debitora kontam. Šie parametri ietver juridisko personu, kas ietver atbilstošo kreditoru un kreditora kontu. Šie parametri ietver kreditora juridisko personu un kontu, pirkšanas pasūtījumu politikas, pārdošanas pasūtījumu politikas, vērtību kartēšanu un pārdošanas līgumu un pirkšanas līgumu politikas. Varat arī norādīt, vai izmantot bāzes datu vērtības no debitora konta vai no kreditora konta citā juridiskajā personā.
1. Atkārtojiet 1.-4. darbību atlikušajiem juridiskās personas starpuzņēmumu debitoriem.
1. Dodieties uz **Kreditori \> Kreditori \> Visi kreditori**.
1. Atlasiet kreditora kontu.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Norādiet starpuzņēmumu iestatījuma parametrus kreditora kontam. Šie parametri ietver juridisko personu, kas ietver atbilstošo debitoru un debitora kontu. Šie parametri ietver pārdošanas pasūtījumu politikas, pirkšanas pasūtījumu politikas, vērtību kartēšanu un pirkšanas līgumu un pārdošanas līgumu politikas. Norādiet arī, vai izmantot bāzes datu vērtības no kreditora konta vai no debitora konta citā juridiskajā personā.
1. Atkārtojiet 6.-9. darbību atlikušajiem juridiskās personas starpuzņēmumu kreditoriem.

## <a name="set-up-products"></a>Iestatiet preces

Lai iestatītu starpuzņēmumu tirdzniecību debitoriem un kreditoriem, rīkojieties šādi.

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Visas preces un preču šabloni**.
1. Definējiet preces, kas izlaistas juridiskajām personām, kurām vēlaties veikt starpuzņēmumu tirdzniecību.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
