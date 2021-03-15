---
title: Iegult pamatnes programmas no Power Apps
description: Šajā tēmā ir paskaidrots, kā iegult pamatnes programmas no pakalpojuma Microsoft Power Apps klientā, lai atbalstītu produkta funkcionalitāti.
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fbdd4dd1bb0b850319b12e55b0e68d6fdc516ad6
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798381"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Iegult pamatnes programmas no Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps ir pakalpojums, kas sniedz iespējas izstrādātājiem un ar tehniku nesaistītiem lietotājiem būvēt pielāgotas biznesa programmas mobilajām ierīcēm, planšetdatoriem un tīmeklim bez nepieciešamības rakstīt kodu. Finance and Operations programmas atbalsta integrāciju ar Power Apps. Jūsu, jūsu organizācijas vai plašākas ekosistēmas izstrādātās pamatnes programma var iegult Finance and Operations programmās klientā produkta funkcionalitātes atbalstam. Piemēram, varat izveidot pamatnes programmu no Power Apps, lai papildinātu programmu Finance and Operations ar informāciju, kura tiek izgūta no citas sistēmas.

Lai uzzinātu vairāk par Power Apps iegulšanu, noskatieties īso video [Kā iegult Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) .

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Iegultas pamatnes programmas pievienošana no Power Apps lapai

### <a name="overview"></a>Pārskats

Pirms pamatnes programma iegulšanas no Power Apps klientā vispirms ir jāatrod vai jāizveido pakalpojums, kas ietver vēlamo vizuālo informāciju vai funkcionalitāti. Šajā tēmā nav ietverta detalizēta informācija par programmu veidošanas procesu. Ja pirmo reizi izmantojat Power Apps, skatiet [Power Apps dokumentācija](https://docs.microsoft.com/powerapps/).

Ir divi veidi, kā piekļūt noteiktai pamatnes programmai lapā, kad esat gatavs iegult programmu. Varat izvēlēties, kurš risinājums ir piemērotāks jūsu scenārijam. Pirmais risinājums izmanto **Power Apps** pogu, kas tika pievienota standarta darbības rūtīm. Programmas, ko pievienojat, izmantojot šo pieeju, parādās kā **Power Apps** izvēlnes pogas vienumi. Atlasot vienu no šiem vienumiem, tiek paradīta sānu rūts, kura ietver iegulto pakalpojumu. Vai arī pakalpojumu var iegult tieši lapā kā jaunu cilni, kopsavilkuma cilni vai paneli, vai kā jaunu darbvietas sadaļu.

Konfigurējot iegulto pamatnes programmu, var atlasīt vienu lauku, kuru vēlaties nosūtīt uz programma kā kontekstu. Šī darbība ļauj programmai reaģēt atbilstoši datiem, kuri pašlaik tiek skatīti.

> [!NOTE]
> Pašlaik nevarat izmantot šo mehānismu, lai iegultu modelētas programmas.  

### <a name="details"></a>Detaļas

Šī procedūra parāda, kā iegult pamatnes programmu no Power Apps tīmekļa vietnes klientā.

1. Atveriet lapu, kurā vēlaties iegult pamatnes programmu. Šī lapa ir lapa, kurā ir dati, kas ir jānodod programmai kā ievade.
2. Atveriet rūti **Pievienot pakalpojumu no Power Apps**:

    - Noklikšķiniet uz **Opcijas** un pēc tam atlasiet **Personalizēt šo lapu**. Izvēlnē **Ievietot** izvēlieties **Power Apps**. Pēc tam atlasiet sadaļu, kurai vēlaties pievienot pakalpojumu. Ja vēlaties iegult pakalpojumu zem izvēlnes pogas Power Apps, atlasiet darbības rūti. Ja vēlaties iegult pakalpojumu tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu).
    - Ja piekļuvei pakalpojumam paredzēts izmantot izvēlnes pogu Power Apps, var arī standarta darbības rūtī noklikšķināt uz izvēlnes pogas **Power Apps** un pēc tam atlasīt **Ievietot pakalojumu**.

