---
title: Periodisko rēķinu iestatīšana un apstrāde
description: Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt periodiskos rēķinus. Periodiskos rēķinus varat izmantot, ja debitoriem regulāri ir jāizraksta rēķini par tādu pašu summu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b443630d1612b5095fefa74b5ed6d057be534b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445488"
---
# <a name="set-up-and-process-recurring-invoices"></a>Periodisko rēķinu iestatīšana un apstrāde

[!include [banner](../includes/banner.md)]

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

<a name="post-recurring-free-text-invoices"></a>Periodisko brīva teksta rēķinu grāmatošana
---------------------------------

Pēc tam, kad periodiskie rēķini ir ģenerēti, rēķinu periodiskuma ID parādīsies grāmatošanas uzdevumā lapā **Periodiskie rēķini**. Visus rēķinus ar vienu periodiskuma ID var skatīt, noklikšķinot uz saites. Pārskatot rēķinus ar vienu periodiskuma ID, atsevišķus rēķinus varat dzēst. Debitora periodiskuma iestatījumi tiks atiestatīti šai veidnei, tādējādi vēlāk to var atkārtoti ģenerēt. Vienam periodiskuma ID var grāmatot vienu, vairākus vai visus rēķinus. Ja darbplūsmas ir iespējotas, lai rēķinus grāmatotu, noklikšķiniet uz **Iesniegt**.

<a name="print-recurring-free-text-invoices"></a>Periodisko brīva teksta rēķinu drukāšana
----------------------------------

Ja periodiskie rēķini ir iegrāmatoti, rēķinus var drukāt no brīva teksta rēķina saraksta lapas. Varat drukāt atlasītos rēķinus, vai arī varat atlasīt drukāšanai rēķinu diapazonu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]