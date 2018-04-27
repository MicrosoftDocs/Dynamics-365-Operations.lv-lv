---
title: "Brīdinājumu pārskats"
description: "Šajā tēmā ir sniegta vispārēja informācija par brīdinājumu pakešveida apstrādi programmā Microsoft Dynamics 365 for Finance and Operations. Brīdinājumus var izmantot, lai saņemtu informāciju par notikumiem, kurus vēlaties izsekot darbdienas laikā."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ad9373faa19761cccca2b5d581de05f0ac9dd165
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="alerts-overview"></a>Brīdinājumu pārskats

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

## <a name="about-alerts"></a>Par brīdinājumiem
Brīdinājumus ģenerē kritisko notikumu ziņošanas sistēma par programmā Microsoft Dynamics 365 Finance and Operations. Brīdinājumus var izmantot, lai saņemtu informāciju par notikumiem, kurus vēlaties izsekot darbdienas laikā. Jūs varat viegli izveidot brīdinājumu kārtulas, lai tādējādi saņemtu brīdinājumus par nokavētām piegādēm, dzēstiem pasūtījumiem, cenu izmaiņām vai citiem notikumiem, uz kuriem jāreaģē.

Uzņēmuma resursu plānošanas (ERP) procesā ir vairāki tipiski scenāriji, kuros var izmantot programmas Finance and Operations brīdinājumu funkciju. Tālāk ir sniegti daži piemēri.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>1. scenārijs. Brīdinājuma kārtulas izveidošana jaunam pārdošanas pasūtījumam.
1. Atveriet lapu **Visi pārdošanas pasūtījumi**.
2. Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot pielāgotu brīdinājumu**.
3. Dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnes **Brīdināt, ja** laukā **Notikums** atlasiet **Ir izveidots ieraksts**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>2. scenārijs. Brīdinājuma kārtulas izveidošana piegādes datuma atlikšanai.
1. Atveriet lapu **Visi pirkšanas pasūtījumi**.
2. Lai piekļūtu pirkšanas pasūtījuma datiem, atlasiet pirkšanas pasūtījuma ID.
3. Izvērsiet kopsavilkuma cilni **Pirkšanas pasūtījuma galvene** .
4. Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot pielāgotu brīdinājumu**.
5. Dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnes **Brīdināt, ja** laukā **Lauks** atlasiet **Piegādes datums**.
6. Laukā **Notikums** atlasiet **ir atlikts**.
    
Kad dialoglodziņš **Izveidot brīdinājuma kārtulu** ir aizvērts, izveidotā kārtula tiek parādīta lapā **Brīdinājuma kārtulu pārvaldīšana**. Lapu **Brīdinājuma kārtulu pārvaldīšana** var izmantot, lai atjauninātu esošās brīdinājuma kārtulas. Piemēram, var mainīt notikumu aktivizēšanas elementus, atjaunināt notikumu paziņojumus un atjaunināt beigu datumus. Lai atvērtu lapu **Brīdinājuma kārtulu pārvaldīšana**, izmantojiet darbību rūts cilnes **Opcijas** pogu **Brīdināt**.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Kas notiek, ja tiek izveidota brīdinājuma kārtula?
Izveidojot brīdinājuma kārtulas, iepriekš definētu notikumu var saistīt ar noteiktu lauku. Piemēram, iestājas laukā norādītais datums vai tiek mainīts lauka saturs. Vai arī var saistīt notikumu ar konkrētas lapas ierakstiem. Piemēram, tiek izveidots vai dzēsts ieraksts.

Ja notiek lapā konkrētajam laukam vai ierakstam atlasītais notikums, tiek nosūtīts brīdinājums. Piemēram, tiek izveidota kārtula, kurā noteikta pirkšanas pasūtījuma rindas lauks **Piegādes datums** tiek saistīts ar notikumu **šis izpildes termiņš bija pirms šāda laika**. Tiek iestatīts piecu dienu laika ierobežojums. Šādā gadījumā piecas dienas pēc pirkšanas pasūtījuma rindas piegādes datuma sasniegšanas tiek nosūtīts brīdinājums.

Turklāt brīdinājuma kārtulas varat precizēt, iestatot nosacījumus. Piemēram, brīdinājumus var nosūtīt par jaunajiem pirkšanas pasūtījumiem, kas tiek izveidoti noteiktiem kreditoru kontiem.

## <a name="preparing-for-an-alert"></a>Sagatavošanās brīdinājuma izveidei
Pirms brīdinājuma kārtulas iestatīšanas padomājiet, kad un kādās situācijās vēlaties saņemt brīdinājumus. Kad ir zināms, par kuriem notikumiem vēlaties saņemt paziņojumus, programmā Finance and Operations atveriet lapu, kurā tiek parādīti dati, kas izraisa šo notikumu. Notikums var būt datums, kas iestājas, vai noteiktas izmaiņas, kuras ir veiktas. Tāpēc ir jāatver lapa, kur ir norādīts datums vai kur ir redzams lauks, kur tiek parādītas izmaiņas vai jaunais ieraksts, kurš tiek izveidots. Kad šī informācija ir iegūta, var izveidot brīdinājuma kārtulu.

## <a name="components-of-an-alert-rule"></a>Brīdinājuma kārtulas komponenti
Brīdinājuma kārtula ietver piecus komponentus.

- **Notikums** — notikums, kas aktivizē brīdinājuma kārtulu var būt datums, kas iestājas, vai noteiktas izmaiņas, kas ir veiktas. Notikumu definē dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Sūtīt e-pasta brīdinājumus par darba statusa izmaiņām**.
- **Nosacījums** — lai kontrolētu brīdinājuma par notikumiem saņemšanas laiku, dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt par** var atlasīt kārtulas saturu. Kārtulu var piešķirt vai nu tikai pašreizējam ierakstam, vai visiem lapā redzamajiem ierakstiem. Ja kārtulas attiecas uz visām juridiskajām personām, var iestatīt vienuma **Visas organizācijas** opciju **Jā**.
- **Kārtulas derīguma termiņa beigas** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt līdz** var norādīt, cik ilgi brīdinājuma kārtulai jādarbojas.
- **Saturs** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt tēmas un ziņojuma tekstu, kurš jāizmanto brīdinājuma ziņojumos.
- **Lietotājs** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt kuru** var norādīt, kuram lietotājam jāsaņem brīdinājuma ziņojumi. Pēc noklusējuma tiek atlasīts jūsu lietotāja ID.

    > [!NOTE]
    > Šī opcija attiecas tikai uz organizācijas administratoriem.

## <a name="email-notifications-from-alerts"></a>E-pasta paziņojumi no brīdinājumiem
E-pasta paziņojumi no brīdinājumiem vēl nav iespējoti. Šī funkcija tiks iespējota ar turpmāku atjauninājumu.

