---
title: Dynamics 365 Human Resources Klientu migrācija uz finanšu un operāciju infrastruktūru
description: Šajā rakstā ir aprakstīta Microsoft Dynamics 365 Human Resources klientu migrācija uz finanšu un operāciju infrastruktūru.
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
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760367"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources Klientu migrācija

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Klientu migrācija ir klientu datu bāzes "pacelšanas un pārvietošanas migrācija" (pārvietošana) uz finanšu un operāciju infrastruktūru. Tam tiek izmantots automatizēts migrācijas rīks. Rezultāts ir jauna finanšu un operāciju vide, kas izmanto klienta cilvēkresursu datu bāzi.

## <a name="prerequisites"></a>Priekšnosacījumi

### <a name="user-access-and-permissions"></a>Lietotāju piekļuve un atļaujas

- Lifecycle Microsoft Dynamics Services lietotājam ir jābūt organizācijas administratora **lomai**.
- Lietotājam vajadzētu būt iespējai [izveidot Azure DevOps projektus](/azure/devops/organizations/projects/create-project) vai izmantot esošu Azure DevOps projektu.
- Lietotājam ir jābūt piekļuvei, lai [izveidotu Azure DevOps personiskās piekļuves drošības pilnvaru](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate), vai arī viņam ir jābūt pilnvarotai lietošanai.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse vides dublēšana (smilškaste)

 - Neobligāti, bet ieteicami: atsvaidziniet esošo cilvēkresursu smilškastes vidi, izmantojot personāla daļas ražošanas vides kopiju.
 - Izveidojiet jaunu Dataverse vidi, izmantojot administrēšanas Power Platform centru.
 - Kopējiet esošo Dataverse vidi, kas ir saistīta ar savrupo cilvēkresursu programmu, vidē, kuru izveidojāt iepriekšējā darbībā.

