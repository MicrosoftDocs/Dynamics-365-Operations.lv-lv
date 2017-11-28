---
title: "Power BI saturs Faktiski pret budžetu"
description: "Šajā tēmā ir aprakstīts Power BI saturs Faktiski pret budžetu. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f09af96fb1c76d8737d2c535f1a46565a18deca0
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Power BI saturs Faktiski pret budžetu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts Microsoft Power BI saturs **Faktiski pret budžetu**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem. 

# <a name="overview"></a>Pārskats

Power BI saturs **Faktiski pret budžetu** tika izveidots personām, kas savā organizācijā atbild par faktiskās izpildes uzraudzīšanu salīdzinājumā ar budžetā paredzēto izpildi. Power BI saturs **Faktiski pret budžetu** nodrošina ieskatu jūsu budžeta novirzēs. Lai gūtu lielāku izpratni par noviržu iemeslu, budžetu pašreizējam gadam var analizēt pēc konta kategorijas, budžeta koda, galvenā konta, galvenā konta aprakstiem vai finanšu perioda. 

# <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja lietojat programmatūru Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs), tad Power BI saturā **Faktiski pret budžetu** ietvertie pārskati tiek rādīti darbvietās **Virsgrāmatas budžeti un prognozes** un **CFO**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Nākamajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir atrodami katrā Power BI satura **Faktiski pret budžetu** pārskata lapā.

| Pārskats                      | Metrika |
|-----------------------------|---------|
| Izdevumi — faktisko un budžeta salīdzinājums | <ul><li>Kopējie izdevumi šajā gadā</li><li>Budžeta kopējie izdevumi šajā gadā</li></ul> |
| Ieņēmumi — faktisko un budžeta salīdzinājums  | <ul><li>Kopējie ieņēmumi šajā gadā</li><li>Budžeta kopējie ieņēmumi šajā gadā</li><ul> |
| Izdevumi                     | <ul><li>Kopējie izdevumi šajā gadā</li><li>Izdevumu mērķis, pamatojoties uz budžetu </li><ul> |
| Ieņēmumi                     | <ul><li>Kopējie ieņēmumi šajā gadā</li><li>Ieņēmumu mērķis, pamatojoties uz budžetu </li><ul> |
| Neto ieņēmumi                  | <ul><li>Neto ieņēmumi šajā gadā</li><li>Neto ieņēmumu mērķis, pamatojoties uz budžetu </li><ul> |

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai. 

Power BI saturs **Faktiski pret budžetu** ir atrodams LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

# <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

| Elements                    | Saturs |
|---------------------------|----------|
| Virsgrāmatas aktivitātes | Transakciju summas virsgrāmatai |
| Budžeta aktivitātes         | Transakciju summas budžeta reģistram |
| Galvenie konti             | Galvenie konti, pēc kuriem filtrēt pārskatus |
| Finanšu kalendāri          | Finanšu kalendāri, pēc kuriem filtrēt pārskatus |
| Virsgrāmatas                   | Virsgrāmatas, ko var izmantot, lai pārskatu filtrētu pašreizējai virsgrāmatai |
| Budžetu kodi              | Budžetu kodi, pēc kuriem filtrēt pārskatus |
| Juridiskās personas            | Juridiskās personas, ko var izmantot, lai pārskatu filtrētu pašreizējai juridiskajai personai |

