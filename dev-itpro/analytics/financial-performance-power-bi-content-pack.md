---
title: "Power BI saturs Finanšu veiktspēja"
description: "Šajā tēmā ir aprakstīta Microsoft Dynamics 365 for Operations satura pakotne Finanšu veiktspēja pakalpojumam Microsoft Power BI. Tajā ir arī aprakstīts informācijas panelis un pārskati, kas ir iekļauti šajā satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai satura pakotni izveidotu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9cd1d7e5b7b1fd892034dcca0a0c141363104a45
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Power BI saturs Finanšu veiktspēja

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīta Microsoft Dynamics 365 for Operations satura pakotne Finanšu veiktspēja pakalpojumam Microsoft Power BI. Tajā ir arī aprakstīts informācijas panelis un pārskati, kas ir iekļauti šajā satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai satura pakotni izveidotu.

<a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
--------------------------

Satura pakotnei Finanšu veiktspēja ir pieejamas divas versijas. Viena versija ir pieejama no Microsoft Dynamics Lifecycle Services (LCS), un otra ir pieejama no PowerBI.com.

-   **No LCS pieejamā versija:** satura pakotne Finanšu veiktspēja, kas ir pieejama no LCS, atbalsta Microsoft Dynamics 365 for Operations versiju 1611. Šī satura pakotne ir atrodama LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Microsoft Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).
-   **No PowerBI.com pieejamā versija:** satura pakotne Finanšu veiktspēja, kas ir pieejama no PowerBI.com, atbalsta Microsoft Dynamics AX versiju 7.0 un 7.0.1. Plašāku informāciju par to, kā pievienot un ielādēt Dynamics 365 for Operations datus, skatiet rakstā [Piekļūt Power BI saturam no PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Galvenā konta iestatīšana
Tā kā organizācijas vēlas, lai saistību un ieņēmumu summas pārskatos tiktu rādītas kā pozitīvas summas, galveno kontu iestatīšana programmatūrā Dynamics 365 for Operations ir svarīga. Lai šie galvenie konti tiktu rādīti kā pozitīvas summas, galvenā konta tips ir jāiestata uz **Saistība** vai **Ieņēmumi**. Kad tiek izmantoti šie kontu tipi, pārskatu veidošana, izmantojot Microsoft Power BI, apgriež zīmes un šīs summas rāda kā pozitīvas.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie informācijas paneļi un pārskati
Pēc satura pakotnes savienošanas ar jūsu Dynamics 365 for Operations datiem informācijas panelī un pārskatos tiek rādīti jūsu finanšu dati. Ja iepriekš neesat lietojis Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Informācijas panelī ir apkopoti datu elementi, kas ir balstīti uz pamata pārskatiem. Katrs elements satur apkopotu informāciju par pašreizējo gadu visos uzņēmumos attiecīgajā organizācijā. Tālāk ir norādīti daži elementi.

-   Kase
-   Kopējie ieņēmumi šajā gadā
-   Kopējie izdevumi šajā gadā
-   Neto ieņēmumi šajā gadā
-   Tiešais koeficients
-   Kopējie izdevumi šajā gadā pēc konta kategorijas
-   Pašreizējais koeficients
-   Parāds kopējiem līdzekļiem
-   Faktiskie un prognozētie ieņēmumi
-   Rēķinos iekļautie ieņēmumi šajā gadā
-   Darbības izmaksu koeficients šajā gadā
-   Peļņas norma šajā gadā
-   Faktiskie un budžeta izdevumi — visi uzņēmumi

Katrs elements balstās uz atbalsta pārskatu. Šie pārskati satur gan diagrammas, gan tabulas, kas sniedz papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                      | Pārskatā iekļautā informācija                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naudas plūsmas analīze               | Naudas plūsma pēc juridiskās personas, naudas plūsma pa ceturkšņiem, kopsumma kasē un naudas plūsma pēc konta. **Piezīme.** Pārskats **Naudas plūsma pa ceturkšņiem** pirmā ceturkšņa kopsummā neietver sākuma bilances. Tas rāda katrā ceturksnī grāmatoto jauno transakciju kopsummu.                                                                                |
| Pašreizējā koeficienta analīze      | Pašreizējais koeficients pēc juridiskas personas, pašreizējais koeficients pa ceturkšņiem un apgrozāmo līdzekļu un īstermiņa saistību atlikumi                                                                                                                                                                                                                              |
| Tiešā koeficienta analīze        | Tiešais koeficients pēc juridiskās personas, tiešais koeficients pa ceturkšņiem un skaidras naudas, debitoru parādu un īstermiņa saistību bilances                                                                                                                                                                                                                      |
| Pārdoto preču pašizmaksas analīze | Pārdoto preču pašizmaksa (PPPI) pēc juridiskas personas, PPPI šājā gadā un iepriekšējā gadā pa ceturkšņiem, PPPI pret apgrozījumu pēc juridiskas personas, PPPI kopsumma un PPPI attiecība pret apgrozījumu procentos                                                                                                                                                                                   |
| Apgrozāmā kapitāla analīze    | Apgrozāmais kapitāls pēc juridiskas personas, apgrozāmais kapitāls pa ceturkšņiem, apgrozāmie līdzekļi, īstermiņa saistības un kopējais apgrozāmais kapitāls                                                                                                                                                                                                                   |
| Aktīvu un parādu analīze     | Kopējo līdzekļu ienesīgums un parādu un kopējo līdzekļu attiecība pēc juridiskas personas, parādu un kopējo līdzekļu attiecība un kopējo līdzekļu ienesīgums pa ceturkšņiem līdz pašreizējam datumam, aktīvi un pasīvi                                                                                                                                                                                     |
| Peļņas normas analīze      | Faktiskā un budžeta peļņas norma pēc juridiskas personas, peļņas norma pa ceturkšņiem, peļņas normas procentuālā vērtība un peļņas norma                                                                                                                                                                                                                       |
| Neto ieņēmumu analīze         | Faktiskie un budžeta neto ieņēmumi pēc juridiskas personas, neto ieņēmumi šajā gadā un iepriekšējā gadā un izdevumu un neto ieņēmumu attiecība procentos                                                                                                                                                                                                                       |
| Ienākumu analīze           | Faktiskie un budžeta ienākumi pirms procentu un nodokļu nomaksas (EBIT) pēc juridiskas personas, EBIT šajā gadā un iepriekšējā gadā, izdevumu un ieņēmumu attiecība procentos un faktiskā un budžeta izdevumu un ieņēmumu attiecība                                                                                                                                                          |
| Ieņēmumu analīze            | Kopējie ieņēmumi, faktiskie un budžeta kopējie ieņēmumi pēc juridiskas personas, kopējie ieņēmumi šajā gadā un iepriekšējā gadā, ieņēmumu budžeta novirze pēc juridiskas personas un kopējie ieņēmumi šajā periodā un iepriekšējā periodā                                                                                                                                                 |
| Izdevumu analīze            | Kopējie izdevumi, faktisko un budžeta kopējo izdevumu attiecība pēc juridiskas personas, faktiskie un budžeta kopējie izdevumi pa ceturkšņiem, kopējie izdevumi pēc kontu kategorijas un darbības izmaksu koeficients                                                                                                                                                                 |
| Rēķinos iekļauto ieņēmumu analīze     | Debitoru parādu kopsumma, debitoru parādu kopsumma pēc juridiskās personas, debitoru parādu kopsumma pa ceturkšņiem un debitoru parādu kontu atlikumi. **Piezīme.** Pārskati neietver sākuma bilances debitoru parādu virsgrāmatas kontiem. Tie rāda debitoru parādos grāmatoto jauno transakciju kopsummu. |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet sadaļā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Dati, ar ko tiek aizpildīts informācijas panelis un pārskati satura pakotnē Finanšu veiktspēja, ir Dynamics 365 for Operations dati. Kā satura pakotnes pamats tika izmantoti tālāk uzskaitītie elementi. **Apkopoto datu elementi**

-   **GeneralLedgerActivities** — šis elements apkopo virsgrāmatas bilances pēc kontu kategorijas.
-   **BudgetActivities** — šis elements apkopo budžeta bilances pēc kontu kategorijas.

**Datu elementi**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Virsgrāmatas
-   ChartofAccounts

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti satura pakotnē. Pēc noklusējuma satura pakotne piegādā datus par pēdējiem trīs gadiem un vienu turpmāko gadu. Lai pārskatos un informācijas panelī iekļautu papildu aprēķinus, varat modificēt [Microsoft Excel darbgrāmatu](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Šī darbgrāmata ir noklusējuma datu modelis, kas tika izmantots, lai izveidotu satura pakotni. Pēc tam, kad esat pabeidzis savu izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur informāciju, kuru pievienojāt.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)





