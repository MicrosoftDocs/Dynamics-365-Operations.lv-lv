---
title: Dokumentu ar programmas datiem ģenerēšana
description: 'Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa — modificēt formātu)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569585"
---
# <a name="generate-documents-that-have-application-data"></a>Dokumentu ar programmas datiem ģenerēšana

[!include [banner](../../includes/banner.md)]

Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa: Modificēt formātu)".



Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus. Šajā procedūrā jums ir jāizpilda ER formāta konfigurācija, lai ģenerētu Intrastat pārskatu un atjauninātu pieteikumu datus detalizētas informācijas arhivēšanai par pārskatu veidošanas procesu.



Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot DEMF datu kopu. Pirms sākat, pārliecinieties, vai valsts konteksts DEMF uzņēmumam ir BEL (Beļģija).


## <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus
1. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.
2. Noklikšķiniet uz cilnes Numuru sērijas.

    Arhivējot detalizētu informāciju par Intrastat pārskatu veidošanas procesu, mums ir nepieciešams noteikt katra izveidotā arhīva ierakstus. Šajā nolūkā ir jākonfigurē īpaša numuru sērija.  

3. Atlasiet atsauci 'Intrastat arhīva ID'.
4. Laukā Numuru sērijas kods, ierakstiet kādu vērtību.

    Laukā 'Numuru sērijas kods' ievadiet vai atlasiet vērtību 'Fore_2'.  

5. ResolveChanges Numuru sērijas kods.
6. Klikšķiniet Saglabāt.
7. Aizvērt lapu.

## <a name="run-modified-er-format"></a>Modificētā ER formāta palaišana
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā izvērsiet "Intrastat (model)".
3. Kokā atlasiet "Intrastat (model)\Intrastat (format)".
4. Noklikšķiniet uz Palaist.
5. Laukā Ievadiet faila nosaukumu ierakstiet "intrastat2.xml".
6. Noklikšķiniet uz Labi.

## <a name="review-er-format-executions-results"></a>ER formāta izpildes rezultātu pārskatīšana
Pārskatiet ģenerēto XML failu.  
1. Aizvērt lapu.
2. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.

    Atveriet šo formu, kas satur Intrastat darbības, kuras iekļautas ģenerētajā elektroniskajā dokumentā.  

3. Noklikšķiniet uz Intrastat arhīva.

    Detalizēta informācija par pabeigtu Intrastat pārskatu tika arhivēta, jo izpildītais ER formāts tagad satur iestatījumus pieteikumu datu atjaunināšanai. Šajā formā varat redzēt izveidotā arhīva galvenes ierakstu.  

4. Noklikšķiniet uz Detaļas.

    Šajā formā varat redzēt detalizētu informāciju par izveidoto arhīvu.  

5. Aizvērt lapu.
6. Aizvērt lapu.
7. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]