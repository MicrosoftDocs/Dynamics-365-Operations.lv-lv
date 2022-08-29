---
title: Veidot daudzvalodu pārskatus Elektroniskajos pārskatos
description: Šajā rakstā skaidrots, kā var lietot elektronisko pārskatu (ER) iezīmes, lai projektētu un ģenerētu daudzvalodu pārskatus.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285491"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Veidot daudzvalodu pārskatus Elektroniskajos pārskatos

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Kā biznesa lietotājs jūs varat izmantot [Elektronisko pārskatu (ER)](general-electronic-reporting.md) struktūru, lai konfigurētu izejošo dokumentu formātus, kas jums jāģenerē saskaņā ar dažādu valstu vai reģionu juridiskajām prasībām. Ja šīs prasības prasa, lai izejošie dokumenti tiktu ģenerēti dažādās valodās dažādām valstīm vai reģioniem, varat konfigurēt vienu ER formātu, kas satur no valodas atkarīgus resursus. Šādā veidā varat atkārtoti izmantot formātu, lai ģenerētu izejošos dokumentus dažādām valstīm vai reģioniem. Varat arī izmantot vienu ER formātu, lai ģenerētu izejošo dokumentu dažādās valodās attiecīgiem klientiem, kreditoriem, filiālēm vai jebkurai citai pusei.

