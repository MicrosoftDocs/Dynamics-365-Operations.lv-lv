---
title: Iegult pamatnes programmas no Power Apps
description: Šajā rakstā skaidrots, kā iegult canvas Microsoft Power Apps programmas no klienta, lai palielinātu preces funkcionalitāti.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: d7dc45e56c5fa616c288ebb4b919f039b7358794
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123660"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Iegult pamatnes programmas no Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps ir pakalpojums, kas sniedz iespējas izstrādātājiem un ar tehniku nesaistītiem lietotājiem būvēt pielāgotas biznesa programmas mobilajām ierīcēm, planšetdatoriem un tīmeklim bez nepieciešamības rakstīt kodu. Finanšu un operāciju programmas atbalsta integrāciju ar Power Apps. Canvas programmas, kuras jūs, jūsu organizācija vai plašāk izstrādātu plašumu, var tikt iegultas finanšu un operāciju programmās, lai paplašinātu produkta funkcionalitāti. Piemēram, varat veidot canvas programmu Power Apps, lai papildinātu finanšu un operāciju programmu ar informāciju, kas izgūta no citas sistēmas.

Lai uzzinātu vairāk par pamatnes programmu iegulšanu, noskatieties īso video [Pamatnes programmu iegulšana](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Iegultas pamatnes programmas pievienošana no Power Apps lapai

Pirms pamatnes programma iegulšanas no Power Apps klientā vispirms ir jāatrod vai jāizveido pakalpojums, kas ietver vēlamo vizuālo informāciju vai funkcionalitāti. Šajā rakstā nav iekļauts detalizēts programmu veidošanas procesa apraksts. Ja pirmo reizi izmantojat Power Apps, skatiet [Power Apps dokumentācija](/powerapps/).

Ir trīs veidi, kā iegult canvas programmu finanšu un operāciju programmā. Varat izmantot pieeju, kas vislabāk atbilst jūsu scenārijam. 

- Iegulstiet pamatnes programmu pogā **Power Apps** standarta darbību rūtī lapā. Programmas, ko pievienojat šādā veidā, tiek parādītas kā izvēlnes pogas **Power Apps** vienumi, un programmas tiek atvērtas sānu rūtīs. 
- Iegulstiet pamatnes programmu tieši esošajā lapā kā jaunu cilnes lapu (koptabulu, kopsavilkuma cilni, failu vai darbvietas sadaļu).
- Izveidojiet jaunu pilnas lapas pieredzi pamatnes programmai no informācijas paneļa.

Konfigurējot iegulto pamatnes programmu, var atlasīt vienu lauku, kuru vēlaties nosūtīt uz programma kā kontekstu. Šī darbība ļauj programmai reaģēt atbilstoši datiem, kuri pašlaik tiek skatīti.

> [!NOTE]
> Jūs nevarat izmantot šo mehānismu, lai iegultu modeļa vadītas programmas.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Pamatnes programmas iegulšana esošā lapā

Šī procedūra parāda, kā iegult pamatnes programmu esošā lapā no Power Apps.

1. Atveriet lapu, kurā vēlaties iegult pamatnes programmu. Šī lapa ietvers jebkādus datus, kas ir jānodod programmai kā ievade.
2. Atveriet rūti **Pievienot pakalpojumu no Power Apps**:

    - Ja programma tiks tieši iegulta lapā, atlasiet **Opcijas** \> **Personalizēt šo lapu** \> **Vairāk** un pēc tam veiciet kādu no tālāk minētajām darbībām.

        - Ja ir ieslēgts līdzeklis **Pilnas lapas programmas**, atlasiet **Pievienot lapu** un atlasiet reģionu, kurā vēlaties pievienot programmu. Lai iegultu programmu izvēlnes pogā **Power Apps**, atlasiet darbību rūti. Lai iegultu programmu tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu). Pēc tam rūtī **Pievienot programmu** atlasiet **Power Apps**.
        - Ja līdzeklis **Pilnas lapas programmas** ir izslēgts, atlasiet **Pievienot lapu no Power Apps** un atlasiet reģionu, kurā vēlaties pievienot programmu. Lai iegultu programmu izvēlnes pogā **Power Apps**, atlasiet darbību rūti. Lai iegultu programmu tieši lapā, atlasiet attiecīgo cilni, kopsavilkuma cilni, paneli vai sadaļu (ja izmantojat darbvietu).

    - Ja programmas piekļuvei paredzēts izmantot izvēlnes pogu **Power Apps**, varat standarta darbību rūtī atlasīt izvēlnes pogu **Power Apps** un atlasīt **Pievienot programmu**.

