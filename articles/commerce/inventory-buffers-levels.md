---
title: Krājumu buferu un krājumu līmeņu konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt krājumu buferus un krājumu līmeņus, kas nosaka krājumu pieejamības ziņojumapmaiņu Microsoft Dynamics 365 Commerce vietnēs.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 842389811169f785235de7ac7d9a49ab903f99ddf7d43f139aba0873a2577d72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727537"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Krājumu buferu un krājumu līmeņu konfigurēšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt krājumu buferus un krājumu līmeņus, kas nosaka ziņojumapmaiņu par krājumu pieejamību Microsoft Dynamics 365 Commerce vietnēs.

Dynamics 365 Commerce Headquarters atrodas krājumu dati un dažādi kanāli, piemēram, pārdošanas punkta (POS) programmas, e-komercijas veikali un citas pielāgotas integrētas programmas, kas asinhroni izgrūž un pievelk krājumus. Tāpēc pieejamās krājumu vērtības, kas tiek iegūtas, izmantojot rīcībā esošo krājumu lapu Commerce Headquarters ar POS lietotāja interfeisu (UI) un e-tirdzniecības krājumu pieejamības API, reāllaikā ne vienmēr ir 100 procentīgi precīzas.

Tā vietā, lai parādītu faktiskās krājumu vērtības e-tirdzniecības veikalos, daudzi mazumtirgotāji izvēlas tikai parādīt ziņojumapmaiņu par krājumu pieejamības statusu (piemēram, "Pieejams" vai "Nav noliktavā"), lai informētu klientus, vai krājums ir pieejams pirkšanai vai potenciāli nav noliktavā. Šajā pieejā ir jābūt pieejamiem un konfigurētiem krājumu buferiem un krājumu līmeņiem, kas nosaka krājumu pieejamības ziņojumapmaiņu.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Priekšnosacījums: ieslēdziet krājumu buferu un krājumu līmeņu līdzekli

Krājumu buferu un krājumu līmeņu līdzeklis tiek kontrolēts, izmantojot līdzekļu pārvaldību programmā Commerce Headquarters. Lai ieslēgtu šo līdzekli, veiciet tālāk minētās darbības.

1. Dodieties uz **Sistēmas administrēšana** \> **Darbvietas** \> **Līdzekļu pārvaldība**.
1. Meklējiet līdzekli **Iespējot krājumu buferus un krājumu līmeņus**, atlasiet tā rindu un pēc tam atlasiet **Iespējot tūlīt**.

Pēc līdzekļa ieslēgšanas varat atrast krājumu līmeņus **Mazumtirdzniecība un komercija \> Krājumu pārvaldība**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Krājumu līmeņa profila izveide un konfigurēšana

*Krājumu līmeņa profils* nosaka, vai tiek uzskatīts, ka attiecīgais preču daudzuma statuss ir Noliktavā, Nav noliktavā vai arī tam ir kāds cits pielāgots statuss. Varat izveidot un konfigurēt vairākus krājumu līmeņa profilus vienai juridiskajai personai. Katrs profils sastāv no krājumu līmeņu kopas, un katru līmeni definē *diapazons*, *kods* un *etiķete*.

- **Diapazons** — katru diapazonu definē *sākuma daudzums* un *beigu daudzums*. Daudzuma vērtība ietilpst diapazonā, ja tā ir lielāka par šī diapazona sākuma daudzumu un nav lielāka par beigu daudzumu.
- **Kods** — kods ir iekšējs saīsinājums, kas attēlo līmeni. Debitori, kas tieši integrējas ar krājumu API, var izmantot kodus, lai izveidotu papildu loģiku dotajam krājumu līmenim. Piemēram, tie var izslēgt preces iegādes iespēju preces, kad tās krājumu līmeņa kods ir **OOS** ("Nav noliktavā").
- **Etiķete** — etiķete ir jēgpilns uz klientu orientēts ziņojums, kas norāda krājumu līmeni debitoriem e-komercijas vietnē.

### <a name="create-an-inventory-level-profile"></a>Krājumu līmeņa profila izveide