3. Konfigurējiet iegulto pakalpojumu:

    - Laukā **Nosaukums** ir norādīts teksts, kas ir redzams uz pogas vai cilnes, kas ietvers iegulto pakalpojumu. Iespējams, ka pakalpojuma nosaukums šajā laukā ir jāatkārto bieži.
    - Lauks **Programmas ID** norāda vispārēji unikālu identifikatoru (globally unique identifier - GUID) pamatnes programmai, ko vēlaties iegult. Lai izgūtu šo vērtību, atrodiet pakalpojumu lapā [make.powerapps.com](https://make.powerapps.com) un pēc tam skatiet sadaļas **Detalizēta informācija** lauku **Programmas ID**.
    - Izmantojot opciju **Pakalpojuma ievades konteksts**, var pēc izvēles atlasīt lauku, kas ietver datus, kurus vēlaties nosūtīt uz pakalpojumu kā ievadi. Skatiet tālāk šajā tēmā sadaļu ar nosaukumu [Tādas programmas izveide, kas piesaista datus, kas nosūtīti no Finance and Operations programmām](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps), lai iegūtu sīkāku informāciju par to, kā pakalpojums var piekļūt datiem, kas nosūtīti no programmām Finance and Operations.
    - Atlasiet opciju **Programmas izmērs**, kas atbilst iegulšanai paredzētajam pakalpojuma veidam. Atlasiet opciju **Plāns** mobilajām ierīcēm izveidotajiem pakalpojumiem un **Plašs** planšetdatoriem izveidotajiem pakalpojumiem. Tādējādi iegultajam pakalpojumam tiek nodrošināts pietiekami daudz vietas.
    - Kopsavilkuma cilnē **Juridiskas personas** var izvēlēties, kurām juridiskajām personām ir pieejams pakalpojums. Noklusējuma iestatījums ir nodrošina pakalpojuma pieejamību visām juridiskajām personām. Šī opcija ir pieejama tikai tad, ja ir atspējots līdzeklis [Saglabātie skati](saved-views.md). 

4. Apstipriniet, ka konfigurācija ir pareiza, un pēc tam noklikšķiniet uz **Ievietot**, lai iegultu pakalpojumu Power App lapā. Tiek parādīta uzvedne ar norādi atsvaidzināt pārlūkprogrammu, lai redzētu iegulto pakalpojumu.

## <a name="sharing-an-embedded-app"></a>Iegultā pakalpojuma koplietošana

Kad pamatnes programma lapā ir iegulta un ir apstiprināts, ka tā darbojas pareizi ar visu datu kontekstu, kas ir nosūtīts no šīs lapas, šo programmu var koplietot ar citiem lietotājiem sistēmā. Lai koplietotu iegultu pamatnes programmu, rīkojieties šādi.

1. [Kopīgot pamatnes programmu](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) ar atbilstošajiem lietotājiem, lai viņi varētu piekļūt programmai Power Apps. 

2. Pārliecinieties, vai mērķa lietotājiem ir atbilstošas personalizācijas, lai iegultā programma parādās, kad šie lietotāji apskata lapu. Jūs variet izmantot jebkuru no sekojošiem risinājumiem.

    - Ieteicams: izmantojiet līdzekli [Saglabātie skati](saved-views.md), lai izveidotu un publicētu skatu, kas ietver iegulto programmu. Šī pieeja nodrošina to, ka visi lietotāji, kuriem ir drošības lomas, kas ir vērstas uz publicēto skatu, redzēs programmu Finance and Operations lietojumprogrammās. 
    - Ja nav ieslēgts līdzeklis Saglabātie skati, jūs varat likt sistēmas administratoram veikt personalizāciju, kas iekļauj iegulto programmu visiem lietotājiem vai lietotāju apakškopai. Varat arī eksportēt lapas personalizācijas un nosūtīt tās vienam vai vairākiem lietotājiem. Pēc tam katrs no šiem lietotājiem var importēt personalizācijas. Personalizēšanas rīkjoslā ir pieejamas darbības, kas ļauj eksportēt un importēt personalizācijas. 
    
> [!NOTE]
> Ja pamatnes programma ir koplietota ar ārējiem lietotājiem, šie lietotāji nevar izmantot iegulto programmu Finance and Operations programmās. Tomēr viņi var piekļūt programmai tieši pakalpojumā Power Apps. Ārējie lietotāji iekļauj viesus un lietotājus, kuri nepieder Microsoft 365 Azure direktorijam, kurā ir izvietota Finance and Operations lietojumprogramma.

Lai iegūtu sīkāku informāciju par personalizēšanas iespējām produktā un kā tās izmantot, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md) .

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Pamatnes programmas izveide, kas izmanto no programmām Finance and Operations nosūtītos datus

Kad izveidojat pamatnes programmu, kas tiks iegulta Finance and Operations lietojumprogrammā, viena svarīga procesa daļa ir izmantot ievades datus no šīs Finance and Operations programmas. Pakalpojuma Power Apps izstrādes pieredze rāda, ka Finance and Operations programmas nodotajiem ievades datiem var piekļūt, izmantojot mainīgo vērtību **Param("Entityld")**.

FPiemēram, pakalpojuma funkcijā OnStart var iestatīt programmu Finance and Operations ievades datus kā mainīgo vērtību, kā norādīts tālāk.

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Pamatnes programmas skatīšana

