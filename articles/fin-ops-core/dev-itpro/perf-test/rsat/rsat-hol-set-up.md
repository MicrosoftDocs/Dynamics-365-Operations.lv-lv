---
title: Regression Suite Automation Tool apmācības iestatīšana un instalēšana
description: Šajā tēmā ir ietverta apmācība, kurā parādīts, kā iestatīt un instalēt Regression Suite Automation Tool (RSAT).
author: tonyafehr
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5dcdd14f54b9c0ad39794ff98ede29332c246513
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781995"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool apmācības iestatīšana un instalēšana

Šajā tēmā ietvertā apmācība palīdzēs iestatīt RSAT un ar RSAT lietošanu saistītos rīkus un sākt darbu ar tiem.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā.

## <a name="key-concepts"></a>Galvenie principi

- Uzziniet par instalēšanu un priekšnosacījumu iestatīšanu, kas nepieciešama dažādajām programmām, lai atbalstītu Regression Suite Automation Tool (RSAT).
- Izprotiet, kā uzdevumu ierakstītāja līdzeklis kopā ar pakalpojumu Microsoft Dynamics Lifecycle Services (LCS) un Microsoft Azure DevOps ļauj izveidot, konfigurēt, palaist un izmeklēt testa gadījumus un sniegt pārskatus par tiem.
- Sniedziet funkcionālajiem lietotājiem iespēju reģistrēt biznesa uzdevumus, izmantojot uzdevumu ierakstītāju, un pēc tam pārveidot uzdevumu ierakstus automātisku testu komplektā bez nepieciešamības rakstīt pirmkodu.

## <a name="before-you-begin"></a>Pirms sākšanas

### <a name="prerequisites"></a>Priekšnosacījumi

- Šai apmācībai ir nepieciešama vide, kurā darbojas Microsoft Dynamics 365 for Finance and Operations versija 10.0 (2019. gada aprīlis) vai jaunāka tās versija. Klientiem, kuri izmanto Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3, tiek nodrošināts arī Platform update 20 (PU20) vai jaunākas versijas atbalsts.
- Lietotājam ir nepieciešamas administratora tiesības vidē.
- Jums ir nepieciešama piekļuve klienta nomnieka LCS un Azure DevOps (iepriekš zināms kā Microsoft Visual Studio Team Services \[ VSTS\]).
- Lietotājam, kas veido un pārvalda testu komplektus, ir nepieciešama Azure DevOps testēšanas plānu vai testu pārvaldnieka licence. Piekļuvi testēšanas plāniem nodrošina arī šādas licence:
    - Visual Studio Enterprise licence;
    - Visual Studio Test Professional licence;
    - MSDN Platforms abonenta licence.
- RSAT ir nepieciešama piekļuve testa videi, izmantojot tīmekļa pārlūku.
- Lai ģenerētu un rediģētu testa parametrus, ir jābūt instalētai programmai Microsoft Excel.

## <a name="configure-azure-devops"></a>Konfigurēt Azure DevOps

### <a name="user-eligibility"></a>Lietotāju atbilstība

