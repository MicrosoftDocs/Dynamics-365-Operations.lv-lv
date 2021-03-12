---
title: Sākt ar elektronisko rēķinu pievienojumu Meksikai
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Meksikai programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d91f377af2514af932ea585adb75a56bdee13871
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988486"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Sākt ar elektronisko rēķinu pievienojumu Meksikai

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronisko rēķinu pievienojums Meksikai pašlaik var nenodrošināt visas funkcijas, kas ir pieejamas Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management iebūvētajā Comprobante Fiscal Digital por Internet (CFDI) dokumentu integrācijā un saistītajā integrācijā.

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Meksikai. Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts risinājumos Regulatory Configuration Services (RCS) un Finance. Tas arī palīdz veikt darbības, kas jāveic programmā Finance, lai iesniegtu CFDI rēķinus, izmantojot pakalpojumu, un tas izskaidro, kā pārskatīt apstrādes rezultātus un CFDI rēķinu statusu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms šajā tēmā aprakstīto darbību veikšanas ir jāpabeidz darbības sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS iestatījumi

RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Importējiet e-rēķinu izrakstīšanas līdzekli CFDI rēķinu apstrādei.
2. Pārskatiet formāta konfigurācijas, kas nepieciešamas, lai ģenerētu, iesniegtu un saņemtu atbildes par CFDI rēķiniem, un lai iesniegtu un saņemtu atbildes par atcelšanu.
3. Konfigurējiet notikumus, kas atbalsta CFDI rēķinu iesniegšanas scenārijus.
4. Publicējiet e-rēķinu izrakstīšanas līdzekli CFDI rēķiniem.

> [!NOTE]
> "E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri. Šajā gadījumā CFDI rēķini (MX) ir e-rēķinu izrakstīšanas līdzeklis, ko iestatīsit.

## <a name="import-the-e-invoicing-feature"></a>Importējiet e-rēķinu izrakstīšanas līdzekli

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **e-rēķinu izrakstīšana**.
3. Lapā **E-rēķina līdzekļi** atlasiet **Importēt**, lai importētu līdzekli **CFDI rēķini (MX)** no Globālās krātuves.

    > [!NOTE]
    > Ja sarakstā neredzat līdzekli, atlasiet **Sinhronizēt** un pēc tam atkārtojiet 3. darbību.

