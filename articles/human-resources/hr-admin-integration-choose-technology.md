---
title: Izvēlēties datu integrācijas tehnoloģiju
description: Šis raksts sniedz informāciju par datu integrēšanu, kurus pārvalda Personāla vadība. Tas apraksta dažādas integrēšanas tehnoloģijas, lai palīdzētu jums izlemt, kuras tehnoloģijas vislabāk atbilst jūsu vajadzībām.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
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
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528345"
---
# <a name="choose-a-data-integration-technology"></a>Izvēlēties datu integrācijas tehnoloģiju

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šis raksts sniedz informāciju datu integrēšanai, kurus pārvalda Dynamics 365 Human Resources. Tas apraksta dažādas integrēšanas tehnoloģijas, lai palīdzētu jums izlemt, kuras tehnoloģijas vislabāk atbilst jūsu vajadzībām.

## <a name="data-integration-background"></a>Datu integrācijas fons

Biznesa dati ir galvenie līdzekļi, kas padara uzņēmumu unikālu. Biznesa dati ir ļoti vērtīgi. Lai uzlabotu biznesa procesus un biznesa informāciju visā uzņēmumā, varat izmantot attiecības starp datiem, kas apkopoti jūsu uzņēmumā. Mēs cenšamies nodrošināt vieglu, drošu un stabilu piekļuvi jūsu biznesa datiem neatkarīgi no sistēmas, no kā tie tiek iegūti.

