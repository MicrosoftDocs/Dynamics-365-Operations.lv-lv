---
title: Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem
description: Šajā rakstā skaidrots, kā var izmantot darbplūsmas, lai pārvaldītu darbinieku informāciju.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750739"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts, kā varat izmantot darbplūsmu iespējas, lai Human resources pārvaldītu darbinieku informāciju. Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu.

Personāla vadības darbplūsmu iespējas nodrošina vairākas darbplūsmas personāla vadības darbību pārvaldībai. Turklāt ir pieejamas vairākas opcijas, kas sniedz iespēju modificēt noteiktas darbplūsmas un saistīt tās ar padotības hierarhiju. Darbplūsmas ir pieejamas, lai palīdzētu pārvaldīt izmaiņas vairāku tipu darbinieku informācijā. Varat saistīt darbplūsmu ar pozīciju. Šādā gadījumā, ja darbinieki maina savu darbinieka ierakstu, tiek sākta darbplūsma, kas pieprasa apstiprināšanu pirms jaunās informācijas saglabāšanas. Darbplūsmas ir iepriekš definētas šāda veida informācijai, lai palīdzētu efektīvi pārvaldīt izmaiņas un uzturēt darbinieku datus precīzi:

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

Kad darbinieki tiek pieņemti darbā, pārcelti citā amatā vai ar viņiem tiek pārtrauktas darba attiecības, darbplūsma var tikt ietverts pārskatīšanas process. Šādā veidā dokumentu var pārskatīt vai darbības noteikumus var definēt kā daļu no darbplūsmas. Kad pārskatīšanas process ir pabeigts, dokuments vai darbība tiek pabeigta un darbplūsma pāriet pie galīgās apstiprināšanas darbības.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Darbplūsmas saistīšana ar padotības hierarhiju

Jūs varat saistīt darbplūsmu ar jebkuru jūsu konfigurēto amatu hierarhiju. Divi hierarhijas tipi tiek izmantoti darbplūsmas maršrutēšanai: vadības **un** konfigurējams **·**.

