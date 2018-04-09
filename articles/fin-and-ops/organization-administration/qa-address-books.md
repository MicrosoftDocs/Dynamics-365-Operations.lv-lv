---
title: "Bieži uzdotie jautājumi par adrešu grāmatām"
description: "Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par adrešu grāmatām programmatūrā Microsoft Dynamics 365 for Finance and Operations."
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2d148b8bd4a2588d282a9077aa76997399693483
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="address-books-faq"></a>Bieži uzdotie jautājumi par adrešu grāmatām

[!include[banner](../includes/banner.md)]




<a name="how-do-i-check-for-duplicate-records"></a>Kā pārbaudīt, vai nav ierakstu dublikātu?
-------------------------------------

Pārbaudīt, vai nav ierakstu dublikātu, varat tieši no saraksta lapas **Globālā adrešu grāmata**. Darbību rūtī, cilnē **Puse**, grupā **Uzturēt** noklikšķiniet uz **Pārbaudīt, vai nav dublikātu**. Pēc tam atlasiet vērtības, ko iekļaut dublikātu pārbaudē.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Vai no adrešu grāmatas pušu ierakstus varu pievienot vai dzēst vairumā?
Jā, adrešu grāmatai varat pievienot vairākus pušu ierakstus, kā arī varat noņemt vairākus pušu ierakstus.

-   Lai adrešu grāmatai pievienotu vairāku pušu ierakstus, atlasiet šis puses saraksta lapā **Globālā adrešu grāmata**. Pēc tam darbību rūtī, cilnē **Puse**, grupā **Uzturēt** noklikšķiniet uz **Piešķirt puses**. Atlasiet adrešu grāmatas, kam pievienot atlasītos pušu ierakstus, un pēc tam noklikšķiniet uz **Labi**. Visi atlasītie pušu ieraksti tiek pievienoti jūsu atlasītajām adrešu grāmatām.
-   Lai no adrešu grāmatas noņemtu vairāku pušu ierakstus, atlasiet šis puses saraksta lapā **Globālā adrešu grāmata**. Pēc tam darbību rūtī, cilnē **Puse**, grupā **Uzturēt** noklikšķiniet uz **Noņemt puses**. Atlasiet adrešu grāmatas, no kurām šīs puses noņemt, un pēc tam noklikšķiniet uz **Labi**. Visi atlasītie pušu ieraksti tiek noņemti no jūsu atlasītajām adrešu grāmatām.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Vai varu mainīt ieraksta puses tipu, vai man ir jādzēš vecais ieraksts un jāizveido jauns?
Iespējams, reizēm ierakstu puses tips ir jāmaina no personas uz organizāciju vai no organizācijas uz personu. Piemēram, Nensija ir pārdošanas darba grupas dalībniece Fabrikam Lielbritānijā. Kādā Londonas tirdzniecības izstādē viņa satiek sešus jaunus potenciālos klientus. Nensija izveido potenciālā klienta puses ierakstu katram potenciālajam klientam. Kad Nensija saglabā šos ierakstus, katrs ieraksts tiek izveidots arī globālajā adrešu grāmatā. Fabrikam noklusējuma puses tips ir iestatīts uz organizāciju, bet diviem no jaunajiem perspektīvajiem klientiem ir nepieciešams personas ieraksta tips. Tādēļ, kad Nensija atgriežas no tirdzniecības izstādes, viņai ir jāmaina šo abu potenciālo klientu ierakstu puses tips. Lai puses ierakstu no viena puses tipa mainītu uz citu, vispirms jums globālajā adrešu grāmatā ir jāizveido jauns puses ieraksts ar pareizo tipu. Pēc tam veco puses ierakstu saistiet ar šo jauno ierakstu. Kad ir izveidota jaunā puses saistība, izdzēsiet sākotnējo puses ierakstu, kuram ir nepareizais ieraksta tips.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Kā mainīt puses ieraksta nosaukumu vai adresi?
Jebkurā laikā varat atjaunināt puses ieraksta nosaukumu, kā arī adreses, kas ir saistītas ar šo ierakstu.