![CFDI rēķinu (MX) līdzekļa importēšana](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Importējot līdzekli **CFDI rēķins (MX)** no globālās krātuves, tiek importēti arī visi līdzekļa iestatījumi, tostarp konfigurācijas un darbības.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Izveidot jaunu CFDI rēķinu (MX) līdzekļa versiju

Varat izveidot jaunu versiju, ja, piemēram, ir jāatjaunina URL. Plašāku informāciju skatiet [E-rēķinu izrakstīšanaa CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Jauns**.

![Jaunas e-rēķinu izrakstīšanas līdzekļa versijas pievienošana](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Atjaunināt konfigurācijas versiju

1. Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Konfigurācijas** vai **Dzēst**, lai pārvaldītu konfigurāciju versijas (ER failu formātu konfigurācijas).

    ![E-rēķinu izrakstīšanas līdzekļa konfigurāciju pārvaldība](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Kad izveidojat jaunu versiju, visas konfigurācijas tiek pārmantotas no pēdējās publicētās versijas. Lai apstrādātu CFDI rēķinus, ir nepieciešamas šādas konfigurācijas:

    - CFDI rēķins (BusinessDocumentService)
    - CFDI atbilžu ziņojuma importēšana
    - CFDI kļūdu žurnāla importēšana
    - CFDI atcelšanas pieprasījums (MX) (BusinessDocumentService)
    - CFDI rēķins (BusinessDocumentService)

2. Sarakstā atlasiet konfigurācijas versiju un pēc tam atlasiet **Rediģēt** vai **Skatīt**, lai atvērtu lapu **Formāta veidotājs**, kurā var rediģēt vai skatīt konfigurāciju.

    ![Formāta veidotāja lapas atvēršana](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Lai rediģētu un skatītu ER formāta failu konfigurācijas, izmantojiet lapu **Formāta veidotājs**. Papildinformāciju skatiet tēmā [Elektronisko dokumentu konfigurāciju izveide](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Formāta veidotāja lapa](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Pārvaldīt e-rēķinu izrakstīšanas līdzekļa iestatījumus

- Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot**, **Dzēst** vai **Rediģēt**, lai pārvaldītu e-rēķinu izrakstīšanas līdzekļa iestatījumus.

![E-rēķinu izrakstīšanas līdzekļa iestatījumu pārvaldība](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Lai iesniegtu CFDI rēķinus autorizācijai (ģenerēt XML failu, iesniegt XML failu un apstrādāt atbildi), ir jānorāda līdzekļa **Pārdošanas rēķins** iestatījums.

Lai iesniegtu CFDI rēķina atcelšanu, ir jānorāda līdzekļu **Atcelšana** un **Atcelt** iestatījumi.

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurēt pārdošanas rēķina līdzekļu iestatījumu

1. Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Pārdošanas rēķins**.
2. Atlasiet **Rediģēt**, lai konfigurētu darbības, piemērojamības nosacījumus un mainīgos.

    ![E-rēķinu izrakstīšanas līdzekļa iestatījumu rediģēšana](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu. Darbības definē oprerāciju sarakstu, kas ir jāpalaiž secīgi, lai veiktu notikuma pilnīgu izpildi.

    ![Cilne Darbības](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Darbības ID | Darbība                   | Darbības nosaukums                                  | Darbības apraksts                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Transformējiet dokumentu       | Ģenerēt CFDI e-rēķinu bez ciparzīmes | Ģenerēt CFDI e-rēķinu.                                |
    | 2         | Parakstīt dokumentu            | Ciparzīme                                 | Elektroniski parakstīt e-rēķinu iesniegšanai.                |
    | 3         | Izsaukt Meksikas PAC pakalpojumu | Iesniegt CFDI e-rēķinu                        | Windows Communication Foundation (WCF) klients iesniedz CFDI e-rēķinu. |
    | 4         | Apstrādāt atbildi         | Analizēt tīmekļa pakalpojuma atbildi                 | Analizēt tīmekļa pakalpojuma atbildi un atgriezt kļūdu žurnālu. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Iestatiet vietrādi URL Meksikas PAC tīmekļa pakalpojumiem 

1. Lapā **Līdzekļu versijas iestatīšana** cilnē **Darbības** kopsavilkuma cilnē **Darbības** atlasiet **Izsaukt Meksikas PAC pakalpojumu**.
2. Kopsavilkuma cilnē **Parametri** laukā **URL adrese** ievadiet vietrādi URL tīmekļa pakalpojuma CFDI rēķina iesniegšanai.

> [!NOTE]
> Izmantojiet tās pašas darbības, lai atjauninātu vietrādi URL darbībai **Izsaukt Meksikas PAC pakalpojumu** līdzekļu **Atcelt** un **Atcelšanas pieprasījums** iestatījumiem.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Piešķirt melnraksta versiju elektroniskajai rēķinu izrakstīšanas videi

1. Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Vides** atlasiet **Iespējot**.
2. Laukā **Vide** atlasiet vidi.
3. Laukā **Spēkā no** atlasiet datumu, kad videi jāstājas spēkā.
3. Atlasiet **Iespējot**.

![E-rēķina vides iespējošana](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Mainiet versijas statusu uz Pabeigts

1. Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Melnraksts**.
2. Atlasiet **Mainīt statusu \> Pabeigts**.

## <a name="change-the-version-status-to-published"></a>Mainiet versijas statusu uz Publicēts

- Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Mainīt statusu \> Publicēt**.

## <a name="publish-the-e-invoicing-feature"></a>Publicējiet e-rēķinu izrakstīšanas līdzekli

1. Lapā **E-rēķina līdzekļi** atlasiet cilni **Versijas**, lai pārvaldītu līdzekļa **CFDI rēķini (MX)** statusu.
2. Atlasiet **Mainīt statusu**, lai mainītu līdzekļa statusu.

![E-rēķinu izrakstīšanas līdzekļa statusa maiņa](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Iestatiet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrāciju programmā Finance

Lai iestatītu elektronisko rēķinu izrakstīšanas pievienojumprogrammas programmā Finance, tiks pabeigti šādi uzdevumi:

1. Importējiet ER datu modeli, ER datu modeļa kartēšanu un formatus, kas ir nepieciešami CFDI rēķiniem.
2. Konfigurējiet atbilžu veidus CFDI rēķinu atjaunināšanai. Šie atbilžu veidi tiek izmantoti atbildei no autorizētā sertifikācijas sniedzēja (PAC) servera.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Importējiet ER datu modeli, ER datu modeļa kartēšanu un konteksta konfigurācijas CFDI rēķiniem

1. Pieteikšanās programmā Finance.
2. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet nosaukumu **Microsoft**. Pārliecinieties, vai šis konfigurācijas nodrošinātājs ir iestatīts kā **Aktīvs**. Papildinformāciju par to, ka iestatīt nodrošinātāju kā **Aktīvs** skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Atlasiet **Repozitoriji**.
4. Atlasiet **Globālais resurss \> Atvērt**.
5. Importējiet **Rēķina modelis**, **Rēķina modeļa kartēšana**, **CFDI rēķina formāts (MX)**, **CFDI rēķina atcelšanas pieprasījuma formāts (MX)** un **CFDI rēķina atcelšanas formāts (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Ieslēdziet līdzekli CFDI rēķinu apstrādei

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Līdzekļi** atzīmējiet izvēles rūtiņu **Iespējot**, kas atrodas līdzekļu reksturojumu rindās **MX-00010** un **MX-00016**.

![CFDI rēķinu apstrādes līdzekļu ieslēgšana](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Importējiet ER konfigurācijas un iestatiet atbilžu veidus CFDI rēķinu grāmatošanai

#### <a name="import-er-configurations"></a>ER konfigurāciju importēšana

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet nosaukumu **Microsoft**.
3. Atlasiet **Repozitoriji**.
4. Atlasiet **Globālais resurss \> Atvērt**.
5. Importējiet **Atbildes ziņojuma modelis**, **CFDI kļūdu žurnāla importēšana (MX)** un **CFDI atbildes ziņojuma importēšana (MX)**.

#### <a name="set-up-the-response-types"></a>Atbildes veidu iestatīšana

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Elektronisks dokuments** atlasiet **Pievienot**.
3. Ievadiet debitora rēķinu žurnālu un pēc tam laukā **Tabulas nosaukums** atlasiet projekta rēķinu.
4. Katrai tabulai definējiet saistīto dokumentu kontekstu:

    - Tabulai **Debitoru rēķinu žurnāls** ievadiet **Debitora rēķina konteksts**.
    - Tabulai **Projekta rēķins** ievadiet **Projekta rēķina konteksts**.

4. Atlasiet **Atbilžu veidi**, lai konfigurētu atbilžu veidus, kas var tikt atgriezti no elektronisko rēķinu izrakstīšanas pievienojumprogrammas un iekļauta debitoru rēķinu žurnālā vai projekta rēķinā.
5. Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** atlasiet **Atbilde**.
6. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
7. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojuma importēšanas formāts — Modeļa kartēšana no atbildes ziņojuma**.
8. Atlasiet **Saglabāt**.
9. Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** atlasiet **ResponseData**.
10. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
11. Laukā **Modeļa kartēšana** atlasiet **CFDI atbildes datu importēšanas formāts (detaļas) — Atbildes datu importēšana**.
12. Atlasiet **Saglabāt**.

## <a name="process-electronic-invoices-in-finance"></a>Apstrādāt elektroniskos rēķinus programmā Finance 

CFDI rēķinu apstrādes laikā programmā Finance, izmantojot elektronisko rēķinu izrakstīšanas pievienojumprogrammu, varat veikt šādus uzdevumus:

- Iesniegt CFDI rēķinus.
- Skatiet iesniegšanas izpildes žurnālus.
- Iesniedziet CFDI rēķina atcelšanu.

### <a name="submit-cfdi-invoices"></a>Iesniegt CFDI rēķinus

Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, vairs nevarēsiet izmantot procesu **Elektronisko rēķinu eksportēšana/importēšana** (**Realizācija \> Rēķini \> E-rēķini**), lai iesniegtu CFDI rēķinus. Tas ir aizstāts ar jaunu procesu, kura nosaukums ir **Iesniegt elektroniskus dokumentus**.

> [!NOTE]
> Pirms izmantojat jauno procesu **Iesniegt elektroniskos dokumentus**, pārbaudiet, vai Meksikas e-rēķiniem nepieciešamais iestatījums ir pabeigts. Plašāku informāciju skatiet [CFDI izkārtojuma versija 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.
2. Pirmā dokumenta iesniegšanai vienmēr iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**. Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.
3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.

![CFDI dokumenta iesniegšana](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu pievienojumprogrammu. Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.

### <a name="view-submission-logs"></a>Skatīt iesniegšanas žurnālus

Var apskatīt visu iesniegto dokumentu vai tikai viena iesniegtā dokumenta iesniegšanas žurnālus.

#### <a name="view-all-submission-logs"></a>Skatīt visus iesniegšanas žurnālus

Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, ir pieejama jauna lapa, kas ļauj sekot līdzi dokumentu iesniegšanas procesam. Varat izmantot šo lapu, lai skatītu visu iesniegto dokumentu iesniegšanas žurnālus.

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls**, lai filtrētu pieprasītos elektroniskos dokumentus.

    ![Dokumenta veida atlasīšana, lai apskatītu iesniegšanas žurnālus](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.

    ![Iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Informācija iesniegšanas žurnālos tiek sadalīta starp trim kopsavilkuma cilnēm:

- **Apstrādes darbības** – Šī kopsavilkuma cilne rāda izpildes žurnālu darbības, kas konfigurētas līdzekļa versijā, kas tika iestatīta RCS. Kolonna **Statuss** rāda, vai darbība ir veiksmīgi izpildīta.
- **Darbības faili** – Šī kopsavilkuma cilne rāda starpposma failus, kas tika ģenerēti darbību izpildes laikā. Varat atlasīt **Skatīt** lai lejupielādētu un skatītu failu.
- **Apstrādes darbību žurnāls** – Šajā kopsavilkuma cilnē tiek rādīti saziņas rezultāti starp elektronisko rēķinu izrakstīšanas pievienojumprogrammu un mērķa tīmekļa pakalpojumu. Tas arī parāda, ko atgrieza apstrāde no tīmekļa pakalpojuma. Kolonnā **Kļūdas kods** ir parādīts atgrieztais kods, ko atgrieza autorizācijas tīmekļa pakalpojums.

Kad iesniegtais CFDI rēķins ir autorizēts, tā statuss tiek atjaunināts uz **Apstiprināts**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Skatīt iesniegumu žurnālus no CFDI rēķiniem

Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, varat arī skatīt iesniegumu žurnālus no CFDI rēķiniem.

1. Dodieties uz **Debitoru parādi \> Uzziņas un atskaites \> CFDI (elektroniskie rēķini)**.
2. Atlasiet CFDI rēķinu, kas tika iesniegts pēc tam, kad līdzeklis **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana** tika ieslēgts.
3. Darbības rūtī, kas atrodas cilnē **Vēsture**, atlasiet **Elektronisko dokumentu žurnāls**.

![Iesniegšanas žurnālu apskate no CFDI rēķiniem](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> CFDI rēķiniem, kas tika iesniegti pirms līdzekļa **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana** ieslēgšanas, ir pieejama poga **Vēsture**. Poga **Vēsture** nav pieejama CFDI rēķiniem, kas tika iesniegti pēc līdzekļa **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana** ieslēgšanas.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Iesniedziet CFDI rēķinu atcelšanu

Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšana**, vairs nevarēsiet izmantot veco procesu, lai atceltu CFDI rēķinus. Tas ir aizstāts ar jaunu atcelšanas procesu, kas ir iegults lapā **Elektronisko dokumentu iesniegšanas žurnāls**.

1. Dodieties uz **Debitoru parādi \> Uzziņas un atskaites \> CFDI (elektroniskie rēķini)**.
2. Ja CFDI rēķina statuss ir **Apstiprināts**, atlasiet **Funkcijas \> Atcelt CFDI**.
3. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
4. Atlasiet CFDI rēķinu un pēc tam atlasiet **Funkcijas \> Sūtīt saistītos iesniegumus**.
5. Ievadiet saistītā iesnieguma aprakstu un pēc tam atlasiet **Labi**.

#### <a name="view-cancellation-submission-logs"></a>Skatīt atcelšanas iesniegšanas žurnālus

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls**, lai filtrētu tikai debitoru rēķinu žurnāla dokumentus.
3. Atlasiet CFDI rīķinu un pēc tam Darbību rūtī atlasiet **Vaicājumi \> Saistītie iesniegumi**.

    Lapa **Saistītais iesniegums** parāda visus saistītos iesniegumus un to iesniegšanas statusu dotajam CFDI rīķinam. Sekojošajā ilustrācijā pirmā rinda ataino iesniegumu, kas pieprasīja CFDI rīķina apstiprināšanu. Otrā rinda ataino iesniegumu, kas atcēla šo CFDI rīķinu.

    ![Atcelšanas iesniegšanas žurnālu apskate](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.

    ![Atcelšanas iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Iespējojot MX-00010 un MX-00016 (CFDI rēķins un CFDI atcelšana) līdzekļus, var būt nepieciešams nosūtīt ierobežotus datus, kas ietver organizācijas nodokļa reģistrācijas ID. Tas tiks nosūtīts trešo personu aģentūrām, ko pilnvarojusi nodokļu iestāde, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekš noteiktā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu. Administrators var iespējot un atspējot līdzekļus MX-00010 un MX-00016 (CFDI rēķins un CFDI atcelšana), pārvietojoties uz **Organizācijas administrēšana \> Iestatījumi \> Elektroniskā dokumenta parametri**. Atlasiet cilni **Līdzekļi**, atlasiet rindas, kas satur līdzekļus MX-00010 un MX-00016, un pēc tam veiciet atbilstošo atlasi. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.

## <a name="additional-resources"></a>Papildu resursi

- [Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-service-overview.md)
- [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md)
- [Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana](e-invoicing-setup.md)