> [!NOTE]
> Pievienojot datu bāzi, pārliecinieties, vai opcijai **Iespējot Dynamics 365 programmas** ir iestatīta vērtība **Jā**. Detalizētu informāciju skatiet sadaļā [Vides sagatavošana Power Platform](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse Jaudas

1. **Izmantojiet lapu** Kopsavilkums Power Platform administrēšanas centrā, lai pārbaudītu, vai [Dataverse krātuvei](/power-platform/admin/finance-operations-storage-capacity) ir pietiekama vides kopijas noslodze.
2. Ja nav pietiekami daudz pieejamās ietilpības, izmantojiet [norādījumus par krātuves vietas](/power-platform/admin/free-storage-space) atbrīvošanu, lai samazinātu kopējo patēriņu. Klienti var arī [pievienot papildu krātuves ietilpību](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Klientu migrācijas process

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Dzīves cikla pakalpojumu projekta izveide cilvēkresursu migrācijai

Pirmais solis ir izveidot jaunu finanšu un operāciju ieviešanas projektu Lifecycle Services. Klientam būs esošs cilvēkresursu dzīves cikla pakalpojumu projekts. Esošās cilvēkresursu vides tiks migrētas uz jauno finanšu un operāciju ieviešanas projektu.

Lai izveidotu jaunu projektu, veiciet tālāk norādītās darbības.

1. Piesakieties Lifecycle Services kā globālais administrators vai norādītais pakalpojuma konta lietotājs.
2. Dzīves cikla pakalpojumu sākumlapā atlasiet **Izveidot/jauns (+)**.
3. Atlasiet Finance and Operations programmas kā produktu.
4. Laukā **Projekta mērķis** atlasiet **Ieviešana**.
5. Ievadiet projekta nosaukumu un aprakstu.
6. Laukā **Project pielāgotais tips** atlasiet **Microsoft Dynamics 365 Human Resources migrācija**.
7. Atzīmējiet izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.
8. Atlasiet **Izveidot**.

Kad esat izveidojis jaunu Lifecycle Services projektu, veiciet tālāk norādītās darbības, lai to iestatītu un konfigurētu.

1. Atlasiet **Project onboarding,** lai pabeigtu projekta pievienošanu. Papildinformāciju skatiet sadaļā [Projekta pievienošana.](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md)

    - Atlasiet to pašu reģionu, kurā atrodas jūsu pašreizējā vide. Šī atlase neietekmēs migrāciju.
    - Mantotajām sistēmām atlasiet **Cits**.

2. Pabeidziet projekta iestatījumus. Šīs darbības ietvaros ir jākonfigurē SharePoint tiešsaistes bibliotēka un Azure savienojumi, Azure DevOps ja tie ir nepieciešami. Papildinformāciju skatiet sadaļā [Lifecycle Services (LCS) lietotāja rokasgrāmata](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Klienti var izmantot esošu Azure DevOps projektu un saistīto personiskās piekļuves drošības pilnvaru. Ja tiek izmantots esošs projekts, konfigurācijas, kas ir saistītas ar projektu, ir automātiski pieejamas, un tās var pārskatīt precizitātes dēļ.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Personāla vadības smilškastes vides migrēšana

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Sagatavošanās smilškastes vides migrēšanai

Kad ir izveidots jauns Lifecycle Services projekts un projekta pievienošanas process ir pabeigts, varat migrēt savu pirmo vidi. Pirms sākat šo procesu, ieteicams atsvaidzināt smilškastes vidi, kuru vēlaties migrēt no ražošanas vides savrupajā infrastruktūrā.

#### <a name="prepare-a-power-platform-environment"></a>Vides sagatavošana Power Platform

> [!NOTE]
> Šī darbība ir piemērojama tikai smilškastes vides migrācijai. Migrējot ražošanas vidi, esošā Power Platform administrēšanas centra vide, kas ir pievienota ražošanas videi, tiks pārnesta uz priekšu. Pievienojot datu bāzi, pārliecinieties, vai pogai Iespējot Dynamics 365 programmas **ir iestatīta** vērtība **Jā**. 

- Power platform administrēšanas centrā [izveidojiet vidi ar datu bāzi](/power-platform/admin/create-environment#create-an-environment-with-a-database), ko izmantot smilškastes migrācijai, vai atlasiet esošu vidi.
- [Kopējiet vidi, lai atsvaidzinātu vidi](/power-platform/admin/copy-environment), Power Platform kas tiek izmantota kartēšanai.

#### <a name="migrate-the-sandbox-environment"></a>Smilškastes vides migrēšana

1. Piesakieties Lifecycle Services kā globālais administrators vai norādītais pakalpojuma konta lietotājs.

    > [!NOTE]
    > Ieteicams izmantot nosauktu lietotāja kontu. Lietotājam, kurš ir pierakstījies, **ir jābūt projekta īpašnieka** vai **vides pārvaldnieka** drošības lomai savrupajā cilvēkresursu dzīves cikla pakalpojumu projektā.

2. Atveriet jaunizveidoto cilvēkresursu migrācijas projektu.
3. Pārskatiet un pabeidziet attiecīgos migrācijas metodoloģijas un projekta pievienošanas posmus.
4. Projekta informācijas paneļa testa **rūtī Noklusējums: standarta** akceptēšana atlasiet **Migrēt HR.**
5. **Rūtī Atlasiet migrējamo** vidi atlasiet atbilstošo Lifecycle Services projektu un sākotnējo cilvēkresursu vidi (no avota savrupās lietojumprogrammas Personāla vadība).
6. Iespējojiet **opciju Kartēt uz jaunu Power Platform vidi un atlasiet atbilstošo** vidi Power Platform. Pēc tam atlasiet **Jauns**.
7. Aizpildiet izvietošanas **iestatījumu (finance and operations – sandbox)** vedni, lai apstiprinātu detalizētu informāciju un klienta pierakstīšanos, un pēc tam atlasiet **Izvietot**.

Vides stāvoklis parādīs progresu. Stāvoklis tiks mainīts no **ielādes** uz izvietošanu uz **izvietošanu** **·**.

> [!NOTE]
> Ražošanas rūts nebūs pieejama, kamēr nebūs pabeigts projekta gatavības pārbaudes saraksts. Papildinformāciju skatiet sadaļā [Sagatavošanās darbības uzsākšanai](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Apsvērumi un pieņēmumi

Personāla vadības smilškastes vide pastāv nomnieka dzīves cikla pakalpojumu projektā, kam ir tālāk norādītie raksturlielumi.

- Personāla vadības smilškastes vide nav saistīta ar esošu sapludinātu vidi. Konkrētā cilvēkresursu vidē vienlaikus var notikt tikai viena migrācija.
- Vienlaikus atļauto smilškastes vidi skaits ir atkarīgs no cilvēkresursu licencēšanas. Ja nomniekam ir iegādāts pietiekami daudz licences, projekta rūtī Vides **tiks norādītas** papildu smilškastes vides.
- Migrācija jāveic uz tāda paša veida vidi. Citiem vārdiem sakot, var veikt tikai migrāciju no smilškastes uz smilškasti vai no ražošanas uz ražošanu.

    > [!NOTE]
    > Nosakot ražošanas vai smilškastes statusu, tiek ņemti vērā tikai cilvēkresursu vides tipi. Ja vides ir nepareizi kategorizētas (tas ir, ražošanas vide ir atzīmēta kā smilškastes vide vai smilškastes vide ir atzīmēta kā ražošanas vide), sazinieties ar atbalsta dienestu.

- Ja migrācija nav veiksmīga, tiks parādīts kļūmes kļūdas ziņojums un **būs pieejama poga Dzēst**. Izmantojiet šo pogu, lai izdzēstu neveiksmīgo migrāciju. Pēc tam jūs varat remigrēt vidi.

#### <a name="validate-the-sandbox-migration"></a>Smilškastes migrācijas validēšana

Kad smilškastes migrācijas process ir veiksmīgi pabeigts, izveidojiet detalizētu testēšanas plānu, lai pārbaudītu un pierakstītos visos biznesa procesos.

Pirms sākat testēšanu, pārbaudiet tālāk norādīto informāciju.

- Pārliecinieties, vai migrētā vide ir pieejama ģenerētajā vietrādī URL.
- Pārliecinieties, vai lietotāji var piekļūt migrētajai smilškastei.
- Pārliecinieties, vai vide, Dataverse kas ir saistīta ar migrēto smilškastes vidi, ir pieejama.
- Pārbaudiet dažādus datus uz vietas, lai pārliecinātos, ka ir pieejami visjaunākie dati.
- Pabeidziet validācijai kritiskos biznesa procesus.
- Pārliecinieties, vai jūsu drošības politikas ir piemērojamas.
- Pārliecinieties, vai pakešuzdevumi tiek aktivizēti, kā paredzēts.

Jums nebūs attālās darbvirsmas piekļuves migrētajai smilškastei. Varat izmantot pašapkalpošanās iespējas un rīkus, lai veiktu tālāk norādītās darbības savā Tier 2+ smilškastes vidē:

- Piekļūstiet Azure SQL datu [bāzei](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Piekļūstiet [žurnālfailiem](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Izmantojiet [perfmon rīkus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Ieslēdziet/izslēdziet [uzturēšanas](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs) režīmu.
- Restartējiet [pakalpojumus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Konfigurējiet Regression komplekta automatizācijas [rīku](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Papildinformāciju skatiet sadaļā [Bieži uzdotie jautājumi par pašapkalpošanās izvietošanu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Cilvēkresursu ražošanas vides migrēšana

Kad esat pabeidzis smilškastes vides migrēšanu un pārbaudi, veiciet tālāk norādītās darbības, lai migrētu ražošanas vidi.

#### <a name="prerequisites"></a>Priekšnosacījumi

- Abonēšanas aprēķinātājs ir jāaizpilda.
- Jāpabeidz Go-live [gatavības novērtējums](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="migrate-the-production-environment"></a>Ražošanas vides migrēšana

1. Piesakieties Lifecycle Services kā globālais administrators vai norādītais pakalpojuma konta lietotājs.

    > [!NOTE]
    > Ieteicams izmantot nosauktu lietotāja kontu. Lietotājam, kurš ir pierakstījies, **Lifecycle Services projektā ir jābūt projekta īpašnieka** vai **vides pārvaldnieka** drošības lomai.

2. Atveriet jauno cilvēkresursu migrācijas projektu.
3. Pārskatiet un pabeidziet attiecīgos migrācijas metodoloģijas un projekta pievienošanas posmus.
4. Projekta informācijas paneļa rūtī **Ražošana** atlasiet **Migrēt HR.**
5. **Rūtī Atlasiet migrējamo** vidi atlasiet atbilstošo Lifecycle Services projektu un sākotnējo cilvēkresursu vidi (no avota savrupās lietojumprogrammas Personāla vadība). Pēc tam atlasiet **Jauns**.
6. Aizpildiet izvietošanas **iestatījumu (finance and operations – sandbox)** vedni, lai apstiprinātu detalizētu informāciju un klienta pierakstīšanos, un pēc tam atlasiet **Izvietot**.

Vides stāvoklis parādīs izvietošanas progresu. Stāvoklis tiks mainīts no **ielādes** uz izvietošanu uz **izvietošanu** **·**.

#### <a name="post-migration-considerations"></a>Apsvērumi pēc migrācijas

- Lietojiet jaunākos [kvalitātes atjauninājumus](/fin-ops-core/fin-ops/get-started/quality-updates) savai videi.
- Ja izmantojat [virtuālās tabulas](hr-admin-integration-common-data-service-virtual-entities.md), pārkonfigurējiet galapunktus.
- Pārkonfigurējiet dubultās rakstīšanas integrāciju. Novērtējiet, kuras entītijas ir jāiespējo.
- Apsveriet iespēju izmantot virtuālās tabulas, lai aizstātu dubulto rakstīšanu integrācijai.

#### <a name="dual-write-integration"></a>Duālā ieraksta integrācija

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Dubultās rakstīšanas integrācijas iestatīšana Microsoft Power Platform

1. Dodieties uz administrēšanas Power Platform centru un kreisajā navigācijas rūtī atlasiet **Vides**.
2. Atlasiet iepriekš kopēto/atsvaidzināto vidi un pārliecinieties, vai stāvoklis ir **Gatavs**.
3. Dodieties uz Lifecycle Services un pārliecinieties, vai migrācijas projekta statuss ir **Izvietots**.
4. Migrētajā vidē atlasiet **Pilna informācija**, lai pārskatītu papildinformāciju un [iestatītu dubultrakstīšanas lietojumprogrammu](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. **Dubultrakstīšanas lietojumprogrammas konfigurācijas** rūtī atzīmējiet izvēles rūtiņu, lai piekristu kartēt un sinhronizēt datus starp datu bāzēm, un pēc tam atlasiet **Konfigurēt**.
6. Kad ziņojuma lodziņš paziņo par veiksmīgu divu burtu konfigurēšanu, atlasiet **Labi**.
7. Jūs varat uzraudzīt konfigurācijas progresu detaļās.
8. Kad konfigurēšana ir pabeigta, atlasiet **Saistīt ar Power Platform vidi**, lai sinhronizētu pieejamos datu elementus.
9. Kad statuss norāda, ka vides ir veiksmīgi saistītas, dodieties uz administrēšanas Power Platform centru, lai pārskatītu un atlasītu atbilstošos datu elementus.
10. Kreisajā rūtī atlasiet **Dynamics 365 programmu \> resursi**.
11. Pārliecinieties, vai duālās rakstīšanas personāla programmas statuss ir **Iespējots**.
12. Atlasiet divu rakstu personāla vadības lietojumprogrammu un pēc tam atlasiet **Instalēt**.
13. **Rūtī Instalēt dubultrakstīšanas Dynamics 365 Human Resources programmu** atlasiet atbilstošo vidi, kurā instalēt pakotni.
14. Atzīmējiet izvēles rūtiņu, lai piekristu pakalpojuma noteikumiem, un pēc tam atlasiet **Instalēt**.
15. Dynamics 365 programmas vidē statuss būs **Instalēšana** instalēšanas laikā. Kad instalēšana būs pabeigta, tas tiks atjaunināts uz **Instalēts**.

##### <a name="review-and-apply-a-dual-write-solution"></a>Pārskatiet un lietojiet divkāršās rakstīšanas risinājumu

1. Jaunajā finanšu un operāciju vidē dodieties uz sadaļu **Datu pārvaldība \> Dual-write**.
2. Atlasiet **Lietot risinājumu**.
3. Rūtī atlasiet **Dynamics instalētie risinājumi**, **Duālās rakstīšanas lietojumprogrammu pamata entītiju kartes un** kartes **Dynamics 365 Human Resources**. Pēc tam atlasiet **Lietot**. Ziņojums apstiprina, ka risinājums tiek lietots. Pēc tam, kad risinājums ir veiksmīgi piemērots, tiks parādītas visas pieejamās tabulas kartes.
4. Pārskatiet pieejamās tabulu kartes, lai atlasītu un palaistu integrāciju, izmantojot dubulto rakstīšanu.
5. Pirmo reizi palaižot dubultās rakstīšanas integrāciju tabulu kartēm, atzīmējiet izvēles rūtiņu **Sākotnējā sinhronizācija**. Ja pastāv integrācija no avota cilvēkresursu vides, palaižot tabulu karšu integrāciju, nav jāatzīmē izvēles rūtiņa **Sākotnējā sinhronizācija**.

#### <a name="recommended-practices"></a>Ieteicamā prakse

Šajā iedaļā ir izklāstīti ieteikumi pārejai no savrupās infrastruktūras uz finanšu un operāciju infrastruktūru.

- Mēs ļoti iesakām sadarboties ar savu Microsoft Dynamics partneri, lai saņemtu palīdzību saistībā ar cilvēkresursu vides migrāciju.
- Plānojiet atbilstošu laiku, lai veiktu pilnīgu lietotāju pieņemšanas testēšanu (UAT) smilškastes migrētajā vidē.
- Plānojiet un dokumentējiet detalizētas darbības, lai migrētu integrācijas uz migrēto vidi.
- Izveidojiet detalizētu kontrolsarakstu, lai strukturētu migrācijas pārslēgšanas procesu.
- Plānojiet savam uzņēmumam atbilstošu dīkstāves laiku, kamēr veicat migrāciju.
- Mēs ļoti iesakām FastTrack kvalificētiem klientiem sadarboties ar savu FastTrack risinājumu arhitektu, lai saņemtu palīdzību migrācijas procesa pārraudzībā.
- Pirms pirmās migrācijas veikšanas ir ļoti ieteicams atsvaidzināt smilškastes vidi savrupā infrastruktūrā. Šajā atsvaidzinājumā ir jāiekļauj jūsu Dataverse vide, kas ir savienota ar smilškastes vidi, uz kuru plānojat migrēt.
- Ir ļoti ieteicams izmantot pakalpojuma kontu, kad izvietojat, migrējat un veidojat savu Lifecycle Services projektu.
- Plānojiet jaunināt smilškastes vidi UAT validācijai jaunākajā vispārējās pieejamības (GA) laidienā. Papildinformāciju skatiet sadaļā [Apsvērumi](hr-infrastructure-merge.md#considerations).
