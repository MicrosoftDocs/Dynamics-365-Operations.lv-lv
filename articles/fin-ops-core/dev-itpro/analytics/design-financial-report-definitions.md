---
title: Atskaišu definīcijas finanšu atskaišu veidotājā
description: Šajā rakstā ir sniegta informācija par atskaišu definīcijām.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802557"
---
# <a name="report-definitions-in-financial-report-designer"></a>Atskaišu definīcijas finanšu atskaišu veidotājā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par atskaišu definīcijām. Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai. 

Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Pārskata definīcijā arī ir papildu opcijas un iestatījumi, kurus varat izmantot pārskata pielāgošanai. Pēc rindu un kolonnu definīciju izveides, tās ir jāapvieno pārskata definīcijā. Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu. Tad varat saglabāt un izveidot atskaiti. Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:

- Finanšu
- Finanšu un konta
- Finanšu, konta un darbības

Taču atkarībā no tā, kā dati tiek glabāti Microsoft Dynamics ERP sistēmā, pārskatos var nebūt pieejami darbību dati.

## <a name="create-a-report-definition"></a>Izveidojiet pārskata definīciju
1. Pārskatu veidotājā izvēlnē Fails **noklikšķiniet** uz Jauns **un** pēc tam atlasiet **Pārskata definīcija**.
2. Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.

## <a name="contents-of-a-report-definition"></a>Pārskata definīcijas saturs
Tālāk redzamajā tabulā ir aprakstītas pārskata definīcijas cilnes un informācijas izmantošanas veids.

<table>
<thead>
<tr>
<th>Cilne</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pārskats</td>
<td>Izveidojiet, konfigurējiet vai modificējiet pārskatu.</td>
</tr>
<tr>
<td>Izvade un sadale</td>
<td>Mainiet pārskata izvades veidu un atrašanās vietu.</td>
</tr>
<tr>
<td>Galvenes un kājenes</td>
<td>Norādiet un formatējiet pārskata galvenes un kājenes. Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē. Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem. Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</td>
</tr>
<tr>
<td>Iestatījumi</td>
<td>Norādiet pārskata definīcijas iestatījumu, piemēram:
<ul>
<li>Formatējums un noapaļošanas summas</li>
<li>Formatēt detalizētos pārskatus</li>
<li>Formatēt pārskatu kokus</li>
<li>Ģenerēt izņēmumu pārskatu</li>
<li>Norādiet valūtas konversiju</li>
<li>Apakšsummas un filtru konta detaļas</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskati](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
