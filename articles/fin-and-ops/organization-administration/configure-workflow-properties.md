---
title: "Konfigurēt darbplūsmas rekvizītus"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba03473dd6fc31d51fd4e890acac1cd1494ef5a3
ms.openlocfilehash: a327b85f18f03294a237c3795ae2e1f4a97095f0
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="configure-workflow-properties"></a>Konfigurēt darbplūsmas rekvizītus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt dažādus darbplūsmas rekvizītus.

Lai konfigurētu darbplūsmas rekvizītus, atveriet darbplūsmu, izmantojot darbplūsmas redaktoru. Noklikšķiniet uz darbplūsmas redaktora audekla un pēc tam noklikšķiniet uz vienuma **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Varat izmantot tālāk aprakstītās procedūras, lai konfigurētu dažādus darbplūsmas rekvizītus.

## <a name="name-the-workflow"></a>Darbplūsmas nosaukums
Veiciet šādas darbības, lai ievadītu darbplūsmas nosaukumu.

1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Laukā **Nosaukums** ievadiet darbplūsmas unikālo nosaukumu. Piemēram, izveidojot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, varat nosaukt pirkšanas pieprasījuma darbplūsmu **Pirkuma pieprasījumi Dānija** vai **Pirkuma pieprasījumi Spānija**.

## <a name="specify-the-workflow-owner"></a>Norādiet darbplūsmas īpašnieku
Darbplūsmas īpašnieks ir persona, kura pārvalda un uztur attiecīgo darbplūsmu. Veiciet šīs darbības, lai norādītu darbplūsmas īpašnieku.

1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Sarakstā **Īpašnieks** izvēlieties tās personas vārdu, kura pārvaldīs darbplūsmu.

## <a name="select-an-email-template"></a>E-pasta veidnes atlasīšana
Veiciet šīs darbības, lai atlasītu e-pasta veidni, kas tiek izmantota, lai ģenerētu ziņojumus par darbplūsmu.

1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Sarakstā **E-pasta veidne darbplūsmas paziņojumiem** atlasiet veidni.

## <a name="enter-instructions-for-users"></a>Ievadiet instrukcijas lietotājam
Varat sniegt informāciju lietotājiem, kuri iesniedz dokumentus apstrādei un apstiprināšanai. Šie lietotāji tiek saukti arī par *veidotājiem*. Piemēram, jūs veidojat pirkuma pieprasījumu darbplūsmu un ievadāt instrukcijas. Šīs instrukcijas varēs skatīt lietotāji, kuri ievada pirkuma pieprasījumus lapā **Pirkuma pieprasījumi**. Lai skatītu instrukcijas, veidotājs noklikšķina uz ikonas darbplūsmas ziņojumu joslā. Veiciet šīs darbības, lai ievadītu instrukcijas lietotājiem.

1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Laukā **Iesniegšanas instrukcijas** ievadiet instrukcijas.
3.  Lai personalizētu instrukcijas, var ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem. Lai ievietotu vietturi, rīkojieties šādi:
    1.  Noklikšķiniet uz lauka **Iesniegšanas instrukcijas**, lai norādītu, kur vēlaties ievietot vietturi.
    2.  Noklikšķiniet uz **Ievietot vietturi**.
    3.  Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4.  Noklikšķiniet uz **Ievietot**.

4.  Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:
    1.  Noklikšķiniet uz **Tulkojumi**.
    2.  Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3.  Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4.  Laukā **Tulkotais teksts** ievadiet tekstu.
    5.  Lai personalizētu tekstu, var ievadīt vietturus. Instrukcijas par to, kā ievadīt vietturi, skatiet 3. darbībā.
    6.  Noklikšķiniet uz **Aizvērt**.

## <a name="specify-when-this-workflow-is-used"></a>Norādiet, kad tiek izmantota šī darbplūsma
Varat izveidot vairākas darbplūsmas, kuru pamatā ir tas pats tips. Piemēram, varat izveidot pirkuma pieprasījuma darbplūsmu katrai valstij/reģionam, kurā strādājat, piemēram, Pirkuma pieprasījumi Dānija un Pirkuma pieprasījumi Spānija. Ja vairāku darbplūsmu pamatā ir tas pats tips, nepieciešams norādīt, kad katra darbplūsma tiek izmantota. Iepriekšējā piemērā norādiet šādus nosacījumus:

-   Pirkuma pieprasījumi Dānija — tiek izmantota, ja: valsts/reģions = DK
-   Pirkuma pieprasījumi Spānija — tiek izmantota, ja: valsts/reģions = ES

Veiciet šīs darbības, lai norādītu, kad tiek izmantota konfigurētā darbplūsma.

