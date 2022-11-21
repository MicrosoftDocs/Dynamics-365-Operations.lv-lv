---
title: Meitasuzņēmuma datu importēšana no failiem
description: Šajā rakstā ir paskaidrots, kā sagatavot datus no ārējām sistēmām, lai tos varētu importēt 365 Microsoft Dynamics Finance.
author: jinniew
ms.date: 10/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 494f6396d5e6fab6fef9404ad473566b02b1b9ab
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780101"
---
# <a name="import-subsidiary-data-from-files"></a>Meitasuzņēmuma datu importēšana no failiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā sagatavot datus no ārējām sistēmām, lai tos varētu importēt 365 Microsoft Dynamics Finance. Izmantojiet lapu **Konsolidēt ar importēšanu** (**Konsolidācija \> Konsolidēt ar importēšanu**), lai sagatavotu meitasuzņēmuma datu pārsūtīšanu no ārējām sistēmām.

1. Meitasuzņēmuma juridiskās personas konsolidācijas izveidošana. Informāciju par to, kā izveidot juridiskās personas, skatiet sadaļā [Juridiskas personas izveidošana](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Papildinformāciju skatiet sadaļās [Juridiskas personas sagatavošana izmantošanai konsolidācijas procesā](prepare-company-for-consolidation.md) un [Meitasuzņēmuma juridiskās personas konsolidācijas iestatīšana](set-up-subsidiary-company-for-consolidation.md).

2. Sagatavojiet failu, kas ietvers importētos datus. Papildinformāciju par importēšanas procesu skatiet [Datu importēšanas un eksportēšanas darbu apskatā](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Eksportējiet datus uz failu, izpildot darbības “Datu importēšanas/eksportēšanas procesa” procedūrā, kas atrodas sadaļā [Datu importēšanas un eksportēšanas darbu pārskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Varat izmantot šo procedūru, lai konsolidētu datus no citas Dynamics 365 Finance instances vai no Dynamics 365 Business Central. Ja importējat datus no ārējām sistēmām, datiem jābūt tādā formātā, kā aprakstīts sadaļā [Meitasuzņēmuma datu eksportēšana uz failiem](export-subsidiary-data-to-file.md).
4. Dodieties uz **Konsolidācija \> Konsolidēt ar importēšanu**. Lapas **Konsolidēt ar importēšanu** cilnē **Kritēriji** norādiet informāciju par pārskatu un/vai importēšanu, iestatot tālāk esošos laukus.

| Lauks                                 | Pārskata vērtība | Importēšanas vērtība |
|---------------------------------------|----------------------|----------------------|
| **Apraksts**                      | Nav attiecināms | Ievadiet aprakstu, lai identificētu importēšanu. |
| **Galvenais konts**    | Norādiet pārskatā iekļaujamo kontu diapazonu. Ja diapazons netiks norādīts, tiks iekļauti visi konti. | Norādiet importēšanā iekļaujamo kontu diapazonu. Ja diapazons netiks norādīts, tiks iekļauti visi konti. |
    | **Konsolidācijas periods**                  | Norādiet konsolidēšanas datumu diapazonu. | Norādiet konsolidēšanas datumu diapazonu. |
    | **Ietvert faktiskās summas**                | Iestatiet šo opciju uz **Jā**, lai iekļautu faktiskās summas. | Iestatiet šo opciju uz **Jā**, lai iekļautu faktiskās summas. |
| **Ietvert budžeta summas** | Iestatiet šo opciju uz **Jā**, lai ietvertu budžeta summas konsolidācijās. | Iestatiet šo opciju uz **Jā**, lai ietvertu budžeta summas konsolidācijās. |
| **Atjaunot bilances konsolidācijas laikā** | Iestatiet šo opciju uz **Jā**, ja atjaunošanas procesam ir pilnībā jānotīra bilance un jaunie ieraksti un no jauna jāizveido bilance no laika sākuma. | Iestatiet šo opciju uz **Jā**, ja atjaunošanas procesam ir pilnībā jānotīra bilance un jaunie ieraksti un no jauna jāizveido bilance no laika sākuma. |
| **Budžeta modeļi**                         | Nav attiecināms | Ja izvēlējāties importēt budžeta summas, ievadiet budžeta modeļus konsolidēšanai. |
    | **Budžeta kursa tips**                      | Nav attiecināms | Ievadiet budžeta maiņas kursa veidus. |

6. Ja jums ir dažādas uzskaites valūtas, izmantojiet laukus cilnē **Valūtas pārrēķināšana**, lai konfigurētu pārrēķināšanu, kas veikta konsolidācijas laikā.

    | Lauks                      | Apraksts |
    |----------------------------|-------------|
 | **Avota juridiskā persona**        | Atlasiet juridisko personu, no kuras tiks importēts. |
 | **Izcelsmes uzskaites valūta** | Šī noklusējuma valūta ir saistīta ar avota juridisko personu, kuru atlasījāt laukā **Avota juridiskā persona**. |
 | **No** un **uz kontiem**       | Norādiet no avota juridiskās personas importējamo kontu diapazonu. |
    | **Maiņas kursa veids**         | Atlasiet maiņas kursa veidu. Maiņas kursu veidi tiek piešķirti, izveidojot galveno kontu. Papildinformāciju skatiet sadaļā [Galvenā konta izveidošana](tasks/create-main-account.md). |
| **Lietot maiņas kursu no**   | Ievadiet datumu, lai piemērotu valūtas kursu, kas bija spēkā šajā datumā. Vai arī ievadiet vērtību, kas jāizmanto kā valūtas maiņas kurss. |
| **Maiņas kurss**  | Noklusējuma vērtība ir atkarīga no valūtas maiņas kursa veida, kas tika atlasīts laukā **Maiņas kursa veids**. Ja ievadījāt lietotāja norādītu valūtas maiņas kursu, tad varat norādīt kursu. |

7. Lai iespējotu importēšanas procesa izpildi fonā, iestatiet opciju **Palaist fonā** uz **Jā**.
8. Lai noteiktā laikā palaistu konsolidāciju kā pakešuzdevumu, iestatiet opciju **Pakešapstrāde** uz **Jā**. Lai nekavējoties palaistu konsolidāciju, atlasiet **Labi**. 

Darījumi un bilances, kas tikuši norādīti konsolidācijai meitasuzņēmumos, tiek pievienoti attiecīgajiem kontiem konsolidētajā juridiskajā personā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