-   Lai atjauninātu puses ieraksta nosaukumu, atveriet puses ierakstu un pēc tam darbību rūtī noklikšķiniet uz **Rediģēt**. Kopsavilkuma cilnē **Vispārīgi** ievadiet puses jauno nosaukumu un pēc tam saglabājiet ierakstu.
-   Lai puses ierakstam atjauninātu adresi, atveriet puses ierakstu un pēc tam kopsavilkuma cilnē **Adreses** atlasiet adresi, kuru vēlaties atjaunināt. Noklikšķiniet uz **Rediģēt** un pēc tam lapā **Rediģēt adresi** veiciet adreses vai adreses parametru nepieciešamās izmaiņas.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Vai divus vai vairākus pušu ierakstus var sapludināt vienā ierakstā?
Laiku pa laikam, iespējams, divu vai vairāku pušu ierakstus ir nepieciešams sapludināt vienā ierakstā. Tas var notikt, ja ar nolūku vai netīšām izveidojat vienu vai vairākus puses ierakstu dublējumus. Kad sapludināt pušu ierakstus, jums ir jāatlasa viens ieraksts, ko paturēt. Pēc tam informācija no pārējiem ierakstiem tiek sapludināta šajā ierakstā. Piemēram, jūs konstatējat, ka informācija par Fabrikam ir saglabāta trīs pušu ierakstos: A, B un C. Jūs izlemjat paturēt puses ierakstu A. Tāpēc informācija, kas glabājas puses ierakstos B un C tiks sapludināta puses ierakstā A. Pastāv noteiktas situācijas, kad pušu ierakstus nevarat sapludināt:

-   Nevar sapludināt pušu ierakstus, kas ir saistīti ar to pašu puses lomu, piemēram, debitoru vai kreditoru, tajā pašā juridiskajā personā. Piemēram, puse A ir saistīta ar juridiskās personas 123 debitoru, bet puse B ir saistīta ar citu juridiskās personas 123 debitoru. Šos pušu ierakstus nevar sapludināt, jo veicot sapludināšanu iegūtais puses ieraksts ir saistīts ar vairākiem vienas juridiskās personas debitoriem un tas nav atļauts. Taču ierakstus var sapludināt, ja puse B ir saistīta ar kreditoru juridiskajā personā 123 vai ar debitoru citā juridiskajā personā.
-   Nevar sapludināt iekšējos puses organizatoriskos ierakstus tajā pašā juridiskajā personā, darba grupā vai pārvaldības struktūrvienībā.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Vai man ir jāizveido puses ieraksts globālajā adrešu grāmatā vai citā vietā, piemēram, lapā Debitors vai Kreditors?
Pušu ierakstus varat ievadīt globālajā adrešu grāmatā vai atbilstošajā elementa lapā. Kad ierakstu pievienojat vienā atrašanās vietā, tas pats ieraksts vienmēr tiek pievienots otrai atrašanās vietai. Piemēram, ja kādam debitoram puses ierakstu pievienojat globālajā adrešu grāmatā, šis ieraksts tiek pievienotas arī lapā **Debitors**. Tāpat, ja kādam debitoram puses ierakstu pievienojat lapā **Debitors**, šis ieraksts tiek pievienots arī globālajā adrešu grāmatā. Lai izlemtu, kur ievadīt jaunus pušu ierakstus, izmantojiet tālāk sniegtās vadlīnijas.

-   **Puses ieraksta izveidošana, kad nezināt elementa tipu** — ja ir jāizveido puses ieraksts, bet jūs nezināt elementa tipu (piemēram, jūs nezināt, vai šis elements ir debitors vai iespēja), izveidojiet ierakstu globālajā adrešu grāmatā. Elementa tipu varat atlasīt vēlāk.
-   **Puses ieraksta izveidošana, kad zināt elementa tipu** — ja zināt puses elementa tipu, ierakstu varat izveidot šim tipam atbilstošajā lapā. Piemēram, izveidot ierakstu debitoram lapā **Debitors**. Kad ierakstu izveidojat un saglabājat, izmantojot atbilstošo elementa lapu, šis ieraksts automātiski tiek izveidots globālajā adrešu grāmatā.

## <a name="can-i-translate-address-information-for-party-records"></a>Vai varu tulkot adreses informāciju pušu ierakstiem?
Varat iestatīt adreses informācijas tulkojumus, lai programmatūrā Microsoft Dynamics 365 for Finance and Operations informācija būtu redzama jūsu lietotāja valodā (sistēmas valodā), bet dokumentos, piemēram, pārdošanas pasūtījumos, būtu redzama citā valodā. Varat ievadīt tulkojumus valstu/reģionu nosaukumiem, adreses nolūkiem un nosaukumu/vārdu secībām. Piemēram, jūsu sistēmas valoda ir Dāņu, un jūs izveidojat pārdošanas pasūtījumu kādam debitoram Francijā. Šajā gadījumā programmā debitora ierakstu varat skatīt dāņu valodā, adreses informāciju drukātajā pārdošanas pasūtījumā varat rādīt franču valodā. Kad iestatāt tulkojumus, tulkojums jums ir jāievada katram vienumam sarakstā. Katrs vienums, kam neievadāt tulkojumu, tiks rādīts sistēmas valodā. Piemēram, jūsu sistēmas valoda ir Dāņu, un jūs sūtāt dokumentu debitoram Spānijā. Ja adreses informācijai neesat ievadījis tulkojumus Spāņu (ESP), šī informācija tiks rādīta dāņu valodā gan programmā, gan izdrukātajā dokumentā.




