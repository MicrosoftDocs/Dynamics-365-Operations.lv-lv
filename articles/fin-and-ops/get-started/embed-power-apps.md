---
title: "Pakalpojuma PowerApps iegulšana"
description: "Šajā tēmā ir sniegta informācija par to, kā iegult pakalpojumu PowerApps Finance and Operations klientā, lai atbalstītu produkta funkcionalitāti."
author: jasongre
manager: AnnBe
ms.date: 04/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>Pakalpojuma PowerApps iegulšana

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pre-release.md)]

Platformas atjauninājuma versija 14, Microsoft Dynamics 365 for Finance and Operations atbalsta integrāciju ar Microsoft PowerApps, izstrādātājiem un ar tehniku nesaistītiem lietotājiem paredzētu pakalpojumu pielāgotu biznesa programmu mobilajām ierīcēm, planšetdatoriem un tīmekļa vietnēm izveidei bez kodu rakstīšanas. Jūsu izstrādāto pakalpojumu PowerApps jūsu organizācija vai plašāka ekosistēma pēc tam var iegult Finance and Operations klientā produkta funkcionalitātes atbalstam. Piemēram, jūs varat izveidot pakalpojumu PowerApp, lai papildinātu programmu Finance and Operations ar informāciju, kas izgūta no citas sistēmas. 

