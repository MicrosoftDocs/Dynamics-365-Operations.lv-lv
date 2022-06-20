---
title: Dīkstāves uzturēšanas aktivitātes
description: Šajā rakstā skaidrots, kā tiek izmantots uzturēšana pēc dīkstāves laika, lai gūtu pārskatu par noslodzi, kas nepieciešama noteiktu pamatlīdzekļu uzturēšanas darbu veikšanai noteiktā periodā.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75e30c8b2d74cc2f1ca538b64e5fc801f9ca130a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897695"
---
# <a name="maintenance-downtime-activities"></a>Dīkstāves uzturēšanas aktivitātes

[!include [banner](../../includes/banner.md)]

Dīkstāve uzturēšanas dēļ tiek izmantota, lai iegūtu pārskatu par noslodzi, kas ir nepieciešama, lai veiktu uzturēšanas darbus konkrētos līdzekļos konkrētā periodā. Piemēram, jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrāciju 10. ražošanas līnijai 29-A ražošanas zālē ražošanas objektā 02. Dīkstāves uzturēšanas dēļ reģistrācijai ir sākuma un beigu laiks, kas norāda uz periodu, kurā līdzekļi, kas ir saistīti ar uzturēšanas apturēšanu, nav pieejami ražošanai.

**Dīkstāves uzturēšanas dēļ darbības** ir pārskats par uzturēšanas grafika rindām un darba pasūtījuma uzturēšanas darbiem saistītos līdzekļos konkrētā periodā. Visām rindām, kas saistītas ar darba pasūtījuma uzturēšanas darbiem, ir paredzamais sākuma datums uzturēšanas pārtraukuma periodā. Jūs varat izvilkt noderīgu informāciju un veikt pielāgojumus plānotiem uzturēšanas darbiem:

- Iegūstiet pārskatu par nepieciešamajiem ražošanas aprīkojuma (līdzekļu) izslēgšanas periodiem.  
- Iegūstiet pārskatu par plānoto uzturēšanu (stundas), grupētu pēc prasmēm (atbildīgo uzturēšanas speciālistu grupām vai uzturēšanas speciālistiem), piemēram, elektriķu, metalurgu vai citu uzturēšanas grupu noslodzi, kuras ir nepieciešamas, lai veiktu plānotos uzturēšanas darbus.  
- Veiciet pielāgojumus uzturēšanas grafika rindām vai darba pasūtījuma uzturēšanas darbiem, kas saistīti ar līdzekļiem, piemēram, mainiet paredzamo sākuma un beigu datumu rindā vai atlasiet citus uzturēšanas speciālistus, lai optimizētu darbplūsmas uzturēšanas speciālistiem un uzturēšanas speciālistu grupām.

Kad dīkstāves uzturēšanas dēļ reģistrācijā ir atlasīti līdzekļi, visas atvērtās uzturēšanas grafika rindas un darba pasūtījuma uzturēšanas darbi, kas attiecas uz aktīviem darba pasūtījumiem, tiek iekļauti dīkstāves uzturēšanas dēļ reģistrācijā.

## <a name="maintenance-downtime-activities"></a>Dīkstāves uzturēšanas dēļ aktivitātes

Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Dīkstāves uzturēšanas dēļ darbības** > **Visas uzturēšanas dīkstāves dēļ darbības**, lai atvērtu sarakstu ar visām dīkstāves uzturēšanas dēļ darbībām un redzētu informāciju, kas saistīta ar darbībām. Noklikšķiniet uz saites kolonnā **Dīkstāves uzturēšanas dēļ darbības**, lai atvērtu detalizētu skatu. Nākamajā attēlā ir parādīts saraksta **Dīkstāves uzturēšanas dēļ aktivitātes** piemērs.

