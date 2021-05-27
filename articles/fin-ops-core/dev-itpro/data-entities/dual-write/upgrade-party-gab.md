---
title: Jaunināšana uz pušu un globālās adrešu grāmatas modeli
description: Šajā tēmā ir aprakstīts, kā jaunināt dubultās rakstīšanas datus puses un globālās adrešu grāmatas modelī.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018316"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Jaunināšana uz pušu un globālās adrešu grāmatas modeli

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šī [Azure datu fabrikas veidne](https://aka.ms/dual-write-gab-adf) palīdz jaunināt esošo **Konta**, **Kontaktpersonas** un **Kreditora** tabulas datus dubultās rakstīšanas puses un globālās adrešu grāmatas modelī. Veidne saskaņo datus no Finance and Operations programmām un Customer Engagement programmām. Procesa beigās **Puses** ierakstu **Puses** un **Kontaktpersonas** lauki tiks izveidoti un saistīti ar **Konta**, **Kontaktpersonas** un **Kreditora** ierakstiem Customer Engagement programmās. Tiek ģenerēts .csv fails (`FONewParty.csv`), lai izveidotu jaunus **Puses** ierakstus programmā Finance and Operations. Šajā tēmā ir sniegtas norādes par datu fabrikas veidnes lietošanu un datu jaunināšanu.

Ja jums nav nekādu pielāgojumu, varat izmantot veidni, kāda tā ir. Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē, izmantojot tālāk norādītās instrukcijas.

> [!Note]
> Veidne palīdz jaunināt tikai **Puses** datus. Nākamajā laidienā tiks iekļautas pasta un elektroniskās adreses.

## <a name="prerequisites"></a>Priekšnosacījumi

Ir nepieciešami šādi priekšnosacījumi:

+ [Azure abonements](https://portal.azure.com/)
+ [Piekļuve veidnei](https://aka.ms/dual-write-gab-adf)
+ Jūs esat jau esošs duālās rakstīšanas debitors.

## <a name="prepare-for-the-upgrade"></a>Sagatavoties jaunināšanai

+ **Pilnībā sinhronizēts**: abas vides ir pilnībā sinhronizētas **Kontam (Debitoram)**, **Kontaktpersonai** un **Kreditoram**.
+ **Integrācijas atslēgas**: tabulas **Konts (Debitors)**, **Kontaktpersona** un **Kreditors** Customer Engagement programmās izmanto integrācijas atslēgas, kas nosūtītas nestandarti. Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.
+ **Puses numurs**: visiem **Konta (Debitora)**, **Kontaktpersonas** un **Kreditora** ierakstiem, kas tiks jaunināti, ir **Puses** numurs. Ieraksti bez **Puses** numura tiks ignorēti. Ja vēlaties jaunināt šos ierakstus, pirms jaunināšanas procesa sākšanas pievienojiet tiem **Puses** numuru.
+ **Sistēmas noplūde**: jaunināšanas laikā jums būs jāizmanto gan Finance and Operations, gan Customer Engagement vides bezsaistē.
+ **Momentuzņēmums**: izveidot momentuzņēmumus gan no Finance and Operations, gan no Customer Engagement programmām. Izmantojiet momentuzņēmumus, lai atjaunotu iepriekšējo stāvokli, ja nepieciešams.

## <a name="deployment"></a>Izvietojums

1. Lejupielādējiet veidni no [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Pierakstīšanās programmā [Microsoft Azure](https://portal.azure.com/).

3. Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.

5. Izveidojiet [datu fabriku](/azure/data-factory/quickstart-create-data-factory-portal) virs izveidotās resursu grupas.

6. Atveriet datu fabriku un atlasiet elementu **Autors & Pārraudzīt**.

7. Cilnē **Pārvaldīt** atlasiet **ARM veidne**.

8. Izvēlieties **Importēt ARM veidni**, lai importētu **Puses** veidni.

9. Importējiet veidni datu fabrikā. Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.

    Lauks | Vērtība
    ---|---
    Abonements | Azure abonements
    Resursa grupa | Nodrošiniet to pašu resursu, kurā ir izveidots glabāšanas konts.
    Reģions | Norādīt reģionu.
    Fabrikas nosaukums | Norādiet fabrikas nosaukumu.
    FO saistīta Pakalpojums_pakalpojums galvenā atslēga | Norādiet pieteikuma atslēgu.
    Azure Blob krātuves_savienojuma virknes | Azure Blob krātuves savienojuma virkne.
    Dynamics CRM saistīta Pakalpojuma_parole | Parole lietotāja kontam, kuru norādījāt kā lietotājvārdu.
    FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks | Norādiet informāciju par nomnieku (domēna vārdu vai nomnieka ID), kurā atrodas jūsu pieteikums.
    FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID | Norādiet pieteikuma debitora ID.
    Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds | Lietotājvārds, ar kuru jāizveido savienojums ar Dynamics.

    Papildinformāciju skatiet šeit: [Manuāli veicināt Resource Manager veidni katrai videi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Saistīto pakalpojumu rekvizīti](/azure/data-factory/connector-dynamics-ax#linked-service-properties) un [Kopēt datus, izmantojot Azure datu fabriku](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.

   ![Datu kopas, datu plūsma un saistītais pakalpojums](media/data-factory-validate.png)

11. Dodieties uz **Pārvaldīt**. Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**. Atlasiet **DynamicsCrmLinkedService**. Formā **Rediģēt saistīto pakalpojumu (Dynamics CRM)** ievadiet šādas vērtības:

    Lauks | Vērtība
    ---|---
    Nosaukums/vārds, uzvārds | Atlasiet DynamicsCrmLinkedService
    Apraksts | Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus
    Izveidot savienojumu, izmantojot integrācijas izpildlaiku | AutoResolvelntegrationRuntime
    Izvietošanas veids | Tiešsaiste
    Pakalpojuma Uri | `https://<organization-name>.crm[x].dynamics.com`
    Autentifikācijas veids | Office365
    Lietotājvārds |
    Parole vai Azure Key Vault | Parole
    Parole |

## <a name="run-the-template"></a>Palaist veidni

1. Apturiet šo **Konta**, **Kontaktpersonas** un **Kreditora** dubultās rakstīšanas darbību, izmantojot programmu Finance and Operations.

    + Debitori V3 (konti)
    + Debitori V3 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + Kreditors V2 (msdyn_vendor)

2. Pārliecinieties, ka kartes no tabulas ir noņemtas no tabulas `msdy_dualwriteruntimeconfig` pakalpojumā Dataverse.

3. Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.

4. Ja šajās tabulās ir dati, tad programmā Finance and Operations palaidiet tām **Sākuma sinhronizāciju**.

    + Uzrunas
    + Personas rakstura veidi
    + Komplimentāra slēgšana
    + Kontaktpersonu amati
    + Lēmumu pieņemšanas lomas
    + Lojalitātes programmu līmeņi

5. Customer Engagement programmā deaktivizējiet tālāk norādītas darbības.

    + Konta atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana
    + Kontaktpersonas atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana
    + msdyn_party atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana
    + msdyn_vendor atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana

6. Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

7. Datu fabrikā palaidiet veidni, atlasot **Aktivizēt tūlīt**, kā parādīts šajā attēlā. Šis process var ilgt dažas stundas, balstoties uz datu apjomu.

    ![Trigera palaišana](media/data-factory-trigger.png)

    > [!NOTE]
    > Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē.

8. Importēt jaunos **Puses** ierakstus programmā Finance and Operations.

    + Lejupielādējiet `FONewParty.csv` failu no Azure BLOB krātuves. Ceļš ir `partybootstrapping/output/FONewParty.csv`.
    + Konvertējiet `FONewParty.csv` failu par Excel failu un importējiet Excel failu programmā Finance and Operations.  Ja jums darbojas csv importēšana, varat tieši importēt csv failu. Atkarībā no datu apjoma, importēšanas laiks var ilgt dažas stundas. Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).

    ![Importēt Datavers puses ierakstus](media/data-factory-import-party.png)

9. Customer Engagement programmās aktivizējiet tālāk norādītas darbības:

    + Konta atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana
    + Kontaktpersonas atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana
    + msdyn_party atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana
    + msdyn_vendor atjaunināšana
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana

10. Customer Engagement programmās aktivizējiet šādas darbplūsmas, ja tās ir deaktivizētas iepriekšējās darbībās:

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

11. Palaidiet ar **Pusi** saistītās kartes, kā norādīts sadaļā [Puse un globālā adrešu grāmata](party-gab.md).

## <a name="troubleshooting"></a>Problēmu novēršana

1. Procesā neizdodas vēlreiz palaist datu fabriku, sākot no neveiksmīgās darbības.
2. Dažus failus ģenerē datu fabrika, ko varat izmantot datu apstiprināšanas nolūkiem.
3. Datu fabrika darbojas, pamatojoties uz csv failiem, kas tiek atdalīti ar komatu. Ja lauka vērtībai ir komats, tas var traucēt rezultātus. Ir jānoņem komati.
4. Cilne **Pārraudzība** sniedz informāciju par visam darbībam un apstrādātajiem datiem. Atlasiet noteiktu darbību, lai to atkļūdotu.

    ![Cilne Pārraudzība](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Uzziniet vairāk par veidni

Komentārus veidnei varat atrast [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) failā.