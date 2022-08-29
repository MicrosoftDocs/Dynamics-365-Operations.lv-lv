---
title: Izvietošanas vadlīnijas kases reģistriem Norvēģijai
description: Šajā rakstā ir sniegti norādījumi par kases sistēmas funkcionalitātes iespējošanu Norvēģijas Microsoft Dynamics 365 Commerce lokalizācijai.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 9149e9da7222699e9ca996b69e56fff07b77a737
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/24/2022
ms.locfileid: "9345996"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Izvietošanas vadlīnijas kases reģistriem Norvēģijai

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Šajā rakstā aprakstītās darbības ir jāievieš tikai tad, ja Microsoft Dynamics 365 Commerce izmantojat versiju 10.0.29 vai jaunāku versiju. Commerce versijā 10.0.28 vai agrākā versijā jums ir jāizmanto iepriekšējā mazumtirdzniecības programmatūras izstrādes komplekta (SDK) versija izstrādātāja virtuālajā datorā (VM) Microsoft Dynamics programmatūrā Lifecycle Services (LCS). Papildinformāciju skatiet šeit: [Norvēģijas kases reģistru izvietošanas vadlīnijas (mantojuma)](./emea-nor-loc-deployment-guidelines.md). Ja izmantojat Commerce versiju 10.0.28 vai jaunāku versiju un migrēja uz Commerce versiju 10.0.29 vai jaunāku versiju, [rīkojieties saskaņā ar soļiem, kas veikti, migrējot no Norvēģijas mantojuma Commerce funkcionalitātes](./emea-nor-fi-migration.md).

