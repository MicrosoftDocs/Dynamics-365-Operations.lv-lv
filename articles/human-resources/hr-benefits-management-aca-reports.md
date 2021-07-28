---
title: Ģenerēt Pieejamas aprūpes akta pārskatus Atvieglojumu pārvaldībā
description: Šajā tēmā ir aprakstīts, kā Atvieglojumu pārvaldība palīdz izsekot informāciju, kas ir norādīta Pieejamas aprūpes akta (ACA) darba devēja mandāta formā 1095-B un formā 1095-C.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b8a83982ad36abfe9032cae50fe4f09339985dc8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353666"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Ģenerēt ACA pārskatus Atvieglojumu pārvaldībā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Atvieglojumu pārvaldība palīdz izsekot informāciju, kas ir norādīta Pieejamas aprūpes akta (ACA) darba devēja mandāta formā 1095-B un formā 1095-C. Līdzīgi ACA pārskata iespējām vecajā **Atvieglojumu** darbvietā šī funkcionalitāte attiecas tikai uz juridiskajām personām Amerikas Savienotajās Valstīs.

Lai lietotu šo funkcionalitāti, vispirms ir jāslēdz **Papildu atvieglojumu pārvaldība**. Papildinformāciju, tostarp svarīgus atvieglojumu pārvaldības procesus, skatiet sadaļā [Atvieglojumu pārvaldības iespējošana vai deaktivizēšana](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Varat izmantot ACA pārskatus tikai no darbvietas **Atvieglojumu pārvaldība** vai no vecās darbvietas **Atvieglojumi**, taču ne no abām. Piemēram, ja esat pārslēdzies uz Atvieglojumu pārvaldību, ACA pārskati ir pieejami tikai no **Atvieglojumu pārvaldības** darbvietas, nevis no vecās darbvietas **Atvieglojumi**.
>
> Ja pārslēdzaties uz Atvieglojumu pārvaldību reģistrācijas gada vidū, Atvieglojumu pārvaldībā pareizi jākonfigurē darbinieka dati par visu gadu. Šādā veidā jūs nodrošināt, ka saņemsiet precīzu pārskatu informāciju par visu gadu.

## <a name="getting-started"></a>Darba sākšana

Lai sekotu līdzi informācijai formām 1095, vispirms izveidojiet vienu vai vairākas Pieejamās aprūpes seguma grupas. Šīs grupas norāda šādu informāciju:

- Darbiniekam nodrošinātais seguma piedāvājums
- Darbinieka daļa no zemāko mēneša prēmiju izmaksām, ja izmaksas pārsniedz federālo nabadzības slieksni
- Darba devēja izmantoto drošo patvērumu, ja piemērojams

Pieejamās aprūpes seguma grupas palīdz pārvaldīt šo informāciju vairākiem darbinieku ierakstiem, kuriem ir vienādi nosacījumi. Grupas var viegli piešķirt vienam vai vairākiem darbiniekiem.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Izveidot vai rediģēt Pieejamās aprūpes seguma grupu

1. Darbvietā **Atvieglojumu pārvaldība** atlasiet **Pieejamās aprūpes seguma grupa**.

    ![Pieejamās aprūpes seguma grupas atlasīšana.](./media/hr-benefits-management-aca-coverage-group.png)

2. Atlasiet **Jauns**, lai izveidotu jaunu Pieejamās aprūpes seguma grupu, vai **Rediģēt**, lai mainītu esošo grupu.

    ![Jauns vai Rediģēt atlasīšana.](./media/hr-benefits-management-aca-new.png)

3. Iestatiet tālāk minētos laukus.

    | Lauks | Apraksts |
    |---|---|
    | Nosaukums/vārds, uzvārds | Ievadiet grupas nosaukumu. |
    | Apraksts | Ievadiet grupas aprakstu. |
    | Vajadzību piedāvājums | Segums, kas tiek piedāvāts darbiniekiem, viņu dzīvesbiedram vai partnerim un viņu apgādājamajiem. |
    | Darbinieka izmaksu daļa | Summa, par kuru darbinieks atbildīgs. |
    | Piemērojamā drošā patvēruma platformas 4980H daļa | 4980H drošā patvēruma vai pārejas atvieglojumu kods. |
    | Plāna sākuma mēnesis | Atlasiet kalendāro mēnesi, kad sākas atvieglojumu plāna gads. |
    | Grupa derīga no | Pirmais datums, kad šis ieraksts ir derīgs. |
    | Grupa derīga līdz | Pēdējais datums, kad šis ieraksts ir derīgs. Ja nav beigu datuma, ievadiet **Nekad**. |

    ![Seguma grupas izveide.](./media/hr-benefits-management-aca-new-group.png)

4. Atlasiet **Saglabāt**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Vairāku darbinieku piešķiršana Pieejamās aprūpes seguma grupai

1. Darbvietā **Atvieglojumu pārvaldība** atlasiet **Pieejamās aprūpes seguma grupa**.
2. Atlasiet grupu, kam piešķirt darbiniekus.
3. Atlasiet **Masveida piešķire**.

    ![Masveida piešķires atlasīšana.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Atlasiet sarakstā darbiniekus un pēc tam atlasiet **Piešķirt**.

    ![Atlasīto darbinieku piešķiršana grupai.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Segumu opciju vairāku versiju uzturēšana

Varat uzturēt jebkuras segumu grupas vairākas versijas. Kad jūsu organizācijā vai sniegtajos atvieglojumos notiek kādas izmaiņas, varat saglabāt grupas informāciju vienmēr atjauninātu, neveidojiet jaunu grupu un atkārtoti nepiešķirot tai darbiniekus.

Kad esat izveidojis Pieejamās aprūpes seguma grupas, varat tām piešķirt darbiniekus masveidā. Varat arī atsevišķi piešķirt darbiniekus grupām, kā arī norādīt, vai ACA informācija tiek izsekota un norādīta pārskatā.

Ja nav nepieciešams izsekot darbinieka ACA informāciju un norādīt to, varat iestatīt opciju **Norādīt segumu** uz **Nē**. Piemēram, jums ir nepilna laika darbinieki, kuri nav jānorāda ACA pārskatos.

### <a name="override-default-values-for-an-employee"></a>Ignorējiet darbinieka noklusētās vērtības

Darbiniekiem, kas piešķirti Pieejamās aprūpes seguma grupai, jūs varat mainīt šādas opcijas par mēnešiem, kam nepieciešamas citas vērtības:

- Vajadzību piedāvājums
- Darbinieka izmaksu daļa
- Piemērojamā drošā patvēruma platformas 4980H daļa

> [!NOTE]
> 2020. gada ACA pārskatiem formā 1095-C jānorāda gan darba, gan mājas pasta indeksi. Vērtības tiek aizpildītas automātiski, pamatojoties uz pašreizējām aktīvām atrašanās vietām. Ja kādā gada daļā kāda no atrašanās vietām bija atšķirīga, vērtība ir jāignorē. Lauks **Pasta indekss** (17. rinda) pārskatā 1095-C tiek aizpildīts tikai tad, ja kods **Seguma piedāvājums** ietver **1L** līdz **1Q**, kā redzams zemāk:
>
> - **1L, 1M vai 1N:** primārās dzīvesvietas pasta indekss
> - **1O, 1P, 1Q:** primārās darba vietas pasta indekss

Lai ievadītu izņēmumus jebkādām seguma grupas vērtībām, izpildiet tālāk norādītās darbības.

1. **Personāla vadības** darbvietā atlasiet **Saites** un pēc tam atlasiet **Darbinieki**.
2. Sarakstā atlasiet darbinieku.
3. Cilnes **Nodarbinātība** sadaļā **Papildinformācija** atlasiet **Pieejamās aprūpes segums**.

    ![Darbinieka opciju maiņa.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Atlasiet **Rediģēt**.
5. Katram mēnesim, kam nepieciešamas izmaiņas, atzīmējiet izvēles rūtiņu **Ignorēt noklusējumu** un pēc tam mainiet pārējās vērtības pēc vajadzības.

    ![Noklusēto vērtību ignorēšana.](./media/hr-benefits-management-aca-override-default.png)

6. Atlasiet **Saglabāt**.

## <a name="report-health-care-coverage"></a>Veselības aprūpes seguma pārskats

Ir jāizseko jebkāds darba devēja sponsorēts paša apdrošināts veselības aprūpes segums pilna laika un nepilna laika darbiniekiem. Ietveriet katru darbinieku kopā ar viņu apgādājamiem 1095-C pārskatā par mēnešiem, kad viņi tika segti.

Lai norādītu, vai jāsniedz pārskats par atvieglojumu plānu, izpildiet tālāk minētās darbības.

1. Darbvietā **Atvieglojumu pārvaldība** atlasiet **Atvieglojumu plāni**.
2. Atlasiet atvieglojumu plānu pārskatam.
3. Atlasiet **Rediģēt**.
4. Iestatiet opciju **Norādīts pārskatā saskaņā ar Pieejamās aprūpes aktu** uz **Jā**.

    ![Veselības aprūpes seguma ziņošana.](./media/hr-benefits-management-aca-report-coverage.png)

5. Atlasiet **Saglabāt**.

Ja darbinieks izvēlas apgādājamā veselības aprūpes segumu, apgādājamā seguma periodu nosaka datums, kad apgādājamais tika reģistrēts vai noņemts. Seguma datumi apgādājamajiem tiek automātiski aprēķināti, pamatojoties uz periodu, kad apgādājamais bija tiesīgs un aktīvs plānā reģistrācijas gada laikā.

## <a name="generate-1095-b-and-1095-c-forms"></a>Formu 1095-B un 1095-C ģenerēšana

Šī produkta ietvaros varat ģenerēt ACA formas 1095-B un 1095-C un pēc tam tās izdalīt katram no saviem darbiniekiem. Varat arī elektroniski ģenerēt formu 1095-C un atbilstošos 1094-C pārsūtāmos failus, lai nosūtītu Iekšējam ieņēmumu dienestam (IRS).

1. Darbvietā **Atvieglojumu pārvaldība** atlasiet **ACA 1095-B forma** vai **ACA 1095-C forma**.
2. Pēc vajadzības mainiet parametrus un pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Ja drukājat formas 1095-C vairāk nekā 500 darbiniekiem, jūs saņemsiet vairāk nekā vienu PDF failu. Iesakām palielināt lauka **Maksimālais faila lielums megabaitos** vērtību lapā **Dokumentu pārvaldības parametri** uz **150**. (Lai ātri atvērtu šo lapu, varat izmantot meklēšanas lauku navigācijas joslā.)
    >
    > ![Maksimālā faila lieluma maiņa.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Lai pārbaudītu pārskatu statusu un tos skatītu, izmantojiet meklēšanas lauku navigācijas joslā, lai atvērtu lapu **Elektronisko pārskatu izveides darbi**.

    ![Elektronisko pārskatu izveides darbu lapas meklēšana.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Atlasiet skatāmo pārskatu un pēc tam atlasiet **Rādīt failus**.

    ![Failu rādīšana.](./media/hr-benefits-management-aca-show-files.png)

5. Atlasiet **Atvērt**.

    ![Faila atvēršana.](./media/hr-benefits-management-aca-open-file.png)

6. No paziņojumu joslas, kas tiek parādīta pārlūkprogrammas loga apakšā, atveriet tilpsaspiesto failu un pēc tam atlasiet pārskatu. Varat apskatīt vai drukāt PDF failu.

    ![Parauga forma 1095-C.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>ACA seguma informācijas skatīšana

Lapā **Darbinieka Pieejamās aprūpes segums** tiek rādīta šāda informācija:

- Darbinieki, kuri piešķirti katrai seguma grupai
- Darbinieki, kuri nav jāiekļauj pārskatā
- Nepiešķirtie darbinieki

Lai apskatītu šo informāciju, veiciet šādas darbības.

1. Darbvietā **Atvieglojumu pārvaldība** atlasiet **Darbinieka Pieejamās aprūpes segums**.
2. Laukā **Grupas nosaukums** atlasiet grupu.

    ![ACA seguma skatīšana.](./media/hr-benefits-management-aca-view-coverage.png)

Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte. Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiek rādīta kolonnā **Visi 12 mēneši**.

Varat skatīt darbiniekus, kuri ir atzīmēti kā tādi, kuri ACA pārskatā nav jānorāda, un kuriem nebūs nepieciešama forma 1095-C. Laukā **Filtrēt pēc** atlasiet **Nav jānorāda ACA pārskatā**.

Varat skatīt darbiniekus, kuri nav piešķirti grupai vai kuri ir piešķirti grupai, kurai beidzies derīguma termiņš. Laukā **Filtrēt pēc** atlasiet **Nepiešķirts vai grupai beidzies derīguma termiņš**.

### <a name="export-to-excel"></a>Eksportēt programmā Excel

Lai eksportētu kādu no sarakstiem uz Microsoft Excel, veiciet tālāk minētās darbības.

1. Atlasiet pogu **Atvērt programmā Microsoft Office**.
2. Atlasiet **HCM Human Resources pagaidu tabula iekšējai lietošanai**.
3. Atlasiet **Lejupielādēt**.

### <a name="view-aca-reportable-dependents"></a>Skatīt ACA pārskatā norādāmos apgādājamos

Ja jums ir jāsniedz pārskats par iekļautajām personām, jo jūs nodrošināt paša apdrošinātu segumu, varat apskatīt visus apgādājamos, kas ietverti atvieglojumu plānos, kuri atzīmēti kā **Norādāmi ACA pārskā**. Darbību rūtī atlasiet **Skatīt apgādājamā segumu**.

![Apgādājamā seguma skatīšana.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Tiek rādīta seguma informācija par darbinieka apgādājamiem.

![Apgādājamo segums.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Lapā tiek rādīti tikai tie atvieglojumu plāni, kas ir atzīmēti kā **Norādāmi ACA pārskatā**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]