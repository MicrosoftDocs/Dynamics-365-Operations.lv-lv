---
title: "Pamatlīdzekļu grupu aizstāšanas izmaksu un apdrošinātās vērtību pārrēķināšana"
description: "Šajā rakstā ir paskaidrots, kā atjaunināt pamatlīdzekļu atjaunošanas izmaksas un apdrošinātās vērtības."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bd07a63c366a03718912f35b9b7ed21ae847828
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Pamatlīdzekļu grupu aizstāšanas izmaksu un apdrošinātās vērtību pārrēķināšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā atjaunināt pamatlīdzekļu atjaunošanas izmaksas un apdrošinātās vērtības.

Periodiski jums var paziņot, ka maksa par noteiktu pamatlīdzekļu atjaunošanu vai apdrošināšanu ir mainījusies. Piemēram, jūsu menedžeris var informēt jūs, ka pagājušajā gadā inflācija bija 3 %, tādēļ visu pamatlīdzekļu atjaunošanas izmaksas jums būs jāpaaugstina par 3 %. 

Kaut arī formā Fiksētās izmaksas var rediģēt atsevišķu pamatlīdzekļu aizstāšanas izmaksas un apdrošinātās vērtības, var izmantot arī formu Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana, lai atjauninātu šīs vērtības visai līdzekļu grupai vienlaicīgi. Šeit ir sniegta informācija par to, kā atjaunināt pamatlīdzekļu grupu vai atsevišķu grupu līdzekļu vērtības.

## <a name="how-values-are-updated"></a> Kā tiek atjauninātas vērtības
Lai pārrēķinātu pamatlīdzekļu grupu aizstāšanas izmaksas un apdrošinātās vērtības, vispirms jānorāda, par cik procentiem nomainīt pašreizējās aizstāšanas izmaksas un apdrošinātās vērtības, un tad var veikt periodisko atjaunināšanu, lai pārrēķinātu faktiskās vērtības. Procentuālo vērtību norādiet formas Pamatlīdzekļu grupas laukā Aizstāšanas izmaksu koeficients un Apdrošinātas vērtības koeficients. Kaut arī šie koeficienti tiek norādīti visai pamatlīdzekļu grupai, izmantojot formu Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana, var atlasīt aizstāšanas izmaksu un apdrošināto vērtību pārrēķināšanu tikai grupas noteiktiem pamatlīdzekļiem. 

Ja forma Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana tiek izmantota, lai pārrēķinātu pamatlīdzekļu atjaunošanas izmaksas un apdrošinātās vērtības, tiek izmantotas tālāk norādītās formulas.

-   \[(Līdzekļu grupas atjaunošanas izmaksu koeficients / 100) + 1\] \* līdzekļa pašreizējās atjaunošanas izmaksas
-   \[(Līdzekļu grupas apdrošināšanas summas koeficients / 100) + 1\] \* līdzekļa pašreizējā apdrošināšanas summa

> [!NOTE] 
> Ja tiek izmantota forma Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana, tiek atjauninātas gan atlasīto pamatlīdzekļu aizstāšanas izmaksas, gan apdrošinātās vērtības; nevar norādīt tikai vienas vērtības atjaunināšanu. Lai nemainītu vienu vērtību, bet atjauninātu otru, formā Pamatlīdzekļu grupas kā koeficientu ievadiet 0 (nulle). Ja koeficients ir nulle vai tukšs, tad aprēķins atjauninājumā tiek izlaists. Periodiskā atjaunināšana pamatlīdzekļu atlikušo vērtību un atlikušo neto vērtību neietekmē. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Kā lietot datumu, lai atlasītu atjaunināmos krājumus
Pēc noklusējuma atjaunināšanas procesa laikā tiek atjaunināti atlasītie pamatlīdzekļi, kas nav atjaunināti pašreizējā dienā, bet, iespējams, ka tie ir jau atjaunināti kādā no iepriekšējām dienām. Piemēram, &lt; pašreizējais datums nozīmē “pirms šodienas”. Varat mainīt datumu veidlapā Atjauniniet aizstāšanas izmaksas un apdrošinātās vērtības, noklikšķinot uz pogas Atlasīt. Norādītais datuma kritērijs tiek salīdzināts ar pamatlīdzekļa pēdējās periodiskās atjaunināšanas datumu (lauks Pēdējā periodiskās vērtības/izmaksu atjaunināšana formā Pamatlīdzekļi). Katru reizi sekmīgi atjauninot pamatlīdzekļa aizstāšanas izmaksas vai apdrošinātās vērtību, laukā Pēdējā periodiskās vērtības/izmaksu atjaunināšana automātiski tiek atjaunināts pašreizējais datums. 

