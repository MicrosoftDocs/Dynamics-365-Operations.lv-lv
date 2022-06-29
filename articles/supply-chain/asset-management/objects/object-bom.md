---
title: Līdzekļa MK
description: Šajā rakstā ir aprakstīti pamatlīdzekļu materiālu komplekti (MK) Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 665c705e3ffb617fc159a1223cb3f776878d5cd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016251"
---
# <a name="asset-boms"></a>Līdzekļa MK

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā ir aprakstīti pamatlīdzekļu materiālu komplekti (MK) Pamatlīdzekļu pārvaldībā. Lapā **Līdzekļa MK** tiek parādīts visu to preču (rezerves daļu un citu vienību) saraksts, kuras tiek izmantotas līdzeklism visā tā dzīves cikla laikā. Kad veidojat jaunu līdzekli, apsveriet iespēju iestatīt līdzekļa MK kā iestatīšanas procedūras daļu. Šādi var izsekot līdzekļa vienību vēsturi no izveides datuma.

Kad esat pabeidzis uzturēšanas darbu un krājuma patēriņš ir reģistrēts darba pasūtījumā, varat izsekot to rezerves daļu un citu vienību patēriņu, kas ir izmantotas līdzeklim. Šī funkcionalitāte ļauj saglabāt pilnīgu vienību patēriņa ierakstu par visiem jūsu līdzekļiem. Piemēram, var izmantot ierakstu, lai pārraudzītu, vai konkrēta rezerves daļa bieži tiek aizstāta, vai lai reģistrētu rezerves daļas vai citas vienības, kas pašlaik tiek izmantotas līdzeklim.

> [!NOTE]
> Darba pasūtījumā krājuma patēriņš var ietvert gan rezerves daļas, gan citas papildu vienības, piemēram, smērvielas, bultskrūves un starplikas.

Līdzekļa MK var automātiski atjaunināt, pamatojoties uz iestatījumu Līdzekļu pārvaldībā. Ja darba pasūtījuma dzīves cikla stāvoklis ir izveidots, lai apstrādātu pabeigtos vai izpildītos darba pasūtījumus, un ja opcija **Atjaunināt līdzekļa MK** šim darba pasūtījuma dzīves cikla stāvoklim ir iestatīta uz **Jā** lapā **Darba pasūtījuma dzīves cikla stāvokļi**, visas vienības, kas izmantotas darba pasūtījumam, tiek automātiski atjauninātas lapā **Līdzekļa MK**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli. 


Varat arī manuāli atjaunināt līdzekļa MK, izveidojot jaunas vienību rindas lapā **Līdzekļa MK**.

Lapā **Līdzekļa MK** varat izsekot rezerves daļu vēsturi līdzekļiem pēc tam, kad vienību patēriņš ir reģistrēts darba pasūtījumā. Lai izmantotu šo funkcionalitāti, ir jāatlasa vienību grupas, kas jāizmanto rezerves daļu reģistrēšanai lapā **Rezerves daļu vienību grupas**.

Lai izmantotu līdzekļa MK funkcionalitāti, vispirms ir jāiestata nepieciešamās rezerves daļu vienību grupas. Pēc tam, ja vēlaties, lai līdzekļa MK tiktu automātiski atjaunināts, kad darba pasūtījums ir pabeigts, varat iestatīt darba pasūtījuma dzīves cikla stāvokli, lai apstrādātu šo atjauninājumu. 


## <a name="set-up-spare-parts-item-groups"></a>Rezerves daļu vienību grupu iestatīšana

Rezerves daļu vēstures iestatīšana ir balstīta uz vienību grupām, kas izveidotas modulī **Krājumu un noliktavas pārvaldība**. Līdzekļu pārvaldībā iestatiet vienību grupas, lai varētu izsekot rezerves daļu vēsturi vienībām atlasītajās krājumu grupās.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzeklis** \> **Rezerves daļu vienību grupas**.
2. Atlasiet **Jauns**, lai iestatītu vienību grupu.
3. Atlasiet grupu laukā **Vienības grupa**. Grupas nosaukums tiek automātiski ierakstīts laukā **Nosaukums**.

## <a name="view-and-update-asset-boms"></a>Llīdzekļa MK skatīšana un atjaunināšana

Pēc vienību patēriņa iegrāmatošanas darba pasūtījumā varat skatīt reģistrēto vienību patēriņu lapā **Līdzekļa MK**.

1. Atlasiet **Aktīvu pārvaldības** \> **līdzekļi** \> **Aktīvie pamatlīdzekļi**. Atlasiet sarakstā līdzekli un pēc tam atlasiet **Llīdzekļa MK**.

    > [!NOTE]
    > Lai skatītu visu vienību patēriņa reģistrācijas par visiem līdzekļiem, atlasiet **Līdzekļu pārvaldība** \> **Uzziņas** \> **Līdzekļi** \> **Līdzekļa MK**.

2. Atlasiet **Atjaunināt līdzekļa MK**. Varat pēc vajadzības pievienot līdzekļus, līdzekļu veidus un resursus ajauninājumam, atlasot **Atlasīt**. Atlasiet **Labi**, lai sāktu atjaunināšanu. Varat arī iestatīt atjaunināšanas funkciju kā pakešuzdevumu.
3. Ja vēlaties redzēt papildu informāciju, kas saistīta ar vienībām, varat pievienot krājumu dimensijas. Atlasiet **Krājumi** \> **Dimensiju parādīšana** un pēc tam atlasiet izvēles rūtiņas dimensijām, kuras vēlaties skatīt. Lai paturētu šo iestatījumu visiem līdzekļiem lapā **Līdzekļa MK**, iestatiet opciju **Saglabāt iestatījumu** uz **Jā**.
4. Lai iegūtu pārskatu par to, kur Līdzekļu pārvaldībā tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem, atlasiet **Vienība tika izmantota**. 
5. Ja vēlaties redzēt tikai aktīvo vienību rindas, atlasiet **Skatīt** \> **Pašreizējais**. Lai skatītu visas vienību rindas, ieskaitot rindas, kurās beigu datums ir agrāks par pašreizējo datumu, atlasiet **Skatīt** \> **Viss**.

> [!NOTE]
> Kad esat pabeidzis darba pasūtījumu, ja dažām vienībām vai rezerves daļām, kas saistītas ar saistīto līdzekli, ir beidzies derīguma termiņš vai arī tās ir aizstātas ar citām vienībām vai rezerves daļām, ieteicams attiecīgi atjaunināt līdzekļa MK.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Jaunas vienības rindas izveide līdzekļa MK

Varat manuāli izveidot vienību rindas līdzekļiem.

1. Lapā **Līdzekļa MK** atlasiet **Jauns**.
2. Laukā **Līdzeklis** atlasiet līdzekli, kuram pievienot vienības rindu.
3. Laukā **Rindas numurs** ievadiet secīgu rindas numuru.
4. Laukā **Ir spēkā** ievadiet sākuma datumu attiecīgajai vienībai.
5. Ja vienībai beigsies derīguma termiņš, laukā **Beigu datums** ievadiet beigu datumu.
6. Laukā **Vienības numurs** atlasiet vienību. Nosaukums tiek automātiski ievadīts laukā **Preces nosaukums**.
7. Laukā **Daudzums** ievadiet daudzumu. Lauks **Mērvienība** tiek automātiski atjaunināts.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]