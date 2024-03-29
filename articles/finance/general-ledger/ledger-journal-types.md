---
title: Virsgrāmatas žurnālu veidi
description: Šajā rakstā ir aprakstīti žurnālu tipi, ko var iestatīt finanšu žurnāliem.
author: kweekley
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883c54b84ed31384a28c31c8b814c75d340d020e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901318"
---
# <a name="ledger-journal-types"></a>Virsgrāmatas žurnālu veidi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti žurnālu tipi, ko var iestatīt finanšu žurnāliem. Izmantojiet žurnālu **nosaukumu lapu**, lai iestatītu žurnālus, ko varat izmantot visā Dynamics 365 Finance.

| Žurnāla veids                      | Nolūks                       | Ievadiet darbības šajā lapā                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Sadalījums                        | Izveidojiet sadalījuma darbības sadalījuma žurnālā. Pirms izveidojat iedales žurnālu, jāizveido iedales noteikums lapā **Virsgrāmatas sadalījuma noteikumi**.      | Apstrādāt piešķiršanas pieprasījumu             |
| Apstiprinājums                          | Grāmatojiet apstiprinātos kreditoru rēķinus, kas ir apstiprināti atbilstošajos Virsgrāmatas kontos.  | Rēķinu apstiprināšanas žurnāls                                       |
| Bankas čeka atgriešana               | Atsauciet grāmatoto čeku. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Maksājumu atgriešanai izmantot pārskatīšanas procesu** lapā **Skaidras naudas un bankas pārvaldības parametri**.   | Čeku atcelšana, maksājumu atgriešana                   |
| Bankas depozīta kvīts atcelšana    | Atceliet depozīta kvīti. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Depozīta kvīts maksājumu atcelšanai izmantot pārskatīšanas procesu** lapā **Skaidras naudas un bankas pārvaldības parametri**.   | Depozīta kvīts maksājumu atcelšanas gadījumi            |
| Budžets                            | Apstrādājiet budžeta asignējumus. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Iespējot budžeta asignēšanu** lapā **Virsgrāmatas parametri**. Budžeta žurnāla ierakstos tiks ietverta informācija, kas ir balstīta uz Virsgrāmatas kontiem, kuri ir definēti lapā **Grāmatošanas definīcijas** page.                                                        |                                                                |
| Debitora vekseļa pieņemšana  | Izveidojiet debitoru pieņemšanas darbības attiecībā uz vekseļiem.             | Vekseļu izrakstīšanas žurnāls – Vekseļu atkārtotas izrakstīšanas žurnāls |
| Debitora bankas pārskaitījums          | Izveidojiet vekseļa pārskaitījuma failu, kuru var nosūtīt uz jūsu organizācijas banku. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Automātiska darbību nosegšana** lapā **Debitoru** **moduļa parametri**.            | Pārskaitījums                                                     |
| Debitora izrakstīts vekselis    | Izveidojiet debitora izrakstītu vekseļu darbības. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Izveidot un grāmatot izrakstīšanas žurnālu automātiski, kad tiek grāmatoti rēķini** lapā **Maksāšanas metodes - debitori**.   | Vekseļu izrakstīšanas žurnāls                                  |
| Debitora maksājums                  | Izveidojiet debitora maksājumu darbības.                             | Maksājumu žurnāls             |
| Debitora vekseļa noraidīšana | Izveidojiet debitora vekseļa noraidīšanas darbības.                    | Vekseļu noraidīšanas žurnāls                               |
| Atkārtoti izrakstīts debitora vekselis  | Izveidojiet debitora atkārtoti izrakstītu vekseļu darbības.                     | Atkārtotas vekseļu izrakstīšanas žurnāls                                |
| Debitoru vekseļu apmaksa  | Izveidojiet debitora vekseļu apmaksas darbības.                       | Vekseļu apmaksas žurnāls                                |
| Ikdienas                             | Izveidojiet ikdienas darbības Virsgrāmatas žurnālā.                          | Virsgrāmatas žurnāls                                                |
| Korekcijas                       | Izveidojiet korekciju darbības korekciju žurnālā. Lai izmantotu šo žurnāla tipu, atlasiet opcijas **Lietot finanšu dzēšanas apstrādei** un **Lietot finanšu konsolidācijai** lapā **Juridiskas personas**. Pirms šī žurnāla veida izmantošanas jums ir jāizveido Virsgrāmatas korekcijas noteikums lapā **Virsgrāmatas korekcijas noteikums**. | Korekcijas                                                    |
| Pamatlīdzekļu budžets                | Izveidojiet pamatlīdzekļu budžeta reģistra ierakstus.                                                                                                                                                                                                                                                                                                                 | Pamatlīdzekļu budžets                                             |
| Rēķinu reģistrs                  | Reģistrējiet pamatinformāciju par kreditora rēķiniem.                                                                                                                                                                                                                                                                                                           | Rēķinu reģistrs                                               |
| Algu izdevumi              | Veiciet maksājumus, kas ir balstīti uz algu pārskatiem. Jūs nevarat manuāli ievadīt darbības šajā žurnālā. Jums ir jāģenerē algu pārskati un pēc tam jāiesniedz šie pārskati maksājumam.                                                                                                                                                              |                                                                |
| Periodisks                          | Izveidojiet periodiskas darbības periodiskajam žurnālam.                                                                                                                                                                                                                                                                                                      | Periodiskie žurnāli                                              |
| Pamatlīdzekļu grāmatošana                 | Grāmatojiet pamatlīdzekļu darbības.                                                                                                                                                                                                                                                                                                                              | Pamatlīdzekļi                                                   |
| Projekts - Izdevumi                | Izveidojiet projekta izdevumu darbības.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Pārskata valūtas korekcija     | Izveidojiet korekcijas pārskata valūtā bilancēm virsgrāmatas kontos.               | Pārskata valūtas korekcijas žurnāli                         |
| Statistikas darbības            | Izveidojiet statistikas darbības.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Kreditora bankas pārskaitījums            | Izveidojiet parādzīmes pārskaitījuma failu, kuru var nosūtīt uz jūsu organizācijas banku.                                                                                                                                                                                                                                                                      | Pārskaitījumu žurnāls                                             |
| Kreditoru rēķinu apmaksa               | Izveidojiet kreditora rēķinu apmaksas darbības.                                                                                                                                                                                                                                                                                                                    | Maksājumu žurnāls                                                |
| Kreditora parādzīmes izrakstīšana       | Izrakstiet kreditoru parādzīmes kā maksājuma metodi. Lai izmantotu šo žurnāla tipu, atlasiet opciju **Izveidot un grāmatot izrakstīšanas žurnālu automātiski, kad tiek grāmatoti rēķini** lapā **Maksāšanas metodes - kreditori**.                                                                                                                                          | Parādzīmju izrakstīšanas žurnāls                                   |
| Negrāmatota kreditoru rēķinu kopa | Izveidojiet kreditora rēķinu darbības, kas vēl nav iegrāmatotas pagaidu saņemšanas kontā.                                                                                                                                                                                                                                                             | Kreditora rēķinu kopa bez detalizētās informācijas par grāmatošanu                  |
| Kreditora rēķinu kopa               | Izveidojiet kreditoru rēķinu kopas darbības.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Kreditora rēķina reģistrēšana          | Grāmatojiet kreditoru rēķinus, kas ir žurnālā.                                                                                                                                                                                                                                                                                                                 | Rēķinu žurnāls                                                |
| Atkārtoti izrakstīta kreditora parādzīme     | Atkārtoti izrakstiet parādzīmi, ko iepriekš izpirkusi jūsu organizācijas banka.                                                                                                                                                                                                                                                                      | Parādzīmju izlikšanas žurnāls                                 |
| Kreditoru parādzīmju apmaksa     | Izveidojiet kreditora parādzīmes segšanas darbības.                                                                                                                                                                                                                                                                                                          | Parādzīmju apmaksas žurnāls                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