Šajā rakstā ir sniegtas norādes par to, kā iespējot kases sistēmas funkcionalitāti Commerce localization Norvēģijai. Lokalizācija sastāv no vairākiem komponentu paplašinājumiem, kas ļauj veikt darbības, piemēram, kvīšu pielāgoto lauku drukāšanu, papildu audita notikumu, pārdošanas darbību un maksājumu darbību reģistrēšanu pārdošanas punktā (POS), ciparparaksta pārdošanas darbību drukāšanu un pārskatu drukāšanu lokālos formātos. Papildinformāciju par Norvēģijas lokalizāciju skatiet Kases [sistēmas funkcionalitāti Norvēģijai](./emea-nor-cash-registers.md). Papildinformāciju par To, kā konfigurēt Commerce for Norway, [skatiet Sadaļā "Iestatīt Norvēģijas tirdzniecību"](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

## <a name="set-up-fiscal-registration-for-norway"></a>Iestatīt Norvēģijas finanšu reģistrāciju

Norvēģijas finanšu reģistrācijas paraugs ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Commerce SDK. Paraugs atrodas Solutions repository mapē src FiscalIntegration **SequentialSign repositoryNorway\\\\**.[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) no fiskālā dokumenta nodrošinātāja un fiskālā savienotāja, kas ir Commerce Runtime paplašinājumi (CRT). Papildinformāciju par to, kā izmantot Commerce SDK, [skatiet download Commerce SDK par paraugos un atsauces pakotnēs no GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[un un iestatiet būvējuma konveijeru neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

Izpildiet finanšu reģistrācijas iestatīšanas soļus, kas ir [aprakstīti sadaļā Tirdzniecības kanālu finanšu integrācijas iestatīšana](./setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatīt fiskālās reģistrācijas procesu](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noteikti atzīmējiet finanšu reģistrācijas procesa iestatījumus, kas ir specifiski [Norvēģijai](#configure-the-fiscal-registration-process).
1. [Iestatīt kļūdu apstrādes iestatījumus](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iespējojiet atliktās finanšu reģistrācijas manuālu izpildi](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurēt finanšu reģistrācijas procesu

Ievērojiet šos soļus, lai iespējotu finanšu reģistrācijas procesu Norvēģijai commerce headquarters.

1. Lejupielādējiet konfigurācijas failus fiskālā dokumenta sniedzējam un fiskālajam savienotājam no Commerce SDK:

    1. Atveriet risinājumu repozitoriju [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Atvērt pēdējo pieejamo filiāles versiju
    1. Atveriet **src \> FiscalIntegration \> SequentialSignairNorway \> CommerceRuntime**.
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu **pie DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSign atnorwaySample.xml**.
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu pie **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSign izn elementuNorwaySample.xml**.

1. Pārejiet uz sadaļu **Mazumtirdzniecības un Commerce \> Headquarters iestatīšanas \> parametri koplietotie \> parametri**. Cilnē Vispārīgi **iestatiet** opciju Aktivizēt **fiskālo integrāciju kā** **Jā**.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu savienotājiem** un ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu dokumentu nodrošinātājiem** un ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības un Commerce \> Channel Setup \> Finanšu integrācijas savienotāja \> funkcionālie profili**. Izveidojiet jaunu savienotāja darbības profilu un atlasiet dokumenta nodrošinātāju un iepriekš ielādēto savienotāju.
1. Pārejiet uz **Retail un Commerce Channel \> setup \> Fiscal integration \> Connector tehniskajiem profiliem**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto savienotāju. Iestatiet savienotāja tipu uz **Iekšējais**.
1. Pārejiet uz **sadaļu \>\>\>** Mazumtirdzniecības un Komercijas kanāla iestatīšanas fiskālās integrācijas fiskālā savienotāja grupas un izveidojiet jaunu fiskālā savienotāja grupu iepriekš izveidotjam savienotāja funkcionalitātes profilam.
1. Pārejiet uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas finanšu \> reģistrācijas procesiem**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma cilnē **Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu. Kopsavilkuma cilnē **Finanšu pakalpojumi** atlasiet savienotāja tehnisko profilu, kuru izveidojāt agrāk. 
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**. Atveriet sadales grafiku un atlasiet darbus **1070 un** **1090**, lai pārsūtītu datus uz kanāla datu bāzi.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurēt ciparparaksta parametrus

Ir jākonfigurē sertifikāti, kas tiks izmantoti pārdošanas darbību ciparparakstam veikalā. Parakstīšanas laikā tiek izmantots ciparsertifikāts, kas ir saglabāts Azure atslēgas līdz ar to. Modern POS bezsaistes režīmam parakstīšanu var veikt, arī izmantojot ciparsertifikātu, kas tiek saglabāts datora, kurā ir instalēts Modern POS, lokālā krātuvē.

Lai varētu izmantot ciparsertifikātu, kas tiek glabāts Atslēgas Informācijas krātuvē, ir jāveic tālāk minētās darbības.

1. Ir jābūt izveidotai atslēgas Noliktavas drošības atslēgai. Ieteicams izvietot noliktavu tādā pašā ģeogrāfiskā reģionā kā Commerce Scale Unit.
1. Sertifikāts ir jāielādē atslēgas to krātuvē Atslēgas krātuvē kā base64 virknes noslēpums.
1. Programmai Application Object Server (AOS) ir jābūt pilnvarotai lasīt atslēgas noliktavas slepenos datus.

Papildinformāciju par to, kā strādāt ar atslēgas lomas laikā, skatiet sadaļā [Sākt darbu ar Azure atslēgas lomas](/azure/key-vault/key-vault-get-started).

Pēc tam lapā **Atslēgas Lietotāja parametri** jānorāda parametri, lai piekļūtu atslēgas glabāšanas atslēgai:

- **Nosaukums** un **apraksts** – Atslēgas Kases glabāšanas nosaukums un apraksts.
- **Atslēgas Url —** Atslēgas Darba glabātavas URL.
- **AtslēgasFaila** klients – interaktīvā Azure Active Directory klienta ID programmā Azure AD, kas ir saistīta ar atslēgu noliktavas noliktavas autentifikācijas nolūkiem. Šim klientam ir jābūt piekļuvei, lai nolasītu noslēpumus no glabāšanas.
- **Atslēga Klienta noslēpuma atslēga** – slepenā atslēga, kas ir Azure AD saistīta ar lietojumprogrammu, kas tiek izmantota autentifikācijai Atslēgas Toka krātuvē.
- **Vārds**, **apraksts** un slepenā **atsauce** – sertifikāta vārds, apraksts un slepenā atsauce.

Pēc tam ir jākonfigurē savienotājs saviem sertifikātiem, kas tiek glabāti atslēgas Loma vai lokālā sertifikātu krātuvē. Šis savienotājs tiek izmantots parakstīšanai kanāla pusē.

1. Pārejiet uz **Retail un Commerce Channel \> setup \> Fiscal integration \> Connector tehniskajiem profiliem**.
1. Kopsavilkuma cilnē **Iestatījumi** norādiet šādus ciparparakstu parametrus:

    - **Slepenais** vārds – izvēlieties slepeno vārdu, ko iepriekš konfigurējāt Key **Svarīgie parametri** lapā.
    - **Lokālā sertifikāta īssavilkums** — norādiet lokāli saglabātā sertifikāta īssavilkumu.
    - **Jaukšanas algoritms** – norādiet vienu no kriptogrāfiskajiem jaukšanas algoritmiem, kurus atbalsta Microsoft .NET, piemēram, **SHA1**.
    - **Sertifikātu krātuves nosaukums** — šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala nosaukumu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Sertifikātu krātuves vieta —** šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala atrašanās vietu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Vispirms mēģiniet veikt lokālā** sertifikāta lietošanu — atlasiet šo opciju, lai parakstīšanas datiem pēc noklusējuma lietotu lokālās krātuves sertifikātu, nevis sertifikātu no atslēgas Informācijas.
    - **Aktivizējiet veselības** pārbaudi – Papildinformāciju par veselības pārbaudes funkciju skatiet finanšu [reģistrācijas veselības pārbaudes sadaļā](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Norvēģijai **pašlaik pieņemams tikai SHA1** kriptogrāfiskais jaukšanas algoritms.
> - Noklusējuma krātuves nosaukums un veikala atrašanās vieta tiek pievienota, lai atvieglotu lokālo sertifikātu meklēšanas procesu CRT. X509StoreProvider satur sarakstu ar mapēm, kur tiek glabāti sertifikāti. Ja noklusējuma veikala nosaukums un noklusējuma krātuves atrašanās vieta nav norādītas, X509StoreProvider mēģina atrast sertifikātu visās tā saraksta mapēs.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

#### <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

1. Lejupielādējiet Solutions repozitoriju vai [Dynamics 365 Commerce lejupielādējiet](https://github.com/microsoft/Dynamics365Commerce.Solutions) to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet Lejupielādes [Commerce SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. **Atveriet risinājumu SequentialSign saskaņā arNorway.sln** **zem Dynamics365Commerce.Solutions\\ FiscalIntegration\\ SequentialSignmaksājotNorway** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast paplašinājuma CRT instalētāju:

        - **Commerce Scale Unit:** **mapē SequentialSignranNorway\\ ScaleUnit\\ ScaleUnit.SequentialSignNorway.Installer\\ bin\\ Debug\\ net461 atrodiet** **mapi ScaleUnit.SequentialSignNorway.Installer installer**.
        - **CRT Modern POS lokāls:** **mapē SequentialSignllaNorway\\ ModernPOS ModernPos.SequentialSignNorway.Installer\\\\ bin\\ Debug\\ net461 atrodiet** **mapi ModernPos.SequentialSignNorway.Installer installer**.

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet [darbības](fiscal-integration-sample-build-pipeline.md), kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos iepakojumus fiskālās integrācijas parauga iepakojumam. Failu **SequentialSign izn elementuNorway build.buildml** veidni VEIKTĀJML **\\ varat atrast Risinājumu repozitorija YAML_Files pipeline** YAML_Files [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Iespējojiet ciparparakstu Modern POS bezsaistes režīmā

Lai iespējotu ciparparakstu Modern POS bezsaistes režīmā, pēc Modern POS aktivizēšanas jaunā ierīcē veiciet šīs darbības.

1. Pierakstieties POS.
1. Datu bāzes **savienojuma statusa lapā** pārliecinieties, ka bezsaistes datu bāze ir pilnībā sinhronizēta. Ja lauka Gaidošie lejupielādes **vērtība ir** **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Izrakstīties no POS.
1. Gaidiet, kamēr bezsaistes datu bāze tiks pilnībā sinhronizēta.
1. Pierakstieties POS.
1. Datu bāzes **savienojuma statusa lapā** pārliecinieties, ka bezsaistes datu bāze ir pilnībā sinhronizēta. Ja gaidošo darbību vērtība **bezsaistes datu bāzes laukā** ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Atkārtoti atveriet Modern POS.
