---
title: Izveidot līdzekļus, pamatojoties uz pirkšanas pasūtījumiem
description: Šajā tēmā ir paskaidrots, kā var izveidot to līdzekļu vienību sarakstu, kurus var izmantot par pamatu uzturēšanas darbu līdzekļu veidošanai Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5068712a7ea1e0d940d4a05a411fb3e1b6f6d9bb9be924d5375b16676561ea1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754111"
---
# <a name="create-assets-based-on-purchase-orders"></a>Izveidot līdzekļus, pamatojoties uz pirkšanas pasūtījumiem

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidrots, kā var izveidot to līdzekļu vienību sarakstu, kurus var izmantot par pamatu uzturēšanas darbu līdzekļu veidošanai Līdzekļu pārvaldībā. Pamatojoties uz līdzekļu vienībām, varat skatīt to pirkšanas pasūtījuma rindu sarakstu, kuras ir izveidotas šīm vienībām. Šīs funkcionalitātes nolūks ir viegli izveidot līdzekli Līdzekļu pārvaldībā, pamatojoties uz pirkšanas pasūtījumu.

Vispirms iestatiet vienības, kas jāizmanto līdzekļu veidošanai no pirkšanas pasūtījuma **Līdzekļu vienībās**. Pēc pirkšanas pasūtījuma rindas izveidošanas jūs veidojat līdzekļus **Gaidošie līdzekļi**. Ir iespējams izlemt, kurā pirkšanas pasūtījuma stadijā līdzeklis būtu jāizveido.


## <a name="select-asset-items"></a>Atlasīt līdzekļa vienības

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļi** > **Vienības**.
2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu līdzekļa vienību.
3. Atlasiet vienību laukā **Vienības kods**. Izejot no šī lauka, vienības nosaukums tiek automātiski ievietots laukā **Preces nosaukums.**
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet vienības līdzekļa tipu.
5. Atlasiet vienības līdzekļa ražotāju un modeli.
6. Saglabājiet vienību.


## <a name="create-assets-from-pending-assets"></a>Līdzekļu izveide no gaidošiem līdzekļiem

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Gaidošie līdzekļi**.
2. Tiks parādīts pirkšanas pasūtījumu atjaunināts saraksts, pamatojoties uz vienībām, kas atlasītas laukā **Līdzekļu vienības**.
3. Varat filtrēt pirkšanas pasūtījumu statusu, lai atlasītu, kurā dzīves cikla stāvoklī šis līdzeklis ir jāizveido. Piemēram, varat izveidot līdzekļus tikai tad, ja preču ieejas plūsma ir iegrāmatota pirkšanas pasūtījumā.
4. Pirkšanas pasūtījuma rindā atlasiet saiti **Atsauces numurs**, lai skatītu detalizētu informāciju par vienību.
5. Ja vēlaties rediģēt, kuras dimensijas tiek rādītas kopsavilkuma cilnē **Krājumu dimensijas**, noklikšķiniet uz pogas **Rādīt dimensijas** un veiciet atlasi.
6. Ja vēlaties izveidot līdzekli, kura pamatā ir pirkšanas pasūtījuma rinda, saraksta lapā atzīmējiet izvēles rūtiņu kolonnā **Atzīmēt** un noklikšķiniet uz **Izveidot līdzekļus**. Tiks parādīts ziņojums, informējot jūs par līdzekļa ID.
7. Atlasiet līdzekli sarakstā **Visi līdzekļi** un noklikšķiniet uz pogas **Rediģēt**, lai pievienotu līdzeklim vairāk informācijas.
8. Laukā **Gaidošie līdzekļi**, ja vēlaties dzēst rindu, jo nevēlaties izveidot līdzekli, atlasiet izvēles rūtiņu rindas kolonnā **Atzīmēt** un noklikšķiniet uz **Atmest gaidošos līdzekļus**. Tiks parādīts ziņojums, informējot jūs par līdzekļa ID. Jūs nedzēšat pirkšanas pasūtījumu vai pārdošanas pasūtījumu — tikai to ierakstu, no kura jūs varētu būt izveidojis līdzekli **Līdzekļu pārvaldībā**.

>[!NOTE]
>Visas preces dimensijas (izmērs, krāsa, konfigurācija utt.) tiek automātiski pārsūtītas uz līdzekļa atribūtiem. Izsekošanas dimensijas (sērijas numurs) tiek glabātas tieši uz līdzekļa, kad līdzeklis ir izveidots.


## <a name="find-pending-assets"></a>Atrast gaidošos līdzekļus

Varat palaist **Gaidošo līdzekļu skaitīšanu**, lai pārbaudītu, vai nav gaidošo līdzekļu. Piemēram, šo funkciju var izmantot, lai saņemtu paziņojumu katru reizi, kad gaidošie līdzekļi ir gatavi, lai tos izveidotu kā līdzekli.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Gaidošo līdzekļu skaitīšana**.
2. Noklikšķiniet uz **Labi**, lai palaistu darbu un atjauninātu sarakstu **Gaidošajos līdzekļos**.
3. Šo darbu var iestatīt, lai palaistu kā pakešuzdevumu, piemēram, reizi dienā.

**Brīdinājums:** ja dati pirkšanas pasūtījumā tiek mainīti *pēc tam*, kad līdzeklis ir izveidots, pamatojoties uz atbilstīgo vienību, šīs izmaiņas līdzeklim netiks atspoguļotas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]