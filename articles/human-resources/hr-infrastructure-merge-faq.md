---
title: Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu
description: Šajā rakstā ir atbildes uz bieži uzdotiem jautājumiem par Microsoft un finanšu Dynamics 365 Human Resources un operāciju programmu infrastruktūras sapludināšanu.
author: twheeloc
ms.date: 09/13/2021
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
ms.openlocfilehash: 32698d887b4d228ded588984b09068e3e2fef9a4
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702072"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Kas ir Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources nodrošina rīkus, kas HR grupām palīdz palielināt organizācijas agveidošanu, pārveidot darbinieku pieredzi un optimizēt HR programmas, lai izveidotu darba vietu, kur cilvēki un uzņēmums var pieaugt. Papildinformāciju skatiet Dynamics 365 Human Resources sadaļā [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **pārveidot darbinieku pieredzi;** Saglabājiet augšējos izpildītājus, sniedzot vadītājiem un darbiniekiem iespējas, izmantojot piesaistīto pašapkalpošanās pieredzi, kas vada iesaisti un izaugsmi.
- **optimizēt HR programmas;** Samaziniet darbības izmaksas un izveidojiet cilvēku uz laiku centrtīvus atvaļinājumus un kavējumus, laiku, atvieglojumus un atlīdzības pārvaldīšanas programmas.
- **Palieliniet organizācijas agtiku.** Iespējojiet HR darbību ar veiklību Dataverse Microsoft Power Platform, kas uzņēmumam nepieciešama, izmantojot un lai centralizētu cilvēku datus un viegli paplašinātu Dynamics 365 Human Resources.
- **Apskatiet darbaspēka ieskatus.** Veiciet uz datiem balstītus lēmumus, spēja analizēt un vizualizēt cilvēku datus jebkurā ierīcē pieejamos bagātinātos informācijas paneļos.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūras sapludināšanas vērtība un atvieglojumi

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas ir Dynamics 365 Human Resources infrastruktūras sapludināšana?

Pašlaik programmā Dynamics 365 ir divas atsevišķas HR spēju kopas divās dažādās infrastruktūras:

- **Dynamics 365 Human Resources**– atsevišķa programma, kas darbojas neatkarīgs infrastruktūrai. Kad palaista šī programma, infrastruktūra tika atdalīta no citām Dynamics 365 operāciju programmām. Mūsu debitori izmanto šo programmu, lai palielinātu organizācijas agtiku, optimizētu HR programmas, pārveidotu darbinieku pieredzi un iegūtu darbaspēka ieskatus.
- **HR modulis** — mantojuma iespēju kopa, kas iepriekš bija daļa no unificētās operāciju licencēšanas noliktavas vienības (NV). HR modulis darbojas finanšu un operāciju infrastruktūrai, kas visās operāciju programmās ir vienāda. Šīs programmas ietver Dynamics 365 Finanses Dynamics 365 Project Operations un Dynamics 365 Supply Chain Management. Debitori saņēma HR iespējas kā daļu no Dynamics 365 finansēm vai Dynamics 365 Supply Chain Management.

Pēdējo trīs gadu laikā korporācija Microsoft hr modulim nav pievienojusi jaunas iespējas vai uzlabojumus. Tā vietā mūsu rīcības plāna ieguldījumi ir fokusēti uz programmu Dynamics 365 Human Resources.

Ieviešot šīs divas iespējas vienā un tajā pašā infrastruktūra, mēs palīdzēsim klientiem iegūt šādas priekšrocības:

- Uzlabojumi, kas pievienoti pēdējo trīs gadu Dynamics 365 Human Resources laikā, tostarp uzlaboti atvaļinājumi un kavējumi, atvieglojumu pārvaldība un pārskatu veidošana.
- Uzlabota paplašināmība, izmantojot Microsoft Power Platform un spēju paplašināt biznesa loģiku, lai personalizētu lapas.
- Uzlabota izvietošana, atjauninājumi un uzturēšana, kas ir konsekventi lietojumprogrammas dzīves cikla pārvaldības (INSTALĒŠANU), dzīves cikla pakalpojumu, ģeogrāfiskās pieejamības un citu informāciju ziņā.
- Vairāk konstruēšanas komandas lieto koplietotos pakalpojumus, rīkus un samazinātās platformu izmaksas.

