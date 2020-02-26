---
title: Datu integrācijas tehnoloģijas izvēle
description: Šis raksts sniedz norādījumus par dažādām Human Resources pārvaldīto datu integrācijas opcijām, aprakstot dažādu integrācijas tehnoloģiju īpašības tā, lai integrētāji varētu pieņemt informētus lēmumus attiecībā uz tehnoloģiju piemērotību savām vajadzībām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029892"
---
# <a name="choose-a-data-integration-technology"></a>Datu integrācijas tehnoloģijas izvēle

 Dynamics 365 Human Resources pārvalda biznesa datus, kas ir noderīgi dažādos biznesa procesos. Šis raksts sniedz norādījumus par dažādām Human Resources pārvaldīto datu integrācijas opcijām, aprakstot dažādu integrācijas tehnoloģiju īpašības tā, lai integrētāji varētu pieņemt informētus lēmumus attiecībā uz tehnoloģiju piemērotību savām vajadzībām.

## <a name="data-integration-vision"></a>Datu integrācijas vīzija

Microsoft uzskata, ka biznesa dati ir galvenie līdzekļi, kas padara uzņēmumu unikālu. Biznesa dati ir ļoti vērtīgi. Dati, ko apkopojusi un uzturējusi viena biznesa daļa, attiecas uz datiem, ko apkopojusi cita biznesa daļa, un šīs attiecības var tikt izmantotas biznesa procesu un biznesa informācijas uzlabošanai jūsu organizācijā. Vieglas, drošas, stabilas piekļuves nodrošināšana biznesa datiem, neatkarīgi no tā, kādai sistēmai "pieder" dati, ir mūsu vīzijas pamatprincips Human Resources datu integrācijai.

