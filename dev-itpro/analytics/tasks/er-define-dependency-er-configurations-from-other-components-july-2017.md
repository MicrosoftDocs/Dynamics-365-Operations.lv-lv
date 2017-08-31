--- 
title: "Definēt konfigurāciju atkarību no citiem komponentiem elektronisko pārskatu veidošanai"
description: "Lai veiktu šīs darbības, vispirms jāveic darbības uzdevuma ceļvedī \"ER: pārvaldīt modeļa kartēšanas konfigurācijas\", un jums ir nepieciešama piekļuve pakalpojumam Microsoft Dynamics Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: be601efd857a0d57210680adcb0b0a1f17ca2f27
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="define-the-dependency-of-configurations-from-othcomponents-for-electronic-reporting-er"></a>Definēt konfigurāciju atkarību no citiem komponentiem elektronisko pārskatu veidošanai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Lai veiktu šīs darbības, vispirms jāveic darbības uzdevuma ceļvedī "ER: pārvaldīt modeļa kartēšanas konfigurācijas", un jums ir nepieciešama piekļuve pakalpojumam Microsoft Dynamics Lifecycle Services (LCS).

Šajā procedūrā ir parādīts, kā izstrādāt elektronisko pārskatu veidošanas (ER) konfigurāciju un norādīt tās atkarību no citiem programmatūras komponentiem, lai varētu nodrošināt, ka konfigurācija ir pareizi lejupielādēta konkrētai Microsoft Dynamics 365 for Finance and Operations Enterprise edition versijai. Šajā piemērā jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos. 

1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
    * Pārliecinieties, vai konfigurācijas koks satur konfigurāciju "Sample data model" un pakārtojiet vienumus. Pretējā gadījumā veiciet darbības, kas norādītas uzdevuma ceļvedī "ER: pārvaldīt modeļa kartēšanas konfigurācijas", un pēc tam vēlreiz startējiet šo ceļvedi.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>ER konfigurāciju atkarības no citiem komponentiem definēšana
1. Kokā izvērsiet "Sample data model".
2. Kokā atlasiet "Sample data modelSample mapping".
    * Mēs atlasījām modeļa kartējuma konfigurācijas "Sample mapping" melnraksta versiju. Tagad definēsim tā atkarību no citiem programmatūras komponentiem. Šis solis tiek uzskatīts par priekšnoteikumu, lai kontrolētu šīs konfigurācijas versijas lejupielādi no ER repozitorija un jebkādu turpmāku šīs versijas izmantošanu.   
3. Izvērsiet priekšnoteikumu sadaļu.
    * Ievērojiet, ka šajā posmā priekšnoteikumu grupa “Implementations” ir pievienota automātiski. Šī grupa satur nepieciešamo komponentu, kas attiecas uz datu modeļa konfigurāciju un kuram ir ieslēgts ieviešanas karodziņš. Šis karodziņš norāda, ka kartējuma konfigurācija "Sample mapping" tiek uzskatīta par datu modeļa "Sample data model" ieviešanu. Šis komponents liks ER lejupielādēt kartējuma konfigurāciju "Sample mapping" no ER repozitorija vienmēr, kad tiks lejupielādēta modeļa konfigurācija "Sample data model".   
4. Noklikšķiniet uz Rediģēt.
    * Konfigurācijas pašreizējās versijas atsevišķu atkarību no programmatūras komponenta var norādīt, izmantojot komponenta veida definīciju un vai nu komponenta versiju vai komponenta versiju diapazonu.  
    * Vēlamās atkarības var sagrupēt. Kad ir atlasīts grupēšanas veids "All of", šīs grupas atkarības nosacījums tiek uzskatīts par izpildītu, ja ir izpildīts katrs šīs grupas un pakārtotās grupas atkarības nosacījums. Kad ir atlasīts grupēšanas veids "One of", šīs grupas atkarības nosacījums tiek uzskatīts par izpildītu, ja ir izpildīts vismaz viens šīs grupas atkarības nosacījums.   
