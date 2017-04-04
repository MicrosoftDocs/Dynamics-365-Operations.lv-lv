---
title: "Finanšu Performance Power BI saturu"
description: "Šī tēma apraksta Microsoft Dynamics 365 par darbības finansiālajiem rezultātiem satura pakotne Microsoft Power BI. Tā apraksta panelis un ziņojumus, kas ir iekļautas satura pakotne, un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Finanšu Performance Power BI saturu

Šī tēma apraksta Microsoft Dynamics 365 par darbības finansiālajiem rezultātiem satura pakotne Microsoft Power BI. Tā apraksta panelis un ziņojumus, kas ir iekļautas satura pakotne, un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne.

<a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
--------------------------

Finanšu darbības satura pakotni divas versijas ir pieejamas. Viena versija ir pieejama no Microsoft Dynamics Lifecycle Services (LCS), un otrs ir pieejamas no PowerBI.com.

-   **Versija, kas pieejama no LCS:** finansiālo darbību satura pakotne, kas ir pieejama no LCS atbalsta Microsoft Dynamics 365 darbību versija 1611. Jūs varat atrast satura pakotne LCS bibliotēkā Shared aktīvu. Lai iegūtu papildinformāciju par satura pakotnes lejupielāde un izveidojiet savienojumu ar savu Microsoft Dynamics 365 darbības datiem, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).
-   **Versija, kas pieejama no PowerBI.com:** finansiālo darbību satura pakotne, kas ir pieejams no PowerBI.com atbalsta Microsoft Dynamics AX versijas 7.0 un 7.0.1. Plašāku informāciju par savienojumu un ielādē savu dinamiku 365 darbības datiem, skatiet [Access Power BI saturu no PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Galvenais konta iestatīšanu
Jo uzņēmumi vēlas pasīvu un ieņēmumu summas tiktu rādīta kā pozitīvas summas atskaitēs, galvenais Dynamics 365 operāciju kontu uzstādījumam ir svarīgi. Šo galveno kontu tiktu rādīta kā pozitīvas summas, galvenā konta tips ir jāiestata **atbildību** vai **ieņēmumi**. Kad šie kontu tipi tiek lietoti, atskaites, izmantojot Microsoft Power BI atsaukt pazīmes un parādīt kā pozitīvas summas.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Paneļa un ziņojumus, kas ir iekļautas satura pakotni
Pēc satura pakotnes savienošanas ar jūsu Dynamics 365 for Operations datiem informācijas panelī un pārskatos tiek rādīti jūsu finanšu dati. Ja neesat lietojis varas BI pirms, jūs varat uzzināt vairāk par to uz [vadīto mācību lapas Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Informācijas panelī ir apkopoti datu elementi, kas ir balstīti uz pamata pārskatiem. Katrs elements satur apkopotu informāciju par pašreizējo gadu visos uzņēmumos attiecīgajā organizācijā. Šeit ir dažas flīzes:

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

Katras mozaīkas ir nodrošināta atbalsta ziņojumu. Šie pārskati satur gan diagrammas, gan tabulas, kas sniedz papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                      | Pārskatā iekļautā informācija                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naudas plūsmas analīze               | Juridiska persona, naudas pa ceturkšņiem, kopējo naudas un naudas konts naudas **Piezīme:****naudas ceturksnī** pārskats neietver sākuma bilances kopsumma pirmajā ceturksnī. Tas parāda pavisam jaunas darbības, kas grāmatotas katrā ceturksnī.                                                                                |
| Pašreizējā koeficienta analīze      | Pašreizējais koeficients pēc juridiskas personas, pašreizējais koeficients pa ceturkšņiem un apgrozāmo līdzekļu un īstermiņa saistību atlikumi                                                                                                                                                                                                                              |
| Tiešā koeficienta analīze        | Ātru attiecību juridiskā vienība, ātri attiecība pēc ceturkšņa un naudas, bilances debitoru parādiem un pašreizējo saistību                                                                                                                                                                                                                      |
| Pārdoto preču pašizmaksas analīze | Pārdoto preču pašizmaksa (PPPI) pēc juridiskas personas, PPPI šājā gadā un iepriekšējā gadā pa ceturkšņiem, PPPI pret apgrozījumu pēc juridiskas personas, PPPI kopsumma un PPPI attiecība pret apgrozījumu procentos                                                                                                                                                                                   |
| Apgrozāmā kapitāla analīze    | Apgrozāmais kapitāls pēc juridiskas personas, apgrozāmais kapitāls pa ceturkšņiem, apgrozāmie līdzekļi, īstermiņa saistības un kopējais apgrozāmais kapitāls                                                                                                                                                                                                                   |
| Aktīvu un parādu analīze     | Kopējo līdzekļu ienesīgums un parādu un kopējo līdzekļu attiecība pēc juridiskas personas, parādu un kopējo līdzekļu attiecība un kopējo līdzekļu ienesīgums pa ceturkšņiem līdz pašreizējam datumam, aktīvi un pasīvi                                                                                                                                                                                     |
| Peļņas normas analīze      | Faktiskā un budžeta peļņas norma pēc juridiskas personas, peļņas norma pa ceturkšņiem, peļņas normas procentuālā vērtība un peļņas norma                                                                                                                                                                                                                       |
| Neto ieņēmumu analīze         | Faktiskie un budžeta neto ieņēmumi pēc juridiskas personas, neto ieņēmumi šajā gadā un iepriekšējā gadā un izdevumu un neto ieņēmumu attiecība procentos                                                                                                                                                                                                                       |
| Ienākumu analīze           | Faktiskie un budžeta ienākumi pirms procentu un nodokļu nomaksas (EBIT) pēc juridiskas personas, EBIT šajā gadā un iepriekšējā gadā, izdevumu un ieņēmumu attiecība procentos un faktiskā un budžeta izdevumu un ieņēmumu attiecība                                                                                                                                                          |
| Ieņēmumu analīze            | Kopējie ieņēmumi, faktiskie un budžeta kopējie ieņēmumi pēc juridiskas personas, kopējie ieņēmumi šajā gadā un iepriekšējā gadā, ieņēmumu budžeta novirze pēc juridiskas personas un kopējie ieņēmumi šajā periodā un iepriekšējā periodā                                                                                                                                                 |
| Izdevumu analīze            | Kopējie izdevumi, faktisko un budžeta kopējo izdevumu attiecība pēc juridiskas personas, faktiskie un budžeta kopējie izdevumi pa ceturkšņiem, kopējie izdevumi pēc kontu kategorijas un darbības izmaksu koeficients                                                                                                                                                                 |
| Rēķinos iekļauto ieņēmumu analīze     | Kopā Debitori kopā Debitori juridiskā vienība, kopā debitori pa ceturkšņiem un bilances pārskatu debitoru kontus **Piezīme:** pārskati neietver sākuma bilances pārskatu debitoru Virsgrāmatas kontiem. Tie parāda jaunas darbības, kas grāmatotas kontiem parādu kopsumma. |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet sadaļā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Datus, kas izplata paneļa un atskaites finanšu sniegums satura pakotne ir dinamika 365 operāciju datus. Šādas vienības izmantoja kā pamatu satura pakotne: **apkopot datu subjekti**

-   **GeneralLedgerActivities** -šai entītijai uzkrāj Virsgrāmatas bilances kontā kategorijā.
-   **BudgetActivities** -šai entītijai uzkrāj budžeta bilances kontu kategorijas.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Virsgrāmatas
-   ChartofAccounts

Šīm vienībām tika izmantoti, lai izveidotu aprēķinātās mērvienības datu modelī. Aprēķinātie līdzekļi tiek izmantoti, lai aprēķinātu galveno veiktspējas rādītāju (KPI) un atskaites, kas tiek izmantotas satura pakotne. Pēc noklusējuma satura pakotne piegādā datus par pēdējiem trīs gadiem un vienu turpmāko gadu. Lai pārskatos un informācijas panelī iekļautu papildu aprēķinus, varat modificēt [Microsoft Excel darbgrāmatu](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Šī darbgrāmata ir noklusējuma datu modelis, kas tika izmantots, lai izveidotu satura pakotni. Pēc tam, kad esat pabeidzis savu izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur informāciju, kuru pievienojāt.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)



