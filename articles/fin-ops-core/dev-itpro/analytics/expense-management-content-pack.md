---
title: Izdevumu pārvaldības Power BI saturs
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Izdevumu pārvaldība.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9391676beea6aac831648d5fa55eae5eba3f6397
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682801"
---
# <a name="expense-management-power-bi-content"></a>Izdevumu pārvaldības Power BI saturs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Izdevumu pārvaldība. 

## <a name="overview"></a>Kopsavilkums
Izmantošanai ar Izdevumu pārvaldību versijā 8.1 un jaunākās versijās ir pieejamas divas Power BI satura pakotnes. 
- Darbiniekiem, kuri iesniedz izdevumu pārskatus, ir paredzēts personisks informācijas panelis. 

  Informācijas panelis ir pielāgots, lai sniegtu personām galveno informāciju par neiesniegtām un iesniegtām summām, kā arī vēsturi un ieskatiem izdevumu darbību vēsturē. Personiskais informācijas panelis ir atsevišķa lapa, kas satur svarīgāko informāciju par lietotāju.

- Tajā ir administratora informācijas panelis, kas paredzēts kreditoru administratoriem un vadītājiem. Informācijas panelis ir pielāgots, lai veiktu uzskaiti un pārskatu izveidi par kopējiem darbinieku izdevumiem. Tas nodrošina galvenos izdevumu rādītājus, piemēram, neiesniegtos izdevumus, nobraukumu un vidējās izdevumu pārskata summas. Tajā tiek izmantoti transakciju dati, un tas nodrošina visu uzņēmumu izdevumu pārvaldības apkopotus skatus. Tas arī sniedz sadalījumu pa darbiniekiem, nodrošinot iespēju pievienot finanšu dimensiju datus. Satura pakotnē Administrēšanas izdevumu analīze ietilpst: 
  - Pārskata lapa ar galvenajiem rādītājiem par izdevumu summām un ieskatiem par melnraksta posmā esošajiem, nepabeigtajiem un pabeigtajiem izdevumu pārskatiem. 
  - Darbinieku statistikas lapa, lai skatītu atsevišķu informāciju par darbinieku atbilstoši laikam, izmaksu veidam un statistikas grupai. 
  - Darbinieku salīdzināšanas lapa, lai salīdzinātu vairākus darbiniekus laika gaitā. 

Visas summas ir norādītas uzņēmuma valūtā. Tiek rādīti dati par visiem uzņēmumiem, bet, ja nepieciešams, var pievienot uzņēmuma filtru. 

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura failus Expense Admin Dashboard.pbix un Expense Personal Dashboard.pbix varat atrast koplietojamo līdzekļu bibliotēkā pakalpojumā Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Saturs ir pieejams no darbvietas Izdevumu pārvaldība, kas iegulta Power BI saturā. Izdevumu veicējs var piekļūt paša veiktajiem personiskajiem izdevumiem, savukārt administratoru saturam, lai skatītu visus lietotāja izdevumu datus, var piekļūt tikai kreditoru administratori un vadītāji.

## <a name="refreshing-the-power-bi-content"></a>Power BI satura atsvaidzināšana
Power BI satura pakotnei Izdevumu pārvaldība ir nepieciešams atsvaidzināt TrvBiExpenseMeasurement mērījumu un BudgetActivityMeasure no elementu krātuves. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie rādītāji
Saturā ietilpst pārskatu lapu komplekts. Katra lapa sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par Power BI satura rādītāju vizualizēšanu.

**Personisko izdevumu analīze**

| Pārskata lapa | Vizualizēšana                             |
|-------------|-------------------------------------------|
| Mani izdevumi | Nobrauktais attālums                         |
|             | Nepabeigtie izdevumu pārskati                |
|             | Nr.p.k. Neiesniegtie izdevumi               |
|             | Personiskie izdevumi, kas jāmaksā              |
|             | Neiesniegtā summa                        |
|             | Iesniegtā summa                          |
|             | Summas, kas jāatlīdzina             |
|             | Izdevumu pārskati ar summām un statusu   |
|             | Iesniegti, bet neapstiprināti izdevumu pārskati  |
|             | Izdevumi pēc izmaksu tipa                     |
|             | Izdevumi pēc tirgotāja                      |
|             | Izdevumi pēc apstrādātajiem izdevumiem            |
|             | Izdevumi pēc projekta                       |
|             | Kopējā darbību summa laika gaitā        |

**Administrēšanas izdevumu analīze**

| Pārskata lapa         | Vizualizēšana                           |           
|---------------------|-----------------------------------------|
| Izdevumu apskats    | Paredzēto izdevumu summa                   |
|                     | Paredzēto izdevumu rindu skaits           |
|                     | Paredzēto izdevumu rindas                     |
|                     | Izdevumu pārskata politikas pārkāpumi        |
|                     | Neapmaksātā summa                      |
|                     | Iesniegti, bet neapstiprināti izdevumi       |
|                     | Apstiprināti izdevumi                       |
|                     | Kopējā izdevumu summa                    |
|                     | Izdevumu pārskatu apkopojumi                |
|                     | Izdevumi pēc izmaksu tipa                   |
|                     | Izdevumi pēc tirgotāja                    |
|                     | Izdevumi pēc darbinieka                   |
|                     | Izdevumi – projekts                     |
| Darbinieku salīdzinājums | Izdevumu summas                         |
|                     | Izdevumu summas laikā gaitā pēc darbinieka   |
| Darbinieku statistika | Izdevumu pārskati pēc izmaksu tipa            |
|                     | Personiskie izdevumi                       |
|                     | Izdevumu pārskati pēc statistikas grupas     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]