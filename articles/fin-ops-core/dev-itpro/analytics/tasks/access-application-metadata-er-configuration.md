---
title: Piekļuve programmas metadatiem, izmantojot ER konfigurāciju
description: Šajā tēmā tiek skaidrots, kā Regulatoru configuration service (RCS) lietotājs var izveidot jaunu Elektroniskā pārskata (ER) kartēšanu, izmantojot metadatus.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093309"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Piekļuve programmas metadatiem, izmantojot ER konfigurāciju

[!include [banner](../../includes/banner.md)]

Nākamajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var noformēt jauna elektronisko pārskatu (Electronic reporting — ER) modeļa kartēšanu, izmantojot programmas metadatus. Programmas metadatiem jāpiekļūst, izmantojot ER metadatu konfigurāciju, kas ietver metadatu paraugu kopu, lai piekļūtu ārējās tirdzniecības transakcijām. Lai izpildītu tālāk norādītās darbības, vispirms pakalpojumā RCS izpildiet darbības, kas ir aprakstītas procedūras tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). Pēc tam izpildiet darbības, kas ir aprakstītas tēmā [Programmas metadatu sagatavošana lietošanai pakalpojumā RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Priekšnosacījumi
1. Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**. 
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Metadatu konfigurācijas importēšana 
1. Noklikšķiniet uz **Metadatu konfigurācijas**. 
2. Importējiet ER metadatu konfigurāciju, kas ir konfigurēta elektronisku dokumentu ģenerēšanai ārējās tirdzniecības uzņēmējdarbībai. Šī ER metadatu konfigurācija ir eksportēta kā XML fails, un procedūras [Programmas metadatu sagatavošana lietošanai pakalpojumā RCS](prepare-application-metadata-rcs.md) darbības ir izpildītas. 
3. Noklikšķiniet uz **Maiņa**. 
4. Noklikšķiniet uz **Ielādēt no XML faila**. 
5. Noklikšķiniet uz **Pārlūkot** un atlasiet failu 'Ārējās tirdzniecības metadati.xml'. 
6. Noklikšķiniet uz **Labi**. 
7. Aizvērt lapu. 

## <a name="create-data-model-configuration"></a>Datu modeļa konfigurācijas izveide
1. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**. 
2. Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. 
3. Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības modelis”. 
4. Klikšķiniet **Izveidot konfigurāciju**. 
5. Noklikšķiniet uz **Veidotājs**. 
6. Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu. 
7. Laukā **Nosaukums** ierakstiet “Sakne”. 
8. Noklikšķiniet uz **Pievienot**. 
9. Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu. 
10.    Laukā **Nosaukums** ierakstiet “Transakcija”. 
11.    Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**. 
12.    Noklikšķiniet uz **Pievienot**. 
13.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu. 
14.    Laukā **Nosaukums** ierakstiet “Preces kods”. 
15.    Laukā **Vienuma veids** atlasiet **Virkne**. 
16.    Noklikšķiniet uz **Pievienot**. 
17.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu. 
18.    Laukā **Nosaukums** ierakstiet “Rēķinā iekļautā summa”. 
19.    Laukā **Vienuma veids** atlasiet **Reāls**. 
20.    Noklikšķiniet uz **Pievienot**. 
21.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu. 
22.    Laukā **Nosaukums** ierakstiet “Datums”. 
23.    Laukā **Vienuma veids** atlasiet **Datums**. 
24.    Noklikšķiniet uz **Pievienot**. 
25.    Noklikšķiniet uz **Saknes atsauce**. 
26.    Noklikšķiniet uz **Labi**. 
27.    Noklikšķiniet uz **Saglabāt**. 
28.    Aizvērt lapu. 
29.    Noklikšķiniet uz **Mainīt statusu**. 
30.    Noklikšķiniet uz **Pabeigt**. 
31.    Noklikšķiniet uz **Labi**. 

## <a name="create-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas izveide 
1. Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. 
2. Laukā **Jauns** ievadiet “Uz datu modeli Ārējās tirdzniecības modelis balstīta modeļa kartēšana”. 
3. Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības kartēšana”. 
4. Klikšķiniet **Izveidot konfigurāciju**. 
5. Izvērsiet sadaļu **Priekšnosacījumi**. 
6. Noklikšķiniet uz **Rediģēt**. 
7. Klikšķiniet **Jauns**. 
8. Sarakstā atzīmējiet atlasīto rindu. 
9. Laukā **Priekšnosacījuma komponenta veids** atlasiet **Konfigurācija**. 
10.    Atlasiet konfigurāciju **Ārējās tirdzniecības metadati**. 
11.    Noklikšķiniet uz **Saglabāt**. 
12.    Tika pievienota atsauce uz konfigurācijas 'Ārējās tirdzniecības metadati' 1. versiju. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati. 
13.    Aizvērt lapu. 
14.    Noklikšķiniet uz **Veidotājs**. 
15.    Noklikšķiniet uz **Veidotājs**. 
16.    Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**. 
17.    Noklikšķiniet uz **Pievienot sakni**. 
18.    Laukā **Nosaukums** ierakstiet “Intrastat”. 
19.    Atlasiet **Intrastat** tabulas ierakstus. 
20.    Noklikšķiniet uz **Labi**. 

> [!NOTE]
> Tika piedāvātas tikai 2 tabulas, jo tikai 2 tabulas bija pievienotas pašlaik izmantotajai metadatu kopai. 

21.    Noklikšķiniet uz **Saistīt**. 
22.    Kokā izvērsiet sadaļu **Intrastat**. 
23.    Kokā atlasiet **Intrastat\AmountMST**. 
24.    Kokā izvērsiet sadaļu **Transakcija = Intrastat**. 
25.    Kokā atlasiet **Transakcija = Intrastat\Rēķinā iekļautā summa**. 
26.    Noklikšķiniet uz **Saistīt**. 
27.    Kokā atlasiet **Intrastat\TransDate**. 
28.    Kokā atlasiet **Transakcija = Intrastat\Datums**. 
29.    Noklikšķiniet uz **Saistīt**. 
30.    Kokā izvērsiet sadaļu **Intrastat\>Relācijas**. 
31.    Kokā izvērsiet sadaļu **Intrastat\>Relācijas\IntrastatCommodity**. 
32.    Kokā atlasiet **Intrastat\>Relācijas\IntrastatCommodity\Kods**. 
33.    Kokā atlasiet **Transakcija = Intrastat\Preces kods**. 
34.    Noklikšķiniet uz **Saistīt**. 
35.    Noklikšķiniet uz **Validēt**. 

> [!NOTE]
> Datu modeļa elementi ir veiksmīgi saistīti ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par programmas metadatiem no atsauces ER metadatu konfigurācijas. 
36.    Noklikšķiniet uz **Saglabāt**. 
37.    Aizvērt lapu. 
38.    Aizvērt lapu. 
39.    Ja nepieciešams, varat paplašināt esošo metadatu kopu un pēc tam eksportēt jauno ER metadatu konfigurācijas versiju. Pēc tam varat importēt to uz RCS un atjaunināt konfigurētā modeļa kartēšanas konfigurācijas priekšnosacījumus, kas attiecas uz jaunu importēto metadatu konfigurācijas versiju. 

> [!NOTE]
> Šāds veids, kā iegūt informāciju par programmas metadatiem, ir vienīgais pieejamais lokāli izvietotajām programmām (kad risinājumā tiek izmantots vietējas biznesa datu (LBD) izvietošanas vai lokālas izvietošanas modelis).
        
