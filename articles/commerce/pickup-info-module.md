---
title: Saņemšanas informācijas modulis
description: Šajā tēmā tiek stāstīts par saņemšanas informācijas moduli un aprakstīts, kā to pievienot izrakstīšanās lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 52015fb973642bfc6f45901e7c1a265f0ccfc415b1324bc62ef77a5fc72550bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764565"
---
# <a name="pickup-information-module"></a>Saņemšanas informācijas modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par saņemšanas informācijas moduli un aprakstīts, kā to pievienot izrakstīšanās lapām programmā Microsoft Dynamics 365 Commerce.

Saņemšanas informācijas moduli var izmantot izrakstīšanās modulī, lai parādītu pasūtījuma saņemšanas informāciju. Klienti var skatīt pieejamos saņemšanas datumus un laika nišas un pēc tam izvēlēties piemērotāko laiku, lai paņemtu pasūtījumu. Piemēram, klients var izvēlēties saņemt pasūtījumu 21. martā plkst. 15.00 no Sanfrancisko veikala.

Commerce Headquarters ir jākonfigurē atbilstošajiem veikaliem paredzētās izdošanas laika nišas. Papildinformāciju skatiet šeit: [Izveidot un atjaunināt laika nišas klientu preču saņemšanai](dev-itpro/pickup-timeslots.md).

Ja saņemšanas informācijas modulis ir izveidots izrakstīšanās lapā, bet veikalam, kas atlasīts saņemšanai, nav definētas laika nišas, modulis parādīs informāciju, bet lietotājs nevarēs atlasīt laika nišas. Laika nišas nav obligātas un nav nepieciešams veikt pasūtījumu.

Ja ir atlasīti vairāki krājumi vairākiem veikaliem, saņemšanas informācijas modulis ļaus lietotājam izvēlēties laika nišu katram veikalam ar nosacījumu, ka laika nišas ir pieejamas.

> [!NOTE]
> Atbalsts laika nišām un izrakstīšanās saņemšanas informācijas modulim ir pieejams Dynamics 365 Commerce versijā 10.0.15 un jaunākās versijās.

Sekojošajā attēlā ir parādīts laika nišas atlases piemērs, izmantojot saņemšanas informācijas moduli, kas atrodas izrakstīšanās lapā.

![Saņemšanas informācijas moduļa piemērs norēķināšanās lapā.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

- **Virsraksts** - ievadiet virsrakstu modulim.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Rādīt laika nišu informāciju pēc tam, kad pasūtījums ir izveidots

Pēc tam, kad pasūtījums ir izveidots, informāciju par atlasīto laika nišu var apskatīt [pasūtījuma apstiprināšanas modulī](order-confirmation-module.md) un [pasūtījuma detalizētas informācijas modulī](account-management.md#order-details-page). Abiem šiem moduļiem ir rekvizīts **Parādīt laika nišu informāciju**. Pirms tiek parādīts atlasītais laika periods pasūtījuma procesa laikā, šis rekvizīts ir jāiestata uz **Patiess**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Pievienot izrakstīšanās saņemšanas informācijas moduli lapā

Instrukcijas par to, kā pievienot saņemšanas informācijas moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).

Sekojošajā attēlā parādīts e-tirdzniecības norēķinu lapas piemērs, kurā ir ietvertas saņemšanas rindu krājumu laika nišas.

![E-tirdzniecības norēķinu lapas piemērs, kurā ir ietvertas saņemšanas rindu krājumu laika nišas.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Papildu resursi

[Laikspraugu izveide un atjaunināšana izsniegšanai klientam](dev-itpro/pickup-timeslots.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Pasūtījumu informācijas modulis](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]