---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9a9b60fbcf6de5377b44ca03d4ffc792a6a78f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206995"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Pārdošanas pasūtījuma izveide konfigurējamam produktam

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam. Šajā piemērā tiek izmantots D0006 skaļruņu modelis paraugdatu uzņēmumā USMF. Parasti pārdošanas pasūtījuma apstrādātājs izmanto šo procedūru.


## <a name="create-a-sales-order"></a>Pārdošanas pasūtījuma izveidošana
1. Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.
2. Noklikšķiniet uz Jauns.
3. Noklikšķiniet uz Pārdošanas pasūtījums.
4. Laukā Debitora konts atlasiet US-001. 
5. Noklikšķiniet uz OK.
6. Laukā Krājuma kods atlasiet D0006.
    * Lai veiktu šo uzdevumu, nepieciešams atlasīt konfigurējamu preci.  
7. Noklikšķiniet uz Preces un piegādes.
8. Noklikšķiniet uz Konfigurēt rindu.
    * Ievērojiet, ka cena ir mainījusies, atkarībā no konfigurācijas, kas tika atlasīta, un lauks Iekļaut kabeli tagad ir iestatīts uz Patiess.  
    * Ievērojiet noklusējuma cenu un iestatījumus, kas ir atlasīti kabelim.  
9. Noklikšķiniet uz Kravas veidne.
    * Šajā piemērā ir parādīts kā jūs varat pielietot veidni, lai atlasītu iepriekš definētu konfigurāciju. Ja izmantojat šo procedūru kā uzdevumu ceļvedi un vēlaties skatīt citas pieejamās atribūtu vērtības, noklikšķiniet uz pogas Atbloķēt.  
10. Noklikšķiniet uz OK.
11. Noklikšķiniet uz OK.
12. Izvērsiet sadaļu Detalizēta informācija par rindu.
13. Noklikšķiniet uz cilnes Prece.
    * Krājuma konfigurācija tiek parādīta preces dimensijās.  
14. Aizvērt lapu.

## <a name="select-the-product-configuration"></a>Atlasiet preces konfigurāciju



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]