Šī pāreja ietekmēs debitorus, kuri pašlaik izmanto vai nu mantojuma Dynamics 365 Human Resources HR moduli.

## <a name="glossary-of-terms-used-in-this-faq"></a>Šajā FAQ lietoto terminu glosārijs

- **Dynamics 365 Human Resources**– mūsu pašreizējā un nākotnes prece, kas piedāvā HR iespējas tirgū.
- **HR modulis** — mantojuma iespēju kopa, kas iepriekš ir piešķirta unificēto operāciju piedāvājumam. Iespējas ir iespējotas, ja debitoram pieder Dynamics 365 Finanses vai Dynamics 365 Supply Chain Management.
- **Finanšu un operāciju** infrastruktūra – izstrādes arhitektūra, ko izmanto operāciju portfeisā, ietverot Dynamics 365 Finanses Dynamics 365 Supply Chain Management un Dynamics 365 Project Operations. Šī ir infrastruktūra, kas tiks izmantota turpmāk. Bieži uzdotajos bieži uzdotajos jautājumiem termins *"sapludinātā* infrastruktūra" attiecas uz finanšu un operāciju vidi.
- **Personāla vadības infrastruktūra** – izstrādes arhitektūra, kas tika iepriekš izmantota programmai Dynamics 365 Human Resources. Infrastruktūras sapludināšanas projekts uzved Dynamics 365 Human Resources finanšu un operāciju infrastruktūru. Savrupa infrastruktūra tiks pārtraukta.

## <a name="general-questions-about-the-infrastructure-merge"></a>Vispārēji jautājumi par infrastruktūras sapludināšanu

### <a name="will-customers-lose-any-features-or-capabilities"></a>Vai debitori zaudēs jebkādas funkcijas vai iespējas?

Mūsu mērķis ir minimizēt ietekmi, kas šai pārejai ir uz debitoriem. Mēs nenovācām līdzekļus vai iespējas. Starp moduli un HR moduli būs funkcionāla Dynamics 365 Human Resources pārība. Gadījumos, kad funkcija pastāv abās infrastruktūras, tiks Dynamics 365 Human Resources izmantota pieredze.

### <a name="will-the-user-experience-change"></a>Vai lietotājam tiks mainīta pieredze?