Vēsturiski datu integrācija starp vairākām sistēmām ir bijusi sarežģīta.
Microsoft veic darbības, lai atvieglotu datu integrāciju, un liels solis pretī šim mērķim tiek realizēts, izmantojot [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Virzoties uz priekšu, Human Resources dod priekšroku Common Data Service kā Human Resources datu publiskajam interfeisam. Laika gaitā mēs sagaidām, ka visi svarīgākie dati, ko pārvalda Human Resources, tiks sniegti Common Data Service. Mēs iesakām Common Data Service kā izvēles tehnoloģiju lielākajai daļai integrācijas pieteikumu. Lai gan mēs saprotam, ka ne visi jūsu pieteikumam nepieciešamie dati pašlaik ir Common Data Service un ka jūsu projekta termiņiem var būt nepieciešama alternatīva tehnoloģija, lūdzu, paziņojiet mums, ja Common Data Service neatbilst jūsu integrācijas vajadzībām.

## <a name="integration-technologies"></a>Integrācijas tehnoloģijas

Turpmākajās sadaļās aprakstītas dažādas datu integrācijas tehnoloģijas, kas pieejamas lietošanai Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service elementi

Common Data Service ir izvēlētais publisko datu interfeiss Human Resources. Common Data Service ir izveidots uz pārdomātas platformas, kas ir izaugusi no Dynamics 365 "XRM" platformas, uz kuras tiek izveidoti [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) risinājumi.

Common Data Service nodrošina platformu datu elementiem un API, lai piekļūtu šiem elementiem. Kad jūsu organizācijā tiek izvietota Human Resources, tā tiek pieslēgta Common Data Service instancei, un elementi, kas uztur Human Resources datus, tiek izvietoti šajā Common Data Service instancē, padarot elementus un to datus pieejamus jebkuram pieteikumam, kas var pieslēgties Common Data Service instancei. Atkarībā no tā, kādas Human Resources programmas lietojat, Human Resources vai nu veic datu operācijas tieši pret Common Data Service elementiem (šis ir gadījums Attract un Onboard), vai sinhronizē datus uz/no Common Data Service elementiem.

Kad datu elementi, kas sniedz datus jūsu integrācijas programmās, atrodas Common Data Service, varat pilnībā izmantot [Common Data Service un API, ko tas atbalsta](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Starp atbalstītajiem API ir [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kas nodrošina OData ieviešanu, lai piekļūtu Common Data Service.

Common Data Service elementi un saistītie API ir vislabākā opcija, lai piekļūtu Human Resources datiem, izmantojot tīmekļa programmas, tīmekļa pakalpojumus/API un no jebkuru citu programmu, kas pieslēdzas OData plūsmām.

> [!NOTE]
> Tā kā lēmums padarīt Common Data Service par izvēlēto datu interfeisu Human Resources ir salīdzinoši nesens, varat nākt pie atziņas, ka Human Resources datu elementi, kas nepieciešami integrācijai, vēl nav pieejami Common Data Service<sup>1.</sup> Ja jūsu integrācijai nepieciešamie Human Resources elementi vēl nav pieejami, būs jāgaida, kamēr datu elementi tika padarīti pieejami vai arī būs jāizmanto kāda no tālāk aprakstītajām integrācijas tehnoloģijām.
> 
> Pēc noklusējuma Common Data Service integrācija ir izslēgta jaunās vidēs, kurās nav ietverti nodrošinātie demonstrācijas dati. Tā ir ieslēgta jaunās vidēs, kas ietver demonstrācijas datus, un vide sāk sinhronizēt datus, kad tie tiek nodrošināti. Pēc tam, kad jūsu vide ir gatava sinhronizēt datus, varat ieslēgt integrāciju.

<sup>1</sup>Sarakstu ar Human Resources elementiem, kas pieejami Common Data Service, skatiet [Human Resources un Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Attract un Onboard visi elementi ir pieejami Common Data Service.

### <a name="dmfdixf-entities"></a>DMF/DIXF elementi

Human Resources, kas galvenokārt izveidota uz tās pašas platformas kā Finance and Operations programmas, nodrošina [Datu pārvaldības struktūru (Data Management Framework — DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), ko dažreiz sauc arī par datu importēšanas/eksportēšanas struktūru vai DIXF, un datu elementu kopu, ko var izmantot datu importēšanai/eksportēšanai uz Human Resources vai no tās. Lai gan Common Data Service elementi ir Human Resources izvēlētais datu integrācijas interfeiss, DMF elementi joprojām būs noderīgi dažos tālāk minētajos gadījumos.

- Common Data Service elementi vēl nav pieejami.

- Integrācijai ir nepieciešamas augstas veiktspējas lielapjoma datu importēšanas/eksportēšanas iespējas.

DMF elementi pašlaik sniedz vispilnīgāko Human Resources datu segumu.

DMF nav piemērots reāllaika integrācijām (piemēram, ja ir nepieciešama tūlītēja lietotāja atsauksme lietotāja interfeisā), jo pakotņu operācijas ir plānoti pakešuzdevumi, un tām bieži vien ir vismaz 1-2 minūšu latentums pirms paketes pakalpojums pieņem darbu izpildei un nepieciešams papildu laiks, lai pabeigtu importēšanas/eksportēšanas operāciju.

DMF var būt vislabākā izvēle, ja ir nepieciešama liela caurlaides spēja (piemēram, naktī ieplānota daudzu tūkstošu ierakstu importēšana/eksportēšana).

> [!NOTE]
> DMF nav pieejams Attract un Onboard.

### <a name="dmf-package-rest-api"></a>DMF pakotnes REST API

DMF nodrošina [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) manipulēšanai ar datu pakotnēm. Šo API var izmantot, lai programmiski mijiedarbotos ar DMF, atļaujot, piemēram, tādas darbības, kas minētas tālāk.

- Datu pakotnes importēšana.

- Datu pakotnes eksportēšana.

- Importēšanas/eksportēšanas operācijas statusa pārbaude.

DMF pakotne REST API tiek pilnībā atbalstīta Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL datu bāze (BYOD)

DMF papildus sniedz jaudīgu līdzekli (vispārzināms kā [Atnes savu datu bāzi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)vai BYOD (Bring Your Own Database), kas ļauj Human Resources eksportēt datus uz savu Microsoft Azure SQL datu bāzi. Tas nodrošina milzīgu elastību, jo, kad dati ir iekļauti jūsu SQL datu bāzē, varat izmantot jebkuru programmu vai starpprogrammatūru, kas var pieslēgties SQL datu glabātuvei.

BYOD parasti ir jāuzskata par tikai lasīšanai paredzētu risinājumu. Lai gan varat Azure SQL datu bāzē manipulēt un glabāt jebkurus datus (piemēram, datu jaucējprogrammas), Azure SQL datu bāzē glabātie dati netiks sinhronizēti ar Human Resources.

BYOD ir piemērots pārskatu risinājumiem, datu integrācijām, datu jaucējprogrammām un kā datu avots [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) konveijeram.

> [!NOTE]
> BYOD nav pieejams Attract un Onboard.

### <a name="odata-enabled-entities"></a>OData iespējotie elementi

Lielākā daļa DMF elementu ir iespējoti arī piekļuvei, izmantojot Human Resources datu pakalpojumu (OData). Dokumentācija, kas paredzēta [Finance and Operations OData pakalpojumam](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata), parasti attiecas arī uz Human Resources, lai gan uz to neattieksies dokumentācija par savu OData sniegto elementu veidošanu.

Lai gan Common Data Service un OData implementācijai, ko sniedz Common Data Service (izmantojot [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), tiek dota priekšroka pret Human Resources datu pakalpojumu, Human Resources datu pakalpojumam pašlaik ir pilnīgāks elementu segums Human Resources datiem.

### <a name="excel-add-in"></a>Excel pievienojumprogramma

[Excel pievienojumprogramma](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) padara OData iespējoto elementu izmantošanu ārpus acīmredzamā. Tas nodrošina ērtu veidu, kā lietotājam iegūt un modificēt Human Resources datus, izmantojot pazīstamo Excel lietotāja interfeisu.

Excel pievienojumprogramma ir piemērota speciālai datu importēšanai/eksportēšanai, ko veic biznesa domēna eksperti. Lai veiktu periodisku datu integrāciju, kam nepieciešama programmatiska automatizācija, piemērotāka būs cita integrācijas tehnoloģija.

### <a name="data-integrator"></a>Datu integrētājs

Common Data Service administratora pieredze nodrošina [Datu integrētāja pakalpojumu](https://docs.microsoft.com/powerapps/administrator/data-integrator), ko var izmantot datu integrācijai uz/no Common Data Service. Datu integrētāju var izmantot, lai definētu integrācijas projektus (bieži, pamatojoties uz iepriekš noteiktām veidnēm, ko programmas izstrādātāji ir pielāgojuši noteiktām integrācijām). Integrācijas projekti var tikt plānoti automātiskai izpildei periodiskā grafikā vai izpildīti manuāli.

Datu integrētāja projekti ir piemēroti Common Data Service paketes integrācijām, un ir lieliska izvēle integrācijai starp Dynamics 365 programmu saimi. Piemēram, Microsoft nodrošina gatavu datu integrētāja veidni, ko var izmantot datu integrācijai no Human Resources uz Dynamics 365 Finance. Papildinformāciju skatiet [Integrācija no Dynamics 365 Human Resources uz Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Datu integrētājs atbalsta arī [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (izmantojot tā [Advanced Query līdzekli](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power Query nodrošina jaudīgu, elastīgu datu filtrēšanu un pārveidošanu, ieskaitot bagātinātu M formulas valodu, un, visticamāk, būs pazīstams tiem, kam pieredze Power BI pārskatu izstrādē.

## <a name="deciding-on-an-integration-technology"></a>Lemšana par integrācijas tehnoloģiju

Kad pieejamas tik daudzas integrācijas tehnoloģijas, dažreiz var būt sarežģīti pieņemt lēmumu par to, kādu integrācijas pieeju izmantot. Laika gaitā, un it īpaši pieaugot datu segumam Common Data Service, lēmums kļūs vieglāks, jo Common Data Service vairumā gadījumu būs izvēlētais datu interfeiss. Bet līdz tam laikam varat nākt pie atziņas, ka Common Data Service vēl neatbilst jūsu vajadzībām. Zemāk redzamā tabula palīdz apkopot atsevišķus dažādu integrācijas tehnoloģiju opciju raksturlielumus.

| Tehnoloģija/Rīks/API    | Atkārtotas integrācijas                   | Sinhrons/asinhrons                    | Programmatiska piekļuve, izmantojot API        | Atbilstoši datu apjomi                                   | Datu segums                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service elementi           | Jā, izmantojot datu integrētāju vai starpprogrammatūru | Sinhrons, asinhrons, pakete (izmantojot datu integrētāju) | Jā, izmantojot Dynamics 365 tīmekļa API (OData) | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Uzlabojas<sup>2</sup>                       |
| DMF elementi           | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā, izmantojot DMF pakotnes REST API         | Augsts (simtiem tūkstošu ierakstu)                    | Augsta                                |
| DMF pakotnes REST API   | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā                                       | Augsts (simtiem tūkstošu ierakstu)                    | API atbalsta visus DMF elementus       |
| BYOD                   | Jā, ieplāno Human Resources administrators        | Asinhrons, pakete                                | Nē<sup>3</sup>                                    | Augsts (simtiem tūkstošu ierakstu)                    | Atbalsta visus DMF elementus           |
| OData iespējotie elementi | Jā, izmantojot starpprogrammatūru                    | Sinhronizēt                                        | Jā, izmantojot Human Resources datu pakalpojumu (OData)  | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Augsta                                |
| Excel pievienojumprogramma           | Nē                                       | Sinhronizēt                                        | Nē                                        | Vidējs (desmitiem tūkstošu ierakstu)                      | Atbalsta visus OData iespējotos elementus |
| Datu integrētājs        | Jā, ieplānots datu integrētājā        | Asinhrons, pakete                                | Nē                                        | Mainās atkarībā no izmantošanas gadījuma                                       | Atbalsta visus Common Data Service elementus           |

<sup>2</sup>Microsoft veic lielus ieguldījumus, palielinot datu segumu Common Data Service elementiem, un iesaka Common Data Service kā izvēlēto datu interfeisu, kad pieejams segums. Pašlaik Common Data Service datu segums ir zems salīdzinājumā ar DMF un OData iespējotiem elementiem.

<sup>3</sup>SQL datu bāzei var piekļūt programmiski.

## <a name="summary"></a>Kopsavilkums

Jūsu biznesa dati ir vērtīgs līdzeklis, bet to vērtība var ievērojami samazināties, ja datus ir grūti izmantot konkrētajiem mērķiem (piemēram, ziņošana, datu jaucējprogrammas vai pielāgotas programmas). Dynamics 365 Human Resources nodrošina vairākas tehnoloģijas darbam ar datiem ārpus Human Resources programmas lietotāja interfeisa (UI), ļaujot integrācijas programmām piekļūt datiem. Šajā tēmā ir aprakstītas pieejamās integrācijas tehnoloģijas un daži to galvenie raksturlielumi. Šai informācijai ir jāpalīdz pieņemt labākus lēmumus par to, kuras pieejas gūs labumu jūsu integrācijas projektiem.

