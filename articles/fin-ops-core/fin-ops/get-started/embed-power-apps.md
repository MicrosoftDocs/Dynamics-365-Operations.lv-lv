---
title: Iegult Power Apps
description: Šajā tēmā ir sniegta informācija par to, kā iegult pakalpojumu Power Apps klientā, lai atbalstītu produkta funkcionalitāti.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824497"
---
# <a name="embed-microsoft-power-apps"></a>Iegult Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Platformas atjauninājumā 14 tiek atbalstīta integrācija ar Microsoft Power Apps — pakalpojumu, kas izstrādātājiem un lietotājiem bez tehniskām zināšanām sniedz iespēju izveidot pielāgotas biznesa programmas mobilajām ierīcēm, planšetdatoriem un tīmekļa vietnēm, nerakstot kodu. Jūsu izstrādāto pakalpojumu Power Apps jūsu organizācija vai plašāka ekosistēma pēc tam var iegult Finance and Operations programmas klientā produkta funkcionalitātes atbalstam. Piemēram, jūs varat izveidot pakalpojumu PowerApp, lai papildinātu programmas Finance and Operations ar informāciju, kas izgūta no citas sistēmas.

Lai uzzinātu vairāk par Power Apps iegulšanu, noskatieties īso video [Kā iegult Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) .

## <a name="adding-an-embedded-power-app-to-a-page"></a>Iegultā pakalpojuma Power App pievienošana lapai

### <a name="overview"></a>Kopsavilkums

Pirms pakalpojuma Power App iegulšanas klientā vispirms ir jāatrod vai jāizveido pakalpojums Power App, kas ietver vēlamo vizuālo informāciju un/vai funkcionalitāti. Mēs šeit nesniegsim detalizētu pakalpojuma Power App izstrādes procesu. Ja pakalpojumu Power Apps izmantojat pirmo reizi, ieteicams skatīt tēmu [Ievads pakalpojumā Power Apps](https://docs.microsoft.com/powerapps/getting-started) .

Ja esat sagatavojies konkrēta pakalpojuma Power App iegulšanai, varat izvēlēties vienu no diviem piekļuves pakalpojumam Power App lapā veidiem atkarībā no tā, kurš scenārijs jums ir piemērotāks. Pirmais piekļuves veids ir standarta darbības rūtī pievienotās pogas Power Apps izmantošana. PakalpojumsPower Apps, kas ir pievienots, izmantojot šo mehānismu, tiek parādīts izvēlnes vienumu veidā izvēlnes pogā Power Apps. Pēc atlasīšanas visi šie izvēlnes vienumi tiek atvērti tajā rūts pusē, kura ietver iegulto pakalpojumu Power App. Vai arī pakalpojumu Power App var parādīt tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu.

Konfigurējot iegulto pakalpojumu Power App, var atlasīt vienu lauku, kuru vēlaties nosūtīt uz pakalpojumu Power App kā ievadi. Tādējādi pakalpojums Power App reaģē atbilstoši datiem, kuri pašlaik tiek skatīti.

### <a name="details"></a>Detalizēta

Tālāk ir sniegti norādījumi par to, kā pakalpojumu Power App iegult tīmekļa vietnes klientā.

1. Atveriet lapu, kurā vēlaties iegult pakalpojumu Power App. Tā ir tā pati lapa, kas ietver visus datus, kuri ir jānosūta pakalpojumam Power App kā ievade.
2. Atveriet rūti **Ievietot Power App**.

    - Noklikšķiniet uz **Opcijas** un pēc tam atlasiet **Personalizēt šo formu**. Izvēlnē **Ievietot** atlasiet **Power App**. Pēc tam atlasiet sadaļu, kurai vēlaties pievienot pakalpojumu Power App. Ja vēlaties iegult pakalpojumu Power App zem izvēlnes pogas Power Apps, atlasiet darbības rūti. Ja vēlaties iegult pakalpojumu Power App tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu).
    - Ja piekļuvei pakalpojumam Power App paredzēts izmantot izvēlnes pogu Power Apps, var arī standarta darbības rūtī noklikšķināt uz izvēlnes pogas **Power Apps** un pēc tam atlasīt **Ievietot Power App**.

