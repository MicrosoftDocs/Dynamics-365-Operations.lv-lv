---
title: Datu integrācijas tehnoloģiju izvēle
description: Šajā tēmā sniegta informācija par integrēšanu ar personāla vadības pārvaldītajiem datiem.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 98c1c56b445ae426103d19f96cbf1a77891221ef
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717144"
---
# <a name="choose-a-data-integration-technology"></a>Datu integrācijas tehnoloģiju izvēle


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šajā tēmā sniegta informācija par integrēšanu ar datiem, ko pārvalda Dynamics 365 cilvēkresursi. Tas apraksta dažādas integrēšanas tehnoloģijas, lai palīdzētu jums izlemt, kuras tehnoloģijas vislabāk atbilst jūsu vajadzībām.

## <a name="data-integration-background"></a>Datu integrācijas fons

Biznesa dati ir galvenie līdzekļi, kas padara uzņēmumu unikālu. Biznesa dati ir ļoti vērtīgi. Lai uzlabotu biznesa procesus un biznesa informāciju visā uzņēmumā, varat izmantot attiecības starp datiem, kas apkopoti jūsu uzņēmumā. Mēs cenšamies nodrošināt vieglu, drošu un stabilu piekļuvi jūsu biznesa datiem neatkarīgi no sistēmas, no kā tie tiek iegūti.