3. Konfigurējiet iegulto programmu. Papildinformāciju skatiet tālāk [šī raksta sadaļā Canvas app](#configuring-a-canvas-app) konfigurēšana.
4. Kad esat pārbaudījis, ka konfigurācija ir pareiza, atlasiet **Ievietot**.

    - Ja līdzeklis **Saglabātie skati** ir izslēgts, tiek piedāvāts atsvaidzināt pārlūkprogrammu, lai redzētu iegulto programmu.
    - Ja līdzeklis **Saglabātie skati** ir ieslēgts, ir jāsaglabā skats, lai izmaiņas tiktu saglabātas.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Pamatnes programmas iegulšana kā pilnas lapas pieredze no informācijas paneļa

Varat vēlēties iegult vadības panelī esošu pārklases programmu, ja programma nav saistīta ar esošu lapu vai ja vēlaties skatīt programmu kā pilnu lapas pieredzi finanšu un operāciju programmā.

> [!NOTE]
> Lai padarītu šo iespēju pieejamu, līdzekļa pārvaldībā ir jāieslēdz līdzeklis **Pilnas lapas programmas**. 

1. Atveriet informācijas paneli.
2. Atlasiet un turiet lapu (vai noklikšķiniet ar peles labo pogu), atlasiet **Personalizēt** un pēc tam atlasiet **Pievienot lapu**.
3. Rūtī **Pievienot lapu** atlasiet **Power Apps**.
4. Konfigurējiet iegulto programmu. Papildinformāciju skatiet tālāk [šī raksta sadaļā Canvas app](#configuring-a-canvas-app) konfigurēšana.
5. Atlasiet **Saglabāt**, lai programmu pievienotu informācijas panelim kā jaunu elementu.
6. Atlasiet vadības panelī jaunu elementu un apstipriniet, ka pamatnes programma tiek parādīta, kā paredzēts.

### <a name="configuring-a-canvas-app"></a>Pamatnes programmas konfigurēšana

Iegulstot pamatnes programmu, ir jāiestata tālāk minētie parametri.

- **Nosaukums** — ievadiet tekstu, kas jāparāda pogai vai cilnei, kas satur iegulto programmu. Iespējams, ka pakalpojuma nosaukums šajā laukā ir jāatkārto bieži.
- **Programmas ID** — norādiet vispārēji unikālu identifikatoru (globally unique identifier - GUID) pamatnes programmai, ko vēlaties iegult. Lai izgūtu šo vērtību, atrodiet pakalpojumu lapā [make.powerapps.com](https://make.powerapps.com) un pēc tam skatiet sadaļas **Detalizēta informācija** lauku **Programmas ID**.
- **Programmas ievades konteksts** — varat atlasīt lauku, kas ietver datus, kurus vēlaties nosūtīt uz programmu kā ievadi. Papildinformāciju par to, kā programma var piekļūt datiem, kas tiek sūtīti no finanšu un operāciju programmām, skatiet sadaļā Programmas veidošana, [kas vēlāk šajā rakstā palīdz piekļūt no finanšu un operāciju programmām](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) nosūtīto datu.

    Sākot ar versiju 10.0.19, pašreizējā juridiskā persona arī tiks pārsūtīta kā konteksts pamatnes programmā, izmantojot **cmp** URL parametru. Šī darbība neietekmēs mērķa pamatnes programmu, kamēr šī programma izmanto šo informāciju.

- **Programmas izmērs** — atlasiet iegultās programmas veidu. Atlasiet **Šaurs** mobilajām ierīcēm paredzētām programmām un **Plats** — planšetdatoriem paredzētam programmām. Šis parametrs nodrošina, ka programmai ir pietiekami daudz vietas.
- **Juridiskas personas** — varat atlasīt juridiskās personas, kurām jābūt pieejamai programmai. Pēc noklusējuma programma ir pieejama visām juridiskajām personām. Šī opcija ir pieejama tikai tad, ja iegulti tieši esošā lapā un līdzeklis **[Saglabātie skati](saved-views.md)** ir izslēgts.

## <a name="sharing-an-embedded-app"></a>Iegultā pakalpojuma koplietošana

Kad pamatnes programma lapā ir iegulta un ir apstiprināts, ka tā darbojas pareizi, šo programmu var koplietot ar citiem lietotājiem sistēmā. Lai koplietotu iegultu pamatnes programmu, rīkojieties šādi.

1. [Kopīgojiet pamatnes programmu pakalpojumā Power Apps](/powerapps/maker/canvas-apps/share-app) ar atbilstošajiem lietotājiem, lai viņi varētu piekļūt programmai pakalpojumā Power Apps.
2. Ar izvēlētiem lietotājiem kopīgojiet personalizēšanu, kas ir saistīta ar iegulto programmu. Jūs variet izmantot jebkuru no sekojošiem risinājumiem.

    - **Publicēt skatu (ieteicams):** ja līdzeklis **[Saglabātie skati](saved-views.md)** ir ieslēgts, ieteicams izveidot skatu, kas ietver iegulto pamatnes programmu, un publicēt šo skatu vēlamajiem lietotājiem. Šī pieeja nodrošina to, ka visi lietotāji, kuriem ir drošības lomas, kas ir vērstas uz publicēto skatu, redzēs pamatnes programmu lapā.

        Varat arī publicēt pamatnes programmu, kas ir iegulta kā pilnas lapas pieredze no informācijas paneļa. Informācijas panelī atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) ar programmu saistīto elementu, atlasiet **Personalizēt** un pēc tam atlasiet **Publicēt lapu**. Yiek parādīta pieredze, kas ir līdzīga *publicēto skatu* pieredzei, un varat atlasīt drošības lomas, lai to publicētu. Ja ir ieslēgts līdzeklis **Uzlabots atbalsts juridiskām personām par saglabātajiem skatiem**, atjauninājumā 10.0.21 vai jaunākās versijās varat publicēt programmu vēlamajām juridiskajām personām.

    - Ja līdzeklis **Saglabātie skati** ir izslēgts, sistēmas administrators var piešķirt personalizēšanu, kas ietver pamatnes programmu atbilstošajai lietotāju kopai, izmantojot lapu **Personalizēšana**. Varat arī eksportēt lapas personalizācijas un nosūtīt tās vienam vai vairākiem lietotājiem. Pēc tam katrs no šiem lietotājiem var importēt personalizāciju. Personalizēšanas rīkjoslā ir pieejamas pogas, kas ļauj eksportēt un importēt personalizācijas.

> [!NOTE]
> Ja canvas programma ir koplietota ar ārējiem lietotājiem, šie lietotāji nevar izmantot iegulto programmu finanšu un operāciju programmās. Tomēr viņi var piekļūt programmai tieši pakalpojumā Power Apps. Ārējie lietotāji ietver viesus un lietotājus, kas nepieder Microsoft 365 Azure direktorijam, kurā ir izvietota finanšu un operāciju programma.

Lai iegūtu sīkāku informāciju par personalizēšanas iespējām produktā un kā tās izmantot, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md) .

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Notiek canvas programmas veidošana, kas izmanto no finanšu un operāciju programmām sūtītos datus

Veidojot pārvadu programmu, kas tiks iegulta finanšu un operāciju programmā, viena svarīga procesa daļa ir izmantot ievades datus no šīs finanšu un operāciju programmas. Izmantojot izstrādes Power Apps pieredzi, ievades datiem, kas ir nodoti no finanšu un operāciju programmas, var piekļūt, **izmantojot mainīgo Param("EntityId"**). Turklāt, sākot ar versiju 10.0.19, pašreizējā juridiskā persona arī tiks pārsūtīta pamatnes programmā, izmantojot **Param("cmp")** mainīgo. 

Piemēram, programmas funkcijā OnStart varat iestatīt ievades datus no finanšu un operāciju programmām uz šādu mainīgo:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Pamatnes programmas skatīšana

Lai finanšu un operāciju programmās skatītu iegulto canvas programmu lapā, dodieties tikai uz lapu, kurā ir iegulta programma. Atcerieties, ka programmām var piekļūt, izmantojot **Power Apps** pogu standarta darbības rūtī. Vai arī tie var parādīties tieši lapā kā jauna cilne, kopsavilkuma cilne vai panelis, vai kā jauna darbvietas sadaļa. Kad lietotāji pirmo reizi mēģinās ielādēt programmu lapā, viņiem tiks piedāvāts pieteikties. Šī darbība nodrošina, ka lietotājiem ir attiecīgās atļaujas, lai lietotu programmu.

## <a name="editing-an-embedded-app"></a>Iegultā pakalpojuma rediģēšana

Kad pakalpojuma iegulšana lapā ir pabeigta, var būt nepieciešams veikt dažas pakalpojuma konfigurācijas izmaiņas. Piemēram, varbūt vēlaties mainīt ar iegulto pakalpojumu saistītu etiķeti vai ir izveidota jauna pakalpojuma versija un ir jāatjaunina programmas ID, lai norādītu jaunāko pakalpojuma versiju.

Lai rediģētu iegultā pakalpojuma konfigurāciju, izpildiet tālāk aprakstītās darbības.

1. Atveriet rūti **Rediģēt pakalpojumu**.

    - Ja piekļuvei iegultajai programmai izmanto izvēlnes pogu Power Apps, atlasiet un turiet (vai ar peles labo pogu noklikšķiniet) izvēlnes pogu Power Apps un atlasiet **Personalizēt**. Nolaižamajā izvēlnē **Atlasīt pakalpojumu** atlasiet konfigurējamo pakalpojumu.
    - Ja iegultais pakalpojums tiek parādīts tieši lapā, atlasiet **Opcijas** un pēc tam atlasiet **Personalizēt šo lapu**. Izmantojot rīku **Atlasīt**, noklikšķiniet uz iegultā pakalpojuma.
    - Ja iegultā programma tika pievienota no informācijas paneļa, atveriet informācijas paneli, atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) elementu, kas ir saistīts ar pamatnes programmu, atlasiet **Personalizēt** un atlasiet **Rediģēt lapu**.

