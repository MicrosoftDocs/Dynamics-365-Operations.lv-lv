---
title: Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem
description: 'Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1. daļa — importa konfigurācijas).'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ca80a2cc1e58723d1f1b39c1fde003fa990a93c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142436"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem

[!include [banner](../../includes/banner.md)]

Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1.



daļa: konfigurāciju importēšana)". Šajā procedūrā jūs izpildāt ER importēta formāta konfigurāciju, kas ir izveidota parauga uzņēmumam Litware.Inc., lai ģenerētu elektroniskos dokumentus.



Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu. 



Pirms sākat, mainiet valsts kontekstu DEMF uzņēmumam no DEU (Vācija) uz BEL (Beļģija). Lai atjauninātu valsts kodu juridiskās personas DEMF primārajā adresē, noklikšķiniet uz Organizācijas administrēšana > Organizācijas > Juridiskās personas. Restartējiet pieteikumu.


## <a name="run-imported-er-format"></a>Palaidiet importēto ER formātu
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā izvērsiet "Intrastat (model)".
3. Kokā atlasiet "Intrastat (model)\Intrastat (format)".
4. Noklikšķiniet uz Palaist.
    * Lai ģenerētu Intrastat pārskatu, palaidiet ER formāta konfigurācijas melnraksta versiju.  
5. Laukā Ievadiet faila nosaukumu ierakstiet "intrastat.xml".
    * Norādiet faila nosaukumu.  
6. Noklikšķiniet uz OK.
    * Pārskatiet ģenerēto XML failu.  
7. Aizvērt lapu.
8. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.
    * Atveriet šo formu, lai apskatītu Intrastat darbības, kas iekļautas ģenerētajā elektroniskajā dokumentā.  
9. Noklikšķiniet uz Intrastat arhīva.
    * Detalizēta informācija par pabeigtu Intrastat pārskatu netika arhivēta, jo izpildītais ER formāts neietver iestatījumus pieteikumu datu atjaunināšanai.  
10. Aizvērt lapu.
11. Aizvērt lapu.

