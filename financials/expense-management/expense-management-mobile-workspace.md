---
title: "Mobilā darbvieta Izdevumu pārvaldība"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Izdevumu pārvaldība, kas ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šajā darbvietā lietotāji var iegūt un augšupielādēt kvīti, ko vēlāk var pievienot izdevumu pārskatam. Mobilā darbvieta arī ļauj lietotājiem ātri izveidot izdevumu rindu, izmantojot pievienoto kvīti."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4e3202de8e5288bbd52e8c28922374de147cc99f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobilā darbvieta Izdevumu pārvaldība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par mobilo darbvietu Izdevumu pārvaldība, kas ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šajā darbvietā lietotāji var iegūt un augšupielādēt kvīti, ko vēlāk var pievienot izdevumu pārskatam. Mobilā darbvieta arī ļauj lietotājiem ātri izveidot izdevumu rindu, izmantojot pievienoto kvīti.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Pārskats par mobilo darbvietu Izdevumu pārvaldība
---------------------------------------------------

Daudzos uzņēmumos komandējuma vai lietišķo izdevumu pārskatam, ko darbinieks iesniedz atmaksāšanai, jāpievieno kvīts kopija. Mobilā darbvieta **Izdevumu pārvaldība** ļauj lietotājiem ātri izveidot jaunas izdevumu rindas mobilajā ierīcē, izmantojot pievienoto kvīts fotoattēlu. Lietotāji var arī tvert kvīts fotoattēlu un pēc tam to pievienot izdevumu pārskatam. Mobilo darbvietu **Izdevumu pārvaldība** lietotāji var izmantot tālāk norādīto darbību veikšanai.

-   Uzņemt kvīts fotoattēlu un augšupielādēt to programmā Microsoft Dynamics 365 for Operations. Lietotājs šo fotoattēlu vēlāk var pievienot izdevumu pārskatam.
-   Augšupielādēt failu kā uzņemtu kvīti. Lietotājs šo failu vēlāk var pievienot izdevumu pārskatam.
-   Izveidot jaunu izdevumu rindu, izmantojot pievienoto kvīti. Vēlāk lietotājs var pievienot izdevumu pārskatam rindas krājumu un iesniegt to apstiprināšanai un atmaksāšanai.

Pārējās šīs tēmas sadāļās ir paskaidrots, kā ieviest un izmantot mobilo darbvietu **Izdevumu pārvaldība**.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu ieviest mobilo darbvietu **Izdevumu pārvaldība**, pārliecinieties, vai sistēmas administrators ir izpildījis tālāk minētos priekšnosacījumus.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnosacījums</th>
<th>Loma</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jābūt ieviestai Microsoft Dynamics 365 for Operation versijai 1611 ar 3. vai jaunāku platformas atjauninājumu.</td>
<td>Sistēmas administrators</td>
<td>Ja programma Dynamics 365 for Operations vēl nav izvietota jūsu organizācijā, jūsu sistēmas administratoram vajadzētu izlasīt rakstu <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations izvietošana demonstrācijas vidē</a>.</td>
</tr>
<tr class="even">
<td>Jāievieš KB 4019015.</td>
<td>Sistēmas administrators</td>
<td>KB 4019015 (X++ atjauninājums vai metadatu labojumfails) satur četras mobilās darbvietas piegāžu ķēdžu pārvaldībai. Lai ieviestu KB 401901, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li>Jālejupielādē KB 4019015 no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Jāizveido izvietojama pakotne</a>, kas ietver modeli <strong>ApplicationSuite</strong> un <strong>ExpenseMobile</strong>, un pēc tam izvietojamā pakotne jāaugšupielādē pakalpojumā LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Lietojiet šo izvietojamo pakotni</a> savai Dynamics 365 for Operations sistēmai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilā darbvieta <strong>Izdevumu pārvaldība</strong> ir jāpublicē Dynamics 365 for Operations mobilajā programmā.</td>
<td>Sistēmas administrators</td>
<td><ol>
<li>Palaidiet pārlūkprogrammā programmu Dynamics 365 for Operations.</li>
<li>Lapā <strong>Sistēmas parametri</strong> atlasiet <strong>Mobilo darbvietu pārvaldība</strong>.</li>
<li>Atlasiet darbvietu <strong>Izdevumu pārvaldība</strong>.</li>
<li>Noklikšķiniet uz <strong>Publicēt mobilo darbvietu</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobilās programmas lejupielāde un instalēšana
Mobilo programmu veikalā lejupielādējiet Dynamics 365 for Operations mobilo programmu un instalējiet to.

