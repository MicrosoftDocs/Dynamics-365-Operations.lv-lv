---
title: Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu
description: Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par infrastruktūras sapludināšanu Microsoft Dynamics 365 Human Resources un Finance and Operations programmām.
author: twheeloc
ms.date: 11/15/2022
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
ms.openlocfilehash: 7325231718d7387450391b16b2866f9a2c05bdc4
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779640"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Kas ir Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources nodrošina rīkus, kas palīdz personāla grupām palielināt organizācijas veiklību, pārveidot darbinieku pieredzi un optimizēt cilvēkresursu programmas, lai izveidotu darba vietu, kur cilvēki un uzņēmums var attīstīties. Lai uzzinātu vairāk par Dynamics 365 Human Resources, skatiet [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Pārveidojiet darbinieku pieredzi.** Saglabājiet labākos izpildītājus, sniedzot iespējas vadītājiem un darbiniekiem, izmantojot savienotas pašapkalpošanās iespējas, kas veicina iesaistīšanos un izaugsmi.
- **Optimizējiet cilvēkresursu programmas.** Samaziniet darbības izmaksas un izveidojiet uz cilvēkiem orientētas atvaļinājuma un prombūtnes, laika, pabalstu un kompensāciju pārvaldības programmas.
- **Palieliniet organizācijas veiklību.** Ļaujiet HR darboties ar veiklību, kas nepieciešama biznesam, izmantojot Dataverse un centralizējot cilvēku datus un Microsoft Power Platform viegli paplašinot Dynamics 365 Human Resources.
- **Atklājiet ieskatus par darbaspēku.** Pieņemiet uz datiem balstītus lēmumus, izmantojot iespēju analizēt un vizualizēt personu datus bagātīgos informācijas paneļos, kas ir pieejami jebkurā ierīcē.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūras sapludināšanas vērtība un atvieglojumi

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas ir Dynamics 365 Human Resources infrastruktūras sapludināšana?

Pašlaik programmā Dynamics 365 ir divas atsevišķas cilvēkresursu iespēju kopas divās dažādās infrastruktūrās:

- **Dynamics 365 Human Resources**– Atsevišķa lietotne, kas darbojas neatkarīgā infrastruktūrā. Kad šī programma tika palaista, infrastruktūra tika atdalīta no citām Dynamics 365 operāciju programmām. Mūsu klienti izmanto šo lietotni, lai palielinātu organizācijas veiklību, optimizētu cilvēkresursu programmas, pārveidotu darbinieku pieredzi un gūtu ieskatu par darbaspēku.
- **HR modulis** — mantota iespēju kopa, kas iepriekš bija daļa no Unified Operations licencēšanas krājumu glabāšanas vienības (Unified Operations licensing stock keeping unit — SKU). Cilvēkresursu modulis darbojas finanšu un operāciju infrastruktūrā, kas ir vienāda visās operāciju programmās. Šīs programmas ietver Dynamics 365 finanses Dynamics 365 Project Operations un Dynamics 365 Supply Chain Management. Klienti saņēma HR iespējas kā daļu no Dynamics 365 Finance vai Dynamics 365 Supply Chain Management.

Pēdējo trīs gadu laikā Microsoft cilvēkresursu modulim nav pievienojis jaunas iespējas vai uzlabojumus. Tā vietā mūsu rīcības plāna ieguldījumi ir fokusēti uz programmu Dynamics 365 Human Resources.

Ieviešot šos divus iespēju kopumus vienā infrastruktūrā, mēs palīdzēsim klientiem iegūt šādas priekšrocības:

- Uzlabojumi, kas pievienoti Dynamics 365 Human Resources pēdējo trīs gadu laikā, tostarp uzlabots atvaļinājums un prombūtne, pabalstu pārvaldība un ziņošana.
- Uzlabota paplašināmība Microsoft Power Platform un iespēja paplašināt biznesa loģiku, lai personalizētu lapas.
- Uzlabota izvietošana, atjauninājumi un uzturēšana, kas ir konsekventa attiecībā uz lietojumprogrammu dzīves cikla pārvaldību (ALM), dzīves cikla pakalpojumiem, ģeogrāfisko pieejamību un daudz ko citu.
- Vairāk tehnoloģisko inovāciju, jo mūsu inženieru komanda izmanto koplietojamus pakalpojumus, rīkus un samazinātas platformas izmaksas.

