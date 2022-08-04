---
title: Jaunināšana uz pušu un globālās adrešu grāmatas modeli
description: Šajā rakstā ir aprakstīts, kā jaunināt dubultās rakstīšanas datus puses un globālās adrešu grāmatas modelī.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 02ab3675db0d78efa1e4e43188d79bb1e763a713
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111824"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Jaunināšana uz pušu un globālās adrešu grāmatas modeli

[!include [banner](../../includes/banner.md)]



Datu [Microsoft Azure fabrikas veidnes](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) palīdz jaunināt šādus esošos datus dubultās rakstīšanas puses un globālās adrešu grāmatas modelī: **datus** konta, **·** **kontaktu** un kreditoru tabulās, pasta un elektroniskās adreses.

Ir pieejamas trīs tālāk norādītās datu fabrikas veidnes. Tie palīdz saskaņot datus no finanšu un operāciju programmām un debitoru lietojumprogrammām.

- **[Puses veidne](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Jauniniet datus uz dubultās rakstīšanas Puses-GAB shēmu/arm_template.json)** – **·** **šī** veidne palīdz atjaunināt pušu un kontaktpersonu datus, kas ir **saistīti ar kontu**,**kontaktpersonu** un **kreditora** datiem.
- **[Puses pasta adreses](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) veidne (Jauniniet datus uz dubultās rakstīšanas Puses GAG shēmu/jauniniet uz puses pasta adresi - GAG/arm_template.json)** –**šī** veidne palīdz atjaunināt pasta adreses, kas saistītas ar kontu, **·** **kontaktpersonu** un kreditora datiem.
- **[Puses elektroniskās adreses](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) veidne (Jauniniet datus uz dubultās rakstīšanas Puses-GAG shēmu/jauniniet uz puses elektronisko adresi - GAG/arm_template.json)** – **šī** veidne palīdz atjaunināt elektroniskās adreses, kas ir saistītas ar kontu, **·** **kontaktpersonu** un kreditora datiem.

Procesa beigās tiek ģenerētas šādas komatatdalīto vērtību (.csv) faili.

| Faila nosaukums | Nolūks |
|---|---|
| FONewParty.csv | Šis fails palīdz izveidot jaunus **Puses** ierakstus finanšu un operāciju programmā. |
| ImportFONewPostalAddressLocation.csv | Šis fails palīdz finanšu un **operāciju programmā** izveidot jaunus pasta adrešu atrašanās vietas ierakstus. |
| ImportFONewPartyPostalAddress.csv | Šis fails palīdz izveidot jaunus **puses pasta adrešu** ierakstus finanšu un operāciju programmā. |
| ImportFONewPostalAddress.csv | Šis fails palīdz izveidot jaunus **pasta adrešu** ierakstus finanšu un operāciju programmā. |
| ImportFONewElectronicAddress.csv | Šis fails palīdz izveidot jaunus **Elektroniskās adreses** ierakstus finanšu un operāciju programmā. |

Šajā rakstā skaidrots, kā izmantot datu fabrikas veidnes un jaunināt savus datus. Ja pielāgojumu nav, tās varat izmantot pēc to pielāgošanas. Tomēr, ja ir pielāgojumi konta, **kontaktpersonas** **un** **kreditora** datiem, veidnes ir jāmodificē, kā aprakstīts šajā rakstā.

> [!IMPORTANT]
> Ir īpašas instrukcijas puses pasta adreses un Puses elektroniskās adreses veidņu izpildē. Vispirms jāpalaiž Puses veidne, tad Puses pasta adreses veidne un pēc tam Puses elektroniskās adreses veidne. Katra veidne ir veidota, lai importētu atsevišķā datu ražotnē.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu jaunināt uz puses un globālās adrešu grāmatas modeli, ir jābūt šādiem priekšnosacījumi:

