---
title: Dynamics 365 Human Resources debitoru migrācija uz finanšu un operāciju infrastruktūru
description: Šajā rakstā ir aprakstīta korporācijas Microsoft klientu Dynamics 365 Human Resources migrācija uz finanšu un operāciju infrastruktūru.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63b08a8493702cf319aa078ef6aa787e2094be87
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732767"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources debitoru migrācija

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Klientu migrācija ir debitoru datu bāzes "liftu un maiņu migrācija" (kustība), kas tiek pārvietota uz finanšu un operāciju infrastruktūru. Tai tiek izmantots automatizētās migrācijas rīks. Rezultāts ir jauna finanšu un operāciju vide, kas izmanto klienta Cilvēkresursu datu bāzi.

## <a name="prerequisites"></a>Priekšnosacījumi

### <a name="user-access-and-permissions"></a>Lietotāju piekļuve un tiesības

- Lifecycle Microsoft Dynamics Services lietotājam ir jābūt organizācijas **administratora lomai**.
- Lietotājam vajadzētu būt iespējai izveidot [Azure DevOps projektus](/azure/devops/organizations/projects/create-project) vai izmantot esošu Azure DevOps projektu.
- Lietotājam ir jābūt piekļuvei [, lai izveidotu Azure DevOps personiskās piekļuves drošības](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) pilnvaras, vai arī lietotājam jābūt pilnvarai, kas ir pieejama lietošanai.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse vides dublējums (kastīte)

