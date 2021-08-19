---
title: Patēriņa atskaišu veidošana
description: Šajā tēmā ir paskaidrots, kā izveidot patēriņa atskaites programmā Asset Management.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e54511932ee9487cccae12a479dd210b5978c593dd7000ec2dfe09c3c4014670
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711981"
---
# <a name="create-consumption-reports"></a>Patēriņa atskaišu veidošana

[!include [banner](../../includes/banner.md)]

 

Kad ir izveidota un publicēta patēriņa reģistrācija darba pasūtījumiem programmā Asset Management, ir pieejamas divas atskaites, kas parāda patēriņa informāciju.


## <a name="asset-consumption-report"></a>Līdzekļu patēriņa atskaite

Kad ir publicēts darba pasūtījumu patēriņš, varat izdrukāt līdzekļa patēriņa atskaiti. Atskaitē parādītas stundas, stundas izmaksas, vienuma izmaksas, līdzekļiem publicētie izdevumi.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Atskaites** > **Līdzekļi** > **Līdzekļu patēriņš**.

2. Dialogā **Līdzekļu patēriņš** atlasiet parametrus un detaļu līmeni, ko gribat redzēt, atlasot **Jā** attiecīgajās pārslēgšanas pogās un ievietojot funkcionālo novietojumu sadaļā **Rādīt**.
    - Jūs varat izmantot lauku **Līmeņi**, lai noteiktu, cik detalizētas vēlaties līdzekļa rindas attiecībā uz funkcionālo novietojumu. 
    
        Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visi līdzekļi funkcionālajam novietojumam tiks uzrādīti augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienots no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
        
        Ja laukā **Līmeņi** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs līdzekļus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti. 
        
    - Lai redzētu summas katram apakšlīdzeklim atskaitē, atlasiet **Jā** pārslēgšanas pogā **Visu apakšlīdzekļu summa**.

3. Atlasiet datuma intervālu sadaļā **Datumi**.

4. Kopsavilkuma cilnē **Galamērķis** atlasiet, vai vēlaties skatīt atskaiti ekrānā, izdrukāt vai saglabāt kā failu vai e-pasta ziņojumu.

5. Ja vajadzīgs, varat atlasīt konkrētus līdzekļus, ko parādīt atskaitē. Kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un pievienojiet līdzekļus, ko vēlaties iekļaut sarakstā.

6. Klikšķiniet **Labi**, lai izveidotu pārskatu.


## <a name="work-order-consumption-report"></a>Darba pasūtījuma patēriņa atskaite

Kad ir publicēts darba pasūtījumu patēriņš, varat izdrukāt darba pasūtījumu patēriņa atskaiti. Atskaitē parādītas darba pasūtījumiem publicētās stundas, stundas izmaksas, vienuma izmaksas, izdevumi.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Atskaites** > **Darba pasūtījumi** > **Darba pasūtījumu patēriņš**.

2. Dialogā **Darba pasūtījuma patēriņš** atlasiet parametrus, ko vēlaties iekļaut atskaitē, atlasot **Jā** attiecīgajās pārslēgšanas pogās un ievietojot funkcionālo novietojumu sadaļā **Rādīt**.

3. Atlasiet datuma intervālu sadaļā **Datumi**.

4. Kopsavilkuma cilnē **Galamērķis** atlasiet, vai vēlaties skatīt atskaiti ekrānā, izdrukāt vai saglabāt kā failu vai e-pasta ziņojumu.

5. Ja vajadzīgs, varat atlasīt konkrētus darba pasūtījumus, ko parādīt atskaitē. Kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un pievienojiet darba pasūtījumus, ko vēlaties iekļaut sarakstā.

6. Klikšķiniet **Labi**, lai izveidotu pārskatu.


>[!NOTE]
>Varat arī izveidot [darba pasūtījuma atskaiti](../work-orders/work-order-report.md), kas satur vel vairāk darba pasūtījuma detaļu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]