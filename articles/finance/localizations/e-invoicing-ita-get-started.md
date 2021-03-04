---
title: Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai elektronisko rēķinu izrakstīšanas pievienojumprogrammai programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2020
ms.locfileid: "4445768"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Elektronisko rēķinu izrakstīšanas pievienojumprogramma Itālija, iespējams, pašlaik neatbalsta visas funkcijas, kas ir pieejamas elektroniskajiem rēķiniem Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management. 

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Itālijai. Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts risinājumos Regulatory Configuration Services (RCS) un Finance. Tas arī palīdz veikt to elektronisko rēķinu iesniegšanas procesu, kas tiek ģenerēti Itālijai specifiskajā **FatturaPA** formātā, izmantojot šo pakalpojumu, un tas izskaidro, kā pārskatīt apstrādes rezultātus.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms šajā tēmā aprakstīto darbību veikšanas ir jāpabeidz darbības sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS iestatījumi

RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Importējiet e-rēķinu izrakstīšanas līdzekli debitoru elektronisko rēķinu eksportēšanai **FatturaPA** formātā.
2. Pārskatiet formāta konfigurācijas, kas nepieciešamas, lai ģenerētu, iesniegtu un saņemtu atbildes par elektroniskiem rēķiniem.
3. Konfigurējiet notikumus, kas atbalsta elektronisko rēķinu iesniegšanas scenārijus.
4. Publicējiet e-rēķinu izrakstīšanas līdzekli.

> [!NOTE]
> "E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri. Šādā gadījumā debitoru elektronisko rēķinu eksportēšana ir uzstādāmais e-rēķinu līdzeklis.

## <a name="import-the-e-invoicing-feature"></a>Importējiet e-rēķinu izrakstīšanas līdzekli

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **e-rēķinu izrakstīšana**.
3. Lapā **E-rēķina līdzekļi** atlasiet **Importēt**, lai importētu e-rēķinu izrakstīšanas līdzekli no Globālās krātuves.

    > [!NOTE]
    > Ja nav redzams pieejamo līdzekļu saraksts, atlasiet **Sinhronizēt**. 

4. Atlasiet līdzekli **E-rēķinu eksportēšana (IT)** un pēc tam atlasiet **Importēt**.

