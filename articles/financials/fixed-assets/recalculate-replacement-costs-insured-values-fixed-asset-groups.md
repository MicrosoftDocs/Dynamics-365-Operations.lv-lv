---
title: "Pamatlīdzekļu grupu aizstāšanas izmaksu un apdrošinātās vērtību pārrēķināšana"
description: "Šajā rakstā ir paskaidrots, kā atjaunināt pamatlīdzekļu atjaunošanas izmaksas un apdrošinātās vērtības."
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
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
ms.sourcegitcommit: eb3db5863bf2fcca31b6af878e7324b079f1c630
ms.openlocfilehash: ad706a9ee441858a6f4a128ff978e24efb6ecfce
ms.contentlocale: lv-lv
ms.lasthandoff: 01/12/2018

---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Pamatlīdzekļu grupu aizstāšanas izmaksu un apdrošinātās vērtību pārrēķināšana

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā atjaunināt pamatlīdzekļu atjaunošanas izmaksas un apdrošinātās vērtības.

Periodiski jums var paziņot, ka maksa par noteiktu pamatlīdzekļu atjaunošanu vai apdrošināšanu ir mainījusies. Piemēram, jūsu menedžeris var informēt jūs, ka pagājušajā gadā inflācija bija 3 %, tādēļ visu pamatlīdzekļu atjaunošanas izmaksas jums būs jāpaaugstina par 3 %. 

Lai gan lapā **Pamatlīdzekļi** var rediģēt atsevišķu pamatlīdzekļu aizstāšanas izmaksas un apdrošinātās vērtības, varat izmantot arī lapu **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana**, lai šīs vērtības vienlaikus atjauninātu visai līdzekļu grupai. Šeit ir sniegta informācija par to, kā atjaunināt pamatlīdzekļu grupu vai atsevišķu grupu līdzekļu vērtības.

## <a name="how-values-are-updated"></a> Kā tiek atjauninātas vērtības
Lai pārrēķinātu pamatlīdzekļu grupu aizstāšanas izmaksas un apdrošinātās vērtības, vispirms jānorāda, par cik procentiem nomainīt pašreizējās aizstāšanas izmaksas un apdrošinātās vērtības, un tad var veikt periodisko atjaunināšanu, lai pārrēķinātu faktiskās vērtības. Procentuālo vērtību norādiet lapas **Pamatlīdzekļu grupas** laukos **Aizstāšanas izmaksu koeficients** un **Apdrošinātas vērtības koeficients**. Lai gan šie koeficienti tiek norādīti visai pamatlīdzekļu grupai, izmantojot lapu **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana**, varat atlasīt aizstāšanas izmaksu un apdrošināto vērtību pārrēķināšanu tikai noteiktiem pamatlīdzekļiem grupā. 

Kad lapu **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana** izmantojat, lai pārrēķinātu līdzekļu aizstāšanas izmaksas un apdrošinātās vērtības, tiek izmantotas tālāk norādītās formulas.

-   \[(Līdzekļu grupas atjaunošanas izmaksu koeficients / 100) + 1\] \* līdzekļa pašreizējās atjaunošanas izmaksas
-   \[(Līdzekļu grupas apdrošināšanas summas koeficients / 100) + 1\] \* līdzekļa pašreizējā apdrošināšanas summa

> [!NOTE] 
> Kad izmantojat lapu **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana**, tiek atjauninātas gan atlasīto līdzekļu aizstāšanas izmaksas, gan apdrošinātās vērtības; nevar norādīt tikai vienas vērtības atjaunināšanu. Lai nemainītu vienu vērtību, bet atjauninātu otru, lapā **Pamatlīdzekļu grupas** kā koeficientu ievadiet 0 (nulle). Ja koeficients ir nulle vai tukšs, tad aprēķins atjauninājumā tiek izlaists. Periodiskā atjaunināšana pamatlīdzekļu atlikušo vērtību un atlikušo neto vērtību neietekmē. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Kā lietot datumu, lai atlasītu atjaunināmos krājumus
Pēc noklusējuma atjaunināšanas procesa laikā tiek atjaunināti atlasītie pamatlīdzekļi, kas nav atjaunināti pašreizējā dienā, bet, iespējams, ka tie ir jau atjaunināti kādā no iepriekšējām dienām. Piemēram, &lt; pašreizējais datums nozīmē “pirms šodienas”. Datumu lapā **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana** varat mainīt, noklikšķinot uz pogas **Atlasīt**. Norādītais datuma kritērijs tiek salīdzināts ar līdzekļa pēdējās periodiskās atjaunināšanas datumu (lauks **Pēdējā periodiskās vērtības/izmaksu atjaunināšana** lapā **Pamatlīdzekļi**). Katru reizi, kad sekmīgi atjaunināt pamatlīdzekļa aizstāšanas izmaksas vai apdrošināto vērtību, laukā **Pēdējā periodiskās vērtības/izmaksu atjaunināšana** automātiski tiek atjaunināts pašreizējais datums. 

