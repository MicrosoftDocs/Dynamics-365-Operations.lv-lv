---
title: Iegult Power Apps
description: Šajā tēmā ir sniegta informācija par to, kā iegult pakalpojumu Power Apps klientā, lai atbalstītu produkta funkcionalitāti.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
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
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017732"
---
# <a name="embed-microsoft-power-apps"></a>Iegult Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations atbalsta integrāciju ar Microsoft Power Apps ,— pakalpojumu, kas izstrādātājiem un lietotājiem bez tehniskām zināšanām sniedz iespēju izveidot pielāgotas biznesa programmas mobilajām ierīcēm, planšetdatoriem un tīmekļa vietnēm, nerakstot kodu. Jūsu izstrādāto pakalpojumu Power Apps jūsu organizācija vai plašāka ekosistēma pēc tam var iegult Finance and Operations programmas klientā produkta funkcionalitātes atbalstam. Piemēram, varat izveidot programmu no Power Apps, lai papildinātu programmu Finance and Operations ar informāciju, kura tiek izgūta no citas sistēmas.

Lai uzzinātu vairāk par Power Apps iegulšanu, noskatieties īso video [Kā iegult Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) .

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Iegulta pakalpojuma pievienošana no Power Apps lapai

### <a name="overview"></a>Pārskats

Pirms pakalpojuma no Power Apps iegulšanas klientā vispirms ir jāatrod vai jāizveido pakalpojums, kas ietver vēlamo vizuālo informāciju un/vai funkcionalitāti. Mēs šeit nesniegsim detalizētu pakalpojumu izstrādes procesu. Ja pakalpojumu Power Apps izmantojat pirmo reizi, ieteicams skatīt tēmu [Ievads pakalpojumā Power Apps](https://docs.microsoft.com/powerapps/getting-started) .

Ja esat sagatavojies konkrēta pakalpojuma iegulšanai, varat izvēlēties vienu no diviem piekļuves pakalpojumiem lapā veidiem atkarībā no tā, kurš scenārijs jums ir piemērotāks. Pirmais piekļuves veids ir standarta darbības rūtī pievienotās pogas Power Apps izmantošana. Pakalpojumi, kas ir pievienoti, izmantojot šo mehānismu, tiek parādīti izvēlnes vienumu veidā izvēlnes pogā Power Apps. Pēc atlasīšanas visi šie izvēlnes vienumi tiek atvērti tajā rūts pusē, kura ietver iegulto pakalpojumu. Vai arī pakalpojumu var iegult tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu.

Konfigurējot iegulto pakalpojumu, var atlasīt vienu lauku, kuru vēlaties nosūtīt uz pakalpojumu kā kontekstu. Tādējādi pakalpojums reaģē atbilstoši datiem, kuri pašlaik tiek skatīti.

### <a name="details"></a>Detalizēta

Tālāk ir sniegti norādījumi par to, kā pakalpojumu no Power Apps iegult tīmekļa vietnes klientā.

1. Atveriet lapu, kurā vēlaties iegult pakalpojumu. Tā ir tā pati lapa, kas ietver visus datus, kuri ir jānosūta pakalpojumam kā ievade.
2. Atveriet rūti **Pievienot pakalpojumu no Power Apps**:

    - Noklikšķiniet uz **Opcijas** un pēc tam atlasiet **Personalizēt šo lapu**. Izvēlnē **Ievietot** izvēlieties **Power Apps**. Pēc tam atlasiet sadaļu, kurai vēlaties pievienot pakalpojumu. Ja vēlaties iegult pakalpojumu zem izvēlnes pogas Power Apps, atlasiet darbības rūti. Ja vēlaties iegult pakalpojumu tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu).
    - Ja piekļuvei pakalpojumam paredzēts izmantot izvēlnes pogu Power Apps, var arī standarta darbības rūtī noklikšķināt uz izvēlnes pogas **Power Apps** un pēc tam atlasīt **Ievietot pakalojumu**.