![E-rēķinu eksportēšanas (IT) līdzekļa importēšana](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Importējot līdzekli **E-rēķina eksportēšana (IT)** no globālās krātuves, tiek importēti arī visi nākamajā sadaļā aprakstītie iestatījumi.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Izveidot jaunu e-rēķina eksportēšanas (IT) līdzekļa versiju

1. Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Jauns**. 

    ![Jaunas e-rēķinu izrakstīšanas līdzekļa versijas pievienošana](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Pēc tam konfigurējiet elektronisko pārskatu (Electronic reporting - ER) formātus, kas ir saistīti ar e-rēķinu izrakstīšanas līdzekli.

2. Cilnē **Konfigurācijas** atlasiet **Pievienot**, lai pārvaldītu konfigurācijas versijas.

    ![E-rēķinu izrakstīšanas līdzekļa konfigurācijas versiju pārvaldība](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Šajā darbībā jūs pievienojat un konfigurējat ER formātus dažādiem failiem, kas tiek izmantoti, lai eksportētu itāļu e-rēķinus. Itāļu FatturaPA e-rēķiniem izmantojiet šādas standarta konfigurācijas vai faktiskās pielāgotās konfigurācijas, ko izmantojat e-rēķinu izrakstīšanai:

    - Pārdošanas rēķins (IT)
    - Projekta rēķins (IT)

    Kad izveidojat e-rēķinu izrakstīšanas līdzekli, kas ir atvasināts no cita e-rēķinu izrakstīšanas līdzekļa, visi ER formāti tiek pārmantoti no oriģinālā līdzekļa.

3. Atlasiet noteiktu ER formāta faila konfigurāciju.
4. Atlasiet **Rediģēt** vai **Skatīt**, lai atvērtu lapu **Formāta veidotājs**.

    ![Formāta veidotāja lapas atvēršana](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Lai rediģētu un skatītu ER formāta failu konfigurācijas, izmantojiet lapu **Formāta veidotājs**.

    ![Formāta veidotāja lapa](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Pārvaldīt e-rēķinu izrakstīšanas līdzekļa iestatījumus

- Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot**, **Dzēst** vai **Rediģēt**, lai pārvaldītu e-rēķinu izrakstīšanas līdzekļa iestatījumus.

![E-rēķinu izrakstīšanas līdzekļa iestatījumu pārvaldība](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Šajā darbībā konfigurējiet notikumus, kas attiecināmi uz elektroniskajiem rēķiniem, tostarp XML izvades failu ģenerēšanu **FatturaPA** formātā un digitālu parakstīšanu (ja nepieciešams).

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurēt pārdošanas rēķina līdzekļu iestatījumu

1. Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Pārdošanas rēķins**.
2. Atlasiet **Rediģēt**.
3. Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu. Darbības definē oprerāciju sarakstu, kas ir jāpalaiž secīgi, lai veiktu notikuma pilnīgu izpildi.

    ![Cilne Darbības](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Darbības ID | Darbības nosaukums        | Darbības apraksts                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Transformējiet dokumentu | Izveidojiet e-rēķina XML failu **FatturaPA** formātā. |
    | 2         | Parakstīt dokumentu      | Lietojiet digitālo parakstu XML failam.             |

4. Atlasiet cilni **Piemērojamības noteikumi**, lai skatītu un uzturētu piemērojamības noteikumus. Piemērojamības noteikumi nosaka kontekstu, kurā darbība tiks izpildīta.

    ![Piemērojamības noteikumu cilne](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Atlasiet cilni **Mainīgie**, lai skatītu un uzturētu mainīgos.

    ![Cilne Mainīgie](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Definējiet publiskus mainīgos, kas nepieciešami darbību izpildei.

### <a name="configure-the-project-invoice-feature-setup"></a>Konfigurēt projektu rēķina līdzekļa iestatījumu 

Darbības un iestatījumi, kas nepieciešami līdzekļa **Projekta rēķins** iestatījuma konfigurēšanai, ir ļoti līdzīgi līdzekļa **Pārdošanas rēķins** iestatījuma darbībām un iestatījumiem. Strādājot ar projekta rēķiniem, skatiet pārdošanas rēķinu procedūras.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>E-rēķinu izrakstīšanas līdzekļa piešķiršana videi

1. Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Vides** atlasiet **Iespējot**.
2. Laukā **Vide** atlasiet vidi.
3. Laukā **Spēkā no** atlasiet datumu, kad videi jāstājas spēkā.
4. Atlasiet **Iespējot**. 

![E-rēķina vides iespējošana](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Publicējiet e-rēķinu izrakstīšanas līdzekli

Varat publicēt e-rēķinu izrakstīšanas līdzekli, mainot versijas statusu uz **Pabeigts** vai **Publicēts**.

### <a name="change-the-version-status-to-completed"></a>Mainiet versijas statusu uz Pabeigts

1. Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Melnraksts**.
2. Atlasiet **Mainīt statusu \> Pabeigts**. 

### <a name="change-the-version-status-to-published"></a>Mainiet versijas statusu uz Publicēts 

1. Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Pabeigts**.
2. Atlasiet **Mainīt statusu \> Publicēt**.

![E-rēķinu izrakstīšanas līdzekļa statusa maiņa](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>Iestatiet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrāciju programmā Finance

Finance iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Importējiet ER datu modeli, ER datu modeļa kartēšanu un konteksta konfigurācijas FatturaPA e-rēķiniem.
2. Konfigurējiet sertifikātu, kas nepieciešams, lai digitāli parakstītu itāļu e-rēķinus.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Importējiet ER datu modeli, datu modeļa kartēšanu un formātus

1. Darbvietā **Elektroniskie pārskati** pārbaudiet, vai konfigurācijas nodrošinātājs **Biznesa dokumentu pakalpojums** ir iestatīts kā **Aktīvs**.
2. Atlasiet **Repozitoriji**.
3. Atlasiet **Globālais resurss \> Atvērt**.
4. Importēt **Rēķina modelis**, **Rēķina modeļa kartēšana** un **Debitora rēķina konteksta modelis**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Ieslēgt līdzekli, lai eksportētu debitoru elektroniskos rēķinus Itālijai

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Līdzekļi** atzīmējiet izvēles rūtiņu **Iespējots**, kas atrodas līdzekļu reksturojuma rindā **IT00036**.

![FatturaPA līdzekļa ieslēgšana](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Konfigurēt elektroniskos dokumentus

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Elektroniskais dokuments** atlasiet **Pievienot** un ievadiet tabulas, kas nepieciešamas, lai ģenerētu itāļu e-rēķinus:

    - **Tabulas nosaukums:** Debitoru rēķinu žurnāls
    - **Tabulas nosaukums:** Projekta rēķins

3. Katrai tabulai definējiet saistīto dokumentu kontekstu:

    - Tabulai **Debitoru rēķinu žurnāls** atlasiet **Debitora rēķina konteksts**.
    - Tabulai **Projekta rēķins** atlasiet **Projekta rēķina konteksts**.

![Atbilžu veidu iestatīšana](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Elektroniska rēķina apstrāde

Finance apstrādes laikā jūs veiksiet šādus uzdevumus:

1. Ģenerēt itāļu e-rēķinus, izmantojot elektronisko rēķinu izrakstīšanas pievienojumprogrammu
2. Skatiet izpildes žurnālus un pārskatiet apstrādes rezultātus

### <a name="generate-electronic-invoices"></a>Ģenerēt elektroniskos rēķinus

Pēc tam, kad ieslēdzat līdzekli **Konfigurējamu elektronisko rēķinu pievienošana** un aktivizējat līdzekli **IT00036**, vairs nevar izmantot veco finanšu procesu itāļu e-rēķinu ģenerēšanai. Tas ir aizstāts ar jaunu procesu, kura nosaukums ir **Iesniegt elektroniskus dokumentus**.

Varat iesniegt dokumentus manuāli, pamatojoties uz pieprasījumu e-rēķinu dokumentiem.

> [!NOTE]
> Pirms turpināt, pārbaudiet, vai ir pabeigts itāļu e-rēķiniem nepieciešamais iestatījums. Plašāku informāciju skatiet šeit: [Debitoru elektroniskie rēķini](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Ņemiet vērā, ka daži no šajā tēmā aprakstītajiem iestatīšanas darbībam var nebūt pieejamas elektronisko rēķinu izrakstīšanas pievienojumprogrammas aktivizēšanas dēļ.

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.
2. Pirmā dokumenta iesniegšanai iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**. Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.
3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.

![Dialoglodziņš Iesniegt elektroniskos dokumentus](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filtra vaicājums

1. Dialoglodziņā **Pieprasījums** konfigurējiet filtrēšanas nosacījumus gan pārdošanas rēķiniem, gan projekta rēķiniem, vai atstājiet nosacījumus tukšus, lai iekļautu visus neiesniegtos rēķinus.

    ![Iesniegšanas filtra kritēriju iestatīšana](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Lai dialoglodziņu **Pieprasījums** aizvērtu, atlasiet **Labi**.
3. Atlasiet **Labi**, iesniedziet atlasītos dokumentus.

> ! [PIEZĪME] Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu pievienojumprogrammu. Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.

#### <a name="view-submission-logs"></a>Skatīt iesniegšanas žurnālus

Varat skatīt visu iesniegto dokumentu iesniegšanas žurnālus.

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls** vai **Projekta rēķins**, lai filtrētu pieprasītos elektroniskos dokumentus.

    ![Dokumenta veida atlasīšana, lai apskatītu iesniegšanas žurnālus](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Vērtība, kas tiek rādīta kolonnā **Iesniegšanas statuss**, norāda iesniegšanas procesa statusu. Tas norāda, vai process darbojās kā konfigurēts, un vai ir nepieciešama papildu darbība.

3. Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.

    ![Iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Kopsavilkuma cilnē **Apstrādes darbības** var skatīt izpildes žurnālu darbībām, kas konfigurētas līdzekļa versijā, kas tika iestatīta RCS. Kolonna **Statuss** rāda, vai darbība ir veiksmīgi izpildīta.
5. Kopsavilkuma cilnē **Darbības faili** var apskatīt starpposma failus, kas tika ģenerēti darbību izpildes laikā. Varat atlasīt **Skats**, lai lejupielādētu izvades XML failu **FatturaPA** formātā un apskatīt tā saturu.

## <a name="related-topics"></a>Saistītās tēmas

- [Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-service-overview.md)
- [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md)
- [Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]