Paraugs 

Vakar esat par 5 % atjauninājis grupu Transportlīdzekļi, Biroja mēbeles un Ēkas atjaunošanas izmaksas un tagad uzskatāt, ka šie līdzekļi ir pareizi atjaunināti. Lai izslēgtu šos līdzekļus, šodien atjauninot visus pārējos pamatlīdzekļus, laukā **Pēdējā periodiskās vērtības/izmaksu atjaunināšana** ievadiet datumu, kas ir pirms vakardienas datuma (&lt; vakardienas datumu), jo pēdējā grupu **Transportlīdzekļi**, **Biroja mēbeles** un **Ēkas** atjaunināšana tika veikta neatbilstoši ievadītajiem datuma kritērijiem.

## <a name="cumulative-effect-of-each-update"></a> Katra atjauninājuma kopējā ietekme
Katram atjauninājumam ir raksturīga kopēja ietekme Tāpēc atjaunināšanas darbības ir rūpīgi jāplāno. Piemēram, ja otrdien visu pamatlīdzekļu vērtība tiek palielināta par 3 % un pēc tam piektdien tiek palielināta biroja mēbeļu vērtība par 4 %, biroja mēbeļu vērtība kopumā palielināsies par 7,12 %.

## <a name="scenario"></a>Scenārijs
Jūsu menedžeris informē jūs par šādām fiksētajām pamatlīdzekļu izmaiņām:
-   Palieliniet par 3,25 % atjaunošanas izmaksas visiem fiksētajiem pamatlīdzekļiem, izņemot datorus.
-   Palieliniet atjaunošanas izmaksas visām biroja mēbelēm papildus par 1 %.
-   Samaziniet par 10 % atjaunošanas izmaksas un apdrošināšanas summu visiem datoriem.

Var veikt tālāk norādītās izmaiņas.
1.  Lapā **Pamatlīdzekļu grupas** visu pamatlīdzekļu grupu, izņemot grupas **Biroja mēbeles** un grupas **Datori**, laukā **Aizstāšanas izmaksu koeficients** ievadiet 3,25 un laukā **Apdrošinātās vērtības koeficients** ievadiet 0.
2.  Grupas **Biroja mēbeles** laukā **Aizstāšanas izmaksu koeficients** ievadiet 4,25 un laukā **Apdrošinātās vērtības koeficients** ievadiet 0.
3.  Grupas **Datori** laukā **Aizstāšanas izmaksu koeficients** ievadiet -10 un laukā **Apdrošinātās vērtības koeficients** ievadiet -10.
4.  Lai pārrēķinātu visu pamatlīdzekļu vērtības, lapā **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana** noklikšķiniet uz **Labi**.

Nākamajā dienā jūsu vadītājs jūs informē, ka datoru vērtība ir samazinājusies par 8 %, nevis 10 %, tādēļ jums jāizlabo aizstāšanas izmaksas un apdrošinātās vērtības. Lai izlabotu kļūdu, varat izmantot vienu no divām metodēm:
-   Manuāli mainiet visu pamatlīdzekļu vērtības pamatlīdzekļu grupas **Datori** lapas **Pamatlīdzekļi** laukos **Apdrošinātā vērtība** un **Aizstāšanas izmaksas**. Aprēķiniet un manuāli ievadiet vērtības tā, it kā sākotnējā summa būtu samazinājusies par 8 procentiem. Izmantojot šo metodi, nav jāizmanto lapa **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana**.
-   Lapas **Pamatlīdzekļu grupas** laukos **Aizstāšanas izmaksu koeficients** un **Apdrošinātās vērtības koeficients** grupai **Datori** ievadiet aizstāšanas izmaksu un apdrošinātās vērtības koeficientus. Tādējādi tiek gan atiestatīta pamatlīdzekļu sākotnējā vērtība (pirms samazinājuma par 10 %), gan sākotnējā vērtība tiek samazināta par 8 %. Pēc tam atkarībā no ievadītajiem koeficientiem pārrēķiniet vērtības, izmantojot lapu **Aizstāšanas izmaksu un apdrošināto vērtību atjaunināšana**.

> [!NOTE]  
> Koeficientu –10 nevar nomainīt, ievadot koeficientu +10 (vai koeficientu 2, starpību starp –10 un –8), jo summas netiks aprēķinātas atbilstoši jūsu vēlmēm. 






