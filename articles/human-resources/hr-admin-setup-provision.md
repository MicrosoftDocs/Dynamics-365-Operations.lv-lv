---
title: Human Resources nodrošināšana
description: Šajā tēmā ir izskaidrota jaunas ražošanas vides nodrošināšana programmai Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79747d0c5c4265315d1757352dfecef09c469dd8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710868"
---
# <a name="provision-human-resources"></a>Human Resources nodrošināšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šajā tēmā ir izskaidrota jaunas ražošanas vides nodrošināšana programmai Microsoft Dynamics 365 Human Resources. 

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat nodrošināt jaunu ražošanas vidi, jābūt nodrošinātiem tālāk norādītajiem priekšnosacījumiem.

- Jūs esat iegādājies(-usies) Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kurā jau ir ietverts Human Resources pakalpojumu plāns, un nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

- Globālais administrators ir pierakstījies [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) un izveidojis jaunu Human Resources projektu. 

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources apgrozījuma vides nodrošināšana

>[!NOTE]
> Sākot no 2022. gada aprīlī, cilvēkresursu izmēģinājuma vides nebūs pieejamas savrupā programmā. Potenciālie debitori, kuri interesējas par cilvēkresursu spēju vērtēšanu finanšu un operāciju programmās, var to darīt, izmantojot bezmaksas 30 dienas izmēģinājuma darbību kopā ar demonstrācijas datiem. Dynamics 365 Finanses ietvers personāla vadības iespējas, kas tiks iesniegtas finanšu infrastruktūrasm, sapludinot savrupu programmu. Papildinformāciju [skatiet sadaļu HR piedāvājumu sapludināšana sniedz jums iespējas kopā ar debitoriem](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers) . Lai iegūtu plašāku informāciju par Dynamics 365 finanšu izmēģinājuma versijām, skatiet pakāpenības [rokasgrāmatu](../fin-ops-core/fin-ops/get-started/before-you-buy.md). 


