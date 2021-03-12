---
title: Krājumu skaitīšana noliktavā
description: Šajā tēmā aprakstīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7f85cb91f36004a6bd6da714e7baa460a83a66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000103"
---
# <a name="count-inventory-in-a-warehouse"></a>Krājumu skaitīšana noliktavā

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā. Procedūra attiecas uz "pamata noliktavas" funkcionalitāti, kas pieejama krājumu vadības modulī, nevis uz noliktavas funkcionalitāti, kas ir pieejama noliktavas vadības modulī. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat savus datus, pārliecinieties, ka ir izveidoti produkti un novietojumi un ka esat izveidojis krājumu žurnāla nosaukumu inventarizācijas žurnāliem. Krājumu inventarizāciju parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-counting-journal"></a>Izveidojiet krājumu inventarizācijas žurnālu
1. Dodieties uz sadaļu **Navigācijas rūts > Moduļi > Krājumu pārvaldība > Žurnāla ieraksti > Krājumu inventarizācija > Inventarizācija**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** atlasiet krājumu inventarizācijas žurnāla nosaukumu, kuru vēlaties izmantot no nolaižamā saraksta. Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu inventarizācijas žurnāla nosaukuma iestatījumiem.  
4. Laukā **Darbinieks** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
5. Sarakstā **Aylasiet** darbinieku, kuru vēlaties izmantot.
6. Atlasiet **Labi**.

## <a name="create-journal-lines"></a>Izveidot žurnāla rindas
1. Atlasiet **Jauns**.
2. Laukā **Krājuma kods** nolaižamamajā sarakstā atlasiet vēlamo ierakstu. Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet **A0001**.  
3. Laukā **Vieta** nolaižamamajā sarakstā atlasiet vēlamo ierakstu. Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet vietu **2**.
4. Laukā **Noliktava** nolaižamamajā sarakstā atlasiet vēlamo ierakstu. Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet noliktavu **24**.  
5. Laukā **Atrašanās vieta** nolaižamamajā sarakstā atlasiet vēlamo ierakstu. Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet atrašanās vietu **Lielapjoma-001**.  
6. Laukā Saskaitīts ievadiet skaitli. Ja ievadāt saskaitīto skaitu, kas atšķiras no laukā **Rīcībā esošs** parādītā skaita, lauks **Daudzums** tiek atjaunināts, lai parādītu neatbilstību.  
7. Atlasiet **Saglabāt**.

## <a name="post-the-inventory-counting-journal"></a>Krājumu inventarizācijas žurnāla grāmatošana
1. Atlasiet **Grāmatot**. Grāmatojot krājumu inventarizācijas žurnālu, ja saskaitītais skaits atšķiras no skaita, kas norādīts laukā **Rīcībā esošs**, tiek grāmatota krājumu ieejas plūsma vai izejas plūsma, tiek mainīts krājumu līmenis un vērtība un tiek ģenerētas virsgrāmatas darbības.
2. Atlasiet **Labi**.

## <a name="view-inventory-transactions"></a>Skatiet krājumu darbības
1. Atlasiet **Krājumi**.
2. Atlasiet **Darbības**. Šeit varat redzēt saistītās darbības, kas tiks izveidotas, grāmatojot krājumu inventarizācijas žurnālu.   