Lai izveidotu krājumu līmeņa profilu, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija** \> **Krājumu pārvaldība** \> **Krājumu līmeņi**.
1. Darbību rūtī atlasiet **Jauns** un pēc tam ievadiet vērtības laukos **Profila ID** un **Apraksts**.
1. Kopsavilkuma cilnē **Diapazoni** atlasiet **Pievienot**, lai pievienotu jaunu līmeni, un pēc tam ievadiet vērtības šī līmeņa kolonnās **Sākuma daudzums**, **Beigu daudzums**, **Kods** un **Etiķete**. Atkārtojiet šo darbību, lai pievienotu vairāk līmeņu. Pēc vajadzības varat rediģēt vērtības datu režģī vai arī varat atlasīt **Dzēst**, lai noņemtu līmeni.
1. Darbību rūtī atlasiet **Saglabāt**.

Izveidojot jaunu profilu, automātiski tiek inicializēti divi krājumu līmeņi, kā norādīts zemāk.

- **OOS** — līmenis "Nav noliktavā", kur diapazona apakšējā robeža ir negatīva bezgalība. Šim līmenim sākuma daudzumu un kodu nevar rediģēt.
- **AVAIL** — "pieejams" līmenis, kur diapazona augšējā robeža ir bezgalība. Šim līmenim beigu daudzumu un kodu nevar rediģēt.

> [!NOTE]
> Profila definīcijā nevar būt iztrūkumu vai pārklāšanās.

Varat izmantot pogu **Tulkojumi** darbības rūtī, lai konfigurētu etiķetes ziņojuma lokalizētās virknes. Tad jums jāpalaiž **1110** (**Globālā konfigurācija**) sadales grafika darbs, lai sinhronizētu lokalizētās virknes ar kanāliem.

### <a name="configure-an-inventory-level-profile"></a>Krājumu līmeņa profila konfigurēšana

Varat konfigurēt krājumu līmeņa profilu preču kategorijas līmenī vai arī atsevišķu preču līmenī. Ja krājuma līmeņa profils ir konfigurēts precei, krājumu līmenis tiek noteikts, pamatojoties uz diapazoniem, kas definēti saistītajā profilā. Pretējā gadījumā krājuma līmenis "Pieejams" vai "Nav noliktavā" tiek noteikts, pamatojoties uz to, vai precei ir pozitīvs rīcībā esošais daudzums.

Lai konfigurētu krājumu līmeņa profilu kategorijai, izpildiet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība** \> **Preces un kategorijas** \> **Tirdzniecības preču hierarhija**.
1. Atlasiet kategoriju, kurai konfigurēt krājumu līmeņa profilu.
1. Kopsavilkuma cilnē **Pārdošanas preču rekvizīti** atlasiet juridisko personu.
1. Sadaļas **Tirdzniecības krājumi** laukā **Krājumu līmeņa profils** atlasiet vienu no iepriekšdefinētajiem krājumu līmeņa profiliem.

Varat izmantot pogu **Atjaunināt preces**, kas atrodas darbības rūtī, lai ieviestu kategorijas līmeņa profila vērtību kategorijas pamatā esošajām precēm. Papildinformāciju skatiet [Preču kategoriju un preču pārvaldība](category-management-product-creation.md).

Lai konfigurētu krājumu līmeņa profilu tirdzniecībā laistai precei, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība** \> **Preces un kategorijas** \> **Tirdzniebā laistās preces pēc kategorijas**.
1. Atlasiet preci un pēc tam atveriet tās preču informācijas lapu.
1. Kopsavilkuma cilnes **Pārdot** sadaļā **Tirdzniecības krājumi** laukā **Krājumu līmeņa profils** atlasiet vienu no iepriekšdefinētajiem krājumu līmeņa profiliem.

Kad tiek izveidota jauna prece, lauks **Krājumu līmeņa profils** tāpat kā daudzi citi preces līmeņa atribūti tiks iestatīts uz vērtību, kas ir konfigurēta kategorijai, ar kuru prece ir saistīta.

> [!NOTE]
> Krājumu līmeņa profils ir juridiska persona — konkrēts atribūts. Vienai un tai pašai kategorijai vai precei krājumu līmeņa profila vērtība dažādām juridiskām personām var atšķirties.

Lai sinhronizētu krājumu līmeņa profilu konfigurācijas ar kanāliem, rīkojieties šādi.

1. Pārejiet uz **Retail un Commerce** \> **Retail un Commerce IT** \> **Sadales grafiks**.
1. Palaidiet **1040** (**Prece**) sadales grafiku.

## <a name="configure-an-inventory-buffer"></a>Krājumu bufera konfigurēšana

