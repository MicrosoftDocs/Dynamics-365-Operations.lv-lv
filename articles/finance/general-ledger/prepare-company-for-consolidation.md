---
title: Juridiskas personas sagatavošana konsolidācijas procesam
description: Konsolidācijas procesā darījumi no vairākām juridiskās personas kontu kopām tiek apkopoti vienā juridiskās personas kontu kopā. Šajā tēmā ir paskaidrots, kā sagatavot juridisku personu konsolidēšanai.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a1ffbf79cdccab457b1aee1bc0f1d963bca49b3e390187c6be5da475f278a3d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720506"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Juridiskas personas sagatavošana konsolidācijas procesam

[!include [banner](../includes/banner.md)]

Konsolidācijas procesā darījumi no vairākām juridiskās personas kontu kopām tiek apkopoti vienā juridiskās personas kontu kopā. Šajā tēmā ir paskaidrots, kā sagatavot juridisku personu konsolidēšanai.

> [!NOTE]
> Ieteicams izmantot Management Reporter programmai Microsoft Dynamics 365 Finance, lai apvienotu finanšu rezultātus vairākām juridiskām personām konsolidētā formātā. Management Reporter ļauj izveidot konsolidētus finanšu pārskatus starp juridiskajām personām, izmantot Excel, lai importētu konsolidēšanas datus no citiem avotiem, un pārvērst summas jebkurā pārskatu valūtā bez vajadzības veikt konsolidācijas procesu Dynamics 365 Finance.

Varat drukāt konsolidētās juridiskās personas pārskatus, piemēram, finanšu pārskatus. Tomēr konsolidēto juridisko personu nevar izmantot ikdienas darījumiem.

Varat konsolidēt datus no juridiskām personām, kuras izmanto datu bāzes, kas atšķiras no konsolidētās juridiskās personas. Šāds konsolidācijas process tiek dēvēts par *importa konsolidāciju*. Juridiskās personas var arī izmantot to pašu datu bāzi, ko izmanto konsolidētā juridiskā persona. Šāds konsolidācijas process tiek dēvēts par *tiešsaistes konsolidāciju*.

Konsolidētā juridiskā persona apkopo meitasuzņēmuma rezultātus un bilances. Lai konsolidēto juridisko personu sagatavotu konsolidācijai, izpildiet tālāk minētos norādījumus.

1. Dodieties uz **Virsgrāmata \> Iestatīšana \> Organizācija \> Juridiskās personas**.
2. Lai izveidotu juridisku personu, kas būs konsolidētā juridiskā persona, atlasiet **Jauns**.
3. Atzīmējiet izvēles rūtiņu **Izmantot finanšu konsolidācijas procesam** un pēc tam ievadiet informāciju par konsolidēto juridisko personu. Pārliecinieties, vai ievadāt šo informāciju tieši tā, kā vēlaties to redzēt konsolidētās juridiskās personas finanšu pārskatos.
4. Aizvērt lapu.
5. Atlasiet konsolidēto juridisko personu laukā lapas augšējā labajā stūrī un pēc tam atlasiet **Labi**.
6. Dodieties uz **Virsgrāmata \> Iestatīšana \> Virsgrāmata**.
7. Atlasiet kontu plānus, finanšu kalendāru, uzskaites valūtu, izvēles pārskata valūtu un konsolidētās juridiskās personas noklusējuma maiņas kursa veidu. 
8. Dodieties uz **Virsgrāmata \> Iestatīšana \> Valūta \> Valūtas maiņas kursi**.
9. Meitasuzņēmuma juridisko personu valūtām iestatiet valūtas maiņas kursus atbilstošajiem periodiem.
10. Aizvērt lapu.
11. Ja konsolidētajai juridiskajai personai ir meitasuzņēmumi, kas izmanto ārvalstu valūtas, rīkojieties šādi:

    1. Dodieties uz **Virsgrāmata \> Iestatīšana \> Grāmatošana \> Automātisko darījumu konti**.
    2. Laukā **Grāmatošanas veids** atlasiet atbilstošo kontu:

        - Ja juridiskajai personai ir ārvalstu meitasuzņēmumi, kas finansiāli vai funkcionāli ir atkarīgi no mātes juridiskās personas, atlasiet atbilstošo kontu grāmatojuma veidam **Peļņas un zaudējumu konts konsolidācijas starpībai**.
        - Ja konsolidējat meitasuzņēmumu, kas finansiāli un funkcionāli ir neatkarīgs no mātes juridiskās personas, vai juridiskas personas, kurā ir ietverti rezultāti no vairākiem meitasuzņēmumiem, kas ir finansiāli un funkcionāli neatkarīgi no mātes juridiskās personas, un ja datu konsolidēšanā izmantojat pārrēķināšanas metodes, atlasiet atbilstošo kontu grāmatojuma veidam **Bilances konts konsolidācijas starpībai**.

    3. Laukā **Galvenais konts** atlasiet galvenos kontus, kas jāizmanto ārvalstu valūtu pārvērtēšanas korekcijās.
    4. Aizvērt lapu.

    Ja konsolidēto juridisko personu izveidojāt agrāk periodā, varat pārvērtēt ārvalstu valūtu daudzumus, konsolidācijas periodā mainoties valūtu kursiem.

Periodiskajam darbam **Konsolidēt** tagad ir iestatīta konsolidētā juridiskā persona. Varat veikt importa konsolidāciju vai tiešsaistes konsolidāciju.

- Lai veiktu importa konsolidāciju, dodieties uz **Virsgrāmata \> Periodiski \> Konsolidācija \> Konsolidēt \[Importēt\]**.
- Lai veiktu tiešsaistes konsolidāciju, dodieties uz **Virsgrāmata \> Periodiski \> Konsolidācija \> Konsolidēt \[Tiešsaiste\]**.

> [!NOTE]
> Pirms konsolidācijas apstrādāšanas meitasuzņēmumu juridiskās personas ir jāsagatavo konsolidēšanai. Papildinformāciju skatiet sadaļā [Meitasuzņēmuma juridiskās personas konsolidācijas iestatīšana](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]