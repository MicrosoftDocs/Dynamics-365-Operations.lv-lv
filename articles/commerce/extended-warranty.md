---
title: Paplašināto garantiju izveide un konfigurēšana
description: Šī tēma apskata paplašinātās garantijas un apraksta, kā izveidot un konfigurēt tās Microsoft Dynamics 365 Commerce.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a875343d9b93f5ebf2c2992fba8b2f182310461e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413941"
---
# <a name="create-and-configure-extended-warranties"></a>Paplašināto garantiju izveide un konfigurēšana

[!include [banner](includes/banner.md)]

Šī tēma apskata paplašinātās garantijas un apraksta, kā izveidot un konfigurēt tās Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Klienti arvien biežāk izvēlas paplašināto atbalstu un pakalpojumus, iegādājoties preces, īpaši patēriņa preces, kas tiek pārdotas par augstākām cenām, piemēram, tālruņiem un datoriem. Piedāvājot pirkumam paplašinātās garantijas, mazumtirgotāji var palīdzēt veidot klientu lojalitāti. Paplašinātās garantijas ļauj klientiem uzzināt, kur viņi var meklēt pakalpojumus un atbalstu. Tāpēc viņi var uzticēties, ka to jautājumi tiks efektīvi risināti.

Paplašinātās garantijas var pārdot klientiem mazumtirdzniecības kanālā sākotnējās preces iegādes laikā. Tos var arī pārdot uz ierobežotu laiku pēc sākotnējā pirkuma.

### <a name="warranty-item-setup"></a>Garantijas vienības iestatīšana

Dynamics 365 Commerce nodrošina funkcionalitāti, kas ļauj izveidot garantijas vienību un iestatīt tai atribūtus. Šie atribūti ietver saistību starp preci un garantijas vienību, garantijas cenu un garantijas ilgumu. Pēc garantijas vienības konfigurēšanas un nodošanas organizatoriskajai vienībai, mazumtirgotājs var pārdot garantijas, izmantojot Moderno pārdošanas punktu (MPOS), tiešsaistes veikalus un citus mazumtirdzniecības kanālus.

### <a name="warranty-item-sales"></a>Garantijas vienības pārdošana

Paplašinātās garantijas tiek pārdotas klientiem mazumtirdzniecības kanālā sākotnējās preces iegādes laikā. Tos var arī pārdot uz ierobežotu laiku pēc sākotnējā pirkuma.

Pārdošanas punktā (POS), pārdošanas partneriem tiek piedāvāts pievienot paplašināto garantiju, kad saistītā prece tiek pievienota klienta grozam. Tādēļ piepārdošanas vai kombinētās pārdošanas iespēja tiek parādīta pārdošanas partneriem kā daļa no pārdošanas plūsmas.

Klienti var arī atgriezties vēlāk un iegādāties paplašināto garantiju precei, ko tie iepriekš iegādājušies. Šādos gadījumos pārdošanas partneris var meklēt sākotnējo transakciju un pārdot debitoram saistīto paplašināto garantijas vienību.

### <a name="warranty-terminology"></a>Garantijas terminoloģija

Tabulā ir definēti daži ar garantijām saistītie termini.

