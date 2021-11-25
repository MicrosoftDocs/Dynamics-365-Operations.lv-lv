---
title: Vienotā preču pieredze
description: Šajā tēmā ir aprakstīta preču datu integrācija starp programmām Finance and Operations un Dataverse
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 81f49cf08dcd1b4b1c3d71ff286a1f070e65e914
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782336"
---
# <a name="unified-product-experience"></a>Vienotā preču pieredze

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ja biznesa ekosistēma ir izveidota no Dynamics 365 lietojumprogrammām, piemēram, Finance, Supply Chain Management un Sales, uzņēmumi bieži lieto šīs programmas, lai iegūtu preču datus. Tas ir tāpēc, ka šīs programmas nodrošina stabilu preču infrastruktūru, kas papildināta ar sarežģītākām cenu noteikšanas koncepcijām un precīziem rīcībā esošajiem krājumu datiem. Uzņēmumi, kuri izmanto ārējo Product Lifecycle Management (PLM) sistēmu, lai iegūtu produktu datus, var novirzīt produktus no Finance and Operations programmām uz citām Dynamics 365 programmām. Vienotā preču pieredze nodrošina integrētu preču datu modeli Dataverse , lai visi programmas lietotāji, ieskaitot Power Platform lietotājus, var izmantot bagātīgo preču datu priekšrocības, ko sniedz Finance and Operations programmas.

Lūk, preču datu modelis no Sales.

![Preču datu modelis CE.](media/dual-write-product-4.jpg)

Šeit it preču datu modelis no Finance and Operations programmām.

![Preču datu modelis pakalpojumā Finance and Operations.](media/dual-write-products-5.jpg)

Šie divi preču datu modeļi ir integrēti Dataverse, kā parādīts zemāk.

![Preču datu modelis Dynamics 365 lietojumprogrammās.](media/dual-write-products-6.jpg)

Duālā ieraksta tabulas kartes precēm ir izveidotas, lai virzītu datus tikai vienā virzienā tuvu reāllaikam no Finance and Operations programmām uz Dataverse. Tomēr, ja nepieciešams, preču infrastruktūra ir atvērta, lai to izveidotu kā divvirzienu. Kaut arī varat to pielāgot, jums pašiem jāuzņemas atbildība, jo korporācija Microsoft šo pieeju neiesaka.

## <a name="templates"></a>Veidnes

Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas. Kā redzams šajā tabulā, tiek izveidota tabulas karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.

