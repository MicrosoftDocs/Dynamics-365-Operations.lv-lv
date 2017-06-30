---
title: "Pamatlīdzekļu integrācija"
description: "Pamatlīdzekļus var integrēt ar Virsgrāmatu, krājumu vadību, debitoriem un kreditoriem. Varat arī uzstādīt, lai pamatlīdzekļi integrētos ar pirkšanas pasūtījumiem."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 305010c41aa87222c652f98e6aa2b097606052e8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-assets-integration"></a>Pamatlīdzekļu integrācija

[!include[banner](../includes/banner.md)]


Pamatlīdzekļus var integrēt ar Virsgrāmatu, krājumu vadību, debitoriem un kreditoriem. Varat arī uzstādīt, lai pamatlīdzekļi integrētos ar pirkšanas pasūtījumiem.

<a name="general-ledger"></a>Virsgrāmata
--------------

Virsgrāmatā visu pamatlīdzekļu vērtība parasti tiek apkopota vairākos galvenajos kontos, kas nepieciešami finanšu pārskatiem. Taču lapā **Pamatlīdzekļi** varat izveidot daudzus pamatlīdzekļu ierakstus. Šie ieraksti var ietvert tādu informāciju kā pirkšanas cena, nolietojums un vērtējums. Katru reizi grāmatojot pamatlīdzekļa darbību, tiek atjaunināti attiecīgie galvenie konti. Pamatlīdzekļu galvenie konti vienmēr rāda atjauninātu pamatlīdzekļu vērtību.

Lapā **Pamatlīdzekļu grāmatošanas metodes** varat definēt galvenos kontus, kur tiek grāmatotas pamatlīdzekļu grāmatas darbības. Varat arī norādīt pamatlīdzekļu darbību veidus, kas tiek grāmatoti katrā galvenajā kontā. Varat izveidot dažādas pamatlīdzekļu galvenos kontu kombinācijas atkarībā no detaļu līmeņa, kādu vēlaties pamatlīdzekļiem Virsgrāmatā. Galvenos kontus var balstīt uz darbību veidiem, grāmatām un citiem galvenajiem kontiem.

## <a name="inventory-management"></a>Krājumu vadība
Pamatlīdzekļu krājumu žurnālos varat ievadīt to pamatlīdzekļu iegādi, ko juridiskā persona pati ir izstrādājusi vai izveidojusi. Pēc tam varat pārsūtīt krājuma vienības uz pamatlīdzekļiem kā iegādi vai daļu no iegādes. 

Pamatlīdzekļus varat arī iegādāties, lietojot pirkšanas pasūtījumus. Ja pirkšanas pasūtījumi satur krājumu vienības, kas ir norādītas kā pamatlīdzekļi, opcijas **Atļaut līdzekļu iegādi no Pirkšanas** iestatījums lapā **Pamatlīdzekļu parametri** nosaka, vai rēķina grāmatošanas laikā tiek grāmatota pamatlīdzekļa iegāde. Pamatlīdzekļu iegādes ietekme uz krājumiem ir atkarīga no juridiskās personas iestatījumiem. 

Kad krājuma vienība kļūst par pamatlīdzekļu iegādi krājumu žurnālā, pirkšanas pasūtījumā vai iegādes piedāvājumā, tiek izveidota pamatlīdzekļu grāmatas iegādes darbība. Ja grāmatas iegādē ir iekļauta atvasināta grāmata, tiks izveidota arī atvasinātās grāmatas iegādes darbība. 

Grāmatošanas kārtulas, kas ir iestatītas moduļa Krājumu vadība lapā **Grāmatošana**, kontrolē krājumu samazinājumu iegādes grāmatošanas laikā. Taču ne vienmēr krājumi samazinās, kad grāmatojat ar pamatlīdzekļiem saistītus rēķinus. Dažos gadījumos pamatlīdzekļi var tikt iegādāti iekšējai lietošanai. Piemēram, pārdošanas departamentam tiek iegādāts klēpjdators. Kad strādājat ar pirkšanas pasūtījumiem, varat izmantot vienības, kuras ir noteiktas gan tālākpārdošanai, gan iekšējai lietošanai. 

Ja izmantojat konkrētus saņemšanas un izdošanas plūsmas kontus krājumu grupu pamatlīdzekļiem, varat izmantot tās pašas krājumu vienības gan iekšējiem pirkumiem, gan tālākpārdošanas krājumiem. 