Pārliecinieties, ka lietotājs ir izveidots pakalpojumā Azure DevOps un ka tam ir abonementa līmenis, kas nodrošina piekļuvi Azure testēšanas plāniem. Azure DevOps testēšanas plānu licence ir nepieciešama tikai tad, ja lietotājs izveidos un pārvaldīs testa gadījumus (t. i., ne visiem RSAT lietotājiem ir nepieciešama šī licence). Informāciju par licenču prasībām skatiet sadaļā [Licenču prasības](/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Jauna Azure DevOps projekta izveide

RSAT izmanto Azure Devops testa gadījumu un testu komplektu pārvaldībai, pārskatu veidošanai un testu un rezultātu izmeklēšanai.

> [!NOTE]
> Varat izmantot esošu Azure DevOps projektu. Tomēr, ja esošais Azure DevOps projekts ir iestatīts tā, ka tam ir pielāgota veidne, tad, sinhronizējot testa gadījumus no biznesa procesu modelētāja (BPM) ar Azure DevOps (skatiet sadaļu [Testu sinhronizēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) ), tiks parādīts kļūdas ziņojums “VSTS sinhronizēšanas kļūme”. Ja pielāgotajā veidnē tiek ievērota tālāk norādītā paraugprakse, ir iespējams sinhronizēt pārbaudes gadījumus ar Azure DevOps. (Šie paraugprakses ieteikumi ir uzskaitīti kļūdas ziņojumā.)

- Neizdzēsiet nevienu darba krājuma veidu vai iebūvētos laukus.
- Neizdzēsiet nevienu darba krājuma stāvokļa veidu.
- Nepievienojiet nevienu obligāto lauku darba krājuma veidam.

![Kļūdas ziņojums ar paraugprakses ieteikumu sarakstu.](./media/setup_rsa_tool_02.png)

Pretējā gadījumā šīs apmācības nolūkos ieteicams izveidot jaunu Azure DevOps projektu. Papildinformāciju skatiet sadaļā [Problēmas saistībā ar sinhronizāciju uz BPM, izmantojot pielāgotu Azure DevOps (VSTS) procesu veidni](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Atveriet Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).
2. Azure DevOps lapas augšējā labajā stūrī atlasiet pogu **Izveidot projektu**.

    ![Poga Izveidot projektu.](./media/setup_rsa_tool_03.png)

3. Aizpildiet tālāk norādītos laukus un pēc tam atlasiet **Izveidot**.

    - **Projekta nosaukums**
    - **Versiju kontrole**— atlasiet **Team Foundation versijas kontrole**. Ņemiet vērā, ka noklusētā opcija **Git** netiek atbalstīta.
    - **Darba vienuma process**

    ![Dialoglodziņš Izveidot jaunu projektu.](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Personiskās piekļuves pilnvaras izveide

Šajā apmācībā jūs izmantosiet LCS biznesa procesu modelētāju (BPM), lai izveidotu testa gadījumu bibliotēku un sinhronizētu jūsu testa gadījumus ar Azure DevOps. Jums būs nepieciešama personiskās piekļuves pilnvara, lai sinhronizētu BPM ar Azure DevOps.

1. Atlasiet profila ikonu Azure DevOps projekta lapas augšējā labajā stūrī un pēc tam atlasiet **Drošība**.

    ![Drošības komanda.](./media/setup_rsa_tool_05.png)

2. Kreisajā rūtī sadaļā **Drošība** atlasiet **Personiskās piekļuves pilnvaras**. Pēc tam atlasiet **Jauna pilnvara**.

    ![Poga Jauna pilnvara sadaļas Lietotāja iestatījumi cilnē Personiskās piekļuves pilnvaras.](./media/setup_rsa_tool_06.png)

3. Aizpildiet tālāk norādītos laukus un pēc tam atlasiet **Izveidot**.

    - **Nosaukums/vārds, uzvārds**
    - **Termiņa beigas (UTC)**— atlasiet **Pielāgots** un pēc tam izmantojiet datuma atlasītāju, lai atlasītu pēdējo pieejamo datumu.
    - **Tvērumi**— atlasiet opciju **Pilna piekļuve**.

    ![Dialoglodziņš Izveidot jaunu personiskās piekļuves pilnvaru.](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Pierakstiet izveidoto personiskās piekļuves pilnvaru. Tā jums būs nepieciešama vēlāk, iestatot RSAT konfigurāciju.

    ![Personiskās piekļuves pilnvara.](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS projekta konfigurēšana

Jūsu galvenajai testu bibliotēkai ir nepieciešams Lifecycle Services (LCS) projekts. LCS biznesa procesu modelētājs (BPM) tiek izmantots kā galvenā jūsu testa gadījumu bibliotēka. BPM tiek izmantots, lai pārvaldītu un izplatītu testa bibliotēkas vairākos LCS projektos. Piemēram, Microsoft partneris vai neatkarīgs programmatūras piegādātājs, kas veido testa bibliotēkas, izlaiž testa gadījumus BPM bibliotēku formā. BPM testa gadījumi tiek organizēti pēc biznesa procesa. BPM nedefinē izpildes secību vai testu izpildes biežumu. Šīs detaļas tiek pārvaldītas pakalpojumā Azure DevOps, kā aprakstīts šajā tēmā.  

Savam LCS projektam varat izmantot esošu debitoru ieviešanu vai partnera projektu.

### <a name="update-the-lcs-language"></a>LCS valodas atjaunināšana

> [!NOTE]
> Lai lietotāja interfeiss (UI) pareizi rādītu biznesa procesus, kā vēlamā LCS valoda ir jāiestata **Angļu (ASV)**.

1. Atveriet LCS ieviešanas projektu.
2. Atlasiet pogu **Iestatījumi** (zobrata simbols) labajā augšējā stūrī un pēc tam atlasiet **Valodas preference**.

    ![Atjaunināt valodas preferenci.](./media/setup_rsa_tool_09.png)

3. Laukā **Vēlamā valoda** atlasiet **Angļu (ASV)** un pēc tam atlasiet **Saglabāt**.

    ![Cilne Valodas preference sadaļā Lietotāja iestatījumi.](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS konfigurēšana savienošanai ar Azure DevOps projektu

Ja iepriekš izveidojāt jaunu Azure DevOps projektu, konfigurējiet LCS projektu, lai izveidotu savienojumu ar to. Ja LCS projekts jau ir savienots ar Azure DevOps projektu, varat pāriet uz nākamo sadaļu.

1. Atveriet LCS ieviešanas projektu.
2. Atlasiet pogu **Izvēlne** un pēc tam atlasiet **Projekta iestatījumi**.

    ![Komanda Projekta iestatījumi.](./media/setup_rsa_tool_11.png)

3. Kreisajā rūtī atlasiet **Visual Studio Team Services** un pēc tam atlasiet **Iestatīt Visual Studio Team Services**.

    ![Visual Studio Team Services cilne projekta iestatījumos.](./media/setup_rsa_tool_12.png)

4. Laukā **Azure DevOps vietnes URL** ievadiet Azure DevOps vietnes URL. Laukā **Personiskās piekļuves pilnvara** ievadiet iepriekš izveidoto personiskās piekļuves pilnvaru.

    > [!NOTE]
    > Lai gan VSTS tagad ir zināms kā Azure DevOps, LCS savienošanai ar Azure DevOps projektu izmantojiet iepriekšējo URL. Piemēram, šajā apmācībā izmantotais Azure DevOps URL ir `https://dev.azure.com/D365FOFastTrack/`. Tomēr tālāk redzamajā attēlā tas ir ievadīts kā `https://D365FOFastTrack.visualstudio.com/`.

    ![1. darbība Visual Studio Team Services iestatīšanā.](./media/setup_rsa_tool_13.png)

5. Atlasiet **Turpināt**.
6. Laukā **Visual Studio Team Services projekts** atlasiet VSTS projektu atlasītajā vietnē, lai saistītu ar LCS projektu. Lauka **Procesa veidne** noklusējuma iestatījums ir **Dinamisks**. Pielāgotai veidnei pārskatiet labākās prakses ieteikumus sadaļā [Jauna Azure DevOps projekta izveide](#create-a-new-azure-devops-project). Pēc tam atlasiet **Turpināt**.

    ![2. darbība Visual Studio Team Services iestatīšanā.](./media/setup_rsa_tool_14.png)

7. Pārskatiet iestatījumus un pēc tam atlasiet **Saglabāt**.

    ![3. darbība Visual Studio Team Services iestatīšanā.](./media/setup_rsa_tool_15.png)

8. Atlasiet **Autorizēt**, lai autorizētu LCS piekļuvi konfigurētajai Azure DevOps vietnei jūsu vārdā un aktivizētu līdzekļus, kas integrējas ar VSTS.

    ![Poga Autorizēt.](./media/setup_rsa_tool_16.png)

9. Tiek parādīts ziņojuma lodziņš ar tekstu “Jūs tiksit novirzīts uz ārēju vietni, lai autorizētu pakalpojumus LCS, lai tie jūsu vārdā varētu izveidot savienojumu ar Visual Studio Team Services. Vai turpināt?”. Atlasiet **Jā**.

    ![Ziņojuma lodziņš.](./media/setup_rsa_tool_17.png)

10. Atlasiet **Pieņemt**.

    ![Piekļuves autorizēšana.](./media/setup_rsa_tool_18.png)

11. Ja esat autorizēts kā lietotājs, UI atkal atver LCS projekta iestatījumu lapu.

    ![Autorizēts lietotājs.](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Jaunas BPM bibliotēkas izveide

1. Atveriet LCS ieviešanas projektu.
2. Atlasiet pogu **Izvēlne** un pēc tam atlasiet **Biznesa procesu modelētājs**.

    ![Biznesa procesu modelētāja komanda.](./media/setup_rsa_tool_20.png)

3. Atlasiet **Jauna bibliotēka**.

    ![Poga Jauna bibliotēka.](./media/setup_rsa_tool_21.png)

4. Laukā **Bibliotēkas nosaukums** ievadiet nosaukumu un pēc tam atlasiet **Izveidot**. Šajā apmācībā piešķiriet BPM bibliotēkai nosaukumu **RSAT**.

    ![Dialoglodziņš Izveidot jaunu bibliotēku.](./media/setup_rsa_tool_22.png)

5. Atveriet jauno BPM bibliotēku **RSAT**.
6. Atlasiet procesu **Galvenā biznesa procesa paraugs** un pēc tam labajā pusē atlasiet **Rediģēšanas režīms**.

    ![Poga Rediģēšanas režīms.](./media/setup_rsa_tool_23.png)

7. Nomainiet lauka **Nosaukums** un lauka **Apraksts** vērtību uz **Preces izveide**. Pēc tam atlasiet **Saglabāt**.

    ![Lauki Nosaukums un Apraksts.](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Vide

### <a name="version-requirement"></a>Versijas prasība

Ir nepieciešama testa vai smilškastes vide, kurā darbojas versija 10. Klientiem, kuri izmanto versiju 7.3, tiek nodrošināts arī Platform update 20 vai jaunākas versijas atbalsts.

> [!NOTE]
> RSAT ir nepieciešama piekļuve jūsu testa videi, izmantojot tīmekļa pārlūku.

### <a name="user-criteria"></a>Lietotāju kritēriji

Lietotājam ir nepieciešamas administratora tiesības šajā vidē.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Palīdzības iestatījumu iestatīšana savienojuma izveidei ar LCS

Šī darbība ir nepieciešama savienojuma izveidei ar LCS, lai uzdevumu ierakstus varētu saglabāt atbilstošajā BPM bibliotēkā pakalpojumā LCS, izmantojot klientu.

1. Atveriet klientu.
2. Dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Sistēmas parametri**.
3. Cilnes **Palīdzība** laukā **Lifecycle Services palīdzības konfigurācija** atlasiet attiecīgo LCS projektu (**RSAT** šajā apmācībā).

    ![Lauks Lifecycle Services palīdzības konfigurācija cilnē Palīdzība.](./media/setup_rsa_tool_25.png)

    BPM bibliotēkas tiek aizpildītas saskaņā ar atbilstošo LCS projektu.

4. Atlasiet **Saglabāt**.
5. Iespējams, būs nepieciešams atsvaidzināt pārlūku, lai redzētu atjaunināto palīdzības saturu.

    ![Paziņojums par pārlūka atsvaidzināšanu.](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Uzdevumu ieraksti

> [!NOTE]
> Pārliecinieties, ka visi uzdevumu ieraksti tiek sākti galvenajā informācijas panelī. Raugieties, lai atsevišķi ieraksti būtu īsi, un koncentrējieties uz vienu biznesa uzdevumu, piemēram, pārdošanas pasūtījuma izveidi.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā

Izveidojiet atbilstošu uzdevuma ierakstu, ko varat pievienot vienkāršajam biznesa procesam, kas tika izveidots jaunajā BPM bibliotēkā.

1. Atveriet klientu.
2. Galvenajā informācijas panelī atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Uzdevuma reģistrētājs**.

    ![Atlasīt Uzdevumu ierakstītāju izvēlnē Iestatījumi.](./media/setup_rsa_tool_27.png)

3. Atlasiet **Izveidot ierakstu**.

    ![Poga Izveidot ierakstu.](./media/setup_rsa_tool_28.png)

4. Aizpildiet laukus **Ieraksta nosaukums** un **Ieraksta apraksts** un pēc tam atlasiet **Sākt**.

    ![Lauki Ieraksta nosaukums un ieraksta apraksts.](./media/setup_rsa_tool_29.png)

5. Reģistrējiet preces izveides darbības. Kad ieraksts ir pabeigts, atlasiet **Apturēt**, lai apturētu ierakstīšanu.

    ![Preces izveides darbības.](./media/setup_rsa_tool_30.png)

6. Atlasiet **Saglabāt pakalpojumos Lifecycle Services**.

    ![Saglabāt Uzdevuma ierakstu pakalpojumos Lifecycle Services.](./media/setup_rsa_tool_31.png)

    Bibliotēkas informācija tiek ielādēta no LCS.

    ![Notiek bibliotēkas informācijas ielāde.](./media/setup_rsa_tool_32.png)

7. Atlasiet BPM bibliotēku, kuru saistīt ar uzdevuma ierakstu. Šajā apmācībā atlasiet BPM bibliotēku **RSAT**, kas tika izveidota iepriekš, un biznesa procesu **Preces izveide** zem tās. Tad atl. **Labi**.

    ![Uzdevuma ieraksta saistīšana ar BPM bibliotēku un biznesa procesu.](./media/setup_rsa_tool_33.png)

    Tiek parādīts ziņojums “Saglabāšana pakalpojumā Lifecycle Services bija sekmīga”.

    ![Ziņojums par sekmīgu saglabāšanu LCS.](./media/setup_rsa_tool_34.png)

8. Ja vēlaties saglabāt uzdevuma ierakstu lokāli un pēc tam augšupielādēt to BPM, izmantojot LCS, izpildiet tālāk norādītās darbības.

    1. Kad ieraksts ir pabeigts, atlasiet **Saglabāt šajā datorā**.

        ![Saglabāt šajā datorā.](./media/setup_rsa_tool_35.png)

    2. Pārlūka paziņojumu joslā atlasiet **Saglabāt** vai **Saglabāt kā**, lai saglabātu failu lokālajā datorā.

        ![Paziņojumu josla.](./media/setup_rsa_tool_36.png)

    3. Dodieties uz BPM bibliotēku **RSAT** un atlasiet biznesa procesu, kura uzdevuma ierakstu saglabāt.
    4. Cilnē **Pārskats** atlasiet **Augšupielādēt**.

        ![Poga Augšupielādēt.](./media/setup_rsa_tool_37.png)

    5. Atlasiet **Pārlūkot** un atlasiet .axtr failu, kuru saglabājāt iepriekš. Atlasiet **Augšupielādēt**.

        ![Augšupielādējamā faila .axtr atlase.](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Sinhronizācijas testēšana no BPM ar Azure DevOps

Tagad, kad uzdevuma ieraksts ir pievienots biznesa procesam, ir jāpārbauda, vai biznesa procesu un saistīto uzdevuma ierakstu var sinhronizēt ar Azure DevOps kā līdzekli un testa gadījumu (attiecīgi), izmantojot VSTS sinhronizācijas līdzekli pakalpojumā LCS.

> [!NOTE]
> Atbilstošais darba vienuma veids, kas izveidots pakalpojumā Azure DevOps, mainās atkarībā no procesa veidnes, kuru atlasījāt, kad konfigurējāt LCS projektu ar Azure DevOps, kā aprakstīts sadaļā [Jauna Azure DevOps projekta izveide](#create-a-new-azure-devops-project).

1. Dodieties uz BPM bibliotēku un atveriet bibliotēku **RSAT**, ko izveidojāt iepriekš.
2. Atlasiet daudzpunktes pogu (**...**) un atlasiet **VSTS sinhronizācija**.

    ![Komanda VSTS sinhronizācija daudzpunktes izvēlnē.](./media/setup_rsa_tool_39.png)

    Kad VSTS sinhronizācija ir pabeigta, kreisajā pusē parādās cilne **Prasības**, kurā ietverts atbilstošais Azure DevOps darbplūsmas vienums.

    > [!NOTE]
    > Darba vienumam, kas tiek izveidots pakalpojumā Azure DevOps, kā prefikss tiek piešķirts BPM bibliotēkas nosaukums.

    ![Cilne Prasības.](./media/setup_rsa_tool_40.png)

3. Atsvaidziniet lapu.
4. Atlasiet daudzpunktes pogu (**...**). Tiek parādīta papildu opcija **Sinhronizēt testa gadījumus**. Atlasiet šo opciju.

    ![Komanda Sinhronizēt testa gadījumus daudzpunktes izvēlnē.](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Ja opcija **Sinhronizēt testa gadījumus** nav pieejama pēc lapas atsvaidzināšanas, dodieties uz BPM galveno lapu un atlasiet **Sinhronizēt testa gadījumus** visai bibliotēkai. Šādā veidā varat efektīvi iespējot visas bibliotēkas piespiedu sinhronizāciju.
    >
    > ![Opcijas Sinhronizēt testa gadījumus atlasīšana visai bibliotēkai.](./media/setup_rsa_tool_42.png)

    Kad komanda Sinhronizēt testa gadījumus ir pabeigta, cilnē **Prasības** tiek izveidots jauns testa gadījums.

    ![Jauns testa gadījums cilnē Prasības.](./media/setup_rsa_tool_43.png)

5. Dodieties uz Azure DevOps projektu un atlasiet **Paneļi \> Darba vienumi**.

    ![Komanda Darba vienumi sadaļā Paneļi.](./media/setup_rsa_tool_44.png)

6. Pārbaudiet, vai pastāv darba vienums un testa gadījums, ko izveidojāt, izmantojot BPM sinhronizāciju.

    ![Darba vienums un testa gadījums.](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT instalēšana un konfigurēšana

RSAT var instalēt jebkurā datorā, kurā darbojas Windows 10 un ko var savienot ar vidi, izmantojot tīmekļa pārlūku (Internet Explorer vai Google Chrome).

> [!NOTE]
> Pirms rīka jaunās versijas instalēšanas ieteicams atinstalēt iepriekšējo versiju.

### <a name="install-an-authentication-certificate"></a>Autentifikācijas sertifikāta instalēšana

Lai iespējotu autentifikāciju, sertifikāts ir jāģenerē un jāinstalē tajā pašā datorā, kurā darbojas RSAT.

#### <a name="generate-a-certificate"></a>Sertifikāta ģenerēšana

1. Lai ģenerētu sertifikāta failu, atveriet Microsoft Windows PowerShell logu kā administrators un izpildiet tālāk norādīto komandu.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Atveriet sertifikātu pārvaldnieku, ievadot **certlm.msc** dialoglodziņā **Palaist**, un pārliecinieties, ka sertifikāts **D365 automātiskās testēšanas sertifikāts** mapē **Personiski \> Sertifikāti** ir izveidots.

    > [!NOTE]
    > Pārliecinieties, ka ievadāt **certlm.msc**, nevis **certmgr.msc**, jo sertifikāti tiek glabāti lokālajā datorā.

    ![Sertifikāts D365 automatizētās testēšanas sertifikāts.](./media/setup_rsa_tool_46.png)

3. Ar peles labo pogu noklikšķiniet uz sertifikāta un pēc tam atlasiet **Kopēt**.
4. Dodieties uz **Uzticamās saknes sertifikātu iestādes \> Sertifikāti**.

    ![Mape Sertifikāti mapē Uzticamās saknes sertifikātu iestādes.](./media/setup_rsa_tool_47.png)

5. Izvēlnē **Darbība** atlasiet **Ielīmēt**, lai iekopētu sertifikātu atrašanās vietā **Uzticamās saknes sertifikātu iestādes**.

    ![Komanda Ielīmēt izvēlnē Darbība.](./media/setup_rsa_tool_48.png)

6. Lai iegūtu instalētā sertifikāta nospiedumu bez atstarpēm vai speciālajām rakstzīmēm, atveriet Windows PowerShell logu kā administrators un palaidiet tālāk norādītās komandas.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Saglabājiet nospiedumu, jo tas būs nepieciešams vēlāk, atjauninot lietojumprogrammas objektu servera (AOS) failus .wif un iestatot RSAT konfigurāciju.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>AOS datora konfigurēšana uzticama savienojuma izveidei

> [!NOTE]
> Ja vide ir 2+ pakāpes vide, sertifikāta nospiedums ir jāatjaunina failā wif.config **visiem** vides AOS datoriem.

1. Izveidojiet attālās darbvirsmas protokola (RDP) savienojumu ar AOS datoru. Pierakstīšanās informācija ir pieejama LCS vides informācijas lapā.
2. Atveriet Microsoft interneta informācijas pakalpojumus (IIS) un vietņu sarakstā meklējiet **AOSService**.

    ![AOSService vietņu sarakstā.](./media/setup_rsa_tool_49.png)

3. Ar peles labo pogu noklikšķiniet uz **Pārlūkot**, lai atvērtu mapi **\<Drive\>: \\ AosService\\ WebRoot**. Atrodiet failu **wif.config**.

    ![Fails wif.config mapē WebRoot.](./media/setup_rsa_tool_50.png)

4. Atjauniniet failu **wif.config**, sertifikātu un iestādes nosaukumam pievienojot jaunu iestādes ierakstu, kā norādīts tālāk redzamajā piemērā.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Ja vairāki lietotāji izmanto vienu un to pašu programmu, katram lietotājam ir jāizveido atsevišķi nospiedumi, un katrs no šiem nospiedumiem ir jāpievieno sadaļā **\<keys\>**.

5. Ja ir vairāk nekā viens AOS dators, atkārtojiet 3.–4. darbību katram papildu datoram.

    > [!NOTE]
    > Atšķirībā no vecākām 2. pakāpes vidēm jaunās 2. pakāpes vides tiek izvietotas ar divām AOS instancēm.

6. Palaidiet **iisreset** visos AOS datoros.

    > [!NOTE]
    > Ja jums nav administratora tiesību **iisreset** palaišanai 1. pakāpes datorā, LCS lapā Informācija par vidi atlasiet Uzturēt > Restartēt pakalpojumus.

#### <a name="tier-2-environment"></a>2+ pakāpes vide

Ja tiek izmantota 2+ pakāpes (standarta pieņemšanas testu smilškaste vai jaunāka versija) vide, pārbaudiet vai iestatiet tālāk norādīto reģistra iestatījumu datorā, kurā ir instalēts RSAT. Šī darbība ir nepieciešama, jo tā palīdz izvairīties no autentifikācijas vai RSAT savienojuma kļūdām.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT instalēšana

1. Dodieties uz <https://www.microsoft.com/download/details.aspx?id=57357> un atlasiet **Lejupielādēt**.
2. Atlasiet visus failus un pēc tam atlasiet **Tālāk**.

    ![Visu failu atlasīšana.](./media/setup_rsa_tool_51.png)

3. Veiciet dubultklikšķi uz .msi pakotnes, lai palaistu instalēšanas programmu. Pēc tam, kad instalēšana ir pabeigta, atlasiet **Pabeigt**.

    ![RSAT instalēšanas programmas fails.](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Selenium un pārlūka draiveru instalēšana

Vecākās RSAT versijās bija nepieciešams instalēt Selenium un pārlūka draiverus. Tagad šie draiveri vairs nav jāinstalē, jo tie ir instalēti automātiski.

1. Pirmo reizi atverot RSAT, tiek parādīta uzvedne ar aicinājumu automātiski lejupielādēt un instalēt Selenium. Papildinformāciju skatiet sadaļā [RSAT konfigurēšana](#configure-rsat).
2. Lai varētu palaist testa gadījumu, vispirms tiek parādīta uzvedne ar aicinājumu automātiski lejupielādēt un instalēt pārlūka draiveri, kas atbilst noklusējuma pārlūkam, kurš atlasīts RSAT konfigurācijā. Papildinformāciju skatiet sadaļā [Testa gadījumu ielādēšana un palaišana](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Darba sākšana ar RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Testēšanas plāna un testu komplektu izveide

1. Dodieties uz Azure DevOps projektu un atlasiet **Testēšanas plāni**.

    ![Testēšanas plānu komanda.](./media/setup_rsa_tool_53.png)

2. Atlasiet **Jauns testēšanas plāns**.

    ![Poga Jauns testēšanas plāns.](./media/setup_rsa_tool_54.png)

3. Aizpildiet lauku **Nosaukums** un pēc tam atlasiet **Izveidot**. Šajā apmācībā piešķiriet testēšanas plānam nosaukumu **RSAT testēšanas plāns**.

    ![Dialoglodziņš Jauns testēšanas plāns.](./media/setup_rsa_tool_55.png)

4. Atlasiet plus zīmi (**+**) un pēc tam atlasiet **Statisks komplekts**, lai izveidotu statisku komplektu atbilstoši jaunajam testēšanas plānam. Piešķiriet jaunajam testu komplektam nosaukumu **T01 – Veikt uz krājumiem**.

    > [!NOTE]
    > Varat arī izveidot uz vaicājumiem balstītu komplektu, ja vēlaties, lai jaunie testa gadījumi no BPM tiktu automātiski ievietoti RSAT testu komplektā.

    ![Statiska komplekta izveide.](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Testa gadījumu pievienošana testu komplektiem

1. Atlasiet **Pievienot esošu**, kas atrodas labajā pusē, lai pievienotu testu komplektam esošos testa gadījumus.

    ![Poga Pievienot esošu.](./media/setup_rsa_tool_57.png)

2. Lapā **Pievienot testa gadījumus komplektam** atlasiet **Izpildīt vaicājumu** un pēc tam atlasiet testa gadījumu, ko pievienot testu komplektam. Šajā apmācībā atlasiet testa gadījumu **Jaunas preces izveide**. Pēc tam atlasiet **Pievienot testa gadījumus** lapas labajā apakšējā stūrī (šī poga nākamajā attēlā nav parādīta).

    ![Poga Izpildīt vaicājumu.](./media/setup_rsa_tool_58.png)

    Testa gadījums ir pievienots testu komplektam **T01 – Veikt uz krājumiem**.

    ![Testu komplektam pievienots testa gadījums.](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfigurēt RSAT

1. Atveriet RSAT.

    ![RSAT ikona.](./media/setup_rsa_tool_60.png)

2. Tiek parādīts brīdinājuma ziņojums ar tekstu “Rīkam Regression Suite Automation Tool ir nepieciešama platforma Selenium; vai vēlaties tūlīt automātiski lejupielādēt un instalēt to?”. Atlasiet **Jā**.

    ![Brīdinājuma ziņojums, ka Regression Suite Automation Tool pieprasa platformu Selenium.](./media/setup_rsa_tool_61.png)

3. Atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī un pēc tam atvērtajā dialoglodziņā aizpildiet tālāk norādītos laukus.

    - **Azure DevOps URL**— ievadiet jūsu Azure DevOps projekta URL, piemēram, `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Piekļuves pilnvara**— ievadiet piekļuves pilnvaru, kas ļauj izveidot savienojumu ar Azure DevOps. Izmantojiet personiskās piekļuves pilnvaru, ko izveidojāt iepriekš šajā pamācībā. Papildinformāciju skatiet sadaļā [Piekļuves autentificēšana ar personiskās piekļuves tiesībām](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projekta nosaukums**— atlasiet Azure DevOps projekta nosaukumu.
    - **Testēšanas plāns**— atlasiet Azure DevOps testēšanas plānu, kas satur jūsu testa gadījumus. Papildinformāciju skatiet sadaļā [Testēšanas plānu un testu komplektu izveide](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Pēc testa plāna atlasīšanas atlasiet **Testēt savienojumu**, lai testētu savienojumu ar Azure DevOps.
    - **Resursdatora nosaukums** — ievadiet testa vides resursdatora nosaukumu, piemēram, **\<myaos\> myaos.cloudax.dynamics.com**. Neiekļaujiet prefiksu **https://** vai **http://**.
    - **SOAP resursdatora nosaukums**— ievadiet testa vides SOAP resursdatora nosaukumu. Parasti SOAP resursdatora nosaukums ir tāds pats kā resursdatora nosaukums, bet tam ir sufikss **soap**. Šeit ir piemērs: **\<myaos\> soap.cloudax.dynamics.com**. Neiekļaujiet prefiksu **https://** vai **http://**.

        > [!NOTE]
        > Lai atrastu resursdatora nosaukumu un SOAP resursdatora nosaukumu, atveriet IIS pārvaldnieku, ar peles labo pogu noklikšķiniet uz **Vietnes \> AOSService** un pēc tam atlasiet **Rediģēt saistījumus**. Vērtības kolonnā **Resursdatora nosaukums** norāda resursdatora nosaukumu un SOAP resursdatora nosaukumu (SOAP resursdatora nosaukuma URL satur sufiksu **soap**).

        ![Resursdatora nosaukums un SOAP resursdatora nosaukums kolonnā Resursdatora nosaukums.](./media/setup_rsa_tool_63.png)

    - **Administratora lietotājvārds**— ievadiet administratora lietotāja e-pasta adresi testa vidē.
    - **Īssavilkums**— ievadiet autentifikācijas sertifikāta nospiedumu, kā aprakstīts iepriekš šajā pamācībā.
    - **Darba direktorijs**— norādiet mapes atrašanās vietu, kur saglabāt testu automatizācijas failus, piemēram, Excel testu datu failus. Piemēram, ievadiet vai atlasiet **C:\\ Temp\\ RegressionTool**.

        > [!NOTE]
        > Ja mapes nosaukumā ir atstarpes, izpilde neizdodas, jo mapi nevar atrast. Šī problēma ir zināma, un jaunākajā rīka versijā tai jābūt labotai.

    - **Noklusējuma pārlūks**— atlasiet **Internet Explorer** vai **Google Chrome**. Pārliecinieties, ka ir instalēti atbilstošie pārlūka draiveri.
    - **Testa izpildes taimauts**— norādiet testa izpilžu taimauta periodu minūtēs. Kad taimauta periods ir beidzies, visi aktīvie logi tiek aizvērti, un gaidoši testa gadījumi ir nesekmīgi.
    - **Testa darbības taimauts**— šis lauks kontrolē Finance and Operation vides servera pieprasījumu taimauta periodu minūtēs. Parasti noklusējuma vērtība (2 minūtes) ir pietiekama. Tomēr lēnākās vidēs šo vērtību var būt nepieciešams palielināt, ja rodas ar taimautu saistītas problēmas.
    - **Uzņēmuma nosaukums**— ievadiet tā uzņēmuma nosaukumu, ko izmantot kā noklusējuma uzņēmumu, kad tiek izveidoti Excel parametru faili. Vēlāk varat nomainīt uzņēmumu, rediģējot Excel parametru failu.

    ![Dialoglodziņš Iestatījumi.](./media/setup_rsa_tool_62.png)

4. Atlasiet **Lietot**, lai lietotu un saglabātu iestatījumus.

    Lai pašreizējos iestatījumus saglabātu konfigurācijas failā datorā, atlasiet **Saglabāt kā**. Lai pašreizējos iestatījumus atjaunotu no konfigurācijas faila datorā, atlasiet **Atvērt**.

5. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.

### <a name="load-and-run-test-cases"></a>Testa gadījumu ielāde un izpilde

1. Atlasiet **Ielādēt**, lai ielādētu testēšanas plānu **RSAT testēšanas plāns** no Azure DevOps projekta.

    ![Poga Ielādēt.](./media/setup_rsa_tool_64.png)

2. Testu komplektā atlasiet testa gadījumu **Jaunas preces izveide** un pēc tam atlasiet **Jauns \> Ģenerēt testa izpildes un parametru failus**.

    ![Komanda Ģenerēt testa izpildes un parametru failus izvēlnē Jauns.](./media/setup_rsa_tool_65.png)

    Excel parametru fails tiek izveidots lokālajā mapē, kas norādīta RSAT konfigurācijā (piemēram, **C:\\ Temp\\ RegressionTool**).

    ![Excel parametru faila izveide.](./media/setup_rsa_tool_66.png)

3. Ja vēlaties saglabāt parametru failus, atlasiet **Augšupielādēt**. Visu atlasīto testa gadījumu testu automatizācijas faili tiek augšupielādēti pakalpojumā Azure DevOps turpmākai izmantošanai. (Šie faili ietver Excel testa parametru failus.)

    Šādā veidā varat atlasīt **Ielādēt**, lai ielādētu testa gadījuma parametru failus (un automatizācijas failus) tieši no Azure DevOps. Nav nepieciešams ģenerēt parametru failus atkārtoti. Šī pieeja kļūs svarīga vēlāk, ja vēlēsities saglabāt modifikācijas parametru failā un nevēlēsities tos pārrakstīt.

4. Lai pārbaudītu, vai automatizācijas faili un parametru faili tiek saglabāti Azure DevOps, dodieties uz Azure DevOps projektu, atlasiet **Paneļi \> Darba vienumi** un atlasiet testa gadījumu **Jaunas preces izveide**. Cilnē **Pielikumi** ir jābūt redzamiem četriem failiem:

    - **.cs**— C\# automatizācijas fails
    - **.dll**— kompilētais automatizācijas fails kā komplektācija
    - **.xlsx**— Excel parametru fails
    - **.xml**— ieraksta fails

    ![Faili cilnē Pielikumi.](./media/setup_rsa_tool_67.png)

5. Atlasiet testa gadījumu, ko izpildīt, un pēc tam atlasiet **Palaist**.

    > [!NOTE]
    > Ja kā pārlūku izmantojat Internet Explorer, pirms testa gadījumu izpildīšanas pārliecinieties, ka darbvirsmas izšķirtspēja ir iestatīta uz **100%** sadaļā **Windows displeja iestatījumi \> Mērogs un izkārtojums**. Ja nevarat mainīt šo iestatījumu virtuālajā mašīnā (VM), nomainiet to klientā (klēpjdatorā), no kura mēģināt piekļūt VM. Pēc tam VM displeja iestatījumi pārmanto izšķirtspējas iestatījumus.

    ![Darbvirsmas izšķirtspēja ir iestatīta uz 100%.](./media/setup_rsa_tool_68.png)

6. Ja pārlūka draiveri sistēmā nav instalēti, tiek parādīts brīdinājuma ziņojums ar tekstu “Šai operācijai ir nepieciešams \<browser name\> draiveris. Vai vēlaties tagad automātiski lejupielādēt un instalēt to?”. Atlasiet **Jā**.

    ![Brīdinājuma ziņojums pārlūkam Internet Explorer.](./media/setup_rsa_tool_69.png)

    ![Brīdinājuma ziņojums pārlūkam Chrome.](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Ja kā pārlūku izmantojat Chrome un saņemat kļūdas ziņojumu, kurā norādīts, ka sesija netika izveidota, jo Chrome versija nav pareiza, lejupielādējiet jaunāko Chrome draiveri no vietnes <http://chromedriver.chromium.org/downloads> mapē **C:\\ Program Files (x86)\\Regression Suite Automation Tool\\ Common\\ External\\ Selenium**.

    ![Kļūdas ziņojums pārlūkam Chrome.](./media/setup_rsa_tool_71.png)

    Testa gadījums tiek izpildīts, un lauks **Rezultāts** tiek atjaunināts.

    ![Lauks Atjauninātais rezultāts.](./media/setup_rsa_tool_72.png)

    Ja izpildījāt šo apmācību atbilstoši norādījumiem, testa gadījums **Jaunas preces izveide** būs nesekmīgs, jo preces izveides uzdevuma ieraksts saglabāja preces nosaukumu kā stingri kodētu vērtību. Izpildot šo testa gadījumu atkārtoti, tiek parādīts kļūdas ziņojums, jo prece jau pastāv.

    ![Lauks Rezultāts ir iestatīts kā Nesekmīgs.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Testa rezultātu skatīšana

1. Veiciet dubultklikšķi uz nesekmīgā testa gadījuma.

    Tiek parādīts kļūdas ziņojums.

    ![Kļūdas ziņojums.](./media/setup_rsa_tool_73.png)

2. Atlasiet **Detalizēti**, lai skatītu pilnu kļūdas ziņojumu.

    ![Pilns kļūdas ziņojums.](./media/setup_rsa_tool_74.png)

3. Lai skatītu detalizētu kļūdas ziņojuma versiju pakalpojumā Azure DevOps, atlasiet **Atvērt pakalpojumā Azure DevOps**. Pakalpojumā Azure DevOps var skatīt testa gadījuma statusu un detalizētu kļūdas ziņojumu.

    ![Detalizēts kļūdas ziņojums pakalpojumā Azure DevOps.](./media/setup_rsa_tool_75.png)

4. Lai skatītu testa rezultātus tieši Azure DevOps projektā, dodieties uz **Testēšanas plāni \> Testēšanas plāni \> Izpildes**. Veiciet dubultklikšķi uz testa izpildes, par kuru vēlaties skatīt detalizētu informāciju.

    ![Testa izpilžu saraksts pakalpojumā Azure DevOps.](./media/setup_rsa_tool_76.png)

5. Cilnē **Izpildes kopsavilkums** ir norādīts, ka testa gadījums ir nesekmīgs, bet nav sniegts faktiskais kļūdas ziņojums. Lai skatītu detalizētu kļūdas ziņojumu, atlasiet cilni **Testa rezultāti**.

    ![Cilne Izpildes kopsavilkums.](./media/setup_rsa_tool_77.png)

    Cilnē **Testa rezultāti** ir sniegta informācija par testa gadījumu, iznākums un kļūdas ziņojums.

    ![Cilne Testa rezultāti.](./media/setup_rsa_tool_78.png)

6. Veiciet dubultklikšķi uz atbilstošā ieraksta, lai skatītu detalizētu kļūdas ziņojumu.

    ![Detalizēts kļūdas ziņojums.](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Visi kļūdu ziņojumi ir pieejami arī lokāli direktorijā **C:\\ Users\\\$ YourUserName\\ AppData\\ Roaming\\ regressionTool\\ errormsg-.txt**.

7. Varat arī eksportēt testa izpildes rezultātus no testēšanas plāna līmeņa, atlasot **Eksportēt**.

    ![Testēšanas plāna eksportēšana.](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Excel parametru faila modificēšana

1. Atveriet RSAT.
2. Atlasiet testa gadījumu un pēc tam atlasiet **Rediģēt**, lai atvērtu Excel parametru failu.

    Lapā **EcoResProductCreate** ievērojiet, ka lauka **Preces numurs** vērtība ir stingri kodēta. Pirms atkārtotas testa gadījuma palaišanas preces numurs šajā laukā ir jāatjaunina uz jaunās preces numuru.

3. Lai ģenerētu unikālu preces numuru katrai izpildei bez vajadzības atkārtoti atvērt Excel parametru failu un manuāli atjaunināt preces numuru katru reizi, izmantojiet šādu Excel formulu.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Papildus cilnei **Vispārīgi** Excel parametru failā ir ietverta datu cilne katrai veidlapas lapai, kura tiek pārskatīta testa gadījuma izpildes laikā.

    ![Lauks Preces numurs.](./media/setup_rsa_tool_81.png)

4. Atlasiet **Saglabāt** un pēc tam aizveriet Excel darbgrāmatu.
5. Atlasiet **Augšupielādēt**, lai saglabātu Excel parametru failu pakalpojumā Azure DevOps.

    ![Ziņojums par sekmīgu augšupielādēšanu.](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Lai palaistu testa gadījumus noteikta lietotāja kontekstā, ievadiet lietotāja e-pasta ID Excel parametru faila laukā **Testēt lietotāju**, kas atrodas cilnē **Vispārīgi**. Jaunākajā RSAT versijā Excel parametru faila lauku izkārtojums ir atjaunināts, bet koncepcija paliek tāda pati.
    >
    > ![Lauks Testēt lietotāju.](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Rezultātu pārbaude

- Atlasiet **Palaist**, lai palaistu testa gadījumu, un pārbaudiet, vai testa gadījums ir sekmīgs. Varat skatīt testa rezultātus, kā aprakstīts sadaļā [Testa rezultātu skatīšana](#view-the-test-results).

    ![Lauks Rezultāts ir iestatīts kā Sekmīgs.](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Testa gadījumu ķēde

Viens no RSAT svarīgākajiem līdzekļiem ir testa gadījumu savienošana ķēdē (jeb iespēja nodot testa vērtības citiem testiem). Testa gadījumi tiek palaisti atbilstoši secībai, kas noteikta Azure DevOps testēšanas plānā. (Šo secību var atjaunināt pašā testēšanas rīkā.) Tādēļ, ja vēlaties pārnest mainīgos no viena testa gadījuma uz citu, ir ļoti svarīgi, lai testi būtu pareizā secībā.

Šajā sadaļā parādīts, kā izveidot saglabātu mainīgo pirmajā testa gadījumā, izveidot otru testa gadījumu un pārnest saglabāto mainīgo no pirmā testa gadījuma uz otro testa gadījumu. Pēc tam testa gadījumi tiek izpildīti kā testa gadījumu ķēde rīkā RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Esoša uzdevuma ieraksta modificēšana saglabāta mainīgā izveidei

1. Atveriet klientu.
2. Atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Uzdevuma reģistrētājs**.
3. Atlasiet **Rediģēt ierakstu**.

    ![Poga Rediģēt ierakstu.](./media/setup_rsa_tool_85.png)

4. Atlasiet **Atvērt no Lifecycle Services**.

    ![Poga Atvērt no Lifecycle Services.](./media/setup_rsa_tool_86.png)

5. Atlasiet **Atlasīt Lifecycle Services bibliotēku**.

    ![Poga Atlasīt Lifecycle Services bibliotēku.](./media/setup_rsa_tool_87.png)

    BPM bibliotēkas tiek ielādētas no LCS.

    ![BPM bibliotēku ielāde.](./media/setup_rsa_tool_88.png)

6. Pēc BPM bibliotēku ielādēšanas no LCS atlasiet BPM bibliotēku **RSAT** un biznesa procesu **Jaunas preces izveide**, ar kuru bija saistīts uzdevuma ieraksts. Pēc tam atlasiet **Labi**.

    ![BPM bibliotēkas un biznesa procesa atlase.](./media/setup_rsa_tool_89.png)

7. Atbilstošā uzdevuma ieraksta nosaukums tiek ievadīts laukā **Ieraksta nosaukums**. Atlasiet **Sākt**.

    ![Uzdevuma ieraksta nosaukums laukā Ieraksta nosaukums.](./media/setup_rsa_tool_90.png)

8. Dodieties uz **Preču informācijas pārvaldība \> Preces** un atlasiet **Jauns**, lai atvērtu lapu, kurā tika reģistrēts sākotnējais uzdevuma ieraksts **Preces izveide**.
9. Atlasiet **Ievietot darbību**.

    > [!NOTE]
    > Jaunā darbība tiek ievietota **pēc** darbības, kuru atlasījāt rūtī.

    ![Poga Ievietot darbību.](./media/setup_rsa_tool_91.png)

10. Ar peles labo pogu noklikšķiniet uz lauka **Preces numurs** un pēc tam atlasiet **Uzdevuma reģistrētājs \> Kopēt**.

    ![Komanda Kopēt.](./media/setup_rsa_tool_92.png)

11. Rūtī tiek pievienota jauna darbība. Pierakstiet laukā **Preces numurs** redzamo vērtību, jo tā būs nepieciešama vēlāk.

    ![Pievienota jauna darbība.](./media/setup_rsa_tool_93.png)

12. Atlasiet **Rediģēšana pabeigta**.
13. Atlasiet **Saglabāt pakalpojumos Lifecycle Services** un saistiet jauno uzdevuma ierakstu ar to pašu BPM bibliotēku un biznesa procesu, ar kuru tika saistīts sākotnējais uzdevuma ieraksts. Papildinformāciju skatiet sadaļā [Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Dodieties uz BPM bibliotēku un atlasiet **Sinhronizēt testa piemērus**, lai pārrakstītu uzdevuma ierakstu, kas ir pievienots testa gadījumam pakalpojumā Azure DevOps, kā aprakstīts sadaļā [Sinhronizācijas testēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).
15. Atveriet RSAT un atlasiet **Ielādēt**, lai atkārtoti ielādētu visus testa gadījumus testu komplektā. Ir nepieciešams atkārtoti ģenerēt atbilstošā testa gadījuma automatizācijas un parametru failus, atlasot testa gadījumu un pēc tam atlasot **Jauns \> Ģenerēt testa izpildes un parametru failus**, kā aprakstīts sadaļā [Testa gadījumu ielāde un izpilde](#load-and-run-test-cases).

    > [!NOTE]
    > Ja Excel parametru fails ir atstāts atvērts, atkārtota ģenerēšana ir nesekmīga. Tāpēc pirms jaunā Excel parametru faila ģenerēšanas pārliecinieties, ka testa gadījuma Excel parametru fails ir aizvērts.

16. Atlasiet **Rediģēt**, lai atvērtu jauno Excel parametru failu. 9. rindā ir redzams jauns ieraksts **Saglabāts mainīgais**. Šis mainīgais **{{ EcoResProductCreate\_ Identification\_ ProductNumber\_ Copy}}** tiek saglabāts uzdevuma ieraksta XML failā, un to var izmantot nākamajos testos.

    ![Ieraksts Saglabāts mainīgais.](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Jauna testa gadījuma izveide

1. Dodieties uz BPM bibliotēku **RSAT**.
2. Atlasiet procesu **Atbalsta biznesa procesa paraugs** un pēc tam labajā pusē atlasiet **Rediģēšanas režīms**.
3. Nomainiet lauka **Nosaukums** un lauka **Apraksts** vērtību uz **Preces izlaišana**. Pēc tam atlasiet **Saglabāt**.

    ![Nosaukums un apraksts ir mainīts uz Preces izlaišana.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Jauna uzdevuma ieraksta izveide, kam ir funkcija Validēt

- Izveidojiet uzdevuma ierakstu, lai izlaistu preci, kas iepriekš tika izveidota USRT juridiskajai personai. Papildinformāciju skatiet sadaļā [Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Ķēdē savienotiem testa gadījumiem vienmēr ieteicams atrast vai filtrēt nepieciešamo ierakstu, *ierakstot lauka vērtību manuāli*. Šādā veidā rīks var noteikt ierakstu, ar kuru ir jāveic darbība attiecībā pret nākamo testa gadījumu.

    ![Jauns uzdevuma ieraksts, kam ir funkcija Validēt.](./media/setup_rsa_tool_96.png)

    Kā redzams iepriekšējā attēlā, pēc produkta atrašanas, izmantojot ātro filtru, bet pirms vienuma **Izlaist preces** atlasīšanas ir jāvalidē lauka **Preces numurs** vērtība, lai pārliecinātos, ka preces ID ir iepriekš izveidotais preces ID. Lai validētu vērtību, ar peles labo pogu noklikšķiniet uz lauka **Preces numurs** un pēc tam atlasiet **Uzdevuma reģistrētājs \> Validēt \> Pašreizējā vērtība**.

    ![Pašreizējās vērtības validēšana.](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Uzdevuma ieraksta saglabāšana BPM

1. Kad uzdevuma ieraksts ir pabeigts, atlasiet **Saglabāt pakalpojumos Lifecycle Services**.

    ![Saglabāt Uzdevuma ierakstu pakalpojumos Lifecycle Services.](./media/setup_rsa_tool_98.png)

2. Bibliotēkas informācija tiek ielādēta no LCS.

    ![Notiek bibliotēkas informācijas ielāde.](./media/setup_rsa_tool_99.png)

3. Atlasiet BPM bibliotēku, kuru saistīt ar uzdevuma ierakstu. Šajā apmācībā atlasiet BPM bibliotēku **RSAT**, kas tika izveidota iepriekš, un biznesa procesu **Preces izlaišana** zem tās. Tad atl. **Labi**.

#### <a name="sync-bpm-to-azure-devops"></a>BPM sinhronizēšana ar Azure DevOps

1. Dodieties uz BPM bibliotēku un atveriet bibliotēku **RSAT**.
2. Atlasiet **VSTS sinhronizācija** un pēc tam atlasiet **Sinhronizēt testa gadījumus**. Papildinformāciju skatiet sadaļā [Sinhronizācijas testēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Kad sinhronizācija ir pabeigta, jaunais darba vienums un atbilstošais testa gadījums biznesa procesam **Preces izlaišana** tiek parādīts pakalpojumā Azure DevOps šeit: **Paneļi \> Darba vienumi**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Jauna testa gadījuma pievienošana esošajam testu komplektam

1. Dodieties uz **Testēšanas plāni \> Testēšanas plāni** un atlasiet plānu **RSAT testēšanas plāns**.
2. Atlasiet **Pievienot esošu**.
3. Lapā **Pievienot testa gadījumus komplektam** atlasiet **Izpildīt vaicājumu**.
4. Atlasiet jauno testa gadījumu, kas tika izveidots procesam **Preces izlaišana**, un pēc tam atlasiet **Pievienot testa gadījumus** lapas apakšējā labajā stūrī (šī poga nākamajā attēlā nav redzama).

    ![Lapa Pievienot testa gadījumus komplektam.](./media/setup_rsa_tool_100.png)

    Tagad testu komplektā ir divi testa gadījumi.

    ![Divi testa gadījumi testu komplektā.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testa gadījumu ielādēšana rīkā RSAT

1. Atveriet RSAT un atlasiet **Ielādēt**.
2. Testa gadījumi tiek ielādēti, un tiek parādīts brīdinājums ar tekstu “Veicot šo darbību, tiks pārrakstīti Excel testa datu faili, un lokālās izmaiņas tiks zaudētas. Vai vēlaties turpināt?”. Atlasiet **Jā**, lai atjauninātu Excel parametru failus lokālajā sistēmā, bet ne tos Excel parametru failus, kas tika augšupielādēti pakalpojumā Azure DevOps.

    ![Ar šo darbību tiks pārrakstīti Excel testa datu faili.](./media/setup_rsa_tool_102.png)

    Abi testa gadījumi tiek ielādēti kopā ar pirmā testa gadījuma Excel parametru failu. Pēdējā izpildē jūs atlasījāt **Augšupielādēt**, tādēļ parametru faili tiek ņemti no Azure DevOps.

    ![Ielādētie testa gadījumi.](./media/setup_rsa_tool_103.png)

3. Atlasiet tikai otro testa gadījumu un pēc tam atlasiet **Jauns \> Ģenerēt testa izpildes un parametru failus**.

#### <a name="edit-the-excel-parameter-file"></a>Excel parametru faila rediģēšana

1. Atlasiet tikai otro testa gadījumu un pēc tam atlasiet **Rediģēt**, lai atvērtu atbilstošo Excel parametru failu.
2. Kopējiet saglabāto mainīgo **{{ EcoResProductCreate\_ Identification\_ ProductNumber\_ Copy}}** (skatiet sadaļu [Esoša uzdevuma ieraksta modificēšana, lai izveidotu saglabātu mainīgo](#modify-an-existing-task-recording-to-create-a-saved-variable) ) no pirmā testa gadījuma visos laukos, kur tiek izmantots preces numurs. Šajā gadījumā mainīgais ir jākopē laukos **Preces numurs** un **Validēt preces numuru** lapā **EcoResProductListPage**.

    ![Lauki Preces numurs un Validēt preces numuru.](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Mainīgie var tikt nodoti starp testiem tikai tās pašas testa izpildes laikā. Mainīgo nosaukumiem ir precīzi jāsakrīt.

3. Atlasiet **Saglabāt** un pēc tam aizveriet Excel darbgrāmatu.
4. Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā.

#### <a name="run-the-chained-test-cases"></a>Ķēdē savienoto testa gadījumu palaišana

1. Atlasiet abus testa gadījumus un pēc tam atlasiet **Palaist**.
2. Pārbaudiet, vai abi testa gadījumi ir sekmīgi.

    ![Rezultātu lauks ir iestatīts kā sekmīgs abiem testa gadījumiem.](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]