---
title: Krājumu pozīcija
description: Šis raksts sniedz informāciju par stratēģisko krājumu pozicionēšanu, kas ietver atšifrēšanas punktu identificēšanu piegādes ķēdē, kur varat veidot rīcībā esošos krājumus, lai palīdzētu saspiešanu izpildes laikus un uzpildītu jūsu piegādes ķēdei.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689543"
---
# <a name="inventory-positioning"></a>Krājumu pozīcija

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Stratēģisko krājumu pozicionēšana ietver dekompozīcijas punktu identificēšanu piegādes ķēdē, kur varat veidot rīcībā esošos krājumus. Šī pieeja galvenokārt tiek lietota, lai palīdzētu saspiest izpildes laikus un darbojas jūsu piegādes ķēdē. Tas ļauj samazināt "whwhip ietekmi", jo pieprasījuma novirze nav visu veidu lejup piegādes ķēdei. *(neapstrādātā ietekme* attiecas uz to, kā neliela pieprasījuma svārstības mazumtirdzniecības līmenī var radīt progresīvi lielākas pieprasījuma svārstības vairumtirdzniecības, izplatītāja, ražotāja un izejmateriālu piegādātāju līmeņos.)

Krājumu pozicionēšana ir pirmais uz pieprasījumu orientēto materiālu resursu plānošanas solis (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Krājumu pozicionēšana ražošanai

Šajā sadaļā sniegts piemērs, kas parāda, kā pieņemt krājumu pozicionēšanas lēmumus, ja ražojam tipisko preces daudzumu. Rīcībā ir vairāklīmeņu materiālu komplekts (MK), kā parādīts šajā ilustrācijā.

![Piemērs par vairāku līmeņu materiālu komplektu (MK) precei.](media/ddmrp-bom-example.png "Piemērs vairāku līmeņu materiālu komplektam (MK) precei")

### <a name="choose-your-decoupling-points"></a>Dekompozīcijas punktu izvēle

Kad izvēlaties, kur novietot atšifrēšanas punktus, par kritēriju apsveriet visus tālāk norādītos MK krājumu aspektus:

- Ārējā novirze
- Krājumu līdzekļi un elastīgums
- Kritiskas operācijas aizsardzība
- Debitora tolerances laiks
- Pārdošanas pasūtījuma redzamības periods
- Tirgus potenciālais izpildes laiks

Ajā piemērā jūs varat novietot savu pirmo atšifrēšanas punktu *šim* apmaksām šādu iemeslu dēļ:

- Ir grūti avotam izveidot materiālu komplektus, un pieejamība ir sarežģīta. Tāpēc ir izpildīts *ārējā novirzes* kritērijs.
- Rēķina rēķinus var sadalīt daudzās un dažādās formās un izmēros, lai izveidotu nospraušanu citiem produktiem, kurus ražosit, papildus laicam. Tāpēc tiek izpildīts *krājumu sviru un* elastīguma kritērijs.

Pēc tam varat novietot nākamo atšifrēšanas punktu materiāla *komplektā*, kas ir iepriekš izgriezts auduma. Šo punktu varat izvēlēties, jo jums ir tikai viena materiāla griešanas iekārta. Tāpēc ir izpildīts *kritiskās operācijas* aizsardzības kritērijs.

Visbeidzot, iespējams, esat norādījis pēdējo atšifrēšanas punktu pabeigtajam preču krājumam. Jūs variet izvēlēties šo punktu, jo jums ir ļoti zems *debitoru tolerances* laiks pārdošanai un tādēļ, ka pārdošanas *pasūtījuma redzamības periods ir* diezgan īss. Tāpēc vēlaties nodrošināt, lai rīcībā esošie krājumi atbilstu ienākošajiem pasūtījumiem. Varat arī iestatīt augstāku cenu, uzturot izpildes laiku šo īsu, kas ir tas *, uz ko attiecas tirgus potenciālā izpildes* laika kritērijs.

Balstoties uz šo analīzi, šajā ilustrācijā parādīts, kā izskatīsies mk mk. Dzelteni krājumu simboli iezīmē atšifrēšanas punktus.

![MK piemērs ar iezīmētiem dekompozīcijas punktiem.](media/ddmrp-bom-decoupling-example.png "MK piemērs ar iezīmētiem dekompozīcijas punktiem")

### <a name="calculate-your-decoupled-lead-time"></a>Dekompozīcijas izpildes laika aprēķins

Šī sadaļa parāda, kā aprēķināt jaunos izpildes laikus pēc dekompozīcijas punktu lietošanas.

Tālāk sniegtajā attēlā par piemērām, kas tika sākts iepriekšējā sadaļā, izpildes laiki tiek rādīti pelēkos lodziņos katra MK komponenta augšējā kreisajā daļā. Lodziņi, kuriem ir sarkana izklāsta, norāda elementus, kas vada kopīgo izpildes laiku (visie garāko izpildes laiku summa katrā MK līmenī). Šis izpildes laiks ir 21 diena, kad sākat no jauna.

![MK piemērs ar izpildes laikiem.](media/ddmrp-bom-lead-times-example.png "MK piemērs ar izpildes laikiem")

Tomēr, ja tiek pielietoti iepriekš izvēlētie atšifrēšanas punkti, dekompozīcijas krājumi vienmēr būs noliktavā. Līdz ar to izpildes laiks būs 0 (nulle). Tagad no 0 līdz 5 dienām ir pienācis jauns izpildes laiks: divas dienas pavediena pirkšanai un trīs dienas krājumu ražošanai. Šis izpildes laiks ir zināms kā dekompozīcijas *izpildes laiks*.

![Dekompozīcijas izpildes laika piemērs.](media/ddmrp-bom-decoupled-lead-time-example.png "Dekompozīcijas izpildes laika piemērs")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Stratēģisko krājumu pozicionēšana mazumtirdzniecības modelī

Tā kā mazumtirgotāji var tikai pabeigtās preces, MK netiek izdoti. Tomēr mazumtirgotāji joprojām var izmantot DDMRP, iestatot stratēģisko krājumu pozicionēšanu un bufera līmeņus, pamatojoties uz uzglabāšanas vietām sadales tīklā.

Šajā attēlā parādīts piemērs par uzņēmumu, kam ir sadales centrs Sietlā un veikaliEm Atsietā, Atvasē un Ejotā.

![Dekompozīcijas punkti, balstoties uz novietojumu mazumtirdzniecības modelī.](media/ddmrp-retail-decoupl-points-example.png "Atšifrēšanas punkti, balstoties uz novietojumu mazumtirdzniecības modelī")

Var izlemt, ka pārsūtīšanas laiks, lai pārvietotu virsproduktu starp sadales centru un veikaliem, ir pretrunā ar klientu tolerances *laiku*, jo debitori plāno, ka virspasūtījumi būs noliktavā, kad viņi apmeklēs. Šajā gadījumā katrā no trim veikaliem iestatīsiet atšifrēšanas punktu virs precei. Katram veikalam būs dažādi bufera līmeņi, balstoties uz tā izpildes laikiem, pieprasījumu modeļiem un tā tālāk.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Ieviest krājumu pozicionēšanu Dynamics 365 Supply Chain Management

Šajā sadaļā ir aprakstīts, kā ieviest jūsu krājumu pozicionēšanas stratēģiju sistēmā Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Iestatīt krājumu vajadzību grupas, kas izveido dekompilēšanas punktus

Krājumi kļūst dekompozīcijas punkti, ja tie **pieder** nodrošinājuma grupai, kas ir konfigurēta ar dekomupēšanas *punkta seguma koda vērtību*. Tāpēc pirmais solis DDMRP iestatīšanas procesā ir izlemt, kuras vajadzības grupas ir jāievieš savā DDMRP stratēģijai, un tad izveidot tās, izpildot šos soļus.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Segums \> Saguma grupas**.
1. Lai izveidotu vajadzību grupu, **darbību rūtī** atlasiet Jauns.
1. Ievadiet informāciju, kas identificē vajadzību grupu, un pēc tam atlasiet kalendāru, ko lietot.
1. Cilnē Vispārīgi **iestatiet** seguma koda lauku **uz** Dekompozīcijas *punktu*. Šis iestatījums izraisīs to, ka visi krājumi, kas pieder šai vajadzību grupai, tiks uzskatīti par dekompozīcijas punktiem par DDMRP. Tas iespējo arī visus DDMRP iestatījumus šai grupai, kā aprakstīts tālāk šajā procedūrā.
1. Cilnes Citi **sadaļā** **DDMRP parametri** iestatiet šādus laukus:

    - **Izpildes laika koeficients** – norādiet koeficientu (kā decimālskaitļa vērtību no 0 līdz 1), lai kontrolētu ietekmi, kādai vajadzētu būt izpildes laikam, kad minimālie un maksimālie krājumu līmeņi tiek aprēķināti krājumiem šajā vajadzības grupā. Parasti, jo ilgāks ir krājuma izpildes laiks, jo mazāks būs tā izpildes laika koeficients. Zemākais izpildes laika koeficients rada mazāku minimālo un maksimālo krājumu līmeni, tāpēc tas rada mazākus un biežākus pasūtījumus. DDMRP metodoloģija iesaka vērtību no 0,20 līdz 0,40 krājumiem, kam ir ilgs izpildes laiks, no 0,41 līdz 0,60 krājumiem ar vidēja izpildes laiku, un no 0,61 līdz 1,00 krājumiem ar īstermiņa izpildes laiku. Papildinformāciju skatiet sadaļā Bufera [profils un līmeņi](ddmrp-buffer-profile-and-levels.md).
    - **Novirzes koeficients** – norādiet koeficientu (kā decimālskaitļa vērtību no 0 līdz 1), lai kontrolētu ietekmi, kādai dažādu pieprasījumu gadījumā ir jāaprēķina krājumu minimums, kas tiek aprēķināts šīs vajadzības grupas krājumiem. Parasti, jo lielāks ir krājuma pieprasījums, jābūt augstākam tā novirzes faktoram. Augstāka novirzes koeficients rada lielāku minimālo krājumu līmeni. DDMRP metodoloģija iesaka vērtību no 0,00 līdz 0,40 krājumiem ar zemu novirzību starp 0,41 un 0,60 krājumiem ar vidēju novirzību, un no 0,61 līdz 1,00 krājumiem ar augstu noviržu. Papildinformāciju skatiet sadaļā Bufera [profils un līmeņi](ddmrp-buffer-profile-and-levels.md).
    - **Min., maksimālais un atkārtota pasūtījuma punktu periods** – norādiet, cik bieži aprēķināt bufera vērtības (katru *dienu* vai *katru nedēļu*).

1. **Cilnes Cits** sadaļā Dienas vidējā izmantošana **iestatiet** šādus laukus:

    - **Vidējā dienas lietošana, pamatojoties** uz – atlasiet, uz kuriem laika periodiem balstīts vidējās dienas lietošanas (ADU) aprēķins. Atlasiet vienu no šīm vērtībām:

        - *Pagātne* – skatiet tikai pagātnes izmantošanas dienu skaitu, kas **norādītas laukā Pagātnes periods (** dienas). ADU tiek aprēķināts, kā kopējais krājuma pieprasījums aprēķina periodā (krājumu vienībās), kas dalīts ar dienu skaitu aprēķina periodā.
        - *Uz* priekšu – skatiet tikai prognozēto turpmāko izmantošanu (iekļaujot prognozes) **dienu skaitam, kas norādīts laukā Uz priekšu periods (** dienas). ADU tiek aprēķināts, kā kopējais krājuma pieprasījums aprēķina periodā (krājumu vienībās), kas dalīts ar dienu skaitu aprēķina periodā. 
        - *Jaukts* – aplūkojiet gan pagātnes, gan turpmākās lietošanas. Iestatījumi laukam **Pagātnes periods (** dienas), laukam **Uz priekšu periods (dienas)** un jaukšanas opcijām tiek lietotas visas. 

            *Jaukts ADU* = (\[*Pagātnes* svara × *ADU*\] + \[*uz* priekšu svēršanas × *Uz priekšu ADU*\]) ÷ (*·* + *Pagātnes svars Uz priekšu svēršanu)*

    - **Pagātnes periods (dienas)** – ievadiet pagājušo dienu skaitu (līdz un ieskaitot šodienu), ko sistēmai būtu jāņem vērā, aprēķinot šīs vajadzības grupas krājumu ADU. Šis iestatījums tiek lietots tikai tad, ja **vidējā ikdienas lietojums**, pamatojoties uz lauku, ir iestatīts uz *Ielīmēts* vai *Jaukts*.
    - **Uz priekšu periods (dienas)** – ievadiet turpmāko dienu skaitu (no šodienas līdz norādītajai dienai), ko sistēmai būtu jāņem vērā, kad tā aprēķina krājumu ADU šajā vajadzības grupā. Šis iestatījums tiek lietots tikai tad, ja **vidējā ikdienas lietojums**, pamatojoties uz lauku, ir iestatīts uz *Uz* priekšu vai *Jaukts*.
    - **Iepriekšējā perioda relatīvais** svars jauktai vidējai ikdienas izmantošanai – ievadiet svaru (procentos), ko piemērot pagātnes periodam, kad tiek aprēķināts jauktais ADU. Šis iestatījums tiek lietots tikai tad, ja **vidējais ikdienas lietojums, pamatojoties** uz lauku, ir iestatīts uz *Jaukts*.
    - **Uz priekšuvērstā perioda** relatīvais svars jauktai vidējai ikdienas izmantošanai – ievadiet svaru (kā procentus), ko piemērot uz priekšu periodu, kad tiek aprēķināts jauktais ADU. Šis iestatījums tiek lietots tikai tad, ja **vidējais ikdienas lietojums, pamatojoties** uz lauku, ir iestatīts uz *Jaukts*.

1. Visām citām cilnēm un laukiem ievadiet detalizētus iestatījumus, kas tiek lietoti, lai aprēķinātu vajadzības krājumiem, kas saistīti ar šo vajadzību grupu.

### <a name="set-an-item-as-a-decoupling-point"></a>Krājuma kā atšifrēšanas punkta iestatīšana

Lai iestatītu elementu kā dekompozīcijas punktu, veiciet šādas darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atrodiet un atlasiet izlaisto krājumu, ko vēlaties iestatīt DDMRP.
1. Darbību rūts cilnē Plāns **atlasiet** Krājumu **vajadzība**.
1. Krājumu vajadzību **lapā,** iespējams, ir jau uzskaitīti vairāki krājumu vajadzības ieraksti, katrs no tiem attiecas uz citu glabāšanas un preču dimensiju kombināciju. Varat atlasīt esošu krājuma nodrošinājuma ierakstu, kas attiecas uz dimensijām, kurās vēlaties izveidot dekompozīcijas punktu. Alternatīvi Darbību rūtī varat **atlasīt** Jauns, lai izveidotu jaunu krājumu vajadzības ierakstu.
1. Iestatiet krājumu vajadzības ierakstu kā parasti. Ir jānorāda vismaz vieta un noliktava, kur tiks lietots dekompozīcijas punkts.
1. Kamēr vēl ir atlasīts atbilstošais ieraksts, atlasiet cilni **Vispārīgi**.
1. Atzīmējiet **izvēles rūtiņu Izmantot noteiktus** iestatījumus.
1. Iestatiet vajadzību **grupas lauku** nodrošinājuma grupai, kas iestatīta atšifrēšanas punktu veidojiet (kā aprakstīts iepriekšējā sadaļā).
1. Krājums tagad ir konfigurēts kā dekompozīcijas punkts. Parasti, ja lietojat DDMRP, šeit konfigurēsiet arī iestatījumus, kas ietekmē bufera izmērus un pārkārtoto daudzumu. Tomēr varat pabeigt šo konfigurāciju vēlāk. Papildinformāciju par iestatījumiem skatiet [šeit: Buferu iestatīšana atšifrēšanas punkta vienumam](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Lai plānotu krājumus, kas nav dekompozīcijas punkti, rīkojieties tāpat, kā lietojot standarta materiālu prasību plānošanu (MRP).