1. Neobligāta, bet ieteikta: atsvaidzināt esošo personāla vadības jostās vidi, izmantojot cilvēkresursu ražošanas vides kopiju.
2. [Izveidojiet jaunu Dataverse vidi](/power-platform/admin/create-environment#create-an-environment-with-a-database), izmantojot Power Platform administrēšanas centru.

    > [!NOTE]
    > Kad pievienojat datu bāzi, nodrošiniet, lai **Enable Dynamics 365 programmu opcija būtu** iestatīta uz **Jā**.

3. [Kopējiet esošo Dataverse vidi](/power-platform/admin/copy-environment), kas ir saistīta ar savrupo personāla vadības programmu, ar iepriekšējā darbībā izveidoto vidi.

### <a name="dataverse-capacity"></a>Dataverse Jaudas

1. Izmantojiet administrēšanas **centra kopsavilkuma lapu**, lai pārbaudītu, vai glabāšanai Power Platform [Dataverse ir pietiekama pieejamā vides](/power-platform/admin/finance-operations-storage-capacity) kopijas noslodze.
2. Ja pieejamā noslodze nav pietiekama, izmantojiet norādes [par glabāšanas vietas brīvo vietu,](/power-platform/admin/free-storage-space) lai samazinātu vispārējo patēriņu. Debitori var arī [pievienot papildu glabāšanas noslodzi](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Debitoru migrācijas process

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Izveidot Lifecycle Services projektu cilvēkresursu migrācijai

Pirmais solis ir izveidot jaunu finanšu un operāciju ieviešanas projektu programmā Lifecycle Services. Debitoram būs esošs cilvēkresursu lifecycle Services projekts. Esošās cilvēkresursu vides tiks migrētas uz jauno finanšu un operāciju ieviešanas projektu.

Lai izveidotu jaunu projektu, sekojiet šiem soļiem.

1. Piesakieties pakalpojumā Lifecycle Services kā globālais administrators vai norādītā pakalpojuma konta lietotājs.
2. Lifecycle Services sākumlapā atlasiet **Izveidot/jaunu (+)**.
3. Atlasīt finanšu un operāciju programmas kā preci.
4. Laukā **Projekta nolūks** atlasiet **Ieviešana**.
5. Ievadiet projekta nosaukumu un aprakstu.
6. Laukā Pielāgots projekta **tips atlasiet Microsoft** **migrāciju Dynamics 365 Human Resources.**
7. Atzīmējiet šo izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.
8. Atlasiet **Izveidot**.

Pēc jauna Lifecycle Services projekta izveides izpildiet šīs darbības, lai to iestatītu un konfigurētu.

1. Izvēlieties **Projekta izpildē,** lai pabeigtu projekta iestudēšanu. Papildinformāciju skatiet sadaļā [Projekta tablo.](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md)

    - Atlasiet to pašu reģionu, kas ir jūsu pašreizējām vidēm. Šī atlase neietekmē migrāciju.
    - Mantojuma sistēmām atlasiet **Cits**.

2. Pabeidziet projekta iestatījumus. Kā daļu no šīs darbības ir jākonfigurē tiešsaistes SharePoint bibliotēka un Azure savienojumi, Azure DevOps ja tie ir nepieciešami. Papildinformāciju skatiet Lifecycle [Services (LCS) lietotāja rokasgrāmatā](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Debitori var izmantot esošu Azure DevOps projektu un saistīto personiskās piekļuves drošības marķieri. Ja tiek izmantots esošs projekts, ar projektu saistītās konfigurācijas ir pieejamas automātiski, un tās var pārskatīt, lai nodrošinātu precizitāti.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Migrēt cilvēkresursu kastu vidi

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Sagatavot migrēt kases vidi

Kad ir izveidots jauns Lifecycle Services projekts un projekta onboarding process ir pabeigts, varat migrēt pirmo vidi. Pirms šī procesa sākšanas ir ieteicams atsvaidzināt kastu vidi, ko vēlaties migrēt no ražošanas vides savrupā infrastruktūra.

#### <a name="prepare-a-power-platform-environment"></a>Power Platform Vides sagatavošana

> [!NOTE]
> Šo darbību var piemērot tikai kases vides migrācijai. Kad migrēsiet ražošanas vidi, ražošanas Power Platform videi pievienotā esošā administrēšanas centra vide tiks pārnesta.

- Power platform administrēšanas centrā izveidojiet power platform vidi, [ko](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) izmantot kastēs migrēšanai, vai atlasiet esošo vidi.
- [Kopējiet vidi,](/power-platform/admin/copy-environment) lai atsvaidzinātu vidi Power Platform, kas tiek izmantota kartēšanai.

#### <a name="migrate-the-sandbox-environment"></a>Migrēt jostlodziņa vidi

1. Piesakieties pakalpojumā Lifecycle Services kā globālais administrators vai norādītā pakalpojuma konta lietotājs.

    > [!NOTE]
    > Ieteicams izmantot nosauktu lietotāja kontu. Pierakstījamajam lietotājam **savrupā** **cilvēkresursu** dzīves cikla pakalpojumu projektā ir jābūt projekta īpašnieka vai vides vadītāja drošības lomai.

2. Atveriet jaunizveidoto cilvēkresursu migrācijas projektu.
3. Pārskatiet un pabeidziet migrācijas metodoloģijas un projektaboardinga atbilstīgās fāzes.
4. Projekta informācijas panelim noklusējuma: **standarta pieņemšanas testa rūtī** atlasiet Migrēt **HR**.
5. Migrējamajā **rūtī** Atlasīt vidi atlasiet atbilstošo projektu Lifecycle Services un sākotnējo cilvēkresursu vidi (no avota savrupas cilvēkresursu programmas).
6. Iespējojiet **opciju Kartēt Power Platform uz jaunu** vidi un atlasiet atbilstošo Power Platform vidi. Pēc tam atlasiet **Jauns**.
7. Lai apstiprinātu detalizēto **informāciju un debitora izrakstītos** datus, pabeidziet izvietošanas iestatījumus (finanses un operācijas — vadīklu) un pēc tam atlasiet **Izvietot**.

Vides stāvoklis rādīs progresu. Stāvoklis tiks mainīts no ielādes **uz** **Izvietot** uz **Izvietots**.

> [!NOTE]
> Ražošanas rūts nav pieejama, kamēr nav pabeigta projekta gatavības pārbaudes veidlapa. Papildinformāciju skatiet sadaļā [Sagatavošanās tiešā darba vietu sagatavošanai](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Apsvērumi un pieņēmumi

Nomnieka Lifecycle Services projektā pastāv cilvēkresursu kastu vide, kam ir šādi raksturlielumi:

- Cilvēkresursu kases vides nav saistītas ar esošo sapludināto vidi. Dotajā cilvēkresursu vidē vienlaicīgi var tikt norise tikai viena migrācija.
- Vienlaikus atļauto kastu vides tiek pamatotas uz personāla vadības licencēšanas sistēmu. Ja nomniekam ir nopirkts pietiekami daudz licencēšanas, papildu tekstlodziņa vides tiks uzskaitītas **projekta** rūtī Vides.
- Migrācija jāveic tā paša tipa vidēs. Citiem vārdiem sakot, var veikt tikai migrēšanu no kastēs uz kasti vai ražošanu no ražošanas uz ražošanu.

    > [!NOTE]
    > Nosakot ražošanas vai kases vides statusu, tiek apsvērti tikai personāla vadības vides tipi. Ja vides ir nepareizi kategorizētas (t.i., ražošanas vide ir atzīmēta kā kastēs vide vai kā ražošanas vide ir atzīmēta kā vides sūtne), sazinieties ar atbalsta dienestu.

- Ja migrācija nav veiksmīga, tiks rādīts kļūdas kļūdas ziņojums, un poga **Dzēst** kļūs pieejama. Izmantojiet šo pogu, lai dzēstu nesekmīgo migrāciju. Pēc tam varat mainīt vidi.

#### <a name="validate-the-sandbox-migration"></a>Pārbaudīt sūtņu migrēšanu

Kad kastu migrācijas process ir veiksmīgi pabeigts, izveidojiet detalizētu testēšanas plānu, lai pārbaudītu un pierakstītos visos biznesa procesos.

Pirms testēšanas sākšanas pārbaudiet šādu informāciju:

- Apstipriniet, ka migrētā vide ir pieejama ģenerētajā vietrādī URL.
- Apstipriniet, ka lietotāji var piekļūt migrētajā lodziņā.
- Apstipriniet, ka Dataverse vide, kas ir saistīta ar migrēto kastu vidi, ir pieejama.
- Pārbaudiet uz vietas dažādus datus, lai apstiprinātu, ka ir pieejami visbiežākie dati.
- Pabeidziet kritiskos biznesa procesus pārbaudei.
- Apstipriniet, ka drošības politikas ir piemērojamas.
- Apstipriniet, ka pakešuzdevumi tiek izraisīti kā paredzēts.

Jums nebūs attālās darbvirsmas piekļuves migrētās tekstlodziņa. Varat izmantot pašapkalpošanās iespējas un rīkus, lai veiktu tālāk norādītās darbības jūsu 2. pakāpes + kastes vidēs:

- Piekļūstiet [Azure SQL datu bāzei](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Piekļūt [žurnāla failiem](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Izmantojiet [perfmon rīkus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Ieslēgt [/izslēgt uzturēšanas režīmu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Restartējiet [pakalpojumus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Konfigurējiet [Regresīcijas komplekta automatizācijas rīku](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Papildinformāciju skatiet bieži uzdotie [jautājumi par pašapkalpošanās izvietošanu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Migrēt cilvēkresursu ražošanas vidi

Kad esat beidzis migrēt un validēt kastu vidi, veiciet šos soļus, lai migrētu ražošanas vidi.

#### <a name="prerequisites"></a>Priekšnosacījumi

- Abonementa novērtējumam jābūt pabeigtam.
- Gatavības novērtēšanai uz [darbu ir](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) jābūt pabeigtai.

#### <a name="migrate-the-production-environment"></a>Migrēt ražošanas vidi

1. Piesakieties pakalpojumā Lifecycle Services kā globālais administrators vai norādītā pakalpojuma konta lietotājs.

    > [!NOTE]
    > Ieteicams izmantot nosauktu lietotāja kontu. Pierakstītā lietotājam lifecycle **Services projektā** ir **jābūt** projekta īpašnieka vai vides vadītāja drošības lomai.

2. Atvērt jauno cilvēkresursu migrācijas projektu.
3. Pārskatiet un pabeidziet migrācijas metodoloģijas un projektaboardinga atbilstīgās fāzes.
4. Projekta informācijas panelim ražošanas rūtī **atlasiet** Migrēt **HR**.
5. Migrējamajā **rūtī** Atlasīt vidi atlasiet atbilstošo Lifecycle Services projektu un sākotnējo cilvēkresursu vidi (no avota savrupas cilvēkresursu programmas). Pēc tam atlasiet **Jauns**.
6. Lai apstiprinātu detalizēto **informāciju un debitora izrakstītos** datus, pabeidziet izvietošanas iestatījumus (finanses un operācijas — vadīklu) un pēc tam atlasiet **Izvietot**.

Vides stāvoklis parādīs izvietošanas progresu. Stāvoklis tiks mainīts no ielādes **uz** **Izvietot** uz **Izvietots**.

#### <a name="post-migration-considerations"></a>Pēcmigrēšanas apsvērumi

- Pielietot visjaunākos [kvalitātes](/fin-ops-core/fin-ops/get-started/quality-updates) atjauninājumus jūsu vidēs.
- Ja izmantojat virtuālās [tabulas](hr-admin-integration-common-data-service-virtual-entities.md), pārkonfigurēt galapunktus.
- Pārkonfigurēt dubultās rakstīšanas integrāciju. Novērtējiet, kuri elementi ir jāiespējo.
- Apsveriet iespēju izmantot virtuālās tabulas, lai aizstātu dubultās rakstīšanas integrācijai.

#### <a name="dual-write-integration"></a>Duālā ieraksta integrācija

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Dubultās Microsoft Power Platform rakstīšanas integrācijas iestatīšana

1. Dodieties uz Power Platform administrēšanas centru un kreisajā **navigācijā** atlasiet Vides.
2. Atlasiet iepriekš kopēto/atsvaidzināto vidi un apstipriniet, ka stāvoklis ir **Gatavs**.
3. Pārejiet uz sadaļu Lifecycle Services un apstipriniet, ka migrācijas projekta statuss ir **Izvietots**.
4. Zem migrētās vides atlasiet Pilnas **detaļas**, lai pārskatītu papildinformāciju [un iestatītu duālo rakstīšanas programmu](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Dubultās **rakstīšanas programmas konfigurācijas rūtī atzīmējiet** izvēles rūtiņu, lai piekristu kartēt un sinhronizēt datus starp datu bāzēm, un pēc tam atlasiet **Konfigurēt**.
6. Ja ziņojumu lodziņš ziņo par veiksmīgu duālās rakstīšanas konfigurāciju, atlasiet **Labi**.
7. Detalizētu informāciju par konfigurācijas progresu var pārraudzīt.
8. Kad konfigurācija ir pabeigta, atlasiet Saiti ar **vidi Power Platform, lai** sinhronizētu pieejamos datu elementus.
9. Kad statuss norāda, ka vides ir veiksmīgi saistītas, dodieties uz administrēšanas centru, Power Platform lai pārskatītu un atlasītu atbilstošos datu elementus.
10. Kreisajā rūtī atlasiet **Dynamics 365 programmu \> resursus**.
11. Apstipriniet, ka ir iespējots dubultās rakstīšanas personāla vadības programmas **statuss**.
12. Atlasiet dubultās rakstīšanas personāla vadības programmu un pēc tam atlasiet **Instalēt**.
13. Rūtī Instalēt **dubultās rakstīšanas Dynamics 365 Human Resources programmu** atlasiet atbilstošo vidi, kurā instalēt pakotni.
14. Atzīmējiet izvēles rūtiņu, lai piekristu pakalpojuma noteikumiem, un pēc tam atlasiet **Instalēt**.
15. Dynamics 365 programmas vidē instalēšanas laikā **statuss tiks** Instalēts. Kad instalēšana būs pabeigta, tā **tiks** atjaunināta uz Instalēts.

##### <a name="review-and-apply-a-dual-write-solution"></a>Pārskatiet un piemēroiet duālo rakstīšanas risinājumu

1. Jaunajā finanšu un operāciju vidē dodieties uz datu pārvaldību **Dubultā \> rakstīšana**.
2. Atlasiet **Lietot risinājumu**.
3. Rūtī atlasiet Dynamics instalētos **risinājumus**, duālās **rakstīšanas programmas pamata elementa** kartes un **Dynamics 365 Human Resources kartes**. Pēc tam atlasiet **Lietot**. Ziņojums apstiprina, ka risinājums ir pielietots. Kad risinājums ir veiksmīgi pielietots, tiks parādītas visas pieejamās tabulu kartes.
4. Pārskatiet pieejamās tabulas kartes, lai izvēlētos un palaistu integrāciju, izmantojot duālo rakstiet.
5. Kad jūs pirmo reizi palaižat dubultās rakstīšanas integrāciju tabulu kartēm, atzīmējiet izvēles **rūtiņu Sākotnējā** sinhronizācija. Ja avota Personāla vadības vidē pastāv integrācija, palaižot tabulu karšu integrāciju, **nav** jāatlasa izvēles rūtiņa Sākotnējā sinhronizācija.

#### <a name="recommended-practices"></a>Rekomendētās prakses

Šajā sadaļā ir sniegti rekomendācijas par migrēšanu no savrupas infrastruktūras uz finanšu un operāciju infrastruktūru.

- Ieteicams strādāt ar partneri, lai Microsoft Dynamics saņemtu palīdzību saistībā ar cilvēkresursu vides migrāciju.
- Plānojiet atbilstošo laiku, lai varētu veikt pilnu lietotāja pieņemšanas pārbaudi (UAT) kastē migrētajā vidē.
- Plānojiet un dokumentē detalizētos soļus, lai migrētu integrācijas migrētajā vidē.
- Izveidojiet detalizētu kontrolsarakstu, lai ieskictu pārslēgšanas procesu migrācijai.
- Plānojiet savam biznesam atbilstošu dīkstāves daudzumu migrācijas laikā.
- Iesakām FastTrack-kvalificētiem debitoriem strādāt ar viņu FastTrack risinājuma arhitektu, lai saņemtu palīdzību par migrācijas procesa raudzīšanu.
- Pirms pirmās migrācijas ieteicams atjaunot savrupas infrastruktūras kases vides. Šajā atsvaidzināšanas laikā ir jāiekļauj Dataverse vide, kas ir saistīta ar vides, uz kuru plānojat migrēt, vides.
- Ieteicams izmantot pakalpojuma kontu, kad izmantojat, izvietojot, migrējot un veidojot Lifecycle Services projektu.
- Plānojiet UAT pārbaudes vides jaunināšanai uz pēdējo vispārējās pieejamības (GA) laidienu. Papildinformāciju skatiet [apsvērumos](hr-infrastructure-merge.md#considerations).
