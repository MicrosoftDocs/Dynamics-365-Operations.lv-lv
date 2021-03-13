---
title: Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem
description: Šajā rakstā ir aprakstīts, kā varat izmantot darbplūsmu iespējas, lai Human resources pārvaldītu darbinieku informāciju. Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c5bb0a363a3094626d81af3d5ffea38d9a1b12a8
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129807"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem

Šajā rakstā ir aprakstīts, kā varat izmantot darbplūsmu iespējas, lai Human resources pārvaldītu darbinieku informāciju. Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu.

Personāla vadības darbplūsmu iespējas nodrošina vairākas darbplūsmas personāla vadības darbību pārvaldībai. Turklāt ir pieejamas vairākas opcijas, kas sniedz iespēju modificēt noteiktas darbplūsmas un saistīt tās ar padotības hierarhiju. Ir pieejamas darbplūsmas, kas palīdz pārvaldīt dažādu standarta darbinieku informācijas veidu izmaiņas. Varat saistīt darbplūsmu ar pozīciju. Šādā gadījumā, ja darbinieki maina savu darbinieka ierakstu, tiek sākta darbplūsma, kas pieprasa apstiprināšanu pirms jaunās informācijas saglabāšanas. Ir pieejamas iepriekš definētas tālāk norādītās informācijas darbplūsmas, kas palīdz efektīvi pārvaldīt izmaiņas un uzturēt darbinieku datus pareizus.

-   Identifikācijas numuri
-   Kursi
-   Izglītība
-   Attēls
-   Patapinātie krājumi
-   Profesionālā pieredze
-   Projektu pieredze
-   Prasmes
-   Atbildīgie amati
-   Personāla vadības darbības
-   Kursu reģistrācija

Kad darbinieki tiek pieņemti darbā, pārcelti citā amatā vai ar viņiem tiek pārtrauktas darba attiecības, darbplūsma var tikt ietverts pārskatīšanas process. Tādējādi darbplūsmas ietvaros var tikt pārskatīts dokuments vai darbības nosacījumi. Kad pārskatīšanas process ir pabeigts, dokuments vai darbība tiek pabeigta un darbplūsma pāriet pie galīgās apstiprināšanas darbības.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Darbplūsmas saistīšana ar padotības hierarhiju
Varat saistīt darbplūsmu ar jebkuru konfigurēto hierarhiju. Piemēram, ja pozīcija ir saistīta ar matricas padotības hierarhiju, varat konfigurēt darbplūsmu, kas nodrošina noteikta projekta izmaksu novirzīšanu projekta vadītajam, nevis tā darbinieka vadītājam, kurš ir saistīts ar šo pozīciju. Lai izveidotu jaunu darbplūsmu vai modificētu esošu darbplūsmu, lapā **Personāla vadības darbplūsmas** noklikšķiniet uz **Jauna**. Sarakstā atlasiet darbplūsmu, lai palaistu darbplūsmu noformētāju. Varat izmantot noformētāju, lai izveidotu jaunu darbplūsmu vai mainītu esošas darbplūsmas darbības. Ja maināt esošu darbplūsmu, izmaiņas tiek saglabātas kā jauna versija. Tāpēc vienmēr varat atgriezieties pie iepriekšējās versijas, ja tas ir nepieciešams.

## <a name="configure-a-human-resources-workflow"></a>Personāla vadības darbības konfigurēšana
Lai konfigurētu pamata darbplūsmu, kas tiek sākta, kad darbinieks pieprasa savas personiskās informācijas izmaiņas, veiciet tālāk norādītās darbības.

1.  Lapā **Personāla vadības darbplūsmas** noklikšķiniet uz **Jauna**.
2.  Pieejamo darbplūsmu sarakstā atlasiet vienumu **Identifikācijas numuri**.
3.  Noklikšķiniet uz **Palaist**, lai palaistu darbplūsmu noformētāju, un pēc tam ievadiet savu lietotājvārdu un paroli, kad tiek parādīta attiecīga uzvedne.
4.  Velciet elementu **Apstiprināt identifikācijas numuru** no darbplūsmas elementu saraksta uz noformētāja rāmi.
5.  Savienojiet apstiprināšanas elementu ar elementiem **Sākt** un **Pabeigt**.
6.  Veiciet dubultklikšķi uz **Apstiprināt elementu**, noklikšķiniet ar peles labo pogu un atlasiet vienumu **Rekvizīti**.
7.  Veiciet tālāk norādītās darbības, lai pievienotu darbplūsmas elementa instrukcijas.
    1.  Atlasiet vienumu **Piešķire** un pēc tam piešķires veida sadaļā atlasiet vienumu **Hierarhija**.
    2.  Sadaļā **Hierarhija** atlasiet vienumu **Konfigurējama hierarhija**.
    3.  Pievienojiet apturēšanas nosacījumu un aizveriet lapu.

8.  Izpildiet visas papildu instrukcijas (nedrīkst būt neviens papildu brīdinājums).
9.  Noklikšķiniet uz **Saglabāt un aizvērt**. Kad tiek atvērts dialoglodziņš, aktivizējiet jauno darbplūsmu un atlasiet vienumu **Padarīt aktīvu**.
10. Pārejiet uz sadaļu **Personāla vadība** &gt; **Pozīcijas** &gt; **Pozīciju hierarhijas tipi**.
11. Atlasiet vienumu **Matrica**.
12. Pievienojiet sarakstam darbplūsmu **Nodarbinātā identifikācijas numurs**.

## <a name="additional-resources"></a>Papildu resursi

[Skatīt un pārvaldīt adreses izmaiņas](hr-personnel-view-address-changes.md) 



