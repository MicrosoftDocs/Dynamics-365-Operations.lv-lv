---
title: Starpuzņēmumu datu avoti elektroniskajos pārskatos (ER)
description: Šajā tēmā ir paskaidrots, kā elektroniskajos pārskatos (Electronic Reporting — ER) varat izmantot starpuzņēmumu datu avotus.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: dc98f060bbb27958436cd2183bb469f821d04320
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181500"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Starpuzņēmumu datu avoti elektroniskajos pārskatos (ER)

[!include[banner](../includes/banner.md)]

Varat noformēt elektronisko pārskatu (Electronic Reporting — ER) formātus, lai izejošos dokumentus ģenerētu dažādos formātos. Kad dokuments tiek ģenerēts, ER formāts izsauc datu avotus, kas bija konfigurēti atbilstošā ER modeļa kartēšanā. Lai ierakstu izgūšanai konfigurētu piekļuvi programmas tabulām, varat izmantot ER datu avotus ar tipu **Tabulas ieraksti**. Ja tabula, kurai piekļūstat, ir koplietota tabula (tas ir, tabula, kur dati tiek saglabāti bez uzņēmuma identifikatora), šis datu avots atgriež visus ierakstus. Ja tabula, kurai piekļūstat, ir no uzņēmuma atkarīga tabula (tas ir, tabula, kur dati tiek saglabāti pēc uzņēmuma), šis datu avots atgriež tikai ierakstus, kas ir saglabāti pašreizējam uzņēmumam (tas ir, tā uzņēmuma kontekstā, kurā darbojas šis ER formāts).

Katru datu avotu ar tipu **Tabulas ieraksti** modeļa kartēšanā tagad var atzīmēt kā starpuzņēmumu datu avotu. Līdz ar to varat izmantot datu avotus ar tipu **Tabulas ieraksti**, lai piekļūtu starpuzņēmumu datiem programmas tabulās.

Ja kādu datu avotu atzīmējat kā starpuzņēmumu, tas darbojas tālāk norādītajā veidā.

- Datu avotam, kas atsaucas uz jebkuru koplietoto tabulu, izņemot CompanyInfo, datu avots atgriež visus ierakstus, kas pastāv šajā tabulā, uz kuru ir atsauce. 
- Datu avotam, kas atsaucas uz tabulu CompanyInfo, lai gan CompanyInfo ir koplietota tabula, datu avots atgriež ierakstus, kuros ir definētajā tvērumā ietilpstošs uzņēmuma identifikators.
- Visām no uzņēmuma atkarīgajām tabulām no tabulas, uz kuru pastāv atsauce, datu avots atgriež ierakstus, kuros ir definētajā tvērumā ietilpstošs uzņēmuma identifikators.

Sistēmas vaicājuma dialoglodziņā, kad ir ieslēgta opcija **Aptaujāt vaicājumam** visiem datu avotiem, kas ir atzīmēti kā starpuzņēmumu, varat manuāli atlasīt vienu vai vairākus uzņēmumus, ko ietvert cilnē **Uzņēmumu diapazons**.

> [!IMPORTANT]
> Tāpat kā citi filtri, arī uzņēmumu filtrs pastāv kā pēdējā izmantotā vērtība vaicājumiem, kad palaižat kādu ER formātu. Filtrs netiek automātiski mainīts, ja datu avotam maināt starpuzņēmumu vērtību. Lai izmantotu citu starpuzņēmumu vērtību citam datu avotam, izdzēsiet atbilstošo lietotājam raksturīgo atlasi.

Katram datu avotam, kas ir atzīmēts kā starpuzņēmumu, varat atlasīt ierakstus, kurus vēlaties, ER izteiksmēs izmantojot funkciju **FILTER** un funkciju **WHERE**. Arī lauku **dataAreaID** var izmantot kā uzņēmuma identifikatoru. Ja tiek izmantota funkcija **FILTER**, laukam **dataAreaID** pašlaik var izmantot tikai tālāk norādītos nosacījumu tipus.

- Tiek atbalstīti tikai nosacījumi, kuriem ir viens lauka **dataAreaID** salīdzinājums.
- Ir atļauti tikai salīdzinājumi, kuru izteiksmes nav atkarīgas no ierakstu saraksta vienumiem.

Tādēļ ir derīga tālāk norādītā izteiksme.

```
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Pēc noklusējuma tvērums ietver visus pašreizējās programmas uzņēmumus. Taču to var ierobežot. Lai ierobežotu starpuzņēmumu datu piekļuves tvērumu vienam ER formātam, piešķiriet šim formātam noteiktu organizācijas hierarhiju. Kad ER formātam ir definēta kāda hierarhija, tiek atgriezti tikai ieraksti juridiskajām personām, kas atrodas piešķirtajā hierarhijā, lai gan ar formātu tiek izsaukti starpuzņēmumu datu avoti. Ja kādam ER formātam ir definēta atsauce uz hierarhiju, kas vairs nepastāv, tiek lietots noklusējuma tvērums un ar formātu tiek izsaukti starpuzņēmumu datu avoti. Šādā gadījumā tiek atgriezti ieraksti visiem programmas uzņēmumiem.

Ņemiet vērā, ka gadījumā, ja ir ieslēgta opcija **Izmantot melnrakstu** vienam ER formātam piešķirtai organizācijas hierarhijai, starpuzņēmumu datu avotu tvēruma identificēšanai tiks izmantotas juridiskās personas no šīs hierarhijas melnraksta versijas. Ja melnraksta versija nepastāv, šim nolūkam tiks izmantotas juridiskās personas no šīs organizācijas hierarhijas pēdējās publicētās versijas.

Ņemiet vērā, ka gadījumā, ja ir izslēgta opcija **Izmantot melnrakstu** vienam ER formātam piešķirtai organizācijas hierarhijai, starpuzņēmumu datu avotu tvēruma identificēšanai tiks izmantotas juridiskās personas no šīs organizācijas hierarhijas pēdējās publicētās versijas. ER struktūrā vēl netiek atbalstīti organizācijas hierarhiju spēkā stāšanās datumi.

Hierarhiju var piešķirt formātam noteiktā lapā, kurai var piekļūt no ER darbvietas vai izmantojot izvēlnes vienumu **Organizācijas administrēšana \>Elektroniskie pārskati \> Juridisko personu filtrs formātiem**. Lai piekļūtu šai lapai, lietotājam ir jābūt piešķirtai privilēģijai **Uzturēt juridisko personu filtrus formātiem** (ERMaintainFormatMappingLegalEntityFilters). No hierarhijas atkarīgu juridisko personu tvēruma ierobežojums formātam tiek lietots papildus ierobežojumam, kuru lietotājs var manuāli norādīt sistēmas vaicājuma dialoglodziņā. Palaižot šo formātu, tiek izmantota šo ierobežojumu krustošanās.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevuma ceļvedi **ER Piekļuve no uzņēmuma atkarīgu tabulu ierakstiem starpuzņēmumu režīmā**, kas veido daļu no biznesa procesa 7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677) un ko var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684). Šajā uzdevuma rokasgrāmatā ir izklāstīts ER modeļa kartēšanas un ER formāta konfigurēšanas process, lai piekļūtu programmas tabulām starpuzņēmumu režīmā.

Lai izpildītu šo uzdevuma ceļvedi, lejupielādējiet tālāk norādītos failus.

- [ER modeļa konfigurācija — CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER formāta konfigurācija — CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)