- Vadības **hierarhija** parāda uzņēmuma vai organizācijas pārskata struktūru. Papildinformāciju par šo hierarhijas tipu skatiet sadaļā [Pārskati par amatu](hr-personnel-positions.md#reports-to-position).
- Konfigurējama **hierarhija** pārstāv matricu vai pielāgotu hierarhiju. Plašāku informāciju par šo hierarhijas tipu skatiet sadaļā [Attiecības](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Vadības hierarhijas piemērs

Varat konfigurēt darbplūsmu tā, ka tad, kad darbinieks iesniedz pirkšanas pieprasījumu jaunam datoram, pieprasījums tiek maršrutēts darbinieka vadītājam un izlaist līmeņa pārvaldniekam. Konfigurējot darbplūsmas soli, piešķires tipa lauku **iestatiet** uz **Hierarhija**. Pēc **tam ir pieejama** cilne Hierarhijas tips. Šajā piemērā atlasiet vadības **hierarhiju**.

### <a name="configurable-hierarchy-example"></a>Konfigurējamas hierarhijas piemērs

Ja amats ir saistīts ar matricas pārskata hierarhiju, darbinieka vadītāja vietā varat konfigurēt darbplūsmu, kas maršrutē izdevumus noteiktam projektam uz projekta potenciālo klientu. Šajā gadījumā piešķires tipa lauku **iestatiet** uz **Hierarhija**. Pēc tam cilnē **Hierarhijas** tips atlasiet konfigurējamu **hierarhiju**. Pēc darbplūsmas iestatīšanas atlasiet saistīt hierarhiju darbplūsmas iestatīšanas lapā, **·** **lai** atlasītu hierarhiju, kas jāizmanto darbplūsmas maršrutēšanai.

> [!IMPORTANT]
> Kad dokuments, darbība vai galvenais ieraksts tiek iesniegts darbplūsmas apstiprināšanai, ieslēga primārais amats tiks izmantots, lai noteiktu, kurš dokuments tiks maršrutēts uz nākamo.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarhijas iestatījums Darbplūsmas parametros

1. Lapā Darbplūsmas **parametri dodieties** uz sadaļu **Hierarhijas maršrutēšana**.
2. Pēc noklusējuma opcija Izmantot **pozīciju hierarhiju** ir iestatīta uz **Nē**. Šajā gadījumā darbplūsma izmantos darbinieka primāro pozīciju, kad tā pārvietos hierarhiju. Iestatiet opciju Jā **,** lai darbplūsmai izmantotu pozīcijas pamatelementu, kad tā navigē hierarhiju.

### <a name="additional-example"></a>Papildu piemērs 

Darbiniekam Grace Sturman ir divi amati: konsultants un darbinieks. Pagarinājuma primārais amats ir galvenais amats. Kad viņai nav apmācības jauno darbinieku, viņa ir pieejama darbā ar konsultantu. Izmantojot viņas primāro amatu, pagarinājuma pārskati Sietai, cilvēkresursu direktoram. Kases pārskati Siam. Viņas konsultanta amatam Pagarinājumam ir vairākas punktlīnijas attiecības atkarībā no projekta.

Pagarinājuma uzņēmums izveido darbplūsmas maršrutēšanas kārtulas, kuru **pamatā** ir konfigurējama hierarhija (matricas/projekta hierarhijas). Šajā hierarhijā tiek izmantots pagarinājuma konsultanta amats. Ja opcija **Izmantot** **pozīciju hierarhiju ir iestatīta uz Nē**, kad dokuments tiek maršrutēts uz Pagarinājumu viņas apstiprinājumam, darbplūsma meklēs viņas primāro pozīciju (iestatīta), lai noteiktu, kur dokuments tiks maršrutēts tālāk. Šajā gadījumā tas vispirms tiks maršrutēts uz Džo un tad uz Džo. Ja opcija ir **iestatīta** uz Jā un darbplūsma izmanto konfigurējamu hierarhiju, darbplūsma meklēs Pagarinājuma konsultanta pozīciju un pārskatu sniegšanas saistības, **lai** noteiktu, kur dokuments tiks maršrutēts tālāk.

### <a name="configure-a-human-resources-workflow"></a>Personāla vadības darbības konfigurēšana
Lai konfigurētu pamata darbplūsmu, kas tiek sākta, kad darbinieks pieprasa savas personiskās informācijas izmaiņas, veiciet tālāk norādītās darbības.

1.  **Cilvēkresursu darbplūsmu lapā** atlasiet **Jauns**.
2.  Pieejamo darbplūsmu sarakstā atlasiet vienumu **Identifikācijas numuri**.
3.  Atlasiet **Palaist,** lai atvērtu darbplūsmas veidotāju, un pēc tam ievadiet lietotājvārdu un paroli.
4.  Pārvietot apstiprinājuma **identifikācijas numura elementu** no darbplūsmas elementu saraksta uz veidotāja kanvas.
5.  Savienojiet apstiprināšanas elementu ar elementiem **Sākt** un **Pabeigt**.
6.  Veiciet dubultklikšķi uz elementa **Apstiprināt**, atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet **Rekvizīti**.
7.  Veiciet tālāk norādītās darbības, lai pievienotu darbplūsmas elementa instrukcijas.

    1.  Atlasiet vienumu **Piešķire** un pēc tam piešķires veida sadaļā atlasiet vienumu **Hierarhija**.
    2.  Sadaļā **Hierarhija** atlasiet vienumu **Konfigurējama hierarhija**.
    3.  Pievienojiet apturēšanas nosacījumu un aizveriet lapu.

8.  Izpildiet visas papildu instrukcijas.
9.  Atlasiet **Saglabāt un aizvērt**. Kad tiek atvērts dialoglodziņš, aktivizējiet jauno darbplūsmu un atlasiet vienumu **Padarīt aktīvu**.
10. Pārejiet uz sadaļu **Personāla vadība** &gt; **Pozīcijas** &gt; **Pozīciju hierarhijas tipi**.
11. Atlasiet vienumu **Matrica**.
12. Pievienojiet sarakstam darbplūsmu **Nodarbinātā identifikācijas numurs**.

## <a name="additional-resources"></a>Papildu resursi

[Skatīt un pārvaldīt adreses izmaiņas](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
