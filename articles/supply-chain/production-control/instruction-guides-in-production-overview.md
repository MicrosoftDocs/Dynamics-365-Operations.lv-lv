---
title: Jauktas realitātes ceļvežu nodrošināšana ražošanas darbiniekiem
description: Šajā tēmā skaidrots, kā integrēt ražošanas pārvaldības moduli programmā Microsoft Dynamics 365 Supply Chain Management ar Dynamics 365 Guides.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 59fe3996013737198d4fbc86d64f8ef9dbe035e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829358"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Jauktas realitātes ceļvežu nodrošināšana ražošanas darbiniekiem

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Darbinieki ražošanas procesos gūs labumu no atbilstošām instrukcijām, kas tiek sniegtas īstajā laikā, ņemot vērā darba kontekstu. *Instrukcijas* attiecas uz vairākiem darbu domēniem, tai skaitā: montāžu, pakalpojumiem, operācijām, sertificēšanu un drošību. Visās šajās pamata biznesa funkcijās pastāvīgas apmācību instrukcijas var palīdzēt darbiniekiem sasniegt vairāk un strādāt labāk.

## <a name="introduction"></a>Ievads

Instrukcijas var sniegt dažādos veidos. Viena efektīva sistēma, kas piegādā nestandarta pielietojuma veidus [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides var sniegt darbiniekiem iespējas, izmantojot praktiskas apmācības. Jūs varat definēt standartizētus procesus, izmantojot detalizētus norādījumus, kas iepazīstinās jūsu darbiniekus ar nepieciešamajiem rīkiem un daļām un parādīs darbiniekiem, kā izmantot šos rīkus reālās darba situācijās.

Varat pievienot ceļvežus dažādiem ražošanas kontroles aspektiem, tostarp:

- [Resursi](#resources)
- [Resursu grupas](#resource-groups)
- [Izlaistās preces](#released-products)
- [Formulas](#formulas)
- [Formulas versijas](#formula-versions)
- [Materiālu komplekti (MK)](#bom)
- [MK versijas](#bom-versions)
- [Maršruti](#routes)
- [Maršruta versijas](#route-versions)
- [Maršruta operāciju relācijas](#route-operation-relations)

> [!NOTE]
> Varat arī pievienot ceļvežus, izmantojot līdzekļu pārvaldību. Papildu informāciju par šo opciju skatiet šeit: [Integrējiet Dynamics 365 Supply Chain Management (līdzekļu pārvaldība) ar Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Kad zemākā līmeņa nodarbinātais izvēlas darbu ražotnē, izmantojot Supply Chain Management, nodarbinātais var redzēt [atbilstošos ceļvežus](#logic) darba kartē. Kad nodarbinātais izvēlas noteiktu ceļvedi, ekrānā tiek parādīts šī ceļveža QR kods. Pēc tam nodarbinātais izmanto savu HoloLens, lai skenētu QR kodu, kas palaiž ceļvežus un parāda nepieciešamās instrukcijas.

Tālāk minētās apakšsadaļas apraksta dažus atlasītus scenārijus, kuros uzņēmumi dažādās nozarēs var redzēt vislielākos ieguvumus, izmantojot ceļvežus ražošanas instrukciju prezentēšanā.

### <a name="assembly"></a>Montāža

![Ceļvežu izmantošana montāžas uzdevumos](media/instruction-guides-hero-assembly.png "Ceļvežu izmantošana pakalpojumu uzdevumos")

Montāžas operāciju instrukcijas parāda nodarbinātajiem nepieciešamos rīkus un daļas un kā tos izmantot reālās darba situācijās.

Ražošanas vadītāji var izveidot un piešķirt ceļvežus, piemēram, [ražošanas maršrutiem](routes-operations.md), [operāciju relācijām](routes-operations.md#operation-relations) vai [materiālu komplektiem](bill-of-material-bom.md). Nodarbinātie atradīs atbilstošās instrukcijas par attiecīgo operācijas pieredzi ražotnē.

### <a name="service"></a>Pakalpojumi

![Ceļvežu izmantošana pakalpojumu uzdevumos](media/instruction-guides-hero-service.png "Ceļvežu izmantošana pakalpojumu uzdevumos")

Aprīkojiet tehniskos darbiniekus ar vadītām instrukcijām darba vietā, novēršot nepieciešamību ieplānot papildu apmeklējumus.

Pakalpojumu pārvaldnieki var piešķirt ceļvežus, piemēram, noteiktiem [produktiem](../../commerce/product.md), kas iepazīstina ar kvalitātes novērtējuma rutīnām.

### <a name="quality"></a>Kvalitāte

![Ceļvežu izmantošana kvalitātes nodrošināšanas uzdevumos](media/instruction-guides-hero-quality.png "Ceļvežu izmantošana kvalitātes nodrošināšanas uzdevumos")

Ieviesiet jaunus procesus un nodrošiniet lielāku konsekvenci, pārvēršot nodarbināto zināšanas par atkārtoti izmantojamu rīku.

Kvalitātes nodrošināšanas pārvaldnieki var piešķirt ceļvežus, piemēram, noteiktiem [produktiem](../../commerce/product.md), kas iepazīstina ar kvalitātes novērtējuma rutīnām.

### <a name="certifications"></a>Sertifikācijas

![Ceļvežu izmantošana ar sertifikāciju saistītos uzdevumos](media/instruction-guides-hero-certification.png "Ceļvežu izmantošana ar sertifikāciju saistītos uzdevumos")

Pārliecinieties, ka katrs nodarbinātais atbilst augstiem standartiem, ātri identificējot, kam un kur nepieciešama palīdzība.

### <a name="safety"></a>Drošība

![Ceļvežu izmantošana darba drošības instrukcijās](media/instruction-guides-hero-safety.png "Ceļvežu izmantošana darba drošības instrukcijās")

Sniedziet norādījumus, kas virtuāli iepazīstina ar bīstamām procedūrām pirms mēģinājuma tās veikt fiziskajā vidē. Ar jaukas realitātes pieeju nodarbinātie var virtuāli gūt pieredzi ar bīstamām procedūrām.

Ražošanas vadītāji var nodrošināt īpašus norādījumus par rīkošanos ar bīstamiem materiāliem vai maigas apiešanās procedūrām, piešķirot instrukcijas [produkta krājumiem](../../commerce/product.md), [maršrutiem](routes-operations.md) un [operācijām](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Sāciet darbu ar instrukcijām un ceļvežiem

Lai iespējotu instrukcijas ražošanas procesos, Supply Chain Management nodrošina gatavu integrāciju ar Dynamics 365 Guides. Lai izveidotu, uzturētu un piešķirtu jauktās realitātes instrukcijas ražošanas pamatlīdzekļiem un darbam, nepieciešama licencēta un instalēta Guides programmas instance.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai izmantotu šo līdzekli, jūsu sistēmā jābūt iekļautam tālāk minētajam:

- Dynamics 365 Supply Chain Management versija 10.0.15 vai jaunāka versija
- [Duālā rakstīšana](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) Supply Chain Management lietojumprogrammām.
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versija 400.0.1.48 vai jaunāka versija

### <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Lai līdzeklis būtu pieejams jūsu sistēmā, ir jāiespējo tā konfigurācijas atslēgas. Tas jādara tikai vienreiz. Lai to izdarītu, administratoram jāveic šādas darbības:

1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Izvērsiet sadaļu **Jauktā realitāte** un tad atzīmējiet izvēles rūtiņu **Jauktās realitātes ceļvedis**.
1. Izvērsiet sadaļu **Produktu pārvaldība** un tad atzīmējiet izvēles rūtiņu **Produktu instrukcijas**.
1. Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Ceļvežu ražotnē parādīšanās veida konfigurēšana

Lai konfigurētu, kā ceļveži parādās ražotnē, dodieties uz **Jauktā realitāte \> Dynamics 365 Guides \> Konfigurēt ceļvežu integrāciju**.

![Konfigurējiet ceļvežu integrāciju ražošanai](media/instruction-guides-configure-integration.png "Konfigurējiet ceļvežu integrāciju ražošanai")

Iestatiet tālāk minētos laukus:

- **Microsoft Dataverse vietrādis URL** - norādiet Microsoft Dataverse vides vietrādi URL, kurā veidojat jūsu Guides. Formāts ir "contoso.crm4.dynamics.com", kurā URL pirmā daļa parasti tiek nosaukta pēc jūsu organizācijas (piemēram, "contoso."), otrā daļa ir raksturīga jūsu vides datu reģionam (piemēram, "crm4."), un pēdējā daļa ir domēns (piemēram, "dynamics.com"). Viens no veidiem, kā atrast pareizo vietrādi URL, ir doties uz [home.dynamics.com](https://home.dynamics.com/) un tad atvērt Guides programmu. Kad Guides atveras, jūsu pārlūkprogrammas adreses joslā redzēsit vietrādi URL (lietojiet tikai pamata vietrādi URL, kam jāizskatās kā iepriekšējā piemērā). Šī vērtība tiek izmantota, lai sastādītu jūsu ceļvežu adreses, un tā tiks iekodēta QR kodos."
- **QR koda izmērs** — iestatiet atveidotā QR koda izmēru. Ieteicams izvēlēties izmēru, kas aizpildīs lielāko daļu displeja ekrāna, bet ne lielāku. Parasti *15* ir laba vērtība.
- **QR koda kļūdu labošanas līmenis** — iestatiet QR koda granularitāti. Lielāka granularitāte var paaugstināt koda uzticamību, bet jūsu **QR koda izmēram** ir jābūt pietiekami lielam, lai varētu atbalstīt detalizācijas līmeni, kāds nepieciešams jūsu atlasītajam labošanas līmenim.

> [!TIP]
> - QR kodu izmēri, kas ir pārāk lieli displejam, aizņems mazliet ilgāku laiku, lai tos atveidotu un pēc tam mērogotu, lai tas atbilstu jūsu displeja izmēram. Tie nenodrošina priekšrocības.
> - QR koda izmēri, kas ir pārāk mazi, var samazināt HoloLens spēju dažās vidēs pareizi nolasīt kodu.
> - Mēs iesakām pārbaudīt iestatījumus katrai ierīcei, kas parādīs QR kodus HoloLens lietotājiem. Izvēlieties iestatījumus, kas nodrošina pietiekamu lasāmību jūsu ražotnes vidē.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Visu ceļvežu norīkojumu pārskata iegūšana

Izmantojiet lapu **Visi ceļveži**, lai redzētu sarakstu ar visiem jūsu organizācijā pieejamajiem ceļvežiem un visiem norīkojumiem, kas piešķirti jūsu ražošanas procesiem un resursiem. Lai to atvērtu, dodieties uz **Jauktā realitāte \> Ceļveži \> Visi ceļveži**. Saraksta augšpusē parādīti visi pieejamie ceļveži, un jūs varat izmantot šeit pieejamo lauku, lai filtrētu sarakstu. Saraksta apakšpusē parādīti visi ceļvežu norīkojumi un ir nodrošināta rīkjosla to pārvaldībai.

![Ceļvežu pārvaldība](media/instruction-guides-allguides.png "Ceļvežu pārvaldība")

Turpmākajās sadaļās ir aprakstīti objektu tipi, kam var piešķirt ceļvežus. Katrs piešķirtais ceļvedis sniedz instrukcijas, kas tiek automātiski pievienotas attiecīgajiem ražošanas darbiem un būs pieejamas ražotnē.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Saistīt ceļvedi ar resursu

Pievienojiet ceļvedi [resursam](operations-resources.md), lai piedāvātu ceļvedi attiecīgo ražošanas darbu kontekstā.

### <a name="typical-scenario-using-resources"></a>Tipisks scenārijs, izmantojot resursus

Piemēram, jūs varētu pievienot ceļvedi ar vispārējām iekārtas drošības instrukcijām vai norādījumiem par rīkošanos resursam vai iekārtas veidam. Pēc tam ceļvedis būs pieejams katrā darbā, kas veikts pie attiecīgās iekārtas.

### <a name="add-a-guide-to-a-resource"></a>Ceļveža pievienošana resursam

Lai pievienotu ceļvedi resursam:

1. Dodieties uz **Ražošanas kontrole \> Uzstādīšana \> Resursi \> Resursi**.
1. No saraksta rūts atlasiet resursu, kuram vēlaties piešķirt ceļvedi.
1. Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.
1. Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**. Režģim tiek pievienota jauna rinda.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt. Ja jums ir daudz ceļvežu, tad varat filtrēt sarakstu, lai atrastu meklēto.
    ![Ceļvežu pārvaldība](media/instruction-guides-allguides.png "Ceļvežu pārvaldība")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Saistīt ceļvedi ar resursu grupu

Varat pievienot ceļvedi [resursu grupām](tasks/define-discrete-manufacturing-resource-group.md), ja izmantojat tos, lai pārvaldītu iekārtu grupas, ražošanas rindas vai darba šūnas.

### <a name="typical-scenarios-using-resource-groups"></a>Tipiski scenāriji, izmantojot resursu grupas

**1. piemērs:** ir definēta resursu grupa vairākām viena modeļa iekārtām. Tā vietā, lai piešķirtu iekārtas modelim atbilstošos norādījumus par rīkošanos katram atbilstošajam resursam, jūs varat piešķirt ceļvedi resursu grupai, kas atspoguļo iekārtas modeli.

**2. piemērs:** ir definēta resursu grupa darba šūnai, kas satur dažādas iekārtas, un jums ir ceļvedis, kas sniedz vispārīgus norādījumus par to, kā uzturēt darba šūnu. Ceļvedis attiecas uz visām ražošanas aktivitātēm šajā darba šūnā.

### <a name="add-a-guide-to-a-resource-group"></a>Ceļveža pievienošana resursu grupai

Lai pievienotu ceļvedi resursu grupai:

1. Dodieties uz **Ražošanas kontrole \> Uzstādīšana \> Resursi \> Resursu grupas**.
1. No saraksta rūts atlasiet resursu grupu, kam vēlaties piešķirt ceļvedi.
1. Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.
1. Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**. Režģim tiek pievienota jauna rinda.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt. Ja jums ir daudz ceļvežu, tad varat filtrēt sarakstu, lai atrastu meklēto.
    ![Ceļveža pievienošana resursu grupai](media/instruction-guides-resourcegroup.png "Ceļveža pievienošana resursu grupai")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Ceļveža saistīšana ar izlaistu preci

Varat pievienot ceļvedi jebkurai [izlaistai precei](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Tipisks scenārijs, izmantojot izlaistas preces

Preču līmeņa ceļveži palīdz ražotnes darbiniekiem ar instrukcijām, kas attiecas uz specifisku izlaistu preču vai krājumu pārvaldību vai apstrādi.

### <a name="add-a-guide-to-a-released-product"></a>Ceļveža pievienošana izlaistai precei

Lai pievienotu ceļvedi izlaistai precei:

1. Dodieties uz **Ražošanas informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet preci, kurai vēlaties piešķirt ceļvedi.
1. Darbības rūtī atveriet cilni **Inženieris** un grupā **Skats** atlasiet **Saistītie ceļveži**.
1. Jūsu atlasītajai precei tiek atvērta lapa **Saistītie ceļveži**.
1. Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**. 
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana izlaistai precei:](media/instruction-guides-ReleasedProduct-AddGuides.png "Ceļveža pievienošana izlaistai precei")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Saistīt ceļvedi ar formulu

Varat pievienot ceļvedi jebkurai [formulai](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Tipisks scenārijs, izmantojot formulas
  
Formulas līmeņa ceļveži sniedz ražotnes darbiniekiem vadītus norādījumus par rīkošanos formulas vai receptes kontekstā. Ceļvežus var piešķirt arī formulas versijām.

> [!NOTE]
> Varat piešķirt norādījumus, kas attiecas uz ražošanas procesiem, pamatojoties uz formulu maršrutam, maršruta versijai vai maršruta operāciju relācijām.  

> Pašlaik ceļvežus nevar pievienot atsevišķām formulas rindām.

### <a name="add-a-guide-to-a-formula"></a>Ceļveža pievienošana formulai

Lai ceļvedi pievienotu formulai:

1. Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.
1. Atveriet formulu, kurai vēlaties piešķirt ceļvedi.
1. Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.
1. Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.
1. Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**. Režģim tiek pievienota jauna rinda.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana formulai:](media/instruction-guides-Formula.png "Ceļveža pievienošana formulai")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Saistīt ceļvedi ar formulas versiju

Varat pievienot ceļvedi jebkurai [formulas versijai](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Tipisks scenārijs, izmantojot formulas versijas

Ceļveži, kas pievienoti atsevišķai formulas versijai sniedz ražotnes darbiniekiem instrukcijas, kas iepazīstina ar formulas receptes attiecīgās versijas ražošanu.

> [!TIP]
> Varat piešķirt norādījumus, kas attiecas uz ražošanas procesiem, pamatojoties uz šīs formulas versiju maršrutam, maršruta versijai vai maršruta operāciju relācijām.  

> [!NOTE]
> Pašlaik ceļvežus nevar pievienot atsevišķām formulas rindām.

### <a name="add-a-guide-to-a-formula-version"></a>Ceļveža pievienošana formulas versijai

Lai ceļvedi pievienotu formulas versijai:

1. Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.
1. Atveriet formulu, kas ietver versiju, kurai vēlaties piešķirt ceļvedi.
1. Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.
1. Kopsavilkuma cilnē **Formulas versijas**, atlasiet versiju, kurai vēlaties piešķirt ceļvedi.
1. Rīkjoslā **Formulas versijas** atlasiet **Saistītie ceļveži**.
    ![Ar atlasīto formulas versiju saistīto ceļvežu atvēršana](media/instruction-guides-FormulaVersion.png "Ar atlasīto formulas versiju saistīto ceļvežu atvēršana")
1. Jūsu formulas versijai tiek atvērta lapa **Saistītie ceļveži**.
1. Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**. 
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana formulas versijai](media/instruction-guides-FormulaVersionAddGuide.png "Ceļveža pievienošana formulas versijai")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Saistiet ceļvedi ar materiālu komplektu

Varat pievienot ceļvedi jebkuram [materiālu komplektam](bill-of-material-bom.md) (MK).

### <a name="typical-scenario-using-bills-of-materials"></a>Tipisks scenārijs, izmantojot materiālu komplektus

Ceļveži, kas pievienoti MK sniedz ražotnes darbiniekiem instrukcijas, kas paskaidro, kā sagatavot un apstrādāt materiālu no MK. Ceļvežus var piešķirt arī MK versijām.

> [!NOTE]
> Pašlaik ceļvežus nevar pievienot atsevišķām MK rindām.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Ceļveža pievienošana materiālu komplektam

Lai ceļvedi pievienotu materiālu komplektam:

1. Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Materiālu komplekti**.
1. Atveriet materiālu komplektu, kuram vēlaties piešķirt ceļvedi.
1. Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.
1. Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.
1. Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**. Režģim tiek pievienota jauna rinda.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana MK:](media/instruction-guides-BOM.png "Ceļveža pievienošana MK")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Saistiet ceļvedi ar materiālu komplekta versiju

Varat pievienot ceļvedi jebkurai [materiālu komplekta versijai](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Tipisks scenārijs, izmantojot materiālu komplekta versijas

Atsevišķai MK versijai piesaistītie ceļveži nodrošina ražotnes darbiniekus ar instrukcijām, kas paskaidro, kā sagatavot un apstrādāt materiālu MK versijai, kas atšķiras no vispārējā MK vai citām tā versijām.

> [!NOTE]
> Pašlaik ceļvežus nevar pievienot atsevišķām MK rindām.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Ceļveža pievienošana materiālu komplekta versijai

Lai ceļvedi pievienotu materiālu komplekta versijai:

1. Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Materiālu komplekti**.
1. Atveriet MK, kas ietver versiju, kurai vēlaties piešķirt ceļvedi.
1. Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.
1. Kopsavilkuma cilnē **MK versijas**, atlasiet versiju, kurai vēlaties piešķirt ceļvedi.
1. Rīkjoslā **MK versijas** atlasiet **Saistītie ceļveži**.
    ![Ar atlasīto MK versiju saistīto ceļvežu atvēršana](media/instruction-guides-BOMVersion.png "Ar atlasīto MK versiju saistīto ceļvežu atvēršana")
1. Jūsu MK versijai tiek atvērta lapa **Saistītie ceļveži**.
1. Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana MK versijai](media/instruction-guides-BOMVersionAddGuide.png "Ceļveža pievienošana MK versijai")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Saistīt ceļvedi ar maršrutu

Varat pievienot ceļvedi jebkuram [maršrutam](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Tipisks scenārijs, izmantojot maršrutus

Maršruti parasti tiek izmantoti, lai norādītu, kā noteikta izlaistā prece jāražo, pamatojoties uz MK vai MK versiju un ar resursu vai resursu grupu kopu.

Piešķiriet ceļvedi maršrutam, lai nodrošinātu detalizētas instrukcijas attiecīgajam ražošanas procesam.

### <a name="add-a-guide-to-a-route"></a>Ceļveža pievienošana maršrutam

Lai ceļvedi pievienotu maršrutam:

1. Doties uz **Ražošanas kontrole \> Visi maršruti**.
1. Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.
1. Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.
1. Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**. Režģim tiek pievienota jauna rinda.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana maršrutam](media/instruction-guides-Route.png "Ceļveža pievienošana maršrutam")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Saistīt ceļvedi ar maršruta versiju

Varat pievienot ceļvedi jebkurai [maršruta versijai](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Tipisks scenārijs, izmantojot maršruta versijas

Maršrutu versijas parasti tiek izmantotas, lai noteiktu ražošanas procesu variantus, pamatojoties uz esošu maršrutu. Katrai maršruta versijai varat piešķirt dažādus ceļvežus.

### <a name="add-a-guide-to-a-route-version"></a>Ceļveža pievienošana maršruta versijai

Lai pievienotu ceļvedi maršruta versijai:

1. Doties uz **Ražošanas kontrole \> Visi maršruti**.
1. Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.
1. Kopsavilkuma cilnē **Versijas** atlasiet versiju, kurai vēlaties piešķirt ceļvedi.
1. Rīkjoslā **Versijas** atlasiet **Saistītie ceļveži**.
    ![Ar atlasīto maršruta versiju saistīto ceļvežu atvēršana](media/instruction-guides-RouteVersion.png "Ar atlasīto maršruta versiju saistīto ceļvežu atvēršana")
1. Jūsu MK versijai tiek atvērta lapa **Saistītie ceļveži**.
1. Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.
    ![Ceļveža pievienošana maršruta versijai](media/instruction-guides-RouteVersionAddGuide.png "Ceļveža pievienošana maršruta versijai")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Saistīt ceļvedi ar maršruta operācijas saiti

Varat pievienot ceļvedi jebkurai [maršruta operācijas saitei](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Tipisks scenārijs, izmantojot maršruta operāciju saites

Operāciju saites ir vispiemērotākais veids, kā pievienot norādījumus preces procesam un ar to saistītajām darbībām. Varat atzīmēt norādījumus katrai operācijai maršrutā un atzīmēt dažādus norādījumus jebkāda veida relāciju kontekstam, kas noteikts maršrutam, piemēram, noteiktiem krājumiem, konfigurācijām un daudz kam citam. Var arī norādīt, uz kuriem operācijas posmiem norādījumi attiecas (piemēram, iestatīšanu, rindošanu, procesu vai transportu).

> [!NOTE]
> Ja jūs norādāt ceļvežus vairākām maršruta operāciju saitēm, no šiem ceļvežiem ražotnē ģenerētajam darbam tiks parādīts tikai ceļvedis, kas saistīts ar viskonkrētāko saiti.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Ceļveža pievienošana maršruta operācijas saitei

Lai pievienotu ceļvedi maršruta operācijas saitei:

1. Doties uz **Ražošanas kontrole \> Visi maršruti**.
1. Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.
1. Darbības rūtī atveriet cilni **Maršruts** un grupā **Uzturēt** atlasiet **Maršruta informācija**.
1. Atlasītajam maršrutam tiek atvērta lapa **Maršruta informācija**.
1. Augšējā režģī atlasiet operāciju, kurai vēlaties sniegt norādījumus.
1. Apakšējā režģī atlasiet specifisku saiti (vai vispārējo saiti **Viss**).
    ![Atlasiet operāciju un pēc tam saiti](media/instruction-guides-RouteOperationRelation.png "Atlasiet operāciju un pēc tam saiti")
1. Virs apakšējā režģa atveriet cilni **Saistītie ceļveži**.  ![Cilne Saistītie ceļveži](media/instruction-guides-RouteOperationRelation-AddGuide.png "Cilne Saistītie ceļveži")
1. Atlasiet **Pievienot** rīkjoslā, kas atrodas apakšējā režģa augšdaļā, lai režģim pievienotu jaunu rindu.
1. Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko jūs vēlaties piešķirt. Pārējā rindā atzīmējiet izvēles rūtiņu katram kontekstam, kurā atlasītajam ceļvedim jābūt pieejamam.

> [!NOTE]
> Katram operācijas posmam var pievienot vienu vai vairākus ceļvežus.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Atlasiet ceļvežus no ražotnes izpildes interfeisa

Kad nodarbinātais atver darbu sarakstu ražotnes izpildes interfeisā, Supply Chain Management atrod atbilstošos ceļvežus parādītajiem darbiem. Izmantojiet pogu **Ceļveži**, lai skatītu atbilstošos ceļvežus.

![Ceļvežu poga ražotnes izpildes interfeisā](media/instruction-guides-Shopfloor1.png "Ceļvežu poga ražotnes izpildes interfeisā")

Pēc tam uzvelciet HoloLens un piekļūstiet attiecīgajam ceļvedim, paskatoties uz QR kodu un aktivizējot atbilstošo ceļvedi.

![QR kods, lai piekļūtu ceļvežiem, izmantojot HoloLens](media/instruction-guides-Shopfloor2.png "QR kods, lai piekļūtu ceļvežiem, izmantojot HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Ceļvežu atlases loģikas risināšana

Varat pievienot ceļvežus šādiem ražošanas datiem:

- [Resursi](#resources)
- [Resursu grupas](#resource-groups)
- [Izlaistās preces](#released-products)
- [Formulas](#formulas)
- [Formulas versijas](#formula-versions)
- [Materiālu komplekti (MK)](#bom)
- [MK versijas](#bom-versions)
- [Maršruti](#routes)
- [Maršruta versijas](#route-versions)
- [Maršruta operāciju relācijas](#route-operation-relations)

Kad Supply Chain Management ģenerē darbus ražotnei, tas apkopos atbilstošos ceļvežus no šiem avotiem. Ņemiet vērā šos svarīgos noteikumus.

- Ja maršrutam vai ražošanas pasūtījumam tiek pievienota MK versija vai formulas versija, darbam tiks rādītas visi šai versijai piesaistītie ceļveži, kā arī ceļveži, kas piesaistīti pamata MK vai tā versijas formulai.
- Ja ražošanas pasūtījumam tiek pievienota maršruta versija, darbam tiks rādīti visi šai versijai piesaistītie ceļveži, kā arī ceļveži, kas piesaistīti šīs versijas pamata maršrutam.
- Ja definējat vairākas maršruta operāciju saites, kas ietver *Visas* saites un piešķir tām ceļvežus, darbam tiks parādīts tikai ceļveži, kas saistīti ar viskonkrētāko saiti.  

![Shēma, kā atrisināt atbilstošos ceļvežus](media/instruction-guides-Resolve.png "Shēma, kā atrisināt atbilstošos ceļvežus")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]