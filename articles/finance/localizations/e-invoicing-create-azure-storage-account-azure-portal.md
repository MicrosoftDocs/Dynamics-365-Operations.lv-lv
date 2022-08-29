---
title: Azure krātuves konta izveide Azure portālā
description: Šajā rakstā ir izskaidrots, kā izveidot Azure glabāšanas kontu elektroniskajai rēķinu izrakstīšanai.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291642"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure krātuves konta izveide Azure portālā

[!include [banner](../includes/banner.md)]

Visi elektroniskie faili, ko ģenerējis Elektronisko rēķinu izrakstīšanas pakalpojums vai apstrādes laikā tiek doties uz šo pakalpojumu, tiek glabāti jūsu glabāšanas Microsoft Azure konta konteineros. Lai nodrošinātu, ka elektronisko rēķinu izrakstīšana var piekļūt šiem konteineriem, jums jānodrošina glabāšanas konta koplietojamā piekļuves paraksta (SAS) marķieris Elektronisko rēķinu izrakstīšanas pakalpojumam. Turklāt, lai nodrošinātu, ka marķieris tiek droši saglabāts, nesniedziet SAS marķieri tieši. Tā vietā saglabājiet to Azure atslēgas veikalā un norādiet Azure atslēgas noslēpumu.

1. Atveriet glabāšanas kontu, ko plānojat izmantot elektronisko rēķinu izrakstīšanas pakalpojumā.
2. Dodieties **uz iestatījumu** \> **konfigurāciju** un pārliecinieties, ka **Allow BLOB publiskās piekļuves parametrs** ir iestatīts uz Iespējots.**·**
3. Dodieties uz **datu glabāšanas** \> **konteineriem** un izveidojiet konteineru.
4. Ievadiet konteinera nosaukumu un iestatiet lauku **Publiskās piekļuves līmenis** uz **Privāts (nav anonīmas piekļuves)**.
5. Atveriet jaunu konteineru un dodieties uz iestatījumu **piekļuves** \> **politiku.**
6. Atlasiet **Pievienot politiku**, lai pievienotu saglabāto piekļuves politiku.
7. Atbilstoši iestatiet **lauku** Identifikators.
8. Laukā **Atļaujas** atlasiet visas atļaujas.

    ![Visas atļaujas, kas atlasītas dialoglodziņa Pievienot politiku laukā Atļaujas.](media/e-invoicing-azure-1.png)

9. Ievadiet sākuma un beigu datumu. Beigu datumam jābūt nākotnē.
10. Atlasiet **Labi**, lai saglabātu politiku, un pēc tam saglabājiet izmaiņas konteinerā.
11. Dodieties **uz** \> **iestatījumiem Koplietojamie piekļuves** marķieri un iestatiet lauka vērtības.
12. Ievadiet sākuma un beigu datumu. Beigu datumam jābūt nākotnē.
13. Laukā **Atļaujas** izvēlieties šādas atļaujas:

    - Lasīt
    - Pievienot
    - Izveidot
    - Rakstīt
    - Delete
    - Saraksts

14. Atlasiet **Ģenerēt SAS marķieri un URL**.
15. Kopējiet un saglabājiet vērtību laukā **BLOB SAS URL**. Šī vērtība tiks izmantota vēlāk šajā procedūrā un tiks saukta par koplietoto piekļuves *paraksta URI*.
16. Atveriet galveno akreditācijas datu glabātavu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanu.
17. Dodieties uz **iestatījumu** \> **noslēpumiem** un atlasiet Ģenerēt **/Importēt,** lai izveidotu slepeno.
18. Lapā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāls**.
19. Ievadiet noslēpuma nosaukumu. Šis nosaukums tiks izmantots pakalpojuma iestatīšanas laikā regulēšanas konfigurācijas pakalpojumā (RCS) *un tiks saukts par atslēgas noslēpuma vārdu*. Papildinformāciju par to, kā iestatīt RCS, skatiet [regulēšanas konfigurācijas pakalpojuma (RCS) iestatīšana](e-invoicing-set-up-rcs.md).
20. Laukā **Vērtība** ievadiet koplietoto piekļuves paraksta URI, kas tika nokopēts agrāk.
21. Atlasiet **Izveidot**.
