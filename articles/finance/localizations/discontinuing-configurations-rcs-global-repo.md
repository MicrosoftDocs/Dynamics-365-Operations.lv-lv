---
title: Konfigurāciju pārtraukšana RCS globālajā repozitorijā
description: Šajā rakstā ir aprakstīts, kā pārtraukt konfigurācijas RCS globālajā repozitorijā.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272342"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Konfigurāciju pārtraukšana RCS globālajā repozitorijā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārtraukt konfigurāciju RCS globālajā repozitorijā. Iepriekš bija iespējams dzēst tikai tās konfigurācijas, kuras vairāk nebija nepieciešamas. Taču tagad varat RCS globālajā repozitorijā atzīmēt konfigurāciju kā **Pārtrauktu**. Ar šo funkcionalitāti jūs varat arī: 
 
 - Nodrošināt iepriekšējus paziņojumus, ja tiek plānots pārtraukt konfigurāciju.
 - Iekļaut saistošu informāciju par maiņas konfigurāciju.
 - Konkrētai konfigurācijai iestatīt datumu **Atbalstīta līdz**, lai informētu lietotāju par laiku, kad tā tiks pārtraukta.

Pārtraucot konfigurācijas versiju, varat neobligāti norādīt šādu informāciju:

  - **Aizstāšanas konfigurācija**
  - **Maiņas konfigurācijas versija**
  - **Brīvā teksta piezīme**: Izmantojiet šo lauku, lai sniegtu saites uz dokumentiem vai atsauces
  - **Atbalstīta līdz**: Šis lauks nodrošina piedāvāto datumu, līdz kuram pašreizējā konfigurācija/versija tiks atbalstīta. Šis datums ir jāatjaunina manuāli.
  
Lai pārtrauktu konfigurāciju, izpildiet šīs darbības: 

1. Atlasiet, vai vēlaties pārtraukt vienu vai visas versijas ar tiem pašiem iestatījumiem vienā darbībā, iestatot opciju **Visas versijas** uz **Jā**. 
2. Iestatiet parametru **Pārtraukt** uz opciju **Jā**.
3. Atlasiet **Labi**, lai pārtrauktu konfigurācijas. Lauks **Pārtraukšanas datums** tiks aizpildīts, kad saglabāsit izmaiņas.

![Konfigurācijas pārtraukšanas informācija.](media/Discontinue-details-2.png)
  
Jebkurā laikā varat atgriezt konfigurāciju statusā **Kopīgota** vai pielāgot konfigurācijas informāciju. Kopīgojot informāciju, norādiet datumu **Atbalstīta līdz** un citu informāciju, kas ir saistīta ar pārtraukšanu, lai norādītu savus plānus attiecībā uz pārtraukšanu nākotnē.

Ja vēlaties kopīgot informāciju par plānoto pārtraukšanu pirms faktiskās konfigurācijas pārtraukšanas, lietotājs var iepriekš aizpildīt visus laukus, kas saistīti ar nomaiņu, bet atstāt parametru **Pārtraukt** iestatītu uz **Nē**.

> [!NOTE]
> Pārtraukšana neierobežo darbības ar konfigurācijām. Varat turpināt importēt, palaist vai atvasināt konfigurācijas, šie lauki ir informatīvi.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance atbalsta šīs informācijas rādīšanu, sākot ar versiju 10.0.14

Sākot ar versiju 10.0.14, Dynamics 365 Finanses atbalsta apskatīt jaunāko informāciju. Lapā **Globālais repozitorijs** varat skatīt jaunāko informāciju, kas saistīta ar pārtraukšanu. Konfigurācijas tiek pēc noklusējuma pārtrauktas un filtrētas.
  
Lapā **Importētās konfigurācijas** (ERSolutionTable) tiek rādītas konfigurācijas, kuras jau tika pārtrauktas importēšanas laikā. Informāciju par konfigurācijām, kuras tika pārtrauktas pēc importēšanas, var sinhronizēt, palaižot darbu **Importēt konfigurāciju atjauninājumus**.


