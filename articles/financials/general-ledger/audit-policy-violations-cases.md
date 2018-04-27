---
title: "Audita ierobežojuma nosacījumu pārkāpumi un gadījumi"
description: "Rakstā ir paskaidrots, kā no audita ierobežojumu nosacījumu pārkāpumiem tiek ģenerēti audita gadījumi. Tajā ir iekļauta arī informācija par dažādiem veidiem, kā audita ierobežojumi izmanto dokumentu atlases datumu diapazonu."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2376a1d6e86eba9f5021cc08dcfaea52f131a3d7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-violations-and-cases"></a>Audita ierobežojuma nosacījumu pārkāpumi un gadījumi

[!INCLUDE [banner](../includes/banner.md)]

Rakstā ir paskaidrots, kā no audita ierobežojumu nosacījumu pārkāpumiem tiek ģenerēti audita gadījumi. Tajā ir iekļauta arī informācija par dažādiem veidiem, kā audita ierobežojumi izmanto dokumentu atlases datumu diapazonu.

<a name="how-audit-cases-are-generated"></a>Audita gadījumu ģenerēšana
-----------------------------

Audita politikas tiek izmantotas, lai identificētu izdevumu pārskatus, pirkšanas pasūtījumus un kreditoru rēķinus, kas neatbilst biznesa kārtulām, ko definē un konfigurē atbilstoši audita ierobežojuma nosacījumiem. 

Audita ierobežojumi tiek palaisti pakešveida režīmā. Palaižot audita ierobežojumu, visi ierobežojuma nosacījumi, kas ir ietverti konkrētajā ierobežojumā, tiek palaisti vienlaicīgi.

Visi ierobežojuma nosacījumi novērtē dokumentu kopu. Ierobežojuma nosacījums atlasa dokumentus, kas atrodas dokumentu atlases datumu diapazonā un atbilst norādītajiem kritērijiem. Piemēram, viens ierobežojuma nosacījums var atlasīt izdevumu pārskatus, kur ir ietvertas maltītes, kuru vērtība pārsniedz 50,00. Cits ierobežojuma nosacījums var atlasīt kreditora rēķinus, kas ir jāsamaksā noteiktam kreditoram. Visiem dokumentiem, kas kopā tiek atlasīti, tiek ģenerēts pārkāpums. Šis pārkāpums ir ieraksts par to, ka noteikts dokuments, piemēram, rēķins Nr. 12345, neatbilst ierobežojuma nosacījumam. 

Vairāki ierobežojuma nosacījumu ieraksti tiek grupēti un saistīti ar audita gadījumiem. Pēc noklusējuma katra audita ierobežojuma gadījumi tiek grupēti pēc audita ierobežojuma nosacījuma. Varat arī atlasīt citu grupēšanas kritēriju, izmantojot lapu **Gadījumu grupēšanas kritēriji**. Piemēram, izdevumu virsrakstus varat grupēt pēc projekta ID, savukārt kreditora rēķinus — pēc kreditora konta. Šajā gadījumā visi izdevumu virsraksta pārkāpumi, kam ir vienāds projekta ID, tiks grupēti vienā gadījumā, savukārt visi kreditora rēķini, kuriem ir vienāds kreditora konts, tiks grupēti tajā pašā gadījumā. 

> [!NOTE]
> Audita ierobežojuma nosacījumiem, kuru pamatā ir vaicājuma tips **Dublikāts**, pārkāpumi netiek grupēti pēc ierobežojuma nosacījuma vai pēc kritērijiem, kas norādīti lapā **Gadījumu grupēšanas kritēriji**. Tā vietā tie tiek grupēti pēc noklusējuma audita ierobežojuma nosacījumu kritērijiem. Piemēram, ja ierobežojuma nosacījums novērtē, vai izdevumu pārskatos ir izdevumu dublikāti ar vienādu summu, tirgotāja ID un datumu, visi izdevumi, kam šajos laukos ir vienādas vērtības, būs viens gadījums. Visis izdevumi, kam ir atšķirīgas vērtības, būs atsevišķs gadījums.

Pēc audita gadījumu ģenerēšanas tie tiek apstrādāti, izmantojot standarta lietu pārvaldības procesus.

## <a name="document-selection-date-ranges"></a>Dokumentu atlases datumu diapazoni
Palaižot audita ierobežojumu, visi ierobežojuma nosacījumi atlasa norādītā veida dokumentu ar datumu, kas atrodas dokumentu atlases datumu diapazonā. Dokumentu atlases datumu diapazons tiek norādīts lapā **Papildu opcijas**. Daudziem dokumentiem ir piesaistīti vairāki datumi. Datuma lauks, ko izmanto audita ierobežojuma nosacījums, tiek norādīts lapā **Ierobežojuma nosacījumu tips**.

Tālāk ir minēti daži citi veidi, kā audita ierobežojums izmanto dokumentu atlases datumu diapazonu.

-   Ierobežojums izmanto katra ierobežojuma nosacījuma versiju, kas ir spēkā dokumenta atlases datumu diapazona pēdējā dienā. Visu ierobežojuma nosacījumu spēkā stāšanās datumus varat skatīt saraksta lapā **Audita ierobežojumi**.
-   Ierobežojums izmanto organizācijas mezglus, kas ir saistīti ar ierobežojumu, pēdējā dokumentu atlases datumu diapazona dienā. Saraksta lapā **Audita ierobežojumi** tiek rādīti tikai tie organizācijas mezgli, kas pašlaik ir saistīti ar ierobežojumu.
-   Saistībā ar ierobežojuma nosacījumiem, kuru pamatā ir vaicājuma veids **Meklēšana sarakstā**, ierobežojums novērtē to uzraudzīto elementu dokumentus, kas ir spēkā dokumentu atlases datumu diapazona pēdējā dienā.


Plašāku informāciju skatiet rakstā [Audita ierobežojuma nosacījumi](audit-policy-rules.md)




