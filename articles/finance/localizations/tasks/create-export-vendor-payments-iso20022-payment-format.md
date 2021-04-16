---
title: Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022
description: Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822709"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.

Šī ir piektā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju. Lai izpildītu šo piemēru, izmantojiet DEMF demonstrācijas datus.

## <a name="example"></a>Paraugs

1.    Pārejiet uz sadaļu **Kreditori > Maksājumi > Maksājumu žurnāls**.
2.    Klikšķiniet **Jauns**.
3.    Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
4.    Noklikšķiniet uz **Rindas >Maksājuma priekšlikums > Izveidot maksājuma priekšlikumu**.
5.    Izvērsiet sadaļu **Iekļaujamie ieraksti**.
6.    Noklikšķiniet uz **Filtrēt**.
7.    Sarakstā atlasiet vienumam **Kreditoru tabula** un **Kreditora konta lauks** atbilstošo rindu.
8.    Ievadiet vai atlasiet vērtību laukā **Kritēriji**. Apmaksājamo kreditoru transakciju atlasei varat izmantot jebkuru kritēriju, šī piemēra ietvaros izmantojiet kreditora kontu DE-001.
12.    Noklikšķiniet uz **Labi**.
13.    Noklikšķiniet uz **Labi**.
14.    Noklikšķiniet uz **Izveidot maksājumus**.
15. Ģenerējiet ISO20022 maksājuma failu.
    1.    Noklikšķiniet uz **Ģenerēt maksājumus**.
    2.    Ievadiet vai atlasiet vērtību laukā **Maksājuma metode**.
    3.    Ievadiet vērtību laukā **Faila nosaukums**. Šī piemēra ietvaros ģenerētas fails būs saderīgs ar SEPA, jo maksājuma valūta ir EUR. Lai ģenerētu maksājumus citās valūtās, var izmantot arī ISO20022 kredīta pārskaitījumu, kā arī citus kreditora maksājumu formātus
    4.    Ievadiet vai atlasiet vērtību laukā **Bankas konts**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]