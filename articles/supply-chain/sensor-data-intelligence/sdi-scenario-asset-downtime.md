---
title: Līdzekļa dīkstāves scenārijs
description: Šajā rakstā ir aprakstīts līdzekļu dīkstāves scenārijs, kas ļauj jums izmantot sensora datus, lai pārraudzītu pamatlīdzekļu pieejamību.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689434"
---
# <a name="the-asset-downtime-scenario"></a>Līdzekļa dīkstāves scenārijs

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Līdzekļa dīkstāves scenārijs ģenerē uzturēšanas dīkstāves ierakstu, ja no datora nav saņemts neviens vērtējums definētā laika sliekšņa robežās kopš pēdējā brīdinājuma saņemšanas. Scenārijam ir nepieciešams, lai dators būtu piemērots ar sensoru, kas periodiski sūta signālu jūsu Azure IoT pārkraušanas centram datora darbības laikā, bet nesūta signālu, kad dators nedarbojas.

## <a name="set-up-the-asset-downtime-scenario"></a>Iestatīt līdzekļa dīkstāves scenāriju

Ievērojiet šos soļus, lai iestatītu *līdzekļu dīkstāves* scenāriju Piegādes ķēžu pārvaldībā.

1. Ejiet uz **Līdzekļu pārvaldības \> iestatīšanas \> sensora datu \> inteliģences** scenārijiem, lai atvērtu **lapu Scenāriji**.
2. Lodziņā Līdzekļu **dīkstāves** scenārijā atlasiet **Konfigurēt**, lai atvērtu šī scenārija iestatīšanas vedni.
3. **Lapā Sensors** atlasiet **Jauns**, lai režģim pievienotu sensoru. Pēc tam iestatiet tai sekojošos laukus:

    - **Sensora ID** – ievadiet jūsu lietotā sensora ID. (Ja izmantojat Pārkaru PI Azure IoT tiešsaistes simulatoru un esat to iestatījis kā aprakstīts [Iestatiet simulētu sensoru testēšanai](sdi-set-up-simulated-sensor.md), ievadiet *AssetDownTime*.)
    - **Sensora** apraksts – ievadiet sensora aprakstu.

4. Atkārtojiet iepriekšējo soli ar katru papildu sensoru, ko vēlaties pievienot tagad. Jebkurā laikā varat atgriezties un pievienot vairāk sensoru.
5. Atlasiet **Nākamais**.
6. Biznesa ierakstu **kartēšanas lapā** sadaļā **Sensors** atlasiet ierakstu vienam no tikko pievienotiem sensoriem.
7. Sadaļā Biznesa **ierakstu kartēšana** atlasiet **Jauns**, lai režģim pievienotu rindu.
8. Jaunajā rindā iestatiet biznesa ieraksta lauku **resursam**, kuru izmantojat, lai pārraudzītu atlasīto sensoru. (Ja izmantojat demonstrācijas datus, atlasiet *AK-101, Gaisa kondicionēšana 1. rindai*.)
9. Atlasiet **Nākamais**.
10. Līdzekļu dīkstāves **sliekšņa** lapā definējiet, cik ilgi pēc pēdējā signāla sistēmai jāgaida pirms līdzekļa dīkstāves paziņojuma nosūtīšanas. Slieksni var definēt divējādi:

    - **Noklusējuma slieksnis (minūtēs)** – iestatiet šo lauku, lai definētu noklusējuma slieksni. Šī vērtība attiecas uz visiem resursiem, kur paziņojuma sliekšņa **(minūšu)** lauks ir iestatīts uz divām minūtēm vai mazāku. Minimālā vērtība ir *2* (minūtes).
    - **Slieksnis, lai noteiktu iekārtu, kura neatbild (minūtēs)** — katram resursam režģī, kur nevēlaties izmantot noklusējuma slieksni, ievadiet šajā laukā ignorēšanas vērtību. Resursi, kas iestatīti divu minūšu vai mazāk sliekšņa izmantošanai, izmantos noklusējuma **sliekšņa (minūšu)** iestatījumu.
11. Atlasiet **Nākamais**.
12. Režģī **aktivizējiet sensoru** lapu, atlasiet iestatāmo sensoru un pēc tam atlasiet **Aktivizēt**. Katram aktivizētam sensoram režģī aktīvā kolonnā parādās **atzīme**.
13. Atl. **Pabeigt**.

## <a name="work-with-the-asset-downtime-scenario"></a>Strādāt ar līdzekļu dīkstāves scenāriju

Ja no pamatlīdzekļa, kas ir scenārija konfigurācijā definētajā sliekšņā, nav saņemts sensora signālus, sistēma šim pamatlīdzeklim izveidos uzturēšanas dīkstāves ierakstu. Pārvaldniekiem periodiski jāpārskata dīkstāves ieraksti (piemēram, vienreiz katrā darba maiņā) un jālieto atbilstoši pamatojuma kodi un beigu laiki katrai dīkstāves reģistrācijai. Sekojiet šiem soļiem, lai skatītu līdzekļa dīkstāves laika ierakstus:

1. Pārejiet **uz sadaļu > Pamatlīdzekļi > visi pamatlīdzekļi**.
2. Atrodiet un atlasiet līdzekli, kuru vēlaties pārbaudīt. (Ja izmantojat demonstrācijas datus, atlasiet *AK-101*.)
3. Darbību rūtī **atveriet** **cilni** Pamatlīdzeklis un no grupas Darba pasūtījums atlasiet Uzturēšana, dīkstāves laiku, **lai** atvērtu lapu atlasītā līdzekļa uzturēšanas dīkstāves ierakstiem.
