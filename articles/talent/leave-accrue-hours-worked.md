---
title: Brīvā laika uzkrāšana, balstoties uz nostrādātajām stundām
description: Šajā sadaļā ir sniegta informācija par to, kā atvaļinājuma plānus var konfigurēt, lai uzkrātu laiku pēc nostrādātajām stundām.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461902"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Brīvā laika uzkrāšana, balstoties uz nostrādātajām stundām

## <a name="overview"></a>Pārskats

Organizācijām ar darbiniekiem ar stundu likmi var piešķirt laika uzkrāšanu pēc organizācijā nostrādātajam stundām, nevis pēc darba stāža. Dati par nostrādātajām stundām tiek glabāti laika un apmeklētības sistēmā. 

## <a name="leave-plans"></a>Atvaļinājumu plāni

Atvaļinājuma plānā uzkrājuma veids var būt vai nu nodarbinātības mēnešu skaits vai nostrādātās stundas. Ja atlasīta ir nostrādāto stundu opcija, pieejami ir divu stundu uzkrāšanas veidi: pastāvīgais darba laiks un virsstundas.

Lai iestatītu atvaļinājumu plānu, izmantojot nostrādātās stundas, veiciet tālāk norādītās darbības.

1. Lapā **Atvaļinājumu un prombūtnes plāni** noklikšķiniet uz **Izveidot jaunu plānu**.
2. Ievadiet atvaļinājuma plāna nosaukumu.
3. Atlasiet plānam paredzēto uzkrājuma biežumu.
5. Atlasiet plāna sākuma datumu.
6. Izvēlieties uzkrājuma perioda kritēriju un atlasiet ar darbinieku saistīto datumu atbilstoši situācijai.
7. Uzkrājuma grafikam atlasiet stundu uzkrājuma tipu **Nostrādātās stundas**.
8. Atlasiet uzkrājumam izmantojamo stundu veidu.
9. Ievadiet nostrādāto stundu skaitu un saistīto uzkrājuma summu, minimālo bilanci un maksimālo pārnešanas vai dotācijas summu.

Lai noteiktu uzkrājamo stundu skaitu, nostrādāto stundu plānu uzkrājuma apstrādē izmanto uzkrāšanas biežumu kopā ar uzkrājuma perioda kritēriju.

## <a name="annual-accrual-frequency"></a>Uzkrāšana reizi gadā

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Uzkrāšana reizi mēnesī

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Uzkrāšana divas reizes mēnesī

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6.                     | 8/16/2018-8/31/2018  | 81                  | 6.                  |        
| 8/31/2018             | 80                   | 6.                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Uzkrāšana reizi nedēļā

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Darbiniekam piešķirtie atvaļinājumu plāni

Darbiniekam piešķirtajos atvaļinājumu plānos tiek parādīts tiem paredzētais pakāpes kritērijs un stundu uzkrāšanas veids, kur nostrādāto stundu skaits ir definēts kā uzkrājuma veids. Aktīvajos plānos kā atsauce tiek parādīts uzkrājuma periodos faktiski nostrādāto stundu skaits, sākot no pašreizējā datuma. 

## <a name="loading-data"></a>Notiek datu ielāde

Faktiski nostrādāto stundu skaitu var importēt, izmantojot nostrādāto atvaļinājuma un kavējuma stundu skaita elementu datu pārvaldībā. Ja tiek izmantoti darba laika kalendāri, importēšanas funkcija pārbauda, var pastāvīgi nostrādāto stundu skaists nepārsniedz ieplānoto stundu skaitu dienā, ko nosaka kalendārs. Importēšanas funkcija arī pārbauda, vai konkrētajā dienā nostrādāto stundu skaits nepārsniedz 24 stundas. 

Tālāk sniegtā informācija ir nepieciešama, lai importētu faktisko stundu skaitu, kas jāizmanto atvaļinājuma uzkrāšanas procesā.

+ Personāla numurs 
+ Darbdienas datums
+ tips
+ Stundas

Uz vienu datumu var attiekties tikai viens ar to saistītais veids.

| PERSONĀLA NUMURS       | DARBDIENAS DATUMS           | TIPS                  | STUNDAS                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regulārs               | 8                    |       
| 000337                | 8/7/2018             | Regulārs               | 8                    |
| 000337                | 8/7/2018             | Virsstundas              | 3                    |
| 000337                | 8/8/2018             | Regulārs               | 8                    |
| 000337                | 8/7/2018             | Regulārs               | 8                    |
| 000337                | 8/9/2018             | Regulārs               | 8                    |
