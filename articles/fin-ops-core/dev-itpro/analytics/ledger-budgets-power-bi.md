---
title: Power BI satura pakotne Faktiski pret budžetu
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Faktiski pret budžetu. Tajā skaidrots, kā piekļūt pārskatiem un sniedz informāciju par izmantoto datu modeli.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9cc52f4cdab3084c9ac43078b0b0d534119ab514
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744243"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI satura pakotne Faktiski pret budžetu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta satura pakotne **Faktiski pret budžetu** programmā Microsoft Power BI. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Faktiski pret budžetu** ir izveidota personām, kas savā organizācijā atbild par faktiskās un budžetā paredzētās veiktspējas salīdzinājuma uzraudzību. Power BI satura pakotne **Faktiski pret budžetu** nodrošina ieskatu budžeta novirzēs. Lai gūtu lielāku izpratni par noviržu iemeslu, budžetu pašreizējam gadam var analizēt pēc konta kategorijas, budžeta koda, galvenā konta, galvenā konta aprakstiem vai finanšu perioda.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotnes **Faktiski pret budžetu** pārskati tiek rādīti darbvietās **Virsgrāmatas budžeti un prognozes** un **CFO**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Faktiski pret budžetu** pārskata lapā.

| Pārskats                      | Metrika                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Izdevumi — faktisko un budžeta salīdzinājums | <ul><li>Kopējie izdevumi šajā gadā</li><li>Budžeta kopējie izdevumi šajā gadā</li></ul>  |
| Ieņēmumi — faktisko un budžeta salīdzinājums  | <ul><li>Kopējie ieņēmumi šajā gadā</li><li>Budžeta kopējie ieņēmumi šajā gadā</li><ul>     |
| Izdevumi                     | <ul><li>Kopējie izdevumi šajā gadā</li><li>Izdevumu mērķis, pamatojoties uz budžetu</li><ul> |
| Ieņēmumi                     | <ul><li>Kopējie ieņēmumi šajā gadā</li><li>Ieņēmumu mērķis, pamatojoties uz budžetu</li><ul>   |
| Neto ieņēmumi                  | <ul><li>Neto ieņēmumi šajā gadā</li><li>Neto ieņēmumu mērķis, pamatojoties uz budžetu</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

| Elements                    | Saturs                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Virsgrāmatas aktivitātes | Transakciju summas virsgrāmatai                                       |
| Budžeta aktivitātes         | Transakciju summas budžeta reģistram                                      |
| Galvenie konti             | Galvenie konti, pēc kuriem filtrēt pārskatus                                               |
| Finanšu kalendāri          | Finanšu kalendāri, pēc kuriem filtrēt pārskatus                                            |
| Virsgrāmatas                   | Virsgrāmatas, ko var izmantot, lai pārskatu filtrētu pašreizējai virsgrāmatai              |
| Budžetu kodi              | Budžetu kodi, pēc kuriem filtrēt pārskatus                                                |
| Juridiskās personas            | Juridiskās personas, ko var izmantot, lai pārskatu filtrētu pašreizējai juridiskajai personai |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]