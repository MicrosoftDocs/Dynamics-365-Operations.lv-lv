---
title: Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 61933bb846383932d7dd73e9c4d3c2db7a515a98
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835997"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu. Vispirms tas palīdz veikt konfigurācijas darbības programmās Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) un Dynamics 365 Finance. Pēc tam tas apraksta dokumentu iesniegšanas procesu ar pakalpojuma starpniecību, izmantojot Dynamics 365 Finance vai Dynamics 365 Supply Chain Management. Uzzināsit arī, kā interpretēt iesniegumu žurnālus.

## <a name="availability"></a>Pieejamība

Elektronisko rēķinu izrakstīšanas pievienojumprogramma sākotnēji ir pieejama vairākām valstīm. Pievienojumprogramma atbalsta elektronisko rēķinu izveidošanu un šādu biznesa dokumentu iesniegšanu:

| Valsts/reģions  | Biznesa dokuments                          |
|-----------------|--------------------------------------------|
| Austrija         | Pārdošanas un Projektu rēķini                 |
| Beļģija         | Pārdošanas un Projektu rēķini                 |
| Brazīlija          | Elektroniskā finanšu dokumenta modelis 55 (NF-e) |
| Dānija         | Pārdošanas un Projektu rēķini                 |
| Igaunija         | Pārdošanas un Projektu rēķini                 |
| Somija         | Pārdošanas un Projektu rēķini                 |
| Francija          | Pārdošanas un Projektu rēķini                 |
| Vācija         | Pārdošanas un Projektu rēķini                 |
| Itālija           | Pārdošanas un Projektu rēķini                 |
| Meksika          | CFDI rēķins                               |
| Nīderlande     | Pārdošanas un Projektu rēķini                 |
| Norvēģija          | Pārdošanas un Projektu rēķini                 |
| Spānija           | Pārdošanas un Projektu rēķini                 |
| Eiropa          | PEPPOL Pārdošanas un Projektu rēķini          |
    
## <a name="licensing"></a>Licencēšana

Varat izmantot Elektronisko rēķinu izrakstīšanas pievienojumprogramma ar pašreizējo licenci. Lai izmantotu pakalpojumu, nav nepieciešamas papildu licences.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat šajā tēmā norādītās darbības, ir jāievieš šādi priekšnosacījumi:

- Piekļūstiet savam LCS kontam.
- LCS izvietošanas projekts, kas ietver Finance vai Supply Chain Management versiju 10.0.12 vai jaunāku.
- Piekļūstiet savam RCS kontam.
- Ieslēdziet līdzekli Globalizācija jūsu RCS kontā, izmantojot moduli **Līdzekļu pārvaldība**. Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)
- Izveidot galvenās glabātavas resursu un krātuves kontu risinājumā Azure. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Pārskats

Sekojošajā attēlā ir parādītas piecas galvenās darbības, kas jāveic šajā tēmā.

