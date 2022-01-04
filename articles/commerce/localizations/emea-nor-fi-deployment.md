---
title: Izvietošanas vadlīnijas kases reģistriem Norvēģijai
description: Šajā tēmā sniegti norādījumi par kases sistēmas funkcionalitātes iespējošanu Microsoft Dynamics 365 Commerce Norvēģijas lokalizācijai.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944744"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Izvietošanas vadlīnijas kases reģistriem Norvēģijai

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegti norādījumi par kases sistēmas funkcionalitātes iespējošanu Microsoft Dynamics 365 Commerce Norvēģijas lokalizācijai. Lokalizācija sastāv no vairākiem komponentu paplašinājumiem. Šie paplašinājumi ļauj veikt tādas darbības kā pielāgoto lauku drukāšanu kvītīs, papildu audita notikumu, pārdošanas darbību un maksājumu darbību drukāšanu pārdošanas punktā (POS), digitāli parakstīšanas pārdošanas darbības un pārskatu drukāšanu lokālos formātos. Papildinformāciju par Norvēģijas lokalizāciju skatiet [Kases sistēmas funkcionalitāti Norvēģijai](./emea-nor-cash-registers.md). Papildinformāciju par To, kā konfigurēt Commerce for Norway, [skatiet Sadaļā "Iestatīt Norvēģijas tirdzniecību"](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šai](../dev-itpro/build-pipeline.md) lokalizācijas funkcionalitātei. Microsoft Dynamics Pakalpojumā Lifecycle Services (LCS) iepriekšējā mazumtirdzniecības programmatūras izstrādes komplekta (SDK) versijā jums ir jāizmanto norvēģijas digitāla parakstīšanas parauga versija, kas instalēta izstrādātāja virtuālajā datorā (VM). Papildinformāciju skatiet šeit: [Norvēģijas kases reģistru izvietošanas vadlīnijas](./emea-nor-loc-deployment-guidelines.md) (mantojuma).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

## <a name="set-up-fiscal-registration-for-norway"></a>Iestatīt Norvēģijas finanšu reģistrāciju