Pamatlīdzekļi, kas ir paredzēti iekšējai lietošanai, tiek iestatīti tā, lai to konta vieds būtu **Pamatlīdzekļa saņemšana**. Šo konta veidu lieto, lai izsekotu pamatlīdzekļa saņemšanai. Grāmatojot kreditora rēķinu, izmantojot pamatlīdzekļa saņemšanas kontu, ja kāds no tālāk minētajiem nosacījumiem ir patiess.

-   Rēķina rinda ietver esošu pamatlīdzekli, kas ir paredzēts iekšējiem nolūkiem.
-   Grāmatotās produktu ieejas plūsmas rindā ir atzīmēta izvēles rūtiņa **Jauns pamatlīdzeklis?**.
-   Kreditora rēķina rindā ir atzīmēta izvēles rūtiņa **Izveidojiet jaunu pamatlīdzekli**.

Parasti šis konts ir izdevumu konts. Varat iestatīt krājumu grupas vai atsevišķa krājuma konta veidu **Pamatlīdzekļa saņemšana**, izmantojot cilni **Pirkšanas pasūtījums** lapā **Krājumu grupa** vai **Grāmatošana**.

Līdzīgā veidā pamatlīdzekļi, kas ir paredzēti iekšējai lietošanai, var tikt iestatīti tā, lai to konta veids būtu **Pamatlīdzekļa izdošana**. Šo konta veidu lieto, lai izsekotu pamatlīdzekļa izdošanai saņēmējam. Pamatlīdzekļa izdošanas konts darbojas kā atlīdzība attiecībā uz pamatlīdzekļa debeta kontu, kad līdzeklis tiek iegādāts, izmantojot pirkšanas pasūtījumu. Līdzekļa iegāde var tikt grāmatota, kad iegrāmatojat kreditora rēķinu vai kad iegrāmatojat līdzekļa iegādi pamatlīdzekļu žurnālā, iespējams, izmantojot iegādes priekšlikumu. Varat iestatīt krājumu grupas vai atsevišķa krājuma konta veidu **Pamatlīdzekļa izdošana**, izmantojot cilni **Krājumi** lapā **Krājumu grupa** vai **Krājumu grāmatošana**. 

Galvenos kontus, kas tiek izmantoti grāmatošanai, nosaka pēc Virsgrāmatas integrācijas opcijām, kas ir norādītas krājuma modeļu grupai. Turklāt galvenie konti, kas tiek izmantoti, atšķiras atkarībā no tā, vai līdzeklis ir piesaistīts pirkšanas pasūtījuma rindai. Konti tiek atvasināti no katras krājumu grupas grāmatošanas metodes. 
**Piezīme.** Grāmatojot preču saņemšanu, ja eksistē krājumu rezervācija, rindā nav iespējams piešķirt vai izveidot pamatlīdzekli. 

Konti, kuriem pamatlīdzekļu darbības tiek grāmatotas, ir atkarīgi no diviem faktoriem: no tā, vai pamatlīdzekļi ir pirkti vai juridiskās personas izveidoti, kā arī no pamatlīdzekļa darbības veida. 

Darbības tips sasaista pamatlīdzekļos krājuma darbību ar grāmatošanas metodi. Tā kā grāmatošanas metode pamatlīdzekļos definē, kuri konti tiek atjaunināti, pamatlīdzekļa darbības veida atlase netieši ir arī galveno kontu atlase, kuriem darbība tiek grāmatota. Gan izveidoto, gan iegādāto pamatlīdzekļu darbību veids parasti ir **Iegāde** vai **Iegādes korekcija**.

## <a name="accounts-receivable"></a>Debitoru parādi
Pamatlīdzekļu integrācija ar kreditoriem izmanto grāmatošanas metodes, kas ir iestatītas pamatlīdzekļos. Šīs grāmatošanas metodes tiek aktivizētas, ja debitora rēķinam ir atlasīts pamatlīdzeklis, grāmata un pamatlīdzekļu darbības veids pirms debitora rēķina grāmatošanas. Tā kā pamatlīdzekļi nav ietverti modulī Krājumu vadība, pārdodot pamatlīdzekli, ir jāizmanto lapa **Brīva teksta rēķins**. 

