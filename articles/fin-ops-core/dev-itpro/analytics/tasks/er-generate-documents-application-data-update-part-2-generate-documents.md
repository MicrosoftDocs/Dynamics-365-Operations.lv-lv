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
ms.openlocfilehash: 9aec1da7fe168b05af10470221ac745ec1c01f6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182328"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
