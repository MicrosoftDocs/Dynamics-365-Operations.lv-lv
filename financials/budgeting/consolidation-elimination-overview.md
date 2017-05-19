---
title: "Konsolidēšanas un koriģēšanas pārskats"
description: "Šajā rakstā ir sniegta vispārīga informācija par konsolidēšanas un koriģēšanas procesu. Tajā ir atbildes uz dažiem bieži uzdotiem jautājumiem."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7ea83b349e5c4ab187cc06cf4df38ac15ea02a7d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="consolidation-and-elimination-overview"></a>Konsolidēšanas un koriģēšanas pārskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta vispārīga informācija par konsolidēšanas un koriģēšanas procesu. Tajā ir atbildes uz dažiem bieži uzdotiem jautājumiem.

Izmantojot konsolidācijas funkcionalitāti, finanšu rezultāti no vairākiem apakšuzņēmumiem tiek kombinēti vienā apvienotā uzņēmumā. Apakšuzņēmumi var būt dažādās versijās vai sistēmās, tie var pilnībā nepiederēt un tie var izmantot dažādas valūtas. Ir vairākas opcijas datu konsolidēšanai.

-   **Konsolidēt tiešsaistē** — šī opcija konsolidē ikdienas bilances pēc atlasītajiem kontiem un dimensijām un saglabā tās konsolidētajā uzņēmumā.
-   **Finanšu pārskati** — šī opcija iespējo transakciju un bilanču konsolidāciju un var tikt veikta jebkurā laikā. Iespējams izveidot vairākus hierarhiju līmeņus un iespējams apskatīt vairākas pārskatu valūtas.
-   **Konsolidēt ar importēšanu** — šī opcija importē bilances konsolidētajā uzņēmumā.
-   **Eksportēt uzņēmumu bilances** — šī opcija veido uzņēmumu bilanču eksporta failu. Pēc tam failu var importēt uz citām instancēm vai sistēmām. Finanšu pārskatu veidošanu var arī izmantot, lai eksportētu bilances uz Microsoft Excel failu.

Par korekcijām var ziņot vairākos veidos.

-   Korekcijas kārtulas var iestatīt sistēmā un pēc tam apstrādāt konsolidācijas procesa laikā vai izmantojot korekcijas priekšlikumu. Kārtulas var grāmatot jebkurā uzņēmumā, kuram juridiskās personas uzstādījumos ir atlasīts vienums **Lietot finanšu korekciju procesā**.
-   Lai manuāli noteiktu un iegrāmatotu korekcijas transakcijas, var izveidot un lietot atsevišķu uzņēmumu. Šis uzņēmums var tikt izmantots konsolidācijas procesā vai finanšu atskaitēs.
-   Konti un finanšu dimensijas, kas tiek izmantoti, lai noteiktu starpuzņēmumu darbības, var tikt atfiltrēti finanšu pārskatu rindu definīcijās vai kolonu definīcijās, un ir iespējams izmantot pilnas detalizācijas iespējas. Aprēķinātā kolonna vai rinda pēc tam var tikt izmantota, lai noņemtu kontus un finanšu dimensijas no konsolidētās kopsummas.

Ir daudz konsolidācijas scenāriju, un katra metode var apstrādāt šos scenārijus dažādos veidos.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
1.  Es labprātāk grāmatoju korekcijas datu bāzē. Kādas ir manas iespējas?

Ir vairākas iespējas. Varat izmantot opciju **Konsolidēt tiešsaistē** un iekļaut korekcijas procesa laikā vai kā priekšlikumu. Transakcijas tiks grāmatotas konsolidētajā uzņēmumā. Alternatīvi varat izveidot atsevišķu uzņēmumu, kurā manuāli izveidosiet korekcijas, un pēc tam izmantosit attiecīgo uzņēmumu finanšu pārskatos vai konsolidācijas procesā.

2.  Konsolidētie rezultāti ir nepieciešami vairākās pārskatu veidošanas valūtās.

Opcijai **Finanšu pārskati** ir neierobežots pārskata valūtu skaits. Datus pārrēķina pārskata ģenerēšanas laikā, pamatojoties uz maiņas kursa tipu un valūtas pārrēķina metodi, kas ir iestatīta galvenajam kontam. Tā kā opcijai **Konsolidēt tiešsaistē** ir tikai viena pārskatu veidošanas valūta, katrai pārskata valūtai ir nepieciešams konsolidētais uzņēmums, ja izmantojat šo opciju. Opcija **Finanšu pārskati** ir ieteicamā metode.