Lietotāja pieredze saskanēs ar standarta Dynamics 365 platformu pieredzi. Lai gan vispārīgā informācijas paneļu un izvēlņu pieredze joprojām būs līdzīga, tā tiks saskaņota ar standarta Dynamics 365 finanšu programmas pieredzi. Navigācija ietvers gan moduļus, gan darbvietas, atļaujot izlasei, kā arī citu informāciju. Darbvietas Dynamics 365 Human Resources, piemēram, Personāla **vadība** un **Cilvēki**, saplūdīs finanšu un operāciju infrastruktūras sistēmā. Nākotnē jaunās iespējas tiks piegādātas, izmantojot Līdzekļu pārvaldību, kas ļauj debitoriem skatīt jaunus līdzekļus un izlemt, kurus vēlaties izmantot. Papildinformāciju skatiet līdzekļu [pārvaldības pārskatā un](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lietotāja [interfeisa dokumentācijā](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Kad tiks pabeigta Dynamics 365 Human Resources infrastruktūras sapludināšana?

Infrastruktūras sapludināšana izbeigsies fāzēs, lai sniegtu debitoriem laiku plānot un veikt nepieciešamos soļus. Dynamics 2021 2. laidienā sākām izlaist iespējas. Līdz 2022. gada 2. kopuma beigām mēs šim projektam plānojam pabeigt visus produktu izstrādes darbus. Ņemiet vērā, ka laika skala var tikt mainīta. Jaunāko informāciju skatiet [nodot izpildei plānus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Kādas apmācības un resursi būs pieejami, lai palīdzētu ar infrastruktūras saplūšanu?

Mēs sniedzam dokumentāciju, kas detalizēti apraksta katru infrastruktūras sapludināšanas procesa soli. Ja nepieciešams, mēs sniedzam papildu apmācību resursus, piemēram, videoklipus un apmācību, kā arī, lai palīdzētu klientiem un partneriem veikt gludu pāreju.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Vai pēc infrastruktūras sapludināšanas pabeigšanas pastāvēs izmaiņas izstrādes iespējām?

Papildinformāciju par izstrādes iespējām skatiet sadaļā Mājas [lapas izstrāde un pielāgošana](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Līdzekļu pieejamības jautājumi

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Vai LinkedIn Talantu pārkraušanas centra integrācija darbojas finanšu un operāciju infrastruktūrai?

Nē, LinkedIn Talantu pārkraušanas punktu integrācija nebūs daļa no sapludinātās infrastruktūras. Publiskās programmas programmēšanas interfeisi (API) ir pieejami, lai veidotu integrācijas ar personāla atlases un kandidāta izsekošanas risinājumiem. Klientiem, kas plāno izmantot LinkedIn Talantu pārkraušanas punktu, jāstrādā ar savu Microsoft partneri, lai integrētu, izmantojot sniegtos API. Papildinformāciju par kandidātu izsekošanas sistēmas (ATS) integrācijas API skatiet kandidāta izsekošanas [sistēmas integrācijas API ievadā](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Vai šobrīd pieejamās iespējas būs pieejamas tikai Dynamics 365 Human Resources (piemēram, atvaļinājumu vadība un atvieglojumu pārvaldība) pēc sapludināšanas pabeigšanas?

Jā. Visas Dynamics 365 Human Resources programmas iespējas tiek atvestas uz finanšu un operāciju infrastruktūru. Funkcijas tiks padarītas pieejamas fāzētajā pieejai. Lai iegūtu informāciju par sapludinātās infrastruktūras līdzekļu pieejamību, regulāri pārskatiet izlaišanas [plānus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Vai ceristruktūras integrācijas būs Dynamics 365 Human Resources pieejamas pēc infrastruktūras sapludināšanas pabeigšanas?

Ceriļļu veido V2 integrāciju, izmantojot Dynamics 365 Human Resources algu API priekšrocības. Uz failu balstīta integrācija, kas pašlaik Dynamics 365 Human Resources pastāv, netiks migrēta uz finanšu un operāciju infrastruktūru. Papildinformāciju skatiet sadaļā [Algas API ievads](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Vai tiks iekļauta darbinieka funkcionalitātes izsekošana kandidāts vai uzņēmuma darbība/offboarding?

Iepriekšējos laidienos esam izveidojuši ATS integrācijas API, lai dotu iespēju partneriem un debitoriem izveidot ATS integrācijas ar Cilvēkresursiem. Papildu ar ATS saistītā funkcionalitāte bija pieejama 1. laivā. Mēs turpināsim uzlabot šos API turpmākajos laidienos.

HR funkcionalitāte, kas šobrīd pastāv finanšu un operāciju infrastruktūrai, ietver dažas personāla atlases pārvaldības funkcijas, kas nepastāv Dynamics 365 Human Resources. Kad infrastruktūras sapludināšana ir pabeigta, šī funkcionalitāte būs pieejama visiem personāla vadības debitoriem. Šī funkcionalitāte nodrošina ērtu ATS funkcionalitāti. Taču turpmāk neplānojam izvērst šo funkcionalitāti. Debitori, kuriem nepieciešama plašāka funkcionalitāte, var izmantot partnera ATS integrācijas priekšrocības. Papildinformāciju par ATS integrācijas API skatiet kandidāta izsekošanas [sistēmas integrācijas API ievadā](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Vai Dynamics AX 2012 jaunināšanas rīki tiks izmantoti HR AX moduļa jaunināšanai programmā 2012 uz Dynamics 365 Human Resources programmu?

Jā. Jaunināšana no Dynamics AX 2012 Dynamics 365 Human Resources uz to pašu jaunināšanas ceļu un rīku rīkņus, kas tiek izmantoti, lai jauninātu uz citu Dynamics 365 operāciju programmu jaunāko versiju, piemēram, Dynamics 365 Finanses vai Dynamics 365 Supply Chain Management.

Papildinformāciju par migrāciju uz finanšu un operāciju infrastruktūru skatiet personāla vadības [debitoru migrācijas FAQ](./customer-migration.md).
