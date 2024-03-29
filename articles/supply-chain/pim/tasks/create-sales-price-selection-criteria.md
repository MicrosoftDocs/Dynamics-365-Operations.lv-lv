---
title: Pārdošanas cenu atlases kritēriju izveide
description: Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568451"
---
# <a name="create-sales-price-selection-criteria"></a>Pārdošanas cenu atlases kritēriju izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem. Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams. Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis paraugdatu uzņēmumā USMF. Parasti produktu menedžeris izmanto šo procedūru.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Jauna kritērija pievienošana esošajam pārdošanas cenas modelim

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet atlasiet modeļa nosaukuma saiti.
1. Darbību rūtī atlasiet **Modelis**.
1. Atlasiet **Cenas modeļa kritēriji**.
1. Atlasiet **Jauns**.
1. Laukā **Nosaukums** ierakstiet 'Debitoru grupa 10'.
    * Cenas modeļa kritērija nosaukums tiek izmantots, lai palīdzētu identificēt pamata atlases kritērijus.  
1. Laukā **Cenas modelis** ievadiet vai atlasiet kādu vērtību.
1. Laukā **Pasūtījuma tips** atlasiet *Pārdošanas pasūtījums*.
    * Pasūtījuma tips nosaka datu bāzes laukus, kas būs pieejami atlases vaicājumā.  
1. Laukā **Spēkā no** ievadiet datumu.
1. Laukā **Beidzas pēc** ievadiet datumu.
1. Atlasiet **Saglabāt**.

## <a name="create-the-query-for-the-selection-criteria"></a>Izveidot vaicājumu atlases kritērijiem

1. Atlasiet **Rediģēt**.
2. Laukā **Tabula** atlasiet *Debitorus*.
3. Laukā **Lauks** atlasiet *Debitoru grupu*.
    * Šajā piemērā atlases kritērijiem tiks izmantota noteikta debitoru grupa.  
4. Laukā **Kritēriji** atlasiet *Debitoru grupu 10*.
5. Atlasiet **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]