Finance and Operations programmas | Citas Dynamics 365 programmas | Apraksts
-----------------------|--------------------------------|---
[Visas preces](mapping-reference.md#138) | msdyn_globalproducts | Visu preču tabula satur visas preces, kas pieejamas Finance and Operations lietojumprogrammās: gan izlaistas, gan neizlaistas preces.
[CDS izlaistās atšķirīgās preces](mapping-reference.md#213) | Produkts | **Preces** tabula satur kolonnas, kas definē preci. Tā ietver atsevišķas preces (preces ar apakštipa preci) un preces variantus. Tālāk esošajā tabulā parādīta kartēšana.
[Krāsas](mapping-reference.md#170) | msdyn\_ productcolors
[Konfigurācijas](mapping-reference.md#171) | msdyn\_ productconfigurations
[Pasūtījuma noklusējuma iestatījumi](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Preces kategorijas](mapping-reference.md#166) | msdyn_productcategories | Katra no preču kategorijām un informācija par tās struktūru un raksturlielumiem ir ietverta preču kategorijas tabulā.
[Preču kategoriju piešķires](mapping-reference.md#167) | msdyn_productcategoryassignments | Lai piešķirtu preci kategorijai, var izmantot preču kategorijas piešķires tabulu.
[Preču kategoriju hierarhijas](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Varat izmantot preču hierarhijas, lai dalītu preces kategorijās vai grupās. Kategoriju hierarhijas ir pieejamas pakalpojumā Dataverse, izmantojot preču kategoriju hierarhijas tabulu.
[Preču kategoriju hierarhijas lomas](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Preču hierarhijas var izmantot atšķirīgām lomām D365 Finance and Operations. Tās norāda, kura kategorija tiek izmantota katrai lomai, kurā preču kategorijas lomā tabula tiek izmantota.
[Preču noklusējuma pasūtījuma iestatījumi V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Preces dimensiju grupas](mapping-reference.md#173) | msdyn\_ productdimensiongroups | Preču dimensiju grupa definē, kuras preces dimensijas definē preci.
[Preces šablona krāsas](mapping-reference.md#187) | msdyn_sharedproductcolors | **Koplietojamās preces krāsas** tabula norāda krāsas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Dataverse, lai saglabātu datus saskaņotus.
[Preces šablona konfigurācijas](mapping-reference.md#188) | msdyn_sharedproductconfigurations | **Koplietojamo preču konfigurācijas** tabula norāda konfigurācijas, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Dataverse, lai saglabātu datus saskaņotus.
[Preces šablona izmēri](mapping-reference.md#190) | msdyn_sharedproductsizes | Tabula **Koplietojamās preces izmērs** norāda izmērus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Dataverse, lai saglabātu datus saskaņotus.
[Preces šablona stili](mapping-reference.md#191) | msdyn_sharedproductstyles | **Koplietojamās preces stila** tabula norāda stilus, kas var būt konkrētam preces šablonam. Šis jēdziens tiek migrēts uz Dataverse, lai saglabātu datus saskaņotus.
[Produkta numura identifikācijas svītrkods](mapping-reference.md#164) | msdyn\_ productbarcodes | Preču svītrkodi tiek izmantoti, lai unikāli identificētu preces.
[Precei specifisku mērvienību pārveidošana](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Izlaistās preces V2](mapping-reference.md#189) | msdyn\_ sharedproductdetails | **msdyn\_ sharedproductdetails** tabula satur kolonnas no Finance and Operations lietojumprogrammām, kas nosaka preci un kurās ir ietverta preces finanšu un pārvaldības informācija.
[Izmēri](mapping-reference.md#174) | msdyn\_ productsizes
[Noliktavas dimensiju grupas](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Produktu noliktavas dimensiju grupa atbilst metodei, kas tiek izmantota, lai definētu preces novietojumu noliktavā.
[Stili](mapping-reference.md#178) | msdyn\_ productsytles
[Izsekošanas dimensiju grupas](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Preču izsekošanas dimensiju grupa parāda metodi, kas tiek izmantota, lai izsekotu preci krājumos.
[Vienības](mapping-reference.md#219) | uoms
[Mērvienību pārveidošana](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Preču integrēšana

Šajā modelī preci attēlo divu Dataverse tabulu kombinācija: **preces** un **msdyn\_ sharedproductdetails**. Tā kā pirmā tabula satur preces definīciju (preces unikālais identifikators, preces nosaukums un apraksts), otrā tabula ietver kolonnas, kas tiek glabātas preču līmenī. Šo divu tabulu kombinācija tiek izmantota, lai definētu preci atbilstoši krājumu uzskaites vienības (SKU) koncepcijai. Katrai izlaistajai precei būs sava informācija minētajās tabulās (Prece un Koplietojamā informācija par preci). Lai izsekotu visām precēm (izlaistām un neizlaistām), tiek izmantota tabula **Globālās preces**.

Tā kā produkts tiek attēlots kā SKU, atšķirīgu preču, preču šablonu un preču variantu koncepcijas var uztvert Dataverse šādi:

- **Preces ar apakštipa preci** ir preces, kas definētas pašas. Dimensijas nav jādefinē. Piemērs ir noteikta grāmata. Šīm precēm viens ieraksts tiek izveidots **Preces** tabulā, un viens ieraksts tiek izveidots **msdyn\_ sharedproductdetails** tabulā. Nav izveidota neviena preču saimes rinda.
- **Preču šabloni** tiek izmantoti kā ģenēriskas preces, kas satur definīciju un nosacījumus, kas nosaka biznesa procesu darbību. Balstoties uz šīm definīcijām, var tikt ģenerētas atšķirīgas preces, kas zināmas kā preces varianti. Piemēram, T-krekls ir preces šablons, un tam var būt Krāsa un Izmērs dimensiju veidā. Var izlaist variantus, kuriem ir dažādas šo dimensiju kombinācijas, piemēram, mazs zils T-krekls vai vidēji zaļš T-krekls. Integrācijā katram variantam preču tabulā tiek izveidota viena rinda. Šī rinda satur ar variantu saistītu informāciju, piemēram, dažādas dimensijas. Vispārīgā informācija par preci tiek uzglabāta **msdyn\_ sharedproductdetails** tabulā. (Šī ir vispārīga informācija tiek turēta preces pamatinformācijā.) Preces pamatinformācija tiek sinhronizēta Dataverse, tiklīdz tiek izveidots izlaistais preces šablons (bet pirms tiek izlaisti varianti).
- **Atšķirīgas preces** attiecas uz visām produktu apakštipa precēm un visiem preces variantiem.

![Preču datu modelis.](media/dual-write-product.png)

Ar iespējotu duālās rakstīšanas funkcionalitāti Finance and Operations preces tiks sinhronizētas citās Dynamics 365 precēs **Melnraksta** stāvoklī. Tās tiek pievienotas pirmajam cenu sarakstam ar to pašu valūtu, kas tiek izmantota debitoru summu programmā, un cenu saraksta nosaukumā tiek izmantota alfabētiskā kārtošana. Citiem vārdiem, tie ir pievienoti pirmajam cenrādim Dynamics 365 lietojumprogrammā, kas atbilst jūsu juridiskās personas valūtai, kur prece tiek izdota Finance and Operations programmā. Ja dotajā valūtā nav cenu saraksta, automātiski tiks izveidota cenu saraksts un prece tiks tam piešķirta.

Pašreizējā dubulto ierakstu spraudņu ieviešana, kas saista noklusējuma cenu sarakstu ar vienību, uzmeklē ar programmu Finance and Operations saistīto valūtu un atrod pirmo cenu sarakstu programmā Customer Engagement, izmantojot alfabētisko secību cenu saraksta nosaukumiem. Lai iestatītu noklusējuma cenu sarakstu noteiktai valūtai, kad jums ir vairāki cenu saraksti šai valūtai, cenu saraksta nosaukums ir jāatjaunina uz nosaukumu, kas alfabētiskajā secībā ir agrāk nekā jebkurš cits cenu saraksts tai pašai valūtai. Ja tai nav neviena cenu saraksta dotajā valūtā, tiek izveidota jauna.

Pēc noklusējuma preces no Finance and Operations programmām tiek sinhronizētas ar citām Dynamics 365 programmām statusā **Melnraksts**. Lai sinhronizētu preci ar statusu **Aktīvs**, lai varētu to tieši izmantot pārdošanas pasūtījuma piedāvājumos, ir jāizvēlas, piemēram, šāds iestatījums: cilnē **Sistēma > Administrēšana > Sistēmas administrēšana > Sistēmas iestatījumi > Pārdošana** atlasiet opciju **Izveidot preces aktīvā stāvoklī = Jā**.

Kad preces ir sinhronizētas, jāievada lauka **Pārdošanas vienība** vērtība programmā Finance and Operations, jo tas ir obligāts lauks programmā Sales.

Preču saimju veidošana no Dynamics 365 Sales netiek atbalstīta, izmantojot preču dubulto ierakstu sinhronizāciju.

Ņemiet vērā, ka preču sinhronizācija notiek no Finance and Operations programmām uz Dataverse. Tas nozīmē, ka preču elementa lauku vērtības var mainīt pakalpojumā Dataverse, taču, kad sinhronizācija tiks uzsākta (kad preces lauks tiek modificēts programmā Finance and Operations), to vērtības tiks pārrakstītas pakalpojumā Dataverse.

Finance and Operations programmas | Customer engagement programmas |
---|---
[CDS izlaistās atšķirīgās preces](mapping-reference.md#213) | Produkts |
[Izlaistās preces V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Visas preces](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Preces dimensijas

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Četras preces dimensijas (krāsa, lielums, stils un konfigurācija) ir arī kartētas Dataverse, lai definētu preces variantus. Sekojošajā attēlā ir parādītas preces dimensijas krāsas datu modelis. Tas pats modelis ir piemērots izmēriem, stiliem un konfigurācijām.

![Datu modelis preces dimensijām.](media/dual-write-product-two.png)

Finance and Operations programmas | Customer engagement programmas |
---|---
[Krāsas](mapping-reference.md#170) | msdyn\_ productcolors
[Izmēri](mapping-reference.md#174) | msdyn\_ productsizes
[Stili](mapping-reference.md#178) | msdyn\_ productsytles
[Konfigurācijas](mapping-reference.md#171) | msdyn\_ productconfigurations

Ja precei ir dažādas preces dimensijas (piemēram, preces šablona izmērs un krāsa ir tādas pašas kā preces dimensijas), katra atšķirīga prece (t.i., katrs preču variants) tiek definēta kā šo preču dimensiju kombinācija. Piemēram, preču numurs B0001 ir īpaši mazs, melns T krekls, un preces numurs B0002 ir neliels melns T krekls. Šādā gadījumā tiek definētas esošās preču dimensiju kombinācijas. Piemēram, no iepriekšējā piemēra T-krekls var būt īpaši mazs un melns, mazs un melns, vidējs un melns vai liels un melns, bet tas nevar būt īpaši liels un melns. Citiem vārdiem sakot, preču dimensijas, ko var veikt preces šablons, ir norādītas, un variantus var izlaist, pamatojoties uz šīm vērtībām.

Lai sekotu preču dimensijām, ko var veikt preces šablons, katrai preces dimensijai tiek izveidotas un kartētas Dataverse tālāk norādītās tabulas. Papildinformāciju skatiet rakstā, [Preču informācija](../../../../supply-chain/pim/product-information.md).

Finance and Operations programmas | Customer engagement programmas |
---|---
[Preces šablona krāsas](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Preces šablona konfigurācijas](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Preces šablona izmēri](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Preces šablona stili](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Produkta numura identifikācijas svītrkods](mapping-reference.md#164) | msdyn\_ productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Noklusējuma pasūtījuma iestatījumi un preces specifiskie noklusējuma iestatījumi

Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes. Šī informācija ir pieejama Dataverse, izmantojot noklusētos pasūtījuma iestatījumus un preces specifiskos noklusējuma pasūtījuma iestatījumu elementu. Plašāku informāciju par funkcionalitāti varat izlasīt tēmā [Noklusējuma pasūtījuma iestatījumi](../../../../supply-chain/production-control/default-order-settings.md).

Finance and Operations programmas | Customer engagement programmas |
---|---
[Pasūtījuma noklusējuma iestatījumi](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Preču noklusējuma pasūtījuma iestatījumi V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mērvienība un mērvienību pārvēršana

Mērvienības un to atbilstošais pārveidojums ir pieejami Dataverse sekojošajā datu modelī, kas redzams diagrammā.

![Mērvienību datu modelis.](media/dual-write-product-three.png)

Mērvienības koncepcija ir integrēta starp Finance and Operations un citām Dynamics 365 lietojumprogrammām. Katrai mērvienību klasei Finance and Operations lietojumprogrammā tiek izveidota mērvienību grupa Dynamics 365 lietojumprogrammā, kas satur mērvienības, kas pieder pie mērvienību kategorijas. Katrai vienību grupai tiek izveidota arī noklusētā pamatvienība.

Finance and Operations programmas | Customer engagement programmas |
---|---
[Precei specifisku mērvienību pārveidošana](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Vienības](mapping-reference.md#219) | uoms
[Mērvienību pārveidošana](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Sākotnējā atbilstošo datu vienību sinhronizēšana starp programmu Finance and Operations un Dataverse

### <a name="initial-synchronization-of-units"></a>Sākotnējā vienību sinhronizācija

Kad duālais ieraksts ir iespējots, vienības no Finance and Operations programmām tiek sinhronizētas ar citām Dynamics 365 programmām. Vienību grupas, kas tiek sinhronizētas no Finance and Operations programmām pakalpojumā Dataverse, ir atzīmētas ar karodziņu kopu, kas norāda, ka tās ir "Uzturētas ārēji".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Atbilstošās vienības un vienību klases/grupas dati no Finance and Operations un citām Dynamics 365 programmām

Pirmkārt, ir svarīgi atzīmēt, ka vienības integrācijas atslēga ir msdyn_symbol. Tāpēc šai vērtībai ir jābūt unikālai pakalpojumā Dataverse vai citās Dynamics 365 programmās. Tā kā citās Dynamics 365 programmās vienības unikalitāti nosaka pāris "Vienību grupas ID" un "Nosaukums", ir jāapsver dažādi scenāriji, kā saskaņot vienību datus starp Finance and Operations programmām un Dataverse.

Vienībām, kas atbilst/pārklājas Finance and Operations programmās un citās Dynamics 365 lietojumprogrammās:

+ **Vienība pieder vienību grupai citās Dynamics 365 programmās, kas atbilst saistītajai vienību klasei Finance and Operations programmās**. Šādā gadījumā kolonna msdyn_symbol citās Dynamics 365 programmās ir jāaizpilda ar vienības simbolu no Finance and Operations programmām. Tāpēc, kad dati tiks saskaņoti, vienību grupa tiks iestatīta kā "Uzturēta ārēji" citās Dynamics 365 programmās.
+ **Vienība pieder kādai vienību grupai citās Dynamics 365 programmās, kas neatbilst saistītajai vienību klasei Finance and Operations programmās (neviena no esošajām vienību klasēm Finance and Operations programmās citās Dynamics 365 lietojumprogrammās).** Šādā gadījumā msdyn_symbol jāaizpilda ar nejaušu virkni. Ņemiet vērā, ka šai vērtībai ir jābūt unikālai citās Dynamics 365 programmās.

Vienībām un vienību klasēm Finance and Operations programmās, kas nepastāv citās Dynamics 365 programmās:

Kā daļa no duālā ieraksta vienību grupas no Finance and Operations programmām un tās atbilstošās vienības tiek izveidotas un sinhronizētas citās Dynamics 365 programmās un Dataverse, un vienību grupa tiks iestatīta kā "Uzturēta ārēji". Nav nepieciešama papildu sāknēšana.

Vienībām citās Dynamics 365 programmās, kas nepastāv Finance and Operations programmās:

Kolonnai msdyn_symbol jābūt aizpildītai visām vienībām. Vienības vienmēr var izveidot Finance and Operations programmās atbilstošajā vienību klasē (ja tāda ir). Ja vienības klase nepastāv, vispirms ir jāizveido vienību klase (ņemiet vērā, ka vienības klasi nevar izveidot Finance and Operations programmās, izņemot paplašinājumu, ja paplašināt uzskaitījumu), kas atbilst pārējo Dynamics 365 programmu vienību grupai. Pēc tam varat izveidot vienību. Ņemiet vērā, ka vienības simbolam Finance and Operations programmās jābūt msdyn_symbol, kas vienībai iepriekš norādīts citās Dynamics 365 programmās.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Preces politikas: dimensija, izsekošanas un glabāšanas grupas

Preces politikas ir politiku kopas, ko izmanto preču definēšanai un to raksturlielumus krājumos. Produktu dimensiju grupa, preču izsekošanas dimensiju grupa un noliktavas dimensiju grupa ir atrodama kā produktu politikas.

Finance and Operations programmas | Customer engagement programmas |
---|---
[Preces dimensiju grupas](mapping-reference.md#173) | msdyn\_ productdimensiongroups |
[Noliktavas dimensiju grupas](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Izsekošanas dimensiju grupas](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Preču hierarhijas

Finance and Operations programmas | Customer engagement programmas |
---|---
[Preču kategoriju piešķires](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Preču kategoriju hierarhijas](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Preču kategoriju hierarhijas lomas](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Preču integrācijas atslēga

Lai unikāli identificētu preces starp Dynamics 365 for Finance and Operations un precēm pakalpojumā Dataverse, tiek izmantotas integrācijas atslēgas.
Precēm **(productnumber)** ir unikāla atslēga, kas identificē preci pakalpojumā Dataverse. To veido šāda konkatenācija: **(uzņēmums, msdyn_productnumber)**. **Uzņēmums** norāda juridisko personu Finance and Operations, un **msdyn_productnumber** norāda preces numuru konkrētai precei Finance and Operations.

Citu Dynamics 365 programmu lietotājiem prece tiek identificēta UI ar **msdyn_productnumber** (ņemiet vērā, ka kolonnas etiķete ir **Preces numurs**). Preces veidlapā tiek rādīts gan uzņēmums, gan msydn_productnumber. Tomēr kolonna (productnumber) - unikālā preces atslēga - netiek rādīta.

Ja izveidojat programmas pakalpojumā Dataverse, ir jāpievērš uzmanība tam, kā izmantojat **productnumber** (unikālo produkta ID) kā integrācijas atslēgu. Nelietojiet **msdyn_productnumber**, jo tā nav unikāla.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Sākotnējā preču sinhronizācija un datu migrēšana no Dataverse uz Finance and Operations

### <a name="initial-synchronization-of-products"></a>Sākotnējā preču sinhronizācija

Kad duālais ieraksts ir iespējots, preces no Finance and Operations tiek sinhronizētas ar Dataverse un Customer engagement programmām. Preces, kas izveidotas Dataverse un citās Dynamics 365 programmās pirms duālā ieraksta palaišanas, netiks atjauninātas vai saskaņotas ar preču datiem no Finance and Operations programmām.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Atbilstošie preču dati no Finance and Operations un citām Dynamics 365 programmām

Ja vienas un tās pašas preces tiek turētas (pārklāšanās/salīdzināšana) Finance and Operations un Dataverse, un citās Dynamics 365 programmās, iespējojot duālo ierakstu, tiks veikta preču sinhronizācija no Finance and Operations, un vienai un tai pašai precei parādīsies dublikāta ieraksti pakalpojumā Dataverse.
Lai izvairītos no iepriekš minētās situācijas, ja citām Dynamics 365 programmām ir produkti, kas pārklājas/saskan ar Finance and Operations, tad administratoram, iespējojot duālo ierakstu, ir jāsāknē lauki **Uzņēmums** (piemērs: "USMF") and **msdyn_productnumber** (piemērs: "1234:Black:S"), pirms tiek veikta preču sinhronizēšana. Citiem vārdiem sakot, šie divi preces lauki pakalpojumā Dataverse ir jāaizpilda ar attiecīgo uzņēmumu Finance and Operations, ar kuru prece ir jāsaskaņo, un ar preces numuru.

Pēc tam, kad sinhronizācija ir iespējota un notiek, preces no Finance and Operations tiks sinhronizētas ar saskaņotajām precēm pakalpojumā Dataverse un citās Dynamics 365 programmās. Tas ir attiecināms uz atšķirīgām precēm un preču variantiem.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Preču datu migrēšana no citām Dynamics 365 programmām uz Finance and Operations

Ja citās Dynamics 365 programmās ir preces, kas nav iekļautas Finance and Operations, administrators var vispirms izmantot **EcoResReleasedProductCreationV2Entity**, lai importētu šīs preces Finance and Operations. Un, otrkārt, saskaņot preču datus no Finance and Operations un citām Dynamics 365 programmām, kā aprakstīts iepriekš.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
