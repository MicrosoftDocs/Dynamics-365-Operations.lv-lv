---
title: Ignorēt noklusējuma rezervācijas principu ražošanā izmantotajiem materiāliem
description: Šajā tēmā ir aprakstīts, kā iestatīt noklusējuma rezervācijas principu katrai krājumu modeļu grupai, lai katram krājumam, kas ir daļa no ražošanas materiālu komplekta (MK) vai partijas pasūtījuma formulas, automātiski var piemērot dažādus rezervēšanas principus.
author: johanhoffmann
manager: tfehr
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8756dc22ffd64f836740124ce08dadca84207147
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078283"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Ignorēt noklusējuma rezervācijas principu ražošanā izmantotajiem materiāliem

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

*Ignorēšanas noklusējuma ražošanas rezervēšanas* funkcija ļauj iestatīt noklusējuma rezervēšanas principu katrai krājumu modeļu grupai. Tāpēc katram krājumam, kas ir daļa no ražošanas materiālu komplektu (MK) vai partijas pasūtījuma formulas, var automātiski piemērot dažādus rezervēšanas principus. Varat atlasīt, vai katrai krājumu modeļu grupai ir jāignorē pasūtījumam iestatītais noklusējuma rezervēšanas princips un kāds rezervēšanas princips jāizmanto (*manuāls*, *novērtējums*, *plānošana*, *izpilde* vai *sākums*).

Veidojot jaunu ražošanas pasūtījumu vai partijas pasūtījumu, tiek piedāvāts atlasīt rezervēšanas principu, kas jālieto laukā pasūtījumam un visām tā MK rindām vai formulas rindām. Ja tiek izmantota funkcija *Ignorēt noklusējuma ražošanas rezervāciju*, dažas vai visas MK vai formulas rindas var ignorēt šo rezervēšanas principu un tā vietā izmantot rezervēšanas principu, kas ir iestatīts atbilstošai krājumu modeļu grupai.

Piemēram, ja ir izejmateriāli vai sastāvdaļas, kam nepieciešams izdošanas darbs, MK vai formulas rindas, kas izveidotas šiem produktiem, ir nepieciešama fiziska rezervācija, jo fiziska rezervācija ir priekšnoteikums noliktavas darba izveidošanai. Parasti, ja vēlaties, lai rezervācija notiktu automātiski, atlasiet vienu no šiem rezervēšanas principiem: *novērtējums*, *plānošana*, *izpilde* vai *sākums*. No otras puses, ja jums ir materiāli vai sastāvdaļas, kam nav nepieciešams izdošanas darbs, jo tie tiek patērēti tieši no atrašanās vietas, parasti atlasiet *manuālās* rezervēšanas principu, kas nepieprasa fiziskās rezervācijas vai ģenerē izdošanasdarbu.

## <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Lai varētu izmantot līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Ražošanas kontrole*
- **Līdzekļa nosaukums:** *Ignorēt noklusējuma ražošanas rezervāciju*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Ražošanas rezervēšanas ierobežojuma piešķiršana krājumu modeļu grupai

1. Pārejiet uz sadaļu **Izmaksu pārvaldības &gt; Krājumu uzskaites politiku iestatījumi &gt; Krājumu modeļu grupas**.
1. Izveidojiet vai atlasiet krājumu modeļu grupu.
1. Kopsavilkuma cilnē **Krājumu politikas** atzīmējiet izvēles rūtiņu **Ignorēt krājuma ražošanas rezervāciju**.
1. Laukā **Rezervācija** atlasiet rezervēšanas principu krājumiem, kas pieder atlasītajai modeļu grupai. (Šie krājumi ietver krājumus, kas ir MK vai formulas rindā.)

    - **Manuāli** - krājumi modeļu grupā automātiski netiks fiziski rezervēti ražošanai. Tomēr tos joprojām var rezervēt manuāli, ja nepieciešams.
    - **Novērtējums** – krājumi modeļu grupā tiks fiziski rezervēti ražošanas pasūtījuma novērtēšanas laikā.
    - **Plānošana** – krājumi modeļu grupā tiks fiziski rezervēti ražošanas pasūtījuma plānošanas laikā.
    - **Izpilde** – krājumi modeļu grupā tiks fiziski rezervēti ražošanas pasūtījuma izpildes laikā.
    - **Sākums** – krājumi modeļu grupā tiks fiziski rezervēti ražošanas pasūtījuma sākumā.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Piemērs: rezervēšanas principu lietošana lielapjoma/pakotnes scenārijā

Lielapjoma saražotais materiāls tiek ražots 1000 litru jaucējā. Kad lielapjoma materiāls ir sagatavots, tas ir palielinājies līdz vairākām uzpildes stacijām, kur ir aizpildītas dažāda lieluma kastītes. Pēc aizpildīšanas pudeles tiek iepakotas kastēs. Tad šīs kastes tiek iepakotas uz paletēm.

Šajā scenārijā tiek izveidots partijas pasūtījums, lai izveidotu 1000 litrus lielapjoma materiāla. (Šis pasūtījums ir lielapjoma pasūtījums.) Kad šis partijas pasūtījums ir pabeigts, tiek ziņots, ka tas ir pabeigts uz aizpildīšanas staciju materiālu ievades vietu. Pēc tam tiek izveidots partijas pasūtījums katras pudeles aizpildīšanai un iepakošanai. (Šie pasūtījumi ir pakotņu pasūtījumi.) Pakošanas pasūtījumiem ir formula, kas sastāv no lielapjoma materiāla, tukšas pudeles, iezīmes un citiem iepakojuma materiāliem. Tā kā lielapjoma materiālu plūsma ir tieši no jaucēja uz aizpildīšanas stacijām, šīs sastāvdaļas izvēlei nav nepieciešams noliktavas darbs, un lielapjoma materiāls tiek patērēts tieši no ievades vietas. Tāpēc rezervēšanas princips tiek iestatīts kā *manuāls*. Pārējie materiāli ir iestatīti uz aizpildīšanas staciju pēc izdošanas darba. Tāpēc šo rindu rezervēšanas princips tiek iestatīts *izpildei*, piemēram, lai rezervēšana automātiski tiktu veikta, kad tiekizdots pakotņu pasūtījums.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]