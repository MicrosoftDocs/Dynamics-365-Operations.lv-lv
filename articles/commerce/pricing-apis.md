---
title: Commerce pricing API
description: Šajā rakstā ir aprakstīti dažādi cenu noteikšanas API, ko nodrošina cenu Microsoft Dynamics 365 Commerce noteikšanas programma.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293653"
---
# <a name="commerce-pricing-apis"></a>Commerce pricing API

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti dažādi cenu noteikšanas API, ko nodrošina cenu Microsoft Dynamics 365 Commerce noteikšanas programma.

Cenu Dynamics 365 Commerce noteikšanas programma nodrošina tālāk norādītos Retail Server API, kurus var patērēt ārējās programmas, lai atbalstītu dažādus cenu noteikšanas scenārijus.

- **GetActivePrices** - Šis API iegūst preces aprēķināto cenu, tai skaitā vienkāršas atlaides.
- **CalculateSalesDocument** — šis API aprēķina preču cenas un atlaides par piešķirtajiem daudzumiem, ja tie tiek pirkti kopā.
- **GetAvailablePromotions** — šis API saņem piemērojamas atlaides precēm grozā. 
- **AddCoupons** - šis API pievieno kuponus grozam.
- **RemoveCoupons** — šis API noņem kuponus no groza.

