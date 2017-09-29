---
title: "Periodisko rēķinu iestatīšana un apstrāde"
description: "Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt periodiskos rēķinus. Periodiskos rēķinus varat izmantot, ja debitoriem regulāri ir jāizraksta rēķini par tādu pašu summu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 463a81d615e6820b6ab45592cd21e28a76c6c04d
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="set-up-and-process-recurring-invoices"></a>Periodisko rēķinu iestatīšana un apstrāde

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt periodiskos rēķinus. Periodiskos rēķinus varat izmantot, ja debitoriem regulāri ir jāizraksta rēķini par tādu pašu summu.

<a name="create-a-recurring-free-text-invoice-template"></a>Periodiska brīva teksta rēķina veidnes izveide
---------------------------------------------

Lai debitoram regulāri izrakstītu rēķinu par vieniem pakalpojumiem, ir jādefinē brīvā teksta rēķina veidne, ko var atkārtoti izmantot, lai izveidotu rēķinus. Šajā veidnē ir ietverta šāda informācija:

-   galvenes informācija, piemēram, PVN grupas, apmaksas nosacījumi un maksāšanas metode;
-   rindas informācija, piemēram, pakalpojuma apraksts, ieņēmumu konti, vienības cena un rēķina summa;
-   piegādes vai apstrādes maksa;
-   uzskaites sadales kopā ar finanšu dimensiju informāciju, piemēram, izmaksu centri un biznesa vienības.

Faktiski tiek izveidots viss rēķins un pēc tam tas tiek saglabāts kā veidne. Var iestatīt veidnes, izmantojot lapu **Periodiskie rēķini**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Brīva teksta rēķina veidnes piešķšana debitoram un periodiskuma datu ievade
Kad veidne ir izveidota, tā ir jāpiešķir debitoriem, kam vēlaties izrakstīt rēķinu. Turklāt ir jānorāda, kad un cik bieži rēķins tiks izmantots. Veidnes varat piešķirt lapas **Debitori** cilnē **Rēķins**. Pievienojiet veidni sarakstam un atjauniniet šādu informāciju:

-   periodiskas rēķinu izrakstīšanas sākuma datumu un, ja nepieciešams, beigu datumu;
-   periodiskas rēķinu izrakstīšanas biežumu (piemēram, katru dienu vai reizi mēnesī);
-   maksimālo rēķina summu (ja šī informācija ir obligāti jānorāda).

Debitoram var būt vairākas veidnes, kam ir iestatīti dažādi biežumi.

## <a name="generate-the-recurring-invoices"></a>Periodisko rēķinu ģenerēšana
Lapā **Periodiskie rēķini** ir uzdevums, kas apstrādā periodisko rēķinu veidnes. Norādiet rēķina datumu un veidni, kas jāizmanto rēķinu ģenerēšanā. Rēķini tiks ģenerēti, un katrai apstrādājamajai rēķinu grupai tiks piešķirts viens periodiskuma ID numurs.
Periodisko brīva teksta rēķinu grāmatošana
---------------------------------

Pēc tam, kad periodiskie rēķini ir ģenerēti, rēķinu periodiskuma ID parādīsies grāmatošanas uzdevumā lapā **Periodiskie rēķini**. Visus rēķinus ar vienu periodiskuma ID var skatīt, noklikšķinot uz saites. Pārskatot rēķinus ar vienu periodiskuma ID, atsevišķus rēķinus varat dzēst. Debitora periodiskuma iestatījumi tiks atiestatīti šai veidnei, tādējādi vēlāk to var atkārtoti ģenerēt. Vienam periodiskuma ID var grāmatot vienu, vairākus vai visus rēķinus. Ja darbplūsmas ir iespējotas, lai rēķinus grāmatotu, noklikšķiniet uz **Iesniegt**.
Periodisko brīva teksta rēķinu drukāšana
----------------------------------

Ja periodiskie rēķini ir iegrāmatoti, rēķinus var drukāt no brīva teksta rēķina saraksta lapas. Varat drukāt atlasītos rēķinus, vai arī varat atlasīt drukāšanai rēķinu diapazonu.



