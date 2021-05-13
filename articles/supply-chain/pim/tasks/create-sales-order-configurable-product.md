---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921293"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Pārdošanas pasūtījuma izveide konfigurējamam produktam

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam. Šajā piemērā tiek izmantots D0006 skaļruņu modelis paraugdatu uzņēmumā USMF. Parasti pārdošanas pasūtījuma apstrādātājs izmanto šo procedūru.

## <a name="create-a-sales-order"></a>Izveidot pārdošanas pasūtījumu

1. Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.
1. Atlasiet **Jauns**.
1. Atlasiet vienumu **Pārdošanas pasūtījums**.
1. Laukā **Debitora konts** atlasiet *US-001*. 
1. Atlasiet **Labi**.
1. Laukā **Krājuma numurs** atlasiet *D0006*.
    * Lai veiktu šo uzdevumu, nepieciešams atlasīt konfigurējamu preci.  
1. Atlasiet **Prece un piegāde**.
1. Atlasiet **Konfigurēt rindu**.
    * Ievērojiet, ka cena ir mainījusies, atkarībā no konfigurācijas, kas tika atlasīta, un lauks **Iekļaut kabeli** tagad ir iestatīts uz *Patiess*.  
    * Ievērojiet noklusējuma cenu un iestatījumus, kas ir atlasīti kabelim.  
1. Atlasiet **Ielādēt veidni**.
    * Šajā piemērā ir parādīts kā jūs varat pielietot veidni, lai atlasītu iepriekš definētu konfigurāciju. Ja izmantojat šo procedūru kā uzdevumu ceļvedi un vēlaties skatīt citas pieejamās atribūtu vērtības, atlasiet pogas **Atbloķēt**.  
1. Atlasiet **Labi**.
1. Atlasiet **Labi**.
1. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
1. Atlasīt cilni **Prece**.
    * Krājuma konfigurācija tiek parādīta preces dimensijās.  
1. Aizvērt lapu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]