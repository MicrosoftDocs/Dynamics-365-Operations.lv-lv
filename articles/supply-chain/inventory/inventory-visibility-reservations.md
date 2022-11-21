---
title: Inventory Visibility rezervācijas
description: Šajā rakstā ir aprakstīts, kā iestatīt rezervēšanas līdzekli, lai izveidotu rezervācijas, patērētu rezervācijas un/vai rezervētu norādītos krājumu daudzumus, izmantojot krājumu redzamību.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762746"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility rezervācijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts tipisks vieglo rezervāciju lietošanas gadījums un paskaidrots, kā tās iestatīt sadaļā Krājumu pārskatāmība. Tas ietver informāciju par to, kā izveidot mīkstās rezervācijas, kompensēt tās pēc fiziskā patēriņa un pielāgot vai rezervēt norādītos krājumu daudzumus.

## <a name="sample-use-case-for-soft-reservation"></a>Lietošanas gadījuma paraugs mīkstajai rezervācijai

Mīkstās rezervācijas palīdz organizācijām sasniegt vienu patiesības avotu pieejamajiem krājumiem, it īpaši pasūtījuma izpildes procesā. Šī funkcionalitāte ir noderīga organizācijām, kurās pastāv šādi nosacījumi:

- Organizācijai ir vismaz divas dažādas sistēmas, kas tieši pieņem izejošos pasūtījumus.
- Organizācija ir ļoti stingra un vēlas novērst produktu krājumu dubultu rezervēšanu, kas var notikt, ja vairākas sistēmas spēj pārrezervēt pēdējo krājumu. Šī situācija tiek novērsta, kad visas pasūtījumu sistēmas var veikt tūlītējus mīkstās rezervēšanas API zvanus uz krājumu redzamību, kas nodrošina vienu patiesības avotu krājumu pieejamībai.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title=" Krājumu redzamības mīkstā rezervācija" width="720" />](media/inventory-visibility-soft-reservation.png)

Iepriekšējā attēlā ir parādīts, kā darbojas vienkāršā rezervēšana, un izceltas tālāk norādītās darbības.

