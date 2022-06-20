---
title: Sūtījumu pārvadātāju iestatīšana
description: Šajā rakstā ir parādīts, kā iestatīt sūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, kravas režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.
author: Weijiesa
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48586a0ddaa7cd95a81380dadffef8f276076dd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858977"
---
# <a name="set-up-shipping-carriers"></a>Sūtījumu pārvadātāju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir parādīts, kā iestatīt sūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, kravas režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme. Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.

## <a name="create-a-new-shipping-carrier"></a>Jauna nosūtījumu pārvadātāja izveide

1. Pārejiet uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Iestatīšana > Pārvadātāji > Sūtījumu pārvadātāji**.
2. Atlasiet **Jauns** darbību rūtī.
3. Ierakstiet vērtību laukā **Sūtījumu pārvadātājs**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Režīms** atlasiet opciju no nolaižamās izvēlnes.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Vispārējās informācijas ievade par nosūtījumu pārvadātāju

1. Pārslēdziet sadaļas **Pārskats** paplašinājumu.
2. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt nosūtīšanas pārvadātāju**.
3. Laukā **Kreditora konts** atlasiet opciju no nolaižamās izvēlnes. Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.  
4. Atlasiet opciju laukā **Transportēšanas norēķinu veids**. Atlasiet **Manuāli**, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet **EDI**, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).  
5. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt pārvadātāja vērtējumu**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam

1. Pārslēdziet sadaļas **Pakalpojumi** paplašinājumu.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Pārvadātāja pakalpojums**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Kravas veidnes ID** atlasiet noslodzes veidni, kuru saistīt ar pakalpojumu. Kravas veidne nosaka maksimālos mērījumus visas kravas svaram un tilpumam. Piemēram, kravas veidne var atspoguļot konteinera vai kravas automašīnas lielumu. Kravas veidnes ID ir norādīti [arī](load-building-workbench.md) noslodzes veidošanas veidnēs un, izmantojot noslodzes veidošanas darba rīks, kas palīdz lietot noslodzes veidošanas stratēģijas kravu izveidošanai. Tādēļ sistēma varēs saskaņot katru jauno noslodzi ar piemērotu kravas pārvadātāja pakalpojumu, salīdzinot norādītos kravas veidnes ID.
6. Laukā **Pārvadāšanas metode** atlasiet opciju no nolaižamās izvēlnes.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Iestatiet pārvadātāja adresi (nav obligāti)

1. Pārslēdziet sadaļas **Adreses** izvēršanu.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums vai apraksts** ierakstiet vērtību.
4. Laukā **Valsts/reģions** atlasiet opciju no nolaižamās izvēlnes.
5. Laukā **Pasta indekss** atlasiet opciju no nolaižamās izvēlnes.
6. Laukā **Iela** ierakstiet kādu vērtību.
7. Atlasiet **Labi**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu

1. Pārslēdziet sadaļas **Novērtējuma profili** izvēršanu.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Novērtējuma profils**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Vieta** atlasiet opciju no nolaižamās izvēlnes.
6. Laukā **Noliktava** atlasiet opciju no nolaižamās izvēlnes.
7. Laukā **Likmes noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes. Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.  
8. Laukā **Likmes šablons** atlasiet opciju no nolaižamās izvēlnes.
9. Laukā **Pārvadājumu ilguma noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.
10. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]