2. Veiciet nepieciešamās pakalpojuma konfigurācijas izmaiņas un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="removing-an-app"></a>Pakalpojuma noņemšana

Kad programmas iegulšana lapā ir pabeigta, to, ja nepieciešams, var noņemt vairākos veidos.

- Pārejiet uz **rūts Rediģēt programmu**, izmantojot norādījumus no sadaļas [Iegultās programmas](#editing-an-embedded-app) rediģēšana iepriekš šajā rakstā. Apstipriniet, ka rūtī ir redzama informācija par iegulto pakalpojumu, kuru vēlaties noņemt, un pēc tam noklikšķiniet uz pogas **Dzēst**.
- Ja iegultā programma tika pievienota no informācijas paneļa, atveriet informācijas paneli, atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) elementu, kas ir saistīts ar pamatnes programmu, atlasiet **Personalizēt** un atlasiet **Noņemt lapu**. 
- Tā kā iegultais pakalpojums ir saglabāts kā personalizācijas dati, notīrot lapas personalizācijas datus, tiek noņemti visi šajā lapā iegultie pakalpojumi. Ņemiet vērā, ka lapas personalizācijas datu notīrīšana ir neatgriezenisks process, un to nevar atsaukt. Lai noņemtu lapā konkrētos personalizācijas datus, atlasiet **Opcijas**, tad **Personalizēt šo lapu**, un pēc tam pogu **Notīrīt**. Veicot pārlūkprogrammas atsvaidzināšanu, visi šīs lapas iepriekšējie personalizācijas dati ir noņemti. Lai iegūtu sīkāku informāciju par to, kā optimizēt lapas, izmantojot personalizēšanu, skatiet tēmu [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

## <a name="appendix"></a>Pielikums

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Izstrādātājs] Pamatnes programmas modelēšana formā

Kamēr šis raksts fokusējas uz iegultām canvas programmām, izmantojot personalizēšanu, izstrādātājiem ir arī opcija formai pievienot canvas programmu, izmantojot Visual Studio izstrādes pieredzi. Lai to paveiktu, formai vienkārši pievienojiet PowerAppsHostControl. Kontrolei pieejamie metadatu rekvizīti nodrošina tādas pašas iespējas kā personalizēšanas pieredzei.

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

