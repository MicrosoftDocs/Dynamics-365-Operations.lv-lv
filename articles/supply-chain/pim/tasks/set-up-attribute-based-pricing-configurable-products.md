---
title: No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm
description: Šajā tēmā ir izskaidrots, kā iestatīt uz atribūtiem balstītu cenu noteikšanu.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921245"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt uz atribūtiem balstītu cenu noteikšanu. Kā priekšnosacījumam, jums jābūt preces konfigurācijas modelim, kam ir viens vai vairāki komponenti un atribūti. Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa preces modelis demonstrācijas datu uzņēmumā USMF. Parasti produktu menedžeris izmanto šo procedūru.


## <a name="create-a-new-price-model"></a>Izveidot jaunu cenas modeli

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Sarakstā atlasiet rindu **Augstākās klases runātājs**, bet neatlasiet saiti nosaukumam.
1. Darbību rūtī atlasiet **Modelis**.
1. Atlasiet **Cenu modeļi**.
1. Atlasiet **Jauns**.
1. Laukā **Cenu modeļa nosaukums** ievadiet vērtību. Izmantojiet nosaukumu, kas ļauj viegli identificēt modeli.  
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Atlasiet **Saglabāt**.

## <a name="add-price-elements"></a>Pievienot cenas elementus

1. Atlasiet **Rediģēt**. Katrs komponents preces modelī var saturēt pamatcenas elementu un jebkādu cenas izteiksmes kārtulu skaitu. Jūs varat arī pievienot cenas dažādās valūtās.  
2. Laukā **Bāzes cenas izteiksme** ierakstiet vērtību. Piemēram, ievadiet 100. Pamatcenas izteiksme var būt skaitliska vērtība, vai tā var sastāvēt no aritmētiska aprēķina, kas ietver vienu vai vairākus atribūtus.  
3. Atlasiet **Pievienot**.
4. Laukā **Nosaukums** ievadiet `Rosewood`. Cenas izteiksmes nosaukums palīdz noteikt, ko atspoguļo cenas elements. Šajā piemērā tiek izveidots cenas elements Rosewood skaļruņa korpusa apdares opcijai.  
5. Atlasīt **Rediģēt nosacījumu**. Cenas nosacījumu palīdz nodrošināt to, ka cenas izteiksmes elements tiek iekļauts pārdošanas cenā tikai tad, ja ir noteiktu atribūtu kombinācija.  
6. Laukā **ConstraintBody** ievadiet `CabinetFinish=="Rosewood"`.
7. Atlasiet **Labi**.
8. Laukā **Izteiksme** ierakstiet vērtību. Piemēram, ievadiet `50`. 
9. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]