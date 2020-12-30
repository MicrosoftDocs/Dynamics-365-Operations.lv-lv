---
title: Sākt ar elektronisko rēķinu pievienojumu Brazīlijai
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Brazīlijai programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2020
ms.locfileid: "4445771"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Sākt ar elektronisko rēķinu pievienojumu Brazīlijai 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Elektronisko rēķinu pievienojums Brazīlijai pašlaik nenodrošina visas funkcijas, kas ir pieejamas Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management iebūvētajā finanšu dokumentu integrācijā.

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Brazīlijai. Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts risinājumos Regulatory Configuration Services (RCS) un Finance and Supply Chain Management. Tas arī palīdz veikt NF-e finanšu dokumenta (elektroniskā finanšu dokumenta modeļa 55) iesniegšanas procesu, izmantojot pakalpojumu, un paskaidro, kā pārskatīt apstrādes rezultātus un finanšu dokumentu statusu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms šajā tēmā aprakstīto darbību veikšanas ir jāpabeidz darbības sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS iestatījumi

RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Importējiet e-rēķinu izrakstīšanas līdzekli NF-e finanšu dokumentiem.
2. Pārskatiet failu formātus, kas nepieciešami, lai iesniegtu NF-e finanšu dokumentus autorizēšanai.
3. Pārskatiet failu formātus, kas ir nepieciešami, lai pieprasītu apstiprinātā NF-e atcelšanu.
4. Konfigurējiet notikumu, kas nepieciešams, lai iesniegtu NF-e finanšu dokumentus autorizēšanai.
5. Konfigurējiet notikumu, kas nepieciešams, lai pieprasītu apstiprinātā NF-e atcelšanu.
6. Piešķiriet elektronisko rēķinu izrakstīšanas līdzekli elektroniskās rēķinu vides pievienojumam.
7. Publicējiet e-rēķinu izrakstīšanas līdzekli.

> [!NOTE]
> "E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri. E-rēķinu izrakstīšanas līdzekļu iestatījums apvieno, cita starpā, elektroniskās ziņošanas (Electronic reporting - ER) konfigurāciju formātus, lai izveidotu konfigurējamas eksporta un importa failus, un darbību un darbību plūsmu izmantošanu, lai iespējotu konfigurējamu noteikumu izveidi, lai nosūtītu pieprasījumus, importētu atbildes un parsētu atbildes saturu.

## <a name="import-the-e-invoicing-feature"></a>Importējiet e-rēķinu izrakstīšanas līdzekli

