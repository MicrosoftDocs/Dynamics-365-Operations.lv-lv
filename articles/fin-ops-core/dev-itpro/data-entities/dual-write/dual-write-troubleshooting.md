---
title: Vispārējā problēmu novēršana
description: Šajā tēmā sniegta vispārīga traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp Finanšu un operāciju programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5896b031229c7fe7e02c8ccf038dd2b1a4f2de05
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614100"
---
# <a name="general-troubleshooting"></a>Vispārējā problēmu novēršana

[!include [banner](../../includes/banner.md)]



Šajā tēmā sniegta vispārīga traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp Finanšu un operāciju programmām un Dataverse.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Spraudņa trasēšanas žurnāla iespējošana un skatīšana Dataverse, lai skatītu kļūdas informāciju

Izsekošanas žurnāli var būt noderīgi, ja traucējumnovēršanas problēmas, kas saistītas ar dubultās rakstīšanas sinhronizāciju starp Finansēm > Operācijas un Dataverse. Žurnālos ir sniegta detalizēta informācija grupām, kas nodrošina tehnisko un inženiertehnisko atbalstu Dynamics 365. Šajā rakstā ir aprakstīts, kā iespējot izsekošanas žurnālus un kā tos skatīt. Izsekošanas žurnāli tiek pārvaldīti Dynamics 365 iestatījumu lapā un tiem ir nepieciešamas administratora līmeņa privilēģijas, lai mainītu un skatītu. 

**Nepieciešamā loma, lai ieslēgtu trasēšanas žurnālu un skatītu kļūdas:** sistēmas administrators

### <a name="turn-on-the-trace-log"></a>Izsekošanas žurnāla ieslēgts
Lai aktivizētu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1.  Piesakieties sistēmā Dynamics 365 un augšējā navigācijas **joslā** atlasiet Iestatījumi. Lapā Sistēmas noklikšķiniet uz **Administrēšana**.
2.  Lapā Administrācija noklikšķiniet uz **Sistēmas iestatījumi**.
3.  Atlasiet cilni **Pielāgošana** un spraudņa un pēc tam pielāgotajā darba plūsmas aktivitātes izsekošanas sadaļā mainiet nolaižamo vērtību uz **Visi**. Tas izsekos visas aktivitātes un sniedz vispusīgu datu kopu komandām, kurām jāpārskata iespējamie jautājumi.

> [!NOTE]
> Iestatot nolaižamo sarakstu uz **Izņēmums**, tiek sniegta izsekošanas informācija tikai tad, ja ir izņēmumi (kļūdas).

Tiklīdz šī opcija ir iespējota, spraudņa izsekošanas žurnāli tiks turpināti iekasēti līdz brīdim, kad tie tiks manuāli izslēgti, atgriežoties šajā atrašanās vietā un atlasot **Izslēgts**.

### <a name="view-the-trace-log"></a>Izsekošanas žurnāla apskate
Lai skatītu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1. Dynamics 365 iestatījumu lapā augšējā **navigācijas** joslā atlasiet iestatījumi. 
2. Atlasiet **Wpa izsekošanas** žurnālu **lapas pielāgojumu** sadaļā.
3. Izsekošanas žurnālu sarakstā ierakstus var atrast, balstoties uz tipa nosaukumu un/vai ziņojuma nosaukumu.
4. Atveriet vēlamo ierakstu, lai apskatītu visu žurnālu. Sadaļā Izpilde ziņojumu blokā tiks sniegta pieejama informācija par spraudņa piestādi. Ja pieejams, tiks sniegta arī izņēmuma informācija. 

Izsekošanas žurnālu saturu var kopēt un ielīmēt citā programmā, piemēram, Notepad vai citos rīkos, lai skatītu žurnālus vai teksta failus un vieglāk skatīt visu saturu. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Iespējot atkļūdošanas režīmu, lai finanšu un operāciju programmās novērstu tiešsaistes sinhronizācijas problēmas

**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators

Dubultās rakstīšanas kļūdas, kas radušās Dataverse, var parādīties Finanšu un operāciju programmā. Lai iespējotu izvērsto kļūdu reģistrēšanu, izpildiet tālāk minētās darbības.