1.  Kreisajā rūtī noklikšķiniet uz **Aktivizēšana**.
2.  Atzīmējiet izvēles rūtiņu **Iestatīt nosacījumus šīs darbplūsmas izpildei**.
3.  Noklikšķiniet uz **Pievienot nosacījumu**.
4.  Ievadīt nosacījumu.
5.  Ievadiet visus nepieciešamos papildu nosacījumus.
6.  Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi iestatīti, rīkojieties šādi:
    1.  Noklikšķiniet uz **Tests**.
    2.  Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3.  Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu norādītajiem nosacījumiem. Piemēram, ja veidojat pirkuma pieprasījumu darbplūsmu Spānijai, lapas apgabalā **Pārbaudīt nosacījumu** tiek parādīts pirkšanas pieprasījumu saraksts. Noklikšķinot uz **Pārbaudīt**, sistēma izvērtēs izvēlētos pirkuma pieprasījumus, lai noteiktu, vai valsts/reģions ir ES.
    4.  Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi
Kad dokuments iesniegts apstrādei, tiek izveidota darbplūsmas instance. Varat nosūtīt paziņojumus lietotājiem, ja darbplūsmas instances, kuru pamatā ir attiecīgā darbplūsmā, ir sāktas, pabeigtas, pārtraukas vai apturētas kļūdas dēļ. Veiciet šīs darbības, lai norādītu, kad tiek nosūtīti paziņojumi.

1.  Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2.  Atzīmējiet izvēles rūtiņu katram notikumam, kam vajadzētu izraisīt paziņojumus:
    -   **Sākts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek sākta.
    -   **Apturēts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta kļūdas dēļ.
    -   **Pabeigts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pabeigta.
    -   **Neatkopjama** — nosūtīt paziņojumus, kad darbplūsmas instance tiek apturēta neatkopjamas kļūdas dēļ.
    -   **Pārtraukts** — nosūtīt paziņojumus, kad darbplūsmas instance tiek pārtraukta.

3.  Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4.  Cilnē **Paziņojuma teksts** ievadiet paziņojuma tekstu.
5.  Lai personalizētu tekstu, var ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad teksts tiks parādīts lietotājiem. Lai ievietotu vietturi, rīkojieties šādi:
    1.  Noklikšķiniet uz lauka, lai norādītu, kur vietturim jāparādās.
    2.  Noklikšķiniet uz **Ievietot vietturi**.
    3.  Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4.  Klikšķiniet **Ievietot**.
    5.  Bieži izmantots opcijas **Paziņojuma teksts** vietturis ir Last Notes: %Workflow.Last note%, kas parāda visus iepriekšējās darbības komentārus.

6.  Lai pievienotu teksta tulkojumus, rīkojieties šādi:
    1.  Noklikšķiniet uz **Tulkojumi**.
    2.  Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3.  Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4.  Laukā **Tulkotais teksts** ievadiet tekstu.
    5.  Lai personalizētu tekstu, var ievadīt vietturus. Instrukcijas par to, kā ievadīt vietturi, skatiet 5. darbībā.
    6.  Noklikšķiniet uz **Aizvērt**.

7.  Cilnē **Adresāts** izmantojiet šādas opcijas, lai norādītu personas, kurām jāsaņem paziņojumi.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Opcija</th>
    <th>Paziņojumi tiek nosūtīti šiem lietotājiem</th>
    <th>Lai nosūtītu paziņojumus, rīkojieties šādi</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td><ol>
    <li>Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Dalībnieks</strong>.</li>
    <li>Cilnē <strong>Pēc lomas</strong>, sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Darbplūsmas lietotājs</td>
    <td>Lietotāji, kuri ir šīs darbplūsmas dalībnieki</td>
    <td><ol>
    <li>Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Darbplūsmas lietotājs</strong>.</li>
    <li>Cilnē <strong>Darbplūsmas lietotājs</strong>, sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet šīs darbplūsmas dalībnieku.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Lietotājs</td>
    <td>Noteikti Dynamics 365 for Finance and Operations lietotāji</td>
    <td><ol>
    <li>Cilnē <strong>Adresāts</strong> noklikšķiniet uz <strong>Lietotājs</strong>.</li>
    <li>Cilnes <strong>Lietotājs</strong> sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi Dynamics 365 for Finance and Operations lietotāji. Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Ievadiet komentārus par attiecīgajā darbplūsmā veiktajām izmaiņām
Lai ievadītu komentārus par izmaiņām, ko veicāt šajā darbplūsmā, rīkojieties šādi.

1.  Kreisajā rūtī noklikšķiniet uz **Piezīmes**.
2.  Laukā **Ievadīt komentārus par darbplūsmu** ievadiet savus komentārus.
3.  Pārskatiet savus komentārus. Pēc komentāru pievienošanas tos nevar pārveidot.
4.  Noklikšķiniet uz **Pievienot**, lai pievienotu jūsu komentārus apgabalā **Komentāru vēsture**.