Varat konfigurēt ER datu modeļus un modeļu kartējumus kā datu avotus, kas ir konfigurēti, lai definētu datu plūsmu, kas norāda, kādi programmas dati tiek ievietoti ģenerētajos dokumentos. Kā ER konfigurācijas [nodrošinātājs](general-electronic-reporting.md#Provider), lai ģenerētu noteiktus izejošos dokumentus, [var](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) publicēt konfigurētus datu modeļus, modeļu kartējumus un formātus kā ER risinājuma komponentus. Varat arī atļaut klientiem [augšupielādēt](general-electronic-reporting-manage-configuration-lifecycle.md) publicēto ER risinājumu, lai to varētu izmantot un pielāgot. Ja domājat, ka klienti var runāt citās valodās, varat konfigurēt ER komponentus, lai tajos būtu no valodas atkarīgi resursi. Šādā veidā rediģējamā ER komponenta saturu var sniegt klienta lietotāja vēlamajā valodā izstrādes laikā.

No valodas atkarīgus resursus varat konfigurēt kā ER etiķetes. Šīs etiķetes var izmantot, lai konfigurētu ER komponentus šādiem nolūkiem:

- Noformēšanas laikā:

    - Pasniegt saturu konfigurētajiem ER komponentiem lietotāja vēlamajā valodā.

- Izpildlaikā:

    - Ģenerēt no valodas atkarīgu saturu izejošajiem dokumentiem.
    - Norādiet brīdinājuma un kļūdu ziņojumus lietotāja vēlamajā valodā.
    - Pieprasīt nepieciešamos laukus lietotāja vēlamajā valodā.

ER etiķetes var konfigurēt katrā ER [konfigurācijā](general-electronic-reporting.md#Configuration), kas ietver dažādus komponentus. Etiķetes var uzturēt neatkarīgi no ER datu modeļu konfigurētās loģikas, ER modeļa kartēšanas un ER formāta komponentes.

Katra ER etiķete tiek identificēta ar ID, kas ir unikāls to ER konfigurācijas sfērā, kas ietver šo etiķeti. Katra iezīme var saturēt iezīmju tekstu katrai valodai, kas tiek atbalstīta pašreizējā Microsoft Dynamics 365 Finanšu instancē. Šīs atbalstītās valodas ietver izvietoto pielāgojumu valodas.

## <a name="entry"></a>Ieraksts

Noformējot ER datu modeli, ER modeļa kartēšanu vai ER formātu, **Tulkošanas** opcija tiek rādīta ikreiz, kad atlasāt lauku, kas var saturēt tulkojamo kontekstu. Kad jūs atlasāt šo opciju, jūs varat saistīt atlasīto lauku ar ER etiķeti sadaļā **Teksta tulkošanas** <a name="TextTranslationPane">rūtī</a>. Varat atlasīt esošu ER etiķeti vai arī pievienot jaunu ER etiķeti, ja tā vēl nav pieejama. Kad atlasāt vai pievienojat ER etiķeti, varat pievienot saistītu tekstu katrai valodai, ko atbalsta pašreizējā finanšu instance.

Sekojošajā attēlā ir parādīts, kā šis tulkojums tiek veikts rediģējamā ER datu modelī. Šajā piemērā **PurchaseOrder** lauka **Apraksta** atribūts rediģējamam **Rēķinu modelim** tiek tulkots Austrijas vācu (DE-AT) un japāņu (JA) valodās.

![Nodrošina ER etiķetes tulkojumu ER datu modeļa noformētājā.](./media/er-multilingual-labels-refer.png)

Var tulkot tikai etiķešu tekstu etiķetēm, kas atrodas rediģējamā ER komponentā. Piemēram, ja atlasāt opciju **Tulkot** ER modeļa kartēšanas datu avota etiķetes atribūtam un pēc tam izvēlaties ER etiķeti, kas atrodas pamata ER datu modelī, jūs redzēsiet etiķetes saturu, bet to nevarēsiet mainīt. Šādos gadījumos lauks **Tulkotais teksts** nav pieejams, kā parādīts sekojošajā ilustrācijā.

![Piedāvātā ER etiķetes tulkojuma pārskatīšana ER modeļa kartēšanas noformētājā.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Jūs nevarat izmantot noformētājus, lai dzēstu etiķeti, kas ievadīta rediģējamā ER komponentā.

## <a name="scope"></a>Tvērums

ER etiķetes var tikt attiecinātas uz vairākiem tulkotiem ER komponentu atribūtiem.

### <a name="data-model-component"></a>Datu modeļa komponents

Konfigurējot ER datu modeli, varat pievienot tam ER etiķetes. Modeļa vienuma **Etiķetes** un **Apraksta** atribūti, katra modeļa lauks un katra <a id="LinkModelEnum"></a>modeļa uzskaitījuma vērtība var tikt saistīta ar ER etiķeti, kas pievienota ER datu modelim.

![Tiek nodrošināts Apraksts atribūtam ER datu modeļu noformētājā.](./media/er-multilingual-labels-refer.png)

Kad ER datu modelis ir konfigurēts šādā veidā, tā saturs tiks prezentēts ER datu modeļa noformētāja lietotājiem katrā lietotāja vēlamajā valodā. Tāpēc modeļa uzturēšana ir vienkāršota. Sekojošās ilustrācijās ir parādīts, kā šī funkcionalitāte darbojas lietotājiem, kuri izmanto DE-AT un JA iestatītu kā vēlamo valodu.

![ER datu modeļa noformētāja izkārtojums lietotājam ar DE-AT iestatītu kā vēlamo valodu.](./media/er-multilingual-labels-refer-de.png)

![ER datu modeļa noformētāja izkārtojums lietotājam ar JA iestatītu kā vēlamo valodu.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Modeļa kartēšanas komponents

Tā kā ER modeļa kartēšana ir balstīta uz ER datu modeli, to datu modeļa elementu iezīmes, uz kuriem attiecas, parādās lietotāja izvēlētā valodā modeļu kartēšanas veidotājā. Sekojošajā attēlā ir parādīts, kā ir izskaidrota lauka **PurchaseOrder** nozīme rediģējamā modeļa kartēšanā, izmantojot **Apraksta** atribūta etiķeti, kas ir pievienota konfigurētajam datu modelim. Ievērojiet, ka šī etiķete ir norādīta lietotāja vēlamajā valodā (šajā piemērā DE-AT).

![ER datu kartēšanas noformētāja izkārtojums lietotājam ar DE-AT iestatītu kā vēlamo valodu.](./media/er-multilingual-labels-show-mapping.png)

Kad **Lietotāja ievades parametru** datu avota **Etiķetes** atribūts ir konfigurēts kā saistīts ar ER etiķeti, parametru lauks, kas atbilst šim datu avotam, tiek parādīts lietotāja dialoglodziņā izpildlaikā lietotājiem vēlamajā valodā.

### <a name="format-component"></a>Komponenta formāts

Konfigurējot ER formātu, varat pievienot tam ER etiķetes. Katra konfigurētā datu avota **Etiķetes** un **Palīdzības teksta** atribūti var būt saistīti ar ER etiķeti, kas pievienotaER formātam. Katra **formāta** uzskaitījuma **vērtības** etiķešu un aprakstu atribūtus <a id="LinkFormatEnum"></a> var saistīt arī ar ER etiķeti, kas ir pieejama rediģējamā ER formātā.

> [!NOTE]
> Varat arī saistīt šos atribūtus ar pamata ER datu modeļa ER etiķeti, kas atkārtoti izmanto modeļa etiķetes katrā ER formātā, kas ir konfigurēta šim ER datu modelim.

Kad ER formāts ir konfigurēts šādā veidā, formāta saturs tiks prezentēts ER operāciju noformētāja lietotājiem katrā lietotāja vēlamajā valodā. Tāpēc ir vienkāršota konfigurētās loģikas formāta uzturēšana un analīze.

Tā kā ER formāts balstās uz ER datu modeli, datu modeļa elementu etiķetes tiek parādītas lietotāja vēlamajā valodā ER formāta noformētājā.

Kad **Lietotāja ievades parametru** datu avota **Etiķetes** atribūts ir konfigurēts kā saistīts ar ER etiķeti, parametru lauks, kas atbilst parametram lietotāja dialoglodziņā izpildlaikā, tiek parādīts lietotājam kā uzvedne. Sekojošās ilustrācijās ir parādīts, kā var saistīt **Lietotāja ievades parametra** datu avota **Etiķetes** atribūtu noformēšanas laikā uz ER etiķeti, lai lietotājiem tiktu pieprasīts parametrs dažādās lietotāja vēlamajās valodās (tiek rādīts angļu valodā Amerikas Savienotajām valstīm (EN-US) un DE-AT valodām) izpildlaikā.

![Tiek nodrošināts lietotāja ievades parametra atribūtu tulkojums ER operāciju noformētājā.](./media/er-multilingual-labels-refer-format.png)

![ER kreditora maksājumu apstrāde izpildlaikā EN-US lietotāja vēlamajā valodā.](./media/er-multilingual-labels-show-runtime-en.png)

![ER kreditora maksājumu apstrāde izpildlaikā DE-AT lietotāja vēlamajā valodā.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Izteiksmes

Lai varētu izmantot etiķeti ER [izteiksmē](er-formula-language.md), jāizmanto sintakse **@"GER\_LABEL:X"**, kur priedēklis **@** norāda, ka operands attiecas uz etiķeti, **GER\_LABEL** norāda, ka ER etiķete ir iesaistīta, un **X** ir ER etiķetes ID.

![Tiek konfigurētas ER izteiksmes, kas satur atsauci uz ER etiķeti ER formulas noformētājā.](./media/er-multilingual-labels-expression1.png)

Lai atsauktos uz sistēmas (programmas) etiķeti, izmantojiet sintaksi **@"X"**, kur prefikss **@** norāda, ka operands attiecas uz etiķeti, un **X** ir sistēmas etiķetes ID.

![Tiek konfigurētas ER izteiksmes, kas satur atsauci uz programmas etiķeti ER formulas noformētājā.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modeļa kartēšana

ER modeļa kartēšanas izpausmi var konfigurēt, izmantojot etiķeti. Kad šo kartējumu izsauc palaistais ER formāts, lai ģenerētu izejošo dokumentu, izpildes konteksts ietver valodas kodu. Konfigurēta izteiksmes etiķete tiks aizpildīta ar etiķetes tekstu, kas ir konfigurēts šai konteksta valodai.

Ja norādītajai etiķetei nav tulkojuma tā formāta izpildes konteksta valodai, kas izsauc modeļa kartēšanu, tā vietā tiek izmantots etiķetes teksts EN-US valodā.

#### <a name="format"></a>Formāts

ER formāta izpausmi var konfigurēt, izmantojot etiķetes. Kad šis formāts ir palaists, lai ģenerētu izejošo dokumentu, izpildes konteksts ietver valodas kodu. Konfigurēta izteiksmes etiķete tiks aizpildīta ar etiķetes tekstu, kas ir konfigurēts šai konteksta valodai.

![Nodrošina tulkojumu ER rediģējamās izteiksmes ER etiķetei ER formulas noformētājā.](./media/er-multilingual-labels-refer-in-expression.png)

![Datu saistījuma paraugs, kas attiecas uz ER etiķeti ER operāciju noformētājā.](./media/er-multilingual-labels-refer-in-binding.png)

Varat konfigurēt ER formāta **FAILA** komponentu, lai ģenerētu pārskatu lietotāja vēlamajā valodā.

![Iestatiet FAILA komponentu ER operāciju noformētājā, lai ģenerētu pārskatu lietotāja vēlamajā valodā.](./media/er-multilingual-labels-language-context-user.png)

Ja jūs konfigurējat ER formātu šādā veidā, tad pārskats tiek ģenerēts, izmantojot attiecīgo ER etiķešu tekstu. Sekojošās ilustrācijās ir parādīti pārskatu piemēri EN-US un DE-AT lietotāja valodām.

![Pārskata priekšskatījums, kas ģenerēts EN-US lietotāja vēlamajā valodā.](./media/er-multilingual-labels-report-preview-en.png)

![Pārskata priekšskatījums, kas ģenerēts DE-AT lietotāja vēlamajā valodā.](./media/er-multilingual-labels-report-preview-de.png)

Ja norādītajai etiķetei nav tulkojuma tā formāta izpildes konteksta valodai, tā vietā tiek izmantots etiķetes teksts EN-US valodā.

> [!TIP]
> Varat izmantot MAPI un **atšķirīgus** **FAILA** komponentu tipus rediģējamā ER formātā, lai norādītu, kā tiek ģenerēts izejošais fails. Lai nosauktu ģenerētā faila nosaukumu, konfigurējiet [ER](er-formula-language.md) izteiksmi komponenta **faila** nosaukuma parametram. Konfigurētajā izteiksmē varat lietot iezīmes. Tā kā **faila nosaukuma parametrs** pēc noklusējuma ir valodas diagnostika, visu iezīmju teksts, uz ko atsaucaties šajā izteiksmē, izpildlaikā tiek pakļauts noklusētajā EN-US valodā. Taču versijā 10.0.28 **un jaunākā versijā varat iespējot parametru Lietot valodas izvēli izteiksmes līdzekli 'Faila** nosaukums'. Aprēķinātā **faila** nosaukuma izteiksme **ņem vērā** valodas preferences parametru.

## <a name="language"></a>Valoda

ER atbalsta dažādus veidus, lai norādītu valodu ģenerētajam pārskatam. Cilnes **Formāts** laukā **Valodas preferences** varat atlasīt šādas vērtības:

- **Uzņēmuma preference** — izveidot pārskatu uzņēmuma noteiktajā valodā.

    ![Ievadiet ER operāciju noformētājā uzņēmuma vēlamo valodu kā ģenerētā pārskata valodu.](./media/er-multilingual-labels-language-context-company.png)

- **Lietotāja preference** — izveidot pārskatu lietotāja vēlamajā valodā.
- **Skaidri definēts** – izveidot pārskatu valodā, kas norādīta izstrādes laikā.

    ![Ievadiet ER operāciju noformētājā izstrādes laikā norādīto valodu kā ģenerētā pārskata valodu.](./media/er-multilingual-labels-language-context-fixed.png)

- **Definēts izpildlaikā** – izveidot pārskatu valodā, kas norādīta izpildlaikā. Atlasot šo vērtību, laukā **Valoda** konfigurējiet ER izteiksmi, kas atgriež valodas kodu valodai, piemēram, atbilstošā klienta valodu.

    ![Ievadiet ER operāciju noformētājā izpildlaikā norādīto valodu kā ģenerētā pārskata valodu.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kultūrai raksturīgais formatējums

ER atbalsta dažādus veidus, lai norādītu kultūru ģenerētajam pārskatam. Tāpēc datumam, laikam un skaitliskām vērtībām var izmantot pareizo kultūras formātu. Kad izstrādāsiet ER formātu, cilnē **Formāts**, laukā **Kultūras preferences** varat izvēlēties vienu no šādām vērtībām katram **Kopējā\\faila**, **Excel\\faila**, **PDF\\faila** vai **PDF\\apvienošanas** tipa formāta komponentam:

- **Lietotāja preference** - formatējiet vērtības saskaņā ar lietotāja vēlamo kultūru. Šī kultūra ir definēta laukā **Datuma, laika un numura formāts** cilnē **Preferences** lapā **Lietotāja opcijas**.

    ![Lietotāja izvēlētās kultūras definēšana kā ģenerētā pārskata kultūra ER operāciju veidotājā.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Skaidri definēts** - formatējiet vērtības saskaņā ar kultūru, kas ir noteikta dizaina laikā.

    ![Definējiet kultūru, kas projektēšanas laikā norādīta kā ģenerētā ziņojuma kultūra ER operāciju izstrādātājā.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Definēts izpildlaikā** - formatējiet vērtības saskaņā ar kultūru, kas ir noteikta izpildlaikā. Ja atlasāt šo vērtību, cilnē **Kartēšana** laukā **Datuma, laika un numura formāts** konfigurējiet ER izteiksmi, kas atgriež kultūras kodu kultūrai, piemēram, attiecīgā debitora kultūrai.

    ![Definējiet kultūru, kas izpildlaikā definēta kā ģenerētā ziņojuma kultūra ER operāciju izstrādātājā.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> ER komponents, kam definēta noteikta kultūra, iespējams, satur pakārtotos ER komponentus, kas ir konfigurēti teksta vērtības aizpildīšanai. Pēc noklusējuma pamatkomponenta kultūra tiek izmantota šo komponentu vērtību formatēšanai. Jūs varat izmantot šādas iebūvētās ER funkcijas, lai konfigurētu šo komponentu saistījumus un vērtību formatēšanai pielietotu alternatīvu kultūru:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Versijā 10.0.20 un jaunākā versijā **Kopējo\\failu** un **Excel\\failu** tipu formāta komponentu lokāle tiek izmantota vērtību formatēšanai ģenerētā dokumenta [PDF pārvēršanas](electronic-reporting-destinations.md#OutputConversionToPDF) laikā.

## <a name="translation"></a>Transformācija

Varat pievienot nepieciešamās ER etiķetes rediģējamam ER komponentam. Kad tiek pievienota ER etiķete, to var tulkot divos veidos: manuāli un automātiski.

### <a name="manual-translation"></a>Manuālais tulkojums

Kad pievienojat ER etiķeti **Teksta tulkojumam** [rūtī](#TextTranslationPane), varat to manuāli tulkot visās valodās, kas atbalstītas pašreizējā finanšu instancē. Varat atlasīt vēlamo valodu **Valodas** laukā sadaļās **Sistēmas valoda** vai **Lietotāja valoda**, ievadiet atbilstošo tekstu atbilstošajā **Tulkotā teksta** laukā un pēc tam atlasiet **Tulkot**. Šis process ir jāatkārto visām nepieciešamajām valodām un visām pievienotajām etiķetēm.

### <a name="automatic-translation"></a>Automātiskā tulkošana

ER komponenta konfigurācija tiek veikta ar to ER konfigurācijas melnraksta versiju, kas atrodas rediģējamā ER komponentā.

![ER konfigurācijas lapa, kas piedāvā piekļuvi konfigurācijas versijai Melnraksta statusā.](./media/er-multilingual-labels-configurations.png)

Kā aprakstīts iepriekš šajā rakstā, rediģējamam ER komponentam var pievienot nepieciešamās ER iezīmes. Šādā veidā var norādīt ER etiķešu tekstu EN-US valodā. Pēc tam varat eksportēt ER komponenta etiķetes, izmantojot iebūvēto ER funkciju. Atlasiet to ER konfigurācijas melnraksta versiju, kas satur rediģējamo ER komponentu un pēc tam atlasiet **Apmainīt \> Eksporta etiķetes**.

![ER konfigurācijas lapa, kas ļauj eksportēt ER etiķetes no atlasītās konfigurācijas versijas.](./media/er-multilingual-labels-export.png)

Varat eksportēt vai nu visas etiķetes, vai arī vienas valodas etiķetes, ko norādāt eksportēšanas sākumā. Etiķetes tiek eksportētas kā zip faili, kas satur XML failus. Katrs XML fails satur vienas valodas etiķetes.

![Eksportētā faila paraugs, kas satur ER etiķetes DE-AT valodā.](./media/er-multilingual-labels-in-xml.png)

Šis formāts tiek lietots automātiskam etiķešu tulkojumam, ko izmanto ārējie tulkošanas pakalpojumi, piemēram [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Kad saņemat tulkotās etiķetes, jūs varat tās importēt atpakaļ uz tās melnraksta versiju, kurā atrodas ER komponenti, kam pieder šīs etiķetes. Atlasiet to ER konfigurācijas melnraksta versiju, kas satur rediģējamo ER komponentu un atlasiet **Apmainīt \> Ielādēt etiķetes**.

![ER konfigurācijas lapa, kas ļauj importēt ER etiķetes uz atlasīto konfigurācijas versiju.](./media/er-multilingual-labels-load.png)

Tulkotās etiķetes tiks importētas atlasītajā ER konfigurācijā. Tulkotās etiķetes, kas pastāv šajā ER konfigurācija, ir aizstātas. Ja ER konfigurācijā trūkst tulkotas etiķetes, tās tiek pievienotas.

## <a name="lifecycle"></a>Dzīves cikls

ER komponenta etiķetes, kas var tikt rediģētas, tiek turētas kopā ar citu komponenta saturu atbilstošajā ER konfigurācijas versijā.

Bāzes ER komponenta etiķetes var tikt minētas atvasinātajā ER komponenta versijā, ko izveidojat, lai ieviestu jūsu izmaiņas.

> [!TIP]
> Veidojot ER risinājumu, var atvasināt savu ER [datu](er-overview-components.md#data-model-component) modeļa komponentu no saņemtā. Šajā atvasinātajā datu modelī varat ieviest savas ER iezīmes un izmantot tās visos ER formātos, kas datu modeli izmantos kā datu avotu. Pēc tam varat iegūt savu ER [formāta](er-overview-components.md#format-component) komponentu no tā, ko nodrošina, atlasot atvasināto ER datu modeli, nevis sniegto. Versijā 10.0.28 un jaunākās versijās varat aktivizēt uzlaboto piekļuvi iezīmes paplašinātajam ER datu modeļa līdzeklim, **lai piekļūtu augoša ER** datu modeļa iezīmēm atvasinātos ER formāta komponentos, pat ja atvasinātajam ER komponentam atlasītais ER datu modelis atšķiras no tā, kas tika izmantots pamata ER komponentā.
>
> Ja atvasinātajam komponentam un tā augošajam komponentam tiek izmantots tas pats iezīmes nosaukums, kā atbilstošāko tiek izmantots tās tulkojums.

ER versijas kontrolē etiķešu piešķiri jebkuram atribūtam ER komponentā. Etiķešu piešķires izmaiņas tiek reģistrētas rediģējamā ER komponenta izmaiņu sarakstā (delta), kas ir izveidots kā atvasināta sniegtā ER komponenta versija. Šīs izmaiņas tiks apstiprinātas, kad atvasinātā versija tiks balstīta uz jaunu bāzes versiju.

## <a name="functions"></a>Funkcijas

Iebūvētā [LISTOFFIELDS](er-functions-list-listoffields.md) ER funkcija var piekļūt ER etiķetēm, kas ir konfigurētas dažām ER komponentu vienībām.

Kā aprakstīts iepriekš šajā rakstā, katra modeļa vai formāta ER uzskaitījuma vērtības etiķetes un apraksta atribūti var būt saistīti ar ER etiķeti, **·** **·**[...](#LinkModelEnum)[kas](#LinkFormatEnum) ir pieejama atbilstošajā ER komponentā. Varat konfigurēt ER izteiksmi, kur tiek izsaukta funkcija **LISTOFFIELDS**, lietojot ER uzskaitījumu kā argumentu. Šī izteiksme atgriež sarakstu, kurā ir ietverts ieraksts katrai ER uzskaitījuma vērtībai, kas ir definēta kā šīs funkcijas arguments. Katram ierakstam ir tāda ER etiķetes vērtība, kas ir saistīta ar ER uzskaitījuma vērtību:

- ER etiķetes vērtība, kas ir saistīta ar **Etiķetes** atribūtiem tiek saglabāta atgrieztā ieraksta **Etiķetes** laukā.
- ER etiķetes vērtība, kas ir saistīta ar **Apraksta** atribūtiem tiek saglabāta atgrieztā ieraksta **Apraksta** laukā.

## <a name="performance"></a><a name=performance></a>Veiktspēja

Konfigurējot ER formāta komponentu, lai ģenerētu atskaiti vēlamajā [valodā](#language) vai, lai importētu ienākošo dokumentu, kura saturu parsē vēlamā valoda, iesakām iespējot līdzekli **Pašreizējā lietotāja vēlamās valodas kešdarba ER palaišanai** darbvietā [Līdzekļu pārvaldība](../../fin-ops/get-started/feature-management/feature-management-overview.md). Šis līdzeklis palīdz uzlabot veiktspēju, īpaši tiem ER formāta komponentiem, kuri satur vairākas atsauces uz marķējumu ER formulās un saistījumos un daudzas [validācijas](general-electronic-reporting-formula-designer.md#TestFormula) kārtulas, lai ģenerētu lietotāja ziņojumus jums vēlamajā valodā.

Mainot ER konfigurācijas versijas statusu no **Melnraksts** **uz** Pabeigts, ja konfigurācijas versija satur ER iezīmes, šīs iezīmes tiek saglabātas programmas datu bāzē. Glabāšanas shēma ir atkarīga no stāvokļa, kad ir pieejama **ER etiķešu glabāšanas** funkcionalitāte:

- Ja funkcija nav aktivizēta, **visas iezīmes tiek glabātas tabulas ERSOLUTIONVERSIONTABLE** laukā LABELXML **kā** viens XML fragments.
- Ja funkcija ir aktivizēta, tabulā **ERSOLUTIONVERSIONLABELSTABLE** katrai valodai tiek izveidots atsevišķs ieraksts. Šīs **tabulas** laukā SATURS ir ietvertas iezīmes pa valodām kā saspiests XML fragments.

Mēs iesakām iespējot **ER etiķešu glabāšanas līdzekli** Paātrināt ER pārvaldības **darbvietu**. Šī funkcija palīdz uzlabot tīkla joslas platumu un vispārējo sistēmas veiktspēju, jo vairākumā gadījumu vienas valodas ER etiķetes tiek izmantotas, strādājot ar vienu ER konfigurāciju.

Lai lietotu atlasīto glabāšanas shēmu visu ER konfigurāciju glabāšanai pašreizējā finanšu instancē, veiciet šādus soļus.

1. Pārejiet uz **sadaļu Organizācijas** > **administrēšana** > **periodiski. Lietojiet atlasītās iezīmes, glabājot shēmu visām ER konfigurācijām**.
2. Atlasiet **Labi**.


## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas funkcijas](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