3.  Vēlos apskatīt transakciju līmeņa informāciju katram uzņēmumam.

Opcija **Finanšu pārskati** ir risinājums, jo transakciju līmeņa informāciju iespējams apskatīt tik uzņēmumiem, cik ir iekļauti pārskata koka definīcijā.

4.  Izmantojam budžeta plānošanu vai budžeta kontroli, un tā ir jākonsolidē.
Opcija **Finanšu pārskati** ir risinājums, lai konsolidētu budžeta plānošanas vai budžeta kontroles datus.

5.  Mūsu apakšuzņēmumi ir izplatīti visā pasaulē, un mums ir vairākas kontu diagrammas. Kāda ir labākā metode mūsu datu konsolidēšanai?

Kad jāstrādā ar vairākām kontu diagrammām, ir vairākas iespējas. Varat izmantot opciju **Konsolidēt tiešsaistē** un pēc tam izvēlēties izmantot vai nu konsolidācijas kontu, kas ir definēts galvenajam kontam, vai konsolidācijas kontu grupu. Varat izmantot arī opciju **Finanšu pārskati**, iekļaujot vairākas saites uz finanšu dimensijām rindas definīcijā un kartējot kontus.

6.  Mums nepieciešama konsolidācija vairākos līmeņos. Citiem vārdiem sakot, mēs vispirms konsolidējam visus mūsu Eiropas apakšuzņēmumus, konvertējot uz Lielbritānijas mārciņu (GBP). Pēc tam mēs strādājam ar šiem datiem un pārrēķinām konsolidēto summu uz ASV dolāriem. Kā mēs varam to izdarīt?

Ja nepieciešami vairāki konsolidācijas līmeņi un katrā līmenī tiek izmantota atšķirīga valūta, ir jāizmanto opcija **Konsolidēt tiešsaistē**. Ir jāizveido vairāki konsolidācijas uzņēmumi, kas savā starpā atšķiras ar uzskaites un pārskata valūtu. Pēc tam konsolidācija jāpalaiž vairākas reizes. Opcija **Finanšu pārskati** vienmēr pārrēķina no katra avota uzņēmuma uzskaites valūtas uz atlasīto valūtu.

7.  Mums ir apakšuzņēmumi, kas izmanto citu sistēmu. Kā mēs varam tos konsolidēt?

Izmantojiet opciju **Konsolidēt ar importēšanu**, lai pārnestu bilances uz konsolidēto uzņēmumu.

8.  Daži no mūsu apakšuzņēmumiem pilnībā mums nepieder. Kāda ir labākā metode to konsolidēšanai?

Pastāv vairākas iespējas daļēji piederošiem apakšuzņēmumiem. Izmantojot opciju **Finanšu pārskati**, varat definēt pārskata koka definīciju un īpašumtiesības. Varat arī izmantot aprēķināto rindu vai kolonnu, lai norādītu daļēji piederošu summu. Varat pat parādīt minoritātes procentu kā atsevišķu rindu pārskatā. Varat arī izmantot opciju **Konsolidēt tiešsaistē**. Cilnē **Juridiskās personas** ir kolonna **Īpašumtiesības**, kurā varat definēt procentuālo daļu, kas pieder mātes uzņēmumam.

9.  Mūsu organizācijai ir jāparāda konsolidācijas atbilstoši biznesa vienībai vai vēlas izmantot organizācijas hierarhijas.

Risinājums ir opcija **Finanšu pārskati**. Organizācijas hierarhijas, kurās ir juridiskās personas vai finanšu dimensijas, var tikt izmantotas finanšu pārskatos. Varat arī izveidot savas daudzlīmeņu hierarhijas, izmantojot pārskata koka definīciju, kurā ir juridisko personu un dimensiju vērtību kombinācija.

10. Mums ir vairāk nekā viena sistēmas instance.

Datus varat konsolidēt, izmantojot opciju **Eksportēt uzņēmuma bilances**, lai eksportētu no vienas instance, un pēc tam izmantojot opciju **Konsolidēt ar importēšanu** citā instancē.


Plašāku informāciju skatiet rakstā [Valūtas pārvērtēšana konsolidācijas uzņēmumā](..\general-ledger\currency-revaluation-consolidation-company.md).