![Pārskats par piecām šīs tēmas darbībām](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure resursu iestatījumi:** Azure krātuves konfigurēšana un ciparu sertifikātu augšupielāde Azure galvenajā glabātavā.
2. **LCS iestatīšana:** instalējiet pievienojumprogrammu, kas paredzēta mikropakalpojumiem.
3. **RCS iestatījumi:** iestatiet vidi, lietotāju piekļuvi un e-rēķinu izrakstīšanas līdzekļus.
4. **Debitora iestatījumi:** iestatiet savienojumu starp debitoru un elektronisko rēķinu izrakstīšanas pievienojumprogrammu un izslēdziet vecos līdzekļus atbilžu iesniegšanai un saņemšanai elektroniskajiem dokumentiem.
5. **Iesniegt rēķinus:** iesniedziet elektroniskus dokumentus, izmantojot elektronisko rēķinu izrakstīšanas pievienojumprogrammu un saņemiet atbildes.

> [!NOTE]
> Dažas konfigurācijas darbības šajā tēmā ir kopīgas un valsts/reģiona agnostiski. Darbības un iestatīšanas procedūras, kas attiecas uz valsti/reģionu, ir aprakstītas tēmās, kas attiecas uz valsti/reģionu.

## <a name="lcs-setup"></a>LCS iestatījumi

1. Piesakieties savā LCS kontā.
2. Atlasiet LCS izvietošanas projektu. Lai varētu atlasīt projektu, tam ir jābūt izveidotam un palaistam.
3. Kopsavilkuma cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
4. Atlasiet **Biznesa dokumentu iesniegšana**.
5. Dialoglodziņā **Iestatīt pievienojumprogrammu** laukā **AAD pieteikuma ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Šī vērtība ir fiksēta vērtība.
6. Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta ID.

    ![Iestatījuma pievienojumprogramma dialoglodziņā LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

7. Atzīmējiet izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.
8. Atlasiet **Instalēt**.

## <a name="rcs-setup"></a>RCS iestatījumi

RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:

1. Iestatiet galveno glabātavu RCS.
2. Iestatiet RCS integrāciju ar elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri.
3. Izveidojiet elektronisko rēķinu izrakstīšanas pievienojumprogrammas vidi jūsu organizācijai.

### <a name="set-up-the-key-vault-in-rcs"></a>Iestatiet galveno glabātavu RCS

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzekļi** sadaļā **Vides** atlasiet elementu **e-rēķinu izrakstīšana**.
3. Atlasiet **Pakalpojumu vides**.

    ![Servisa vides izvēle](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Opcija **Saistītās lietojumprogrammas** nodrošina piekļuvi elektroniskās rēķinu izrakstīšanas pievienojumprogrammas automātiskai konfigurēšanai Finance vai Supply Management caur RCS. Tomēr pašlaik šis līdzeklis joprojām ir izstrādes gaitā.

4. Darbību rūtī atlasiet **Galvenās glabātavas parametri**.

    ![Galvenās glabātavas parametru izvēle](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Lai pievienotu galveno glabātavu, darbību rūtī atlasiet **Jauns**.
6. Laukā **Laukā Key Vault URI** ievadiet galvenās glabātavas resursa atribūta vērtību **DNS nosaukums**, ko konfigurējāt risinājumā Azure. Lai iegūtu informāciju par to, kur atrast vērtību **DNS nosaukums**, skatiet sadaļu [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Galvenās glabātavas URI lauks](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Kopsavilkuma cilnē **Sertifikāti** atlasiet **Pievienot** un ievadiet ciparsertifikātu nosaukumus un galvenās glabātavas noslēpumus. Abas vērtību kopas ir konfigurētas uz galvenās glabātavas resursu Azure.

    ![Sertifikātu pievienošana](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Ja jūsu valstij/reģionam raksturīgam rēķinam ir nepieciešama sertifikātu ķēde, lai pielietotu elektronisko parakstu, atlasiet **Sertifikātu ķēde** darbības rūtī un pēc tam ievadiet sertifikātu vai galvenās glabātavas noslēpumu secību, kas veido šo ķēdi.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Iestatiet RCS integrāciju ar elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri

1. Darbvietas **Globalizācijas līdzekļi** sadaļā **Saistītās saites** atlasiet saiti **Elektronisko pārskatu veidošanas parametri**.
2. Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar Lifecycle Service**. Ja nevēlaties izveidot savienojumu ar LCS, atlasiet **Atcelt**.
3. Cilnē **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**, kas atrodas laukā **Pakalpojuma galapunkta URI**, ievadiet `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
4. Laukā **Programmas ID** pārbaudiet, vai tas rāda ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Šī vērtība ir fiksēta vērtība.
5. Laukā **LCS vides ID** ievadiet jūsu LCS abonementa konta ID.

![Elektronisko rēķinu izrakstīšanas pievienojumprogrammas parametru ievade](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Pievienot elektronisko rēķinu izrakstīšanas pievienojumprogrammas vidi

Elektroniskajai rēķinu izrakstīšanas pievienojumprogrammai, piemēram, Dev, Test vai ražošanas vidēm, var izveidot dažādas vides.

1. Darbvietā **Globalizācijas līdzekļi** sadaļā **Vides** atlasiet elementu **e-rēķinu izrakstīšana**.
2. Atlasiet **Jauns**, lai izveidotu vidi.
3. Laukā **Krātuves SAS marķiera konts** ievadiet galvenās glabātavas noslēpuma nosaukumu, ko konfigurējāt galvenajā glabātavā RCS.

    ![Noliktavas SAS marķiera konta lauks](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Kopsavilkuma cilnē **Lietotāji** atlasiet **Jauns**, lai piešķirtu piekļuvi lietotājiem šai videi.

    ![Pakalpojuma lietotāju pievienošana](media/e-invoicing-services-get-started-enter-service-users.png)

5. Darbības rūtī atlasiet **Publicēt**, lai publicētu vidi elektronisko rēķinu izrakstīšanas pievienojumprogrammas serverī.

    ![Poga Publicēt](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>E-rēķinu izrakstīšanas līdzekļa iestatījumu

"E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri. E-rēķinu izrakstīšanas līdzekļu iestatījums apvieno, cita starpā, elektroniskās ziņošanas (Electronic reporting - ER) konfigurāciju formātus, lai izveidotu konfigurējamas eksporta un importa failus, un darbību un darbību plūsmu izmantošanu, lai iespējotu konfigurējamu noteikumu izveidi, lai nosūtītu pieprasījumus, importētu atbildes un parsētu atbildes saturu.

Rēķinu formātu un darbību plūsmu izmaiņu dēļ elektronisko rēķinu izrakstīšanas līdzekļa iestatījums ir atkarīgs no valsts/reģiona.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Iestatīt elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanu Finance vai Supply Chain Management 

Šīs iestatīšanas laikā, tiks izpildīti tālāk minētie uzdevumi.

1. Atvērt ierobežoto līdzekli
2. Ieslēdziet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanas iespēju, lai iespējotu integrāciju ar Finance.
3. Iestatiet elektronisko rēķinu izrakstīšanas pievienojumprogrammas galapunkta URL.
4. Importējiet ER konfigurācijas, kas saistītas ar valsts/reģiona specifisko elektroniskās rēķinu izrakstīšanas līdzekli.
5. Ieslēdziet piemērojamo valsts/reģiona e-rēķinu izrakstīšanas līdzekli.
6. Importējiet ER konfigurācijas un iestatiet atbildes veidus, kas ir nepieciešami, lai atjauninātu jūsu valsts/reģiona specifisko rēķina dokumentu kā iesniegšanas procesa rezultātu.

### <a name="open-flighted-feature"></a>Atvērt ierobežoto līdzekli
Elektronisko rēķinu integrācijas līdzeklis ir aktivizēts, izmantojot testējamo variantu (flighting). Testējamais variants ir jēdziens, kas dod iespēju pēc noklusējuma ieslēgt vai izslēgt līdzekli. Tālāk aprakstītās darbības nodrošina testējamo variantu neražošanas vidē. 

1. Izpildiet šādu SQL komandu:

    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Pēc iepriekš minēto izmaiņu veikšanas veiciet IISReset darbību visos AOS

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Iesledziet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrācijas līdzekli

1. Pierakstieties Finance vai Supply Chain Management.
2. Darbvietā **Līdzekļu pārvaldība** meklējiet jauno līdzekli, **Konfigurējamā elektronisko rēķinu pievienošanas integrācija**. Ja līdzeklis joprojām netiek uzrādīts Līdzekļu pārvaldības lapā, palaidiet **Pārbaudīt, vai nav atjauninājumu** funkciju
3. Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**.

### <a name="set-up-the-service-endpoint-url"></a>Pakalpojuma galapunkta URL iestatīšana

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Iesniegšanas pakalpojums**, kas atrodas laukā **Pakalpojuma galapunkta URL**, ievadiet `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. Laukā **Vide** ievadiet elektronisko rēķinu izrakstīšanas pievienojuma vides nosaukumu, ko izveidojāt RCS iestatīšanas laikā.

![Pakalpojuma parametru ievadīšana](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>ER konfigurāciju importēšana

Lai iespējotu to, ka biznesa dati tiek apkopoti un nosūtīti elektronisko rēķinu izrakstīšanas pievienojumprogrammai, ir jāimportē ER datu modelis un ER datu modeļa konfigurācija, kas saistīta ar valsts/reģiona specifisko e-rēķinu izrakstīšanas līdzekli, ko vēlaties izmantot.

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**. Pārliecinieties, vai šis konfigurācijas nodrošinātājs ir iestatīts kā **Aktīvs**. Papildinformāciju par to, ka iestatīt nodrošinātāju kā **Aktīvs** skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Atlasiet **Repozitoriji**.
4. Atlasiet **Globālais resurss**un pēc tam atlasiet **Atvērt**.
5. Dialoglodziņā **Savienojuma izveide ar Lifecycle Services** atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar Lifecycle Services**.
6. Atkarībā no valsts vai reģiona, kurā vēlaties izmantot e-rēķinu izrakstīšanas līdzekli, ir jāimportē atbilstošais datu modelis, datu modeļa kartēšana un formāti. Lai iegūtu informāciju par ER konfigurācijām, kuras ir jāimportē, skatiet valsts/reģiona specifisko tēmu "Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu".
7. Importēt **Debitora rēķina konteksta modelis**. Šis modelis ietver papildu parametrus, kas apraksta, cita starpā, vidi programmā Finance, kas tiek izmantots elektronisko rēķinu izrakstīšanas pievienojumprogrammai biznesa datu iesniegšanas laikā.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Ieslēdziet valsts/reģiona e-rēķinu izrakstīšanas līdzekļus

Lai ieslēgtu valstij/reģionam raksturīgos elektronisko rēķinu izrakstīšanas līdzekļus, lai tie darbotos ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu, ir jāieslēdz līdzeklis katrai juridiskajai personai, kurai vēlaties to izmantot. Pēc tam veco elektronisko rēķinu izrakstīšanas integrāciju vairs nevar izmantot, un ir ieslēgta integrācija ar jauno elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnē **Līdzekļi** tā līdzekļa rindā, kas ir saistīts ar jūsu valstij/reģionam raksturīgo e-rēķinu izrakstīšanas līdzekli, atzīmējiet izvēles rūtiņu kolonnā **Iespējots**. Lai iegūtu informāciju par to, kuru līdzekli ir jāieslēdz, skatiet valsts/reģiona specifisko tēmu "Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu".

![E-rēķinu izrakstīšanas līdzekļa ieslēgšana](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Ja jums ir vairākas juridiskas personas, kas ir konfigurēti dažādām valstīm vai reģioniem, jūs varat ieslēgt valsts/reģiona specifisko e-rēķinu izrakstīšanas līdzekli katrai juridiskajai personai.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importējiet ER konfigurācijas un iestatiet atbilžu veidus, lai atjauninātu savu valsts/reģiona specifisko rēķina dokumentu

Ja iesniegtais rēķina dokuments pieprasa atjaunināšanu pēc atbildes uz iesniegšanu valdības autorizācijas dienestos, jums ir jāimportē īpašs ER datu modelis un konfigurācijas, lai varētu atjaunināt rēķina dokumenta vai jebkura cita papildu lauka statusu.

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
2. Atlasiet **Repozitoriji**.
3. Atlasiet **Globālais resurss**un pēc tam atlasiet **Atvērt**.
4. Importēt **Atbildes ziņojuma modelis**, **Atbildes ziņojuma importēšanas formāts**, **Atbildes ziņojuma modeļa kartēšana uz mērķi** un **Faila satura importēšanas formāts**.
5. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
6. Cilnē **Elektroniskais dokuments** atlasiet **Pievienot**, lai ievadītu tabulas nosaukumu, kas ir saistīts ar jūsu valsts/reģiona specifisko rēķina dokumentu. Lai iegūtu informāciju par to, kurus tabulas nosaukumus ir jāizvēlās, skatiet valsts/reģiona specifisko tēmu "Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu".
7. Atlasiet **Atbilžu veidi**, lai konfigurētu atbilžu veidus. Lai iegūtu informāciju par to, kurus tabulas nosaukumus ir jāizvēlās, skatiet valsts/reģiona specifisko tēmu "Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu".

![Atbilžu veidu iestatīšana](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>E-rēķinu izrakstīšanas līdzekļu nosaukumi pēc valstīm 
Sekojošajā tabulā ir aprakstīti citi e-rēķinu izrakstīšanas līdzekļi, kas pieejami lejupielādei no elektronisko pārskatu globālās krātuves, lai ģenerētu elektroniskos rēķinus.
RCS varat lejupielādēt elektronisko rēķinu izrakstīšanas līdzekļus, kas uzskaitīti šajā tabulā, ER konfigurācijas un pieejamos e-rēķinu izrakstīšanas līdzekļu iestatījumus.
Programmā Finance varat iespējot saistītās līdzekļu atsauces lapā **Elektronisko dokumentu parametri**, lai izsniegtu elektroniskus rēķinus šīm valstīm. Lai iegūtu papildu informāciju, skatiet sadaļu [Valstu/reģionu specifiskie elektronisko rēķinu izrakstīšanas līdzekļi](#region-specific) ārgāk šajā tēmā.

| Līdzekļa nosaukums                      | Apraksts                                 | ER konfigurācijas                                                                                                  | Iestatījumi                                                                                                                                                         | Valsts/reģions  | Līdzekļa atsauce      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Austrijas elektroniskie rēķini (AT) | Pārdošanas un Projektu rēķini Austrijai      | - OIOUBL pārdošanas rēķins <br>- OIOUBL projekta rēķins <br>- OIOUBL pārdošanas kredīta nota <br>- OIOUBL projekta kredīta nota | - Pārdošanas rēķina ģenerēšana (AT) <br>- Projekta rēķina ģenerēšana (AT) <br>- Pārdošanas kredīta notas ģenerēšana (AT) <br>- Projekta kredīta notas ģenerēšana (AT)         | Austrija         | EUR-00023              |
| Beļģijas elektroniskais rēķins (BE)   | Pārdošanas un Projektu rēķini Beļģijai      | - UBL Pārdošanas rēķins BE <br>- UBL Projekta rēķins BE <br>- UBL projekta kredīta nota BE <br>- UBL pārdošanas kredīta nota BE | - Pārdošanas rēķina ģenerēšana (BE)<br>- Projekta rēķina ģenerēšana (BE) <br>- Pārdošanas kredīta notas ģenerēšana (BE) <br>- Projekta kredīta notas ģenerēšana (BE)         | Beļģija         | EUR-00023              |
| Dānijas elektroniskais rēķins (DK)    | Pārdošanas un Projektu rēķini Dānijai      | - OIOUBL pārdošanas rēķins <br>- OIOUBL projekta rēķins <br>- OIOUBL pārdošanas kredīta nota <br>- OIOUBL Projekta kredīta nota | - Pārdošanas rēķina ģenerēšana (DK) <br>- Projekta rēķina ģenerēšana (DK) <br>- Pārdošanas kredīta notas ģenerēšana (DK)<br>- Projekta kredīta notas ģenerēšana (DK)         | Dānija         | EUR-00023<br> DK-00001 |
| Nīderlandes elektroniskais rēķins (NL)     | Pārdošanas un Projektu rēķini Nīderlandei  | - UBL Pārdošanas rēķins NL <br>- UBL Projekta rēķins NL <br>- UBL pārdošanas kredīta nota NL <br>- UBL projekta kredīta nota NL | - Pārdošanas rēķina ģenerēšana (NL) <br> - Projekta rēķina ģenerēšana (NL) <br> - Pārdošanas kredīta notas ģenerēšana (NL) <br>- Projekta kredīta notas ģenerēšana (NL)          | Nīderlande | EUR-00023              |
| Igaunijas elektroniskais rēķins (EE)  | Pārdošanas un Projektu rēķini Igaunijai      | - Pārdošanas rēķins (EE) <br> - Projekta rēķins (EE)                                                                     | - Pārdošanas rēķina ģenerēšana (EE) <br>- Projekta rēķina ģenerēšana (EE)                                                                                           | Igaunija         | EUR-00023              |
| Somijas elektroniskais rēķins (FI)   | Pārdošanas un Projektu rēķini Somijai      | - Pārdošanas rēķins (FI) <br>- Projekta rēķina ģenerēšana (FI)                                                          | - Pārdošanas rēķina ģenerēšana (FI) <br>- Projekta rēķina ģenerēšana (FI)                                                                                           | Somija         | EUR-00023              |
| Francijas elektroniskais rēķins (FR)    | Pārdošanas un Projektu rēķini Francijai    | - UBL Pārdošanas rēķins FR <br> - UBL Projekta rēķins FR <br> - UBL pārdošanas kredīta nota FR <br>- UBL projekta kredīta nota FR | - Pārdošanas rēķina ģenerēšana (FR) <br> - Projekta rēķina ģenerēšana (FR) <br>- Pārdošanas kredīta notas ģenerēšana (FR) <br>- Projekta kredīta notas ģenerēšana (FR)         | Francija          | EUR-00023              |
| Vācijas elektroniskais rēķins (DE)    | Pārdošanas un Projektu rēķini Vācijai      |- Pārdošanas rēķins (DE) <br> - Projekta rēķins <DE>                                                                     | - Pārdošanas rēķina ģenerēšana (DE) <br>- Projekta rēķina ģenerēšana (DE)                                                                                           | Vācija         | EUR-00023              |
| Norvēģijas elektroniskais rēķins (NO) | Pārdošanas un Projektu rēķini Norvēģijai       | - OIOUBL pārdošanas rēķins <br>- OIOUBL projekta rēķins <br>- OIOUBL pārdošanas kredīta nota <br>- OIOUBL projekta kredīta nota | - Pārdošanas rēķina ģenerēšana (NO) <br>- Projekta rēķina ģenerēšana (NO) <br>- Pārdošanas kredīta notas ģenerēšana (NO) <br>- Projekta kredīta notas ģenerēšana (NO)          | Norvēģija          | EUR-00023<br> NO-00010 |
| Spānijas elektroniskais rēķins (ES)   | Pārdošanas un Projektu rēķini Spānijai        | - Pārdošanas rēķins (ES) <br>- Projekta rēķins (ES)                                                                     | - Pārdošanas rēķina ģenerēšana (ES) <br>- Projekta rēķina ģenerēšana (ES)                                                                                           | Spānija           | EUR-00023 <br>ES-00025 |
| Itālijas elektroniskais rēķins (IT)   | Pārdošanas un Projektu rēķini Itālijai        | - (Priekšskatījums) Pārdošanas rēķins (IT) <br> - Projekta rēķins (IT)                                                           | - Pārdošanas rēķins <br> - Projekta rēķins                                                                                                                           | Itālija           | EUR-00023 <br>IT-00036 |
| PEPPOL elektroniskais rēķins         | PEPPOL Pārdošanas un Projektu rēķinu ģenerēšana | - PEPPOL pārdošanas rēķins <br>- PEPPOL projekta rēķins <br>- PEPPOL pārdošanas kredīta nota <br> - PEPPOL Projekta kredīta nota | - PEPPOL Pārdošanas rēķina ģenerēšana <br>- PEPPOL Projekta rēķina ģenerēšana <br>- PEPPOL Pārdošanas kredīta notas ģenerēšana <br>- PEPPOL Projekta kredīta notas ģenerēšana |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektronisko rēķinu apstrāde programmās Finance un Supply Chain Management

Apstrādes laikā jūs veiksiet šādus uzdevumus:

1. Iesniedziet biznesa dokumentu (rēķinu), izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
2. Skatiet iesniegšanas izpildes žurnālus.

### <a name="submit-business-documents"></a>Biznesa dokumentu iesniegšana

Parastā iesniegšanas procesa laikā saziņa starp klientu un elektronisko rēķinu izrakstīšanas pievienojumprogrammu ir divvirzienu. Nolūks ir veikt divus galvenos uzdevumus elektronisko dokumentu iesniegšanas laikā:

1. Sūtīt visus elektroniskos dokumentus, kas gaida iesniegšanu no Finance, un kam ir pareizs iesniegšanas statuss, kas atbilst atlases kritērijiem.
2. Importēt, uz Finance, atbildi, ka elektronisko rēķinu izrakstīšanas pievienojumprogramma atgriežas iepriekš iesniegtajiem elektroniskajiem dokumentiem. Pēc importēšanas atbildes tiek parsētas, un biznesa dokumentu statuss tiek atbilstoši atjaunināts.

Jūs variet iesniegt biznesa dokumentus vai nu manuāli, vai balstoties uz jūsu grafika prasībām.

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.
2. Pirmā dokumenta iesniegšanai vienmēr iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**. Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.
3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.

![Dialoglodziņš Iesniegt elektroniskos dokumentus](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filtra vaicājums

1. Dialoglodziņā **aicājums** cilnē **Diapazons** ievadiet filtra kritērijus, izmantojot laukus **Tabula**, **Atveidotā tabula**, **Lauks** un **Kritēriji**.
2. Atlasiet **Pievienot**, lai pievienotu tik daudz papildu kritēriju, cik nepieciešams, lai atlasītu biznesa dokumentus.

    ![Iesniegšanas filtra kritēriju iestatīšana](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Lai dialoglodziņu **Pieprasījums** aizvērtu, atlasiet **Labi**.
4. Atlasiet **Labi**, lai iesniegtu atlasītos biznesa dokumentus elektroniskajai rēķinu izrakstīšanas pievienojumprogrammai.

    > [!NOTE]
    > Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu pievienojumprogrammu. Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.
    >
    > ![Izveidot savienojumu ar elektronisko dokumentu iesniegšanas pakalpojuma ziņojumu lodziņu](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Ja savienojums ir veiksmīgs, tiek parādīts apstiprinājuma ziņojums.
    >
    > ![Apstiprinājums savienojumam ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Aizveriet dialoglodziņu.

> [!NOTE]
> Pēc katra iesnieguma darbību centrs parāda iesniegto dokumentu skaitu.
>
> ![Darbību centra ziņojumi](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Iesniegšana pēc partijas

Tā vietā, lai veiktu dokumentu manuālu iesniegšanu, varat automatizēt iesniegšanas procesu un palaist to fonā, pamatojoties uz konfigurētu pakešuzdevuma izpildes biežumu.

1. Dialoglodziņā **Iesniegt elektroniskos dokumentus**, kopsavilkuma cilnē **Palaist fonā** iestatiet opciju **Pakešapstrāde** uz **Jā**.
2. Cilnē **Periodiskums** konfigurējiet pakešapstrādes biežumu.

![Iesniegšanas iestatīšana pēc partijas](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Skatīt visus iesniegšanas žurnālus

1. Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumenta veids** atlasiet dokumenta veidu, pēc kura filtrēt.

    ![Dokumenta veida atlasīšana, kuram skatīt iesniegšanas žurnālus](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Vērtība, kas tiek rādīta kolonnā **Iesniegšanas statuss**, kolonna attēlo statusu, kas saistīts ar paša iesniegšanas procesa pabeigšanu. Tas norāda, vai darbību plūsma, kas konfigurēta RCS, tika palaista līdz beigām, neatkarīgi no tā, vai elektroniskais dokuments tika apstiprināts vai noraidīts. Vērtība kolonnā **Iesniegšanas statuss**, nenorāda iesniegtā dokumenta statusu. Varat skatīt iesniegtā dokumenta statusu (tas ir, vai dokuments tika apstiprināts vai noraidīts) kopsavilkuma cilnē **Apstrādes darbību žurnāls**, kā aprakstīts tālāk.

3. Darbību rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**.
4. Iesniegšanas žurnāla informācijas skatīšana.

    ![Informācija par iesniegšanas žurnālu](media/e-invoicing-services-get-started-view-submission-log-form.png)

Rezultāti, kas tiek parādīti iesniegšanas žurnālā, ir atkarīgi no tā, kā e-rēķinu izrakstīšanas līdzeklis tika iestatīts RCS. Tomēr, neņemot vērā iestatījumu, iesniegšanas žurnālam vienmēr ir trīs kopsavilkuma cilnes:

- **Apstrādes darbības** – Šī kopsavilkuma cilne rāda izpildes žurnālu darbības, kas konfigurētas līdzekļa versijā, kas tika iestatīta RCS. Kolonna **Statuss** rāda, vai darbība ir veiksmīgi izpildīta.
- **Darbības faili** – Šī kopsavilkuma cilne rāda starpposma failus, kas tika ģenerēti darbību izpildes laikā. Varat atlasīt **Skatīt** lai lejupielādētu failu un skatītu tā saturu.
- **Apstrādes darbību žurnāls** – Šajā kopsavilkuma cilnē tiek rādīti saziņas rezultāti starp elektronisko rēķinu izrakstīšanas pievienojumprogrammu un mērķa tīmekļa pakalpojumu. Tas parāda arī to, ko atgrieza tīmekļa pakalpojuma apstrāde.

## <a name="related-topics"></a>Saistītās tēmas

- [Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-service-overview.md)
- [Sākt ar elektronisko rēķinu pievienojumu Brazīlijai](e-invoicing-bra-get-started.md)
- [Sākt ar elektronisko rēķinu pievienojumu Meksikai](e-invoicing-mex-get-started.md)
- [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai](e-invoicing-ita-get-started.md)
- [Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana](e-invoicing-setup.md)
