---
title: Budžeta formas transakciju kontu un kopsummas kontu izveide
description: Šajā rakstā ir sniegts pārskats par budžetu veidošanas procesu, pamatojoties uz kopsummu kontiem. Tajā ir arī paskaidrots, kā kopsummu kontiem ieslēgt budžeta kontroli, ja ir nepieciešama budžeta kontrole.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e296118b3b806a5267e29c2b2d4d859c1aea1977
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827390"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Budžeta formas transakciju kontu un kopsummas kontu izveide

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par budžetu veidošanas procesu, pamatojoties uz kopsummu kontiem. Tajā ir arī paskaidrots, kā kopsummu kontiem ieslēgt budžeta kontroli, ja ir nepieciešama budžeta kontrole.

Izmantojot budžeta plānu un budžeta reģistra ieraksta dokumentus, var budžetēt galvenos kontus, kam galvenā konta veids ir **Kopsummas**. Faktiskās izmaksas var grāmatot tikai transakciju galvenajos kontos. 

Periodiskajam procesam **Budžeta plāna ģenerēšana no virsgrāmatas** cilnē **Avots** kā kritēriju var norādīt galvenā konta veidu **Kopsummas**. Šādā gadījumā visi kopsummu galvenie konti tiks iekļauti mērķa budžeta plānā un summa būs vienāda ar atlasīto galveno kontu kopsummu. 

Varat aktivizēt budžeta kontroli galvenajiem kontiem ar veidu **Kopsummas**. Šī funkcionalitāte tiek atbalstīta, izmantojot budžeta grupas. Katram kopsummu galvenajam kontam budžets, kas jākontrolē attiecībā uz budžeta grupu, ir jāizveido lapā **Budžeta kontroles konfigurācija**. Jūsu norādītajos kritērijos ir jāietilpst kopsummu galvenajam kontam un kontu diapazonam. Lai paātrinātu budžeta grupu izveides procesu, varat izmantot budžeta kontroles grupu datu elementu. 

Ja budžets tiek izmantots pārskatā, piemēram, finanšu pārskatā, kopsummu konta budžeta summa sastāv no:

-   budžetiem, kas izveidoti no katra transakcijas virsgrāmatas konta kopsummu intervālā;
-   budžeta kopsummas, kas ievadīta tieši kopsummas kontā.

Tas ļauj izveidot atsevišķus budžetus visnozīmīgākajiem transakciju kontiem kopsummu konta intervālā un pievienot atlikušo budžeta daudzumu kopsummas kontam.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]