Lai uzzinātu vairāk par pakalpojuma PowerApps iegulšanu, noskatieties īso video [Kā iegult pakalpojumu PowerApps programmā Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Iegultā pakalpojuma PowerApp pievienošana lapai
### <a name="overview"></a>Pārskats
Pirms pakalpojuma PowerApp iegulšanas Finance and Operations klientā vispirms ir jāatrod vai jāveido pakalpojums PowerApp, kas ietver vēlamo vizuālo informāciju un/vai funkcionalitāti. Mēs šeit nesniegsim detalizētu pakalpojuma PowerApp izstrādes procesu. Ja pakalpojumu PowerApps izmantojat pirmo reizi, ieteicams skatīt tēmu [Ievads par pakalpojumu PowerApps](https://docs.microsoft.com/en-us/powerapps/getting-started).

Ja esat sagatavojies konkrēta pakalpojuma PowerApp iegulšanai, varat izvēlēties vienu no diviem piekļuves pakalpojumam PowerApp lapā veidiem atkarībā no tā, kurš scenārijs jums ir piemērotāks. Pirmais piekļuves veids ir standarta darbību rūtī pievienotās pogas PowerApps izmantošana. Pakalpojums PowerApps, kas ir pievienots, izmantojot šo mehānismu, tiek parādīts izvēlnes vienumu veidā izvēlnes pogā PowerApps. Pēc atlasīšanas visi šie izvēlnes vienumi tiek atvērti tajā rūts pusē, kura ietver iegulto pakalpojumu PowerApp. Vai arī pakalpojumu PowerApp var parādīt tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu. 

Konfigurējot iegulto pakalpojumu PowerApp programmā Finance and Operations, var atlasīt vienu lauku, kuru vēlaties nosūtīt uz pakalpojumu PowerApp kā ievadi. Tādējādi pakalpojums PowerApp reaģē atbilstoši datiem, kuri pašlaik tiek skatīti programmā Finance and Operations.  

### <a name="details"></a>Informācija
Tālāk ir sniegti norādījumi par to, kā pakalpojumu PowerApp iegult Finance and Operations tīmekļa vietnes klientā.  

1. Atveriet lapu, kurā vēlaties iegult pakalpojumu PowerApp. Tā ir tā pati lapa, kas ietver visus datus, kuri ir jānosūta pakalpojumam PowerApp kā ievade.  
2. Atveriet rūti **Ievietot PowerApp**.
   - Noklikšķiniet uz **Opcijas** un pēc tam atlasiet **Personalizēt šo formu**. Izvēlnē **Ievietot** atlasiet **PowerApp**. Pēc tam atlasiet sadaļu, kurai vēlaties pievienot pakalpojumu PowerApp. Ja vēlaties iegult pakalpojumu PowerApp izvēlnes pogā PowerApps, atlasiet darbību rūti. Ja vēlaties iegult pakalpojumu PowerApp tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu).   
   - Ja piekļuvei pakalpojumam PowerApp paredzēts izmantot izvēlnes pogu PowerApps, var arī standarta darbību rūtī noklikšķināt uz izvēlnes pogas **PowerApps** un pēc tam atlasīt **Ievietot PowerApp**.  
3. Konfigurējiet iegulto pakalpojumu PowerApp.
   - Laukā **Nosaukums** ir norādīts teksts, kas ir redzams uz pogas vai cilnes, kas ietvers iegulto pakalpojumu PowerApp. Iespējams, ka PowerApp nosaukums šajā laukā ir jāatkārto bieži.  
   - **App ID** ir pakalpojuma PowerApp, ko vēlaties iegult, GUID. Lai izgūtu šo vērtību, atrodiet pakalpojumu PowerApp lapā [web.powerapps.com](https://web.powerapps.com) un pēc tam sadaļā **Detalizēta informācija** atrodiet lauku **App ID**.  
   - Izmantojot opciju **PowerApp ievades dati**, var pēc izvēles atlasīt lauku, kas ietver datus, kurus vēlaties nosūtīt uz pakalpojumu PowerApp kā ievadi. Lai iegūtu sīkāku informāciju par to, kā pakalpojums PowerApp var piekļūt datiem, kas nosūtīti no programmas Finance and Operations, skatiet sadaļu tālāk šajā tēmā ar nosaukumu [Tāda pakalpojuma PowerApp izveide, kas piesaista datus no programmas Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations).  
   - Atlasiet opciju **Programmas izmērs**, kas atbilst iegulšanai paredzētajam pakalpojuma PowerApp veidam. Atlasiet opciju **Plāns** mobilajām ierīcēm izveidotajam pakalpojumam PowerApps un **Plašs** planšetdatoriem izveidotajam pakalpojumam PowerApps. Tādējādi iegultajam pakalpojumam PowerApp tiek nodrošināts pietiekami daudz vietas.
   - Kopsavilkuma cilnē **Juridiskas personas** var izvēlēties, kurām juridiskajām personām ir pieejams pakalpojums PowerApp. Noklusējuma iestatījums ir pakalpojuma parādīšana PowerApp visām juridiskajām personām.  
4. Apstipriniet, ka konfigurācija ir pareiza, un pēc tam noklikšķiniet uz **Ievietot**, lai iegultu pakalpojumu PowerApp lapā. Tiek parādīta uzvedne ar norādi atsvaidzināt pārlūkprogrammu, lai redzētu iegulto pakalpojumu PowerApp. 

## <a name="sharing-an-embedded-powerapp"></a>Iegultā pakalpojuma PowerApp koplietošana
Kad pakalpojums PowerApp lapā ir iegults un ir apstiprināts, ka tas darbojas pareizi un visu datu konteksts ir no lapas nosūtīts, šo iegulto pakalpojumu PowerApp var koplietot ar citiem lietotājiem sistēmā. To var izdarīt divos dažādos veidos, izmantojot produkta personalizēšanas iespējas.

- To ieteicams veikt sistēmas administratoram, kurš personalizāciju var piegādāt visiem lietotajiem vai lietotāju apakškopai. 

- Vai arī lapas personalizācijas datus var eksportēt, nosūtīt tos vienam vai vairākiem lietotājiem un norādīt visiem šiem lietotājiem importēt šīs izmaiņas. Izmantojot personalizēšanas rīkjoslā esošo opciju Pārvaldīt, varat eksportēt un importēt personalizācijas.

Lai iegūtu sīkāku informāciju par personalizēšanas iespējām produktā un kā tās izmantot, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md) .

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Tāda pakalpojuma PowerApp izveide, kas piesaista datus no programmas Finance and Operations
Lai varētu izveidot pakalpojumu PowerApp, kas tiks iegults programmā Finance and Operations, ir jāizmanto programmas Finance and Operations ievades dati. Pakalpojumā PowerApp šiem ievades datiem var piekļūt, izmantojot mainīgo vērtību Param("EntityId").  

Piemēram, PowerApp funkcijā OnStart var iestatīt programmas Finance and Operations ievades datus kā mainīgo vērtību, kā norādīts tālāk.

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Iegultā pakalpojuma PowerApp skatīšana
Lai skatītu iegulto pakalpojumu PowerApp programmas Finance and Operations lapā, atveriet lapu, izmantojot iegulto pakalpojumu PowerApp. Ņemiet vēra, ka pakalpojumam PowerApps var piekļūt, izmantojot pogu PowerApps standarta darbību rūtī, vai to var redzēt tieši lapā kā jaunu cilni, kopsavilkuma cilni, paneli vai kā jaunu darbvietas sadaļu. Pirmo reizi mēģinot ielādēt pakalpojumu PowerApp lapā, tiek parādīta uzvedne ar norādi pieteikties pakalpojumā PowerApps, lai pārliecinātos, ka lietotājam ir atbilstošas atļaujas izmantot pakalpojumu PowerApp.   

## <a name="editing-an-embedded-powerapp"></a>Iegultā pakalpojuma PowerApp rediģēšana
Kad pakalpojuma PowerApp iegulšana lapā ir pabeigta, var būt nepieciešams veikt dažas pakalpojuma PowerApp konfigurācijas izmaiņas. Piemēram, varbūt vēlaties mainīt ar iegulto pakalpojumu PowerApp saistītu etiķeti vai ir izveidota jauna PowerApp versija un ir jāatjaunina programmas ID, lai norādītu jaunāko pakalpojuma PowerApp versiju. 

Lai rediģētu iegultā PowerApp konfigurāciju, izpildiet tālāk aprakstītās darbības.
1. Atveriet rūti **Rediģēt PowerApp**. 
   - Ja piekļuvei iegultajam pakalpojumam PowerApp izmanto izvēlnes pogu PowerApps, ar peles labo pogu noklikšķiniet uz izvēlnes pogas PowerApps un atlasiet **Personalizēt**. Nolaižamajā izvēlnē **Atlasīt PowerApp** atlasiet konfigurējamo pakalpojumu PowerApp.  
   - Ja iegultais pakalpojums PowerApp tiek parādīts tieši lapā, atlasiet **Opcijas** un pēc tam atlasiet **Personalizēt šo formu**. Izmantojot rīku **Atlasīt**, noklikšķiniet uz iegultā pakalpojuma PowerApp.  
2. Veiciet nepieciešamās pakalpojuma PowerApps konfigurācijas izmaiņas un pēc tam noklikšķiniet uz **Saglabāt**.  

## <a name="removing-an-embedded-powerapp"></a>Iegultā pakalpojuma PowerApp noņemšana
Kad pakalpojuma PowerApp iegulšana lapā ir pabeigta, to, ja nepieciešams, var noņemt divējādi. 

- Atveriet rūti **Rediģēt PowerApp**, izmantojot norādījumus iepriekš šīs tēmas sadaļā [Iegultā pakalpojuma PowerApp rediģēšana](#editing-an-embedded-powerapp). Apstipriniet, ka rūtī ir redzama informācija par iegulto pakalpojumu PowerApp, kuru vēlaties noņemt, un pēc tam noklikšķiniet uz pogas **Dzēst**. 

- Tā kā iegultais pakalpojums PowerApp ir saglabāts kā personalizācijas dati, notīrot lapas personalizācijas datus, tiek noņemtai visi šajā lapā iegultā pakalpojuma PowerApps dati. Ņemiet vērā, ka lapas personalizācijas datu notīrīšana ir neatgriezenisks process, un to nevar atsaukt. Lai noņemtu lapā konkrētos personalizācijas datus, atlasiet **Opcijas** un pēc tam noklikšķiniet uz **Personalizēt šo formu**. Izvēlnē **Pārvaldīt** atlasiet pogu **Notīrīt**. Veicot pārlūkprogrammas atsvaidzināšanu, visi šīs lapas iepriekšējie personalizācijas dati ir noņemti. Lai iegūtu sīkāku informāciju par to, kā optimizēt lapas, izmantojot personalizēšanu, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).  

## <a name="appendix"></a>Pielikums 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Izstrādātāja pakalpojuma PowerApp iegulšanas iespēju kontrole
Pēc noklusējuma lietotāji var iegult pakalpojumu PowerApps jebkurā lapā, izmantojot vai nu izvēlnes pogas PowerApps metodi, vai parādot to tieši lapā kā cilni, kopsavilkuma cilni, paneli vai jaunu darbvietas sadaļu. Tomēr, ja nepieciešams, izstrādātāji var arī konfigurēt šo funkciju, lai atļautu iegult pakalpojumu PowerApps tikai konkrētās lapās, izmantojot tālāk norādītās metodes. 

- **isPowerAppPersonalizationEnabled** — ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad izvēlnes poga PowerApps netiek parādīta un lietotāji nevarēs iegult pakalpojumu PowerApps jebkurā šīs lapas vietā, tostarp arī cilnes veidā. 

- **isPowerAppTabPersonalizationEnabled** — ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad lietotāji nevarēs iegult pakalpojumu PowerApps tieši lapā kā cilni, kopsavilkuma cilni vai panorāmas sadaļu. Lietotāji joprojām var iegult pakalpojumu PowerApps, izmantojot izvēlnes pogu PowerApps, ja iegulšana lapā ir atļauta.  

Nākamajā piemērā ir parādīta jauna klase ar divām metodēm, kuras nepieciešamas, lai varētu konfigurēt pakalpojuma PowerApps iegulšanas vietu.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


