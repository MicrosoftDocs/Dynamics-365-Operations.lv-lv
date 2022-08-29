---
title: IoT informācijas scenārija iestatīšana
description: Šajā rakstā skaidrots, kā konfigurēt scenārijus Iot Intelligence programmā Microsoft Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2f097f33abb55dd69d4a38a9a7b0b2e9bdfbaea1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227809"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT informācijas scenārija iestatīšana

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šajā rakstā skaidrots, kā konfigurēt scenārijus Iot Intelligence programmā Microsoft Dynamics 365 Supply Chain Management. <!-- KFM: Hide setup info for now: Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md). -->

Šajā rakstā jūs konfigurēsiet aprīkojuma **dīkstāves** scenāriju, lai piegādes ķēdes pārvaldībā tiek ģenerēts paziņojums, kad iekārta nolaižas. Rakstā ir arī **parādīts**, kā konfigurēt produktu kvalitātes scenāriju, lai tiek ģenerēts paziņojums, ja krājuma atribūts ir ārpus norādītā diapazona, un kā konfigurēt Ražošanas aizkaves scenāriju, **tādējādi paziņojums tiek ģenerēts**, ja ražošanas caurlaide ir zem sliekšņa vērtības.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju Aprīkojuma dīkstāve Supply Chain Management

Scenārijs **Aprīkojuma dīkstāve** kartē iekārtas brīdinājuma sliekšņa **PartOut** signālu. Iekārta tiek uzraudzīta tikai tad, ja tā ir izvēlēta scenārijam un, kad tā ir iestatīta kā **Darbībā esoša** risinājumā Supply Chain Management. Ja laiks, kas pagājis kopš pēdējā saņemtā **PartOut** signāla no iekārtas pārsniedz brīdinājuma robežvērtību, tiek parādīts paziņojums **Iekārta dīkstāvē**. Ja iekārta joprojām darbojas, tiek parādīts paziņojums **Iekārta darbojas**, kad tiek saņemts nākamais **PartOut** signāls. Ja iekārta pārstāj darboties uz 30 minutēm, tiek parādīts jauns paziņojums **Iekārta dīkstāvē**.

Scenārijam **Aprīkojuma dīkstāve** ir šādas atkarības:

+ Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā.
+ Signāls, kas apzīmē kartētu iekārtas **PartOut** signālu ir jānosūta uz IoT centrmezglu un ir jāiekļauj unikāls rekvizīta nosaukums.
+ UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta milisekundēs (ms), ir jāatrodas Azure IoT Hub ziņojumā.

Lai konfigurētu scenāriju, rīkojieties šādi.

