---
title: "Pamatlīdzekļu atjaunošanas pārskats"
description: "Šajā tēmā izskaidrots, kā izmantot pārskatu Pamatlīdzekļu atjaunošana."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 16f7c199fb4c9905c465e5d4596d3eaa90104b83
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Pamatlīdzekļu atjaunošanas pārskats

[!include [banner](../includes/banner.md)]

Pārskats **Pamatlīdzekļu atjaunošana** viegli lasāmā Microsoft Excel formātā nodrošina detalizētus pamatlīdzekļu datus, kas jums nepieciešami perioda slēgšanai, finanšu pārskatiem un nodokļu pārskatiem. Šajā pārskatā ietvertas pamatlīdzekļu sākuma un beigu bilances kopā ar perioda novērtēšanas kustībām un visiem perioda laikā notikušajiem jaunu līdzekļu iegādes un izslēgšanas gadījumiem. Dati tiek sniegti par atsevišķiem pamatlīdzekļiem, un tiek arī apkopotas pamatlīdzekļu grupu un juridisko personu vērtības.

Pārskatā **Pamatlīdzekļu atjaunošana** izmantota elektronisko pārskatu (ER) platforma. Pirms pārskata palaišanas no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS) ir jāimportē pamatlīdzekļu modeļu un pamatlīdzekļu atjaunošanas konfigurācijas. Norādījumus skatiet sadaļā [Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Šis pārskats ir pieejams risinājumā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 vai kā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada jūlija) labojumfails. Vidēs, kurās ir 2017. gada jūlija laidiens, ir jālieto trīs labojumfaili.

- **KB 4041754:** elektronisko pārskatu (ER) konfigurāciju nevar lejupielādēt no LCS, jo tā neattiecas uz pašreizējo programmas versiju pēc platformas atjauninājumu pakotnes lietošanas
- **KB 4056107:** elektronisko pārskatu (GER) 5. kumulatīvais atjauninājums
- **KB 4056353:** pamatlīdzekļu pārskats un piezīmju pārskati neatbilst GAAP un IFRS prasībām

Tālāk esošajā tabulā ir aprakstīti pārskatā pieejamie lauki.


|                    Lauks                    |                                                                                                                                apraksts                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Bilance: sākuma              |                                                                                           Pamatlīdzekļa atlikusī vērtība kopš pārskatā norādītā “no” datuma.                                                                                           |
|              Bilance: slēguma              |                                                                                            Pamatlīdzekļa atlikusī vērtība kopš pārskatā norādītā “līdz” datuma.                                                                                            |
|         Iegāde: sākuma vērtība         |                                                 Visu veidu <strong>Iegāde</strong> un <strong>Iegādes korekcija</strong> transakciju summa līdz pārskatā norādītajam “no” datumam.                                                  |
|      Iegāde: iegādes periodā      |                                                 Visu veidu <strong>Iegāde</strong> un <strong>Iegādes korekcija</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                                                  |
|       Iegāde: izslēgšana periodā        |                                                                        Visu to iegādes atsaukumu summa, kas tika iegrāmatoti un kam bija izslēgšanas transakcija pārskata datumu diapazonā.                                                                        |
|         Iegāde: beigu vērtība         |                                                  Visu veidu <strong>Iegāde</strong> un <strong>Iegādes korekcija</strong> transakciju summa līdz pārskatā norādītajam “līdz” datumam.                                                   |
|        Nolietojums: sākuma vērtība         | Visu veidu <strong>Nolietojums</strong>, <strong>Nolietojuma korekcija</strong>, <strong>Speciālā nolietojuma atļautais daudzums</strong> un <strong>Ārkārtas nolietojums</strong> transakciju summa līdz pārskatā norādītajam “no” datumam. |
|     Nolietojums: nolietojumi periodā     |                         Visu veidu <strong>Nolietojums</strong>, <strong>Nolietojuma korekcija</strong> un <strong>Ārkārtas nolietojums</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                          |
| Nolietojums: speciālie nolietojumi periodā |                                                              Visu tipa <strong>Speciālā nolietojuma atļautais daudzums</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                                                               |
|       Nolietojums: izslēgšana periodā       |                                                                       Visu to nolietojumu atsaukumu summa, kas tika iegrāmatoti un kam bija izslēgšanas transakcija pārskata datumu diapazonā.                                                                        |
|        Nolietojums: beigu vērtība         |  Visu veidu <strong>Nolietojums</strong>, <strong>Nolietojuma korekcija</strong>, <strong>Speciālā nolietojuma atļautais daudzums</strong> un <strong>Ārkārtas nolietojums</strong> transakciju summa līdz pārskatā norādītajam “līdz” datumam.  |
|    Vērtības palielināšana/vērtības samazināšana: sākuma vērtība     |                              Visu veidu <strong>Vērtības palielināšana</strong>, <strong>Vērtības samazināšana</strong> un <strong>Pārvērtēšana</strong> transakciju summa līdz pārskatā norādītajam “no” datumam.                               |
|   Vērtības palielināšana/vērtības samazināšana: vērtības palielinājumi periodā   |                                                                    Visu tipa <strong>Vērtības palielināšana</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                                                                    |
|  Vērtības palielināšana/vērtības samazināšana: vērtības samazinājumi periodā  |                                                                   Visu tipa <strong>Vērtības samazināšana</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                                                                   |
| Vērtības palielināšana/vērtības samazināšana: pārvērtējumi periodā  |                                                                        Visu tipa <strong>Pārvērtēšana</strong> to transakciju summa, kas tika iegrāmatotas pārskata datumu diapazonā.                                                                        |
|   Vērtības palielināšana/vērtības samazināšana: izslēgšana periodā   |                                                           Visu to vērtības palielinājumu, vērtības samazinājumu un pārvērtējumu atsaukumu summa, kas tika iegrāmatoti un kam bija izslēgšanas transakcija pārskata datumu diapazonā.                                                           |
|    Vērtības palielināšana/vērtības samazināšana: beigu vērtība     |                               Visu veidu <strong>Vērtības palielināšana</strong>, <strong>Vērtības samazināšana</strong> un <strong>Pārvērtēšana</strong> transakciju summa līdz pārskatā norādītajam “līdz” datumam.                                |
|          Izslēgšana: izslēgšanas datums           |                                                                                                                Pamatlīdzekļu grāmatas izslēgšanas datums.                                                                                                                |
|    Izslēgšana: atlikusī vērtība, veicot izslēgšanu    |                                                                                                    Pamatlīdzekļu grāmatas atlikusī vērtība izslēgšanas laikā                                                                                                    |
|            Izslēgšana: pārdošanas vērtība            |                                                                                               Pārdošanas vērtība pamatlīdzekļu grāmatai ar izslēgšanas-pārdošanas transakciju.                                                                                                |
|           Izslēgšana: lūžņu vērtība            |                                                                                               Lūžņu vērtība pamatlīdzekļu grāmatai ar izslēgšanas-lūžņu transakciju.                                                                                               |
|           Izslēgšana: peļņa/zaudējumi            |                                                                                 Peļņas vai zaudējumu vērtība, kas pamatlīdzekļu grāmatai aprēķināta kā daļa no izslēgšanas transakcijas.                                                                                 |


