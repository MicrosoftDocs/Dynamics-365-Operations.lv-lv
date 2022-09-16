---
title: Commerce Tērzēšana ar Debitorachannel klientu pakalpojuma modulim
description: Šajā rakstā ir aprakstīts Commerce Chat ar Parchannel, kas paredzēts Klientu apkalpošanas modulim sadaļā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473814"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce Tērzēšana ar Debitorachannel klientu pakalpojuma modulim

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts Commerce *Chat ar Parchannel, kas paredzēts Klientu apkalpošanas modulim* sadaļā Microsoft Dynamics 365 Commerce.

Commerce versijas 10.0.29 laidienā Modulis Commerce Commerce Chat arBalstīts uz Customer Service moduli tika pievienots Commerce moduļa bibliotēkai. Commerce tērzēšanas līdzeklis nodrošina e-komercijas klientus ar Pakalpojuma Dynamics 365 Par Debitoriem 365 par tiešsaistes kanālu, kas ietver tiešsaistes aģenta atbalstu, lai palīdzētu vaicāt debitoru vaicājumiem, nodrošinātu klientu apkalpošanu un veicinātu pārdošanu Commerce klientiem.

Commerce tērzēšanas funkcija ļauj mazumtirgotājiem sasniegt šos mērķus:

- Palieliniet personalizētās piesaistes debitoriem, lai palīdzētu uzlabot debitoru ieturējumus.
- Uzlabot klientu apkalpošanu, integrējot cilvēkresursu aģentu un pašapkalpošanās tērzēšanu.
- Palīdzības aģenti iegūst pieredzi reāllaika klientu profilā, pasūtījumā un iepirkumu datos, kas vada operāciju uzlabojumus un iesaistes.
- Uzlabot vispārējo klientu apmierinātību, lai palīdzētu palielināt pārdošanu;

Tālāk norādītās iespējas ir pieejamas kā daļa no Commerce Tērzēšanas funkcionalitātes:

- Komercijas tērzēšana ar Para&Tonel, kas paredzēts klientu apkalpošanai
- **Commerce Call Center kā pieteikuma** cilnes pievienošana aģenta pieredzi sistēmā Dynamics 365 Fontschannel klientu apkalpošanai

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Priekšnosacījumi Kārneli klientu apkalpošanai

Kā priekšnosacījums ir jākonfigurē tērzēta prece Debitora pakalpojumu administrācijas logrīrīki Nechannel un jāiegūst daži parametri, lai konfigurētu Commerce Tērzēšanas pieredzi. Norādījumus skatiet sarakstes kanāla [konfigurēšana](/dynamics365/customer-service/set-up-chat-widget).

Pēc tam, kad būsiet konfigurējis tērzēšanu Debitora pakalpojumu administrācijas logrīku Debitoriemchannelā, tiks saņemts skripts, kas līdzīgs šim piemēram.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopējiet šo skriptu, jo, lai konfigurētu tērzēšanu moduli, tajā būs nepieciešamas vērtības.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Commerce Tērzēšana ar Paramteriālu, kas paredzēts Customer Service obligātajiem laukiem

Tabulā ir parādītas skripta vērtības no Debitora pakalpojumu administrēšanas logrīku debitorachannela, kas nepieciešami, lai konfigurētu Commerce Papchannel debitoru pakalpojuma modulim.

| Logrīku rekvizīts | Apraksts |
| ------------- |--------------|
| Skripta avots | Srces **vērtība tērzēšanas** logrīka skriptā. |
| Datu programmas ID | Datu-app-ID **vērtība tērzēšanas** logrīka skriptā. |
| Datu organizācijas ID | Datu-org-ID **vērtība tērzēšanas** logrīka skriptā. |
| Datu organizācijas URL | Datu org-URL **vērtība tērzēšanas** logrīka skriptā. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Commerce tērzēšanas pieredzes konfigurēšana jūsu e-komercijas vietnei

Viens no ieteiktajiem veidiem, kā izmantot tērzēšanu jūsu e-komercijas vietnē, ir pievienot Moduli Commerce Chat ar Customer Service moduli Par Debitoriem, kopīgotam virsraksta fragmentam, kas tiek izmantots jūsu e-komercijas vietņu lapās.

Lai pievienotu tērzētavas moduli jūsu vietnes virsraksta fragmentam Commerce Site Builder, sekojiet šiem soļiem.

1. Vietas veidotājā savā vietā dodieties uz **Fragments**.
1. Atlasiet **Jauna**.
1. Dialoglodziņā Atlasīt **fragmentu atlasiet** **moduli Commerce Tērzēšana ar Debitoru pakalpojumu kanālu**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Izklāsta skatā atlasiet **Msdstruktūras365 cs tērzēšanas savienotāja slotu**.
1. Tērzētavas **rekvizītu** rūtī labajā pusē veiciet tālāk aprakstītās darbības.

    1. Laukā **Skripta avots** ievadiet **rikt** vērtību, ko ieguvāt no Debitora pakalpojuma skripta Katnel.
    1. Laukā **Datu lietojumprogrammas ID** ievadiet **datu-programmas ID** vērtību, ko ieguvāt no Debitorachannel debitoru pakalpojuma skripta.
    1. Laukā **Datu organizācijas ID** dati-org-ID **vērtība,** ko ieguvis no Debitora pakalpojuma skripta Toms (I).
    1. Laukā **Datu organizācijas URL** ievadiet **datu-org-URL** vērtību, ko ieguvāt no Debitora pakalpojuma skripta Par debitoriem iegūtā parametrā.

    ![Commerce Chat moduļa fragmenta izveide Commerce Site Builder.](media/Commerce-chat-creating-new-fragment.png)

