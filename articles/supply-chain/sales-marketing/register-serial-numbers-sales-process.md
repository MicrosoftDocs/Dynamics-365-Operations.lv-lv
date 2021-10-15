---
title: Darbs ar sērijas krājumiem
description: Šajā tēmā ir paskaidrots, kā pārdošanas procesa laikā varat reģistrēt sērijas numurus iepakojuma pavadzīmēs vai rēķinos. Šo darbību var izmantot, ja uzņēmums vēlas reģistrēt sērijas numurus pakalpojumu un garantijas nodrošināšanas nolūkos, bet nevēlas saglabāt krājumu sērijas numurus no saņemšanas līdz izsniegšanas brīdim.
author: Henrikan
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e53ec57a8d5c5c922f580219e4bde5338d0707
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571693"
---
# <a name="working-with-serialized-items"></a>Darbs ar sērijas krājumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pārdošanas procesa laikā varat reģistrēt sērijas numurus iepakojuma pavadzīmēs vai rēķinos. Šo darbību var izmantot, ja uzņēmums vēlas reģistrēt sērijas numurus pakalpojumu un garantijas nodrošināšanas nolūkos, bet nevēlas saglabāt krājumu sērijas numurus no saņemšanas līdz izsniegšanas brīdim.

Daudzi uzņēmumi vēlaties tikai reģistrēt sērijas numurus pakalpojumu un garantijas nodrošināšanas nolūkos, un tiem nav jāglabā visu krājumu sērijas numuri no saņemšanas līdz izsniegšanas brīdim. Šādos scenārijos varat reģistrēt sērijas numurus pavadzīmēs vai rēķinos, kad tiek pārdotas preces. Ja preces vēlāk tiek atgrieztas, varat atrast katras preces rēķinu, lai noteiktu, vai jūs esat preces pārdevējs un vai ir spēkā pakalpojumu sniegšanas vai garantijas saistības.