1. Visām projekta konfigurācijām finanšu un operāciju programmā **tabulā DualWriteProjectConfiguration** ir karodziņš **IsDebugMode**.
2. Atveriet elementu **DualWriteProjectConfiguration**, izmantojot Excel pievienojumprogrammu. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu pievienojumprogrammai Finanses un operācijas Excel un pievienojiet **lapai DualWriteProjectConfiguration**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
3. Projektā iestatiet **IsDebugMode** uz **Jā**.
4. Palaidiet scenāriju, kas ģenerē kļūdas.
5. Izvērstie žurnāli ir pieejami tabulā **DualWriteErrorLog**.
6. Lai uzmeklēt tabulas pārlūka datus, izmantojiet šādu saiti: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, `999`aizvietošana.
7. Atjauniniet vēlreiz pēc [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), kas ir pieejams platformas atjauninājumiem 37 vai jaunākai versijai. Ja šis labojums ir instalēts, atkļūdošanas režīms tvers vairāk žurnālu.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Pārbaudīt finanšu un operāciju programmas sinhronizācijas kļūdas virtuālajā datorā

**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators

1. Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).
2. Atveriet LCS projektu, kuram izvēlējāties veikt duālā ieraksta pārbaudi.
3. Atlasiet elementu **Mākoņvides**.
4. Izmantojiet Attālo darbvirsmu, lai pieteiktos virtuālajā datorā (VM) finanšu un operāciju programmā. Izmantojiet lokālo kontu, kas tiek parādīts LCS.
5. Atveriet Notikumu skatītāju,
6. Atlasiet **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.
7. Pārskatiet neseno kļūdu sarakstu.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Duālās rakstīšanas UI lietotāja lapa, kurā redzamas tukšas
Atverot dubultās rakstīšanas lapu Microsoft Edge pārlūkā Vai Arzīmēta pārlūkā, mājas lapa netiek ielādēta un ir redzama tukša lapa vai kļūda, piemēram, "Radās problēma".
Devtools redzat kļūdu konsoles žurnālos:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: neizdevās lasīt rekvizītu "sessionStorage" no "Window": piekļuve šim dokumentam ir liegta. At t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860) jaunā t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728) pie Jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692) at Vai (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076) pie Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750) pret (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130) pie hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151)

Ui izmanto pārlūka 'sesijas krātuvi', lai saglabātu dažas rekvizītu vērtības mājas lapas ielādei. Lai šis varētu strādāt, pārlūkā šai vietai ir jāatļauj trešās puses cepumi. Kļūda ir indikatīvā vērtība no UI, kas nevar piekļūt sesijas glabāšanai. Var būt divi scenāriji, kuros rodas šī problēma:

1.  Jūs atverat UI inco cookiesto režīmā Edge/Chrome, un trešās puses cepumi inco saskaņā ar ir bloķēti.
2.  Jūs esat bloķējis trešās puses cepumus kopā ar Edge/Chrome.

### <a name="mitigation"></a>Mazinājums
Pārlūkprogrammas iestatījumos ir jāatļauj trešās puses cepumi.

### <a name="google-chrome-browser"></a>Konta hromēta pārlūks
1. opcija:
1.  Dodieties uz iestatījumiem, chrome://settings/ vārdu adreses joslā un pēc tam dodieties uz "Konfidencialitāte un drošība", > Cepumi un citi vietnes dati.
2.  Atlasiet Atļaut visus cepumus. Ja to nevēlaties darīt, pārejiet pie otrās opcijas.

Otrā opcija:
1.  Dodieties uz iestatījumiem, chrome://settings/ vārdu adreses joslā un pēc tam dodieties uz "Konfidencialitāte un drošība", > Cepumi un citi vietnes dati.
2.  Ja ir atlasīts 'Bloķēt trešās puses cepumus Inco cookies' vai 'Bloķēt trešās puses cepumus', dodieties uz "Vietnes, kas vienmēr var izmantot cepumus" un noklikšķiniet uz **Pievienot**. 
3.  Pievienojiet jūsu Finanšu &operāciju lietojumprogrammu vietnes nosaukumu — https://<your_FinOp_instance>.cloudax.dynamics.com. Pārliecinieties, ka jūs atzīmējiet izvēles rūtiņu "Visi sīkfaili, tikai šajā vietā". 

### <a name="microsoft-edge-browser"></a>Microsoft Edge Pārlūkprogrammas
1.  Pārejiet uz iestatījumiem > vietnes atļaujām -> cepumus un vietas datus.
2.  'Bloķēt trešās puses cepumus' izslēgšana.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Atsaistīt un saistīt citu Dataverse vidi no programmas Finanses un operācijas

**Nepieciešama loma, lai atsaistītu vidi:** sistēmas administrators programmai Finanses un operācijas vai Dataverse.

1. Piesakieties finanšu un operāciju programmā.
2. Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.
3. Atlasiet visus darbojošos kartējumus, pēc tam atlasiet **Apturēt**.
4. Atlasiet **Atsaistīt vidi**.
5. Atlasiet **Jā**, lai apstiprinātu darbību.

Tagad varat saistīt jaunu vidi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nevar skatīt pārdošanas pasūtījuma rindas informācijas veidlapu 