- Jūsu sākotnējais krājumu līmenis tiek sinhronizēts ar Microsoft krājumu redzamību Dynamics 365 Supply Chain Management.
- Mīkstās rezervācijas tiek grāmatotas no katra jūsu pasūtījuma kanāla vai sistēmas sadaļā Krājumu redzamība. Krājumu redzamība validē krājumu pieejamību un mēģina veikt neierobežotu rezervāciju. Ja mīkstā rezervācija izdodas, krājumu redzamība papildina rezervēto daudzumu, atskaita no rezervēšanai pieejamā daudzuma (AFR) un atbild ar neierobežotu rezervācijas ID.
- Šajā laikā jūsu fiziskā inventāra daudzums paliek nemainīgs.
- Pēc tam varat sinhronizēt atsevišķus vai apkopotus mīkstie rezervētos pasūtījumus (pasūtījuma rindas) programmatūrā Supply Chain Management, lai veiktu stingrās rezervācijas un izlaistu preces noliktavā vai atjauninātu galīgo krājumu daudzumu.
- Varat iestatīt sistēmu, lai [tā kompensētu neobligātās rezervācijas](#offset-scm), kad piegādes ķēdes pārvaldībā tiek atjaunināti fiziskie krājumi.

Mīkstās rezervācijas parasti tiek izveidotas, patērētas un atceltas, izmantojot API zvanus uz krājumu redzamības pakalpojumu.

> [!NOTE]
> Pēc izvēles varat iestatīt Supply Chain Management (un citas trešo pušu sistēmas), lai automātiski kompensētu rezervēto daudzumu, izmantojot krājumu redzamību. Korespondējošais daudzums tiek dzēsts no rezervāciju ierakstiem Krājumu redzamībai.
>
> Pēc noklusējuma nobīdes funkcija tiek automātiski ieslēgta, kad iespējojat mīkstās rezervēšanas līdzekli.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Rezervācijas līdzekļa iespējošana un iestatīšana

Lai ieslēgtu šo līdzekli, veiciet tālāk minētās darbības.

1. Piesakieties Power Apps un atveriet **sadaļu Krājumu redzamība**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Līdzekļu pārvaldība** ieslēdziet līdzekli *OnHandReservation*.
1. Piesakieties savā Supply Chain Management vidē.
1. Dodieties uz **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietu un iespējojiet *Inventory Visibility integrāciju ar rezervācijas nobīdes* līdzekli (vajadzīga 10.0.22. vai jaunāka versija).
1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**, atveriet **Rezervāciju nobīdes** cilni un veiciet šādus iestatījumus:

    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervācijas nobīdes pārveidotājs** — atlasiet krājumu transakcijas statusu, kas kompensēs krājumu redzamībā veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Atlasiet vienu no šīm vērtībām:

        - *Pēc pasūtījuma* — pasūtījumi, kuriem ir *statuss Pēc pasūtījuma*, nosūtīs nobīdes pieprasījumu, kad tie tiks izveidoti. Kompensācijas daudzums būs izveidotā pasūtījuma (rindas) daudzums.
        - *Rezervēt* — pasūtījumi, kuriem ir Rezerves *statuss, nosūtīs* korespondējošu pieprasījumu, kad tie būs rezervēti vai fiziski rezervēti. Kad veicat nobīdi ar statusu Rezervēt *, pasūtījums nosūta nobīdes pieprasījumu pie jebkura jauna krājumu statusa, kas ir vistuvāk rezervētajam atlasītajam (piemēram,* komplektēšana, grāmatota pavadzīme vai izrakstīts rēķins). Šī problēma rodas pat tad, ja izlaižat rezervāciju programmatūrā Supply Chain Management un turpināt citu krājumu statusu (piemēram, ja pārejat no izlaišanas uz noliktavu, lai paņemtu un iepakotu). Pieprasījums tiks aktivizēts tikai vienu reizi. Ja tas ir aktivizēts izvēles brīdī, tas nedublē nobīdi, kad tiek publicēta pavadzīme. Kompensācijas daudzums būs tāds pats kā krājumu transakcijas statusa daudzums, kad tika aktivizēta nobīde (citiem vārdiem sakot, *rezervēts pasūtīts*/*rezerves fiziskais* vai vēlāks statuss atbilstošajā pasūtījuma rindā).

1. Pierakstieties atpakaļ programmā Krājumu redzamība, dodieties uz **lapu Konfigurācija** un pēc tam **cilnē Mīkstā rezervācija** pārskatiet noklusējuma mīksto rezervāciju hierarhiju. Ja nepieciešams, pievienojiet hierarhijai jaunas dimensijas.
1. **Sadaļā Iestatīt mīksto rezervāciju kartēšanu** skatiet noklusējuma iestatījumus. Pēc noklusējuma mīksti rezervētie krājumu daudzumi tiks reģistrēti pret `softreservephysical` datu avota `iv` fizisko mēru. Rezervētajai *rezervācijai* pieejamais aprēķinātais mērs tiek kartēts uz `availabletoreserve`. Ja vēlaties atjaunināt `availabletoreserve` aprēķināto mēru, dodieties uz **lapu Konfigurācija** un pēc tam **cilnē Aprēķinātais mērs** izvērsiet un modificējiet aprēķināto mēru.

Papildinformāciju skatiet sadaļā [Krājuma redzamības konfigurēšana](inventory-visibility-configuration.md).

> [!NOTE]
> Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tāpat kā indeksu hierarhija darbojas rīcībā esošiem vaicājumiem, taču tā tiek izmantota neatkarīgi, lai lietotāji varētu norādīt dimensiju detaļas un veikt precīzākas rezervācijas.
>
> Mīkstajā rezervāciju hierarhijā ir jābūt kā `SiteId``LocationId` komponentiem, jo tie veido krājumu redzamības nodalījuma konfigurāciju.

Papildinformāciju par rezervāciju konfigurēšanu skatiet rakstā [Rezervāciju konfigurācija](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Rezervācijas izmantošana Krājumu redzamības pievienojumprogrammai

Izsaucot rezervācijas API, sistēma atzīmē norādīto preču un daudzumu rezervāciju.

Tālāk ir sniegts scenārija piemērs un API vaicājuma pamatteksta paraugs. Uzņēmums Contoso pārdod produktu D0002 (kabinets) no savas e-komercijas tīmekļa vietnes. Klients, izmantojot vietni, veic neliela sarkana skapja pārdošanas pasūtījumu. Contoso nolemj izpildīt šo pasūtījumu, izmantojot tālāk norādītās dimensijas.

- Organizācijas ID = usmf
- Vietne = 1
- Noliktava = 11
- Produkts = D0002
- Krāsa = sarkana
- Izmērs = mazs

Contoso jau ir izveidojis API savienojumu ar krājumu redzamību no savas e-komercijas sistēmas. Kad pasūtījums ir saņemts, sistēma uzreiz aktivizē API zvanu, lai veiktu mīksto rezervāciju skapim inventāra redzamībā.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Izveidojiet vienkāršās rezervācijas, izmantojot rezervēšanas API

Rezervācijas tiek veiktas krājumu redzamības pakalpojumā, iesniedzot GRĀMATOŠANAS pieprasījumu pakalpojuma vietrāža URL, piemēram, `/api/environment/{environmentId}/onhand/reserve`.

Rezervēšanai pieprasījuma pamattekstam ir jāietver organizācijas ID, preces ID, rezervētie daudzumi un dimensijas.

Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

Ja vēlaties atcelt rezervāciju vai atsaukt konkrētu krājuma daudzumu rezervāciju, iestatiet daudzumu uz negatīvu vērtību, un iestatiet parametru `ifCheckAvailForReserv` uz vērtību `False`, lai izlaistu validāciju.

Tālāk ir sniegts pieprasījuma pamatteksta piemērs, kurā ir atsauce uz pārdošanas pasūtījumu iepriekšējā kontekstā.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Veiksmīgs neobligātās rezervācijas pieprasījums atgriež *mīkstās rezervācijas ID* katram rezervācijas ierakstam. Mīkstās rezervācijas ID nav unikāls identifikators atsevišķam nesaistošās rezervācijas ierakstam, bet gan produkta ID un dimensiju vērtību kombinācija, kas ir saistīta ar nesaistošo rezervācijas pieprasījumu. Jūs varat ierakstīt mīkstās rezervācijas ID pasūtījuma rindā, sinhronizējot veiksmīgi rezervētos pasūtījumus ar Supply Chain Management vai citu ERP sistēmu nobīdei.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a> Atviegloto rezervāciju kompensēšana piegādes ķēdes pārvaldībā

Jūs varat kompensēt mīksti rezervēto daudzumu pēc tam, kad pasūtījuma daudzums ir fiziski atskaitīts Supply Chain Management vai citā ERP sistēmā. Krājumu redzamība piedāvā iebūvētu vieglo rezervāciju nobīdes integrāciju ar Supply Chain Management.

Veiciet tālāk norādītās darbības, lai kompensētu neierobežoto rezervāciju.

1. Pierakstieties Supply Chain Management.
1. Pārejiet uz sadaļu **Pārdošanas un mārketinga pasūtījumi \> Visi pārdošanas pasūtījumi \>**.
1. Darbību rūtī atlasiet **Jauns**.
1. Atkārtoti izveidojiet ārējo pārdošanas pasūtījumu un pievienojiet pārdošanas rindu, kurā tiek izmantotas tieši tās pašas preces ID, organizācijas, vietas, noliktavas un dimensiju vērtības.
1. **Kopsavilkuma cilnē Pārdošanas pasūtījuma rindas** atlasiet tikko ievadīto pārdošanas rindu un pēc tam rīkjoslā atlasiet **Krājumu \> rezervācijas ID**.
1. Izpildiet kādu no šīm darbībām:

    - Nokopējiet mīkstās rezervācijas ID atbildē uz nesaistošo rezervācijas pieprasījumu un ielīmējiet to **laukā Rezervācijas ID**.
    - Atstājiet lauku Rezervācijas **ID** tukšu, bet atzīmējiet izvēles rūtiņu **Krājumu pakalpojuma automātiskā nobīde**. Sistēma automātiski noteiks, kuras preču un preču dimensijas kompensēt, pamatojoties uz atlasītajā rindā ievadīto krājuma ID un dimensiju vērtībām.

1. Atlasiet **Labi**.
1. Kamēr tā pati pārdošanas rinda joprojām ir atlasīta, fiziski rezervējiet pasūtīto daudzumu, kopsavilkuma cilnes Pārdošanas pasūtījuma rindas rīkjoslā **atlasot \> Krājumu** rezervācija **.**
1. Ja iepriekš esat iestatījis **lauka Rezervācijas nobīdes pārveidotājs** vērtību *Rezervēts, nobīde tiks aktivizēta, kad pasūtījuma rindas statuss* Rezervēt fizisko *vai* Rezervējums ir *pasūtīts*. Pakešuzdevums tiek izpildīts reizi minūtē, lai sinhronizētu nosūtīšanas pieprasījumus no piegādes ķēdes pārvaldības uz krājumu redzamību.

> [!NOTE]
> Transakciju statusiem, kas ietver noteiktu rezerves korespondences modifikatoru, transakcijas atjauninājums kompensēs atbilstošo rezervācijas ierakstu, ja būs izpildīti visi tālāk minētie nosacījumi.
>
> - Krājumu darījumā norādītais rezervācijas ID atbilst rezervācijas ID rezervācijas ierakstam sadaļā Krājumu pārskatāmība.
> - Krājumu transakcijas dimensijas atbilst rezervācijas ieraksta dimensijām sadaļā Krājumu pārskatāmība.
> - Krājumu darbību statusa izmaiņas izraisa korespondējošās darbības rezervācijām, ja krājuma darbības statuss atspoguļo faktu, ka pasūtījuma process ir pabeigts vai izlaists.

Korespondējošie daudzumi atbilst krājumu daudzumiem, kas ir norādīti attiecīgajās krājumu transakcijās. Nobīde stāsies spēkā tikai tad, ja rezervētais daudzums paliks krājumu redzamībā.

### <a name="cancel-or-revert-a-soft-reservation"></a>Mīkstās rezervācijas atcelšana vai atjaunošana

Ja sākotnējā pasūtījuma rinda tiek atcelta vai dzēsta un jums ir jāatgriež atbilstošā vienkāršā rezervācija, grāmatojiet negatīvu daudzumu, kura API vaicājuma pamattekstā ir tieši tāda pati informācija.
