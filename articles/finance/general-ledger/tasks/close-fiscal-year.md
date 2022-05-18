---
title: Finanšu gada slēgšana
description: Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu.
author: aprilolson
ms.date: 07/11/2019
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
ms.openlocfilehash: 8eb36cb856d191d64561060e7de4a1f9fd947882
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717479"
---
# <a name="close-the-fiscal-year"></a>Finanšu gada slēgšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu.


## <a name="validate-year-end-close-parameters"></a>Apstiprināt gada beigu slēgšanas parametrus
1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Virsgrāmatas iestatīšana > Virsgrāmatas parametri**.
2. Izvērsiet sadaļu **Finanšu gada slēgšana**.
3. Atlasiet **Jā** vai **Nē** gada **slēgšanas darbību dzēšanai pārsūtīšanas opcijas** laikā.
    
Ja finanšu gads jau ir slēgts, un gada beigu slēgšana tiek palaista vēlreiz, šis iestatījums ir svarīgs. Ja iestatījums ir **Jā, iepriekšējā gada beigu slēgšanas dokuments tiks dzēsts, un visiem kontiem** tiks izveidots jauns dokuments. Ja iestatījums **ir Nē**, iepriekšējais dokuments paliks un jaunais dokuments tiks izveidots tikai to ierakstu pielāgošanai, kas grāmatoti pēc pēdējās gada beigu slēgšanas.

4. Atlasiet **Jā** vai **Nē**, lai pārsūtīšanas **laikā izveidotu slēguma** darbības.

Ja iestatīts **kā Jā**, tiek izveidotas divas darbības. Finanšu gadā, kas tiek noslēgts, ir izveidots viens dokuments, lai visu Virsgrāmatas kontu bilances samazinātu līdz nullei, un nākamais finanšu gads sākuma bilancēm tiek izveidots otrs dokuments. Ja iestatījums **ir** Nē, nākamajā finanšu gadā sākuma bilancēm tiek izveidots viens dokuments.  

5. Lai **iestatītu** finanšu gada **statusu** uz **neatgriezeniski slēgtu opciju, atlasiet Jā vai** Nē.

Ja iestatīts kā **Jā**, finanšu gada statuss tiks iestatīts uz Neatgriezeniski slēgts. Tā kā neatgriezeniski slēgtu gadu vairs nevar atvērt, ieteicams iestatīt šo opciju uz **Nē**.  

6. Atlasiet **Jā** vai **Nē** dokumenta **numuram gada beigu slēgšanas** opcijas laikā.

Ja iestatījums **ir** Jā, dokumenta numurs jāievada manuāli gada beigu slēgšanas procesa laikā. Numuru sērija netiek izmantota, lai ģenerētu šo dokumenta numuru. Vislabākā prakse ir to iestatīt uz **Jā**.  

7. Aizvērt lapu.
8. Pārejiet uz sadaļu **Virsgrāmata > Perioda noslēgšana > Gada beigu slēgšana**.
9. Noklikšķiniet uz **Jauns**, lai izveidotu gada beigu slēgšanas veidni.

Veidni var izveidot juridisku personu grupai, kurai vēlaties palaist gada beigu slēgšanu. Šo veidni var izmantot atkārtoti katru gadu.  

10. Laukā **Grupas** nosaukums ievadiet gada beigu veidnes slēgšanas nosaukumu.
11. Laukā **Finanšu kalendārs** atlasiet finanšu gadu, kuram veidne tiks izveidota.

Tikai juridiskas personas, kas izmanto vienā finanšu gadu, var sagrupēt gada beigu slēgšanas veidnē. Tas ir tāpēc, ka gada beigu slēgšana tiek veikta, izvēloties finanšu gadu, nevis datumu.  

12. **Darbību rūtī** noklikšķiniet uz **Saglabāt**.
13. Sadaļā **Juridiskās personas** noklikšķiniet uz **Pievienot**, lai atlasītu šīs veidnes juridiskās personas.
    
Juridiskās personas var pievienot, atlasot juridiskās personas vai atlasot organizācijas hierarhiju. Tiks pievienotas tikai juridiskās personas ar organizācijas hierarhiju, ar atlasītu to pašu finanšu kalendāru.  

14. Atlasiet juridiskās personas vai organizācijas hierarhiju.
15. Noklikšķiniet uz **Labi**.
16. Pārsūtiet **bilances** **dimensiju** Jā **vai Nē**.

Vislabākā prakse ir iestatīt šo opciju kā Jā **bilances** kontiem. Tas saglabās grāmatoto darbību finanšu dimensijas, veidojot bilances kontu sākuma atlikumus. Peļņas un zaudējumu kontiem varat izvēlēties saglabāt finanšu dimensijas (**Aizvērt** visas), ja bilances tiek pārvietotas uz Nesadalītā peļņa, vai atlasīt, lai finanšu dimensijas aizstātu ar citu dimensijas vērtību (**Aizvērt vienu**). Ja izvēlaties **Aizvērt vienu**, katrai dimensijai varat definēt noteiktu dimensijas vērtību vai arī atstāt to tukšu.  

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
