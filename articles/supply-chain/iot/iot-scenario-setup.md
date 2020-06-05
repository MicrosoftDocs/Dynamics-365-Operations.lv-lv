---
title: IoT informācijas scenārija iestatīšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt IoT informācijas Supply Chain Management scenāriju.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386538"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT informācijas scenārija iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt IoT informācijas Supply Chain Management scenāriju. Pirms scenāriju iestatīšanas ir [jāiestata LCS](iot-lcs-setup.md).

Šajā tēmā jūs konfigurēsit scenāriju **Aprīkojuma dīkstāve**, lai izveidotu paziņojumu Supply Chain Management, kad iekārta netiek izmantota.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju **Aprīkojuma dīkstāve** Supply Chain Management

Scenārijs **Aprīkojuma dīkstāve** kartē iekārtas brīdinājuma sliekšņa izslēgšanas signālu. Iekārta tiek uzraudzīta tikai tad, ja iekārta ir izvēlēta scenārijam un ir iestatīta Supply Chain Management darbam. Ja laiks, kas pagājis kopš iekārtas pēdējā saņemtā izslēgšanas signāla ir lielāks nekā brīdinājuma robežvērtība, tiek parādīts paziņojums **Iekārta dīkstāvē**. Ja iekārta joprojām darbojas, kad tiek saņemts nākamais **PartOut** signāls, tiek parādīts paziņojums **Iekārta darbojas**. Ja iekārta pārstāj darboties uz 30 min., tiek parādīts jauns paziņojums **Iekārta dīkstāvē**.

Scenārijam **Aprīkojuma dīkstāve** ir šādas atkarības:

+ Lai brīdinājums tiktu parādīts, ražošanas pasūtījumam ir jādarbojas kartētā iekārtā.
+ Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē kartētās iekārtas izslēgšanas signālu.
+ IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.

Lai konfigurētu scenāriju, rīkojieties šādi:

1. Piesakieties Supply Chain Management.
2. Iespējojiet IoT informācijas līdzekļa karodziņu. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurējiet rādītājus. Papildinformāciju skatiet [Rādītāju konfigurēšana](iot-metrics-setup.md#configure-metrics).
4. Pārejiet uz **Ražošanas kontrole**.
5. Pārejiet uz **Iestatījumi \> IoT informācija \> Scenārija pārvaldība**.
6. Noklikšķiniet uz **Konfigurēt**, kas atrodas **Aprīkojuma dīkstāve** elementā. Konfigurācijas vednis sākas ar lapu **Aprīkojuma sensora shēmas definīcija**. Mērķis ir iestatīt shēmu Supply Chain Management, lai tā atbilstu IoT ziņojumu JSON formātam. Var tikt definētas vairākas ziņojumu shēmas. Papildinformāciju skatiet [Ziņojumu shēmas formāti IoT centrmezglam](iot-schema-format.md). Šajā piemērā ziņojuma lietderīgā slodze satur ziņojumu paketi ar šādu formātu:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Pievienojiet tabulai rindu.

    1. Iestatiet **Shēmas nosaukumu** uz **ID**.
    2. Iestatiet **Shēmas ceļu** uz **/payload[\*]/id**.
    3. Iestatiet **Aprakstu** uz **Ziņojuma ID**.

8. Pievienojiet tabulai rindu.

    1. Iestatiet **Shēmas nosaukumu** uz **Laikspiedols**.
    2. Iestatiet **Shēmas ceļu** uz **/payload[\*]/timestamp**.
    3. Iestatiet **Aprakstu** uz **Ziņojuma laikspiedols**.

9. Pievienojiet tabulai rindu.

    1. Iestatiet **Shēmas nosaukumu** uz **Vērtība**.
    2. Iestatiet **Shēmas ceļu** uz **/payload[\*]/value**.
    3. Iestatiet **Aprakstu** uz **Ziņojuma vērtība**.

    Nav nepieciešams definēt visus ziņojuma rekvizītus, tikai tos, kas nepieciešami. Šajā piemērā netika veidota rinda **Saknes laikspiedols**. **Saknes laikspiedola** ceļš būtu **/timestamp**.
  
10. Noklikšķiniet uz **Tālāk**, lai dotos uz lapu **Aprīkojuma sensora shēmas karte**.
11. Rindā **Aprīkojuma resursa ID** iestatiet **Shēmas nosaukumu** uz **ID**. Derīgās vērtības tiek rādītas nolaižamajā tabulā.
12. Rindā **UTC laiks** iestatiet **Shēmas nosaukumu** uz **Laikspiedols**. Derīgās vērtības tiek rādītas nolaižamajā tabulā.
13. Rindā **Daļējas izgatavošanas signāls** iestatiet **Shēmas nosaukumu** uz **Vērtība**. Derīgās vērtības tiek rādītas nolaižamajā tabulā.
14. Noklikšķiniet uz **Tālāk**, lai nonāktu lapā **Aprīkojuma resursa ID konfigurācija**.
15. Šajā darbībā kartējiet IoT centrmezgla ziņojuma vērtības uz Supply Chain Management resursiem.

    1. Tabulā **Signāla datu vērtības** pievienojiet jaunu rindu un ievadiet **IoTInt.Machine1225.PartOut** kolonnā **Vērtība**. Vērtība **IoTInt.Machine1225.PartOut** tiek iegūta no IoT centrmezgla ziņojuma JSON **id** rekvizīta.
    2. Noklikšķiniet uz **Saglabāt**.
    3. Tabulā **Biznesa ieraksta kartēšana** klikšķiniet **Jauns**. Noklusējuma vērtība **Biznesa ieraksta veidam** tiek automātiski aizpildīta, un jums nav nepieciešams to mainīt.
    4. Kolonnā **Biznesa ieraksts** atlasiet Supply Chain Management iekārtas resursu, no kura tiek sūtīta šī signāla vērtība.
    5. Noklikšķiniet uz **Saglabāt**.
    6. Atkārtojiet šīs darbības, pievienojot jaunu biznesa ieraksta kartējumu **Machine1226**. Varat kartēt vairāku signālu datu vērtības vienam Supply Chain Management ierakstam.

16. Izmantojiet kolonnu **Atlasīts**, lai izvēlētos iekārtas, ko vēlaties apstrādāt. Nav jādefinē visas signāla vērtības un nav jāatlasa visas iekārtas.
17. Noklikšķiniet **Tālāk**, lai dotos uz lapu **Daļu ražošanas signāla konfigurācija**.
18. Tabulā **Signāla datu vērtības** pievienojiet rindu un iestatiet **Vērtību** uz **Patiess**. Vērtība **Patiess** tiek iegūta no IoT centrmezgla ziņojuma JSON **vērtības** rekvizīta. Scenārijam var pievienot tik daudz vērtību, cik nepieciešams.
19. Noklikšķiniet uz **Saglabāt**.
20. Noklikšķiniet **Tālāk**, lai dotos uz lapu **Aprīkojuma dīkstāves slieksnis**. Norādītās iekārtas ir iepriekš uz signālu vērtībām kartētās iekārtas. Šajā darbībā definējiet slieksni, lai noteiktu, vai iekārta darbojas. Piemēram, ja iestatāt slieksni uz 10, Supply Chain Management ģenerē paziņojumu, ja 10 minūtes no iekārtas netiek izvadīts neviens ziņojums.
21. Noklikšķiniet **Tālāk**, lai dotos uz lapu **Iespējot scenāriju**. Pārslēdziet slīdni, lai iespējotu scenāriju.
22. Noklikšķiniet uz **Pabeigt**.

Scenāriju iestatīšana ir pabeigta. IoT informācija automātiski sāks apstrādāt IoT centrmezgla ziņojumus.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju **Preces kvalitāte** Supply Chain Management

**Preces kvalitātes** scenārijs ģenerē paziņojumu, ja vienuma atribūts atrodas ārpus norādītā diapazona. Piemēram, sensors katra vienuma svaru varētu nosūtīt uz IoT centrmezglu. Paziņojums Supply Chain Management tiks ģenerēts, ja vienums būs pārāk smags vai pārāk viegls.

Scenārijam ir šādas atkarības:

+ Ražošanas pasūtījumam ir jādarbojas kartētā iekārtā un jāražo prece ar kartētu partijas atribūtu, lai tiktu parādīts brīdinājums.
+ Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē partijas atribūtu.
+ IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju **Ražošanas aizkaves** Supply Chain Management

**Ražošanas aizkaves** scenārijs ģenerē paziņojumu, ja ražošanas caurlaidspēja ir zemāka par sliekšņa vērtību. Šādā gadījumā **PartOut** signāls tiek nosūtīts uz IoT centrmezglu katram saražotajam krājumam. Supply Chain Management pasūtījuma aizkave tiek aprēķināta, pamatojoties uz to, cik ilgā laikā paredzēts izpildīt ražošanas pasūtījumu, cik krājumu ir jāražo, cik ilgi darbs tiek veikts un cik **PartOut** signālu tiek saņemts. Aizkavēšanas paziņojums tiks ģenerēts, ja **PartOut** signālu skaits darbam nokrītas zem paredzētās sliekšņa vērtības.

Scenārijam ir šādas atkarības:

+ Lai brīdinājums tiktu parādīts, ražošanas pasūtījumam ir jādarbojas kartētā iekārtā.
+ Uz IoT centrmezglu ar unikālu rekvizīta nosaukumu jānosūta signāls, kas apzīmē kartētās iekārtas izslēgšanas signālu.
+ IoT centrmezgla ziņojumā jābūt Unix milisekundes laikspiedola rekvizītam.

## <a name="how-to-disable-a-scenario"></a>Scenārija atspējošana

Lai atspējotu scenāriju, izpildiet tālāk aprakstītās darbības:

1. Supply Chain Management pārejiet uz **Ražošanas kontrole \> Iestatīšana \> IoT informācija \> Scenārija pārvaldība**.
2. Scenārijā noklikšķiniet uz **Konfigurēt**.
3. Noklikšķiniet **Tālāk**, lai nokļūtu pēdējā vedņa cilnē.
4. Pārslēdziet slīdni, lai atspējotu scenāriju.