Šī pāreja ietekmēs klientus, kuri pašlaik izmanto vienu vai otru Dynamics 365 Human Resources HR moduli.

## <a name="glossary-of-terms-used-in-this-faq"></a>Šajā bieži uzdoto jautājumu sadaļā izmantoto terminu glosārijs

- **Dynamics 365 Human Resources**– Mūsu pašreizējais un nākotnes produkts, kas piedāvā HR iespējas tirgū.
- **HR modulis** — mantoto iespēju kopums, kas iepriekš tika licencēts ar vienoto operāciju piedāvājumu. Iespējas tiek iespējotas, ja klientam pieder Dynamics 365 Finance vai Dynamics 365 Supply Chain Management.
- **Finance and operations infrastructure** — izstrādes arhitektūra, ko izmanto operāciju portfelis, tostarp Dynamics 365 Finance, Dynamics 365 Supply Chain Management un Dynamics 365 Project Operations. Šī infrastruktūra ir tā, kas tiks izmantota turpmāk. Šajā bieži uzdoto jautājumu sadaļā termins *"apvienota infrastruktūra* " attiecas uz finanšu un operāciju vidi.
- **Cilvēkresursu infrastruktūra** – izstrādes arhitektūra, kas vēsturiski tika izmantota lietotnei Dynamics 365 Human Resources. Infrastruktūras apvienošanas projekts ievieš Dynamics 365 Human Resources finanšu un operāciju infrastruktūru. Atsevišķā infrastruktūra tiks pārtraukta.

## <a name="general-questions-about-the-infrastructure-merge"></a>Vispārīgi jautājumi par infrastruktūras apvienošanu

### <a name="will-customers-lose-any-features-or-capabilities"></a>Vai klienti zaudēs kādas funkcijas vai iespējas?

Mūsu mērķis ir samazināt šīs pārejas ietekmi uz klientiem. Mēs nenoņemsim nekādus līdzekļus vai iespējas. Būs funkcionāla paritāte starp Dynamics 365 Human Resources HR moduli un to. Gadījumos, kad iezīme pastāv abās infrastruktūrās, Dynamics 365 Human Resources tiks izmantota pieredze.

### <a name="will-the-user-experience-change"></a>Vai mainīsies lietotāja pieredze?