3. Konfigurējiet iegulto pakalpojumu Power App.

    - Laukā **Nosaukums** ir norādīts teksts, kas ir redzams uz pogas vai cilnes, kas ietvers iegulto pakalpojumu Power App. Iespējams, ka Power App nosaukums šajā laukā ir jāatkārto bieži.
    - **Programmas ID** ir pakalpojuma Power App, ko vēlaties iegult, GUID. Lai izgūtu šo vērtību, atrodiet pakalpojumu Power App lapā [web.powerapps.com](https://web.powerapps.com) un pēc tam sadaļā **Detalizēta informācija** atrodiet lauku **App ID**.
    - Izmantojot opciju **Power App ievades dati**, var pēc izvēles atlasīt lauku, kas ietver datus, kurus vēlaties nosūtīt uz pakalpojumu Power App kā ievadi. Lai iegūtu sīkāku informāciju par to, kā pakalpojums Power App var piekļūt datiem, kas nosūtīti no programmām Finance and Operations, skatiet sadaļu tālāk šajā tēmā ar nosaukumu [Tāda pakalpojuma Power App izveide, kas piesaista datus no programmām Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps).
    - Atlasiet opciju **Programmas izmērs**, kas atbilst iegulšanai paredzētajam pakalpojuma Power App veidam. Atlasiet opciju **Šaurs** mobilajām ierīcēm izveidotajam pakalpojumam Power Apps un **Plašs** planšetdatoriem izveidotajam pakalpojumam Power Apps. Tādējādi iegultajam pakalpojumam Power App tiek nodrošināts pietiekami daudz vietas.
    - Kopsavilkuma cilnē **Juridiskas personas** var izvēlēties, kurām juridiskajām personām ir pieejams pakalpojums Power App. Noklusējuma iestatījums ir pakalpojuma parādīšana Power App visām juridiskajām personām.

4. Apstipriniet, ka konfigurācija ir pareiza, un pēc tam noklikšķiniet uz **Ievietot**, lai iegultu pakalpojumu Power App lapā. Tiek parādīta uzvedne ar norādi atsvaidzināt pārlūkprogrammu, lai redzētu iegulto pakalpojumu Power App.

## <a name="sharing-an-embedded-power-app"></a>Iegultā pakalpojuma Power App koplietošana

Kad pakalpojums Power App lapā ir iegults un ir apstiprināts, ka tas darbojas pareizi un visu datu konteksts ir no lapas nosūtīts, šo iegulto pakalpojumu Power App var koplietot ar citiem lietotājiem sistēmā. To var izdarīt divos dažādos veidos, izmantojot produkta personalizēšanas iespējas.

- To ieteicams veikt sistēmas administratoram, kurš personalizāciju var piegādāt visiem lietotajiem vai lietotāju apakškopai.
- Vai arī lapas personalizācijas datus var eksportēt, nosūtīt tos vienam vai vairākiem lietotājiem un norādīt visiem šiem lietotājiem importēt šīs izmaiņas. Izmantojot personalizēšanas rīkjoslā esošo opciju Pārvaldīt, varat eksportēt un importēt personalizācijas.

Lai iegūtu sīkāku informāciju par personalizēšanas iespējām produktā un kā tās izmantot, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md) .

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Tāda pakalpojuma Power App izveide, kas piesaista datus no programmām Finance and Operations

Lai varētu izveidot pakalpojumu Power App, kas tiks iegults programmās Finance and Operations, ir jāizmanto programmu Finance and Operations ievades dati. Pakalpojumā Power App šiem ievades datiem var piekļūt, izmantojot mainīgo vērtību Param("EntityId").

Piemēram, Power App funkcijā OnStart var iestatīt programmu Finance and Operations ievades datus kā mainīgo vērtību, kā norādīts tālāk.

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Iegultā pakalpojuma Power App skatīšana

Lai skatītu iegulto pakalpojumu Power App programmu Finance and Operations lapā, atveriet lapu, izmantojot iegulto pakalpojumu Power App. Ņemiet vēra, ka pakalpojumam Power Apps var piekļūt, izmantojot pogu Power Apps standarta darbības rūtī, vai to var redzēt tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu. Pirmo reizi mēģinot ielādēt pakalpojumu Power App lapā, tiek parādīta uzvedne ar norādi pieteikties pakalpojumā Power Apps, lai pārliecinātos, ka lietotājam ir atbilstošas atļaujas izmantot pakalpojumu Power App.

## <a name="editing-an-embedded-power-app"></a>Iegultā pakalpojuma Power App rediģēšana