3. Konfigurējiet iegulto pakalpojumu:

    - Laukā **Nosaukums** ir norādīts teksts, kas ir redzams uz pogas vai cilnes, kas ietvers iegulto pakalpojumu. Iespējams, ka pakalpojuma nosaukums šajā laukā ir jāatkārto bieži.
    - **Programmas ID** ir pakalpojuma, ko vēlaties iegult, GUID. Lai izgūtu šo vērtību, atrodiet pakalpojumu lapā [web.powerapps.com](https://web.powerapps.com) un pēc tam sadaļā **Detalizēta informācija** atrodiet lauku **App ID**.
    - Izmantojot opciju **Pakalpojuma ievades konteksts**, var pēc izvēles atlasīt lauku, kas ietver datus, kurus vēlaties nosūtīt uz pakalpojumu kā ievadi. Skatiet tālāk šajā tēmā sadaļu ar nosaukumu [Tāda pakalpojuma izveide, kas piesaista datus no programmām Finance and Operations](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps), lai iegūtu sīkāku informāciju par to, kā pakalpojums var piekļūt datiem, kas nosūtīti no programmām Finance and Operations.
    - Atlasiet opciju **Programmas izmērs**, kas atbilst iegulšanai paredzētajam pakalpojuma veidam. Atlasiet opciju **Plāns** mobilajām ierīcēm izveidotajiem pakalpojumiem un **Plašs** planšetdatoriem izveidotajiem pakalpojumiem. Tādējādi iegultajam pakalpojumam tiek nodrošināts pietiekami daudz vietas.
    - Kopsavilkuma cilnē **Juridiskas personas** var izvēlēties, kurām juridiskajām personām ir pieejams pakalpojums. Noklusējuma iestatījums ir nodrošina pakalpojuma pieejamību visām juridiskajām personām. Šī opcija ir pieejama tikai tad, ja ir atspējots līdzeklis [Saglabātie skati](saved-views.md). 

4. Apstipriniet, ka konfigurācija ir pareiza, un pēc tam noklikšķiniet uz **Ievietot**, lai iegultu pakalpojumu Power App lapā. Tiek parādīta uzvedne ar norādi atsvaidzināt pārlūkprogrammu, lai redzētu iegulto pakalpojumu.

## <a name="sharing-an-embedded-app"></a>Iegultā pakalpojuma koplietošana

Kad pakalpojums lapā ir iegults un ir apstiprināts, ka tas darbojas pareizi un visu datu konteksts ir no lapas nosūtīts, šo pakalpojumu var koplietot ar citiem lietotājiem sistēmā. To var izdarīt divos dažādos veidos, izmantojot produkta personalizēšanas iespējas.

- To ieteicams veikt sistēmas administratoram, kurš personalizāciju var piegādāt visiem lietotajiem vai lietotāju apakškopai.
- Vai arī lapas personalizācijas datus var eksportēt, nosūtīt tos vienam vai vairākiem lietotājiem un norādīt visiem šiem lietotājiem importēt šīs izmaiņas. Personalizēšanas rīkjoslā ir pieejamas darbības, kas ļauj eksportēt un importēt personalizācijas.

Lai iegūtu sīkāku informāciju par personalizēšanas iespējām produktā un kā tās izmantot, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md) .

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Tādas programmas izveide, kas piesaista no programmām Finance and Operations nosūtītos datus

Izveidojot no Power Apps programmu, kas tiks iegulta programmā Finance and Operations, būtiska programmas izveides daļa ir ievades datu izmantošana no šīs programmas. Power Apps izstrādes pieredze rāda, ka Finance and Operations programmas nodotajiem ievades datiem var piekļūt, izmantojot mainīgo vērtību Param("Entityld").

FPiemēram, pakalpojuma funkcijā OnStart var iestatīt programmu Finance and Operations ievades datus kā mainīgo vērtību, kā norādīts tālāk.

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Programmas skatīšana

Lai skatītu iegulto pakalpojumu programmu Finance and Operations lapā, atveriet lapu, izmantojot iegulto pakalpojumu. Ņemiet vērā, ka pakalpojumiem var piekļūt, izmantojot pogu Power Apps standarta darbības rūtī, vai to var redzēt tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu. Pirmo reizi mēģinot ielādēt pakalpojumu lapā, tiek parādīta uzvedne ar norādi pieteikties pakalpojumā , lai pārliecinātos, ka lietotājam ir atbilstošas atļaujas izmantot pakalpojumu.

