---
title: Pamatlīdzekļu nolietojums
description: Šajā tēmā ir sniegts pārskats par pamatlīdzekļu nolietojumu.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ec8544b885485781b0b9c0a59ec47f90fdceb6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826886"
---
# <a name="fixed-asset-depreciation"></a>Pamatlīdzekļu nolietojums

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par pamatlīdzekļu nolietojumu.

Nolietojums ir periodiska darbība, kas parasti samazina pamatlīdzekļa vērtību bilancē un tiek maksāta kā izdevumi peļņas un zaudējumu kontā. Tāpēc galvenais konts parasti tiek izmantots, lai kreditētu periodisko nolietojumu bilancē. Korespondējošais konts ir konts kontu plāna peļņas un zaudējumu daļā.

## <a name="depreciation-adjustment"></a>Nolietojuma korekcijas
Parasti tikai jau grāmatotas nolietojuma darbības korekcija tiek grāmatota kā nolietojuma korekcija. Tāpēc gan galvenais konts, gan korespondējošais konts tiek iestatīts tāpat kā nolietojuma konts. Nolietojuma korekcija var būt gan pozitīva summa, gan negatīva summa, taču galvenā konta (kā bilances konta) funkcionalitāte un korespondējošā konta (parasti kā peļņas un zaudējumu konta) funkcionalitāte paliek tā pati.

## <a name="extraordinary-depreciation"></a>Ārkārtas nolietojums
Ārkārtas nolietojums darbojas tāpat kā pamata nolietojums. Līdz ar to galvenais konts tiek izmantots, lai kreditētu nolietojuma summu bilancē un samazinot pamatlīdzekļa vērtību. Korespondējošais konts ir peļņas un zaudējumu konts, kur nolietojums, kas tiek aprēķināts finanšu periodam, tiek apmaksāts kā izdevumi. 

Ārkārtas nolietojums darbojas neatkarīgi no pamata nolietojuma. Izmantojot ārkārtas nolietojumu kā atsevišķu darbības tipu, varat grāmatot un sniegt pārskatu par ārkārtas nolietojumu atsevišķi no pamata nolietojuma.

## <a name="special-depreciation-allowance"></a>Speciālā nolietojuma atļautais daudzums
Speciālā nolietojuma atļauto daudzumu var lietot, lai iegūtu papildnolietojuma summas pirmā gada laikā, kurā pamatlīdzeklis tiek nodots ekspluatācijā un nolietots. Speciālā nolietojuma atļautais daudzums ir jāizmanto pirms pārējiem nolietojuma aprēķiniem. Tā kā speciālā nolietojuma atļautais daudzums bieži vien kļūst zināms tikai pēc tam, kad pagājis noteikts pamatlīdzekļa lietošanas laiks, šo nolietojuma veidu ieteicams lietot ar grāmatu, kuras ieraksti netiek grāmatoti virsgrāmatā. Varat izmantot periodisko funkciju Dzēst virsgrāmatā negrāmatotās transakcijas, lai dzēstu šīm grāmatām darbību vēsturi. Pēc tam varat dzēst nolietojuma vēsturi pamatlīdzekļu grāmatai, grāmatot speciālā nolietojuma atļauto daudzumu, kad tas ir zināms, un pēc tam grāmatot atlikušās nolietojuma darbības par attiecīgo gadu. 

Var izveidot neierobežotu speciālā nolietojuma atļautā daudzuma ierakstu skaitu. Pēc šo ierakstu piešķiršanas līdzekļu grupas grāmatai tie tiek lietoti attiecīgajai līdzekļu grāmatai. 

Speciālā nolietojuma atļautais daudzums tiek ievadīts kā procenti vai fiksēta summa. Grāmatojot nolietojuma priekšlikumus, speciālā nolietojuma atļautā daudzuma darbības tiek grāmatotas grāmatā kā darbības, kas ir atsevišķi no nolietojuma darbībām.

## <a name="depreciation-calendars"></a>Nolietojuma kalendāri
Katrai grāmatai ir kalendārs, ko izmanto, aprēķinot pamatlīdzekļu nolietojumu. Pēc noklusējuma, ja nenorādīsiet kalendāru grāmatai, grāmata izmantos virsgrāmatas finanšu kalendāru. Nepieciešams atlasīt finanšu kalendāru grāmatai, ja ar grāmatu saistītais nolietojuma profils izmanto finanšu nolietojuma gadu. 

Varat izveidot koplietojamu kalendāru, izmantojot sadaļas Virsgrāmata lapu **Finanšu kalendāri**.

Papildinformāciju skatiet rakstā [Nolietojuma metodes un konvencijas](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]