Kad pakalpojuma Power App iegulšana lapā ir pabeigta, var būt nepieciešams veikt dažas pakalpojuma Power App konfigurācijas izmaiņas. Piemēram, varbūt vēlaties mainīt ar iegulto pakalpojumu Power App saistītu etiķeti vai ir izveidota jauna Power App versija un ir jāatjaunina programmas ID, lai norādītu jaunāko pakalpojuma Power App versiju.

Lai rediģētu iegultā Power App konfigurāciju, izpildiet tālāk aprakstītās darbības.

1. Atveriet rūti **Rediģēt Power App**.

    - Ja piekļuvei iegultajam pakalpojumam Power App izmanto izvēlnes pogu Power Apps, ar peles labo pogu noklikšķiniet uz izvēlnes pogas Power Apps un atlasiet **Personalizēt**. Nolaižamajā izvēlnē **Atlasīt Power App** atlasiet konfigurējamo pakalpojumu Power App.
    - Ja iegultais pakalpojums Power App tiek parādīts tieši lapā, atlasiet **Opcijas** un pēc tam atlasiet **Personalizēt šo formu**. Izmantojot rīku **Atlasīt**, noklikšķiniet uz iegultā pakalpojuma Power App.

2. Veiciet nepieciešamās pakalpojuma Power Apps konfigurācijas izmaiņas un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="removing-an-embedded-power-app"></a>Iegultā pakalpojuma Power App noņemšana

Kad pakalpojuma Power App iegulšana lapā ir pabeigta, to, ja nepieciešams, var noņemt divējādi.

- Atveriet rūti **Rediģēt Power App**, izmantojot norādījumus iepriekš šīs tēmas sadaļā [Iegultā pakalpojuma Power App rediģēšana](#editing-an-embedded-powerapp). Apstipriniet, ka rūtī ir redzama informācija par iegulto pakalpojumu Power App, kuru vēlaties noņemt, un pēc tam noklikšķiniet uz pogas **Dzēst**.
- Tā kā iegultais pakalpojums Power App ir saglabāts kā personalizācijas dati, notīrot lapas personalizācijas datus, tiek noņemtai visi šajā lapā iegultā pakalpojuma Power Apps dati. Ņemiet vērā, ka lapas personalizācijas datu notīrīšana ir neatgriezenisks process, un to nevar atsaukt. Lai noņemtu lapā konkrētos personalizācijas datus, atlasiet **Opcijas** un pēc tam noklikšķiniet uz **Personalizēt šo formu**. Izvēlnē **Pārvaldīt** atlasiet pogu **Notīrīt**. Veicot pārlūkprogrammas atsvaidzināšanu, visi šīs lapas iepriekšējie personalizācijas dati ir noņemti. Lai iegūtu sīkāku informāciju par to, kā optimizēt lapas, izmantojot personalizēšanu, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

## <a name="appendix"></a>Pielikums

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Izstrādātāja pakalpojuma Power App iegulšanas iespēju kontrole

Pēc noklusējuma lietotāji var iegult pakalpojumu Power Apps jebkurā lapā, izmantojot vai nu izvēlnes pogas Power Apps metodi, vai parādot to tieši lapā kā cilni, kopsavilkuma cilni, paneli vai jaunu darbvietas sadaļu. Tomēr, ja nepieciešams, izstrādātāji var arī konfigurēt šo funkciju, lai atļautu iegult pakalpojumu Power Apps tikai konkrētās lapās, izmantojot tālāk norādītās metodes.

- **irIespējotaPowerAppPersonalizācija** — ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad izvēlnes poga Power Apps netiek parādīta, un lietotāji nevarēs iegult pakalpojumu Power Apps jebkurā šīs lapas vietā, tostarp arī cilnes veidā.
- **irIespējotaPowerAppPersonalizācija** — ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad lietotāji nevarēs iegult pakalpojumu Power Apps tieši lapā kā cilni, kopsavilkuma cilni vai panorāmas sadaļu. Lietotāji joprojām var iegult pakalpojumu Power Apps, izmantojot izvēlnes pogu Power Apps, ja iegulšana lapā ir atļauta.

Nākamajā piemērā ir parādīta jauna klase ar divām metodēm, kuras nepieciešamas, lai varētu konfigurēt pakalpojuma Power Apps iegulšanas vietu.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
