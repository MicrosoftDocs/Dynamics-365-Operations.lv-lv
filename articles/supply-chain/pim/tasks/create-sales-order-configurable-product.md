---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570589"
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