Pirms pirmās smilškastes vai ražošanas vides nodrošināšanas, iespējams, vēlēsieties nodrošināt [Human Resources apgrozījuma vidi](https://go.microsoft.com/fwlink/p/?LinkId=2115962), lai validētu Human Resources funkcionalitāti. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot Human Resources sistēmas administrēšanu. 

Izmēǵinājuma vides ļauj novērtēt cilvēkresursu funkciju personām, kurām vēl nav piekļuves Human Resources videi. Ja nodrošināt izmēģinājuma vidi un autentificētajam lietotājam jau ir piekļuve vienai vai vairākām esošām Human Resources vidēm, lietotājs tiks pārvirzīts uz esošo vidi vai vižu sarakstu.

Izmēģinājuma vides vides nav paredzētas izmantošanai kā ražošanas vides. Tās ir ierobežotas līdz 30 dienu pārbaudes periodam. Kad beidzas izmēģinājuma periods, vide un visi dati tiek dzēsti un nevar tikt atgūti. Vidi nevar pārvērst par smilškastes vai ražošanas vidi. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

Izveidojot Human Resources izmēģinājuma vidi, nomniekam tiek izveidota arī Power Apps izmēģinājuma vide un saistīta ar Human Resources vidi. Power Apps videi, kas tiek nodēvēta par "TestDrive", ir tāds pats izmēģinājuma periods kā Human Resources videi.

> [!NOTE]
> Human Resources izmēģinājuma vides nodrošināšana neizdosies, ja autentificētajam lietotājam nav atļaujas izveidot Power Apps izmēģinājuma vides. Lietotājam jābūt iekļautam lietotāju grupā, kura var izveidot izmēģinājuma vides Power Platform administrēšanas centrā. Papildinformāciju skatiet rakstā [Pārvaldīt, kuri var izveidot un pārvaldīt vides Power Platform administrēšanas centrā](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Human Resources vižu plānošana

Pirms jūs izveidojiet pirmo Human Resources vidi, jums uzmanīgi jāplāno jūsu projekta vides vajadzības. Human Resources pamata abonementā ir ietvertas divas vides: ražošanas vide un smilškastes vides. Atkarībā no projekta sarežģītības, iespējams, ir jāiegādājas papildu smilškastes vides, lai atbalstītu projekta aktivitātes. 

Papildu vides apsvērumi.

- **Datu migrācija**: jums var būt nepieciešams apsvērt papildu vidi datu migrācijas aktivitātēm, lai ļautu jūsu smilškastes vidi izmantot testēšanas nolūkiem visā projektā. Ja ir papildu vide, testēšanas un konfigurēšanas laikā datu migrācijas aktivitātes var turpināties dažādās vidēs vienlaicīgi.
- **Integrācija**: jums var būt nepieciešams apsvērt papildu vidi, lai konfigurētu un testētu integrācijas. Tās varētu ietvert tādas vietējā integrācijas kā Ceriforce dayforce vai LinkedIn Talent Hub integrācijas vai pielāgotas integrācijas, piemēram, algas, kandidātu izsekošanas sistēmas vai atvieglojumu sistēmas un nodrošinātāju integrācijas.
- **Apmācība**: iespējams, būs nepieciešama atsevišķa vide, kas konfigurēta ar apmācību datu kopu, lai darbiniekus apmācītu par to, kā lietot jauno sistēmu. 
- **Vairākfāžu projekts**: jums var būt nepieciešama papildu vide, lai atbalstītu konfigurāciju, datu migrāciju, testēšanu vai citas aktivitātes projekta fāzē, kas tiek plānota pēc sākotnējās projekta uzsākšanas.

 > [!IMPORTANT]
 > Apsverot vidi, mēs iesakām tālāk minētos aspektus.
 > - Izmantojiet savu ražošanas vidi visā projektā kā jūsu GOLD konfigurācijas vidi. Tas ir būtiski, jo ražošanas vidē nevar kopēt smilškastes vidi. Tādēļ, kad sāksit darbu, jūsu GOLD vide ir jūsu ražošanas vide un jūs izpildīsit savas pārslēgšanas darbības šajā vidē.</br></br>
 > - Lai veiktu pārbaudāmā objekta pārslēgšanu pirms darbība sākšanas, izmantojiet izmēģināšanas vai citu vidi. To var izdarīt, atsvaidzinot ražošanas vidi ar jūsu GOLD konfigurāciju smilškastes vidē.</br></br>
 > - Saglabājiet detalizētu pārslēgšanas kontrolsarakstu, kas ietver visas datu pakotnes, kas nepieciešamas gala datu migrācijai ražošanas vidē darba sākšanas pārslēgšanas laikā.</br></br>
 > - Izmantojiet savu izmēģināšanas vidi visā projektā kā jūsu TEST vidi. Ja jums ir nepieciešamas papildu vides, jūsu organizācija var iegādāties tās par papildu samaksu.</br></br>

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana

Lai lietotu LCS un pārvaldītu savas Human Resources vides, vispirms ir jāizveido LCS projekts.

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/Logon/Index), izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai.

   > [!NOTE]
   > Lai nodrošinātu sekmīgu nodrošināšanu, kontam, kuru izmantojat Human Resources vides nodrošināšanai, ir jābūt piešķirtam vai nu **Sistēmas administratora**, vai **Sistēmas pielāgotāja** lomai Power Apps vidē, kas saistīta ar Human Resources vidi. Papildu informāciju par drošības lomu piešķiršanu lietotājiem Power Platform, skatiet sadaļā [Lietotāju drošības konfigurēšana resursiem](/power-platform/admin/database-security).

2. Atlasiet pluszīmi (**+**), lai izveidotu projektu.

3. Kā produkta nosaukumu un produkta versiju atlasiet **Microsoft Dynamics 365 Human Resources**.

4. Atlasiet metodoloģiju **Dynamics 365 Human Resources**.

5. Atlasiet **Izveidot**.

Informāciju par to, kā sākt darbu ar Human Resources, skatiet **Human Resources** metodoloģijā, ko izveidojāt savā jaunajā projektā. Kad projekta izveidošana ir pabeigta, izpildiet tālāk minēto procedūru, lai nodrošinātu savu Human Resources vidi.

## <a name="provision-a-human-resources-project"></a>Human Resources projekta nodrošināšana

Kad esat izveidojis LCS projektu, varat nodrošināt Human Resources kādā vidē.

1. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.

2. Norāda, vai šī vide ir Human Resources ražošanas vai smilškastes instance. Smilškastes instancēs varētu būt pieejami agrīni priekšskatījuma līdzekļi, lai varētu agri veikt testēšanu un saņemt atsauksmes.
   
    > [!NOTE]
    > Human Resources instances tipu nevar mainīt pēc iestatīšanas. Pirms turpināt, pārbaudiet, vai ir atlasīts pareizais instances tips.</br></br>
    > Human Resources instances veids ir neatkarīgs no Microsoft Power Apps vides instances veida, kuru iestatāt Power Apps administrēšanas centrā.
    
3. Atlasiet opciju **Iekļaut demonstrācijas datus**, ja vēlaties konkrētajā vidē iekļaut to pašu demonstrācijas datu kopu, kas izmantota Human Resources izmēģinājuma vidē. Demonstrācijas dati ir izdevīgi ilgtermiņa demonstrācijas vai apmācības vidē, un tos nekādā gadījumā nedrīkst lietot ražošanas vidē. Jums ir jāizvēlas šī opcija pēc sākotnējās izvietošanas. Esošu izvietošanu vēlāk nevar atjaunināt.

4. Human Resources vienmēr tiek nodrošināta Microsoft Power Apps vidē, lai iespējotu Power Apps integrāciju un paplašināmību. Pirms turpināšanas izlasiet šī raksta sadaļu “ Power Apps vides izvēle”. Ja jums vēl nav pieejama Power Apps vide, pakalpojumā LCS atlasiet Pārvaldīt vides vai pārejiet uz Power Apps administrēšanas centru. Pēc tam izpildiet norādījumus par procedūru [Izveidot Power Apps vidi](/powerapps/administrator/create-environment).

5. Atlasiet vidi, kurā nodrošināt Human Resources.

6. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

   Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

7. Lai izmantotu jauno vidi, atlasiet **Pieteikties Human Resources**.

    > [!NOTE]
    > Ja vēl neesat izrakstījies no gala prasībām, projektā varat izvietot Human Resources testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

## <a name="select-a-power-apps-environment"></a>Atlasiet Power Apps vidi

Varat integrēt un paplašināt Human Resources datu izmantošanu, izmantojot Power Apps rīkus. Papildinformāciju par Power Apps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par Power Apps vidēm](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Izvēloties Power Apps vidi, kurā izvietot Human Resources, ņemiet vērā tālāk sniegtos norādījumus. 

1. Pakalpojumā LCS atlasiet **Pārvaldīt vides**. Jūs varat arī doties uzreiz uz Power Apps administrēšanas centru, kur varat skatīt esošās vides un izveidot jaunas vides.

2. Katra Human Resources vide ir kartēta atsevišķā Power Apps vidē.

3. Power Apps vide satur Human Resources, kā arī atbilstošās Power Apps, Power Automate un Dataverse programmas. Ja tiek dzēsta Power Apps vide, kopā ar to tiek dzēstas arī programmas. Kad nodrošināt Human Resources vidi, varat nodrošināt vai nu vidi **Izmēģinājumversija**, vai **Ražošana**. Vides tips ir jāizvēlas atkarībā no veida, kādā šī vide tiks izmantota. 

4. Ir jāapsver datu integrācijas un pārbaudes metodes, piemēram, smilškastes, UAT vai ražošanas. Uzmanīgi apsveriet izvietojuma saistīšanas iespējas, jo nevar viegli mainīt to, kura Human Resources vide ir kartēta uz Power Apps vidi.

5. Tālāk minētās Power Apps vides nevarat izmantot kā Human Resources vides. Tie ir filtrēti no atlases saraksta sistēmā LCS:
 
    - **Noklusējuma Power Apps vides** — lai gan katrs nomnieks tiek automātiski nodrošināts ar noklusējuma Power Apps vidi, mēs neiesakam tās izmantot personāla vadības sistēmā. Visi nomnieku lietotāji var piekļūt Power Apps videi un, pārbaudot un pētot ar Power Apps vai Power Automate integrācijām, var netīši bojāt ražošanas datus.
   
    - **Izmēģinājuma vides** – šīs vides tiek veidotas ar beigu datumu. Pēc termiņa beigām jūsu vide un visas Human Resources instances, kas atrodas tajā, tiks automātiski noņemtas.
   
    - **Neatbalstītas ģeogrāfiskās vietas** — videi ir jābūt atbalstītā ģeogrāfiskā atrašanās vietā. Papildinformāciju skatiet sadaļā [Atbalstītas ģeogrāfiskās atrašanās vietas](hr-admin-setup-provision.md#supported-geographies).

6. Divkāršās rakstīšanas iespējas Human Resources datu integrēšanai ar Power Apps vidi var izmantot tikai tad, ja videi ir atlasīta opcija **Iespējot Dynamics 365 programmas**. Papildu informāciju par divkāršo rakstīšanu skatiet sadaļā [Divkāršās rakstīšanas sākumlapa](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md).

    > [!NOTE]
    > Laikā, kad tiek izveidota Power Apps vide, ir jābūt atlasītai opcijai **Iespējot Dynamics 365 programmas**. Ja opcija netiek atlasīta nodrošināšanas laikā, jūs nevarēsit izmantot divkāršo rakstīšanu, lai integrētu datus starp Dynamics 365 Human Resources un Power Apps vidi vai lai vidē instalētu Dynamics 365 programmas, piemēram Dynamics 365 Sales un Field Service. Šī opcija nav atgriezeniska. Papildu informāciju skatiet Power Platform dokumentācijas vietnes sadaļā [Būtiski apsvērumi, izveidojot jaunu vidi](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment).

7. Kad ir noteikta izmantošanai pareizā vide, var pāriet pie nodrošinājuma procesa. 

### <a name="supported-geographies"></a>Atbalstītas ģeogrāfiskās vietas

Human Resources pašlaik atbalsta šādas ģeogrāfiskās vietas:

- ASV
- Eiropa
- Apvienotā Karaliste
- Austrālija
- Kanāda
- Āzija 

Veidojot Human Resources vidi, atlasiet Power Apps vidi, kuru saistīt ar Human Resources vidi. Tādā gadījumā Human Resources vide tiek nodrošināta tajā pašā Azure ģeogrāfiskajā vietā, kurā ir atlasīta Power Apps vide. Varat atlasīt, kur fiziski atrodas Human Resources vide un datu bāze, atlasot ģeogrāfiju, veidojot Power Apps vidi, kas tiks saistīta ar Human Resources vidi.

Varat atlasīt Azure *ģeogrāfiju*, kurā tiek nodrošināta vide, taču nevarat atlasīt noteiktu Azure *reģionu*. Automatizācija nosaka specifisku ģeogrāfijas reģionu, kurā tiek izveidota vide, lai optimizētu noslodzes līdzsvarošanu un veiktspēju. Informāciju par Azure ģeogrāfiskām vietām un reģioniem varat atrast [Azure ģeogrāfijas](https://azure.microsoft.com/global-infrastructure/geographies) dokumentācijā.

Human Resources vides dati vienmēr būs ietverti Azure ģeogrāfijā, kurā tā ir izveidota. Tomēr šī informācija vienmēr netiks ietverta vienā Azure reģionā. Ārkartas gadījuma seku novēršanas nolūkā dati tiks replicēti gan primārajā Azure reģionā, gan sekundārajā neveiksmju reģionā ģeogrāfijā.

 > [!NOTE]
 > Human Resources vides migrācija no viena Azure reģionu citā netiek atbalstīta.

## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi

Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Jums ir īpaši jāpiešķir piekļuve citiem programmas lietotājiem. Jums ir jāpievieno lietotāji un jāpiešķir viņiem atbilstošās lomas Human Resources vidē. Plašāku informāciju skatiet tēmā [Jaunu lietotāju izveide](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [Drošības lomu piešķiršana lietotājiem](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