| Termiņš | apraksts |
|------------------------------|--------------|
| Paplašināta garantija/garantija | *Paplašināta garantija* attiecas uz pakalpojumu vienošanos vai līgumu, kas nodrošina Klientam pagarinātu garantiju. Paplašinātās garantijas ietver papildu pakalpojumus, kas attiecas uz preču aizstāšanu vai remontu paplašinātās garantijas laika periodā. |
| Ražotāja garantija | *Ražotāja garantija* (bieži minēta kā *ierobežotā garantija*) ir garantija, ko klienti saņem, iegādājoties preci. Piedāvājam dažus ražotāja garantijas līdzekļus:<ul><li>Garantijas izmaksas tiek iekļautas preces cenā. Klientiem nav jāmaksā papildu summa ražotāja garantijai.</li><li>Atkarībā no preču kategorijas ražotāja garantija parasti ilgst 30 dienas, sešus mēnešus vai vienu gadu. (Lielākajai daļai patērētāju elektronikas garantijas ilgums ir viens gads).</li><li>Garantija sedz visus defektus, kas radušies mehānisku vai elektrisko kļūmju dēļ. Segšana ir ierobežota, un tajā nav ietverti iegādātās preces nejauši bojājumi. Klientiem, kuri vēlas aizsargāt iegādātās preces no ikdienas bojājumiem, ir jāinvestē paplašinātajā garantijā. Paplašinātās garantijas ilgst no diviem līdz desmit gadiem atkarībā no preču kategorijas. Tām ir arī plašāks pārklājums, un tas aptver ikdienas negadījumus, piemēram, ūdens pilienus, izplūdes un traipus.</li></ul> |
| Garantijas krājums | *Garantijas prece* ir pagarinātas garantijas prece, ko pārdod garantijas precei. Piemēram, klēpjdatoriem ir divu gadu nelaimes gadījumu aizsardzības plāns. |
| Garantētā prece | *Garantētā prece* ir serializējama prece, kam tiek pārdota garantija. Piemēram, klēpjdators ir garantējamā prece, kam tiek pārdotas divu un trīs gadu paplašinātās garantijas. |
| Garantijas grupa | *Garantijas grupa* ir saistības starp garantijas precēm un garantējamajām precēm. POS izmanto garantijas grupas, lai noteiktu, kuras garantijas preces pārdošanas dalībniekiem ir jāpievieno, kad debitora grozam tiek pievienota garantējamā prece. |
| Garantijas politika | *Garantijas politika* ir entītija, kas ir izveidota tirdzniecībā, kad garantijas politika tiek pārdota. Garantijas politika ietver informāciju, piemēram, iegādātās garantijas preces sākuma un beigu datumus, noteikumi un nosacījumi, kā arī garantētās preces sērijas numurs. Garantijas politikas numurus var koplietot ar debitoriem, lai tiem būtu atsauce uz iegādāto paplašinātās garantijas preci. |

## <a name="create-a-warranty-item"></a>Izveidot garantijas preci

Lai izveidotu garantijas preci sadaļā Komercija, veiciet šādas darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Preces un kategorijas \> Preces**.
1. Atlasiet **Jauns**, lai izveidotu garantijas preci.
1. Dialoglodziņā **Jauns produkts** laukā **Preces veids** atlasiet **Pakalpojums**.
1. Laukā **Preces apakštips** atlasiet opciju **Prece**.
1. Laukā **Preces pakalpojuma tips** atlasiet opciju **Pakalpojums**.
1. Laukā **Preces nosaukums** ievadiet preces nosaukumu.
1. Laukā **Mazumtirdzniecības kategorija** atlasiet vērtību nolaižamajā dialoglodziņā un pēc tam atlasiet **Labi**.
1. Laukā **Preces numurs** ievadiet preces numuru.
1. Atlasiet **Labi**.
1. Lapā **Preces detalizēta informācija** kopsavilkuma cilnē **Garantija** iestatiet laukus **Laika vienība** un **Laika ilgums**.

    | Lauka nosaukums | Vērtība | apraksts |
    |------------|-------|-------------|
    | Laika vienība | **Diena(s)**, **Nedēļa(s)**, **mēnesis(-ši)** vai **Gads(-i)** | Šis lauks norāda garantijai izmantoto laika vienību. |
    | Laika ilgums | Pozitīva vesela skaitļa vērtība | Šis lauks norāda garantijas ilgumu atlasītajā laika vienībā. |

    Piemēram, divu gadu garantijai iestatiet **Laika vienības** lauku uz **Gads(-i)** un **Laika ilguma** lauku uz **2**. Vai arī iestatiet **Laika vienības** lauku uz **Mēnesis(-ši)** un **Laika ilguma** lauku uz **24**, kā parādīts sekojošajā ilustrācijā.

    ![Preces detalizētas informācijas lapa garantijas precei](./media/ew-time-properties.png)