5. Noklikšķiniet uz Jauns.
6. Atlasiet komponentu Preces priekšnosacījums.
7. Atlasiet Microsoft Dynamics 365 for Operations (1611).
8. Laukā Versija ierakstiet "[7.1.1541.3036,8)".
    * [7.1.1541.3036,8)  
    * Ievadītās atkarības tiek novērtētas, kad šī konfigurācija ir lejupielādēta no ER repozitorija. Šī konfigurācijas versija tiks lejupielādēta no ER repozitorija, kad parauga datu modeļa konfigurācijas 1. versija ir vai nu jau instalēta vai lejupielādēta iepriekš. Ja tā ir lejupielādēta iepriekš, tai ir jābūt pabeigtai Finance and Operations versijā ne vecākā par 7.1.1541.3036 vai jaunākā, bet ne jaunākā par galveno versiju 8.   
9. Noklikšķiniet uz Saglabāt.
10. Aizvērt lapu.
11. Noklikšķiniet uz Mainīt statusu.
12. Noklikšķiniet uz Pabeigt.
13. Noklikšķiniet uz OK.
14. Kokā atlasiet "Sample data model\Sample mapping (alternative)".
15. Noklikšķiniet uz Rediģēt.
16. Noklikšķiniet uz Jauns.
17. Atlasiet komponentu Preces priekšnosacījums.
18. Atlasiet Microsoft Dynamics AX 7.0 RTW.
19. Laukā Versija ierakstiet "[7.0.1265.3015,7.1)".
    * [7.0.1265.3015,7.1)  
    * Atkarības tiek novērtētas, kad šī konfigurācija ir lejupielādēta no ER repozitorija. Šī konfigurācijas versija tiks lejupielādēta no ER repozitorija, kad parauga datu modeļa konfigurācijas 1. versija ir vai nu jau instalēta vai lejupielādēta iepriekš. Ja tā ir lejupielādēta iepriekš, tai ir jābūt pabeigtai Microsoft Dynamics 365 for Finance and Operations Enterprise versijā ne vecākā par 7.1.1541.3036 vai jaunākā, bet ne jaunākā par papildversiju 1.   
20. Noklikšķiniet uz Saglabāt.
21. Aizvērt lapu.
22. Noklikšķiniet uz Mainīt statusu.
23. Noklikšķiniet uz Pabeigt.
24. Noklikšķiniet uz OK.

## <a name="configure-the-er-repository"></a>ER repozitorija konfigurēšana
1. Aizvērt lapu.
2. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Atveriet sarakstu ar ER repozitorijiem, kas paredzēti pašreizējam ER nodrošinātājam, Litware, Inc.  
3. Sarakstā atzīmējiet atlasīto rindu.
4. Noklikšķiniet uz Repozitoriji.
5. Noklikšķiniet uz Rādīt filtrus.
6. Laukā "Type name" ievadiet "LCS" filtra vērtību, izmantojot filtra operatoru "contains".
    * Ja LCS repozitorijs jau ir reģistrēts pašreizējam ER nodrošinātājam, varat izlaist šī apakšuzdevuma atlikušos soļus. Ja LCS repozitorijs vēl nav reģistrēts, izpildiet atlikušos soļus.   
7. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
8. Laukā Konfigurācijas repozitorija veids ievadiet "LCS".
9. Noklikšķiniet uz Izveidot repozitoriju.
10. Laukā Projekts ievadiet vai atlasiet kādu vērtību.
    * Atlasiet vēlamo LCS projektu no meklēšanas lauka "Project".  
11. Noklikšķiniet uz OK.
12. Aizvērt lapu.

## <a name="upload-configurations-to-lcs"></a>Konfigurāciju augšupielāde pakalpojumā LCS
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
2. Kokā atlasiet "Sample data model".
3. Atlasiet šīs konfigurācijas pabeigto versiju.
4. Noklikšķiniet uz Mainīt statusu.
5. Noklikšķiniet uz Koplietot.
6. Noklikšķiniet uz OK.
    * Šīs modeļa konfigurācijas 1. versija ir augšupielādēta LCS, izmantojot LCS projektu ER repozitorijam, kas tika iepriekš konfigurēts.   