Ja grāmatā ir iekļauta atvasināta grāmata, atvasinātās grāmatas darbība tiek izveidota, grāmatojot debitora rēķinu.

## <a name="accounts-payable"></a>Kreditoru parādi
Parasti pamatlīdzekļi tiek iegādāti no ārējiem kreditoriem. Varat izmantot lapu **Pamatlīdzekļu parametri**, lai norādītu, vai vienmēr ir jāgrāmato līdzekļa iegāde, kad tiek grāmatoti kreditora rēķini, vai līdzekļa iegādi var grāmatot tikai modulī Pamatlīdzekļi. Ja iespējojat līdzekļu iegādes grāmatošanu no kreditoriem, pamatlīdzekļi tiek atjaunināti vienmēr, kad tiek grāmatots kreditora rēķins par pamatlīdzekļa iegādi. 

Ja ir uzstādīta līdzekļu iegādes grāmatošana tad, kad tiek grāmatots rēķins, darbība tiek iegrāmatota atbilstoši pamatlīdzekļu grāmatošanas metodēm dažādiem pamatlīdzekļu darbību tipiem. Grāmatošana ir atkarīga no pamatlīdzekļa, grāmatas un pamatlīdzekļa transakcijas veida, kas ir atlasīti lapā **Pirkšanas pasūtījums** pirms kreditora rēķina grāmatošanas. 

Ja grāmatā ir iekļauta atvasināta grāmata, atvasinātās grāmatas darbība tiek izveidota, grāmatojot kreditora rēķinu.

Katras pasūtījuma rindas integrācija tiek aktivizēta lapas **Pirkšanas pasūtījums** kopsavilkuma cilnes **Detalizēta informācija par rindu** cilnē **Pamatlīdzekļi**. Pamatlīdzekļa pirkšanas pasūtījumu varat nosūtīt kreditoram. Tomēr pamatlīdzekļi un galvenie konti tiek atjaunināti tikai tad, kad grāmatojat kreditora rēķinu pēc pamatlīdzekļa saņemšanas. Tā kā pirkšanas pasūtījumos var būt iekļautas tikai krājumu vienības, pamatlīdzekļu iegādes ietekme uz krājumiem ir atkarīga no juridiskās personas iestatījumiem.

## <a name="project-management-and-accounting"></a>Projektu vadība un uzskaite
Jūs varat projektu piesaistīti līdzekli, kas ietekmē projektu. Jūs varat arī piesaistīt katru posmu, uzdevumu vai apakšprojektu dažādiem līdzekļiem. Viens pamatlīdzeklis var būt saistīts ar katru projekta ierakstu. Jūs veidojat saistību, kad ievadāt pamatlīdzekļa numuru lapas **Projekti** laukā **Pamatlīdzekļa numurs**. Projekta veidam ir jābūt **Iekšējs** vai **Izmaksu projekts**. 

Varat arī izmantot lapu **Projekti**, lai skatītu detalizētu informāciju par līdzekļiem, kas ir saistīti ar projektiem. Ja vēlaties skatīt pamatlīdzekļa ierakstu, noklikšķiniet uz līdzekļa saites kopsavilkuma cilnē **Iestatīšana**, lai atvērtu lapu **Pamatlīdzekļi**. Pēc tam noklikšķiniet uz **Projekti** &gt; **Visi projekti**, lai skatītu projektus, kas ir saistīti ar pamatlīdzekli. 

Parasti pamatlīdzekļi tiek saistīti ar projektiem, ja projekti ir saistīti ar darbu, apkopi vai līdzekļu uzlabošanu. Kad projekts ir pabeigts, līdzekļa vērtības palielināšana netiek veikta automātiski. Tāpēc, ja ir nepieciešama vērtības palielināšana, tā jāveic manuāli. 

Lai dzēstu saistību starp projektu un līdzekli, notīriet lauku **Pamatlīdzekļa numurs** lapā **Projekti**. 

Varat arī norādīt pamatlīdzekli, ko izveidojat vai ražojat kā daļu no paredzētā projekta. Paredzēta projekta beigās, varat automātiski iegrāmatot līdzekļa ieguves darbību.

Papildinformāciju skatiet tēmā [Līdzekļu iegādāšanās, izmantojot iepirkuma procesu](acquire-assets-procurement.md)




