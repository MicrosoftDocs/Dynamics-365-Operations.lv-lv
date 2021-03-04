---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 31. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461890"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 31. oktobris)

**Būvējums 8.1.2031**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="create-links-from-talent-to-finance"></a>Saišu izveidošana no Talent uz Finance
Šī jaunā navigācijas funkcionalitāte ļauj jums izveidot saiti no Talent uz Finance, nodrošinot tiešu navigāciju Finance. Kad saites ir konfigurētas, varat norādīt saites nosaukumu un grupu, norādīt vietu, kur saitei būtu jābūt redzamai programmā Talent, ka arī mērķa lapu, ko atvērt programmā Finance.

#### <a name="coming-soon"></a>Drīzumā
Nākotnē tiks pievienots lauka konteksts, lai ļautu tieši pāriet uz atbilstošajiem ierakstiem programmā Finance. Piemēram, varat izmantot vienumu **Saite uz lauku**, lai sniegtu kontekstu pāriešanai tieši uz noteiktu darbinieku vai amatu programmā Finance.

### <a name="configure-target-systems"></a>Mērķa sistēmu konfigurēšana

Programmā Talent sistēmas administratori var definēt saites, kas tiks rādītas dažādās sistēmas administrēšanas darbvietas vietās. Daļa no konfigurācijas ir Finance vides, uz kurām jūs vēlētos pāriet, un tās ir jānorāda kā šādu saišu “mērķis”. To var izdarīt, piešķirot mērķa sistēmai nosaukumu un norādot Finance vides vietrādi URL. Lūk, piemērs Finance vietrādim URL, ko jūs norādītu: https://devax00124aos.cloud.test.dynamics.com/. Kad esat konfigurējis mērķa sistēmu, varat definēt savas saites.

### <a name="configure-links"></a>Saišu konfigurēšana

Katrai izveidotajai saitei ir definēta tālāk norādītā informācija.

- Saite —-saites nosaukums, izmantots vienīgi identificēšanai.

- Iespējot šo saiti — iestatiet uz **Jā**, ja vēlaties šo saiti rādīt programmas Talent lietotājiem.

- Parādāmais nosaukums — definējiet nosaukumu, kas būs redzams kā saite uz Finance. Šie dati pašlaik nav tulkoti.

- Rādīt saiti formā — izvēlēties, kurā lapā vēlaties rādīt šo saiti.

- Grupa — grupas nav obligātas, taču, ja vēlaties kārtot savas saites, izmantojot grupas, atlasiet esošu grupu vai izveidojiet jaunu, izmantojot lauku **Grupas**.

- Mērķa sistēma — atlasiet mērķa sistēmu, kas tika izveidota, izmantojot opciju **Konfigurēt mērķa sistēmu**. Šī būs Finance vide, kas tiks izmantota, kad šo saiti lietosiet navigēšanai.

- Lietotāja pašreizējais uzņēmums — atlasiet **Jā**, ja vēlaties izmantot lietotāja pašreizējā uzņēmuma kontekstu, kad notiek navigēšana uz Finance. Ja ir atlasīta vērtība **Nē**, varat atlasīt izmantojamo uzņēmumu.

- Mērķa izvēlnes vienums — ievadiet izvēlnes vienumu no Finance, kas saitei būtu jāizmanto navigēšanas laikā. Ir pieejami izvēlnes vienumi, uz kuriem varat pāriet tieši. Lai atrastu nepieciešamo izvēlnes vienumu, atveriet programmu Finance un atveriet lapu, kas ir navigācijas mērķis. Kopējiet izvēlnes vienumu no vietrāža URL. Piemēram, ja vēlaties, lai saite jūs pārceltu uz darbinieku sarakstu programmā Finance and Operations, ievadiet vērtību, kas vietrādī URL ir redzama aiz “&mi”. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Izvēlnes vienums pāriešanai uz darbinieku saraksta lapu šajā piemērā ir: HcmWorkerListPage_Employees.

- Saite uz datu avotu — atlasiet datu avotu, uz kuru šī saite atsaucas. Ir pieejami visbiežāk izmantotie avoti, piemēram, **Nodarbinātais** un **Amats**.

- Saite uz lauku — (drīzumā) šī lauka atlasīšana ļaus tieši pāriet no atsevišķa ieraksta programmā Talent uz atsevišķu ierakstu programmā Finance.

### <a name="access-to-links"></a>Piekļuve saitēm

Sistēmas administratori redzēs jaunizveidotās saites uz definētām lapām pat tad, ja opcija **Iespējot šo saiti** būs ir iestatīta uz **Nē**. Šo funkcionalitāti var izmantot saišu testēšanai pirms to rādīšanas citiem darbiniekiem. Visas pārējās lomas konfigurētās saites varēs redzēt tikai pēc tam, kad opcija **Iespējot šo saiti** būs iestatīta uz **Jā**. Darbinieki, kam ir piekļuve lapām, kurās saites tiek rādītas, varēs piekļūt šīm saitēm.

Lietotājiem var būt arī programmā Finance definētas drošības tiesības piekļūt lapām programmatūrā Finance and Operations. Ja viņiem tādu nav, saites lietošanas laikā tiek parādīts drošības dialoglodziņš.


## <a name="other-changesfixes"></a>Citas izmaiņas/labojumi

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Amatus ar sākuma datumu nākotnē nevar piešķirt jaunam darbiniekam

Ir veiktas izmaiņas, lai ļautu darbiniekus piešķirt amatiem ar datumiem nākotnē. Var atlasīt amatus, kuru sākuma datumi ir nākotnē, un darbinieka piešķire tiek veikta, izpildot darbplūsmas saglabāšanu vai pabeigšanu (ja šī darbplūsma ir iespējota).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Jaunu darbinieku nevar piešķirt esošam amatam

Ir veiktas izmaiņas, tāpēc jauna darbinieka piešķiri tagad var piešķirt esošiem amatiem.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Darba stāža datums/biroja vieta pazūd, kad nodarbinātības sākuma datums ir pagātnē un ieraksts tiek saglabāts

Ir veiktas izmaiņas, lai labotu vienumu **Darba stāža datums** un **Biroja vieta** redzamību, kad tiek saglabātas izmaiņas iepriekšējiem darbiniekiem.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Nodarbinātā lapā nevar ievadīt datus par nodarbinātību ar datumu nākotnē

Galvenajā nodarbināto lapā ir atspējoti nodarbinātības dati nodarbinātībai ar datumu nākotnē. Nodarbinātības datus var ievadīt, izmantojot lapas **Datumu pārvaldnieks**. Turpmākajos laidienos tiks ieviestas papildu izmaiņas, lai iespējotu nodarbinātības datu ievadīšanu tieši darbplūsmas procesa laikā.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Vērtības ValidFrom un ValidTo pievienošana elementam HcmPersonalContactPersonEntity

Elements Datu pārvaldības struktūra (Data Management Framework — DMF) HcmPersonalContactPersonEntity ir atjaunināts, ietverot tajā datumus “derīgs no” un “derīgs līdz”, lai iespējotu noteiktus atvieglojumu ieviešanas scenārijus. 

## <a name="known-issue"></a>Zināma problēma
- **Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas. 
- **Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti. Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas. (Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]