+ Jums ir jābūt Azure [abonementam](https://portal.azure.com/).
+ Jums nepieciešama piekļuve [veidnēm](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Jums jābūt jau esošam duālās rakstīšanas debitoram.

## <a name="prepare-for-the-upgrade"></a>Sagatavoties jaunināšanai

Jaunināšanai ir nepieciešama šāda sagatavošana:

+ **Pilna sinhronizācija: gan finanšu**, gan operāciju vide, kā arī debitoru tiesīju vide ir pilnībā sinhronizētā stāvoklī, kas paredzēts konta (Debitora) **,** **kontaktpersonu un kreditoru** tabulām **.**
+ **Integrācijas atslēgas:** konts (Debitors) **,** **·** **kontakts un kreditors tabulas debitoru ieslēgšanas programmās izmanto box integrācijas atslēgas.** Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.
+ **Puses numurs:** visiem **konta (Debitora)**, **kontaktpersonas** **un kreditora** ierakstiem, kas tiks jaunināti, ir puses numurs. Ieraksti, kuriem nav puses numura, tiks ignorēti. Ja vēlaties jaunināt šos ierakstus, pirms jaunināšanas procesa sākšanas pievienojiet tiem puses numuru.
+ **Sistēmas nobraukums:** jaunināšanas procesa laikā bezsaistē jālieto gan Finanšu un operāciju vide, gan debitoru iesaistīšanos vide.
+ **Momentuzņēmums:** paņem momentuzņēmumu gan finanšu, gan operāciju programmām un debitoru ieslēgšanas programmām. Pēc tam var izmantot momentuzņēmumus, lai atjaunotu iepriekšējo stāvokli, ja tas nepieciešams.

## <a name="deployment"></a>Izvietojums

1. Lejupielādējiet veidnes no [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Pierakstieties [Azure portālā](https://portal.azure.com/).
3. Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.
5. Izveidojiet [datu rūpnīcā](/azure/data-factory/quickstart-create-data-factory-portal) jūsu izveidoto resursu grupā.
6. Atveriet datu rūpnīcā un atlasiet elementu Autors **&Pārraudzīt**.
7. Cilnē **Pārvaldīt** atlasiet **ARM veidne**.
8. Atlasiet **Importēt ARM veidni,** lai importētu **puses** veidni.
9. Importējiet veidni datu fabrikā. Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.

    | Lauks | Vērtība |
    |---|---|
    | Abonements | Azure abonements |
    | Resursa grupa | Nodrošiniet tos pašus resursus, kuros ir izveidots glabāšanas konts. |
    | Reģions | Reģions |
    | Fabrikas nosaukums | Fabrikas nosaukums |
    | FO saistīta Pakalpojums_pakalpojums galvenā atslēga | Programmas atslēga |
    | Azure Blob krātuves_savienojuma virknes | Azure BLOB glabāšanas savienojuma virkne |
    | Dynamics CRM saistīta Pakalpojuma_parole | Parole lietotāja kontam, kuru norādāt kā lietotājvārdu |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks | Informācija (domēna vārds vai nomnieka ID) par nomnieku, kurā atrodas jūsu programma |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID | Programmas klienta ID |
    | Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds | Lietotājvārds, kas tiek izmantots, lai izveidotu savienojumu ar Dynamics 365 |

    Papildinformāciju skatiet tālāk norādītajās tēmās.

    - [Manuāli veicināt Resource Manager veidni katrai videi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Saistītie pakalpojuma rekvizīti](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopēt datus, izmantojot Azure datu ražotni](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.

    ![Datu kopas, datu plūsma un saistītais pakalpojums.](media/data-factory-validate.png)

11. Dodieties uz **Pārvaldīt**. Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**. Pēc tam **atlasiet DynamicsCrmLinkedService**. **Dialoglodziņā Rediģēt saistīto pakalpojumu (Dynamics CRM)** ievadiet šādas vērtības.

    | Lauks | Vērtība |
    |---|---|
    | Nosaukums/vārds, uzvārds | Atlasiet DynamicsCrmLinkedService |
    | Apraksts | Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus |
    | Izveidot savienojumu, izmantojot integrācijas izpildlaiku | AutoResolvelntegrationRuntime |
    | Izvietošanas veids | Tiešsaiste |
    | Pakalpojuma Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentifikācijas veids | Office365 |
    | Lietotājvārds | |
    | Parole vai Azure Key Vault | Parole |
    | Parole | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Sagatavošanās datu fabrikas veidņu palaišanai

Šajā sadaļā aprakstīti iestatījumi, kas ir nepieciešami pirms Puses pasta adreses un Puses elektroniskās adreses datu fabrikas veidņu palaišanas.

### <a name="setup-to-run-the-party-postal-address-template"></a>Puses pasta adreses veidnes palaišanas iestatīšana

1. Piesakieties debitoru piesaistes programmās un dodieties uz iestatījumu **personalizēšanas** \> **iestatījumiem.** Pēc tam cilnē **Vispārīgi** konfigurējiet laika joslas iestatījumu sistēmas administratora kontam. Laika joslai ir jābūt universālajā koordinētajā laikā (UTC), lai atjauninātu pasta adrešu datumus "derīgs no" un "derīgs līdz" no finanšu un operāciju programmām.

    ![Laika joslas iestatīšana sistēmas administratora kontam.](media/ADF-1.png)

2. Datu fabrikas cilnē Pārvaldīt **zem** Globālie parametri **izveidojiet** šādu globālo parametru.

    | Numurs | Nosaukums/vārds, uzvārds | Veids | Vērtība |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | virkne | Šis parametrs pievieno sērijas numuru tikko izveidotajām pasta adresēm kā prefiksu. Noteikti norādiet virkni, kas nav pretrunā ar pasta adresēm finanšu un operāciju programmās un debitoru iesaistes programmās. Piemēram, izmantojiet **ADF-PAD-**. |

    ![Cilnē Pārvaldīt izveidots globālais PostalAddressIdPrefix parametrs.](media/ADF-2.png)

3. Kad esat beidzis, atlasiet Publicēt **visu**.

    ![Publicēt visu pogu.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Iestatīt puses elektroniskās adreses veidnes palaišanai

1. Cilnes Pārvaldīt cilnē Datu rūpnīca **,** zem Globālie **parametri**, izveidojiet šādus globālos parametrus.

    | Numurs | Nosaukums/vārds, uzvārds | Veids | Vērtība |
    |---|---|---|---|
    | 1 | IsFO avots | Būla (Bool) | Šis parametrs nosaka, kuras primārās sistēmas adreses tiek aizvietotas konfliktu gadījumā. Ja vērtība ir **patiesa**, primārās adreses finanšu un operāciju programmās aizstās primārās adreses debitoru lietojumprogrammās. Ja vērtība ir **nepatiesa**, primārās adreses debitoru piesaistes programmās aizstās primārās adreses finanšu un operāciju programmās. |
    | 2 | ElectronicAddressIdPrefix (elektroniskaisaddressIdPrefix) | virkne | Šis parametrs pievieno sērijas numuru tikko izveidotajām elektroniskajām adresēm kā prefiksu. Pārliecinieties, vai ir sniegta virkne, kas nav pretrunā ar elektroniskajām adresēm finanšu un operāciju programmās un debitoru iesaistes programmās. Piemēram, izmantojiet **ADF-EAD-**. |

    ![IsFOSource un ElectronicAddressIdPrefix globālie parametri, kas izveidoti cilnē Pārvaldīt.](media/ADF-4.png)

2. Kad esat beidzis, atlasiet Publicēt **visu**.

## <a name="run-the-templates"></a>Veidņu palaišana

1. Apturiet šādas **Puses**, **Konta**, Kontaktpersonas **un** Kreditora **duālās** rakstīšanas kartes, kas izmanto finanšu un operāciju programmas:

    + CDS puses (msdyn_parties) 
    + Debitori V3 (konti)
    + Debitori V3 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + Kreditors V2 (msdyn_vendor)
    + Kontakti V2 (msdyn_contactforparties)
    + CDS puses pasta adrešu atrašanās vietas (msdyn_partypostaladdresses)
    + CDS pasta adreses vēsture V2 (msdyn_postaladdresses)
    + CDS puses pasta adrešu atrašanās vietas (msdyn_postaladdresscollections)
    + Puses kontaktpersonas V3 (msdyn_partyelectronicaddresses)

2. Pārliecinieties, ka kartes tika noņemtas no **msdy_dualwriteruntimeconfig** tabulas Dataverse.
3. Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.
4. Finanšu un operāciju programmā palaidiet sākotnējo sinhronizāciju **tālāk redzamajās** tabulās, ja tajās ir dati:

    + Uzrunas
    + Personas rakstura veidi
    + Komplimentāra slēgšana
    + Kontaktpersonu amati
    + Lēmumu pieņemšanas lomas
    + Lojalitātes programmu līmeņi

5. Debitoru summu programmā atspējojiet šādus spraudņa soļus:

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

    + Debitora adrese

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Pirkšana.CreatePartyAddress: debitora adreses izveide

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Pirkšanas pasūtījumi.CreatePartyAddress: customeraddress atjauninājums

        + Delete

            + Microsoft.Dynamics.GABExtended.Failus DeleteCustomerAddress: debitoraaddress dzēšana

    + msdyn_partypostaladdress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Pirkšana.CreateCustomerAddress: izveidojiet msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Gabs.PartyPostalAddress: izveidojiet msdyn_partypostaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Pirkšana.CreateCustomerAddress: atjaunināšana msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Gabs.PartyPostalAddress: atjaunināšana msdyn_partypostaladdress

    + msdyn_postaladdress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Wps.PostalAddress: izveidojiet msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Wps.PostalAddressPostCreate: izveidojiet msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Pirkšana.UpdateCustomerAddress: izveide msdyn_postaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Grips.PostalAddressUpdate: atjaunināšana msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Tora.UpdateCustomerAddress: atjaunināšana msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Gabs.PartyElectronicAddressSync: izveide msdyn_partyelectronicaddress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Gabs.PartyElectronicAddressSync: atjaunināšana msdyn_partyelectronicaddress

        + Delete

            + Microsoft.Dynamics.GABExtended.Failus DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

6. Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

7. Datu rūpnīcā palaidiet veidni, atlasot Trigeri **tagad**, kā parādīts šajā ilustrācijā. Šis process var aizņemt dažas stundas, atkarībā no datu apjoma.

    ![Veidnes atstāšana.](media/data-factory-trigger.png)

    > [!NOTE]
    > Ja esat pielāgojumus kontam **, kontaktpersonai** **un** kreditoram **·**, veidne ir jāmodificē.

8. Importēt jaunos **Puses** ierakstus finanšu un operāciju programmā.

    1. Lejupielādējiet **FONewParty.csv** failu no Azure BLOB krātuves. Ceļš ir **partybootstrapping/output/FONewParty.csv**.
    2. Konvertējiet **FONewParty.csv** failu uz Excel failu un importējiet Excel failu finanšu un operāciju programmā. Vai arī, ja CSV imports darbojas jūsu darbiem, jūs varat importēt .csv failu. Šī darbība var aizņemt dažas stundas, atkarībā no datu apjoma. Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).

    ![Notiek puses ierakstu Dataverse importēšana.](media/data-factory-import-party.png)

9. Datu rūpnīcas izpildiet Puses pasta adreses un Puses elektroniskās adreses veidnes vienu pēc otras.

    + Puses pasta adreses veidne upsert visus pasta adrešu ierakstus debitoru piesaistes programmā un saista tos ar atbilstošajiem konta, **kontaktpersonas** **un** **kreditora** ierakstiem. Tiek ģenerēti arī trīs .csv faili: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv un ImportFONewPostalAddress.csv.
    + Puses elektroniskās adreses veidne upsert visas elektroniskās adreses debitoru ieslēgšanu programmā un **saista** tās ar atbilstošajiem konta, **kontaktpersonas** un **kreditora** ierakstiem. Tas ģenerē arī vienu .csv failu: ImportFONewElectronicAddress.csv.

    ![Notiek Puses pasta adreses un Puses elektronisko adrešu veidņu izpildšana.](media/ADF-7.png)

10. Lai atjauninātu finanšu un operāciju programmu ar šie datiem, jums .csv failu konvertēšana Excel [darbgrāmatā un jāimportē to finanšu un operāciju programmā](../data-import-export-job.md). Vai arī, ja CSV imports darbojas jūsu darbiem, jūs varat importēt .csv failus. Šī darbība var aizņemt dažas stundas, atkarībā no apjoma.

    ![Veiksmīgi importēts.](media/ADF-8.png)

11. Debitoru ieslēgšanu programmā iespējojiet šādas spraudņa darbības:

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

    + msdyn_partypostaladdress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Pirkšana.CreateCustomerAddress: izveidojiet msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Gabs.PartyPostalAddress: izveidojiet msdyn_partypostaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Pirkšana.CreateCustomerAddress: atjaunināšana msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Gabs.PartyPostalAddress: atjaunināšana msdyn_partypostaladdress

    + msdyn_postaladdress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Wps.PostalAddress: izveidojiet msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Wps.PostalAddressPostCreate: izveidojiet msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Pirkšana.UpdateCustomerAddress: izveide msdyn_postaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Grips.PostalAddressUpdate: atjaunināšana msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Tora.UpdateCustomerAddress: atjaunināšana msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Gabs.PartyElectronicAddressSync: izveide msdyn_partyelectronicaddress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Gabs.PartyElectronicAddressSync: atjaunināšana msdyn_partyelectronicaddress

        + Delete

            + Microsoft.Dynamics.GABExtended.Failus DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

12. Ja iepriekš esat tās dezaktivējat, programmā Debitoru saistības aktivizējiet šādas darbplūsmas:

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

13. Palaidiet ar **pusi** saistīto karti, kā tas ir aprakstīts Puses un [globālajā adrešu grāmatā](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Datu fabrikas veidņu skaidrojums

Šajā sadaļā ir jāveic soļi katrā datu fabrikas veidnē.

### <a name="steps-in-the-party-template"></a>Soļi puses veidnē

1. 1. līdz 6. darbībā ir identificēti uzņēmumi, kas ir iespējoti duālai rakstīšanai, un tiem tiek veidots filtra klauzula.
2. No 7. līdz 7.09. darbībai ir izgūti dati gan no finanšu un operāciju programmas, gan no debitoru piesaistes programmas, kā arī no datu jaunināšanai stadijas.
3. No 8. līdz 9. darbībai **ir** salīdzināts konta, **·** **kontaktpersonas** un kreditora ierakstu puses numurs starp finanšu un operāciju programmu un debitoru piesaistes programmu. Visi ieraksti, kam nav puses numura, tiek izlaisti.
4. 10. darbībā tiek ģenerēti .csv failu puses ierakstiem, kas ir jāizveido debitoru piesaistes programmā un finanšu un operāciju programmā.

    - **FOCDSParty.csv** – šajā failā ir iekļauti visi pušu ieraksti no abām sistēmām, neatkarīgi no tā, vai uzņēmums ir aktivizēts duālām rakstiet.
    - **FONewParty.csv** – šis fails Dataverse satur apakškopu no pušu ierakstiem, kas ir informēti (piemēram, potenciālo **klientu tipa** konti).

5. 11. darbība izveido puses debitoru piesaistes programmā.
6. 12. darbībā tiek izgūti pušu globāli unikālie identifikatori (GUID) **no** debitoru ieslēgšanas programmas un tā, lai vēlākos soļos tos varētu saistīt ar kontu, **·** **kontaktpersonu** un kreditoru ierakstiem.
7. 13. darbība saista **kontu**, **kontaktu** un **kreditora** ierakstus ar puses GUID.
8. No 14. līdz 14.-3 **. solim tiek atjaunināti konta,** **·** **kontaktpersonas un kreditora ieraksti debitoru piesaistes programmā ar puses GUID.**
9. Darbības 15-1 līdz 15-3 **·** **sagatavojiet kontaktpersonu puses ierakstiem kontam**, **kontaktpersonai** un kreditora **ierakstiem**.
10. No 16. līdz 16.07. darbībām tiek izgūti atsauces dati, piemēram, uzrunas un personisko rakstzīmju tipi, **un tie tiek asociēti ar kontaktpersonu puses** ierakstiem.
11. 17. darbībā tiek apvienota **konta**, **kontaktpersonas** **un kreditora ierakstu** kontaktpersonas **ieraksti**.
12. 18. darbība importē **Kontaktpersonu puses ierakstiem** debitoru tiesīgņu programmā.

### <a name="steps-in-the-party-postal-address-template"></a>Soļi Puses pasta adreses veidnē

1. No 1. līdz 1.10. darbībai ir izgūti dati gan no finanšu un operāciju programmas, gan no debitoru piesaistes programmas, kā arī no stadijas, kurā tiek jaunināti dati.
2. 2. darbībā tiek de normalizēti pasta adrešu dati finanšu un operāciju programmā, pievienojot pasta adresi un puses pasta adresi.
3. 3. darbībā tiek noņemti konta, kontaktpersonas un kreditora adreses datu dublikāti un sapludināšana no debitoru ieslēgšanu programmas.
4. 4. darbībā .csv finanšu un operāciju programmas failu sarakstu, lai izveidotu jaunus adrešu datus, kas ir balstīti uz kontu, kontaktpersonu un kreditoru adresēm.
5. 5. - 1. darbība izveido .csv debitoru piesaistes programmai, lai izveidotu visus adrešu datus, pamatojoties gan uz finanšu un operāciju programmu, gan uz debitoru piesaistes programmu.
6. No 5. līdz 2. .csv importa faili tiek pārveidoti finanšu un operāciju importa formātā manuālai importēšanai.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 6. darbība importē pasta adrešu kolekcijas datus debitoru piesaistes programmā.
8. 7. darbības izgūst pasta adrešu kolekcijas datus no debitoru piesaistes programmas.
9. 8. darbība izveido debitora adreses datus un saista pasta adrešu kolekcijas ID.
10. No 9. soļiem 9-1 līdz 9-2 ir asociēta puse un pasta adrešu kolekcijas D ar pasta adresēm un pušu pasta adresēm.
11. No 10. līdz 10.03. solim debitoru adrešu, pasta adrešu un pušu pasta adrešu importēšana debitoru piesaistes programmā.

### <a name="steps-in-the-party-electronic-address-template"></a>Soļi Puses elektroniskās adreses veidnē

1. No 1. līdz 1.,5. darbībai ir izgūti dati gan no finanšu un operāciju programmas, gan no debitoru piesaistes programmas, kā arī no datu jaunināšanai stadijas.
2. 2. darbība konsolidē elektroniskās adreses debitoru iesaistījumtņu programmā no konta, kontaktpersonas un kreditora entītijām.
3. 3. darbībā tiek apvienoti primārās elektroniskās adreses dati no debitoru piesaistes programmas un finanšu un operāciju programmas.
4. 4. darbība izveido .csv failus.

    - Izveidojiet jaunus elektroniskās adreses datus finanšu un operāciju programmai, pamatojoties uz kontu, kontaktpersonu un kreditoru adresēm.
    - Izveidojiet jaunus elektroniskās adreses datus debitoru lietojumprogrammai, balstoties uz elektronisko adresi, kontu, kontaktpersonu un kreditoru adresēm finanšu un operāciju programmā.

5. 5.-1. darbība importē elektroniskās adreses debitoru piesaistes programmā.
6. No 5. līdz 2. .csv tiek izveidoti faili, lai atjauninātu primārās adreses kontiem un kontaktpersonām debitoru iesaistes programmā.
7. No 6. līdz 6.2. solim importējiet kontus un sazinieties ar primārajām adresēm klientu runāšanas programmā.

## <a name="troubleshooting"></a>Problēmu novēršana

1. Ja process neizdodas, atkārtoti palaidiet datu ražotni. Sāciet no neizdevušās aktivitātes.
2. Daži datu fabrikas ģenerētie faili var tikt izmantoti datu validēšanai.
3. Datu fabrika darbojas balstoties uz .csv failiem. Tāpēc, ja komats ir iekļauts jebkurā lauka vērtībā, tas var atbilst rezultātiem. Visu komatu noņemšana no lauku vērtībām.
4. Cilne **Pārraudzība** sniedz informāciju par visiem soļiem un datiem, kas ir apstrādāti. Atlasiet noteiktu darbību, lai to atkļūdotu.

    ![Cilne Pārraudzība.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Uzziniet vairāk par veidni

Papildinformāciju par veidni skatiet sadaļā [Komentāri par Azure datu fabrikas veidnes readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