Vēsturiski datu integrācija starp vairākām sistēmām ir bijusi sarežģīta. Microsoft veic darbības, lai atvieglotu datu integrāciju, un liels solis pretī šim mērķim tiek realizēts, izmantojot [Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Personāla vadība dod priekšroku Dataverse kā Personāla vadības datu publiskajam interfeisam. Laika gaitā mēs sagaidām, ka visi svarīgākie dati, ko pārvalda Human Resources, tiks sniegti Dataverse. Mēs iesakām Dataverse kā izvēles tehnoloģiju lielākajai daļai integrācijas pieteikumu.

Mēs saprotam, ka Dataverse vēl nav ietverti visi dati, kuri jūsu programmai ir nepieciešami. Mēs arī saprotam jūsu projekta grafikam, iespējams, būs nepieciešama alternatīva tehnoloģija. Noteikti dariet mums zināmu, kad Dataverse neatbilst jūsu integrācijas vajadzībām.

## <a name="integration-technologies"></a>Integrācijas tehnoloģijas

Turpmākajās sadaļās aprakstītas dažādas datu integrācijas tehnoloģijas, kas pieejamas lietošanai Human Resources.

### <a name="dataverse-tables"></a>Dataverse tabulas

Dataverse ir izvēlētais publisko datu interfeiss Human Resources. Tas ir attīstījies no Dynamics 365 XRM platformas, ko izmanto [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps) risinājumi.

Dataverse nodrošina platformu un API datu tabulām. Kad tiek izvietota Personāla vadība, tie tiek savienoti ar Dataverse instanci. Personāla vadības datu entītijas tiek izvietotas šajā Dataverse instancē. Tabulas un to dati ir pieejami jebkurai programmai, kas var pieslēgties Dataverse instancei. Human Resources sinhronizē datus uz un no Dataverse tabulām.

> [!NOTE]
> Human Resources elementi atbilst Dataverse tabulām. Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Ja datu tabulas, ko pieprasa jūsu integrēšanas programmas, ir Dataverse, jūs varat pilnībā izmantot [Dataverse un API, ko tā atbalsta](/powerapps/?panel=developer#pivot=home). Starp atbalstītajiem API ir [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kas nodrošina OData ieviešanu, lai piekļūtu Dataverse.

Dataverse tabulas un to saistītie API ir vislabākā opcija, lai piekļūtu Personāla vadības datiem, izmantojot tīmekļa programmas, tīmekļa pakalpojumus/API un no jebkuru citu programmu, kas pieslēdzas OData plūsmām.

> [!NOTE]
> Tā kā lēmums padarīt Dataverse par izvēlēto datu interfeisu Personāla vadībai ir salīdzinoši nesens, varat nākt pie atziņas, ka Personāla vadības datu elementi, kas nepieciešami integrācijai, vēl nav pieejami Dataverse.
> </br>
> Sarakstu ar Personāla vadības elementiem, kas pieejami Dataverse, skatiet [Personāla vadība un Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Ja jūsu integrācijai nepieciešamie Personāla vadības elementi vēl nav pieejami, jums būs vai nu jāgaida, kamēr datu elementi tika padarīti pieejami, vai arī būs jāizmanto kāda no tālāk aprakstītajām integrācijas tehnoloģijām.
> </br>
> Pēc noklusējuma Dataverse  integrācija ir izslēgta jaunās vidēs, kurās nav ietverti nodrošinātie demonstrācijas dati. Tā ir ieslēgta jaunās vidēs, kas ietver demonstrācijas datus, un vide sāk sinhronizēt datus, kad tie tiek nodrošināti. Pēc tam, kad jūsu vide ir gatava sinhronizēt datus, varat ieslēgt integrāciju.

### <a name="dmfdixf-entities"></a>DMF/DIXF elementi

Cilvēkresursi, galvenokārt uz tās pašas platformas, kurā atrodas finanšu un operāciju programmas, nodrošina datu [pārvaldības struktūru (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF ir zināms arī kā Datu importēšanas un eksportēšanas struktūra (DIXF). Personāla vadība nodrošina datu elementu kopu, ko varat izmantot, lai importētu un eksportētu Personāla vadības datus. Lai gan Dataverse tabulas ir Personāla vadības izvēlētais datu integrācijas interfeiss, DMF elementi joprojām ir noderīgi dažos tālāk minētajos gadījumos:

- Dataverse tabulas vēl nav pieejamas.

- Integrācijai ir nepieciešamas augstas veiktspējas lielapjoma datu importēšanas/eksportēšanas iespējas.

> [!NOTE]
> Human Resources elementi atbilst Dataverse tabulām. Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

DMF elementi pašlaik sniedz vispilnīgāko Human Resources datu segumu.

DMF nav piemērots reāllaika integrācijām, piemēram, kad ir nepieciešama tūlītēja lietotāja atsauksme lietotāja interfeisā. Pakešu operācijas ir plānotie pakešuzdevumi, un tām bieži ir vismaz 1-2 minūšu latentums, pirms pakešpakalpojums paņem darbu izpildei, kā arī laiks, kas nepieciešams importa/eksporta operācijas pabeigšanai.

DMF var būt vislabākā izvēle, ja ir nepieciešama liela caurlaides spēja (piemēram, naktī ieplānota daudzu tūkstošu ierakstu importēšana/eksportēšana).

> [!NOTE]
> DMF nav pieejams Attract un Onboard.

### <a name="dmf-package-rest-api"></a>DMF pakotnes REST API

DMF nodrošina [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) manipulēšanai ar datu pakotnēm. Šo API var izmantot, lai programmiski mijiedarbotos ar DMF, atļaujot, piemēram, tādas darbības, kas minētas tālāk.

- Datu pakotnes importēšana.

- Datu pakotnes eksportēšana.

- Importēšanas/eksportēšanas operācijas statusa pārbaude.

DMF pakotne REST API tiek pilnībā atbalstīta Human Resources.

### <a name="azure-sql-db-byod"></a>Azure SQL datu bāze (BYOD)

DMF papildus sniedz jaudīgu līdzekli (zināms kā [Atnes savu datu bāzi](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) vai BYOD (Bring Your Own Database)), kas ļauj Personāla vadībai eksportēt datus uz savu Microsoft Azure SQL datu bāzi. Šī iespēja sniedz milzīgu elastību. Kad dati ir iekļauti jūsu SQL datu bāzē, varat izmantot jebkuru programmu vai starpprogrammatūru, kas var pieslēgties SQL datu glabātuvei.

BYOD galvenokārt ir tikai lasāms risinājums. Lai gan varat Azure SQL datu bāzē manipulēt un glabāt jebkurus datus (piemēram, datu jaucējprogrammas), Azure SQL datu bāzē glabātie dati nav sinhronizēti ar Personāla vadību.

BYOD ir piemērots pārskatu risinājumiem, datu integrācijām, datu jaucējprogrammām un kā datu avots [Azure Data Factory](/azure/data-factory/) konveijeram.

> [!NOTE]
> BYOD nav pieejams Attract un Onboard.

### <a name="odata-enabled-entities"></a>OData iespējotie elementi

Lielākā daļa DMF elementu ir iespējoti arī piekļuvei, izmantojot Human Resources datu pakalpojumu (OData). Dokumentācija, kas sniegta Finanšu [un operāciju OData](/dynamics365/unified-operations/dev-itpro/data-entities/odata) pakalpojumam, attiecas uz cilvēkresursiem, izņemot pašu OData atklāto entītiju izveidi.

Lai gan Dataverse un OData implementācijai, ko sniedz Dataverse (izmantojot [Dynamics 365 Web API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), tiek dota priekšroka pret Human Resources datu pakalpojumu, Human Resources datu pakalpojumam pašlaik ir pilnīgāks elementu segums Human Resources datiem.

### <a name="excel-add-in"></a>Excel pievienojumprogramma

[Excel pievienojumprogramma](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) padara OData iespējoto elementu izmantošanu ārpus acīmredzamā. Tas nodrošina ērtu veidu, kā lietotājam iegūt un modificēt Human Resources datus, izmantojot pazīstamo Excel lietotāja interfeisu.

Excel pievienojumprogramma ir piemērota speciālai datu importēšanai/eksportēšanai, ko veic biznesa domēna eksperti. Lai veiktu periodisku datu integrāciju, kam nepieciešama programmatiska automatizācija, piemērotāka būs cita integrācijas tehnoloģija.

### <a name="data-integrator"></a>Datu integrētājs

Jūs varat izmantot [Datu integratora pakalpojumu](/powerapps/administrator/data-integrator), lai integrētu datus uz un no Dataverse. Datu integrētāju ļauj jums definēt integrācijas projektus, bieži pamatojoties uz iepriekš noteiktām veidnēm, ko programmas izstrādātāji ir pielāgojuši noteiktām integrācijām. Jūs varat ieplānot integrācijas projektu palaišanu automātiskai izpildei periodiskā grafikā vai to palaišanai manuāli.

Datu integratora projekti ir piemēroti Dataverse partijas integrācijai. Tā ir lieliska izvēle integrācijai starp Dynamics 365 saimes programmām. Piemēram, Microsoft nodrošina datu integrētāāja veidni datu integrēšanai dynamics 365 finansēs no personāla vadības. Par veidni Integrācija no Dynamics [Dynamics 365 Human Resources 365 finansēm varat uzzināt vairāk](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Datu integrētājs atbalsta paplašinātā [Power Query](/power-query/power-query-what-is-power-query) vaicājuma [līdzekli](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query nodrošina jaudīgu, elastīgu datu filtrēšanu un pārvēršanu, ietverot bagātinātās M formulas valodu. Power Query iespējams, būs zināms, ja būsiet izstrādājis Power BI pārskatus.

## <a name="deciding-on-an-integration-technology"></a>Lemšana par integrācijas tehnoloģiju

Kad pieejamas tik daudzas integrācijas tehnoloģijas, dažreiz var būt sarežģīti pieņemt lēmumu par to, kādu integrācijas pieeju izmantot. Pieaugot datu segumam Dataverse, lēmums kļūs vieglāks, jo Dataverse vairumā gadījumu būs izvēlētais datu interfeiss. Bet līdz tam laikam varat nākt pie atziņas, ka Dataverse vēl neatbilst jūsu vajadzībām. Zemāk redzamā tabula apkopo atsevišķus integrācijas tehnoloģiju opciju raksturlielumus.

| Tehnoloģija/Rīks/API    | Atkārtotas integrācijas                   | Sinhrons/asinhrons                    | Programmatiska piekļuve, izmantojot API        | Atbilstoši datu apjomi                                   | Datu segums                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse tabulas           | Jā, izmantojot datu integrētāju vai starpprogrammatūru | Sinhrons, asinhrons, pakete (izmantojot datu integrētāju) | Jā, izmantojot Dynamics 365 tīmekļa API (OData) | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Uzlabojas<sup>2</sup>                       |
| DMF elementi           | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā, izmantojot DMF pakotnes REST API         | Augsts (simtiem tūkstošu ierakstu)                    | Augsta                                |
| DMF pakotnes REST API   | Jā, ieplānots, izmantojot starpprogrammatūru        | Asinhrons, pakete                                | Jā                                       | Augsts (simtiem tūkstošu ierakstu)                    | API atbalsta visus DMF elementus       |
| BYOD                   | Jā, ieplāno Human Resources administrators        | Asinhrons, pakete                                | Nē<sup>3</sup>                                    | Augsts (simtiem tūkstošu ierakstu)                    | Atbalsta visus DMF elementus           |
| OData iespējotie elementi | Jā, izmantojot starpprogrammatūru                    | Sinhronizēt                                        | Jā, izmantojot Human Resources datu pakalpojumu (OData)  | Mainās atkarībā no izmantošanas gadījuma (atbalsta lapošana interaktīvai lietošanai) | Augsta                                |
| Excel pievienojumprogramma           | Nē                                       | Sinhronizēt                                        | Nē                                        | Vidējs (desmitiem tūkstošu ierakstu)                      | Atbalsta visus OData iespējotos elementus |
| Datu integrētājs        | Jā, ieplānots datu integrētājā        | Asinhrons, pakete                                | Nē                                        | Mainās atkarībā no izmantošanas gadījuma                                       | Atbalsta visas Dataverse tabulas           |

<sup>2</sup>Microsoft veic lielus ieguldījumus, palielinot datu pārklājumu Dataverse tabulām. Mēs iesakām izmantot Dataverse, kad pārklājums ir pieejams. Pašlaik Dataverse datu segums ir zems salīdzinājumā ar DMF un OData iespējotiem elementiem.

<sup>3</sup>SQL datu bāzei var piekļūt programmiski.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
