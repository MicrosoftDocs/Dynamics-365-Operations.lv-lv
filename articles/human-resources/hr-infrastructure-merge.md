---
title: Dynamics 365 Human Resources infrastruktūras sapludināšanas apskats
description: Šajā rakstā aprakstīta Microsoft Dynamics 365 Human Resources infrastruktūras sapludināšana.
author: twheeloc
ms.date: 10/24/2022
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
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732768"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources infrastruktūras sapludināšana 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics cilvēkresursi 365

Microsoft Dynamics 365 Human Resources nodrošina rīkus, kas HR grupām palīdz palielināt organizācijas agveidošanu, pārveidot darbinieku pieredzi un optimizēt HR programmas, lai izveidotu darba vietu, kur cilvēki un uzņēmums var pieaugt. Papildinformāciju skatiet Dynamics 365 Human Resources sadaļā [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Pārveidot darbinieku pieredzi.** Saglabājiet augšējos izpildītājus, sniedzot vadītājiem un darbiniekiem iespējas, izmantojot piesaistīto pašapkalpošanās pieredzi, kas vada iesaisti un izaugsmi.
- **optimizēt HR programmas;** Palīdziet samazināt darbības izmaksas un izveidot uz cilvēkiem vērstus atvaļinājumus un kavējumus, laiku, atvieglojumus un kompensācijas pārvaldības programmas.
- **Palieliniet organizācijas agtiku.** Iespējojiet HR darbību ar veiklību Dataverse Microsoft Power Platform, kas uzņēmumam nepieciešama, izmantojot un lai centralizētu cilvēku datus un viegli paplašinātu Dynamics 365 Human Resources.
- **Apskatiet darbaspēka ieskatus.** Veiciet uz datiem balstītus lēmumus, spēja analizēt un vizualizēt cilvēku datus jebkurā ierīcē pieejamos bagātinātos informācijas paneļos.

## <a name="human-resources-infrastructure-merge"></a>Cilvēkresursu infrastruktūras sapludināšana

Dynamics 365 Human Resources ir savrupa programma, kas pašlaik izmanto atšķirīgu infrastruktūru nekā citas finanšu un operāciju programmas, piemēram, Dynamics 365 Finanses vai Dynamics 365 Supply Chain Management. Infrastruktūras sapludināšana apvienos tajā Dynamics 365 Human Resources pašā infrastruktūra kā citas finanšu un operāciju programmas.

Lai iegūtu plašāku informāciju par cilvēkresursu infrastruktūras sapludināšanu, skatiet sadaļu [HR piedāvājumu apvienošana](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Atbildes uz bieži uzdotiem jautājumiem skatiet Personāla vadības [infrastruktūras sapludināšanas FAQ](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Debitoru migrācija pret debitoru sapludināšanu

Kā daļa no infrastruktūras sapludināšanas visas Personāla vadības programmas iespējas ir padarītas pieejamas finanšu un operāciju vidēs. Klienti var migrēt savas cilvēkresursu vides, izmantojot migrācijas rīku, kas ir pieejams pakalpojumos Microsoft Dynamics Lifecycle Services. Pēc izvēles viņi var arī sapludināt datus ar savām esošajām finanšu un operāciju vidēm. 

Klientu migrācija un debitoru sapludināšana atšķiras šādā veidā:

- **Debitoru migrācija** — automatizēto migrācijas rīku izmanto, lai veiktu debitoru datu bāzes "liftu un maiņu migrāciju" (kustību) no cilvēkresursu infrastruktūras uz finanšu un operāciju infrastruktūru. Rezultāts ir jauna finanšu un operāciju vide, kas izmanto klienta Cilvēkresursu datu bāzi. 
- **Debitoru sapludināšana** - šo papildu darbību nav pieprasa Microsoft. Tas ir paveikts debitora izvēles iespēju un debitora paša laika skalas laikā. Šī soļa laikā debitora dati tiek pārvietoti uz esošo vidi, piemēram, Finanšu vai projekta operāciju vidē. Tas ir lielākā daļa manuālu un to var izdarīt, izmantojot datu pārvaldības struktūras (DMF) datu elementus. 

## <a name="planning-a-human-resources-environment-migration"></a>Cilvēkresursu vides migrācijas plānošana

Kā daļa no infrastruktūras sapludināšanas visiem debitoriem būs nepieciešams migrēt savas esošās personāla vadības vides no savrupas infrastruktūras. Lai palīdzētu šim procesam, ieteicams izmantot automātisko migrācijas rīku pakalpojumu Lifecycle Services, lai pārvietotu pašreizējās vides uz jauno infrastruktūru. 

Tālāk sadaļās ir sniegta plašāka informācija par to, kā izmantot Lifecycle Services rīkus, lai migrētu savrupu cilvēkresursu vidi. 

Klientiem, kas plāno migrāciju, var būt šādas izredzes:

- Lai varētu migrēt ražošanas vidi, visiem debitoriem būs jāmigrē kastu vide. 
- Migrācijas rīku rīks iespējo tikai migrēšanu no kastēs uz kasti un ražošanu pēc ražošanas. Tādējādi vides tips noteiks, kura vide var tikt atbilstoši migrēta. 
- Debitori var migrēt tik daudz kastītes, cik nepieciešams, pirms migrēt ražošanas vidi, ja ir pieejams mērķa vadīklu slots. Debitori var arī dzēst migrēto vadīklu un nomusēt vairākas reizes. 
- Ja kastu migrācija neizdodas vai ja vēlaties sākt no jauna, ir iespējams dzēst finanšu un operāciju infrastruktūras vidi un mainīt to pašu vidi.
- Pēc migrācijas jūsu Cilvēkresursu vides URL atšķirsies.
- Plānojiet piemērotu dīkstāves daudzumu ražošanas vides migrācijai. Plānotais laika periods automatizētās migrācijas procesa pabeigšanai ir trīs līdz četras stundas. Laika periods atšķirsies atkarībā no jūsu organizācijas datiem. Ir jāpārbauda laika daudzums, kas nepieciešams jūsu kastēs vides migrācijas laikā, un ir jāpārbauda laiks, kad veicami papildu manuālie uzdevumi.

> [!IMPORTANT] 
> Kad ražošanas vide ir veiksmīgi migrēta uz finanšu un operāciju infrastruktūru, avota savrupa ražošanas vide tiek automātiski dzēsta. Migrēto ražošanas vidi nedrīkst dzēst. 

Migrācijas process ir ļoti automātisks. Tomēr biznesa lietotājiem būs jāveic daži manuāli soļi un pārbaude pēc migrācijas.

Jāveic šādi manuālie soļi:

- Izveidojiet jaunu Lifecycle Services projektu migrācijai.
- Pārskatiet ikvienu integrāciju savā vecajā vidē, norādot integrāciju uz jaunajiem URL/galapunktiem, balstoties uz katru integrācijas konfigurāciju.
- Atsvaidziniet datu krātuvi iegultiem Power BI pārskatiem.
- Atsvaidziniet datu elementu sarakstu no DMF darbvietas.
- Lai saņemtu palīdzību, sazinieties ar pakalpojumu Lifecycle Services.
- Izveidojiet finanšu kalendārus.

Automātisko procesu laikā ir jāveic tālāk norādītās darbības, un tās ir jāpārbauda:

- Datu:

    - Konfigurācijas
    - Drošības lomas (tostarp pielāgotās lomas)
    - Darbplūsmas
    - Personalizēšanas un saglabātie skati
    - Transakcijas
    - Pielāgotie lauki
    - Pielikumi

- Datu pārvaldība – uzdāciet savu datu bāzi (BYOD).
- Līdzekļu pārvaldība - iespējotās/deaktivizētās funkcijas.
- Iegulto Power Apps.
- Power Platform administrēšanas centra pievienotā vide (tikai ražošana).
- Pakešuzdevumi.
- Katrai juridiskajai personai tiek izveidota tukša Virsgrāmata. Katrai virsgrāmatai tiek iestatīts noklusējuma maiņas kursa tips un uzskaites valūta.
- Jauns kontu plāns tiek automātiski izveidots un saistīts ar Virsgrāmatas lapu **katrai** juridiskajai personai. Personāla vadības vidē konfigurētās finanšu dimensijas automātiski tiks pievienotas jaunai konta struktūrai un piesaistītas Virsgrāmatai. 

> [!NOTE]
> Finanšu un operāciju infrastruktūrai kā daļa no Dynamics 365 finanšu produkta ir nepieciešama Virsgrāmata. Savrupajā programmā izmantotais pielāgotās Dynamics 365 Human Resources dimensijas kontrolleris nav pieejams. Sapludinātā cilvēkresursu infrastruktūra ir atkarīga no finanšu loģikas, lai parādītu finanšu dimensijas cilvēkresursu **modulī**. Lai uzzinātu vairāk par kontu plānu un finanšu dimensijām, skatiet [šeit](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Apsvērumi

- Migrācija uz vidēm vienmēr būs pēdējā vispārīgi pieejamā (GA) versijā. Atkarībā no migrācijas un testēšanas plāna, ja migrēšanas pārbaude kastēs vides bija citā versijā, mēs iesakām pārbaudīt slīpstlodziņa migrāciju tajā pašā versijā, kurā atrodas ražošanas vide. 
- Migrācijas laikā migrētās vides tiks novietotas tajā pašā reģionā, kur avota savrupās cilvēkresursu vides.

## <a name="licensing"></a>Licencēšana

Nepastāv izmaiņas licencēšanai šādos Dynamics 365 Human Resources apgabalos: 

- **Minimālā licences pirkšanas prasība**
- **Licences ražošanas un kases vides vajadzībām — ja jums ir atsevišķas** personāla vadības licences, kas piešķir vienu ražošanas vidi un vienu kases vides vidi, finanšu un operāciju infrastruktūrai ir pieejams vienāds licenču skaits bez papildu izmaksām.
- **Papildu noliktavas kastītes** licences — ja esat iegādājies papildu tekstlodziņa licences savrupai personāla vadības programmai, tas pats kastēs licenču skaits ir pieejams standarta pieņemšanas testa (noliktavas kastīte) videi finanšu un operāciju infrastruktūrai bez papildu izmaksām. 
