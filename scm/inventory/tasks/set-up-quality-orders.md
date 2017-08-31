--- 
title: "Kvalitātes pasūtījumu iestatīšana"
description: "Šajā procedūrā parādīts, kā iespējot kvalitātes pārvaldības procesu, kurā ienākošie krājumi ir jāpārbauda uzreiz pēc saņemšanas reģistrācijas."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 0bd8bc73a3cbb42cb7e6d42a07d58c0b02673ba1
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-quality-orders"></a>Kvalitātes pasūtījumu iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iespējot kvalitātes pārvaldības procesu, kurā ienākošie krājumi ir jāpārbauda uzreiz pēc saņemšanas reģistrācijas. Procedūru parasti veic kvalitātes pārvaldītājs. Process ietver kvalitātes grupas izveidi, lai definētu krājumus, kuriem būs jāveic paraugu ņemšana, un testa grupas izveidi, lai grupētu testus, kas jāveic kvalitātes grupas krājumiem. Šo ceļvedi varat palaist demonstrācijas datu uzņēmumā USMF.


## <a name="enable-quality-management"></a>Iespējot kvalitātes pārvaldību
1. Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Kvalitātes pārvaldība.
3. Opcijai Izmantot kvalitātes pārvaldību iestatiet Jā.
4. Noklikšķiniet uz Pārskatu iestatījums.
    * Uzņēmumā USMF kvalitātes pārvaldības pārskata iestatījumi jau ir definēti. Ja tas nebija izdarīts, varat šeit pievienot jaunas rindas dažādiem pārskatu tipiem, un atlasīt dokumentu tipu, kuru vēlaties lietot katram pārskatam.  
5. Aizvērt lapu.
6. Aizvērt lapu.

## <a name="create-a-test"></a>Testa izveide
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testi.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Tests.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Tips atlasiet Opcija.
    * Šajā piemērā atlasīsim „Opcija”, kas ļaus piešķirt testa rezultātus, ņemot vērā iepriekš definētās vērtības.  
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Testa mainīgo lielumu izveide, lai noteiktu to, kā tiek ierakstīti testa rezultāti
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testa mainīgie lielumi.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Mainīgais.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz Rezultāti.
7. Noklikšķiniet uz Jauns.
8. Ierakstiet vērtību laukā Rezultāts.
9. Apraksta laukā ierakstiet vērtību.
10. Laukā Rezultāta statuss atlasiet Veiksmīgs.
11. Noklikšķiniet uz Saglabāt.
12. Noklikšķiniet uz Jauns.
13. Ierakstiet vērtību laukā Rezultāts.
14. Apraksta laukā ierakstiet vērtību.
15. Noklikšķiniet uz Saglabāt.
16. Aizvērt lapu.
17. Aizvērt lapu.

## <a name="set-up-item-sampling"></a>Krājuma paraugu izveides iestatīšana
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Krājumu paraugu ņemšana.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Krājumu paraugu ņemšana.
4. Apraksta laukā ierakstiet vērtību.
5. Ievadiet skaitli laukā Vērtība.
    * Šī vērtība attiecas uz daudzuma specifikāciju, kas atlasīta blakus esošajā laukā.  
6. Izvērsiet vai sakļaujiet sadaļu Process.
7. Atzīmējiet izvēles rūtiņu Pilna bloķēšana vai noņemiet tās atzīmi.
    * Ja atlasāt šo opciju, neveiksmīga testa gadījumā tiek bloķēta visa partija vai pasūtījuma rindas daudzums. Ja tā netiek atlasīta, tiek bloķēti tikai krājumi kvalitātes pārbaudes pasūtījumā.  
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.

## <a name="create-a-quality-group"></a>Kvalitātes grupas izveide
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Kvalitātes grupas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Kvalitātes grupa.
    * Ierakstiet aprakstošu nosaukumu, kas palīdzētu noteikt, kāda veida krājumus grupa ietvers (paraugu atlases kritēriji).  
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. noklikšķiniet uz Pievienot preces.
7. Izvēlieties krājuma koda rindu.
    * Šajā piemērā filtrēšana tiks veikta pēc krājuma koda.  
8. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemēram, ierakstiet T*, lai atfiltrētu krājumu numurus, kas sākas ar burtu T.  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz OK.
11. Noklikšķiniet uz Krājumu kvalitātes grupas.
12. Aizvērt lapu.
13. Aizvērt lapu.

## <a name="create-a-test-group"></a>Testa grupas izveide
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testa grupas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Testa grupa.
    * Piešķiriet testa grupai nosaukumu, kas palīdzēs atcerēties, kāda veida testi tiek izmantoti un ar kuru kvalitātes grupu tai jābūt saistītai. Piemēram, ja tā ir jāizmanto ar kvalitātes grupu, kas atlasa krājumus, kuru identifikatori sākas ar "T", tās nosaukums varētu būt "T krājumu testi".  
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Krājumu paraugu ņemšana atlasiet krājumu paraugu ņemšanas rindu, kuru izveidojāt iepriekš.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Noklikšķiniet uz Pievienot.
8. Ievadiet skaitli laukā Secības numurs.
9. Laukā Tests atlasiet iepriekš izveidoto testu.
10. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
11. Noklikšķiniet uz cilnes Tests.
12. Laukā Mainīgais atlasiet iepriekš izveidoto mainīgo.
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Laukā Rezultāts pēc noklusējuma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
16. Noklikšķiniet uz Saglabāt.
17. Aizvērt lapu.

## <a name="define-when-quality-orders-will-be-created"></a>Kvalitātes pārbaudes pasūtījumu izveides definēšana
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Kvalitātes piesaistes.
2. Noklikšķiniet uz Jauns.
3. Atlasiet opciju laukā Atsauces tips.
4. Laukā Krājuma kods atlasiet Grupa.
    * Šajā piemērā tiks atlasīta "Grupa" un izmantota iepriekš izveidotā kvalitātes grupa. Var arī iestatīt "Tabula", lai norādītu krājumus manuāli, vai izvēlieties "Visi", lai kvalitātes pārbaudes pasūtījumam pievienotu visus krājumus.  
5. Laukā Krājums izvēlieties iepriekš izveidoto kvalitātes grupu.
    * Laukā Krājums pieejamās opcijas ir atkarīgas no tā, ko iestatāt laukā Krājuma kods.  
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Izvērsiet vai sakļaujiet sadaļu Process.
8. Atlasiet opciju laukā Notikuma tips.
    * Tas ir notikums, kas aktivizē testu. Šeit pieejamās opcijas ir atkarīgas no tā, kuri procesi atlasīti laukā Atsauces tips.  
9. Atlasiet opciju laukā Izpilde.
10. Izvērsiet vai sakļaujiet sadaļu Kvalitātes pārbaudes pasūtījuma process.
11. Laukā Notikumu aizturēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Šajā laukā parādīts procesu saraksts, kurus ir iespējams bloķēt, ja kvalitātes pasūtījums ir joprojām atvērts. Opcijas ir atkarīgas no tā, ko atlasījāt laukā Notikuma tips.  
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Tas būs atkarīgs no iepriekš atlasītajām vērtībām. Atlasiet, ja šie procesi ir jābloķē laikā, kad pastāv atvērti kvalitātes pārbaudes pasūtījumi, kas saistīti ar pamatdokumenta rindu.  
13. Izvērsiet vai sakļaujiet sadaļu Specifikācijas.
14. Laukā Testa grupa atlasiet iepriekš izveidoto grupu.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
16. Noklikšķiniet uz Saglabāt.
17. Aizvērt lapu.


