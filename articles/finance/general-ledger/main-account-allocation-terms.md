---
title: Sadalījuma nosacījumi
description: Šajā tēmā sniegta informācija par sadalījuma nosacījumu izmantošanu galvenajā kontā.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 957baba1364fbbd4a51c6f51b0fad5bf8db46680fa97b9d3d0474dc015064609
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776532"
---
# <a name="allocation-terms"></a>Sadalījuma nosacījumi

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta informācija par sadalījuma nosacījumu izmantošanu galvenajā kontā. Sadalījumu nosacījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.

Katrs sadalījuma nosacījums, ko izveidojat galvenajā kontā, nosaka dokumenta procentuālo daļu, kas jāpiešķir no viena avota galvenā konta un finanšu dimensiju kombinācijas. Turklāt jūs nosakāt mērķa galveno kontu un finanšu dimensijas, kur summa tiks piešķirta. 

Definējot sadalījuma avota finanšu dimensiju, varat atlasīt, vai katra dimensija ir īpaša vai nespecifiska. Specifisks norāda, ka avota darbības finanšu dimensijai ir jāatbilst atlasītajai dimensijai. Atlasot nespecifisku, tas norāda, ka jebkura vērtība finanšu dimensijai var veicināt atbilstību.

Definējot mērķa virsgrāmatas kontu sadalījuma nosacījumam, jānorāda galvenais konts, kurā summa tiek iedalīta. Varat izmantot to pašu galveno kontu, kurā tiek grāmatota avota darbība, vai citu galveno kontu. Ja tiek izmantots tas pats galvenais konts, saglabājot ierakstu, tiek parādīts brīdinājums. Papildus galvenā konta norādīšanai jānorāda arī mērķa dimensijas. Katrai dimensijai varat norādīt, vai vēlaties saglabāt avota finanšu dimensijas vērtību vai mainīt to. Ja atlasāt Nē, jums jāatlasa jauna finanšu dimensijas vērtība. Ja atlasīsit Jā, papildu informācija netiek norādīta, un, grāmatojot sistēma saglabās sākotnējās finanšu dimensijas.

Sadalījuma nosacījumu skaits, ko var pievienot galvenajam kontam, nav ierobežots. Tomēr procentu summa, kas jāsadala sadalījuma nosacījumā, nevar pārsniegt 100. Varat izveidot sadalījumus, kas mazāki par 100 procentiem, ja sākotnējās dokumenta summas daļa paliek avota finanšu dimensijās. Sadalījuma nosacījumus galvenajam kontam var pievienot kā juridiskās personas ignorēšanu. Ja izmantojat kopīgu kontu plānu, katrai juridiskajai personai ir jādefinē sadalījuma nosacījumi. Lai piekļūtu pogai **Sadalījuma nosacījumi**, vispirms ir jāatlasa **Sadalījuma** izvēles rūtiņa juridiskās personas ignorēšanai.

## <a name="allocation-term-example"></a>Sadalījuma nosacījuma piemērs
Jūs esat definējis jūsu organizācijas izmaksu centru, ko sauc par CORPORATE, kas ir numurēta kā 000. Kad rēķini tiek grāmatoti komunālajiem izdevumiem, tie ir kodēti šim CORPORATE izmaksu centram. Jūsu uzņēmums ir definējis kārtulu, ka visi komunālie izdevumi ir jāpiešķir katram no atsevišķiem izmaksu centriem procentos. Citas nodaļas un biznesa vienības finanšu dimensijas paliks tās pašas.

Izmantojot šo piemēru, komunālo izdevumu galvenajam kontam tiks izveidots jauns sadalījuma nosacījums. Katram izmaksu centram tiks izveidota viena rinda ar sadalītajiem procentiem. Katras rindas avota finanšu dimensiju **Atlases kritēriji** ir **Specifiski** **Izmaksu centram**, un vērtība tiks iestatīta uz 000: CORPORATE. Struktūrvienībai un biznesa vienībai **Atlases kritēriji** būtu **Nespecifiski**.

**Mērķa virsgrāmatas konta** kopsavilkuma cilnē galvenais konts būs tas pats komunālo izdevumu konts, un, opcija **Saglabāt avota finanšu dimensijas** būs iestatīta uz **Jā** **Biznesa struktūrvienībai** un **Departamentam**. Opcija **Saglabāt avota finanšu dimensijas** **Izmaksu centram** būs iestatīta uz **Nē**, un atlasītā vērtība būs katrs atbilstošais izmaksu centrs, kuram tiek piešķirts sadalījums. Ja ir trīs izmaksu centri, kam var to piešķirt, tiks izveidoti trīs sadalījuma nosacījumu ieraksti. Vienīgā atšķirība starp katra sadalījuma nosacījumu ir izmaksu centrs, kas norādīts mērķa virsgrāmatas kontā.

## <a name="create-an-allocation-term-on-a-main-account"></a>Izveidot sadalījuma nosacījumu galvenajā kontā

1. Sadaļā **Navigācijas rūts** dodieties uz **Moduļi > Virsgrāmata > Kontu plāns > Konti > Galvenie konti**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Kopsavilkuma cilnē **Juridiskā persona ignorē** atlasiet **Pievienot**.
4. Atlasiet **Uzņēmums** un pēc tam atlasiet **Pievienot**.
5. Atzīmējiet izvēles rūtiņu **Sadalījums**.
6. Atlasiet **Sadalījuma nosacījumi** .
7. Atlasiet **Rediģēt**, lai pārveidotu noklusējuma ierakstu, vai atlasiet **Jauns**, lai pievienotu ierakstu.
8. Laukā **Procenti** ievadiet to dokumentu transakciju procentuālo daudzumu, ko vēlaties piešķirt.
9. Kopsavilkuma cilnē **Avota finanšu dimensija** katrai finanšu dimensijai sadaļā **Atlases kritēriji** atlasiet opciju.
    - Ja atlasāt **Specifisks**, labajā pusē nolaižamajā lodziņā atlasiet finanšu dimensijas vērtību.
    - Ja izvēlaties **Nespecifisks**, finanšu dimensijai nav nepieciešama papildu informācija.
10. **Mērķa virsgrāmatas** konta kopsavilkuma cilnē laukā **Uz kontu** atlasiet galveno kontu, kurā vēlaties sadalīt dokumenta darbības procentuālo vērtību.
11. Katrai finanšu dimensijai sadaļā **Saglabāt avota finanšu dimensijas** atlasiet opciju.
    - Ja atlasāt **Nē**, atlasiet finanšu dimensijas vērtību nolaižamajā lodziņā labajā pusē, kur vēlaties, lai dokumenta darbība tiktu piešķirta.
    - Ja atlasāt **Jā**, papildu informācija nav nepieciešama. Iegrāmatojot sadalījumu, sistēma saglabās sākotnējo dokumenta vērtību.
12. Atkārtojiet 7.-11. darbību katram papildu sadalījumam. Visu sadalījumu summa ir norādīta laukā **Kopējā procentuālā summa**. Šī summa nevar pārsniegt 100.
13. Aizveriet visas lapas.

>[!NOTE] 
> Pēc izvēles jūs varat izmantot pogu **Kopēt**, lai dublētu atlasīto sadalījumu.

Kad galvenajam kontam ir izveidots sadalījuma nosacījums, sistēma automātiski grāmatos jaunu dokumentu, kolīdz tiks grāmatots dokuments, kas atbilst avota finanšu dimensijām sadalījuma nosacījumos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]