Lai skatītu iegulto pamatnes programmu lapā programmās Finance and Operations, vienkārši atveriet lapu, kurā ir iegulta programma. Atcerieties, ka programmām var piekļūt, izmantojot **Power Apps** pogu standarta darbības rūtī. Vai arī tie var parādīties tieši lapā kā jauna cilne, kopsavilkuma cilne vai panelis, vai kā jauna darbvietas sadaļa. Kad lietotāji pirmo reizi mēģinās ielādēt programmu lapā, viņiem tiks piedāvāts pieteikties. Šī darbība nodrošina, ka lietotājiem ir attiecīgās atļaujas, lai lietotu programmu.

## <a name="editing-an-embedded-app"></a>Iegultā pakalpojuma rediģēšana

Kad pakalpojuma iegulšana lapā ir pabeigta, var būt nepieciešams veikt dažas pakalpojuma konfigurācijas izmaiņas. Piemēram, varbūt vēlaties mainīt ar iegulto pakalpojumu saistītu etiķeti vai ir izveidota jauna pakalpojuma versija un ir jāatjaunina programmas ID, lai norādītu jaunāko pakalpojuma versiju.

Lai rediģētu iegultā pakalpojuma konfigurāciju, izpildiet tālāk aprakstītās darbības.

1. Atveriet rūti **Rediģēt pakalpojumu**.

    - Ja piekļuvei iegultajam pakalpojumam izmanto izvēlnes pogu Power Apps, ar peles labo pogu noklikšķiniet uz izvēlnes pogas Power Apps un atlasiet **Personalizēt**. Nolaižamajā izvēlnē **Atlasīt pakalpojumu** atlasiet konfigurējamo pakalpojumu.
    - Ja iegultais pakalpojums tiek parādīts tieši lapā, atlasiet **Opcijas** un pēc tam atlasiet **Personalizēt šo lapu**. Izmantojot rīku **Atlasīt**, noklikšķiniet uz iegultā pakalpojuma.

2. Veiciet nepieciešamās pakalpojuma konfigurācijas izmaiņas un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="removing-an-app"></a>Pakalpojuma noņemšana

Kad pakalpojuma iegulšana lapā ir pabeigta, to, ja nepieciešams, var noņemt divējādi.

- Atveriet rūti **Rediģēt pakalpojumu**, izmantojot norādījumus iepriekš šīs tēmas sadaļā [Iegultā pakalpojuma rediģēšana](#editing-an-embedded-app). Apstipriniet, ka rūtī ir redzama informācija par iegulto pakalpojumu, kuru vēlaties noņemt, un pēc tam noklikšķiniet uz pogas **Dzēst**.
- Tā kā iegultais pakalpojums ir saglabāts kā personalizācijas dati, notīrot lapas personalizācijas datus, tiek noņemti visi šajā lapā iegultie pakalpojumi. Ņemiet vērā, ka lapas personalizācijas datu notīrīšana ir neatgriezenisks process, un to nevar atsaukt. Lai noņemtu lapā konkrētos personalizācijas datus, atlasiet **Opcijas**, tad **Personalizēt šo lapu**, un pēc tam pogu **Notīrīt**. Veicot pārlūkprogrammas atsvaidzināšanu, visi šīs lapas iepriekšējie personalizācijas dati ir noņemti. Lai iegūtu sīkāku informāciju par to, kā optimizēt lapas, izmantojot personalizēšanu, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

## <a name="appendix"></a>Pielikums

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Izstrādātājs] Programmas iegulšanas vietas norādīšana

Pēc noklusējuma lietotāji var iegult pakalpojumus jebkurā lapā, izmantojot vai nu izvēlnes pogas Power Apps metodi, vai parādot to tieši lapā kā cilni, kopsavilkuma cilni, paneli vai jaunu darbvietas sadaļu. Tomēr, ja nepieciešams, izstrādātāji var arī konfigurēt šo funkciju, lai atļautu iegult pakalpojumus tikai konkrētās lapās, izmantojot tālāk norādītās metodes.

- **irIespējotaPowerAppPersonalizācija** – ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad izvēlnes poga Power Apps netiek parādīta, un lietotāji nevarēs iegult pakalpojumus jebkurā šīs lapas vietā, tostarp arī cilnes veidā.
- **irIespējotaPowerAppPersonalizācija** – ja šī metode konkrētajai lapai atgriež atbildi Aplams, tad lietotāji nevarēs iegult pakalpojumus tieši lapā kā cilni, kopsavilkuma cilni FastTab vai panorāmas sadaļu. Lietotāji joprojām var iegult pakalpojumus, izmantojot Power Apps izvēlnes pogu, ja iegulšana lapā ir atļauta.

Nākamajā piemērā ir parādīta jauna klase ar divām metodēm, kuras nepieciešamas, lai varētu konfigurēt pakalpojumu iegulšanas vietu.

```powerapps
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]