Lietotāja pieredze atbildīs standarta Dynamics 365 platformas pieredzei. Lai gan informācijas paneļa un izvēļņu vispārējā pieredze saglabāsies līdzīga, tā tiks saskaņota ar standarta Dynamics 365 Finance programmas pieredzi. Navigācija ietvers gan moduļus, gan darbvietas, atļaus izlasi un daudz ko citu. Darbvietas Dynamics 365 Human Resources, piemēram **, personāla vadība** un personas **, apvienosies finanšu un** operāciju infrastruktūrā. Nākotnē jaunas iespējas tiks nodrošinātas, izmantojot līdzekļu pārvaldību, kas ļaus klientiem skatīt jaunos līdzekļus un izlemt, kurus līdzekļus viņi vēlas izmantot. Papildinformāciju skatiet sadaļā [Līdzekļu pārvaldības pārskats](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un [Lietotāja interfeisa dokumentācija](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Dynamics 365 Human Resources Kad tiks pabeigta infrastruktūras apvienošana?

Infrastruktūras apvienošana tiks ieviesta pa posmiem, lai dotu klientiem laiku plānot un veikt nepieciešamās darbības. Mēs sākām ieviest iespējas Dynamics 2021 laidiena 2. vilnī. Mēs plānojam pabeigt visus produktu izstrādes centienus šim projektam līdz 2022. gada 2. laidiena viļņa beigām. Ņemiet vērā, ka laika grafiki var mainīties. Jaunāko informāciju skatiet sadaļā [Laidiena plāni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Kādas apmācības un resursi būs pieejami, lai palīdzētu apvienot infrastruktūru?

Mēs sniegsim dokumentāciju, kas detalizēti apraksta katru infrastruktūras apvienošanas procesa soli. Mēs nodrošināsim papildu apmācības resursus, piemēram, video un seminārus, ja nepieciešams, lai palīdzētu klientiem un partneriem ar vienmērīgu pāreju.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Vai pēc infrastruktūras apvienošanas pabeigšanas būs izmaiņas attīstības iespējās?

Papildinformāciju par izstrādes iespējām skatiet rakstā [Sākumlapas](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md) izstrāde un pielāgošana.

## <a name="feature-availability-questions"></a>Jautājumi par līdzekļu pieejamību

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Vai LinkedIn Talent Hub integrācija darbosies finanšu un operāciju infrastruktūrā?

Nē, LinkedIn Talent Hub integrācija nebūs daļa no apvienotās infrastruktūras. Ir pieejamas publiskas lietojumprogrammu programmēšanas saskarnes (API), lai izveidotu integrāciju ar darbā pieņemšanas un kandidātu izsekošanas risinājumiem. Klientiem, kuri plāno izmantot LinkedIn Talent Hub, ir jāsadarbojas ar savu Microsoft partneri, lai veiktu integrāciju, izmantojot nodrošinātos API. Papildinformāciju par kandidātu izsekošanas sistēmas (ATS) integrācijas API skatiet rakstā [Pieteikuma iesniedzēja izsekošanas sistēmas integrācijas API ievads](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Vai iespējas, kas pašlaik ir pieejamas tikai pakalpojumā Dynamics 365 Human Resources (piemēram, atvaļinājumu pārvaldība un priekšrocību pārvaldība), būs pieejamas pēc sapludināšanas pabeigšanas?

Jā. Visas Dynamics 365 Human Resources lietojumprogrammu iespējas tiek ieviestas finanšu un operāciju infrastruktūrā. Funkcijas būs pieejamas, izmantojot pakāpenisku pieeju. Lai iegūtu jaunāko informāciju par līdzekļu pieejamību apvienotajai infrastruktūrai, regulāri pārskatiet [laidiena plānus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Vai Ceridian integrācijas ar Dynamics 365 Human Resources būs pieejamas pēc infrastruktūras apvienošanas pabeigšanas?

Ceridian pašlaik veido V2 integrāciju, ar Dynamics 365 Human Resources kuru tiek izmantotas algu API priekšrocības. Pašlaik pastāvošā Dynamics 365 Human Resources failu integrācija netiks migrēta uz finanšu un operāciju infrastruktūru. Papildinformāciju skatiet sadaļā [Algas API ievads](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Vai tiks iekļauta pretendenta izsekošana vai darbinieku piesaistīšana / izslēgšana?

Iepriekšējos laidienos mēs izveidojām ATS integrācijas API, lai partneri un klienti varētu izveidot ATS integrācijas ar personāla vadību. Papildu ar ATS saistītā funkcionalitāte kļuva pieejama 2022. gada 1. kārtā. Mēs turpināsim uzlabot šīs API turpmākajos laidienos.

Cilvēkresursu funkcionalitāte, kas pašlaik pastāv finanšu un operāciju infrastruktūrā, ietver dažas darbā pieņemšanas pārvaldības funkcijas, kas nepastāv Dynamics 365 Human Resources. Kad infrastruktūras sapludināšana būs pabeigta, šī funkcionalitāte būs pieejama visiem cilvēkresursu klientiem. Šī funkcionalitāte nodrošina vieglu ATS funkcionalitāti. Tomēr mēs neplānojam nākotnē paplašināt šo funkcionalitāti. Klienti, kuriem nepieciešama uzlabota funkcionalitāte, var izmantot partneru ATS integrācijas priekšrocības. Papildinformāciju par ATS integrācijas API skatiet rakstā [Pieteikuma iesniedzēju izsekošanas sistēmas integrācijas API ievads](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Vai Dynamics AX 2012 jaunināšanas rīki tiks izmantoti, lai 2012. gadā AX jauninātu HR moduli uz Dynamics 365 Human Resources programmu?

Jā. Jaunināšana no Dynamics 2012 uz tiks veikta pa to pašu jaunināšanas ceļu un rīkiem, kas tiek izmantoti, lai jauninātu uz AX citu Dynamics 365 operāciju programmu jaunāko versiju, piemēram, Dynamics Dynamics 365 Human Resources 365 Finance vai Dynamics 365 Supply Chain Management.

Papildinformāciju par migrāciju uz finanšu un operāciju infrastruktūru skatiet sadaļā [Bieži uzdotie jautājumi](./customer-migration.md) par cilvēkresursu klientu migrāciju.
