---
title: Mērvienības pārvaldība
description: Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886996"
---
# <a name="manage-unit-of-measure"></a>Mērvienības pārvaldība

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām. Šo procedūru var izmēģināt, izmantojot demonstrācijas datus vai izmantojot savus datus.

1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Izlaisto preču uzturēšana**.
2. Noklikšķiniet uz **Mērvienības**.

## <a name="create-a-unit-of-measure"></a>Mērvienības izveide
1. Klikšķiniet **Jauns**.
2. Laukā **Vienība** ierakstiet vērtību. Ievadiet ID vai simbolu, kas jāizmanto, atsaucoties uz mērvienību.  
3. Laukā **Apraksts** ierakstiet kādu vērtību. Ievadiet mērvienības aprakstošo nosaukumu sistēmas valodā.  
4. Laukā **Mērvienību kategorija** atlasiet opciju. Mērvienību kategorija nosaka, kādam loģiskam grupējumam pieder mērvienība, piemēram, platībai, masai vai daudzumam.  
5. Laukā **Decimālā precizitāte** ievadiet skaitli. Norādiet decimāldaļu skaitu, līdz kuram jānoapaļo konvertētā mērvienība, kad mērvienības aprēķins ir pabeigts.  
6. Noklikšķiniet uz **Saglabāt**.

## <a name="define-unit-translations"></a>Vienību tulkojumu definēšana
1. **Darbību rūtī** noklikšķiniet uz **Vienību teksti**.
2. Klikšķiniet **Jauns**. Izmantojiet vienības tekstu, lai izveidotu ID vai simbola, kas apzīmē mērvienību, tulkojumu izmantošanai ārējos dokumentos debitoram vai kreditoram specifiskā valodā.  
3. Laukā **Valoda** ievadiet vai atlasiet kādu vērtību.
4. Laukā **Teksts** ierakstiet vērtību.
5. Noklikšķiniet uz **Saglabāt**.
6. Aizvērt lapu.
7. **Darbību rūtī** noklikšķiniet uz **Tulkotie vienību apraksti**.
8. Klikšķiniet **Jauns**. Definējiet valodai raksturīgus mērvienības aprakstus.  
9. Laukā **Valoda** ievadiet vai atlasiet kādu vērtību.
10. Laukā **Apraksts** ierakstiet kādu vērtību.
11. Noklikšķiniet uz **Saglabāt**.
12. Aizvērt lapu.

## <a name="define-unit-conversion-rules"></a>Vienību pārveidošanas noteikumu definēšana
1. **Darbību rūtī** noklikšķiniet uz **Vienību pārveidošana**. Definējiet noteikumus mērvienības pārveidošanai uz citām mērvienībām un no citām mērvienībām atlasītajā mērvienību kategorijā.  
2. Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā **Koeficients** ievadiet skaitli. Pārveidošanas koeficients no No vienības uz Uz vienību. Piemēram, pārveidošanas koeficients no centimetriem uz metriem ir 100, jo viena metrā ir 100 centimetru.  
4. Laukā **Uz vienību** ievadiet vai atlasiet kādu vērtību.
5. Laukā **Noapaļošana** atlasiet opciju. Nosakiet, kā pārveidotā vērtība ir jānoapaļo.  
6. Noklikšķiniet uz **Labi**.
7. Aizvērt lapu.

