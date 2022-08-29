---
title: Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā rakstā ir aprakstīts, kā projektēt elektronisko pārskatu (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu. (1. daļa - konfigurāciju importēšana).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290550"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