7. Kokā izvērsiet "Sample data model".
8. Kokā atlasiet "Sample data modelSample mapping".
9. Atlasiet šīs konfigurācijas pabeigto versiju.
10. Noklikšķiniet uz Mainīt statusu.
11. Noklikšķiniet uz Koplietot.
12. Noklikšķiniet uz OK.
    * Šīs modeļa kartējuma konfigurācijas 1.1 versija ir augšupielādēta LCS, izmantojot LCS projektu ER repozitorijam, kas tika iepriekš konfigurēts.   
13. Kokā atlasiet "Sample data model\Sample mapping (alternative)".
14. Atlasiet šīs konfigurācijas pabeigto versiju.
15. Noklikšķiniet uz Mainīt statusu.
16. Noklikšķiniet uz Koplietot.
17. Noklikšķiniet uz OK.
    * Šīs modeļa kartējuma konfigurācijas 1.1 versija ir augšupielādēta LCS, izmantojot LCS projektu ER repozitorijam, kas tika iepriekš konfigurēts.   

## <a name="evaluate-er-configuration-dependencies"></a>ER konfigurācijas atkarību novērtēšana
    * Mēs dzēsīsim izveidotās konfigurācijas no sistēmas un lejupielādēsim tās atpakaļ no LCS repozitorija.  
1. Kokā atlasiet "Sample data modelSample mapping".
2. Noklikšķiniet uz Dzēst.
3. Noklikšķiniet uz Jā.
4. Kokā atlasiet "Sample data model\Sample mapping (alternative)".
5. Noklikšķiniet uz Dzēst.
6. Noklikšķiniet uz Jā.
7. Kokā atlasiet "Sample data model\Sample format".
8. Noklikšķiniet uz Dzēst.
9. Noklikšķiniet uz Jā.
10. Kokā atlasiet "Sample data model".
11. Noklikšķiniet uz Dzēst.
12. Noklikšķiniet uz Jā.
13. Aizvērt lapu.
    * Atveriet sarakstu ar ER repozitorijiem, kas paredzēti pašreizējam ER nodrošinātājam, Litware, Inc.  
14. Noklikšķiniet uz Repozitoriji.
15. Noklikšķiniet uz Rādīt filtrus.
16. Laukā "Type name" ievadiet "LCS" filtra vērtību, izmantojot filtra operatoru "contains".
17. Noklikšķiniet uz Atvērt.
18. Kokā atlasiet "Sample data model".
    * Ņemiet vērā, ka varat skatīt novērtējumu par to, vai pašreizējā repozitorija katras ER konfigurācijas versijas priekšnosacījumi ir izpildīti. Lai skatītu šo novērtējumu, noklikšķiniet uz Pārbaudīt priekšnosacījumus.   
19. Nosklikšķiniet uz Pārbaudīt priekšnosacījumus.
20. Noklikšķiniet uz Importēt.
21. Noklikšķiniet uz Jā.
22. Aizvērt lapu.
23. Aizvērt lapu.
24. Aizvērt lapu.
25. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
26. Kokā izvērsiet "Sample data model".
    * Ņemiet vērā, ka kartējuma konfigurācija "Sample mapping" tika lejupielādēta kopā ar atlasīto datu modeļa konfigurāciju. Divi faili tika lejupielādēti kopā, jo "Sample mapping" ir definēts kā atlasītā datu modeļa ieviešana, un tas ir piemērojams risinājumam Finance and Operations. Konfigurācija "Sample mapping (alternative)" netika lejupielādēta, jo nosacījums nepieciešamajai programmas versijai nav izpildīts.   
    * Ja pierakstīsities Dynamics 365 for Finance and Operations Enterprise edition, reģistrēsit tādu pašu nodrošinātāju, piekļūsit tādam pašam LCS projektam un lejupielādēsit tādu pašu datu modeļa konfigurāciju, konfigurācija "Sample mapping (alternative)" tiks lejupielādēta, savukārt konfigurācija "Sample mapping" tiks izlaista.  


