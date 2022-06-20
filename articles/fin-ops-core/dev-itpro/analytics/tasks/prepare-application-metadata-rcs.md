---
title: Programmas metadatu sagatavošana lietošanai ar RCS
description: Šajā rakstā ir aprakstīts, kā izveidot jaunu pārskata konfigurāciju, kas satur programmas metadatus.
author: NickSelin
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b5e7f69653381e16b4a8a8def56845a41bb14b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868802"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Programmas metadatu sagatavošana lietošanai ar RCS
[!include [banner](../../includes/banner.md)]

Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot jaunu elektronisko pārskatu (Electronic reporting — ER) konfigurāciju, kurā ir programmas metadati ER modeļa kartēšanas konfigurāciju veidošanai pakalpojumā Regulatory Configuration Service (RCS). Šī konfigurācija tiks izmantota, lai izstrādātu parauga ER modeļa kartēšanas konfigurāciju, kura ir paredzēta piekļūšanai ārējās tirdzniecības transakcijām. Šajā piemērā tiek izveidota konfigurācija parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā. Lai veiktu šīs darbības, vispirms ir jāveic soļi rakstā, izveidojiet konfigurācijas nodrošinātājus [un atzīmējiet tos kā aktīvus](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Priekšnosacījumi
1.    Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**. 
2.    Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). 
3.    Noklikšķiniet uz **Metadatu konfigurācijas**. 
4.    Pieņemsim, ka pakalpojums RCS tiks izmantots, lai izveidotu ER risinājumu kādai Finance and Operation programmai, kas ģenerēs elektroniskus dokumentus, kuros ir informācija no ārējās tirdzniecības uzņēmējdarbības jomas. Lai norādītu kartēšanu starp ER datu modeli un nepieciešamo datu avotiem, pakalpojumā RCS mums ir nepieciešama piekļuve Finance and Operation programmas metadatiem. Tādēļ ER risinājuma veidošanas gaitā mums ir jākonfigurē jauna ER metadatu konfigurācija, kas ietver visus metadatus, kuri pašlaik ir nepieciešami ER pārskatu veidošanai atlasītajai uzņēmējdarbības jomai. 

## <a name="add-metadata-configuration"></a>Metadatu konfigurācijas pievienošana 
1.    Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. 
2.    Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības metadati”. 
3.    Noklikšķiniet uz **Izveidot konfigurāciju**. 
4.    Noklikšķiniet uz **Noformētājs**. 
5.    Noklikšķiniet uz **Pievienot**. 
  
> [!NOTE]
> Varat atlasīt visus metadatus visai programmai vai atlasītajiem modeļiem, vai atlasītajiem moduļiem. Ņemiet vērā, ka tādā gadījumā automātiski tiks pievienoti šādi metadati: ierakstu tabulas, uzskaitījumi un paplašinātie datu tipi. Ja ir nepieciešami papildu metadatu tipi, tie ir jāpievieno manuāli. 
 
Mums ir daži ar ārējās tirdzniecības transakcijām saistīti metadati, kuri tika iegūti, atlasot metadatu vienumus manuāli. 
  
6.    Noklikšķiniet uz **Pievienot datu avotu**. 
7.    Noklikšķiniet uz **Tabulas ieraksti**. 
8.    Izmantojiet ātro filtru, lai filtrētu pēc lauka **Nosaukums** ar vērtību “Intrastat”. 
9.    Atlasiet **Intrastat** tabulas ierakstu. 
10.    Noklikšķiniet uz **Labi**.
  
Mēs pievienojām metadatu informāciju par Intrastat ierakstu tabulu. 
  
11.    Koka struktūrā izvērsiet zaru **Tabulas ieraksti Intrastat**\>**Relācijas**. 
12.    Koka struktūrā atlasiet **Tabulas ieraksti Intrastat**\>**Relācijas\IntrastatCommodity (Tabulas ieraksti EcoResCategory)**.     
13.    Noklikšķiniet uz **Pievienot metadatus**. 
  
> [!NOTE]
> Metadati par nepieciešamajām relācijām atlasītajai ierakstu tabulai ir jāpievieno manuāli. 
  
16.    Noklikšķiniet uz **Pievienot datu avotu**. 
17.    Noklikšķiniet uz **Uzskaitījums**. 
18.    Izmantojiet ātro filtru, lai filtrētu pēc lauka **Nosaukums** ar vērtību “IntrastatDirection”. 
19.    Atlasiet uzskaitījuma ierakstu **IntrastatDirection**. 
20.    Noklikšķiniet uz **Labi**. 
21.    Noklikšķiniet uz **Saglabāt**.  
22.    Aizveriet lapu. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Metadatu konfigurācijas melnraksta versijas pabeigšana
1.    Noklikšķiniet uz **Mainīt statusu**. 
2.    Noklikšķiniet uz **Pabeigt**. 
3.    Noklikšķiniet uz **Labi**. 
4.    Atlasiet **1**. pabeigto versiju. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Pabeigtās metadatu konfigurācijas versijas eksportēšana no programmas XML faila veidā
1.    Noklikšķiniet uz **Maiņa**. 
2.    Noklikšķiniet uz **Eksportēt kā XML failu**. 
3.    Noklikšķiniet uz **Labi**. 
    
Izveidotā ER metadatu konfigurācija ir saglabāta kā XML fails, kuru var importēt pakalpojumā RCS un izmantot kā avotu informācijai par metadatiem ārējās tirdzniecības uzņēmējdarbības jomai. Balstoties uz šo informāciju, mēs varam norādīt kartējumu starp programmas metadatiem un ER datu modeli.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]