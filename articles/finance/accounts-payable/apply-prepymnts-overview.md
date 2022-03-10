---
title: Automātiski lietot priekšapmaksu kreditoru rēķiniem
description: Šajā tēmā aprakstīta iespēja automātiski piemērot priekšapmaksas kreditoru rēķiniem.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8583962c41a7ac5e27463f325ddc2ccd367331cc
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358223"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automātiski lietot priekšapmaksu kreditoru rēķiniem

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta iespēja automātiski piemērot priekšapmaksas kreditoru rēķiniem. Priekšapmaksu var izveidot pirkšanas pasūtījumam kā daļu no pirkšanas līguma. Pēc kreditora rēķina saņemšanas priekšapmaksu var izmantot, lai nokārtotu kreditoru rēķinus. Jaunā funkcija ļauj sistēmai automātiski izmantot pirkšanas pasūtījumu numurus kreditora rēķinā, lai iegūtu atbilstošas priekšapmaksas, kad kreditora rēķins tiek importēts.

Ja tiek atrastas un lietotas priekšapmaksas, rindas tiek pievienotas esošajām rēķina rindām, lai piemērotu priekšapmaksas. Priekšapmaksas rindas nekad netiek uzskatītas rēķinu salīdzināšanas procesa laikā.

Sekojošos punktus aprakstīts, kā tiek pielietotas priekšapmaksas, ja tiek sekots dažādiem iepirkumu procesiem:

- **Viens kreditora rēķins uz pirkšanas pasūtījumu** – priekšapmaksa pirkšanas pasūtījumā tiks piemērota kreditora rēķinam.
- **Viens kreditora rēķins vairākiem pirkšanas pasūtījumiem** – priekšapmaksa visiem pirkšanas pasūtījumiem tiks piemērota kreditora rēķinam.
- **Vairāki kreditora rēķini uz pirkšanas pasūtījumu** – priekšapmaksa pirkšanas pasūtījumā tiks piemērota pirmajam importētajam kreditora rēķinam. Ja priekšapmaksas summa pārsniedz rēķina summu, priekšapmaksas pieteikums neizdodas, un priekšapmaksu jums ir jāpiemēro manuāli.
- **Vairāki kreditora rēķini vairākiem pirkšanas pasūtījumiem** – priekšapmaksa pirkšanas pasūtījumiem tiks piemērota pirmajam saistošajam rēķinam. Ja priekšapmaksas summa pārsniedz rēķina summu, priekšapmaksas pieteikums neizdodas, un priekšapmaksu jums ir jāpiemēro manuāli. Ja jebkādas priekšapmaksas, kas paliek pēc priekšapmaksu grāmatošanas, tiek piemērotas pirmajam rēķinam, tās var piemērot rēķiniem, kas seko.

Ja mēģinājums piemērot priekšapmaksu neizdodas, **bloķēšanas turpinājuma automatizācijas procesa iestatīšana** priekšapmaksas programmas kļūmes gadījumā noteiks nākamās darbības:

- **Jā** - automatizācijas vēsturē ir pievienots kļūdas ziņojums "Automātiska priekšapmaksas lietošana: neizdevās", un rēķins paliek neizlemto kreditoru rēķinu sarakstā. Rēķins paliek bloķēts līdz brīdim, kad priekšapmaksa tiks lietota manuāli.

Lai manuāli piemērotu priekšapmaksas, dodieties uz neizlemto kreditora rēķinu. Lapā **Detalizēta informācija par rēķinu** iestatiet bloķētā rēķina opciju **Iekļaut automatizētā apstrādē** uz **Nē**. Tagad priekšapmaksu var piemērot manuāli. Kad priekšapmaksa ir lietota, iestatiet automātiskās apstrādes opciju **Iekļaut automatizētā apstrādē** atpakaļ uz **Jā**, lai rēķinu varētu automātiski apstrādāt.

Varat arī apiet automātisko priekšapmaksas lietojumprogrammu, iestatot opciju **Iekļaut automatizētā apstrādē** uz **Nē** un pēc tam iestatot to atpakaļ uz **Jā**. Jūs saņemsit šādu ziņojumu: "Pirkšanas pasūtījumam jau pastāv priekšapmaksa. Vai vēlaties to ignorēt atlasītajam kreditora rēķinam?" Atlasiet **Jā**. Ziņojums "Manuāli apietās priekšapmaksas pieteikums" tiek pievienots automatizācijas vēsturei, un kreditora rēķins netiks bloķēts, ja automatizētais process tiek palaists vēlreiz.

- **Nē** – sekošanas automatizācijas procesi turpināsies. Šo priekšapmaksu joprojām var lietot segšanas laikā.
