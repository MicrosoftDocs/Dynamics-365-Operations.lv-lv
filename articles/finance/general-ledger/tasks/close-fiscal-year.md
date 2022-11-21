---
title: Finanšu gada slēgšana
description: Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779817"
---
# <a name="close-the-fiscal-year"></a>Finanšu gada slēgšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu.


## <a name="validate-year-end-close-parameters"></a>Apstiprināt gada beigu slēgšanas parametrus
1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Virsgrāmatas iestatīšana > Virsgrāmatas parametri**.
2. Izvērsiet sadaļu **Finanšu gada slēgšana**.
3. Atlasiet Jā vai Nē opcijai **Dzēst gada beigu transakcijas pārsūtīšanas** laikā.**·** **·**
    
Ja finanšu gads jau ir slēgts, un gada beigu slēgšana tiek palaista vēlreiz, šis iestatījums ir svarīgs. Ja iestatījums ir **Jā**, iepriekšējā gada beigu slēgšanas kupons tiks dzēsts un tiks izveidots jauns kupons visiem kontiem, kuros sākas atlikumi. Ja iestatījums ir **Nē**, iepriekšējais kupons paliks un jauns kupons tiks izveidots tikai, lai pielāgotu ierakstus, kas tika publicēti pēc pēdējā gada beigu slēgšanas.

4. Atlasiet **Jā** vai **Nē** opcijai Izveidot slēgšanas transakcijas pārsūtīšanas **laikā**.

Ja iestatījums ir **Jā**, tiek izveidotas divas transakcijas. Viens kupons tiek izveidots slēgtajā finanšu gadā, lai samazinātu visu Virsgrāmatas kontu atlikumus līdz nullei, un nākamajā finanšu gadā tiek izveidots otrs kupons sākuma bilancēm. Ja iestatīts uz **Nē**, nākamajā finanšu gadā tiek izveidots viens kupons sākuma bilancēm.  

5. **Opcijai** Iestatīt finanšu gada statusu uz pastāvīgi slēgtu **atlasiet Jā** vai **Nē**.

Ja iestatījums **ir Jā**, finanšu gada statuss tiks iestatīts uz **Pastāvīgi slēgts**. Tā kā pastāvīgi slēgtu gadu nevar atvērt no jauna, labākā prakse būtu iestatīt šo opciju uz **Nē**.  

6. Atlasiet **Jā (Yes) vai Nē (Yes**) vai Nē **(** **Document number ir jāaizpilda) gada beigu slēgšanas** opcijas laikā.

Ja iestatīts uz **Jā**, kupona numurs ir jāievada manuāli gada beigu slēgšanas procesā. Numuru sērija netiek izmantota, lai ģenerētu šo dokumenta numuru. Labākā prakse ir iestatīt to uz **Jā**.  

7. Aizvērt lapu.
8. Pārejiet uz sadaļu **Virsgrāmata > Perioda noslēgšana > Gada beigu slēgšana**.
9. Noklikšķiniet uz **Jauns**, lai izveidotu gada beigu slēgšanas veidni.

Veidni var izveidot juridisku personu grupai, kurai vēlaties palaist gada beigu slēgšanu. Šo veidni var izmantot atkārtoti katru gadu.  

10. Laukā **Grupas nosaukums** ievadiet gada beigu slēgšanas veidnes nosaukumu.
11. Laukā **Finanšu kalendārs** atlasiet finanšu gadu, kuram veidne tiks izveidota.

Tikai juridiskas personas, kas izmanto vienā finanšu gadu, var sagrupēt gada beigu slēgšanas veidnē. Tas ir tāpēc, ka gada beigu slēgšana tiek veikta, izvēloties finanšu gadu, nevis datumu.  

12. **Darbību rūtī** noklikšķiniet uz **Saglabāt**.
13. Sadaļā **Juridiskās personas** noklikšķiniet uz **Pievienot**, lai atlasītu šīs veidnes juridiskās personas.
    
Juridiskās personas var pievienot, atlasot juridiskās personas vai atlasot organizācijas hierarhiju. Tiks pievienotas tikai juridiskās personas ar organizācijas hierarhiju, ar atlasītu to pašu finanšu kalendāru.  

14. Atlasiet juridiskās personas vai organizācijas hierarhiju.
15. Noklikšķiniet uz **Labi**.
16. Atlasiet **Jā** vai **Nē** kategorijā **Pārskaitījuma** bilance.

Labākā prakse ir iestatīt šīs opcijas vērtību Jā **bilances** kontiem. Tas saglabās grāmatoto darbību finanšu dimensijas, veidojot bilances kontu sākuma atlikumus. Peļņas un zaudējumu kontiem varat atlasīt, lai uzturētu finanšu dimensijas (Aizvērt visu **), kad bilances tiek pārvietotas uz Nesadalīto peļņu, vai arī varat atlasīt, lai finanšu dimensijas tiktu aizstātas ar citu dimensijas vērtību (** **Aizvērt vienu**). Ja izvēlaties **Aizvērt vienu**, varat definēt konkrētu dimensijas vērtību katrai dimensijai vai pat izvēlēties to atstāt tukšu.  

17. Noklikšķiniet uz **Saglabāt**.
18. Sāciet gada beigu slēgšanu, **Darbību rūtī** izvēloties **Palaist finanšu slēgšanu**. Gada beigu slēgšana tiks veikta atlasītajai veidnei.  
19. Atlasiet visas vai juridisko personu apakškopu no veidnes, kurā vēlaties palaist gada beigu slēgšanu.

Pirmo reizi palaižot gada beigu slēgšanu, lai iegūtu sākuma bilances daļa organizāciju var izvēlēties veikt gada beigu slēgšanas visām juridiskajām personām veidnē. Ja pēc tam tiek veikti pielāgošanas ieraksti, jūs varat palaist gada beigu slēgšanu tikai juridiskām personām, kurām ir korekcijas.  

20. Noklikšķiniet uz **Labi**.
21. Atlasiet finanšu gadu, kuram vēlaties palaist gada beigu slēgšanu.
22. Laukā **Dokuments** ievadiet vērtību. Vislabākais veids ir iekļaut finanšu gada dokumenta numuru, lai būtu vieglāk atrast gada beigu slēgšanas dokumentu, kas tiek izveidots.  
23. Gada beigu slēgšanas noklusējumi, kas jāpalaiž paketē. Tas ir vislabākais veids, kā ilgstošus procesus palaist pakešveida režīmā. Tas parasti ir viens no šiem procesiem, tāpēc pēc noklusējuma nepieciešams izmantot pakešveida režīmu.  
24. Noklikšķiniet uz **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