![1. attēls.](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Izveidojiet dīkstāves uzturēšanas dēļ aktivitāti

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Dīkstāves uzturēšanas dēļ darbības** > **Visas dīkstāves uzturēšanas dēļ darbības** vai **Aktīvās uzturēšanas dīkstāves dēļ darbības**.

2. Klikšķiniet **Jauns**.

3. Laukā **Dīkstāves uzturēšanas dēļ darbības** ievadiet ID un laukā **Nosaukums** ievadiet nosaukumu.

4. Ievadiet uzturēšanas pārtraukuma periodu laikos **Sākuma datums/laiks** un **Beigu datums/laiks**.

5. Kopsavilkuma cilnē **Dīkstāves uzturēšanas dēļ darbību līdzekļi** noklikšķiniet **Pievienot rindu**, lai pa vienam dīkstāves uzturēšanas dēļ pievienotu līdzekļus.

6. Kad visi līdzekļi ir pievienoti, noklikšķiniet uz **Saglabāt**. Nākamajā attēlā ir parādīts dīkstāves uzturēšanas dēļ aktivitātes ar saistītajiem līdzekļiem un uzturēšanas darbiem piemērs.

7. Darba pasūtījuma uzturēšanas darbi un atvērtas uzturēšanas grafika rindas, kas ir saistītas ar atlasītiem līdzekļiem, tiek uzrādītas kopsavilkuma cilnēs **Darba pasūtījuma uzturēšanas gala darbi** un **Uzturēšanas grafika rindas**. Kopsavilkuma cilnē **Vispārīgi** > grupā **Darba pasūtījumi** > laukā **Uzturēšanas prognozes stundas** un kopsavilkuma cilnē **Vispārīgi** > grupā **Uzturēšanas grafiks** > laukā **Uzturēšanas prognozes stundas** ir redzams kopējo stundu skaits, kuras prognozētas darba pasūtījuma uzturēšanas darbiem un uzturēšanas grafika rindām.

Nākamajā attēlā ir parādīts detalizētā skata **Dīkstāves uzturēšanas dēļ aktivitātes** piemērs.

![2. attēls.](media/20-preventive-maintenance.png)

>[!NOTE]
>Darba pasūtījuma uzturēšanas darbi un uzturēšanas grafika rindas, kas saistītas ar atlasītiem līdzekļiem, tiek automātiski atjauninātas, ja tiek izveidoti jauni darba pasūtījumi vai uzturēšanas grafika rindas pēc tam, kad izveidojat dīkstāves uzturēšanas dēļ darbību. Piemēram, ja ieplānojat uzturēšanas plānus vai uzturēšanas ciklus saistītos līdzekļos divas dienas pēc dīkstāves uzturēšanas dēļ darbības izveides, jaunās uzturēšanas grafika rindas tiek automātiski pievienotas dīkstāves uzturēšanas dēļ darbībai.

8. **Visas dīkstāves uzturēšanas dēļ darbības** > **Dīkstāves uzturēšanas dēļ darbības** > sarakstā atlasiet dīkstāves uzturēšanas dēļ darbību un noklikšķiniet uz **Noslodze**, lai atvērtu dialoglodziņu **Aprēķināt noslodzi**. Izmantojiet šo dialogu, lai iegūtu pārskatu par noslodzi, piemēram, datumiem, līdzekļiem, līdzekļu tipiem un uzturēšanas darbu tipiem. Ņemiet vērā, ka datumi, kas uzrādīti dialogā ir sākuma un beigu datumi, kas atlasīti laukā **Dīkstāves uzturēšanas dēļ darbības**. Aprēķins ietver līdzekļus, kas saistīti ar dīkstāves uzturēšanas dēļ darbību.

9. Dialogā **Aprēķināt noslodzi** rediģējiet sākuma un beigu laikus, ja nepieciešams, un izvēlieties, vai vēlaties aprēķinā iekļaut darba pasūtījumus un uzturēšanas grafikus. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētu vēlaties noslodzes aprēķinu attiecībā uz funkcionālo novietojumu. Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visi līdzekļi funkcionālajam novietojumam, kuri ir atlasīti dīkstāves uzturēšanas dēļ darbībai, tiks uzrādīti augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas noslodzes rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

10. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu. Kopējais stundu skaits ir uzrādīts pārskatā **Noslodze**. Cilnē **Noslodze** darbību rūts grupās **Grupēt pēc...** noklikšķiniet uz attiecīgajām pogām, lai iegūtu detalizētāku pārskatu par prognozēto stundu piešķiršanu. Nākamajā attēlā ir redzami **Noslodzes** aprēķina rezultāti.

![3. attēls.](media/21-preventive-maintenance.png)

11. Lai iegūtu pārskatu par noslodzi, ja vēlaties veikt darba pasūtījuma uzturēšanas darbu vai uzturēšanas grafika rindu pielāgojumus, atgriezieties detalizētajā skatā **Dīkstāves uzturēšanas dēļ darbības** un atlasiet rindas, kuras vēlaties pielāgot kopsavilkuma cilnēs **Darba pasūtījumu uzturēšanas gala darbi** un **Uzturēšanas grafika rindas**.

12. Noklikšķiniet uz pogas **Pielāgot** un atjauniniet paredzamos sākuma/beigu datumus, servisa līmeni vai atbildīgos uzturēšanas speciālistus atlasītiem darba pasūtījuma uzturēšanas darbiem vai uzturēšanas grafika rindām.

13. Kad esat veikuši nepieciešamos pielāgojumus, noklikšķiniet uz **Labi**. 

>[!NOTE]
>Darba pasūtījuma uzturēšanas darbi un uzturēšanas grafika rindas, kuras nav ietvertas dīkstāves uzturēšanas dēļ periodā pēc tam, kad veicāt pielāgojumus, tiek automātiski dzēstas no **Dīkstāves uzturēšanas dēļ darbībām**.

14. **Visas dīkstāves uzturēšanas dēļ darbības** > **Dīkstāves uzturēšanas dēļ darbības** > sarakstā atlasiet dīkstāves uzturēšanas dēļ darbību un noklikšķiniet uz **Vienuma prognoze**, lai atvērtu dialogu **Aprēķināt vienuma prognozi**. Izmantojiet šo dialogu, lai aprēķinātu prognozes vienumiem (rezerves daļām vai citiem nepieciešamiem vienumiem) un grupētu tos, lai iegūtu pārskatu, piemēram, pēc datuma, līdzekļa, līdzekļa tipa un uzturēšanas darba tipa. Ņemiet vērā, ka datumi, kas uzrādīti dialogā ir sākuma un beigu datumi, kas atlasīti laukā **Dīkstāves uzturēšanas dēļ darbības**. Šis aprēķins ietver rezerves daļas un vienumus, kas saistīti ar līdzekļiem, kas ir atlasīti dīkstāves uzturēšanas dēļ darbībā.

15. Dialogā **Aprēķināt vienuma prognozi** rediģējiet sākuma un beigu laikus, ja nepieciešams, un izvēlieties, vai vēlaties aprēķinā iekļaut darba pasūtījumus un uzturēšanas grafikus. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētu vēlaties noslodzes aprēķinu attiecībā uz funkcionālo novietojumu. Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visi līdzekļi funkcionālajam novietojumam, kuri ir atlasīti dīkstāves uzturēšanas dēļ darbībai, tiks uzrādīti augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas noslodzes rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

16. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu. Kopējais vienuma prognožu skaits ir uzrādīts pārskatā  **Vienuma prognoze**. Cilnē **Vienuma prognoze** > darbību rūts grupās **Grupēt pēc...** noklikšķiniet uz attiecīgajām pogām, lai iegūtu detalizētāku pārskatu par prognozēto vienumu piešķiršanu. Nākamajā attēlā ir parādīti **Vienuma prognozes** aprēķina rezultāti.

![4. attēls.](media/22-preventive-maintenance.png)

- Jūs varat nokopēt līdzekļus no vienas dīkstāves uzturēšanas dēļ darbības citā. In **Visas dīkstāves uzturēšanas dēļ darbības** atlasiet pogu **Kopēt dīkstāves uzturēšanas dēļ darbības** un veiciet atlasi laukos **Dīkstāves uzturēšanas dēļ darbības no** un **Dīkstāves uzturēšanas dēļ darbības līdz** un noklikšķiniet uz **Labi**.
- Laukā **Visas dīkstāves uzturēšanas dēļ darbības** noklikšķiniet uz pogas **Uzturēšanas grafika rindas** vai pogas **Aktīvi darba pasūtījumi**, lai atvērtu saistītos sarakstus un skatītu rindas, kas ir saistītas ar atlasīto dīkstāves uzturēšanas dēļ darbību.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]