Norvēģijas finanšu reģistrācijas paraugs ir balstīts uz [finanšu integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ SequentialSign repositoryNorway**[Dynamics 365 Commerce (piemēram, paraugs](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[release/9.34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway) Paraugs sastāv [no](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskālā dokumenta nodrošinātāja un fiskālā savienotāja, kas ir Commerce Runtime paplašinājumi CRT (). Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

Izpildiet finanšu reģistrācijas iestatīšanas soļus, kas [ir aprakstīti sadaļā Tirdzniecības kanālu finanšu integrācijas](./setting-up-fiscal-integration-for-retail-channel.md) iestatīšana:

1. [Iestatīt finanšu reģistrācijas](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) procesu. Noteikti atzīmējiet finanšu reģistrācijas procesa iestatījumus, kas ir specifiski [Norvēģijai](#configure-the-fiscal-registration-process).
1. [Iestatīt kļūdu apstrādes](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) iestatījumus.
1. [Aktivizējiet atliktās finanšu reģistrācijas manuālu](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) izpildi.
1. [Konfigurējiet kanāla](#configure-channel-components) komponentus.

### <a name="configure-the-fiscal-registration-process"></a>Konfigurēt finanšu reģistrācijas procesu

Ievērojiet šos soļus, lai iespējotu finanšu reģistrācijas procesu Norvēģijai commerce headquarters.

1. Lejupielādējiet konfigurācijas failus fiskālā dokumenta sniedzējam un fiskālajam savienotājam no Commerce SDK:

    1. Atveriet risinājumu [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atveriet pēdējo pieejamo filiāles izlaidi (piemēram, **[izlaidiet/9,34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**
    1. Atveriet **src \> FiscalIntegration \> SequentialSignairNorway \> CommerceRuntime.**
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu **pie DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSign atnorwaySample.xml** (piemēram, fails izlaišanai/9,34). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu pie **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSign izdarbošanāsSample.xml** (piemēram, fails laidienam/9,34). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)

1. Pārejiet uz **sadaļu Mazumtirdzniecības un Commerce \> Headquarters \> iestatīšanas parametri \> koplietotie** parametri. Cilnē **Vispārīgi** iestatiet opciju Aktivizēt fiskālo integrāciju **kā** **Jā**.
1. Dodieties uz **mazumtirdzniecības un commerce kanālu iestatīšanas finanšu integrācijas finanšu savienotājiem un \>\>\>** ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Dodieties uz **Retail un Commerce Channel \> iestatīšanas finanšu integrācijas finanšu dokumentu nodrošinātājiem un \>\>** ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības \> un Commerce Channel Setup Finanšu integrācijas \>\> savienotāja funkcionālie** profili. Izveidojiet jaunu savienotāja darbības profilu un atlasiet dokumenta nodrošinātāju un iepriekš ielādēto savienotāju.
1. Pārejiet uz **Retail un Commerce Channel setup Fiscal integration Connector \>\>\> tehniskajiem** profiliem. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto savienotāju. Iestatiet savienotāja tipu uz **Iekšējais**.
1. Dodieties uz mazumtirdzniecības un commerce kanāla iestatīšanas fiskālās integrācijas fiskālā savienotāja grupām un izveidojiet jaunu fiskālā savienotāja grupu iepriekš **\>\>\>** izveidotjam savienotāja funkcionalitātes profilam.
1. Pārejiet uz **mazumtirdzniecības un Commerce \> channel \> iestatīšanas finanšu integrācijas \> finanšu reģistrācijas** procesiem. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma **cilnē Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu. Kopsavilkuma cilnē **Finanšu** pakalpojumi atlasiet savienotāja tehnisko profilu, kuru izveidojāt agrāk. 
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**. Atveriet sadales grafiku un atlasiet darbus **1070** un **1090,** lai pārsūtītu datus uz kanāla datu bāzi.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurēt ciparparaksta parametrus

Ir jākonfigurē sertifikāti, kas tiks izmantoti pārdošanas darbību ciparparakstam veikalā. Parakstīšanas laikā tiek izmantots ciparsertifikāts, kas ir saglabāts Azure atslēgas līdz ar to. Modern POS bezsaistes režīmam parakstīšanu var veikt, arī izmantojot ciparsertifikātu, kas tiek saglabāts datora, kurā ir instalēts Modern POS, lokālā krātuvē.

Lai varētu izmantot ciparsertifikātu, kas tiek glabāts Atslēgas Informācijas krātuvē, ir jāveic tālāk minētās darbības.

1. Ir jābūt izveidotai atslēgas Noliktavas drošības atslēgai. Ieteicams izvietot noliktavu tādā pašā ģeogrāfiskā reģionā kā Commerce Scale Unit.
1. Sertifikāts ir jāielādē atslēgas to krātuvē Atslēgas krātuvē kā base64 virknes noslēpums.
1. Programmai Application Object Server (AOS) ir jābūt pilnvarotai lasīt atslēgas noliktavas slepenos datus.

Papildinformāciju par to, kā strādāt ar atslēgas lomas laikā, skatiet [sadaļā Sākt darbu ar Azure atslēgas lomas](/azure/key-vault/key-vault-get-started).

Pēc tam lapā **Atslēgas Lietotāja parametri jānorāda parametri, lai** piekļūtu atslēgas glabāšanas atslēgai:

- **Nosaukums** un apraksts – **Atslēgas** Kases glabāšanas nosaukums un apraksts.
- **Atslēgas Url** — Atslēgas Darba glabātavas URL.
- **AtslēgasFaila klients – interaktīvā klienta ID programmā, kas ir** Azure Active Directory saistīta ar atslēgu Azure AD e-pasta krātuvi autentifikācijas nolūkiem. Šim klientam ir jābūt piekļuvei, lai nolasītu noslēpumus no glabāšanas.
- **Atslēga Klienta noslēpuma atslēga – slepenā atslēga, kas ir saistīta ar lietojumprogrammu, kas tiek** Azure AD izmantota autentifikācijai Atslēgas Toka krātuvē.
- **Vārds,** **apraksts un** **slepenā** atsauce – sertifikāta vārds, apraksts un slepenā atsauce.

Pēc tam ir jākonfigurē savienotājs saviem sertifikātiem, kas tiek glabāti atslēgas Loma vai lokālā sertifikātu krātuvē. Šis savienotājs tiek izmantots parakstīšanai kanāla pusē.

1. Pārejiet uz **Retail un Commerce Channel setup Fiscal integration Connector \>\>\> tehniskajiem** profiliem.
1. Kopsavilkuma **cilnē** Iestatījumi norādiet šādus ciparparakstu parametrus:

    - **Slepenais** vārds – izvēlieties slepeno vārdu, ko iepriekš konfigurējāt **Key Svarīgie parametri** lapā.
    - **Lokālā sertifikāta** īssavilkums — norādiet lokāli saglabātā sertifikāta īssavilkumu.
    - **Jaukšanas** algoritms – norādiet vienu no kriptogrāfiskajiem jaukšanas algoritmiem, kurus Microsoft .NET atbalsta, piemēram, **SHA1**.
    - **Sertifikātu krātuves nosaukums** — šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala nosaukumu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Sertifikātu krātuves vieta** — šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala atrašanās vietu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Vispirms mēģiniet veikt lokālā sertifikāta lietošanu — atlasiet šo opciju, lai parakstīšanas datiem pēc noklusējuma lietotu lokālās krātuves sertifikātu, nevis sertifikātu** no atslēgas Informācijas.
    - **Veselības pārbaudes aktivizēšana** - Papildinformāciju par veselības pārbaudes funkciju skatiet finanšu [reģistrācijas veselības pārbaudes](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check) sadaļā.

> [!NOTE]
> - Norvēģijai **pašlaik pieņemams tikai SHA1** kriptogrāfiskais jaukšanas algoritms.
> - Noklusējuma krātuves nosaukums un veikala atrašanās vieta tiek pievienota, lai atvieglotu lokālo sertifikātu meklēšanas CRT procesu. X509StoreProvider satur sarakstu ar mapēm, kur tiek glabāti sertifikāti. Ja noklusējuma veikala nosaukums un noklusējuma krātuves atrašanās vieta nav norādītas, X509StoreProvider mēģina atrast sertifikātu visās tā saraksta mapēs.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

### <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

1. Lejupielādējiet Solutions [Dynamics 365 Commerce repozitoriju vai](https://github.com/microsoft/Dynamics365Commerce.Solutions) lejupielādējiet to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet **risinājumu SequentialSign saskaņā arNorway.sln** **zem Dynamics365Commerce.Solutions \\ FiscalIntegration \\ SequentialSignmaksājotNorway** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast CRT paplašinājuma instalētāju:

        - **Commerce Scale Unit: mapē** **SequentialSignranNorway \\\\ ScaleUnit ScaleUnit.SequentialSignNorway.Installer \\ bin \\ Debug \\ net461 atrodiet mapi** **ScaleUnit.SequentialSignNorway.Installer** installer.
        - **CRT Modern POS lokāls: mapē** **SequentialSignllaNorway \\\\ ModernPOS ModernPos.SequentialSignNorway.Installer \\ bin \\ Debug \\ net461 atrodiet** mapi **ModernPos.SequentialSignNorway.Installer** installer.

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Ražošanas vide

Izpildiet darbības, kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos [iepakojumus](fiscal-integration-sample-build-pipeline.md) fiskālās integrācijas parauga iepakojumam. **Failu SequentialSignoraNorway build-build.buildml template UZML var atrast Risinājumu** repozitorija YAML_Files **\\ pipeline**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) YAML_Files.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Iespējojiet ciparparakstu Modern POS bezsaistes režīmā

Lai iespējotu ciparparakstu Modern POS bezsaistes režīmā, pēc Modern POS aktivizēšanas jaunā ierīcē veiciet šīs darbības.

1. Pierakstieties POS.
1. Datu **bāzes savienojuma statusa** lapā pārliecinieties, ka bezsaistes datu bāze ir pilnībā sinhronizēta. Ja lauka Gaidošie **lejupielādes vērtība** ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Izrakstīties no POS.
1. Gaidiet, kamēr bezsaistes datu bāze tiks pilnībā sinhronizēta.
1. Pierakstieties POS.
1. Datu **bāzes savienojuma statusa** lapā pārliecinieties, ka bezsaistes datu bāze ir pilnībā sinhronizēta. Ja gaidošo darbību **vērtība bezsaistes datu bāzes** laukā ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Atkārtoti atveriet Modern POS.