Vēsturiski datu integrācija starp vairākām sistēmām ir bijusi sarežģīta.
Microsoft veic darbības, lai atvieglotu datu integrāciju, un liels solis pretī šim mērķim tiek realizēts, izmantojot [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Personāla vadība dod priekšroku Common Data Service kā Personāla vadības datu publiskajam interfeisam. Laika gaitā mēs sagaidām, ka visi svarīgākie dati, ko pārvalda Human Resources, tiks sniegti Common Data Service. Mēs iesakām Common Data Service kā izvēles tehnoloģiju lielākajai daļai integrācijas pieteikumu.

Mēs saprotam, ka Common Data Service vēl nav ietverti visi dati, kuri jūsu programmai ir nepieciešami. Mēs arī saprotam jūsu projekta grafikam, iespējams, būs nepieciešama alternatīva tehnoloģija. Noteikti dariet mums zināmu, kad Common Data Service neatbilst jūsu integrācijas vajadzībām.

## <a name="integration-technologies"></a>Integrācijas tehnoloģijas

Turpmākajās sadaļās aprakstītas dažādas datu integrācijas tehnoloģijas, kas pieejamas lietošanai Human Resources.

### <a name="common-data-service-entities"></a>Common Data Service elementi

Common Data Service ir izvēlētais publisko datu interfeiss Human Resources. Tas attīstījās no Dynamics 365 XRM platformas, ko izmanto [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) risinājumi.

Common Data Service nodrošina platformu un API datu entītijām. Kad tiek izvietota Personāla vadība, tie tiek savienoti ar Common Data Service instanci. Personāla vadības datu entītijas tiek izvietotas šajā Common Data Service instancē. Entītijas un to dati ir pieejami jebkurai programmai, kas var pieslēgties Common Data Service instancei. Personāla vadība sinhronizē datus uz un no Common Data Service entītijām.

Ja datu entītijas, ko pieprasa jūsu integrēšanas programmas, ir Common Data Service, jūs varat pilnībā izmantot [Common Data Service un API, ko tā atbalsta](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Starp atbalstītajiem API ir [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kas nodrošina OData ieviešanu, lai piekļūtu Common Data Service.

Common Data Service elementi un to saistītie API ir vislabākā opcija, lai piekļūtu Personāla vadības datiem, izmantojot tīmekļa programmas, tīmekļa pakalpojumus/API un no jebkuru citu programmu, kas pieslēdzas OData plūsmām.

> [!NOTE]
> Tā kā lēmums padarīt Common Data Service par izvēlēto datu interfeisu Personāla vadībai ir salīdzinoši nesens, varat nākt pie atziņas, ka Personāla vadības datu elementi, kas nepieciešami integrācijai, vēl nav pieejami Common Data Service.
</br>
> Sarakstu ar Personāla vadības elementiem, kas pieejami Common Data Service, skatiet [Personāla vadība un Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Ja jūsu integrācijai nepieciešamie Personāla vadības elementi vēl nav pieejami, jums būs vai nu jāgaida, kamēr datu elementi tika padarīti pieejami, vai arī būs jāizmanto kāda no tālāk aprakstītajām integrācijas tehnoloģijām.
> </br>
> Pēc noklusējuma Common Data Service integrācija ir izslēgta jaunās vidēs, kurās nav ietverti nodrošinātie demonstrācijas dati. Tā ir ieslēgta jaunās vidēs, kas ietver demonstrācijas datus, un vide sāk sinhronizēt datus, kad tie tiek nodrošināti. Pēc tam, kad jūsu vide ir gatava sinhronizēt datus, varat ieslēgt integrāciju.

### <a name="dmfdixf-entities"></a>DMF/DIXF elementi

Personāla vadība, kas galvenokārt tiek veidota uz tās pašas platformas kā Finance and Operations programmas, sniedz [Datu pārvaldības struktūru (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). DMF ir zināms arī kā Datu importēšanas un eksportēšanas struktūra (DIXF). Personāla vadība nodrošina datu elementu kopu, ko varat izmantot, lai importētu un eksportētu Personāla vadības datus. Lai gan Common Data Service elementi ir Personāla vadības izvēlētais datu integrācijas interfeiss, DMF elementi joprojām ir noderīgi dažos tālāk minētajos gadījumos:

- Common Data Service elementi vēl nav pieejami.

- Integrācijai ir nepieciešamas augstas veiktspējas lielapjoma datu importēšanas/eksportēšanas iespējas.

DMF elementi pašlaik sniedz vispilnīgāko Human Resources datu segumu.

DMF nav piemērots reāllaika integrācijām, piemēram, kad ir nepieciešama tūlītēja lietotāja atsauksme lietotāja interfeisā. Pakešu operācijas ir plānotie pakešuzdevumi, un tām bieži ir vismaz 1-2 minūšu latentums, pirms pakešpakalpojums paņem darbu izpildei, kā arī laiks, kas nepieciešams importa/eksporta operācijas pabeigšanai.

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

DMF papildus sniedz jaudīgu līdzekli (zināms kā [Atnes savu datu bāzi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) vai BYOD (Bring Your Own Database)), kas ļauj Personāla vadībai eksportēt datus uz savu Microsoft Azure SQL datu bāzi. Šī iespēja sniedz milzīgu elastību. Kad dati ir iekļauti jūsu SQL datu bāzē, varat izmantot jebkuru programmu vai starpprogrammatūru, kas var pieslēgties SQL datu glabātuvei.

BYOD galvenokārt ir tikai lasāms risinājums. Lai gan varat Azure SQL datu bāzē manipulēt un glabāt jebkurus datus (piemēram, datu jaucējprogrammas), Azure SQL datu bāzē glabātie dati nav sinhronizēti ar Personāla vadību.

BYOD ir piemērots pārskatu risinājumiem, datu integrācijām, datu jaucējprogrammām un kā datu avots [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) konveijeram.

> [!NOTE]
> BYOD nav pieejams Attract un Onboard.

### <a name="odata-enabled-entities"></a>OData iespējotie elementi

Lielākā daļa DMF elementu ir iespējoti arī piekļuvei, izmantojot Human Resources datu pakalpojumu (OData). [Finance and Operations OData pakalpojumam](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) paredzētais dokuments attiecas uz Personāla vadību, izņemot, lai izveidotu savus OData elementus.

Lai gan Common Data Service un OData implementācijai, ko sniedz Common Data Service (izmantojot [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), tiek dota priekšroka pret Human Resources datu pakalpojumu, Human Resources datu pakalpojumam pašlaik ir pilnīgāks elementu segums Human Resources datiem.

### <a name="excel-add-in"></a>Excel pievienojumprogramma

[Excel pievienojumprogramma](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) padara OData iespējoto elementu izmantošanu ārpus acīmredzamā. Tas nodrošina ērtu veidu, kā lietotājam iegūt un modificēt Human Resources datus, izmantojot pazīstamo Excel lietotāja interfeisu.

Excel pievienojumprogramma ir piemērota speciālai datu importēšanai/eksportēšanai, ko veic biznesa domēna eksperti. Lai veiktu periodisku datu integrāciju, kam nepieciešama programmatiska automatizācija, piemērotāka būs cita integrācijas tehnoloģija.

### <a name="data-integrator"></a>Datu integrētājs

Jūs varat izmantot [Datu integratora pakalpojumu](https://docs.microsoft.com/powerapps/administrator/data-integrator), lai integrētu datus uz un no Common Data Service. Datu integrētāju ļauj jums definēt integrācijas projektus, bieži pamatojoties uz iepriekš noteiktām veidnēm, ko programmas izstrādātāji ir pielāgojuši noteiktām integrācijām. Jūs varat ieplānot integrācijas projektu palaišanu automātiskai izpildei periodiskā grafikā vai to palaišanai manuāli.

Datu integratora projekti ir piemēroti Common Data Service partijas integrācijai. Tā ir lieliska izvēle integrācijai starp Dynamics 365 saimes programmām. Piemēram, Microsoft nodrošina Datu integrētāja veidni, ko var izmantot datu integrācijai no Personāla vadības uz Dynamics 365 Finance. Jūs varat uzzināt vairāk par veidni sadaļā [Integrācija no Dynamics 365 Human Resources uz Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Datu integrētājs atbalsta [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query), izmantojot tā [Advanced Query līdzekli](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query nodrošina spēcīgu, elastīgu datu filtrēšanu un pārveidošanu, ieskaitot bagātinātu M formulas valodu. Power Query, visticamāk, būs zināms, ja esat izstrādājis Power BI pārskatus.

## <a name="deciding-on-an-integration-technology"></a>Lemšana par integrācijas tehnoloģiju

Kad pieejamas tik daudzas integrācijas tehnoloģijas, dažreiz var būt sarežģīti pieņemt lēmumu par to, kādu integrācijas pieeju izmantot. Pieaugot datu segumam Common Data Service, lēmums kļūs vieglāks, jo Common Data Service vairumā gadījumu būs izvēlētais datu interfeiss. Bet līdz tam laikam varat nākt pie atziņas, ka Common Data Service vēl neatbilst jūsu vajadzībām. Zemāk redzamā tabula apkopo atsevišķus integrācijas tehnoloģiju opciju raksturlielumus.

| Tehnoloģija/Rīks/API    | Atkārtotas integrācijas                   | Sinhrons/asinhrons                    | Programmatiska piekļuve, izmantojot API        | Atbilstoši datu apjomi                                   | Datu segums                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service elementi           | Jā, izmantojot datu integrētāju vai starpprogrammatūru | Sinhrons, asinhrons, pakete (izmantojot datu integrētāju) | Jā, izmantojot Dynamics 365 tīmekļa API (OData) | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Uzlabojas<sup>2</sup>                       |
| DMF elementi           | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā, izmantojot DMF pakotnes REST API         | Augsts (simtiem tūkstošu ierakstu)                    | Augsta                                |
| DMF pakotnes REST API   | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā                                       | Augsts (simtiem tūkstošu ierakstu)                    | API atbalsta visus DMF elementus       |
| BYOD                   | Jā, ieplāno Human Resources administrators        | Asinhrons, pakete                                | Nē<sup>3</sup>                                    | Augsts (simtiem tūkstošu ierakstu)                    | Atbalsta visus DMF elementus           |
| OData iespējotie elementi | Jā, izmantojot starpprogrammatūru                    | Sinhronizēt                                        | Jā, izmantojot Human Resources datu pakalpojumu (OData)  | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Augsta                                |
| Excel pievienojumprogramma           | Nē                                       | Sinhronizēt                                        | Nē                                        | Vidējs (desmitiem tūkstošu ierakstu)                      | Atbalsta visus OData iespējotos elementus |
| Datu integrētājs        | Jā, ieplānots datu integrētājā        | Asinhrons, pakete                                | Nē                                        | Mainās atkarībā no izmantošanas gadījuma                                       | Atbalsta visus Common Data Service elementus           |

<sup>2</sup> Microsoft veic lielus ieguldījumus, palielinot datu pārklājumu Common Data Service vienībām. Mēs iesakām izmantot Common Data Service, kad pārklājums ir pieejams. Pašlaik Common Data Service datu segums ir zems salīdzinājumā ar DMF un OData iespējotiem elementiem.

<sup>3</sup>SQL datu bāzei var piekļūt programmiski.


[!INCLUDE[footer-include](../includes/footer-banner.md)]