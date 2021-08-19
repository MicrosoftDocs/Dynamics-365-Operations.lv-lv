---
title: Integrētā virsgrāmata
description: Šajā tēmā ir aprakstīta virsgrāmatas datu integrācija starp Finance and Operations un citām Dynamics 365 programmām, izmantojot Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 18a95725af8014845d6fb39806917de7632ad56b92b75387cd916de927127b38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723085"
---
# <a name="integrated-ledger"></a>Integrētā virsgrāmata

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas. Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto. Šī tēma apraksta šo pamata finanšu datu integrēšanu.

## <a name="templates"></a>Veidnes

Virsgrāmatas dati ietver pamata finanšu tabulas vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Customer engagement programmas     | Apraksts
---------------------------------|----------------------------------|------------
[CDS maiņas kursi](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Kontu plāns](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valūtas](mapping-reference.md#218) | transactioncurrencies |
[Maiņas kursa valūtu pāris](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Maiņas kursa veids](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Finanšu dimensijas formāts](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Finanšu dimensijas](mapping-reference.md#128) | msdyn_dimensionattributes |
[Elements Finanšu kalendāra integrācija](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Finanšu kalendāra periods](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Elements Finanšu kalendāra gada integrācija](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Galvenais konts](mapping-reference.md#152) | msdyn_mainaccounts |
[Galvenā konta kategorijas](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
