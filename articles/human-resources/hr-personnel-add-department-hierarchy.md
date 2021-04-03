---
title: Nodaļu izveide un ietveršana nodaļu hierarhijā
description: Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu. Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību. Nodaļas var izmantot, lai ziņotu par funkcionālām jomām. Nodaļām var būt peļņas un zaudējumu atbildība.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 723e46f98545e80551da9f79b6aeffc3eca48830
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466018"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Nodaļu izveide un ietveršana nodaļu hierarhijā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu. Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību. Nodaļas var izmantot, lai ziņotu par funkcionālām jomām. Nodaļām var būt peļņas un zaudējumu atbildība.

Nodaļu var ietvert izmaksu centru grupā. Pozīcijas var piešķirt nodaļām. Lai izveidotu nodaļu, noklikšķiniet uz **Personāla vadība** &gt; **Nodaļas** &gt; **Nodaļa**. Nākamajā tabulā ir aprakstīti pieejamie lauki.

| Lauks               | Apraksts                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nosaukums                | Ievadiet struktūrvienības nosaukumu.                                                                                                                                                                                  |
| Nodaļas numurs   | Noklusējuma vērtība var tikt automātiski ģenerēta, ja numuru sērijas kods ir piešķirts atsaucei **Organizācijas numurs** lapā **Numuru sērijas**.                                                 |
| Meklēšanas nosaukums         | Ievadiet nosaukumu vai akronīmu, ko var izmantot nodaļas meklēšanai.                                                                                                                                            |
| Atgādne                | Ievadiet papildinformāciju šeit.                                                                                                                                                                            |
| Hierarhijā        | Atzīmētā izvēles rūtiņa nozīmē, ka nodaļa ir iekļauta nodaļu hierarhijā. Informāciju par to, kā pievienot nodaļu nodaļu hierarhijai, skatiet tālāk šajā rakstā. |
| Universālās datu numerācijas sistēmas (DUNS) numurs         | DUNS nozīmē universālo datu numerācijas sistēmu. Tas ir deviņu ciparu numurs, ko piešķir Dun & Bradstreet.                                                                                                     |
| Vadītājs             | Ievadiet personu, kas pārvalda nodaļu.                                                                                                                                                                    |
| Adreses           | Pievienojiet nodaļai adreses informāciju. Piemēram, pievienojiet pasta adresi ēkai, kas atrodas struktūrvienība.                                                                          |
| Kontaktinformācija | Pievienojiet nodaļai kontaktinformāciju. Piemēram, pievienojiet struktūrvienības informācijas nodaļas tālruņa numuru.                                                                                           |

Lai pievienotu nodaļu nodaļu hierarhijai, rīkojieties šādi.

1.  Noklikšķiniet uz **Personāla vadība** &gt; **Nodaļas** &gt; **Nodaļu hierarhija**.
2.  Noklikšķiniet uz **Rediģēt** un pēc tam atlasiet organizāciju, kurā jābūt nodaļai.
3.  Noklikšķiniet uz **Iespraust** un sarakstā atlasiet **Nodaļa**.
4.  Nodaļu sarakstā, kas parādās, atlasiet nodaļu, ko pievienot hierarhijai.
5.  Saglabājiet izmaiņas. Jūs saņemsiet ziņojumu, ka ir izveidota hierarhijas melnraksta versija.
6.  Kad esat pabeidzis, hierarhijas veidotājā noklikšķiniet uz **Publicēt**. Varat ievadīt spēkā stāšanās datumu, kas norāda, kad šī hierarhija ir jāpublicē. Piemēram, lai pievienotu jaunu nodaļu nākamā kalendārā gada sākumā, iestatiet spēkā stāšanās datumu uz jaunā kalendāra gada 1. janvāri. Hierarhijas izmaiņas stāsies spēkā šajā datumā.

## <a name="steps-for-creating-a-department"></a>Norādījumi par nodaļas izveidi
Sīku jaunas nodaļas izveides procedūras aprakstu skatiet rakstā [Jaunu nodaļu definēšana](../fin-and-ops/hr/tasks/define-new-departments.md). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]