-   Operētājsistēmai Android: [Dynamics 365 for Operations Google Play veikalā](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Operētājsistēmai iPhone: [Dynamics 365 for Operations iTunes programmu veikalā](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Pierakstīšanās Dynamics 365 for Operations mobilajā programmā
1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet Dynamics 365 for Operations URL.
3.  Ievadiet uzņēmumu, kurā pierakstīties. Ievadiet, piemēram, **USMF**.
4.  Pirmajā pierakstīšanās reizē ir jāievada Microsoft Dynamics 365 for Operations konta lietotājvārds un parole. Ievadiet savus akreditācijas datus.
5.  Pēc pierakstīšanās ir redzamas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā! Ja sistēmas administrators jaunu darbvietu publicēs vēlāk, varat vilkt, lai atsvaidzinātu mobilo darbvietu sarakstu. 

[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kvīts tveršana, izmantojot mobilo darbvietu Izdevumu pārvaldība
1.  Mobilajā ierīcē atlasiet darbvietu **Izdevumu pārvaldība**.
2.  Atlasiet **Tvert kvīti**.
3.  Atlasiet **Uzņemt fotoattēlu** vai **Izvēlēties attēlu**.
4.  Ja atlasījāt **Uzņemt fotoattēlu**, rīkojieties kā aprakstīts tālāk.
    1.  Kvīts fotoattēli jāuzņem, izmantojot mobilās ierīces kameru. Kad fotoattēls ir uzņemts, noklikšķiniet uz **Labi**, lai to apstiprinātu.
    2.  Nav obligāti: ievadiet fotoattēlu nosaukumu un jebkādas piezīmes.

     **Vai:** ja atlasījāt **Izvēlēties attēlu**, veiciet tālāk norādītās darbības.
    1.  Šajā sarakstā atlasiet attēlu.
    2.  Nav obligāti: ievadiet attēla nosaukumu un jebkādas piezīmes.

5.  Atlasiet **Gatavs**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Ātra izdevumu ievadīšana, izmantojot mobilo darbvietu Izdevumu pārvaldība
1.  Mobilajā ierīcē atlasiet darbvietu **Izdevumu pārvaldība**.
2.  Atlasiet **Ātra izdevumu ievade**.
3.  Atlasiet izdevumu kategoriju. Tiek parādīts to izdevumu kategoriju saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma var tikt ielādētas ne vairāk par 50 krājumu vienībām, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform). Ja vajadzīgā kategorija nav ietverta sarakstā, atlasiet vienumu **Meklēt**, lai veiktu tiešsaistes meklēšanu programmatūrā Dynamics 365 for Operations. Meklējiet pēc izdevumu kategorijas vai pārslēdzieties uz meklēšanu pēc izdevumu veida.
4.  Ievadiet izdevuma darījuma datumu.
5.  Nav obligāti: ievadiet izdevumu komersanta nosaukumu.
6.  Ievadiet izdevumu summu.
7.  Atlasiet izdevumu valūtu. Tiek parādīts to valūtas kodu saraksts, kas ir ielādēti programmā lietošanai bezsaistes režīmā. Pēc noklusējuma var tikt ielādēts ne vairāk par 400 valūtu nosaukumiem, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform). Ja vajadzīgā valūta nav ietverta sarakstā, atlasiet vienumu **Meklēt**, lai veiktu tiešsaistes meklēšanu programmatūrā Dynamics 365 for Operations. Meklējiet pēc valūtas vai pārslēdzieties uz meklēšanu pēc nosaukuma.
8.  Atlasiet **Uzņemt fotoattēlu** vai **Izvēlēties attēlu**.
9.  Ja atlasījāt **Uzņemt fotoattēlu**, kvīts fotoattēli jāuzņem, izmantojot mobilās ierīces kameru. Kad fotoattēls ir uzņemts, noklikšķiniet uz **Labi**, lai to apstiprinātu.  Ja atlasījāt **Izvēlēties attēlu**, sarakstā atlasiet attēlu.
10. Atlasiet **Gatavs**.






