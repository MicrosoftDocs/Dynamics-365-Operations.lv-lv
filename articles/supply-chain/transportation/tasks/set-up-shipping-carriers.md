---
title: Sūtījumu pārvadātāju iestatīšana
description: Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.
author: Henrikan
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e9bc4fefb6aabc0b93d4d96f5930590ef99235b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567660"
---
# <a name="set-up-shipping-carriers"></a>Sūtījumu pārvadātāju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme. Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.


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
5. Laukā **Pārvadāšanas metode** atlasiet opciju no nolaižamās izvēlnes.

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