Ir jāiespējo sērijas numuru izmantošana pārdošanas procesā, atlasot opciju **Aktīvs pārdošanas procesā** lapā **Izsekošanas dimensiju grupas**. Pēc tam Supply Chain Management parādās šādi notikumi:
-   Kopsavilkuma cilnē **Sērijas numuri** tiek atlasīta opcija **Sērijas numura kontrole**. Ja ir atlasīta šī opcija, katram krājumam pavadzīmē vai rēķinā ir jāreģistrē viens sērijas numurs.
-   Tiek atcelta visu izsekošanas dimensijas grupas sērijas numuru opciju atlase, izņemot opciju **Tukša izejas plūsma atļauta**. Varat atlasīt opciju **Tukša izejas plūsma atļauta**, lai ignorētu sērijas numuru kontroli un atļautu preču iepakošanu un iekļaušanu rēķinā, nereģistrējot sērijas numurus.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Kad reģistrēt sērijas numurus pārdošanas procesa laikā?
Varat reģistrēt sērijas numurus pārdošanas pasūtījuma pavadzīmē vai rēķinā. Sagatavojot rēķinu par serializētu krājumu, kas ir nosūtīts kopā ar pavadzīmi, varat izvēlēties, kurus no pavadzīmē norādītajiem sērijas numuriem iekļaut rēķinā. Reģistrēto sērijas numuru skaits nedrīkst pārsniegt nosūtīto krājumu daudzumu. Ja veidojat daļēju rēķinu, varat izvēlēties mazāku serializētu krājumu skaitu, nekā ir reģistrēts pavadzīmē. Drukājot pavadzīmi vai rēķinu, tiek iekļauti reģistrētie sērijas numuri.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Vai sērijas numurus var ievadīt skenējot, vai tie ir jāieraksta?
Varat skenēt vai ierakstīt sērijas numurus. Ja izmantojat skeneri, no skenēšanas režīma ir atkarīgs tas, vai sērijas numuri tiek pievienoti rēķinā vai pavadzīmē iekļauto sērijas numuru sarakstam vai tiek noņemti no tā. Ja vēlaties skenēt sērijas numurus, izmantojot, piemēram, rokas svītrkoda skeneri, konfigurējiet skeneri tā, lai pēc sērijas numura tiktu nosūtīta komanda Enter vai TAB. Šī komanda norāda datplūsmas beigas. Pretējā gadījumā pēc katra sērijas numura skenēšanas ir jānospiež tastatūras taustiņš Enter vai TAB.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Ja ir iespējota sērijas numuru izmantošana pārdošanas procesā, vai ir jāreģistrē visu krājumu sērijas numuri?
Tas, vai ir jāreģistrē visu pavadzīmē vai rēķinā iekļauto krājumu sērijas numuri, ir atkarīgs no precei piešķirtās izsekošanas dimensiju grupas iestatījumiem. Kad iespējojat sērijas numuru izmantošanu pārdošanas procesā, tiek automātiski atlasīta opcija **Sērijas numura kontrole**. Pēc tam ir jāreģistrē viens sērijas numurs vai tukšs nenolasāma numura ieraksts atbilstoši katram pavadzīmē vai rēķinā iekļautajam krājumam. Ja nevēlaties, lai katram krājumam būtu nepieciešams sērijas numurs, krājumam piešķirtajā izsekošanas dimensiju grupā atlasiet opciju **Tukša izejas plūsma atļauta**. Pēc tam varat reģistrēt sērijas numuru skaitu, kas ir mazāks par nosūtīto krājumu daudzumu. Ja reģistrēto sērijas numuru skaits ir lielāks par nosūtīto krājumu daudzumu, pavadzīmi vai rēķinu nevar grāmatot.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Vai var reģistrēt sērijas numurus daļējiem rēķiniem un piegādēm pa daļām?
Varat izveidot pārdošanas pasūtījumu daļējus rēķinus un pavadzīmes un reģistrēt tikai to krājumu sērijas numurus, kas ir iekļauti šajos rēķinos un pavadzīmēs. Ja vēlaties izveidot daļēju rēķinu un pastāv vairākas pārdošanas pasūtījuma pavadzīmes, varat iekļaut sērijas numurus no vairākām pavadzīmēm. Taču varat izveidot tikai vienu pavadzīmi, kurā nav iekļauti visi sērijas numuri. Piemēram, ja ir trīs pavadzīmes un katrā no tām ir iekļauti divi serializēti krājumi, nevarat izveidot daļēju rēķinu par vienu krājumu no katras pavadzīmes.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Ko darīt, ja sērijas numuru nevar nolasīt?
Ja sērijas numuru nevar nolasīt vai ieskenēt, varat krājumam izveidot tukšu rindu, noklikšķinot uz **Nav lasāms** lapā **Sērijas numuri**. Ja vēlāk sērijas numurs kļūst pieejams, varat atjaunināt rēķinu vai pavadzīmi. Plašāku informāciju skatiet nākamajā sadaļā “Vai varu labot vai mainīt pārdošanas pasūtījumam reģistrētos sērijas numurus?”

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Vai var labot vai mainīt pārdošanas pasūtījumam reģistrētos sērijas numurus?
Jā, varat labot sērijas numurus, ja ir izpildīti tālāk norādītie nosacījumi.
-   **Rēķini** — varat mainīt to krājumu sērijas numurus, kas vēl nav iekļauti rēķinos. Pēc tam tiek atjaunināta arī pavadzīme. Taču, ja pārdošanas pasūtījuma rinda ir labota, reģistrējot negatīvu daudzumu, nevarat mainīt šis pārdošanas pasūtījuma rindas sērijas numurus.
-   **Pavadzīmes** - nevarat daļēji labot pavadzīmes rindu, kurā ir ietverti serializēti krājumi. Ir jāatsauc pilnais rindas daudzums. Ja pavadzīme ir atcelta vai labota, atsauktie sērijas numuri nav atkārtoti jāreģistrē, izveidojot jaunu pavadzīmi tiem pašiem serializētajiem krājumiem. Tiks izmantoti jau reģistrētie numuri.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Vai varu skatīt sērijas numurus, kas tika nosūtīti kopā ar noteiktu pavadzīmi vai tika iekļauti rēķinā?
Jā, pavadzīmju žurnāla vai rēķinu žurnāla rindā var palaist vaicājumu, lai apskatītu sarakstu ar visiem dokumentā iekļautajiem sērijas numuriem.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Vai var skatīt manā rīcībā esošos serializētos krājumus?
Nē, nevarat skatīt jūsu rīcībā esošos serializētos krājumus jo krājumu sērijas numuri netiek reģistrēti līdz krājumu pārdošanas brīdim.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Vai var reģistrēt pieļaujamā svara krājumu sērijas numurus?
Nē, pārdošanas procesa laikā nevarat reģistrēt pieļaujamā svara krājumu sērijas numurus. Turklāt, ja prece ir iestatīta kā pieļaujamā svara krājums, šo preci nevarat piešķirt izsekošanas dimensiju grupai, kas ir iestatīta sērijas numuru izmantošanai tikai pārdošanas procesa laikā.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Vai varu reģistrēt sērijas numurus mazumtirdzniecības POS?

Jā, lietotājam ir jāievada sērijas numurs mazumtirdzniecības pārdošanas punktā (POS), kad lietotājs pārdod krājumu, kas ir piešķirts izsekošanas dimensiju grupai, kas ir iestatīta sērijas numuru izmantošanai tikai pārdošanas procesa laikā.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Kādas drošības lomas ir nepieciešamas, lai varētu reģistrēt sērijas numurus pārdošanas procesa laikā?
Šī funkcionalitāte ir pieejama visām lomām, kas var pārvaldīt pārdošanas pavadzīmes un pārdošanas rēķinus. Tālāk norādītie pienākumi ļauj darbiniekiem labot sērijas numurus un reģistrēt tukšus ierakstus tad, ja sērijas numurus nevar nolasīt vai noskenēt.
-   Uzturēt sērijas numuru labojumu
-   Uzturēt nenolasāmo sērijas numuru reģistrāciju







[!INCLUDE[footer-include](../../includes/footer-banner.md)]