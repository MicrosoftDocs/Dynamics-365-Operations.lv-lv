---
title: "PowerBI.com risinājums Finanšu veiktspēja"
description: "Šajā tēmā ir aprakstīts PowerBI.com risinājums Finanšu veiktspēja."
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 78512e39e82e24f94dae93bbac116e6f07d25438
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="financial-performance-powerbicom-solution"></a>PowerBI.com risinājums Finanšu veiktspēja

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šis PowerBI.com risinājums ir novecojis, kā dokumentēts tēmā [AppSource pieejamās Power BI satura pakotnes](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Šajā tēmā ir aprakstīts PowerBI.com risinājums **Finanšu veiktspēja**. Tajā ir aprakstīts informācijas panelis un ietvertie pārskati, kā arī sniegta informācija par risinājuma izstrādei izmantoto datu modeli un elementiem.

## <a name="main-account-setup"></a>Galvenā konta iestatīšana
Tā kā organizācijas vēlas, lai saistību un ieņēmumu summas pārskatos tiktu rādītas kā pozitīvas summas, galveno kontu iestatīšana ir svarīga. Lai šie galvenie konti tiktu rādīti kā pozitīvas summas, galvenā konta tips ir jāiestata uz **Saistība** vai **Ieņēmumi**. Kad tiek izmantoti šie kontu tipi, pārskatu veidošana, izmantojot Power BI, apgriež zīmes un šīs summas rāda kā pozitīvas.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>PowerBI.com risinājumā ietvertie informācijas paneļi un pārskati
Informācijas panelī ir apkopoti datu elementi, kas ir balstīti uz pamata pārskatiem. Katrs elements satur apkopotu informāciju par pašreizējo gadu visos uzņēmumos attiecīgajā organizācijā. Tālāk ir norādīti daži elementi.

- Kase
- Kopējie ieņēmumi šajā gadā
- Kopējie izdevumi šajā gadā
- Neto ieņēmumi šajā gadā
- Tiešais koeficients
- Kopējie izdevumi šajā gadā pēc konta kategorijas
- Pašreizējais koeficients
- Parāds kopējiem līdzekļiem
- Faktiskie un prognozētie ieņēmumi
- Rēķinos iekļautie ieņēmumi šajā gadā
- Darbības izmaksu koeficients šajā gadā
- Peļņas norma šajā gadā
- Faktiskie un budžeta izdevumi — visi uzņēmumi

Katrs elements balstās uz atbalsta pārskatu. Šie pārskati satur gan diagrammas, gan tabulas, kas sniedz papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                      | Pārskatā iekļautā informācija |
|-----------------------------|--------------------------------------|
| Naudas plūsmas analīze               | Naudas plūsma pēc juridiskas personas, naudas plūsma pa ceturkšņiem, kopsumma kasē un naudas plūsma pēc konta<blockquote>[!NOTE] Informācija par naudu pēc ceturkšņa pirmā ceturkšņa kopsummā neietver sākuma bilances. Tas rāda katrā ceturksnī grāmatoto jauno transakciju kopsummu.</blockquote> |
| Pašreizējā koeficienta analīze      | Pašreizējais koeficients pēc juridiskas personas, pašreizējais koeficients pa ceturkšņiem un apgrozāmo līdzekļu un īstermiņa saistību atlikumi |
| Tiešā koeficienta analīze        | Tiešais koeficients pēc juridiskās personas, tiešais koeficients pa ceturkšņiem un skaidras naudas, debitoru parādu un īstermiņa saistību bilances |
| Pārdoto preču pašizmaksas analīze | Pārdoto preču pašizmaksa (PPPI) pēc juridiskas personas, PPPI šājā gadā un iepriekšējā gadā pa ceturkšņiem, PPPI pret apgrozījumu pēc juridiskas personas, PPPI kopsumma un PPPI attiecība pret apgrozījumu procentos |
| Apgrozāmā kapitāla analīze    | Apgrozāmais kapitāls pēc juridiskas personas, apgrozāmais kapitāls pa ceturkšņiem, apgrozāmie līdzekļi, īstermiņa saistības un kopējais apgrozāmais kapitāls |
| Aktīvu un parādu analīze     | Kopējo līdzekļu ienesīgums un parādu un kopējo līdzekļu attiecība pēc juridiskas personas, parādu un kopējo līdzekļu attiecība un kopējo līdzekļu ienesīgums pa ceturkšņiem līdz pašreizējam datumam, aktīvi un pasīvi |
| Peļņas normas analīze      | Faktiskā un budžeta peļņas norma pēc juridiskas personas, peļņas norma pa ceturkšņiem, peļņas normas procentuālā vērtība un peļņas norma |
| Neto ieņēmumu analīze         | Faktiskie un budžeta neto ieņēmumi pēc juridiskas personas, neto ieņēmumi šajā gadā un iepriekšējā gadā un izdevumu un neto ieņēmumu attiecība procentos |
| Ienākumu analīze           | Faktiskie un budžeta ienākumi pirms procentu un nodokļu nomaksas (EBIT) pēc juridiskas personas, EBIT šajā gadā un iepriekšējā gadā, izdevumu un ieņēmumu attiecība procentos un faktiskā un budžeta izdevumu un ieņēmumu attiecība |
| Ieņēmumu analīze            | Kopējie ieņēmumi, faktiskie un budžeta kopējie ieņēmumi pēc juridiskas personas, kopējie ieņēmumi šajā gadā un iepriekšējā gadā, ieņēmumu budžeta novirze pēc juridiskas personas un kopējie ieņēmumi šajā periodā un iepriekšējā periodā |
| Izdevumu analīze            | Kopējie izdevumi, faktisko un budžeta kopējo izdevumu attiecība pēc juridiskas personas, faktiskie un budžeta kopējie izdevumi pa ceturkšņiem, kopējie izdevumi pēc kontu kategorijas un darbības izmaksu koeficients |
| Rēķinos iekļauto ieņēmumu analīze     | Debitoru parādu kopsumma, debitoru parādu kopsumma pēc juridiskās personas, debitoru parādu kopsumma pēc ceturkšņa un debitoru parādu kontu atlikumi<blockquote>[!NOTE] Šī informācija neietver sākuma bilances debitoru parādu virsgrāmatas kontiem. Tā rāda debitoru parādos grāmatoto jauno transakciju kopsummu.</blockquote> |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet sadaļā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
PowerBI.com risinājuma **Finanšu veiktspēja** pamatā tika izmantoti tālāk norādītie elementi.

**Apkopoto datu elementi**

- **GeneralLedgerActivities** — šis elements apkopo virsgrāmatas bilances pēc kontu kategorijas.
- **BudgetActivities** — šis elements apkopo budžeta bilances pēc kontu kategorijas.

**Datu elementi**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Virsgrāmatas
- ChartofAccounts

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti saturā. Pēc noklusējuma saturs apkopo datus par pēdējiem trīs gadiem un vienu turpmāko gadu. Lai pārskatos un informācijas panelī iekļautu papildu aprēķinus, varat modificēt [Microsoft Excel darbgrāmatu](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Šī darbgrāmata ir noklusējuma datu modelis, kas tika izmantots satura izveidošanai.