*Krājumu buferis* ir lietotāja definēta vērtība, kas no sākotnējā krājuma daudzuma atņem papildu daudzumu, lai aprēķinātu paredzamo daudzumu. Šis paredzamais daudzums sniedz mazumtirgotājiem drošu buferi, lai tie nepārdotu vairāk preču nekā ir tās faktiskais rīcībā esošais krājums. Varat konfigurēt krājumu buferi preču kategorijas līmenī vai arī atsevišķu preču līmenī. Ja nav krājuma buferis nav norādīts, tiks izmantota noklusējuma vērtība **0** (nulle).

Lai konfigurētu krājumu buferi kategorijai, izpildiet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība** \> **Preces un kategorijas** \> **Tirdzniecības preču hierarhija**.
1. Atlasiet kategoriju, kurai konfigurēt krājumu buferi.
1. Kopsavilkuma cilnē **Pārdošanas preču rekvizīti** atlasiet juridisko personu.
1. Sadaļas **Tirdzniecības krājumi** laukā **Krājumu buferis** ievadiet pozitīvu vērtību.

Varat izmantot pogu **Atjaunināt preces**, kas atrodas darbības rūtī, lai ieviestu kategorijas līmeņa buferi vērtību kategorijas pamatā esošajām precēm. Papildinformāciju skatiet [Preču kategoriju un preču pārvaldība](category-management-product-creation.md).

Lai konfigurētu krājumu buferi tirdzniecībā laistai precei, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība** \> **Preces un kategorijas** \> **Tirdzniebā laistās preces pēc kategorijas**.
1. Atlasiet preci un pēc tam atveriet tās preču informācijas lapu.
1. Kopsavilkuma cilnes **Pārdot** sadaļas **Tirdzniecības krājumi** laukā **Krājumu buferis** ievadiet pozitīvu vērtību.

Kad tiek izveidota jauna prece, lauks **Krājumu buferis** tiks iestatīts uz vērtību, kas ir konfigurēta kategorijai, ar kuru prece ir saistīta.

> [!NOTE]
> Ja precei ir konfigurēti gan krājumu bufera, gan krājumu līmeņa profili, tad diapazona aprēķināšanai, lai noteiktu krājumu līmeni, tiks izmantots preces aplēstais daudzums (proti, sākotnējais daudzums mīnus bufera vērtība).

Lai sinhronizētu krājumu buferu konfigurācijas ar kanāliem, rīkojieties šādi.

1. Pārejiet uz **Retail un Commerce** \> **Retail un Commerce IT** \> **Sadales grafiks**.
1. Palaidiet **1040** (**Prece**) sadales grafiku.

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Krājumu buferu un krājumu līmeņu izmantošana e-tirdzniecības scenārijā

Commerce vietnes būvētājs izmanto krājuma bufera un krājumu līmeņa iespējas programmā Commerce Headquarters, lai noteiktu krājumu pieejamības ziņojumapmaiņu e-komercijas vietnēs. Papildinformāciju skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

Vai arī, ja integrējat trešās puses e-komercijas risinājumu, varat izmantot **GetEstimatedAvailability** un **GetEstimatedProductWarehouseAvailability** API, lai parādītu preces krājumu pieejamību savā e-tirdzniecības scenārijā. Papildinformāciju par šiem API skatiet [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).

Krājumu buferu un krājumu līmeņu ieviešana iespējo šos API, lai atgrieztu krājumu līmeņa kodus un etiķešu ziņojumus, kas tiek noteikti, pamatojoties uz kopējām pieejamām un pieejamām fiziskām vērtībām. API var tālāk konfigurēt, lai noteiktu, vai krājumu daudzums tiek atgriezts kopā ar ziņojumu un vai pieejamais daudzums tiek samazināts par krājuma bufera vērtību.

Lai konfigurētu preces pieejamības API atbildi, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība** \> **Headquarters iestatīšana** \> **Parameteri** \> **Tirdzniecības parametri**.
1. Sadaļas **Veikala krājumi** cilnes **Krājumi** laukā **Preču pieejamības API e-tirdzniecībai** atlasiet vērtību.
1. Lai lietotu iestatījumus kanāliem, palaidiet **1110** (**Globālā konfigurācija**) sadales grafika darbu.

## <a name="additional-resources"></a>Papildu resursi

[Preču kategoriju un preču pārvaldība](category-management-product-creation.md)

[Krājumu iestatījumu lietošana](inventory-settings.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