1. Piesakieties savā RCS kontā
2. Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **e-rēķinu izrakstīšana**.
3. Lapā **E-rēķina līdzekļi** atlasiet **Importēt**, lai importētu NF-e finanšu dokumentu e-rēķinu izrakstīšanas līdzekli no Globālās krātuves.

    ![Poga ´Importēt´](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Atlasiet līdzekli NF-e finanšu dokuments un pēc tam atlasiet **Importēt**.

    ![NF-e līdzekļa importēšana](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Izveidot jaunu NF-e finanšu dokumentu līdzekļa versiju

- Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Jauns**.

![Jaunas e-rēķinu izrakstīšanas līdzekļa versijas pievienošana](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Atjaunināt konfigurācijas versiju

1. Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Konfigurācijas** vai **Dzēst**, lai pārvaldītu konfigurāciju versijas (ER failu formātu konfigurācijas).

    ![E-rēķinu izrakstīšanas līdzekļa konfigurāciju pārvaldība](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Kad izveidojat jaunu NF-e finanšu dokumentu līdzekļa versiju, visas konfigurācijas versijas (ER failu formāti) tiek pārmantotas no jaunākās versijas.
    - Lai iesniegtu NF-e finanšu dokumentu autorizācijai, ir nepieciešamas šādas konfigurācijas versijas:

        - NFe iesniegšanas eksporta formāts
        - NFe atbilžu ziņojuma importēšana
        - NFe kļūdu žurnāla importēšana

    - Lai iesniegtu NF-e atcelšanu, ir jānorāda šāda konfigurācijas versija:

        - NFe atcelšanas eksporta formāts

2. Sarakstā atlasiet konfigurācijas versiju un pēc tam atlasiet **Rediģēt** vai **Skatīt**, lai atvērtu lapu **Formāta veidotājs**, kurā var rediģēt vai skatīt konfigurāciju.

    ![Formāta veidotāja lapas atvēršana](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Lai rediģētu vai skatītu ER formāta failu konfigurācijas, izmantojiet lapu **Formāta veidotājs**. Papildinformāciju skatiet tēmā [Elektronisko dokumentu konfigurāciju izveide](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formāta veidotāja lapa](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Pārvaldīt e-rēķinu izrakstīšanas līdzekļa iestatījumus

- Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot** vai **Dzēst**, lai pārvaldītu e-rēķinu izrakstīšanas līdzekļa iestatījumus (tas ir, NF-e notikumus).

![E-rēķinu izrakstīšanas līdzekļa iestatījumu pārvaldība](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Kad izveidojat jaunu versiju NF-e finanšu dokumenta līdzeklim, kas iegūts no cita e-rēķinu izrakstīšanas līdzekļa, visi līdzekļu iestatījumi (NF-e notikumi) tiek pārmantoti no jaunākās versijas.

Lai iesniegtu NF-e finanšu dokumentus autorizēšanai, ir nepieciešams līdzekļa iestatījums **Iesniegt**.

Lai iesniegtu NF-e atcelšanu, ir nepieciešams līdzekļa iestatījums **Atcelšana**.

#### <a name="configure-the-submit-feature-setup"></a>Konfigurēt līdzekļa iestatījumu Iesniegt

1. Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Iesniegt**.
2. Atlasiet **Rediģēt**.

    ![Rediģējiet e-rēķinu izrakstīšanas līdzekļa iestatījumu](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu.

    ![Cilne Darbības](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Pārskatiet darbības, kas nepieciešamas, lai iesniegtu NF-e autorizēšanai.

    | Darbības ID | Darbības nosaukums                  | Darbības apraksts                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Transformējiet dokumentu           | Izveidojiet NF-e XML failu iesniegšanai.                          |
    | 2         | Parakstīt dokumentu                | Lietojiet digitālo sertifikātu XML failam.                    |
    | 3         | Izsauciet Brazīlijas SEFAZ pakalpojumu | Iesniedziet parakstīto XML failu tīmekļa pakalpojumiem autorizācijai. |
    | 4         | Apstrādājiet atbildi             | Saņemiet tīmekļa pakalpojuma atbildi.                                     |
    | 5         | Transformējiet dokumentu           | Parsējiet faila saturu, kas saņemts kā atbilde.     |
    | 6         | Transformējiet dokumentu           | Izveidojiet XML failu, lai iegūtu informāciju par iesniegšanas statusu.    |
    | 7         | Izsauciet Brazīlijas SEFAZ pakalpojumu | Iesniedziet XML failu, kas pieprasa iesniegšanas statusu.          |
    | 8         | Apstrādājiet atbildi             | Saņemiet tīmekļa pakalpojuma atbildi.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Iestatiet vietrādi URL SEFAZ tīmekļa pakalpojumiem 

1. Lapā **Līdzekļu versijas iestatīšana** cilnē **Darbības** kopsavilkuma cilnē darbības **Darbības** atlasiet **Izsaukt Brazīlijas SEFAZ pakalpojumu** (darbības ID **3**).
2. Kopsavilkuma cilnē **Parametri** laukā **URL adreses parametrs** ievadiet SEFAZ tīmekļa pakalpojuma vietrādi URL NF-e iesniegšanai.
3. Kopsavilkuma cilnē **Darbības** atlasiet **Izsaukt Brazīlijas SEFAZ pakalpojumu** (darbības ID **7**).
4. Kopsavilkuma cilnē **Parametri** laukā **URL adreses parametrs** ievadiet SEFAZ tīmekļa pakalpojuma vietrādi URL NF-e iesniegšanai.

#### <a name="configure-the-cancellation-feature-setup"></a>Konfigurēt līdzekļa iestatījumu Atcelšana

1. Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Atcelšana**.
2. Atlasiet **Rediģēt**.
3. Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu.
4. Pārskatiet darbības, kas ir nepieciešami, lai pieprasītu apstiprinātā NF-e atcelšanu.

    | Darbības ID | Darbības nosaukums                  | Darbības apraksts                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Transformējiet dokumentu           | Izveidojiet NF-e atcelšanas XML failu iesniegšanai.            |
    | 2         | Parakstīt dokumentu                | Lietojiet digitālo sertifikātu XML failam.                   |
    | 3         | Izsauciet Brazīlijas SEFAZ pakalpojumu | Iesniedziet parakstīto XML failu tīmekļa pakalpojumiem atcelšanai. |
    | 4         | Apstrādājiet atbildi             | Saņemiet tīmekļa pakalpojuma atbildi.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Iestatiet vietrādi URL SEFAZ tīmekļa pakalpojumiem

1. Lapā **Līdzekļu versijas iestatīšana** cilnē **Darbības** kopsavilkuma cilnē darbības **Darbības** atlasiet **Izsaukt Brazīlijas SEFAZ pakalpojumu** (darbības ID **3**).
2. Kopsavilkuma cilnē **Parametri** laukā **URL adreses parametrs** ievadiet SEFAZ tīmekļa pakalpojuma vietrādi URL apstiprināta NF-e atcelšanai.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Padariet pieejamu e-rēķinu izrakstīšanas vidi un piešķiriet melnraksta versiju

1. Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Vides** atlasiet **Iespējot**.
2. Laukā **Vide** atlasiet vidi.
3. Laukā **Spēkā no** atlasiet datumu, kad videi jāstājas spēkā.
4. Atlasiet **Iespējot**.

![E-rēķina vides iespējošana](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Mainiet statusu uz Pabeigts

1. Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Melnraksts**.
2. Atlasiet **Mainīt statusu \> Pabeigts**.

### <a name="change-the-status-to-publish"></a>Mainiet statusu uz Publicēt

1. Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Pabeigts**.
2. Atlasiet **Mainīt statusu \> Publicēt**.

![E-rēķinu izrakstīšanas līdzekļa publicēšana](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Iestatīt elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanu Finance vai Supply Chain Management

Iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Ieslēdziet NF-e federālo līdzekli Brazīlijai.
2. Importējiet konkrētu ER datu modeli, datu modeļa kartēšanu un formātus, kas ir nepieciešami NF-e finanšu dokumentiem.
3. Importējiet ER konfigurāciju un iestatiet atbildes veidus, kas ir nepieciešami, lai atjauninātu finanšu dokumenta statusu pēc iesniegšanas procesa atgriešanas.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Ieslēdziet NF-e federālo līdzekli Brazīlijai

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Līdzekļi** atzīmējiet izvēles rūtiņu **Iespējot**, kas atrodas līdzekļu reksturojuma rindā **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Importējiet ER datu modeļa kartēšanu, kas nepieciešama NF-e finanšu dokumentiem

1. Pieteikšanās programmā Finance.
2. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**. Pārliecinieties, vai šis konfigurācijas nodrošinātājs ir iestatīts kā **Aktīvs**. Papildinformāciju par to, ka iestatīt nodrošinātāju kā **Aktīvs** skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Atlasiet **Repozitoriji**.
4. Atlasiet **Globālais resurss \> Atvērt**.
5. Importējiet konfigurācijas **Finanšu dokumentu kartēšana**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Importējiet ER konfigurācijas un iestatiet atbilžu veidus finanšu dokumentiem

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
2. Atlasiet **Repozitoriji**.
3. Atlasiet **Globālais resurss \> Atvērt**.
4. Importējiet **NF-e kļūdu žurnāla importēšana (BR)**, **NF-e atbilžu datu importēšanas formāts (BR)** un **NF-e atbilžu ziņojumu importēšana (BR)**.
5. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
6. Cilnē **Elektronisks dokuments** atlasiet **Pievienot**.
6. Laukā **Tabulas nosaukums** ievadiet **Finanšu dokumenta virsraksts**.
7. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksta modelis – Finanšu dokumenta konteksts**.
8. Atlasiet **Atbilžu veidi**.
9. Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** atlasiet **Atbilde**.
10. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
11. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojuma importēšanas formāts — Modeļa kartēšana no atbildes ziņojuma**.
12. Atlasiet **Saglabāt**.
13. Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** ievadiet **ResponseData**.
14. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
15. Laukā **Modeļa kartēšana** atlasiet **NFe atbildes datu importēšanas formāts — Atbildes datu importēšana**.
16. Atlasiet **Saglabāt**.

## <a name="electronic-invoice-processing"></a>Elektroniska rēķina apstrāde

Finance apstrādes laikā jūs veiksiet šādus uzdevumus:

1. Iesniedziet finanšu dokumentu, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
2. Skatiet iesniegšanas izpildes žurnālus un pārskatiet apstrādes rezultātus.
3. Iesniedziet finanšu dokumentu atcelšanu, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Iesniedziet NF-e finanšu dokumentus SEFAZ autorizācijai 

Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, vairs nevarēsiet izmantot veco procesu, lai iesniegtu NF-e finanšu dokumentus autorizācijai (**Eksporta/Importa NF-e process)**. Tas ir aizstāts ar jaunu procesu, kura nosaukums ir **Iesniegt elektroniskus dokumentus**.

> [!NOTE]
> Pirms turpināt, pārliecinieties, ka jums ir viens vai vairāki debitoru finanšu dokumentu modeļi 55, ko izsniedza debitoru finanšu uzņēmums. Šo finanšu dokumentu virziens ir jāiestata uz **Izejošs**, un statusam ir jābūt **Izveidots**. Papildinformāciju skatiet šeit: [Debitora finanšu dokumenta izsniegšana (Brazīlija)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.
2. Pirmā dokumenta iesniegšanai vienmēr iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**. Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.
3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.
4. Cilnē **Diapazons** atlasiet **Pievienot**.
5. Laukā **Tabula** atlasiet **Finanšu dokumenta virsraksts**.
6. Laukā **Atveidotā tabula** atlasiet **Finanšu dokumenta virsraksts**.
6. Laukā **Lauks** atlasiet **Numurs**.
7. Laukā **Kritērijs** ievadiet iesniedzamā finanšu dokumenta numuru.
8. Lai dialoglodziņu **Pieprasījums** aizvērtu, atlasiet **Labi**.
8. Atlasiet **Labi**, lai iesniegtu atlasītos dokumentus.

> [!NOTE]
> Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu pievienojumprogrammu. Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.

### <a name="view-all-submission-logs"></a>Skatīt visus iesniegšanas žurnālus

Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, ir pieejama jauna lapa, kas ļauj sekot līdzi dokumentu iesniegšanas procesam. Varat izmantot šo lapu, lai skatītu visu iesniegto dokumentu iesniegšanas žurnālus.

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet **Finanšu dokumenta virsraksts**, lai filtrētu tikai finanšu dokumentus.
3. Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.

![Iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Attiecībā uz NF-e finanšu dokumentiem kolonnā **Kļūdas kods** ir parādīts atgrieztais kods, kas tika atgriezts ar SEFAZ tīmekļa pakalpojumu palīdzību.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Skatiet iesniegšanas žurnālus, izmantojot finanšu dokumenta lapu

Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, varat arī skatīt iesniegumu žurnālus, izmantojot finanšu dokumenta lapu.

1. Dodieties uz **Virsgrāmata \> Vaicājumi un pārskati \> Finanšu dokumenti \> Visi finanšu dokumenti**.
2. Atlasiet finanšu dokumentu, kas iepriekš tika iesniegts, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
3. Darbības rūtī, kas atrodas cilnē **NF-e federālais**, atlasiet **Elektronisko dokumentu žurnāls**.

![Iesniegumu žurnālu skatīšana no finanšu dokumenta lapas](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Iesniedziet apstiprinātus NF-e finanšu dokumentus SEFAZ atcelšanai

Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, vairs nevarēsiet izmantot veco procesu, lai atceltu NF-e finanšu dokumentus. Tas ir aizstāts ar jaunu atcelšanas procesu, kas ir iegults lapā **Elektronisko dokumentu iesniegšanas žurnāls**.

> [!NOTE]
> Pārliecinieties, ka esat palaidis debitora finanšu dokumenta atcelšanu apstiprinātajam NF-e finanšu dokumentam. Papildinformāciju skatiet šeit: [Debitora finanšu dokumenta atcelšana (Brazīlija)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Atlasiet finanšu dokumentu un pēc tam atlasiet **Funkcijas \> Sūtīt saistītos iesniegumus**.
3. Ievadiet saistītā iesnieguma aprakstu un pēc tam atlasiet **Labi**.

### <a name="view-cancellation-submission-logs"></a>Skatīt atcelšanas iesniegšanas žurnālus

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet **Finanšu dokumenta virsraksts**, lai filtrētu tikai finanšu dokumentus.
3. Atlasiet finanšu dokumentu un pēc tam Darbību rūtī atlasiet **Vaicājumi \> Saistītie iesniegumi**.

    Saistītie iesniegumi ir iesniegumi, kas attiecas uz galveno iesniegumu, kas tika veikts pirmais. Piemēram, iesniegums, kas autorizē konkrētu NF-e, ir galvenais iesniegums. Iesniegums, kas pieprasa atcelšanu tai pašai NF-e SEFAZ, ir saistīts iesniegums. Tas pastāv tikai tāpēc, ka tas pieprasa anulēt darbu, kas tika veikts, izmantojot citu iesniegumu.

    Lapa **Saistītais iesniegums** parāda visus saistītos iesniegumus un to iesniegšanas statusu attiecīgajam finanšu dokumentam. Sekojošajā ilustrācijā pirmā rinda ataino iesniegumu, kas pieprasīja finanšu dokumenta apstiprināšanu. Otrā rinda ataino iesniegumu, kas atcēla šo finanšu dokumentu.

    ![Atcelšanas iesniegšanas žurnālu apskate](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.

    ![Atcelšanas iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Iespējojot līdzekli BR-00053 (NF-e federālais), var būt nepieciešams nosūtīt ierobežotus datus, kas ietver organizācijas nodokļa reģistrācijas ID. Tas tiks nosūtīts trešo personu aģentūrām, ko pilnvarojusi nodokļu iestāde, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekš noteiktā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu. Administrators var iespējot un atspējot līdzekli BR-00053 (NF-e Federal), pārvietojoties uz **Organizācijas administrēšana \> Iestatījumi \> Elektroniskā dokumenta parametri**. Atlasiet cilni **Līdzekļi**, atlasiet rindu, kas satur līdzekli BR-00053, un pēc tam veiciet atbilstošo atlasi. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, lūdzu, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.


## <a name="additional-resources"></a>Papildu resursi

- [Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-service-overview.md)
- [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md)
- [Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana](e-invoicing-setup.md)