1. Atlasiet **Saglabāt**, lai saglabātu garantijas preci.
1. Izlaidiet garantijas preci uzņēmumam, lai to varētu pārdot. Papildinformāciju skatiet [Uzstādīt mazumtirdzniecības preces](set-up-retail-products.md).
1. Lapā **Izlaistās preces detaļas**, kas atrodas **Garantijas** kopsavilkuma cilnē, iestatiet laukus **Cenas diapazona bāze**, **Apakšējā robeža** un **Augšējā robeža**.

    | Lauka nosaukums | Vērtība | apraksts |
    |------------|-------|-------------|
    | Pamatcenu diapazons | **Nav**, **Pamatcena** vai **Pārdošanas cena** | <ul><li>**Nav** - **Apakšējās robežas** un **Augšējās robežas** preces vērtības netiek piemērotas.</li><li>**Pamatcena** – dotā garantija tiks piemērota, ja pamatcena (tas ir, cena bez atlaidēm), kas norādīta garantijas precē, ir robežās no **Apakšējās robežas** un **Augšējās robežas** vērtībām, kas norādītas šeit, pamatojoties uz garantējamās preces cenas.</li><li>**Pārdošanas cena** - Šī vērtība ir paredzēta izmantošanai nākotnē.</li></ul> |
    | Apakšējā robeža, Augšējā robeža | Pozitīva vesela skaitļa vērtība | Šie lauki nosaka garantētā krājuma augšējās un apakšējās cenas robežas un to, kā pašreizējā garantijas prece tiek piemērota garantējamajai precei. Šīs robežas var tikt balstītas uz garantējamās preces pamatcenu (to sauc arī par ražotāja ieteikto mazumtirdzniecības cenu \[MSRP\]). Ja **Cenas diapazona bāzes** lauks ir iestatīts uz **Pamatcenu**, tikai garantējamajai precei, kam ir pamatcena no **Apakšējās robežas** un **Augšējās robežas** vērtības, tiks parādīta uzvedne ar aicinājumu pievienot garantijas preci POS sistēmā. |

    Piemēram, sekojošajā attēlā parādīts **Cenu diapazonu bāzes** lauks, kas iestatīts uz **Pamatcenu**, **Apakšējās robežas** lauks ir iestatīts kā $500 un **Augšējās robežas** lauks ir iestatīts uz $1000.
    
    ![Izlaistās preces detalizētas informācijas lapa garantijas precei](./media/ew-release-product-details.png)

1. Pievienojiet garantijas preci kanālam, kur tā tiks pārdota. Plašāku informāciju skatiet [Iestatīt sortimentus](set-up-assortments.md).

### <a name="example"></a>Paraugs

Klēpjdatora garantējamajai precei ir pamatcena $999, un ir divas klēpjdatora garantijas preces:

- 1.\_garantijai ir zemāka $500 robeža un augšējā $1000 robeža, **Cenas diapazona bāzes** lauks ir iestatīts uz **Pamatcenu**.
- 2.\_garantijai ir zemāka $1001 robeža un augšējā $2000 robeža, **Cenas diapazona bāzes** lauks ir iestatīts uz **Pamatcenu**.

Šādā gadījumā, kad klēpjdators ir pievienots debitora grozam, tiek parādīts piedāvājums pievienot 1.\_garantiju, kas tiek parādīta POS sistēmā, jo klēpjdatora cena ir starp apakšējo un augšējo 1.\_garantijas robežu.

> [!NOTE]
> Piemēram, ja vēlaties parādīt uzvednes gan 1.\_garantijai, gan 2.\_garantijai neatkarīgi no garantējamās preces cenas, iestatiet **Cenas diapazona bāzes** lauku uz **Nav**.

## <a name="configure-channel-specific-settings"></a>Konfigurēt kanālam raksturīgos iestatījumus

Ar kanālu saistīti iestatījumi ļauj jums norādīt, vai POS sistēmā tiek parādīts aicinājums pievienot garantijas preci, kad klienta grozam tiek pievienota garantējama prece.

Lai konfigurētu ar kanālu saistītos iestatījumus programmā Commerce, veiciet šādas darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Garantija \> Garantijas iestatījumi**.
1. Cilnē **Ar kanālu saistīti**, kas atrodas kolonnā **Uzvedne garantijai**, veiciet vienu no šīm darbībām:

    - Atzīmējiet izvēles rūtiņu, ja garantijas preces uzvednei ir jāparādās POS sistēmā, kad garantējamā prece ir pievienota grozam.
    - Notīriet izvēles rūtiņu, ja garantijas preces uzvednei nav jāparādās POS sistēmā, kad garantējamā prece ir pievienota grozam.

1. Palaidiet **1070** darbu, lai sinhronizētu datus kanālā.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigurējiet numuru sēriju garantijas politikām

