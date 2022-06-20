---
title: Iestatiet itālijas FatturaPA tiešo integrāciju ar SDI
description: Šajā rakstā sniegta informācija, kas palīdzēs jums uzsākt elektronisko rēķinu izrakstīšanu Itālijai un iestatīt tiešo Itālijas FatturaPA integrāciju ar Apmaiņas sistēmu (SDI).
author: abaryshnikov
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 510cf05e7bbc925478f9a1a4ea2ea27fe397c570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853197"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Iestatiet itālijas FatturaPA tiešo integrāciju ar SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektroniskā rēķinu izrakstīšana Itālijai pašlaik neatbalsta visas funkcijas, kas ir pieejamas elektroniskajiem rēķiniem Microsoft Dynamics 365 Finanses un Dynamics 365 Supply Chain Management.

Šajā rakstā sniegta informācija, kas jums palīdzēs uzsākt elektronisko rēķinu izrakstīšanu Itālijai finanšu un piegādes ķēžu pārvaldībā. Tas jūs vadīs caur konfigurācijas soļiem, kas ir atkarīgi no valsts/reģiona regulēšanas konfigurācijas pakalpojumos (RCS). Šīs darbības papildina darbības, kas aprakstītas sadaļā Sākt [darbu ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms šajā rakstā norādīto darbību veikšanas ir jāizpilda šādi priekšnosacījumi:

- Veiciet darbības, kas soļi [sadaļā Sākt darbu ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).
- Importējiet **Itālijas FatturaPA (IT) elektronisko** rēķinu izrakstīšanas līdzekli RCS no globālā repozitorija. Plašāku informāciju skatiet [sadaļas "Sākt darbu ar elektronisko rēķinu izrakstīšanu" sadaļā Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) konfigurācijas nodrošinātājs, kas atrodas sadaļā "Sākt darbu ar elektronisko rēķinu izrakstīšanu".
- Pievienojiet pakalpojumu videi saites no nepieciešamajiem sertifikātiem. Nepieciešamais sertifikāts ietver ciparparaksta sertifikātu, sertifikāta iestādi (CA) sertifikātu un klientu sertifikātu. Papildinformāciju skatiet sadaļas ["Sākt ar elektronisko](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) rēķinu izrakstīšanas pakalpojumu administrāciju" sadaļā "Sākt darbu ar elektronisko rēķinu izrakstīšanas pakalpojuma administrēšanu".

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Valstij raksturīgā konfigurācija Itālijas FatturaPA (IT) elektronisko rēķinu izrakstīšanas līdzeklim

Pirms programmatūras izvietošanas pievienotajā Finanšu vai piegādes ķēžu pārvaldības programmā veiciet tālāk norādītās procedūras.

Šī sadaļa papildina sadaļas ["Sākt](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) darbu ar elektronisko rēķinu izrakstīšanu" sadaļā Pieteikuma iestatījumi, kas attiecas uz konkrētu valsti.

### <a name="create-a-new-feature"></a>Izveidot jaunu līdzekli

1. Pierakstieties RCS.
2. Elektronisko pārskatu **izveides** darbvietā sadaļā Konfigurācijas **nodrošinātāji** atzīmējiet jūsu uzņēmuma konfigurācijas nodrošinātāju kā aktīvu.
3. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
4. Lapā Elektronisko **rēķinu izrakstīšanas līdzekļi** atlasiet **Pievienot** \> **, balstoties uz esošo līdzekli.**
5. Zem **Microsoft konfigurācijas nodrošinātājs** atlasiet **Itālijas FatturaPA (IT)** kā pamatlīdzekļa nosaukumu, ievadiet nosaukumu un pēc tam atlasiet **Izveidot funkciju**.

### <a name="set-up-application-specific-parameters"></a>Programmai raksturīgu parametru iestatīšana

1. Elektronisko rēķinu **izrakstīšanas funkciju** lapā izvēlieties rediģējamo līdzekli.
2. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
3. Cilnē Konfigurācijas **atlasiet** konfigurāciju un pēc tam atlasiet Programmas specifiskie **parametri**.
4. Informācijas iegūšanas **sadaļā** pārliecinieties, ka ir **atlasīta uzmeklēšanu Kolonnu apgriezto** maksu apakškategorijas.
5. Sadaļā Nosacījumi **atlasiet** **Pievienot**.
6. Pievienojiet katrai sistēmā definētai apakškategorijai specifiskus nosacījumus un pēc tam saglabājiet izmaiņas.

    > [!NOTE]
    > Kolonnā Nosaukums **noteiktas** vērtības vietā varat atlasīt **\* vērtību Tukšs\*** **\*\*** vai Nav tukšs vietturis.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigurēt eksporta apstrādes konveijeru

1. Elektronisko rēķinu **izrakstīšanas funkciju** lapā izvēlieties rediģējamo līdzekli.
2. Cilnē Iestatījumi **atlasiet** Pārdošanas rēķini **un pēc** tam atlasiet **Rediģēt**.
3. Sadaļā Konveijera **apstrāde** dodieties cauri darbībām un iestatiet visus nepieciešamos laukus:

    - Parakstīšanas **dokumenta** darbībai laukā **Sertifikāta nosaukums** norādiet ciparparaksta sertifikātu.
    - Lai iesniegtu darbību, iestatiet url **adreses un** **sertifikātu laukus**.**·** Lauka Sertifikāti **vērtība** ir sertifikātu ķēde, no kuras pirmais ir saknes CA sertifikāts (caentrate.cer), un otrais no tiem ir Klienta sertifikāts.

4. Atlasiet **Pārbaudīt,** lai pārliecinātos, ka visi obligātie lauki ir iestatīti.
5. Saglabājiet izmaiņas un aizveriet lapu.
6. Cilnē Iestatījumi **atlasiet** Projekta rēķini **un pēc** tam atlasiet **Rediģēt**.
7. Atkārtojiet soļus no 3. līdz 5. projekta rēķiniem.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigurēt konveijera apstrādi importēšanai

1. Elektronisko rēķinu **izrakstīšanas funkciju** lapā izvēlieties rediģējamo līdzekli.
2. Cilnē Iestatījumi **atlasiet** Importēt rēķinus **un pēc** tam atlasiet **Rediģēt**.
3. **Datu kanāla sadaļas** cilnē **Parametri**, laukā **Datu** kanāls ievadiet virknes vērtību.
4. Cilnē Piemērojamības **noteikumi** iestatiet iestatījuma laukus. Varat lietot noklusēto klauzulu **Kanāls**, nododot **vērtību**, kas iepriekšējā solī iestatīta datu kanāla laukam, uz **lauku** Vērtība.

    ![Piemērojamības noteikumu iestatīšanu;](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Atlasiet **Pārbaudīt,** lai pārliecinātos, ka visi obligātie lauki ir iestatīti.

### <a name="deploy-the-feature"></a>Izvietot līdzekli

1. Pabeidziet, publicējiet un izvietojiet šo līdzekli pakalpojumu vidē. Papildinformāciju skatiet [sadaļas](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) "Sākt darbu ar elektronisko rēķinu izrakstīšanu" sadaļā "Sākt darbu ar elektronisko rēķinu izrakstīšanu".
2. Izvietojiet līdzekli pievienotajā programmā. Papildinformāciju skatiet [sadaļas](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) "Sākt darbu ar elektronisko rēķinu izrakstīšanu" sadaļā "Sākt darbu ar elektronisko rēķinu izrakstīšanu".

### <a name="set-up-finance"></a>Iestatīt finanses

1. Piesakieties savā finanšu vidē.
2. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
3. Atlasiet **globāli atvērtus reposiries** \> **·** \> **·**.
4. Atlasiet un importējiet **debitora rēķina konteksta modeli** un **kreditora rēķina importa (IT)** konfigurācijas.
5. Dodieties uz **Organizācijas administrēšana** \> **Iestatījumi** \> **Elektronisko dokumentu parametri**.
6. Cilnē Līdzekļi **atrodiet** un atlasiet Itāliešu elektroniskā rēķina **līdzekli** un pēc tam atzīmējiet izvēles **rūtiņu** Iespējot.
7. Cilnē Elektronisks **dokuments** pārliecinieties, vai lauki **debitoru** **rēķinu** žurnālam un projekta rēķinam ir iestatīti saskaņā ar informāciju, kas atrodas [Konfigurēt programmas iestatījumus.](e-invoicing-get-started.md#configure-the-application-setup)

### <a name="set-up-vendor-invoice-import"></a>Iestatīt kreditora rēķinu importu 

1. Finanšu sadaļas Elektronisko **pārskatu izveide** sadaļā Konfigurācijas nodrošinātāji **atzīmējiet** jūsu uzņēmuma konfigurācijas nodrošinātāju kā aktīvu.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Atlasiet **debitora rēķina konteksta modeli** un pēc tam atlasiet **Izveidot konfigurāciju**.
4. Atlasiet **Atvasināt no nosaukuma: debitora rēķina konteksts, Microsoft**, lai izveidotu atvasinātu konfigurāciju.
5. Melnraksta **versijā** atlasiet **Veidotājs**.
6. Datu modeļa **kokā** atlasiet Kartēt **modeli ar datu avotu**.
7. Definīciju kokā atlasiet DataChannel un **pēc tam atlasiet Veidotājs** **.** **·**
8. Datu avotu **kokā** paplašiniet konteksta **\$ kanāla\_ konteineru**.
9. Laukā **Vērtība** atlasiet **Rediģēt**. 
10. Ievadiet datu kanāla nosaukumu. Nosaukumam jābūt ne vairāk kā 10 rakstzīmēm. Tam ir jāatbilst datu kanāla **datu kanāla** vērtībai elektronisko rēķinu izrakstīšanas līdzeklim RCS.
11. Saglabājiet izmaiņas un pēc tam atveriet pārskatu **konfigurācijas pilna konfigurācijas** \> **versija.**
12. **Cilnes Ārējie kanāli** sadaļā **Kanāli** atlasiet **Pievienot**.
13. **Kanāla laukā** ievadiet konteksta **\$ kanāla** vērtību.
14. Ievadiet vērtības **laukos Apraksts** un **Uzņēmums**.
15. Dokumenta konteksta **laukā** atlasiet jauno konfigurāciju, kas atvasināta no **debitora rēķina konteksta modeļa**. Kartējuma aprakstam vajadzētu būt **Datu kanāla konteksts**.
16. Cilnē Importēt **avotus** atlasiet Pievienot **un** pēc tam iestatiet šādas vērtības:

    - **Nosaukums:** OutputFile
    - **Datu elementa nosaukums:** kreditora rēķina virsraksts (**datu elements:** VendorInvoiceHeaderEntity)
    - **Modeļa kartēšana:** kreditora rēķina imports (IT)

> [!NOTE]
> Ja ir importēti kreditora rēķini no dažādiem avotiem, jūs varat izveidot vairākus ārējos kanālus un vairākas atvasinātās konfigurācijas ar atšķirīgām konteksta **\$ kanāla** vērtībām. Piemēram, varat vēlēties importēt kreditora rēķinus dažādām juridiskajām personām.

## <a name="proxy-server-setup"></a>Starpniekservera iestatīšana

Šajā sadaļā ir sniegta informācija, kas palīdzēs jums iestatīt un konfigurēt starpniekservera pakalpojumu sakariem starp Apmaiņas sistēmu (SDI) un Elektronisko rēķinu izrakstīšanas pakalpojumu.

### <a name="create-an-app-registration"></a>Izveidot programmas reģistrāciju

1. Izmantojiet tālāk norādīto Windows PowerShell skriptu, lai izveidotu paš parakstītu sertifikātu pakalpojuma-pakalpojuma (S2S) autentifikācijai.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Saglabājiet .pfx sertifikāta failu atslēgas izpildē un pēc tam dzēsiet lokālo kopiju.
3. Piesakieties [Azure portālā](https://portal.azure.com) kā administrators.
4. Izveidot programmas reģistrāciju SDI starpniekservera pakalpojumam.

    1. Dodieties **uz programmu** reģistrācijām, izveidojiet reģistrāciju un pēc tam iestatiet tai tālāk norādītās vērtības.

        - **Nosaukums:** SDI starpniekservera klients
        - **Atbalstītie kontu tipi:** konti tikai šajā organizācijas direktorijā (viens nomnieks)

    2. Atlasiet **reģistru** un pēc tam atlasiet tikko izveidoto programmas reģistrāciju.
    3. Dodieties uz **API atļaujām** un atlasiet **Piešķirt administratora atļauju**.
    4. Pārejiet uz **sertifikātiem > noslēpumiem,** **atlasiet Augšupielādes** sertifikāts un augšupielādējiet .cer sertifikāta failu S2S autentifikācijai.
    5. Dodieties uz **uzņēmuma** programmām un atlasiet izveidoto programmu.
    6. Saglabājiet **programmas ID** (klienta ID) **un objekta ID** vērtības programmai.
    7. Rēķinu izrakstīšanas pakalpojuma komandai jāpiešķir programmas piekļuve pakalpojumam. Nosūtīt šādu parametru vērtības uz <D365EInvoiceSupport@microsoft.com>:

        - AAD nomnieka ID
        - LCS vides ID
        - Lietojumprogrammas ID
        - Objekta ID

5. RCS pievienojiet programmu jūsu pakalpojumu vides programmu sarakstam.

    1. Dodieties uz **globalizācijas** \> **funkciju Vides** \> **Elektronisko rēķinu izrakstīšanas** \> **pakalpojuma vides** un atlasiet jūsu vidi.
    2. **Sadaļā Pieteikumi** pievienojiet režģim rindu un ievadiet programmas nosaukumu un objekta ID.

        ![Programmas pievienošana pakalpojumu videi.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Atlasiet **Saglabāt** un pēc tam atlasiet **Publicēt**.

### <a name="create-an-azure-virtual-machine"></a>Azure virtuālās mašīnas izveide

1. Azure portālā [dodieties](https://portal.azure.com) uz Virtuālās **mašīnas** un atlasiet **Izveidot jaunu**.
2. Cilnē Pamata **atlasiet** abonementa un resursu grupu. Vērtībām vajadzētu būt abonementa un resursu grupai, kur atrodas jūsu atslēgas Krātuve un BLOB krātuve.
3. Atlasiet reģionu. Šai vērtībai ir jābūt reģionam, kurā ir izvietota finanšu vide.
4. Pievienojiet administratora lietotājvārdu un paroli un saglabājiet tos atslēgas krātuvē.
5. Laukā **Atlasīt ienākošo pieprasījumu portus** atlasiet **HTTPS (443)** un **RPD (3389)**.

    > [!NOTE]
    > Ieteicams atspējot RDP **(3389)** portu, ja sistēma iet uz ražošanu. To var aktivizēt atkārtoti, ja problēmu novēršanas nolūkiem ir jāizveido savienojums ar virtuālo mašīnu (VM).

    ![Lauku iestatīšana pamata cilnē, lai izveidotu Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Cilnes Diski **kopsavilkuma** cilnē Papildu **atlasiet** izvēles rūtiņu Izmantot pārvaldītos **diskos**. Atstājiet **ešimīālu OS disk izvēles** rūtiņu notīrītu.

    ![Lauku iestatīšana cilnē Diski, lai izveidotu Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. **Cilnes Vispārīgi** laukā Publiskais **IP** atlasiet Izveidot **jaunu**.

    ![Iestata laukus cilnē Abonements, lai izveidotu Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. **Valsts IP adreses izveides** dialoglodziņa SKU **lauku** grupā atlasiet **standarta** opciju. Lauku grupā **Piešķire** atlasiet opciju **Statisks**.

    ![Tiek radīta publiskā IP adrese.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Cilnē Pārvaldība **notīriet** izvēles rūtiņu **Automātiska izslēgšana**, lai deaktivizētu automātisko izslēgšanu.
10. Iestatiet viesa **OS atjauninājumu lauku** uz Manuāli **un** pēc tam iestatiet visas citas politikas.
11. Pārskatiet un izveidojiet VM.
12. Jaunajā VM dodieties uz piešķirto **identitātes** \> **sistēmu** un iestatiet statusa opciju **Uz**.**·**
13. Piešķirt VM piekļuvi atslēgai.

    1. Produkta atslēgas vietā dodieties uz lomu **piešķirēm Piekļuve kontrolei (IAM** \> **·**).
    2. Atlasiet **Pievienot lomu piešķiri** un pēc tam iestatiet šādus laukus:

        1. Laukā Loma **norādiet** Atslēgas **Noslēpumu lietotājs**.
        2. Laukā **Piešķirt piekļuvi** norādiet Virtuālā **mašīna**.
        3. Laukā **Abonements** norādiet savu abonementu.
        4. Laukā **Atlasīt** norādiet savu VM.

    3. Dodieties uz **piekļuves politikām**.
    4. Atlasiet **Pievienot piekļuves politiku** un pēc tam iestatiet šādus laukus:

        1. Laukā **Atlasītais** galvenais izvēlieties savu VM.
        2. Sadaļā Sertifikāts **atlasiet** Sarakstu **un** Iegūstiet **atļaujas**.

14. Azure portālā [atveriet](https://portal.azure.com) publiskās **IP adreses** un atlasiet VM izveidoto IP adresi.
15. Dodieties **uz** Konfigurāciju un iestatiet Domēna nosaukuma sistēmas (DNS) nosaukumu.

### <a name="prepare-the-proxy-service-environment"></a>Starpniekservera pakalpojumu vides sagatavošana

Veiciet šīs darbības datorā, kur tiek viesots starpniekservera pakalpojums.

1. Pievienojieties VM, izmantojot Attālās darbvirsmas savienojumu.
2. Atveriet lokālā datora sertifikāta papildprogrammu. Papildinformāciju skatiet šeit [: Kā skatīt sertifikātus ar MMC pieķeršanos](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Importējiet **ražošanas caentrate.cer** sertifikātu un **CAEntratetest.cer** testēšanai uzticamo [saknes sertifikācijas iestāžu krātuvē](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** ir saknes CA sertifikāts, ko sniedza iestāde.)
4. Vadības panelī atveriet **ieslēgšanu vai izslēgšanas Windows** **·** \> **līdzekļus vai dodieties uz servera pārvaldniekam pievienot lomas** un līdzekļus servera operētājsistēmai (OS), un slēdziet interneta informācijas pakalpojumu (IIS) līdzekļus:

    - Tīmekļa pārvaldības rīki
        - IIS pārvaldības konsolēms
    - Interneta web pakalpojumi
        - Programmas izstrādes funkcijas
            - .NET paplašināmība 4.7 (vai 4.8)
            - ASP
            - ASP.NET 4.7 (vai 4.8)
            - CGI
            - ISAPI paplašinājumi
            - ISAPI filtri
        - Parastās HTTP funkcijas
            - Noklusējuma dokuments
            - Direktorija pārlūkošana
            - HTTP kļūdas
            - Statisks saturs
        - Veselības un diagnostika
            - HTTP reģistrēšana
            - Trasēšana
        - Veiktspējas līdzekļi
            - Statiskā satura saspiešana
        - Drošība
            - Pieprasījumu filtrēšana

    ![IIS funkciju ieslēdzšana.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Iestatīt SDI starpniekservera pakalpojumu IIS

1. Sadaļā Microsoft Dynamics Lifecycle Services (LCS) dodieties uz kopīgoto līdzekļu bibliotēku un atlasiet **datu pakotni** kā līdzekļu tipu.
2. Atrodiet **elektronisko rēķinu izrakstīšanas pakalpojuma Sdi starpnieku** un lejupielādējiet to VM.
3. Konfigurējiet pakalpojumu.

    1. Izņemiet lejupielādēto **Elektronisko rēķinu izrakstīšanas pakalpojuma Sdi** starpniekservera arhīva mapi.
    2. **Mapē src\\ FattureService** atveriet **appsettings.json** failu un iestatiet šādus parametrus:

        - **KeyVaultUri** - norādiet atslēgas adresi, kas glabā rēķina izrakstīšanas pakalpojuma klienta sertifikātu.
        - **TenantId** – norādiet debitora nomnieka globāli unikālo identifikatoru (GUID).
        - **EnvironmentId** - norādiet LCS vides ID.
        - **ClientId** — norādiet starpposma pakalpojumu programmas reģistrācijas programmas ID debitora nomniekā.
        - **ClientCertificateName** – atslēgas komplektā norādiet S2S sertifikāta nosaukumu.
        - **SecurityServiceClientOptions.Endpoint** – norādiet drošības pakalpojuma URL.
        - **SecurityServiceClientOptions.Resurss** – norādiet, kuriem tvēruma iestatījumiem jāiegūst marķieris.
        - **InvoicingServiceClientOptions.Endpoint** – norādiet rēķinu izrakstīšanas pakalpojuma galapunktu. Šai vērtībai jābūt tam pašam galapunktam, kas tiek izmantots RCS un Finanses.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** — norādiet pakalpojumu vides nosaukumu. Šai vērtībai ir jābūt jūsu Finanšu vides nosaukumam.
        - **NotificationsFolder** – norādiet mapi, kurā saglabāt ienākošo paziņojumu failus.

    3. **Failā web.config** atrodiet norādīto rindu un pievienojiet starpniekservera sertifikāta īssavilkumu.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Kad sistēma iet uz ražošanu, jūs varat mainīt dažas vērtības failā web.config, lai palīdzētu samazināt apkopotās žurnāla informācijas daudzumu un palīdzētu ietaupīt vietu diskā. Zarā **\<system.diagnostics\>\<source\>** mainiet switchValue vērtību **uz** Kritiska,Kļūda **·**. Papildinformāciju skatiet MS pakalpojuma [izsekošanas skatītājā](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Atveriet IIS pārvaldnieku. Kreisajā kokā paliek saknes zarā. Labajā pusē atlasiet **Servera sertifikāti**.

    ![PAKALPOJUMA sertifikātu atlase IIS pārvaldniekā.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Atveriet izvēlni un atlasiet **Importēt**.
6. Dialoglodziņa Importēt **sertifikātu** laukā **Sertifikāta fails (.pfx)** norādiet .pfx faila ceļu starpniekservera sertifikātam.

    ![Tiek norādīts starpniekservera pakalpojuma sertifikāta fails.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) **vietnes** un pēc tam atlasiet Pievienot **vietni**.
8. **Dialoglodziņa Pievienot vietni** laukā Vietnes **nosaukums** ievadiet vietnes nosaukumu.
9. Laukā **Fiziskais** ceļš norādiet uz mapi **src\\ FattureService**.
10. Laukā **Saistīšanas** tips atlasiet **https**.
11. Laukā **Resursdatora** nosaukums norādiet resursdatora nosaukumu.
12. Atstājiet **IP adreses un** porta **laukus** iestatīt uz noklusējuma vērtībām.
13. Pārliecinieties, ka **izvēles rūtiņa Pieprasīt** servera nosaukuma norādīšanu ir notīrīta, jo SDI neatbalsta šo tehnoloģiju.
14. Laukā **SSL sertifikāts** atlasiet importēto starpniekservera sertifikātu.
15. Laukā **Programmu pūls** norādiet vietai kopu un atzīmējiet tās nosaukumu (piemēram, **SdiAppPool**).

    ![Tiek pievienošana vietnei.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Kad tīmekļa vietnes izveide pabeigta, atveriet izvēlni SSL **iestatījumiem**.

    ![Atver izvēlni SSL iestatījumiem.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Atzīmējiet **izvēles rūtiņu Pieprasīt SSL** un pēc tam **lauku** grupā Klienta sertifikāti atlasiet opciju **Pieprasīt**.

    ![SSL iestatījumu konfigurēšana.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Atveriet **Direktorija pārlūku un** izvēlieties **Aktivizēt**.
19. Jebkurā tīmekļa pārlūkprogrammā dodieties uz **failu serverDNS/TrasmissioneFatture.svc**. Par pakalpojumu ir jāparādās standarta lapai.

    ![Pārbauda pakalpojumu pārlūkprogrammā.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Izveidojiet šādas mapes, kur glabāt žurnālus un failus:

    - **C:\\ Žurnāli\\** - Saglabā šeit žurnāla failus. Šos failus var skatīt MS Service [Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\ Faili\\** - Glabājiet visus atbilžu failus šeit.

21. Programmā File Explorer piešķiriet **TĪKLA pakalpojumu un** **IIS AppPool\\ SdiAppPool** (**vai IIS AppPool\\ DefaultAppPool**, ja izmantojat noklusējuma pūlu) **piekļuvi žurnāliem** **un failu mapēm**.

    1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) uz vienas no mapēm, un pēc tam atlasiet **Rekvizīti**.
    2. Dialoglodziņa Rekvizīti **cilnē Drošība** **atlasiet Rediģēt**.**·**
    3. Pievienojiet lietotājus, ja tie nav uzskaitīti.
    4. Atkārtojiet 1. līdz 3. soli citai mapei.

    ![Notiek atļauju pievienošana pakalpojuma lietotājam.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti 

Itālijas elektroniskā **rēķina funkcijas iespējošanai** var būt nepieciešams, lai tiktu nosūtīti ierobežoti dati. Šie dati ietver organizācijas nodokļu reģistrācijas ID. Administrators var aktivizēt un deaktivizēt Itālijas elektroniskā rēķina funkciju. Lai atspējotu šo līdzekli, sekojiet šiem soļiem.

1. Dodieties uz **Organizācijas administrēšana** \> **Iestatījumi** \> **Elektronisko dokumentu parametri**.
2. Cilnē Līdzekļi **atlasiet** rindas, kas satur Itālijas elektroniskā **rēķina** līdzekli, un pēc tam atlasiet Deaktivizēt **tūlīt**.

Uz datiem, kas no šīm ārējām sistēmām tiek importēti šajā Dynamics 365 tiešsaistes pakalpojumā, attiecas mūsu paziņojums par [konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=512132). Papildinformāciju skatiet sadaļā "Paziņojums par konfidencialitāti", kas atrodas funkcionalitātes dokumentācijā, kas attiecas uz valsti/reģionu.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveidi](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