Veidojot pārdošanas pasūtījumu Dynamics 365 Sales, noklikšķinot uz **+ pievienot preces**, varat tikt novirzīts uz Dynamics 365 Project Operations pasūtījuma rindas veidlapu. No šīs veidlapas nav iespējams skatīt pārdošanas pasūtījuma rindas **Informācijas** veidlapu. **Informācijas** opcija neparādās nolaižamajā sarakstā zem **Jaunas pasūtījuma rindas**. Tas notiek tāpēc, ka projekta operācijas ir uzstādītas jūsu vidē.

Lai atkārtoti iespējotu **Informācijas** veidlapas opciju, rīkojieties šādi:

1. Pārejiet uz **Pasūtījuma rindas** tabulu.
2. Atrodiet **Informācijas** veidlapu zem veidlapas zara.
3. Atlasiet **Informācijas** veidlapu un noklikšķiniet uz **Iespējot drošības lomas**.
4. Mainiet drošības iestatījumu uz **Parādīt visiem**.

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Kā nodrošināt datu integrāciju, izmantojot vis pašreizējo Finanšu un operāciju shēmu

Jūs variet saskarties ar datu problēmām jūsu datu integrācijā, ja netiek lietota visnosāk izmantotā shēma. Šīs darbības palīdzēs atsvaidzināt elementu sarakstu finanšu un operāciju programmās un elementus datu integrētājā.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Atsvaidzināt elementu sarakstu Finanšu un operāciju vidē
1.  Piesakieties finanšu un operāciju vidē.
2.  Atlasiet **Datu pārvaldību**.
3.  Iekšējo datu pārvaldību atlasiet Struktūras **parametri**.
4.  Lapā Datu **importēšanas/eksportēšanas struktūras** parametri atlasiet cilni **Elementa iestatījumi** un atlasiet Atjaunināt **elementu sarakstu**. Tas var ilgt vairāk nekā 30 minūtes, lai atsvaidzinātu atkarībā no iesaistīto entītiju skaita.
5.  Pārejiet uz **Datu pārvaldību** un atlasiet **Datu elementi,** lai pārbaudītu, vai ir uzskaitīti paredzamie elementi. Ja paredzamās entītijas nav uzskaitītas, pārbaudiet, vai entītijas parādās jūsu Finanšu un operāciju vidē un atjaunot trūkstošos elementus pēc nepieciešamības.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Ja atsvaidzināšana neizdodas novērst problēmu, dzēsiet un pievienojiet elementus vēlreiz

> [!NOTE]
> Iespējams, ka vajadzēs apturēt visas apstrādes grupas, kas aktīvi lieto šos elementus pirms dzēšanas.

1.  Atlasiet **Datu pārvaldību** jūsu Finanšu un operāciju vidē un atlasiet **Datu elementus**.
2.  Meklējiet elementus, kuriem ir problēmas, un atzīmējiet mērķa elementu, sagatavošanas tabulu, elementa nosaukumu un citus iestatījumus. Dzēst elementu vai elementus no saraksta.
3.  Atlasiet **Jauns** un vēlreiz pievienojiet elementu vai elementus, izmantojot datus no 2. soļa. 

#### <a name="refresh-entities-in-data-integrator"></a>Atsvaidzināt datu integrētāāja elementus
Piesakieties Power Platform Administrēšanas centrā un izvēlieties **Datu integrāciju**. Atveriet projektu, kurā notiek problēmas, un atlasiet Atsvaidzināt **elementus**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kā iespējot un saglabāt tīkla izsekošanu, lai izsekošanu varētu pievienot atbalsta biļetēm

Iespējams, atbalsta komandai būs jāpārskata tīkla izsekošana, lai novērstu dažas problēmas. Lai izveidotu tīkla izskeošanu, rīkojieties šādi.

### <a name="google-chrome-browser"></a>Konta hromēta pārlūks

1. Atvērtajā cilnē nospiediet **F12** vai izvēlieties **Izstrādātāja rīki**, lai atvērtu izstrādātāja rīkus.
2. Atveriet cilni **Tīkls** un filtra tekstlodziņā ierakstiet **integ**.
3. Palaidiet scenāriju un ievērojiet reģistrētos pieprasījumus.
4. Ar peles labo pogu noklikšķiniet uz ierakstiem un atlasiet **Saglabāt visu kā HAR ar saturu**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge Pārlūkprogrammas

1. Atvērtajā cilnē nospiediet **F12** vai izvēlieties **Izstrādātāja rīki**, lai atvērtu izstrādātāja rīkus.
2. Atveriet cilni **Tīkls**.
3. Palaidiet scenāriju.
4. Atlasiet **Saglabāt**, lai eksportētu rezultātus kā HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