Katru garantijas politiku unikāli identificē garantijas ierobežojuma numurs, ko ģenerējusi numuru sērija. Papildinformāciju par numuru sērijām skatiet nodaļā [Numuru sēriju pārskats](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Lai konfigurētu numuru sēriju garantijas politikām Commerce, veiciet šīs darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Garantija \> Garantijas iestatījumi**.
1. Cilnē **Numuru sērijas**, kas atrodas **Garantijas politikas** atsauces rindā, ievadiet vai atlasiet vērtību laukā **Numuru sērijas kods**.

## <a name="set-up-a-warranty-group"></a>Garantijas grupas iestatīšana

Garantijas grupa ir saistības starp garantijas precēm un garantējamajām precēm. POS izmanto garantijas grupas, lai noteiktu, kuras garantijas preces pārdošanas dalībniekiem ir jāpievieno, kad debitora grozam tiek pievienota garantējamā prece.

Lai iestatītu garantijas grupas piešķiri Commerce, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Garantija \> Garantijas grupas**.
1. Atlasiet **Jauns**, lai izveidotu garantijas grupu.
1. Laukā **Nosaukums** ievadiet jaunās grupas nosaukumu.
1. Kopsavilkuma cilnē **Vispārīgi** laukā **Apraksts** ievadiet grupas aprakstu.
1. Kopsavilkuma cilnē **Garantijas preces** atlasiet **Pievienot rindu**, lai pievienotu garantijas preci.
1. Laukā **Parādīt pasūtījumu** ievadiet skaitli, lai novērtētu garantijas grupu POS sistēmā. POS sistēma rādīs garantijas preces pieaugošā kārtībā garantijas uzvednē.
1. Kopsavilkuma cilnē **Garantējamās preces** atlasiet **Pievienot rindu**, lai pievienotu garantējamās preces.
1. Ja garantijas prece ir pielietojama visai garantējamo preču kategorijai, izvēlieties kategoriju laukā **Kategorija**. Ja garantijas prece ir pielietojama īpašai garantējamai precei, atlasiet preci laukā **Prece**.
1. Kopsavilkuma cilnē **Piemērotie kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu, kurā vēlaties pārdot garantijas preci.
1. Atlasiet **Saglabāt**, lai saglabātu konfigurāciju.
1. Atlasiet **Publicēt**, lai publicētu garantijas grupu.
1. Palaidiet **1040** darbu, lai sinhronizētu datus kanālā.

## <a name="sell-warranty-items-at-the-pos"></a>Pārdot garantijas preces POS sistēmā

Divas POS operācijas ļauj pārdošanas partneriem pārdot garantijas preces debitora pirkumiem darbplūsmas laikā:

- **Pievienot garantiju** - šī operācija izraisa uzvedni, kas parāda piemērojamās garantijas grozā atlasītajai garantējamajai precei.
- **Pievienot garantiju esošajai transakcijai** - šī operācija pārdošanas partneriem ļauj pārdod garantijas iepriekš pārdotajām garantējamajām precēm. Pārdošanas partneri var atrast sākotnējo darījumu garantējamajai precei, ievadot darījuma kvīts numuru.

Sekojošajā attēlā parādīts POS termināļa lapas piemērs ar uzvedni, lai pievienotu garantijas preci pašreizējam garantējamās preces pirkumam.

![Uzvednes piemērs, lai pašreizējam pirkumam pievienotu garantijas preci](./media/ew-sell-warranty.png)

Šajā ilustrācijā parādīts garantijas preces pievienošanas funkcijas piemērs garantējamajai precei, kas iepriekš tika pārdota.

![Garantijas preces pievienošanas funkcijas piemērs iepriekš pārdotai garantējamai precei](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Apstrādāt garantijas transakcijas

Kad garantijas tiek pārdotas skaidras nauda pārvadāšanas darījumos, pēc tam, kad transakcijas ir iegrāmatotas Commerce Headquarters, Commerce lietotāji var palaist **Procesa garantijas transakcijas** darbu, lai apstrādātu garantijas darbības un izveidotu garantijas noteikumus.

Lai apstrādātu garantijas darījumus programmā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Garantija \> Apstrādāt garantijas iestatījumus**.
1. Dialoglodziņā **Izvēlēties organizācijas mezglus** laukā **Organizācijas hierarhija** atlasiet vērtību.
1. Sarakstā **Pieejamie organizācijas mezgli** atlasiet vai nu atsevišķu veikalu, vai arī - ja vēlaties izveidot pakešuzdevumu veikalu grupai - mezglu.
1. Atlasiet labās bultiņas pogu, lai pievienotu izlasi sarakstam **Atlasītie organizācijas mezgli**.
1. Atlasiet cilni **Palaist fonā**.
1. Iestatiet **Partijas apstrādes** opciju uz **Jā** un pēc tam atlasiet **Periodiskums**.
1. Dialoglodziņā **Noteikt periodiskumu** laukā **Sākuma datums** atlasiet vai ievadiet periodiskuma sākuma datumu.
1. Laukā **Sākuma laiks** atlasiet vai ievadiet periodiskuma sākuma laiku.
1. Izpildiet kādu no norādītajām transakcijām.

    - Atlasiet opciju **Bez beigu datuma**, ja atkārtošanās nekad nav jāpārtrauc.
    - Atlasiet opciju **Beigt pēc**, ja atkārtošanās beigsies pēc noteikta laidienu skaita. Ja atlasāt šo opciju, ievadiet laidienu reižu skaitu.
    - Atlasiet opciju **Beigt līdz**, ja atkārtošanās jābeidz līdz konkrētam datumam. Ja atlasāt šo opciju, atlasiet vai ievadiet datumu.

1. Atlasiet **Labi**.
1. Atlasiet **Labi**.

## <a name="warranty-policies"></a>Garantijas politikas

Kad tiek pārdota paplašināta garantija, tiek automātiski izveidots garantijas politikas elements. Garantijas politikas numurus var koplietot ar debitoriem, lai tiem būtu atsauce uz iegādāto garantijas preci. Garantijas politiku rekvizītos ir ietverts garantijas derīguma sākuma datums un beigu datums, kā arī garantijas, noteikumu un nosacījumu sērijas numurs garantējamajai precei, kurai garantija tika pārdota.

> [!NOTE]
> Garantijas politikas rekvizīti tiek ģenerēti automātiski, kad tiek izveidotas garantijas politiku entītijas. Pašlaik tos nevar manuāli konfigurēt vai rediģēt.

Sekojošajā tabulā ir aprakstīti garantijas politikas rekvizīti un to vērtības. Commerce Headquarters datu bāzes tabulas nosaukums ir WARRANTYPOLICY.

| Rekvizīta nosaukums | Vērtība | apraksts |
|---------------|-------|-------------|
| PolicyNumber | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantijas politikas numurs |
| WarrantiedItemId | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantējamās preces ID |
| WarrantiedInventoryLotId | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantējamās preces krājuma laidiena ID |
| WarrantiedSerialNumber | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantējamās preces sērijas numurs |
| WarrantiedFulfilledDate | Datums | Garantējamās preces izpildes datums |
| WarrantyItemId | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantijas preces ID |
| WarrantyInventoryLotId | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Garantijas preces krājuma laidiena ID |
| WarrantySalesDate | Datums | Garantijas preces pārdošanas datums |
| WarrantyEffectiveDate | Datums | Garantijas politikas spēkā stāšanās datums |
| WarrantyExpirationDate | Datums | Garantijas politikas beigu datums |
| CustAccount | Rakstzīmju virkne (maksimāli 20 rakstzīmes) | Debitora konta numurs |
| Statuss | **Izveidots**, **Anulēts**, **Stājas spēkā** vai **Beidzies** | Garantijas politikas statuss |
| Piezīmes | Rakstzīmju virkne (maksimāli 255 rakstzīmes) | Piezīmes par garantijas politiku, piemēram, noteikumiem un nosacījumiem |

## <a name="frequently-asked-questions-faq"></a>Bieži uzdotie jautājumi (BUJ)

**Kāpēc es neredzu garantijas uzvedni POS sistēmā?**

Pārliecinieties, vai garantijas prece ir pievienota kanālam. Pārliecinieties, vai garantijas grupa ir konfigurēta tā, lai tā iekļautu atbilstošo kanālu.

**Kad mēģinu pievienot garantiju esošajai transakcijai un ievadīt debitora pasūtījuma saņemšanas numuru, kāpēc es neredzu nevienu transakcijas rindas vienību?**

Kvītis var atrast tikai tad, ja tiek palaists vilkšanas darbs (P-job), lai kvītis augšupielādētu Commerce Headquarters. Lai palaistu P-job, dodieties uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**, atlasiet **P-0001** darbu un pēc tam atlasiet **Palaist tūlīt**.

**Kāpēc garantijas līdzeklis ir piemērojams tikai sērijas precēm?**

Garantija ir pakalpojums, kas tiek sniegts konkrētai, unikālai precei. Dynamics 365 preci var unikāli identificēt tikai ar sērijas numuru.

## <a name="additional-resources"></a>Papildu resursi

[Mazumtirdzniecības preču iestatīšana](set-up-retail-products.md)

[Preču klāstu iestatīšana](set-up-assortments.md)

[Pārskats par numuru sērijām](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]