1. Pierakstieties Supply Chain Management.
2. Iespējojiet IoT informācijas līdzekļa karodziņu. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurējiet rādītājus. Papildinformāciju skatiet [Rādītāju konfigurēšana](iot-metrics-setup.md#configure-metrics).
4. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> IoT informācija \> Scenāriju pārvaldība**.
6. Lai atvērtu konfigurācijas vedni, elementā **Aprīkojuma dīkstāve** atlasiet **Konfigurēt**.

   Pirmā lapa vednī ir lapa **Aprīkojuma sensora shēmas definīcija**. Šajā lapā jūsu mērķis ir iestatīt shēmu risinājumā Supply Chain Management, lai tā atbilstu IoT Hub ziņojuma JavaScript Object Notation (JSON) formātam. Var tikt definētas vairākas ziņojumu shēmas. Papildinformāciju skatiet [Shēmas formāti IoT Hub ziņojumiem](iot-schema-format.md). Šajā piemērā ziņojuma lietderīgā slodze satur ziņojumu paketi ar šādu formātu.

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

7. Pievienojiet rindu tabulai un iestatiet šādas vērtības:

    1. Iestatiet lauku **Shēmas nosaukums** uz **ID**.
    2. Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/id**.
    3. Iestatiet lauku **Apraksts** uz **Ziņojuma ID**.

8. Pievienojiet vēl vienu rindu tabulai un iestatiet šādas vērtības:

    1. Iestatiet lauku **Shēmas nosaukums** uz **Laikspiedols**.
    2. Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/timestamp**.
    3. Iestatiet lauku **Apraksts** uz **Ziņojuma laikspiedols**.

9. Pievienojiet vēl vienu rindu tabulai un iestatiet šādas vērtības:

    1. Iestatiet lauku **Shēmas nosaukums** uz **Vērtība**.
    2. Iestatiet lauku **Shēmas ceļš** uz **/payload\[\*\]/value**.
    3. Iestatiet lauku **Apraksts** uz **Ziņojuma vērtība**.

    > [!NOTE]
    > Nav jādefinē visi ziņojuma rekvizīti. Nosakiet tikai tos rekvizītus, kas ir nepieciešami. Iepriekšējās darbībās neesat izveidojis rindu **Saknes laikspiedols**. Ceļš laukam **Saknes laikspiedols** būtu **/timestamp**.

10. Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma sensora shēmas karte**.
11. Rindā **Aprīkojuma resursa ID** laukā **Shēmas nosaukums** atlasiet **ID**.
12. Rindā **UTC laiks** laukā **Shēmas nosaukums** atlasiet **Laikspiedols**.
13. Rindā **Daļējas izgatavošanas signāls** laukā **Shēmas nosaukums** atlasiet **Vērtība**.
14. Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma resursa ID konfigurācija**.
15. Veiciet tālāk norādītās darbības, lai kartētu vērtības IoT Hub ziņojumā uz Supply Chain Management resursiem.

    1. Tabulā **Signāla datu vērtības** pievienojiet jaunu rindu. Laukā **Vērtība** ievadiet **IoTInt.Machine1225.PartOut**. Šī vērtība tiek iegūta no IoT Hub ziņojuma JSON **id** rekvizīta.
    2. Atlasiet **Saglabāt**.
    3. Tabulā **Biznesa ieraksta kartēšana** atlasiet **Jauns**. Noklusējuma vērtība laukam **Biznesa ieraksta veids** tiek automātiski aizpildīta, un jums nav nepieciešams to mainīt.
    4. Laukā **Biznesa ieraksts** atlasiet Supply Chain Management iekārtas resursu, no kura tiek sūtīta šī signāla vērtība.
    5. Atlasiet **Saglabāt**.
    6. Atkārtojiet šīs darbības, lai pievienotu jaunu biznesa ieraksta kartējumu **Machine1226**. Varat kartēt vairāku signālu datu vērtības vienam Supply Chain Management ierakstam.

16. Izmantojiet kolonnu **Atlasīts**, lai atlasītu iekārtas, ko vēlaties apstrādāt. Nav jādefinē visas signāla vērtības, un nav jāatlasa visas iekārtas.
17. Atlasiet **Tālāk**, lai dotos uz lapu **Daļu ražošanas signāla konfigurācija**.
18. Tabulā **Signāla datu vērtības** pievienojiet rindu un iestatiet lauku **Vērtība** uz **Patiess**. Šī vērtība tiek iegūta no IoT Hub ziņojuma JSON **vertība** rekvizīta. Scenārijam var pievienot tik daudz vērtību, cik nepieciešams.
19. Atlasiet **Saglabāt**.
20. Atlasiet **Tālāk**, lai dotos uz lapu **Aprīkojuma dīkstāves slieksnis**. Norādītās iekārtas ir iekārtas, kas iepriekš tika kartētas uz signāla vērtībām. Šajā lapā definējiet slieksni, lai noteiktu, vai iekārta darbojas. Piemēram, ja iestatāt slieksni uz **10**, Supply Chain Management ģenerēs paziņojumu, ja 10 minūtes no iekārtas netiek saņemts neviens **PartOut** signāls.
21. Atlasiet **Tālāk**, lai dotos uz lapu **Iespējot scenāriju**. Iestatiet opciju, lai iespējotu scenāriju.
22. Atl. **Pabeigt**.

Scenāriju iestatīšana tagad ir pabeigta. IoT informācija automātiski sāks apstrādāt IoT centrmezgla ziņojumus.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju Preces kvalitāte Supply Chain Management

**Preces kvalitātes** scenārijs ģenerē paziņojumu, ja vienuma atribūts atrodas ārpus norādītā diapazona. Piemēram, sensors katra vienuma svaru nosūta uz IoT centrmezglu. Ja vienums ir pārāk smags vai pārāk viegls, tiek ģenerēts paziņojums risinājumā Supply Chain Management.

Scenārijam **Preču kvalitāte** ir šādas atkarības:

+ Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā un ražo preci ar kartētu partijas atribūtu.
+ Signāls, kas apzīmē partijas atribūtu, ir jānosūta uz IoT Hub, un ir jāiekļauj unikāls rekvizīta nosaukums.
+ UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta ms, ir jāatrodas IoT Hub ziņojumā.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurēt scenāriju Ražošanas aizkaves Supply Chain Management

**Ražošanas aizkaves** scenārijs ģenerē paziņojumu, ja ražošanas caurlaidspēja ir zemāka par sliekšņa vērtību. Šādā gadījumā **PartOut** signāls tiek nosūtīts uz IoT Hub katrai ražotajai precei. Risinājumā Supply Chain Management pasūtījuma aizkave tiek aprēķināta, ņemot vērā laiku, kad ražošanas pasūtījums tiek plānots izpildei, krājumu skaitu, kas jāsagatavo, laiku, kad darbs ir palaists, un **PartOut** saņemto signālu skaitu. Aizkavēšanas paziņojums tiek ģenerēts, ja **PartOut** signālu skaits darbam nokrītas zem sliekšņa vērtības.

Scenārijam **Ražošanas kavējumi** ir šādas atkarības:

+ Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā.
+ Signāls, kas apzīmē kartētu iekārtas **PartOut** signālu ir jānosūta uz Azure IoT centrmezglu un ir jāiekļauj unikāls rekvizīta nosaukums.
+ UNIX rekvizīts **laikspiedols**, kur vērtība ir izteikta ms, ir jāatrodas IoT Hub ziņojumā.

## <a name="disable-a-scenario"></a>Scenārija atspējošana

Lai atspējotu scenāriju, izpildiet tālāk aprakstītās darbības.

1. Risinājumā Supply Chain Management dodieties uz **Ražošanas kontrole \> Iestatīšana \> IoT informācija \> Scenārija pārvaldība**.
2. Scenārija elementā atlasiet **Konfigurēt**.
3. Atlasiet **Tālāk**, lai dotos uz pēdējo vedņa lapu.
4. Iestatiet opciju, lai atspējotu scenāriju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]