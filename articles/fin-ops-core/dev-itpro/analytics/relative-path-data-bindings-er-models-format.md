---
title: Relatīva ceļa lietošana ER modeļu un formātu datu saistījumiem
description: Elektronisko pārskatu veidošanas (Electronic reporting — ER) rīks ļauj definēt elektronisko formātu struktūras un pēc tam aprakstīt, kā šīs struktūras vajadzētu aizpildīt.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 141d58c2183c386584b0b974f4997e7a81ef3109
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749990"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Relatīva ceļa lietošana ER modeļu un formātu datu saistījumiem

[!include[banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (Electronic reporting — ER) rīks ļauj lietotājiem definēt elektronisko formātu struktūras un pēc tam aprakstīt veidu, kā šīs struktūras vajadzētu aizpildīt, izmantojot datus un algoritmus, kas pastāv programmā. Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas (ER) konfigurāciju izveide](electronic-reporting-configuration.md). Lai norādītu datu plūsmu Finance and Operations datu izgūšanai un to izmantotu elektroniska dokumenta ģenerēšanai, ir jāizpilda tālāk aprakstītā procedūra.

- Konfigurētie datu avoti ir jāsaista ar izveidotajam domēnam raksturīgā [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) elementiem. Modeļa struktūra un atlasītie datu avoti var veidot daļu no kompleksas hierarhiskas struktūras. Šī iemesla dēļ galīgie saistījumi var būt diezgan lieli un tajos var būt daudz dažādu tipu elementu (piemēram, relācijas, tabulas un metodes). Saistījumi var kļūt grūtāk lasāmi, un tos var būt diezgan sarežģīti pārskatīt un saprast, it īpaši lietotājiem, kas nav to īpašnieki. 
- Datu modeļu elementi ir jāsaista ar [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentiem, lai noteiktu, kādi dati no attiecīgā datu modeļa tiks aizpildīti uz ģenerēto formāta izvadi.

Lai uzlabotu ER kartēšanas noformētāju lietojamību, ir izlaists [relatīvā ceļa](er-formula-language.md#relative-path) līdzeklis. Pēc noklusējuma relatīvā ceļa rādīšanas opcija ir ieslēgta visām jaunajām programmas instancēm, kur ir iespējota ER noformējuma funkcionalitāte (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Mēs ieviesām relatīvā ceļa parametru, lai lietotāji varētu turpināt izmantot pilno ceļu, strādājot ar šo ER saistījumu attēlojumu.

[![Lietotāja parametri](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Kad ir ieslēgts relatīvā ceļa lietošanas parametrs, ceļu uz vecākelementa vienumu pašreizējā modeļa elementa saistījumā aizstāj viena rakstzīme @. Viss saistījuma ceļš kļūst īsāks, līdz ar to viss kartējums ir skaidrāks un saprotamāks. Vairumā gadījumu ER noformētājā nav nepieciešams veikt papildu ritināšanu, lai skatītu visus datu modeļa saistījumus.

[![Modeļa kartējuma noformētājs](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Kad sākat noformēt jaunu ER izteiksmi, ir jāievada tikai viena rakstzīme, lai definētu saistījumu ar kādu vecākelementa vienuma lauku.

[![Formulas veidotājs](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Kad vecākelementa modeļa vienumam izlemjat mainīt datu avotu, ja izmantojat absolūto ceļu, jums šim modeļa vienumam, kā arī visiem ligzdotajiem vienumiem, ir manuāli jāmaina piesaiste uz jaunu datu avotu. Ja ir ieslēgta relatīvā ceļa lietošana un jūs atlasāt jaunu datu avotu, kas ir jāsaista ar kādu vecākelementa vienumu, jums tiek piedāvāta opcija visiem šajā vecākelementa vienumā ligzdotajiem elementiem ar vienu klikšķi mainīt piesaisti automātiski.

[![Ziņojums par esoša ceļa aizstāšanu](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Ja apstiprināt ligzdoto vienumu piesaistes maiņu, jaunais vecākelementa vienums tiks ievietots visu to ligzdoto vienumu ceļā, kuros ir pastāvošais vecākelementa vienums.
Šis līdzeklis nesabojā ER struktūras atpakaļsaderību. Visas iepriekš izveidotās ER konfigurācijas darbosies ar šo jauno līdzekli, un nav jāveic nekāda jaunināšana vai konvertēšana.

> [!NOTE]
> Visas izmaiņas, kas tiek ieviestas ar ligzdotu elementu masveida modificēšanu modeļa kartējumos, tiek pareizi saglabātas konfigurācijas deltā (izmaiņu izsekošanā). Tas ļauj klientiem mainīt savu atvasināto modeļu kartējumu versiju bāzi uz jebkādu jaunu bāzes versiju, kura ir modificēta, izmantojot šo jauno līdzekli.

## <a name="additional-resources"></a>Papildu resursi

[ER formulu valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]