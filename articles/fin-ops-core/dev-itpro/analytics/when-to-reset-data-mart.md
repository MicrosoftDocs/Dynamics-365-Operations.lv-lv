---
title: Kad atiestatīt data mart
description: Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754148"
---
# <a name="when-to-reset-a-data-mart"></a>Kad atiestatīt data mart

Data mart atiestatīšana var būt laikietilpīga. Atkarībā no apstākļiem šī darbība var nebūt nepieciešamais risinājums. Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Kad nepieciešams veikt data mart atiestatīšanu?
Pirms data mart atiestatīšanas aplūkosim šādus jautājumus. Atbildot "jā" uz vienu vai vairākiem jautājumiem, var norādīt, ka jūsu organizācija var gūt labumu, atiestata data mart.

- Programmas datu bāze tika atjaunota, bet data mart netika atjaunota.
- Jūs redzat nepareizus datus uzskaites periodam, kas nav pārskata dizaina problēmas rezultāts.
- Jūs redzat nepareizus datus uzskaites periodam, un ieraksti tiek uzskaitīti integrācijas mēģinājumu sarakstā pārskatu veidotāja lapā **Integrācijas statuss** (startējiet pārskatu veidotāju un atlasiet **Rīki > Integrācijas statuss**).
- Jūs esat atvēris atbalsta incidentu, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Kad nav atbilstoši atiestatīt data mart?
Ir daži apstākļi, kad nav ieteicams atiestatīt data mart. Tie ietver. 

- Jebkurā laikā šajā tēmā nav uzskaitīts iemesls.
- Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmas. Šajā iestatījumā, iespējams, data mart atiestatīšana nelīdzēsies.
- Ja periodisks atiestatīšanas modelis ir nepieciešams kāda no šo iemeslu dēļ: 
  - **Trūkst dati** - vispirms likvidējiet pārskata dizaina problēmas un datu sinhronizēšanas hronometrāžas problēmas, piemēram, jūs ievērojat, ka fakta karte nav palaista, jo trūkstošie dati tika grāmatoti.
  - **Kavēts integrācijas stāvoklis** - Ja integrācija ir lēna vai šķiet, ka pielīmē, datu izejas plūsma tiek atiestatīta, maz ticams, lai atrisinātu problēmu.
  - **Mēģinājumi atiestatīt ir bijuši neveiksmīgi** - Ja ir veikts mēģinājumu skaits pabeigt atiestatīšanu, un to nav bijis neveiksmīgs, tāpēc ieteicams atvērt atbalsta atgadījumu un strādāt ar atbalsta inženieri, lai analizētu jūsu situāciju pirms datu neveiksmīgas atiestatīšanas mēģinājuma vēlreiz.
  - **Novecojuši ieraksti** - novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu. Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tā rezultāts būs uzlabojums.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Ko data mart atiestatīšana nedara  
- Atiestatīšana sāksies tikai tad, kad esošie uzdevumi būs pabeigti. Tas nodrošina, ka vecie dati netiek ievietoti. Šajā brīdī varat redzēt ziņojumu, piemēram, "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ. Lūdzu, vēlāk mēģiniet vēlreiz."
- Atiestatīšana atspējos integrācijas uzdevumus un izdzēsīs visus data mart datus. Integrācijas atkārtota iespējošana.

> [!NOTE]
> Tālāk norādītajiem punktiem ir divas lietas, kas *neatiestata* data mart. <br>
> - Atiestatīšana nenoņem pārskata dizainus. <br>
> - Atiestatīšana, ja nav atlasīta, nenoņem uzņēmuma datus vai lietotāja datus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]