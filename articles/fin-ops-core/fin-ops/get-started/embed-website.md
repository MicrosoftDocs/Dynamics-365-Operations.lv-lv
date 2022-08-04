---
title: Trešās puses programmu iegulšana
description: Šajā rakstā ir izskaidrots, kā iegult trešās puses programmas preces funkcionalitātes palielināšanai.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef5ed6c3c99d62010643940f3e2f158963ff0dc2
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123724"
---
# <a name="embed-third-party-apps"></a>Iegult trešās puses programmas

[!include [banner](../includes/banner.md)]

Daudzi debitori biznesa izpildē izmanto vairākas programmas. Dažas no šīm programmām ir trešās puses Web programmas, kas darbojas kopā ar finanšu un operāciju programmām. Lai nodrošinātu daudz daudz lielākas lietotāju pieredzes pieredzi, varat izmantot līdzekli Pilnas lapas programmas, **lai** iegultu šīs trešās personas programmas tieši jūsu finanšu un operāciju programmās (nodrošināts, ka trešās puses programmas ļauj iegulties). Šādā veidā lietotāji var piekļūt vietnēm un nepieciešamām programmām, nepārslēdzot cilnes vai logus.

Pirms varat produktā iegult trešās puses programmas, līdzekļa pārvaldībā ir jāslēdz līdzekli **Pilnas lapas programmas** . Pēc tam varat izmantot vienu no šīm metodēm, lai iegultu trešās puses programmu vai vietni. Šīs metodes ir analogas metodēm, kas tiek izmantotas, lai iegultu canvas programmas no Microsoft Power Apps finanšu un operāciju programmām.

- Iegult programmu vai vietni esošajā lapā kā jaunu cilnes lapu (koptabulu, kopsavilkuma cilni, failu vai darbvietas sadaļu).
- Izveidojiet jaunu pilnas lapas pieredzi programmai vai vietnei no informācijas paneļa.

## <a name="embed-a-website-on-an-existing-page"></a>Iegult vietni esošā lapā

Izmantojiet šo procedūru, ja vēlaties papildināt esošu sistēmas lapu ar iegulto programmu.

1. Atveriet lapu, kurā vēlaties iegult programmu.
2. Atveriet rūti **Pievienot programmu**:

    1. Atlasiet **Iestātījumi** un pēc tam **Personalizēt**, lai atvērtu rīkjoslu **Personālizācija**.
    2. Atlasīt **Papildu \> Pievienot programmu**.

3. Atlasiet tās lapas sadaļu, kurā vēlaties pievienot programmu. Šai sadaļai ir jābūt *cilnes konteineram*, kas paredzēts rakursa cilnei, kopsavilkuma cilnei, panelim vai darbvietas sadaļai.
4. Atlasiet **Vietni**.
5. Konfigurējiet iegulto pakalpojumu:

    - **Nosaukums** — ievadiet tekstu, kas jāparāda cilnei, kas satur iegulto programmu. Bieži vien vēlēsieties, lai šis teksts būtu programmas nosaukums.
    - **URL** - Norādiet programmas atrašanās vietu.

    > [!IMPORTANT]
    > - Drošības iemeslu dēļ URL jālieto protokolu Hypertext Transfer Protocol Secure (HTTPS).
    > - Programmai vai vietnei jābūt konfigurētai tā, lai atļautu sevi iegult.