## <a name="editing-an-embedded-app"></a>Iegultā pakalpojuma rediģēšana

Kad pakalpojuma iegulšana lapā ir pabeigta, var būt nepieciešams veikt dažas pakalpojuma konfigurācijas izmaiņas. Piemēram, varbūt vēlaties mainīt ar iegulto pakalpojumu saistītu etiķeti vai ir izveidota jauna pakalpojuma versija un ir jāatjaunina programmas ID, lai norādītu jaunāko pakalpojuma versiju.

Lai rediģētu iegultā pakalpojuma konfigurāciju, izpildiet tālāk aprakstītās darbības.

1. Atveriet rūti **Rediģēt pakalpojumu**.

    - Ja piekļuvei iegultajam pakalpojumam izmanto izvēlnes pogu Power Apps, ar peles labo pogu noklikšķiniet uz izvēlnes pogas Power Apps un atlasiet **Personalizēt**. Nolaižamajā izvēlnē **Atlasīt pakalpojumu** atlasiet konfigurējamo pakalpojumu.
    - Ja iegultais pakalpojums tiek parādīts tieši lapā, atlasiet **Opcijas** un pēc tam atlasiet **Personalizēt šo lapu**. Izmantojot rīku **Atlasīt**, noklikšķiniet uz iegultā pakalpojuma.

2. Veiciet nepieciešamās pakalpojuma konfigurācijas izmaiņas un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="removing-an-app"></a>Pakalpojuma noņemšana

Kad pakalpojuma iegulšana lapā ir pabeigta, to, ja nepieciešams, var noņemt divējādi.

- Atveriet rūti **Rediģēt pakalpojumu**, izmantojot norādījumus iepriekš šīs tēmas sadaļā [Iegultā pakalpojuma rediģēšana](#editing-an-embedded-power-app). Apstipriniet, ka rūtī ir redzama informācija par iegulto pakalpojumu, kuru vēlaties noņemt, un pēc tam noklikšķiniet uz pogas **Dzēst**.
- Tā kā iegultais pakalpojums ir saglabāts kā personalizācijas dati, notīrot lapas personalizācijas datus, tiek noņemti visi šajā lapā iegultie pakalpojumi. Ņemiet vērā, ka lapas personalizācijas datu notīrīšana ir neatgriezenisks process, un to nevar atsaukt. Lai noņemtu lapā konkrētos personalizācijas datus, atlasiet **Opcijas**, tad **Personalizēt šo lapu**, un pēc tam pogu **Notīrīt**. Veicot pārlūkprogrammas atsvaidzināšanu, visi šīs lapas iepriekšējie personalizācijas dati ir noņemti. Lai iegūtu sīkāku informāciju par to, kā optimizēt lapas, izmantojot personalizēšanu, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

## <a name="appendix"></a>Pielikums

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Izstrādātāja pakalpojuma iegulšanas iespēju kontrole

Pēc noklusējuma lietotāji var iegult pakalpojumus jebkurā lapā, izmantojot vai nu izvēlnes pogas Power Apps metodi, vai parādot to tieši lapā kā cilni, kopsavilkuma cilni, paneli vai jaunu darbvietas sadaļu. Tomēr, ja nepieciešams, izstrādātāji var arī konfigurēt šo funkciju, lai atļautu iegult pakalpojumus tikai konkrētās lapās, izmantojot tālāk norādītās metodes.

- **irIespējotaPowerAppPersonalizācija** – ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad izvēlnes poga Power Apps netiek parādīta, un lietotāji nevarēs iegult pakalpojumus jebkurā šīs lapas vietā, tostarp arī cilnes veidā.
- **irIespējotaPowerAppPersonalizācija** – ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad lietotāji nevarēs iegult pakalpojumus tieši lapā kā cilni, kopsavilkuma cilni FastTab vai panorāmas sadaļu. Lietotāji joprojām var iegult pakalpojumus, izmantojot Power Apps izvēlnes pogu, ja iegulšana lapā ir atļauta.

Nākamajā piemērā ir parādīta jauna klase ar divām metodēm, kuras nepieciešamas, lai varētu konfigurēt pakalpojumu iegulšanas vietu.

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