Paraugs 

Vakar esat par 5 % atjauninājis grupu Transportlīdzekļi, Biroja mēbeles un Ēkas atjaunošanas izmaksas un tagad uzskatāt, ka šie līdzekļi ir pareizi atjaunināti. Lai izslēgtu šos līdzekļus, šodien atjauninot visus pārējos pamatlīdzekļus, laukā Datums, kad pēdējoreiz atjaunināta periodiskā vērtība/cena ievadiet datumu, kas ir pirms vakardienas datuma (&lt; vakardienas datums), jo pēdējā grupu Transportlīdzekļi, Biroja mēbeles un Ēkas atjaunināšana tika veikta neatbilstoši ievadītajam datuma kritērijam.

## <a name="cumulative-effect-of-each-update"></a> Katra atjauninājuma kopējā ietekme
Katram atjauninājumam ir raksturīga kopēja ietekme Tāpēc atjaunināšanas darbības ir rūpīgi jāplāno. Piemēram, ja otrdien visu pamatlīdzekļu vērtība tiek palielināta par 3 % un pēc tam piektdien tiek palielināta biroja mēbeļu vērtība par 4 %, biroja mēbeļu vērtība kopumā palielināsies par 7,12 %.

## <a name="scenario"></a>Scenārijs
Jūsu menedžeris informē jūs par šādām fiksētajām pamatlīdzekļu izmaiņām:
-   Palieliniet par 3,25 % atjaunošanas izmaksas visiem fiksētajiem pamatlīdzekļiem, izņemot datorus.
-   Palieliniet atjaunošanas izmaksas visām biroja mēbelēm papildus par 1 %.
-   Samaziniet par 10 % atjaunošanas izmaksas un apdrošināšanas summu visiem datoriem.

Var veikt tālāk norādītās izmaiņas.
1.  Formā Pamatlīdzekļu grupas visu pamatlīdzekļu grupu, izņemot grupas Biroja mēbeles un Datori, laukā Aizstāšanas izmaksu koeficients ievadiet 3,25 un laukā Apdrošinātās vērtības koeficients ierakstiet 0.
2.  Grupas Biroja mēbeles laukā Aizstāšanas izmaksu koeficients ievadiet 4,25 un laukā Apdrošinātās vērtības koeficients ierakstiet 0.
3.  Grupas Datori laukā Aizstāšanas izmaksu koeficients ievadiet -10 un laukā Apdrošinātās vērtības koeficients ierakstiet -10.
4.  Lai pārrēķinātu visu pamatlīdzekļu vērtības, formā Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana noklikšķiniet uz Labi.

Nākamajā dienā jūsu vadītājs jūs informē, ka datoru vērtība ir samazinājusies par 8 %, nevis 10 %, tādēļ jums jāizlabo aizstāšanas izmaksas un apdrošinātās vērtības. Lai izlabotu kļūdu, varat izmantot vienu no divām metodēm:
-   Manuāli mainiet visu pamatlīdzekļu vērtības pamatlīdzekļu grupas Datori formas Pamatlīdzekļi laukā Apdrošinātā vērtība un Aizstāšanas izmaksas. Aprēķiniet un manuāli ievadiet vērtības tā, it kā sākotnējā summa būtu samazinājusies par 8 procentiem. Izmantojot šo metodi, nav jāizmanto forma Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana.
-   Formas Pamatlīdzekļu grupas laukā Aizstāšanas izmaksu koeficients un Apdrošinātās vērtības koeficients grupai Datori ievadiet aizstāšanas izmaksu un apdrošinātās vērtības koeficientus. Tādējādi tiek gan atiestatīta pamatlīdzekļu sākotnējā vērtība (pirms samazinājuma par 10 %), gan sākotnējā vērtība tiek samazināta par 8 %. Pēc tam atkarībā no ievadītajiem koeficientiem pārrēķiniet vērtības, izmantojot formu Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana.

> [!NOTE]  
> Koeficientu –10 nevar nomainīt, ievadot koeficientu +10 (vai koeficientu 2, starpību starp –10 un –8), jo summas netiks aprēķinātas atbilstoši jūsu vēlmēm. 