6. Atlasiet **Saglabāt**, lai iegultu programmu lapā. Programma tiek pievienota kā pēdējā cilnes vai grupas sadaļas daļa.
7. Apstipriniet, ka programma parādās, kā paredzēts. Ja programma netiek atveidota, skatiet tālāk šī raksta [sadaļu](#troubleshooting) Problēmu novēršana.
8. Atveriet skatījuma atlasītāju un atlasiet **Saglabāt** (ja programmai jābūt saistītai ar pašreizējo skatu) vai **Saglabāt kā** (lai saglabātu programmu citā skatā).

    Ja lapai nav skatījuma atlasītāja (piemēram, ja lapa ir dialoglodziņš vai darbvieta), varat izlaist šo darbību.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Iegult vietni kā pilnas lapas pieredzi no informācijas paneļa

Izmantojiet šo procedūru, ja programma, kuru vēlaties iegult, nav saistīta ar esošu lapu vai ja vēlaties tikai iegūt pilnu lapas pieredzi programmai finanšu un operāciju programmā.

1. Atveriet informācijas paneli.
2. Atlasiet un turiet lapu (vai noklikšķiniet ar peles labo pogu) informācijas paneli, atlasiet **Personalizēt** un pēc tam atlasiet **Pievienot lapu**.
3. Rūtī **Pievienot lapu** atlasiet **Vietne**.
4. Konfigurējiet iegulto pakalpojumu:

    - **Nosaukums** — ievadiet tekstu, kas jāparāda elementā, kas ir pievienots iegultajā programmā informācijas panelī. Bieži vien vēlēsieties, lai šis teksts būtu programmas nosaukums.
    - **URL** - Norādiet programmas atrašanās vietu.

    > [!IMPORTANT]
    > - Drošības iemeslu dēļ URL ir jāizmanto HTTPS.
    > - Programmai vai vietnei jābūt konfigurētai tā, lai atļautu sevi iegult.

5. Atlasiet **Saglabāt**, lai programmu pievienotu informācijas panelim kā jaunu elementu.
6. Atlasiet vadības panelī jaunu elementu un apstipriniet, ka programma tiek parādīta, kā paredzēts. Ja programma netiek atveidota, skatiet tālāk šī raksta [sadaļu](#troubleshooting) Problēmu novēršana.

## <a name="sharing-embedded-apps"></a>Iegulto programmu koplietošana

Kad ir iegulta programma, izmantojot vienu no metodēm, kas aprakstītas iepriekšējās sadaļās, iespējams, vēlēsieties koplietot skatu ar citiem lietotājiem sistēmā. Lai koplietotu iegulto programmu, izmantojiet vienu no tālāk aprakstītajām metodēm.

- **Publicējiet skatu (ieteicams):** Ja iegultā programma ir saglabāta skatā, ieteicamais un vēlamais veids, kā to kopīgot, ir publicēt šo skatu lietotājiem, kuriem ir atbilstošās drošības lomas mērķa juridiskajās personās. Šajā gadījumā tikai vēlamais lietotājs redzēs šajā lapā iegulto programmu. Papildinformāciju par to, kā publicēt skatu, skatiet sadaļā [Skatu publicēšana](saved-views.md#publishing-views).

    Varat arī publicēt programmu, kas ir iegulta kā pilnas lapas pieredze no informācijas paneļa. Informācijas panelī atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) ar programmu saistīto elementu, atlasiet **Personalizēt** un pēc tam atlasiet **Publicēt lapu**. Yiek parādīta pieredze, kas ir līdzīga *publicēto skatu* pieredzei, un varat atlasīt drošības lomas, lai to publicētu. Ja ir ieslēgts līdzeklis **Uzlabots atbalsts juridiskām personām par saglabātajiem skatiem**, atjauninājumā 10.0.21 vai jaunākās versijās varat publicēt programmu vēlamajām juridiskajām personām.

- **Kopēt personalizēšanu:** lapām, kas neatbalsta skatus (piemēram, dialoglodziņam vai darbvietam), vai pilnas lapas programmu pieredzei, varat kopēt personalizēšanu atbilstošajiem lietotājiem. Papildinformāciju skatiet sadaļā [Personalizēšanas koplietošana](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Iegulto programmu skatīšana

Lai skatītu finanšu un operāciju programmu lapā iegulto programmu, atveriet lapu, kurā ir iegultā programma. Atcerieties, ka dažās lapās iegultām programmām var piekļūt, izmantojot **Power Apps** pogu standarta darbības rūtī. Vai arī tie var parādīties tieši lapā kā jauna cilne vai kopsavilkuma cilne, vai panelis, vai kā jauna darbvietas sadaļa.

## <a name="editing-or-removing-embedded-apps"></a>Iegulto programmu rediģēšana vai noņemšana

Kad programma ir iegulta lapā, iespējams, būs jārediģē tās konfigurācija (piemēram, mainot sadaļas iezīmi vai URL). Alternatīvi iespējams, ka tā ir jānoņem no lapas. Izmantojiet vienu no šīm procedūrām, lai rediģētu iegultās programmas konfigurāciju vai noņemtu to pilnībā.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Programmas, kas ir iegultas esošajās lapās

1. Atveriet lapu, kurā programma ir iegulta.
2. Atlasiet **Iestātījumi** un pēc tam **Personalizēt**, lai atvērtu rīkjoslu **Personālizācija**.
3. Atlasiet rīku **Atlasīt** un pēc tam atlasiet iegulto programmu.
4. Lai rediģētu programmu, veiciet nepieciešamās izmaiņas tās konfigurācijā un pēc tam atlasiet **Saglabāt**.

    Vai arī, lai noņemtu programmu, atlasiet **Dzēst**.

5. Vēlreiz saglabājiet vai atkārtoti publicējiet skatu. Ievērojiet, ka, atstājot lapu bez skaidras skata saglabāšanas, neviena no darbībām, ko veicāt rūti **Rediģēt vietnei**, netiks uzturēta.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Lietojumprogrammas, kas ir iegultas no informācijas paneļa

1. Atveriet informācijas paneli.
2. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) ar iegulto programmu saistīto elementu, un atlasiet **Personalizēt**.
3. Lai rediģētu programmu, atlasiet **Rediģēt lapu**. Rūtī **Rediģēt vietni** veiciet nepieciešamās izmaiņas programmas konfigurācijā un pēc tam atlasiet **Saglabāt**.

    Vai arī, lai noņemtu programmu, atlasiet **Noņemt lapu**.

## <a name="appendix"></a>Pielikums

### <a name="troubleshooting"></a>Problēmu novēršana

Ja tīmekļa vietne nav atveidota pareizi pēc tās iegultas Finance and Operation programmā vai ja saņemat kļūdas ziņojumu, ka URL tika atteikts savienojumam, vietne, iespējams, ir konfigurēta tā, lai neļautu sevi iegult iFrame. Izpildiet šīs darbības, lai noteiktu, vai vietne var tikt iegulta.

1. Atveriet izstrādātāju rīkus pārlūkam, kuru izmantojat.
2. Cilnē **Tīkls** atrodiet un atlasiet atbildi no iegultās vietnes.
3. Cilnes **Virsraksti** sadaļā **Atbilžu virsraksti** meklējiet **x-frame opcijas**. Ja atbilžu virsrakstos pastāv **x-frame opcijas** un to vērtība ir **DENY** vai **SAMEORIGIN**, vietne pašlaik nevar tikt iegulta. Lai aktivizētu programmas īpašnieku, tam jābūt droši iegultam.

### <a name="developer-modeling-a-website-on-a-form"></a>[Izstrādātājs] Vietnes modelēšana formā

Lai gan šis raksts ir fokusēts uz iegultajām trešās puses programmām vai vietnēm, izmantojot personalizāciju, izstrādātāji var arī iegult tās formā, izmantojot Visual Studio izstrādes pieredzi. Vienkārši pievienojiet **WebsiteHostControl** kontroli formai. Kontrolei pieejamie metadatu rekvizīti nodrošina tādas pašas iespējas kā personalizēšanas pieredzei.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