1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Fragmenti** un atveriet jūsu vietnes virsraksta fragmentu.
1. Noklusējuma konteinera **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **fragmentu**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet iepriekš izveidoto tērzēta fragmentu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Pievienot Commerce Headquarters kā lietojumprogrammu cilni, kas ir paredzēts Klientu apkalpošanas debitoriem

Programmas cilni Commerce headquarters var pievienot sadaļā Debitora pakalpojumu debitoriem nospīdāmais rēķins. Live aģenti tad var izmantot lietotāja interfeisu, kas paredzēts Debitora pakalpojumu aģenta pieredzes debitorachannelim Dynamics 365 Commerce, lai viegli piekļūtu klientu apkalpošanas modulim, kas ietver kontekstuālu informāciju debitoram kopā ar viņu pārdošanas pasūtījumu informāciju. Turklāt klientu apkalpošanas aģenti var veikt jaunus pasūtījumus, sākt atgriešanu un pārbaudīt pasūtījuma statusa informāciju.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Izveidot jaunu pieteikuma cilni, kas modulī ielādē programmu Commerce Headquarters iFrame 

Lai izveidotu jaunu programmas cilni, kas ielādē commerce headquarters modulī iFrame, izpildiet šīs darbības.

1. Atveriet portālu [Power Apps Veidotājs](https://make.powerapps.com).
1. Navigācijas rūtī kreisajā pusē atlasiet **Programmas**.
1. Atlasiet **Klientu apkalpošanas administrēšanas centru**.
1. Dodieties uz **aģenta pieredzi**.
1. Pieteikumu **ciļņu veidnēm** atlasiet **Pārvaldīt**.
1. Izveidojiet jaunu trešās puses **tīmekļa vietnes tipa programmas** cilni. Norādījumus skatiet programmu [ciļņu veidņu pārvaldīšana](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Zem **Parametri** vietrāža **URL** **parametra** laukā Vērtība ievadiet tālāk norādīto URL, kur `<YourOrganizationHeadquartersURL>``<LegalEntityname>` un tiek aizstāts ar atbilstošajām vērtībām. Debitora pakalpojuma kanālu nolasa **{AccountNumber}** no tērzētavas konteksta. Tādēļ atstājiet **{AccountNumber}** tāpat, kā ir.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Atstājiet **datu** parametra lauku **Vērtība** tukšu.

![Notiek programmas cilnes izveide programmā Dynamics 365 Tornel Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Iespējojiet jaunu programmas cilni klientu aģentiem programmā Dynamics 365 Fontschannel klientu apkalpošanai

Lai iespējotu jaunu programmas cilni klientu aģentiem programmā Dynamics 365 Fontschannel klientu apkalpošanai, sekojiet šiem soļiem.
    
1. Atveriet portālu [Power Apps Veidotājs](https://make.powerapps.com).
1. Navigācijas rūtī kreisajā pusē atlasiet **Programmas**.
1. Atlasiet **Klientu apkalpošanas administrēšanas centru**.
1. Pārejiet uz **sadaļu Debitoru \> atbalsta darbastraumes**.
1. Atveriet darbastraumes, ko esat izveidojis saviem aģentiem, un pēc tam sadaļā Papildu **iestatījumi** atlasiet Sesijas **noklusējums**.
1. Sadaļā **Pieteikumu cilnes**, atlasiet Pievienot **esošu pieteikuma cilni** un pēc tam pievienojiet jaunu pieteikuma cilni, ko izveidojāt agrāk. Šis solis nodrošina, ka pieteikuma cilne, kas ielādē Commerce Headquarters iFrame modulī, parādīsies, kad aģents saņems ienākošo tērzēšanu no jūsu e-komercijas vietnes.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Pievienot konteksta mainīgos programmā Dynamics 365 Tornel, kas paredzēts klientu apkalpošanai

Lai pievienotu konteksta mainīgos programmā Dynamics 365 Tolachannel for Customer Service, izpildiet šīs darbības.

1. Atveriet portālu [Power Apps Veidotājs](https://make.powerapps.com).
1. Navigācijas rūtī kreisajā pusē atlasiet **Programmas**.
1. Atlasiet **Klientu apkalpošanas administrēšanas centru**.
1. Pārejiet uz **sadaļu Debitoru \> atbalsta darbastraumes**.
1. Atveriet darbastraumes, kuru esat izveidojis saviem aģentiem, **un** pēc tam sadaļā Papildu iestatījumi atveriet sadaļu Konteksta **mainīgais**.
1. Atlasiet **Labot** un pēc tam pievienojiet **AccountNumber** kā teksta tipa konteksta **mainīgo**. Šis mainīgais palīdzēs Commerce Headquarters ielādēt debitora informāciju ar atbilstošiem kontu numuriem.

> [!NOTE]
> Ja vēlaties lasīt e-pasta adreses un parakstīto lietotāju vārdus no e-komercijas kanāla, **·** **papildus** AccountNumber **konteksta mainīgajam varat pievienot e-pasta ziņojumu un vārdu kā teksta tipa konteksta mainīgos.** **·**