Papildinformāciju par to, kā patērēt Retail Server API ārējās programmās, skatiet sadaļā [Retail Server API patērēšanu ārējās programmās](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>IegūtActivePrices

API *GetActivePrices tika ieviests* Commerce versijā 10.0.4 laidienā. Šis API iegūst preces aprēķināto cenu, ieskaitot vienkāršas atlaides. Tā neaprēķina daudzrindu atlaides, un tiek pieņemts, ka katram produktam API pieprasījumā ir daudzums 1. Šis API var arī paņemt produktu sarakstu kā ievadi un pieprasīt atsevišķu produktu lielapjoma cenu.

GetActivePrices API atbalsta lomas *Darbinieks*,**Debitors**, **Anonīms** **un** Application Commerce.**·**

Galvenais lietošanas *gadījums GetActivePrices* API ir preču informācijas lapa (PDP), kur mazumtirgotāji vēlas uzrādīt preces labāko cenu, ieskaitot visas faktiskās atlaides.

Tabulā ir parādīti API *GetActivePrices ievades* parametri.

| Vārds/nosaukums                                    | Apakškods | Veids | Pieprasīta/Nav obligāta | Apraksts |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Obligāti | |
|                                         | ChannelId | Ilgi | Obligāti | |
|                                         | CatalogId | Ilgi | Obligāti | |
| productIds                              | | Uzkrājams\<long\> | Obligāti | Preču saraksts cenu jāaprēķina. |
| activeDate(a)                              | | DateTimeOffset | Obligāti | Datums, kad tiek aprēķinātas cenas. |
| Customerid                              | | virkne | Neobligāti | Debitora konta numurs. |
| piederībaLoyaltyTiers                 | | Uzkrājams\<AffiliationLoyaltyTier\> | Neobligāti | Piederības un lojalitātes programmas pakāpes. |
|                                         | Piederības Id | Ilgi | Obligāti | Piederības ID. |
|                                         | Lojalitātes programmasTierId | Ilgi | Neobligāti | Lojalitātes programmas pakāpes ID. |
| includeSimpleDiscountsInContextualPrice | | Būla (Bool) | Neobligāti | Iestatiet šo parametru kā **patiesu**, lai cenu noteikšanā iekļautu vienkāršas atlaides. Noklusējuma vērtība ir **false**. |
| includeVariantPriceRange                | | Būla (Bool) | Neobligāti | Iestatiet šo parametru kā **patiesu,** lai iegūtu minimālās un maksimālās cenas starp visiem šablona preces variantiem. Noklusējuma vērtība ir **false**. |
| includeAttainablePricesAndDiscounts     | | Būla (Bool) | Neobligāti | Iestatiet šo parametru kā **patiesu,** lai iegūtu sasniegtās cenas un atlaides. Noklusējuma vērtība ir **false**. |

**Pieprasījuma pamatteksta paraugs**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Atbildes pamatteksts paraugs**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>AprēķinātpārdošanasDokuments

Api *CalculateSalesDocument* tika ieviests Commerce versijā 10.0.25 laidienā. Šis API aprēķina cenas un atlaides precēm ar noteiktu daudzumu, ja tās tiek pirktas kopā pasūtījumā. Cenu aprēķināšana aiz *CalculateSalesDocument* API ņem vērā gan vienas rindas atlaides, gan vairāku rindu atlaides.

*Api CalculateSalesDocument* galvenais lietošanas gadījums ir cenu noteikšana scenārijos, kuros nepastāv pilns groza konteksts (piemēram, pārdošanas piedāvājumi). Šajā lietošanas gadījumā var izmantot arī pārdošanas punkta (POS) un komercijas e-komercijas scenārijus. Zemāka kopējā cena, kad groza krājumi tiek aprēķināti kā kopums (piemēram, diskrētiem saišķus, saistītajām vai ietiktajām precēm, vai precēm, kas jau ir pievienotas grozam), var piesaistīt produktus grozam.

Data Model gan CalculateSalesDocument *API* pieprasījumam, gan atbildei ir **Grozs**. Tomēr šī API kontekstā datu modelis tiek nosaukts par **SalesDocument**. Tā kā lielākā daļa rekvizītu ir izvēles, un tikai daži no tiem ietekmē cenu aprēķinu, tikai ar cenu noteikšanu saistītie lauki ir parādīti tālāk esošajā tabulā. Nav ieteicams API pieprasījumā iesaistīt nevienu citu lauku.

*API CalculateSalesDocument sfēra* ir tikai cenu un atlaižu aprēķins. Nav iesaistīti nodokļi un maksas.

Tabulā ir parādīti ievades parametri objektā ar nosaukumu **salesDocument**.

| Vārds/nosaukums             | Apakškods | Veids | Pieprasīta/Nav obligāta | Apraksts |
|------------------|----------|------|-------------------|-------------|
| ID               | | virkne | Obligāti | Pārdošanas dokumenta identifikators. |
| CartLines        | | IList (IList)\<CartLine\> | Neobligāti | Rindu saraksts, kurām jāaprēķina cenas un atlaides. |
|                  | Preces ID | Ilgi | Nepieciešams CartLine darbības jomai | Preces ieraksta ID. |
|                  | ItemId | virkne | Neobligāti | Krājuma identifikators. Ja tiek nodrošināta vērtība, tai ir jāatbilst **ProductId parametra vērtībai**. |
|                  | Krājumu dimensijasId | virkne | Neobligāti | Krājumu dimensijas identifikators. Ja ir nodrošināta vērtība, **ItemId** **un InventoryDimensionId** vērtību **kombinācijai ir jāatbilst ProductId parametra vērtībai**. |
|                  | Daudzums | Decimāldaļas | Nepieciešams CartLine darbības jomai | Preces daudzums. |
|                  | UnitOfMeasureSymbol | virkne | Neobligāti | Preces vienība. Pēc noklusējuma, ja vērtība nav norādīta, API izmanto preces pārdošanas vienību. |
| CustomerId       | | virkne | Neobligāti | Debitora konta numurs. |
| Lojalitātes programmasCardId    | | virkne | Neobligāti | Lojalitātes programmas kartes identifikators. Jebkuram debitora kontam, kas ir saistīts ar **lojalitātes programmas karti, ir jāatbilst CustomerId** parametra vērtībai (ja tā tiek sniegta). Lojalitātes programmas karte netiks apsvērta, ja tā nav atrasta vai tās statuss ir **Bloķēts**. |
| Piederības līnijas | | IList (IList)\<AffiliationLoyaltyTier\> | Neobligāti | Piederības lojalitātes programmas pakāpes rindas. Ja **tiek nodrošinātas CustomerId** un/ **vai LoyaltyCardId** vērtības, **atbilstošās piederības lojalitātes programmas pakāpes rindas tiks sapludinātas ar rindām, kas ir noteiktas AffiliationLines** vērtībā. |
|                  | Piederības Id | Ilgi | Nepieciešams AffiliationLoyaltyTier sfērai | Piederības ieraksta ID. |
|                  | Lojalitātes programmasTierId | Ilgi | Nepieciešams AffiliationLoyaltyTier sfērai | Lojalitātes programmas pakāpes ieraksta ID. |
|                  | PiederībasTypeValue | Tiešais | Nepieciešams AffiliationLoyaltyTier sfērai | Vērtība, kas norāda, vai piederības rindas tips ir **Vispārīgi** (**0**) vai Lojalitātes **programmas** veids (**1**). Ja šis parametrs ir iestatīts **uz 0**, API **izmanto vērtību AffiliationId** kā identifikatoru un ignorē vērtību LoyaltyTierId **.** Ja api ir iestatīts **uz** 1 **,** tas izmanto vērtību LoyaltyTierId **kā identifikatoru un ignorē vērtību AffiliationId**. |
|                  | Iemesla koda līnijas | Iekasēšana\<ReasonCodeLine\> | Nepieciešams AffiliationLoyaltyTier sfērai | Iemesla koda rindas Šis parametrs neietekmē cenu aprēķinu, bet tas ir nepieciešams **kā daļa no objekta AffiliationLoyaltyTier**. |
|                  | CustomerId | virkne | Nepieciešams AffiliationLoyaltyTier sfērai | Debitora konta numurs. |
| Kuponi          | | IList (IList)\<Coupon\> | Neobligāti | Kuponi, kas nav piemērojami (neaktīvi, kuriem beidzies derīguma termiņš vai nav atrasti), netiks apsvērti cenu aprēķinā. |
|                  | Kods | virkne | Nepieciešams kupona darbības jomai | Kupona kods. |
|                  | CodeId (Koda ID) | virkne | Neobligāti | Kupona koda identifikators Ja tiek nodrošināta vērtība, tai ir jāatbilst koda parametra **vērtībai**. |
|                  | DiscountOfferId | virkne | Neobligāti | Atlaides identifikators. Ja tiek nodrošināta vērtība, tai ir jāatbilst koda parametra **vērtībai**. |

**Pieprasījuma pamatteksta paraugs**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Viss groza objekts tiek atgriezts kā atbildes pamatteksts. Lai pārbaudītu cenas un atlaides, jāfokusē uz laukiem šajā tabulā.

| Vārds/nosaukums           | Apakškods | Veids | Apraksts |
|----------------|----------|------|--------------|
| NetPrice (Neto Cena)       | | Decimāldaļas | Visa pārdošanas dokumenta neto cena pirms atlaižu lietošanas. |
| DiscountAmount</a1 | | Decimāldaļas | Visa pārdošanas dokumenta kopējā atlaides summa. |
| TotalAmount</a1    | | Decimāldaļas | Visa pārdošanas dokumenta kopsumma. |
| CartLines      | | IList (IList)\<CartLine\> | Aprēķinātās rindas, kurās iekļauta detalizēta informācija par cenu un atlaidēm. |
|                | Cena | Decimāldaļas | Preces vienības cena. |
|                | NetPrice (Neto Cena) | Decimāldaļas | Rindas neto cena pirms atlaižu lietošanas (= *cenas*&times;*daudzums).* |
|                | DiscountAmount</a1 | Decimāldaļas | Atlaides summa. |
|                | TotalAmount</a1 | Decimāldaļas | Rindas gala kopējās cenu noteikšanas rezultāts. |
|                | Cenu līnijas | IList (IList)\<PriceLine\> | Detalizēta informācija par cenu, ieskaitot cenas avotu (pamatcena, cenas korekcija vai tirdzniecības līgums) un summu. |
|                | Atlaižu rindas | IList (IList)\<DiscountLine\> | Atlaides informācija. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Ņemot vērā grozu ar vairākām groza rindām, *GETAvailablePromotions* API atgriež visas piemērojamās groza rindu atlaides. 

Galvenais lietošanas gadījums *API getAvailablePromotions* ir grozu lapa, kur mazumtirgotāji vēlas rādīt piemērotās atlaides vai pieejamos kuponus pašreizējam grozam.

Tabulā ir parādīti API *GetAvailablePromotions ievades* parametri.

| Vārds/nosaukums        | Veids | Pieprasīta/Nav obligāta | Apraksts |
|-------------|------|-------------------|-------------|
| atslēga         | virkne | Obligāti | Groza ID. |
| cartLineIds | Uzkrājams\<string\> | Neobligāti | Iestatiet šo parametru, lai atgrieztu atlaides tikai atlasītajām groza rindām. |

**Atbildes pamatteksts paraugs**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons* API atbalsta kuponu saraksta pievienošanu grozam. Tas atgriež groza objektu pēc kuponu pievienošanas.

Tabulā ir parādīti *AddCoupons API ievades* parametri.

| Vārds/nosaukums                 | Veids | Pieprasīta/Nav obligāta | Apraksts |
|----------------------|------|-------------------|-------------|
| atslēga                  | virkne | Obligāti | Groza ID. |
| couponCodes          | Uzkrājams\<string\> | Obligāti | Grozam pievienojamie kuponu kodi |
| isLegacyDiscountCode | Būla (Bool) | Neobligāti | Iestatiet šo parametru kā patiesu **,** lai norādītu, ka kupons ir mantojuma atlaides kods. Noklusējuma vērtība ir **false**. |

## <a name="removecoupons"></a>RemoveCoupons

*API RemoveCoupons* atbalsta kuponu saraksta noņemšanu no groza. Tas atgriež groza objektu pēc kuponu noņemšanas.

Šajā tabulā ir parādīti RemoveCoupons *API ievades* parametri.

| Vārds/nosaukums        | Veids | Pieprasīta/Nav obligāta | Apraksts |
|-------------|------|-------------------|-------------|
| atslēga         | virkne | Obligāti | Groza ID. |
| couponCodes | Uzkrājams\<string\> | Obligāti | No groza izņemamo kuponu kodi |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
