---
title: Jaunināšana uz pušu un globālās adrešu grāmatas modeli
description: Šajā tēmā ir aprakstīts, kā jaunināt dubultās rakstīšanas datus puses un globālās adrešu grāmatas modelī.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 579a7d19ee7196d3242c78bd9915df24ec479c31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060489"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Jaunināšana uz pušu un globālās adrešu grāmatas modeli

[!include [banner](../../includes/banner.md)]



Datu rūpnīcas [Microsoft Azure veidnes](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) palīdz jaunināt šādus esošos datus divrakstotā uz pušu un globālo adrešu grāmatas modeli: dati **tabulās Konts**, **Kontaktpersona** un **Piegādātājs**, kā arī pasta un elektroniskās adreses.

Tiek nodrošinātas šādas trīs datu fabrikas veidnes. Tie palīdz saskaņot datus gan no Finance, gan Operations programmām un klientu iesaistes programmām.

- **[Puses veidne](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Jaunināt datus uz divrakstīšu Party-GAB shēmu/arm_template.json)** — šī veidne palīdz jaunināt **pušu** un **kontaktpersonu** datus, kas ir saistīti ar **uzņēmuma**, **kontaktpersonas** un **piegādātāja** datiem.
- **[Puses pasta adreses veidne](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Jaunināt datus uz divrakstīšu Party-GAB shēmu/Jaunināt uz puses pasta adresi - GAB/arm_template.json)** — šī veidne palīdz jaunināt pasta adreses, kas ir saistītas ar **konta**, **kontaktpersonas** un **piegādātāja** datiem.
- **[Puses elektroniskās adreses veidne](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Jaunināt datus uz divrakstīšu Party-GAB shēmu/ Jaunināt uz puses elektronisko adresi - GAB / arm_template.json)** - Šī veidne palīdz jaunināt elektroniskās adreses, kas ir saistītas ar **konta**, **kontaktpersonas** un **piegādātāja** datiem.

Procesa beigās tiek ģenerēti šādi ar komatiem atdalīti vērtību (.csv) faili.

| Faila nosaukums | Nolūks |
|---|---|
| FONewParty.csv | Šis fails palīdz izveidot jaunus **pušu** ierakstus programmā Finanses un operācijas. |
| ImportFONewPostalAddressLocation.csv | Šis fails palīdz izveidot jaunus **pasta adreses atrašanās vietas** ierakstus programmā Finanses un operācijas. |
| ImportFONewPartyPostalAddress.csv | Šis fails palīdz izveidot jaunus **pušu pasta adrešu** ierakstus programmā Finanses un operācijas. |
| ImportFONewPostalAddress.csv | Šis fails palīdz izveidot jaunus **pasta adreses** ierakstus programmā Finanses un operācijas. |
| ImportFONewElektroniskāAddress.csv | Šis fails palīdz izveidot jaunus **elektroniskās adreses** ierakstus programmā Finanses un operācijas. |

Šajā tēmā ir paskaidrots, kā izmantot datu fabrikas veidnes un jaunināt datus. Ja jums nav pielāgojumu, varat izmantot veidnes tādas, kādas tās ir. Tomēr, ja jums ir konta, kontaktpersonas **un** **piegādātāja** datu pielāgojumi, veidnes ir jāmodificē, kā aprakstīts šajā tēmā. **·**

> [!IMPORTANT]
> Ir īpaši norādījumi par Puses pasta adreses un pušu elektronisko adrešu veidņu vadīšanu. Vispirms ir jāpalaiž puses veidne, pēc tam puses pasta adreses veidne un pēc tam puses elektroniskās adreses veidne. Katra veidne ir paredzēta importēšanai atsevišķā datu rūpnīcā.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu jaunināt uz pušu un globālās adrešu grāmatas modeli, ir jābūt ieviestiem šādiem priekšnosacījumiem:

+ Jums ir [nepieciešams Azure abonements](https://portal.azure.com/).
+ Jums ir jābūt piekļuvei [veidnēm](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Jums jābūt jau esošam duālās rakstīšanas debitoram.

## <a name="prepare-for-the-upgrade"></a>Sagatavoties jaunināšanai

Jaunināšanai ir nepieciešama šāda sagatavošana:

+ **Pilnīga sinhronizācija:** gan finanšu un operāciju vide, gan klientu piesaistes vide ir pilnībā sinhronizēta tabulām **Konts (klients),** **Kontaktpersona** un **Piegādātājs**.
+ **Integrācijas atslēgas:** klientu iesaistes programmu tabulās **Konts (klients)** **, Kontaktpersona** un **Piegādātājs** tiek izmantota iebūvētās integrācijas atslēgas. Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.
+ **Puses numurs:** visiem **jauninātajiem konta (klienta)**, **kontaktpersonas** un **piegādātāja** ierakstiem ir puses numurs. Ieraksti, kuriem nav puses numura, tiks ignorēti. Ja vēlaties jaunināt šos ierakstus, pievienojiet tiem puses numuru pirms jaunināšanas procesa sākšanas.
+ **Sistēmas darbības pārtraukums:** jaunināšanas procesa laikā jums būs jāņem gan finanšu un darbības vide, gan klientu piesaistes vide bezsaistē.
+ **Momentuzņēmums:** uzņemiet momentuzņēmumu gan finanšu un operāciju lietotnēs, gan klientu iesaistes lietotnēs. Pēc tam momentuzņēmumus var izmantot, lai atjaunotu iepriekšējo stāvokli, ja tas ir nepieciešams.

## <a name="deployment"></a>Izvietojums

1. Lejupielādējiet veidnes no [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Pierakstieties [Azure portālā](https://portal.azure.com/).
3. Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.
5. [Izveidot datu rūpnīcu](/azure/data-factory/quickstart-create-data-factory-portal) izveidotajā resursu grupā.
6. Atveriet datu rūpnīcu un atlasiet **elementu Autors un pārraugs**.
7. Cilnē **Pārvaldīt** atlasiet **ARM veidne**.
8. Atlasiet **Importēt ARM veidni**, lai importētu **puses** veidni.
9. Importējiet veidni datu fabrikā. Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.

    | Lauks | Vērtība |
    |---|---|
    | Abonements | Azure abonements |
    | Resursa grupa | Norādiet to pašu resursu, saskaņā ar kuru tiek izveidots krātuves konts. |
    | Reģions | Reģions |
    | Fabrikas nosaukums | Rūpnīcas nosaukums |
    | FO saistīta Pakalpojums_pakalpojums galvenā atslēga | Lietojumprogrammas atslēga |
    | Azure Blob krātuves_savienojuma virknes | Azure BLOB krātuves savienojuma virkne |
    | Dynamics CRM saistīta Pakalpojuma_parole | Tā lietotāja konta parole, kuru norādāt kā lietotājvārdu |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks | Informācija (domēna vārds vai nomnieka ID) par nomnieku, uz kuru atrodas jūsu pieteikums |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID | Lietojumprogrammas klienta ID |
    | Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds | Lietotājvārds, kas tiek izmantots, lai izveidotu savienojumu ar Dynamics 365 |

    Papildinformāciju skatiet tālāk norādītajās tēmās.

    - [Manuāli veicināt Resource Manager veidni katrai videi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Saistītie pakalpojuma rekvizīti](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopēt datus, izmantojot Azure datu ražotni](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.

    ![Datu kopas, datu plūsma un saistītais pakalpojums.](media/data-factory-validate.png)

11. Dodieties uz **Pārvaldīt**. Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**. Pēc tam atlasiet **DynamicsCrmLinkedService**. Dialoglodziņā **Saistītā pakalpojuma (Dynamics CRM)** rediģēšana ievadiet šādas vērtības.

    | Lauks | Vērtība |
    |---|---|
    | Nosaukums | Atlasiet DynamicsCrmLinkedService |
    | Apraksts | Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus |
    | Izveidot savienojumu, izmantojot integrācijas izpildlaiku | AutoResolvelntegrationRuntime |
    | Izvietošanas veids | Tiešsaiste |
    | Pakalpojuma Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentifikācijas veids | Office365 |
    | Lietotājvārds | |
    | Parole vai Azure Key Vault | Parole |
    | Parole | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Sagatavošanās datu rūpnīcas veidņu palaišanai

Šajā sadaļā ir aprakstīti iestatījumi, kas nepieciešami pirms pušu pasta adreses un pušu elektroniskās adreses datu rūpnīcas veidņu palaišanas.

### <a name="setup-to-run-the-party-postal-address-template"></a>Iestatījumi puses pasta adreses veidnes palaišanai

1. Piesakieties klientu iesaistes lietotnēs un dodieties uz **Iestatījumu** \> **personalizēšanas iestatījumi.** Pēc tam **cilnē Vispārīgi** konfigurējiet sistēmas administratora konta laika joslas iestatījumu. Laika joslai jābūt universālajā koordinētajā laikā (UTC), lai atjauninātu pasta adrešu datumus "derīgs no" un "derīgs līdz", izmantojot Finance and Operations lietotnes.

    ![Laika joslas iestatījums sistēmas administratora kontam.](media/ADF-1.png)

2. Datu fabrikas **cilnes Pārvaldība** sadaļā **Globālie parametri** izveidojiet šādu globālo parametru.

    | Numurs | Nosaukums | Veids | Vērtība |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | virkne | Šis parametrs jaunizveidotajām pasta adresēm pievieno sērijas numuru kā prefiksu. Noteikti norādiet virkni, kas nav pretrunā pasta adresēm Finance and Operations programmās un klientu iesaistes programmās. Piemēram, izmantojiet **ADF-PAD-**. |

    ![PastaAddressIdPrefix globālais parametrs, kas izveidots cilnē Pārvaldība.](media/ADF-2.png)

3. Kad esat pabeidzis, atlasiet **Publicēt visu**.

    ![Poga Publicēt visu.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Iestatījumi puses elektroniskās adreses veidnes palaišanai

1. Datu fabrikas **cilnes Pārvaldība** sadaļā **Globālie parametri** izveidojiet šādus globālos parametrus.

    | Numurs | Nosaukums | Veids | Vērtība |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Šis parametrs nosaka, kuras primārās sistēmas adreses tiek aizstātas konfliktu gadījumā. Ja vērtība ir **patiesa**, primārās adreses Finance and Operations lietojumprogrammās aizstās primārās adreses klientu iesaistes programmās. Ja vērtība ir **aplama**, primārās adreses klientu iesaistes programmās aizstās primārās adreses Finance and Operations lietojumprogrammās. |
    | 2 | ElectronicAddressIdPrefix | virkne | Šis parametrs jaunizveidotajām elektroniskajām adresēm pievieno sērijas numuru kā prefiksu. Noteikti nodrošiniet virkni, kas nav pretrunā ar elektroniskajām adresēm Finance and Operations programmās un klientu iesaistes programmās. Piemēram, izmantojiet **ADF-EAD-**. |

    ![Cilnē Manage ir izveidots ISFOSource un ElectronicAddressIdPrefix globālie parametri.](media/ADF-4.png)

2. Kad esat pabeidzis, atlasiet **Publicēt visu**.

## <a name="run-the-templates"></a>Veidņu palaišana

1. Apturiet šādas **konta**, **kontaktpersonas** un **piegādātāja** divrakstīšu kartes, kas izmanto programmu Finanses un operācijas:

    + Debitori V3 (konti)
    + Debitori V3 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + CDS kontaktpersonas V2 (kontaktpersonas)
    + Kreditors V2 (msdyn_vendor)

2. Pārliecinieties, vai kartes ir noņemtas **no tabulas msdy_dualwriteruntimeconfig** programmā Dataverse.
3. Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.
4. Programmā Finanses un operācijas palaidiet **Sākotnējo sinhronizāciju** šādām tabulām, ja tajās ir dati:

    + Uzrunas
    + Personas rakstura veidi
    + Komplimentāra slēgšana
    + Kontaktpersonu amati
    + Lēmumu pieņemšanas lomas
    + Lojalitātes programmu līmeņi

5. Klientu piesaistes lietotnē atspējojiet šādas spraudņa darbības:

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

    + Customeraddress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Customeraddress izveide

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Customeraddress atjaunināšana

        + Dzēst

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Customeraddress dzēšana

    + msdyn_partypostaladdress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress izveide
            + Microsoft.Dynamics.GABPaplašinātie.plugins.PartyPostalAddress: msdyn_partypostaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress atjaunināšana
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress atjauninājums

    + msdyn_postaladdress

        + Izveidot

            + Microsoft.Dynamics.GABPaplašinātie.Plugins.PostalAddress: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress izveide
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABPaplašinātie.plugins.PostalAddressUpdate: msdyn_postaladdress atjaunināšana
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress atjaunināšana

    + msdyn_partyelectronicaddress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress izveide

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress atjaunināšana

        + Dzēst

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

6. Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

7. Datu rūpnīcā palaidiet veidni, atlasot **Trigeris tūlīt**, kā parādīts nākamajā attēlā. Atkarībā no datu apjoma šī procesa pabeigšana var ilgt dažas stundas.

    ![Veidnes palaišana.](media/data-factory-trigger.png)

    > [!NOTE]
    > Ja jums ir pielāgojumi **Konts**, **·**, un **Pārdevējs**, jums ir jāmaina veidne.

8. Importējiet jauno **Ballīte** ierakstus lietotnē Finance and Operations.

    1. Lejupielādēt **FONewParty.csv** failu no Azure Blob krātuves. Ceļš ir **partybootstrapping/output/FONewParty.csv**.
    2. Konvertēt **FONewParty.csv** failu Excel failā un importējiet Excel failu programmā Finance and Operations. Vai arī, ja CSV importēšana darbojas jūsu labā, varat importēt .csv failu tieši. Atkarībā no datu apjoma šī darbība var ilgt dažas stundas. Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).

    ![Importējot Dataverse Partiju rekordi.](media/data-factory-import-party.png)

9. Datu rūpnīcā vienu pēc otras palaidiet partijas pasta adreses un partijas elektroniskās adreses veidnes.

    + Puses pasta adreses veidne atceļ visus pasta adrešu ierakstus klientu iesaistīšanas lietotnē un saista tos ar atbilstošo **Konts**, **·**, un **Pārdevējs** ieraksti. Tas arī ģenerē trīs .csv failus: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv un ImportFONewPostalAddress.csv.
    + Puses elektroniskās adreses veidne pievieno visas elektroniskās adreses klientu iesaistīšanas lietotnē un saista tās ar atbilstošām **Konts**, **·**, un **Pārdevējs** ieraksti. Tas arī ģenerē vienu .csv failu: ImportFONewElectronicAddress.csv.

    ![Partijas pasta adreses un partijas elektroniskās adreses veidņu palaišana.](media/ADF-7.png)

10. Lai atjauninātu programmu Finance and Operations ar šiem datiem, jums ir jāpārveido .csv faili Excel darbgrāmatā un [importējiet to programmā Finance and Operations](/data-entities/data-import-export-job). Vai arī, ja CSV importēšana darbojas jūsu labā, varat importēt .csv failus tieši. Atkarībā no skaļuma šī darbība var ilgt dažas stundas.

    ![Veiksmīga importēšana.](media/ADF-8.png)

11. Klientu iesaistīšanas lietotnē iespējojiet tālāk norādītās spraudņa darbības.

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

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress izveide
            + Microsoft.Dynamics.GABPaplašinātie.plugins.PartyPostalAddress: msdyn_partypostaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress atjaunināšana
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress atjauninājums

    + msdyn_postaladdress

        + Izveidot

            + Microsoft.Dynamics.GABPaplašinātie.Plugins.PostalAddress: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress izveide
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress

        + Atjaunināšana

            + Microsoft.Dynamics.GABPaplašinātie.plugins.PostalAddressUpdate: msdyn_postaladdress atjaunināšana
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress atjaunināšana
 
    + msdyn_partyelectronicaddress

        + Izveidot

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress izveide

        + Atjaunināšana

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress atjaunināšana

        + Dzēst

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

12. Klientu iesaistīšanas lietotnē aktivizējiet tālāk norādītās darbplūsmas, ja tās iepriekš esat deaktivizējis.

    + Kreditoru izveide kontu tabulā
    + Kreditoru izveide kontu tabulā
    + Izveidot kreditorus ar veidu persona kontaktpersonu tabulā
    + Izveidot kreditorus ar veidu Persona kreditoru tabulā
    + Kreditoru atjaunināšana kontu tabulā
    + Kreditoru atjaunināšana kreditoru tabulā
    + Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
    + Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

13. Palaidiet **Ballīte** ar ierakstiem saistītas kartes, kā aprakstīts [Partiju un globālā adrešu grāmata](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Datu fabrikas veidņu skaidrojums

Šajā sadaļā ir aprakstītas darbības katrā Data Factory veidnē.

### <a name="steps-in-the-party-template"></a>Darbības ballītes veidnē

1. 1.–6. darbībā tiek identificēti uzņēmumi, kuriem ir iespējota dubultā rakstīšana, un tiem tiek izveidota filtra klauzula.
2. Veicot 7.-1. līdz 7.-9. darbību, tiek izgūti dati gan no lietotnes Finance and Operations, gan no klientu iesaistīšanas lietotnes, un tiek sagatavoti šie dati jaunināšanai.
3. 8.–9. darbībā salīdziniet partijas numuru **Konts**, **·**, un **Pārdevējs** ieraksti starp lietotni Finance and Operations un klientu piesaistes lietotni. Visi ieraksti, kuriem nav partijas numura, tiek izlaisti.
4. 10. darbībā tiek ģenerēti divi .csv faili puses ierakstiem, kas jāizveido klientu iesaistīšanas lietotnē un programmā Finance and Operations.

    - **FOCDSParty.csv** – Šajā failā ir visi abu sistēmu pušu ieraksti neatkarīgi no tā, vai uzņēmumam ir iespējota dubultā rakstīšana.
    - **FONewParty.csv** – Šajā failā ir ietverta partijas ierakstu apakškopa, kas Dataverse ir informēts par (piemēram, kontiem par **Izredzes** veids).

5. 11. darbībā tiek izveidotas puses klientu iesaistīšanas lietotnē.
6. 12. darbībā tiek izgūti pušu globāli unikālie identifikatori (GUID) no klientu iesaistīšanas lietotnes un sakārtoti tie, lai tos varētu saistīt ar **Konts**, **·**, un **Pārdevējs** ierakstus turpmākajās darbībās.
7. 13. darbība ir saistīta ar **Konts**, **·**, un **Pārdevējs** ieraksti ar partiju GUID.
8. Darbības 14-1 līdz 14-3 atjauniniet **Konts**, **·**, un **Pārdevējs** ieraksti klientu iesaistīšanas lietotnē ar pušu GUID.
9. Sagatavojiet 15.-1. līdz 15.-3. darbību **Sazinieties ar ballīti** ieraksti par **Konts**, **·**, un **Pārdevējs** ieraksti.
10. No 16-1. līdz 16.-7. darbībai izgūstiet atsauces datus, piemēram, sveicienus un personīgo rakstzīmju tipus, un saistiet tos ar **Sazinieties ar ballīti** ieraksti.
11. 17. darbība apvieno **Sazinieties ar ballīti** ieraksti par **Konts**, **·**, un **Pārdevējs** ieraksti.
12. 18. darbība importē **Sazinieties ar ballīti** ierakstus klientu iesaistīšanas lietotnē.

### <a name="steps-in-the-party-postal-address-template"></a>Darbības partijas pasta adreses veidnē

1. No 1. līdz 1. darbībai līdz 1. līdz 10. darbībai tiek izgūti dati gan no lietotnes Finance and Operations, gan no klientu iesaistīšanas lietotnes un pakāpeniski šie dati tiek atjaunināti.
2. 2. darbībā tiek denormalizēti pasta adreses dati lietotnē Finance and Operations, savienojot pasta adresi un partijas pasta adresi.
3. 3. darbībā tiek noņemti un apvienoti konta, kontaktpersonas un piegādātāja adreses dati no klientu iesaistīšanas lietotnes.
4. 4. darbībā tiek izveidoti .csv faili programmai Finance and Operations, lai izveidotu jaunus adrešu datus, kuru pamatā ir konta, kontaktpersonas un piegādātāja adreses.
5. 1. darbībā tiek izveidoti .csv faili klientu iesaistīšanas lietotnei, lai izveidotu visus adrešu datus, pamatojoties gan uz programmu Finance and Operations, gan uz klientu piesaistes lietotni.
6. 5-2. darbība pārvērš .csv failus Finance and Operations importēšanas formātā manuālai importēšanai.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 6. darbībā pasta adrešu apkopošanas dati tiek importēti klientu iesaistīšanas lietotnē.
8. Veicot 7. darbību, tiek izgūti pasta adrešu apkopošanas dati no klientu iesaistīšanas lietotnes.
9. 8. darbībā tiek izveidoti klienta adreses dati un tiek piesaistīts pasta adrešu vākšanas ID.
10. Darbība 9-1 līdz 9-2 saistīto pušu un pasta adrešu vākšanas ID ar pasta adresēm un partijas pasta adresēm.
11. No 1. līdz 3. darbībai importējiet klientu adreses, pasta adreses un pušu pasta adreses klientu iesaistīšanas lietotnē.

### <a name="steps-in-the-party-electronic-address-template"></a>Darbības partijas elektroniskās adreses veidnē

1. No 1.–1. līdz 1.–5. darbībai tiek izgūti dati gan no lietotnes Finance and Operations, gan no klientu iesaistīšanas lietotnes, un pakāpeniski sagatavojiet šos datus jaunināšanai.
2. 2. darbībā tiek konsolidētas elektroniskās adreses klientu iesaistīšanas lietotnē no konta, kontaktpersonas un piegādātāja entītijām.
3. 3. darbībā tiek apvienoti primārie elektroniskās adreses dati no klientu iesaistīšanas lietotnes un programmas Finance and Operations.
4. 4. darbībā tiek izveidoti .csv faili.

    - Izveidojiet jaunus elektroniskās adreses datus programmai Finance and Operations, pamatojoties uz kontu, kontaktpersonu un piegādātāju adresēm.
    - Izveidojiet jaunus elektroniskās adreses datus klientu piesaistes lietotnei, pamatojoties uz elektroniskās adreses, konta, kontaktpersonas un piegādātāja adresēm programmā Finance and Operations.

5. 5-1. darbība importē elektroniskās adreses klientu iesaistīšanas lietotnē.
6. 5.–2. darbībā tiek izveidoti .csv faili, lai klientu iesaistīšanas lietotnē atjauninātu kontu un kontaktpersonu primārās adreses.
7. 6.-1. līdz 6.-2. darbība. Importējiet kontus un sazinieties ar primārajām adresēm klientu iesaistīšanas lietotnē.

## <a name="troubleshooting"></a>Problēmu novēršana

1. Ja process neizdodas, atkārtoti palaidiet datu rūpnīcu. Sāciet no neveiksmīgās darbības.
2. Datu validācijai var izmantot dažus datu rūpnīcas ģenerētos failus.
3. Datu rūpnīca darbojas, pamatojoties uz .csv failiem. Tāpēc, ja kādā lauka vērtībā ir iekļauts komats, tas var traucēt rezultātiem. No lauka vērtībām ir jānoņem visi komats.
4. The **Uzraudzība** cilne sniedz informāciju par visām darbībām un datiem, kas ir apstrādāti. Atlasiet noteiktu darbību, lai to atkļūdotu.

    ![Cilne Pārraudzība.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Uzziniet vairāk par veidni

Papildinformāciju par veidni skatiet [Komentāri par Azure Data Factory veidni readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
