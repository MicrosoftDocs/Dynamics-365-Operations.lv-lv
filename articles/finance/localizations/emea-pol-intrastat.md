---
title: Poļu Intrastat
description: Šajā tēmā iekļauta informācija par Intrastat pārskatiem Polijai.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: 9564892f768adb8f48208fe10b31c7c6392a4567
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779911"
---
# <a name="polish-intrastat"></a>Poļu Intrastat

[!include[banner](../includes/banner.md)]

Lapa **Intrastat** tiek izmantota, lai veidotu un paziņotu informāciju par tirdzniecību starp Eiropas Savienības (ES) valstīm. Polijas Intrastat deklarācija satur informāciju par preču tirdzniecību pārskatiem.

Šie lauki ir iekļauti Polijas Intrastat deklarācijā. Visi lauki ir iekļauti ierodas un izsūtījumos, izņemot **RodzajTransportu (transportēšanas režīmu) un** NosūtīšanasPochodzeliz (izcelsmes valsti vai reģionu), kas nav ietverti nosūtīšanā, un **·** **IdKontrahenta (debitora ārzemju PVN numurs), kas** nav iekļauts ierodas.

| Lauka nosaukums | Apraksts |
|-------------------------|-------------------------|
| Deklaracja dati | Dokumenta izveides datums. |
| Miesiac | Deklarācijas atsauces mēnesis. |
| Ierašanās tiesības | Deklarācijas atsauces gads. |
| Numurs | Deklarācijas numurs atsauces periodā. |
| Versa | Deklarācijas versijas numurs. |
| Laukuts NrWlas saskaņā ar | Deklarācijas identifikators. Vērtība tiek ģenerēta automātiski. |
| Darba tips | Pārskata virziens.</br><li>Saņemšanas gadījumā tiek drukāts "P".</li><li>Nosūtīšanai tiek drukāts "W".</li> |
| Rodzaj (Rodzaj) | Deklarācijas tips. Šī vērtība norāda, vai pārskats ir sākotnējā deklarācija vai labojuma deklarācija. |
| Darba VIETU NOD. | Vienības kods, uz kuru attiecas Intrastat deklarācija. Vērtība ir norādīta PVN **reģistrācijas numura** laukā PVN sadaļas Aģents lapā Ārējās tirdzniecības **·** **·** **·** parametri. |
| Nazwa (Nazwa) | Uzņēmuma nosaukums. |
| Miejsclicasc, UlicaNumer, KodPocztett | Juridiskās personas pilna adrese. |
| Nip | Polijas nodokļa identifikācijas numurs (pievienotās vērtības nodoklis [PVN] ID). |
| Regona (Regon) | Polijas statistiskās identifikācijas numurs (uzņēmuma numurs). |
| LacznaWartoscFaktur ; | Rēķinu vērtību summa. |
| LacznaWartoscStatystyczna | Statistisko vērtību summa. |
| LacznaLiczbaPo papildmaksas | Preču krājumu kopējais skaits. |
| PozId (PozId) | Secīgais dotā preču krājuma numurs. |
| OpisTowaru (opisTowaru) | Preces tirdzniecības nosaukums. |
| Nešopochodze ne, Unikos, Ne uz koki | Starptautiskais standartizācijas organizācijas (International Organization for Standardization – ISO) kods, kas ir paredzēts partnera valstij vai reģionam. |
| Karakidostas | Intrastat kods piegādes nosacījumiem. |
| RodzajTransakcji | Kods, kas norāda darbības raksturu. Polijas uzņēmumi izmanto divciparu darbību kodus. |
| KodTowar arī | Astoņciparu preces kods atbilstoši kombinētajām aprakstam. |
| RodzajTransportu | Transportēšanas veida Intrastat kods. |
| Nešopochodze saskaņā ar | Valsts vai reģiona, kur preces tika ražotas vai saražotas, ISO kods. |
| MasaNetto | Neto masa pilnos kilogramos. |
| IloscUzupelhonjacaJm | Daudzums papildu mērvienībās veselos skaitļos. |
| Ierašanās un spēcFaktury | Visu ar vienu krājumu segto darbību rēķina vērtība. |
| BratoscStatystyczna | Statistiskā vērtība. |
| Darba kļūda: NazwiskoImie, Telefon, Fakss, E-pasts | Tās personas vārds un uzvārds, tālruņa numurs, faksa numurs un e-pasta adrese, kas iesniedz deklarāciju. |
| IdKontrahenta (IdKontrahenta) | Debitora ārzemju PVN numurs ES dalībvalstī. |


## <a name="set-up-intrastat"></a>Iestatīt Intrastat

No globālā repozitorija importējiet elektronisko pārskatu (ER) konfigurāciju jaunāko versiju:

   - Intrastat modelis
   - Intrastat pārskats
   - Intrastat (PL)

Plašāka informācija pieejama rakstā [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Iestatiet sava uzņēmuma PVN ID un uzņēmuma numuru.

### <a name="create-registration-types-for-company-codes"></a>Izveidot uzņēmumu kodu reģistrācijas tipus

Uzņēmuma kodiem ir jāizveido divi reģistrācijas tipi: viens PVN ID (NIP kods) un viens uzņēmuma numuram (Regon kods).

1. Dodieties uz **organizācijas** > **administrēšanas globālās adrešu** > **grāmatas reģistrācijas tipu reģistrācijas** > **·** tipiem.
2. Darbību rūtī atlasiet Jauns, **lai izveidotu PVN ID reģistrācijas** tipu.
3. Dialoglodziņā **Ievadīt reģistrācijas veida** detaļas laukā **Nosaukums** ievadiet jaunā reģistrācijas tipa nosaukumu. Piemēram, ievadiet **·** NRN.
4. Laukā **Valsts/reģions** atlasiet **POL**.
5. Atlasiet **Izveidot**.
6. Darbību rūtī atlasiet Jauns, **lai izveidotu uzņēmuma numura reģistrācijas** tipu.
7. Dialoglodziņā **Ievadīt reģistrācijas veida** detaļas laukā **Nosaukums** ievadiet jaunā reģistrācijas tipa nosaukumu. Piemēram, ievadiet **·** Regon.
8. Laukā **Valsts/reģions** atlasiet **POL**.
9. Atlasiet **Izveidot**.

### <a name="match-the-registration-types-with-registration-categories"></a>Saskaņot reģistrācijas tipus ar reģistrācijas kategorijām

1. Doties uz **organizācijas** > **administrēšanas globālās adrešu** > **grāmatas reģistrācijas tipu reģistrācijas** > **·** kategorijām.
2. Darbību rūtī atlasiet Jauns, **lai izveidotu saiti starp katru jūsu** izveidoto reģistrācijas tipu un reģistrācijas kategoriju.

    - Pvn ID (NRN koda) reģistrācijas veidam atlasiet **PVN ID** reģistrācijas kategoriju.
    - Uzņēmuma numura reģistrācijas tipam (Regon code) atlasiet uzņēmuma **ID (COID)** reģistrācijas kategoriju.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Iestatiet sava uzņēmuma PVN ID un uzņēmuma numuru.

1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
2. Režģī atlasiet uzņēmumu.
3. Darbību rūtī atlasiet **reģistrācijas** VISUS.
4. Kopsavilkuma **cilnē Reģistrācijas ID** atlasiet **·** Pievienot.
5. Laukā **Reģistrācijas tips atlasiet vienu no iepriekš** izveidotajiem reģistrācijas tipiem.
6. Ievadiet sava uzņēmuma PVN ID (NRN kodu) vai uzņēmuma numuru (Reēnkodu) atkarībā no iepriekšējā solī atlasītā reģistrācijas veida.
7. Atkārtojiet no 4. līdz 6. solim citam reģistrācijas tipam, ko iepriekš izveidojāt.

## <a name="set-up-a-company-address"></a>Uzņēmuma adreses iestatīšana

1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
2. Režģī atlasiet uzņēmumu.
3. Cilnē **Adreses** atlasiet **·** Rediģēt.
4. Dialoglodziņa **Rediģēt** adresi laukā **Pasta indekss** atlasiet uzņēmuma pasta indeksu.
5. Laukā **·** Iela ievadiet savu adresi.
6. Laukā **·** Pilsēta atlasiet savu pilsētu.

## <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

1. Doties uz **nodokļu** > **iestatījuma** > **ārējās tirdzniecības parametriem**.
2. Cilnes **Intrastat** kopsavilkuma cilnes **Elektroniskie pārskati** laukā Failu formātu **·** kartēšana atlasiet Intrastat **·** (PL).
3. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
4. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.
5. **Transakcijas kods** – izvēlieties transakcijas kodu īpašuma pārsūtīšanai. Varat izmantot šo kodu transakcijām, kas izraisa faktisko vai plānoto īpašuma pārsūtīšanu attiecībā uz kompensāciju (finansiālu vai cita veida). To izmanto arī labojumiem. Uzņēmumi Polijai izmanto divciparu darbības kodus.
6. Laukā **Kredīta nota** izvēlieties transakcijas kodu preču atgriešanai.
7. Cilne **Valsts/reģiona rekvizīti**, lauks **Valsts/reģions** uzskaita visas valstis vai reģionus, ar kuriem jūsu organizācija veic darījumus. Katrai valstij, kas ietilpst ES, atlasiet ES laukā **·** **Valsts/reģiona tips, lai** valsts parādītos Intrastat pārskatā. Polijai atlasiet **Iekšzemes** laukā **Valsts/reģiona** tips.
8. Cilnes Aģents kopsavilkuma cilnē Aģenta FastTab, sadaļā PVN, laukā PVN reģistrācijas numurs **·** **·** **·** **·** ievadiet **420000,** lai norādītu vienības kodu, uz kuru attiecas Intrastat deklarācija.
9. Cilnē **Kontaktpersona ievadiet tās personas vārdu, telefona numuru, faksa numuru un** e-pasta adresi, kas iesniedz deklarāciju.
10. Cilnes Numuru sērijas laukā Numuru sērijas kods XML faila numura atsaucei norādiet nemitīgu numuru sēriju, kuras maksimālais skaits ir **·** **·** **·** deviņas rakstzīmes. Šis lauks tiek izmantots, lai intrastat pārskatā **automātiski** ģenerētu vērtību deklarācijas identifikatora laukam.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Iestatīt preces parametrus Intrastat deklarācijai

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet preci.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Prece** izvēlieties atbilstošo preces kodu. Preces nosaukums tiks drukāts Intrastat pārskata laukā Preces **·** apraksts.
4. Sadaļas **·** Izcelsme **laukā** Valsts/reģions atlasiet preces izcelsmes valsti vai reģionu.
5. Kopsavilkuma cilnes **Krājumu pārvaldība** laukā **Neto svars**  ievadiet preces svaru kilogramos.

## <a name="set-up-compression-of-intrastat"></a>Iestatīt Intrastat arhivēšanu

-   Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Intrastat arhivēšana** un atlasiet laukus, kas jāsalīdzina, kad tiek apkopota Intrastat informācija. Polijas Intrastat laukos atlasiet šādus laukus:

    - Prece
    - Darbības kods
    - Izcelsmes valsts/reģions
    - Transportēšana
    - Piegādes nosacījumi
    - Sūtītāja valsts/reģions
    - Valsts/reģions
    - Labojums
    - PVN reģistrācijas numurs
    - Virziens
    - Rēķins

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Iestatīt transportēšanas metodi un piegādes nosacījumus

1.  Transportēšanas kodu iestatīšana;

    1. Atveriet **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transportēšanas metode**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **·** Transportēšana ievadiet unikālu kodu. Polijas uzņēmumi izmanto viena cipara transporta kodus.

2.  Iestatiet piegādes veidu Intrastat kodiem.

    1. Atveriet **sagādes un avotu** > **iestatīšanas** > **sadales piegādes** > **·** nosacījumus.
    2. Režģī atlasiet piegādes nosacījumu kopu.
    3. Kopsavilkuma **cilnes** Vispārīgi laukā **Intrastat kods** ievadiet unikālo kodu.

## <a name="intrastat-transfer"></a>Intrastat pārsūtīšana

Lapā **Intrastat** darbību rūtī varat atlasīt **Pārsūtīt**, lai automātiski pārsūtītu informāciju par EK iekšējo tirdzniecību no pārdošanas pasūtījumiem, brīva teksta rēķiniem, pirkšanas pasūtījumiem, kreditora rēķiniem, kreditora produktu ieejas plūsmām, projekta rēķiniem un pārsūtīšanas pasūtījumiem. Tiks pārsūtīti tikai dokumenti, kuru adresāta valsts vai reģions ir ES valsts vai sūtījuma valsts.

Darbības var ievadīt arī manuāli, **darbības rūtī** atlasot Jauns.

### <a name="generate-an-intrastat-report"></a>Ģenerēt Intrastat pārskatu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Rezultāts** &gt; **Pārskats**.
3. Dialoglodziņā **Intrastat pārskats** iestatiet tālak norādītos laukus.

    | Lauks | Apraksts |
    |-------------------------|-------------------------|
    | No datuma | Atlasiet pārskata sākuma datumu. |
    | Ģenerēt failu | Iestatiet šo opciju kā **·** Jā, lai intrastat pārskatam ģenerētu .xml failu. |
    | Faila nosaukums | Ievadiet .xml faila nosaukumu. |
    | Ģenerēt pārskatu | Iestatiet šo opciju kā **Jā**, lai ģenerētu .xlsx failu Intrastat pārskatam. |
    | Pārskata faila nosaukums | Ievadiet .xlsx faila nosaukumu. |
    | Virziens | Atlasiet **Saņemšanas** pārskatam par EK iekšējām saņemšanas.</br>Atlasiet **Nosūtīšanas** pārskatam par EK iekšējām nosūtīšanām. |
    | Deklarācijas identifikators | Dokumenta ID tiek ģenerēts automātiski, un to var atjaunināt. |
    | Deklarācijas tips | Atlasiet **deklarāciju** oriģinālai deklarācijai.</br>Atlasiet Deklarācijas labojums - aizstāšana labojuma deklarācijai, kas paredzēta, lai **·** pilnībā aizstātu esošu, iepriekš iesniegtu sākotnējo vai labojuma deklarāciju. |
    | Dokumenta izveides pilsēta | Ievadiet vērtību, kas jādrukā **Intrastat deklarācijas laukā Miejscettsc.** |
    | Dokumenta izveides datums | Ievadiet vērtību, kas jādrukā **Intrastat deklarācijas laukā Deklaracja** dati. |
    | Dokumenta Nr. | Ievadiet vērtību, kas jādrukā **Intrastat deklarācijas** laukā Skaitītājs. |
    | Dokumenta versija | Ievadiet vērtību, kas jādrukā **Intrastat deklarācijas laukā Wersja.** |

4. Atlasiet **Labi**, un pārskatiet ģenerētos pārskatus.

## <a name="example"></a>Paraugs

Šajā piemērā parādīts, kā grāmatot saņemšanas un nosūtīšanas Intrastatm, izmantojot **LEGALF** juridisko personu.

### <a name="preliminary-setup"></a>Iepriekšēja iestatīšana

Importējiet pēdējo ER konfigurāciju versiju:

   - Intrastat modelis
   - Intrastat pārskats
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Uzņēmuma adreses iestatīšana

1. Dodieties uz **Organizācijas administrēšana** > **Globālā adrešu grāmata** > **Adreses** > **Adrešu iestatīšana**.
2. Cilnē **Pilsēta** atlasiet **·** Jauns.
3. Laukā **Valsts/reģions** atlasiet **POL**.
4. Laukā **Pilsēta** ievadiet **·** Sia.
5. Cilnē **Pasta indekss** atlasiet **·** Jauns.
6. Laukā **Valsts/reģions** atlasiet **POL**.
7. Laukā **Pilsēta** atlasiet **·** Sia.
8. Laukā **Pasta indekss** ievadiet **00-844.**
9. Atveriet **Organizācijas administrēšana** > **Organizācija** > **Juridiskās personas** un atlasiet juridisko personu **DEMF**.
10. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
11. Laukā **Valsts/reģions** atlasiet **POL**.
12. Laukā **Pasta indekss** atlasiet **31-111**.
13. Laukā **Iela** ievadiet **Statystyczna 22/1**.
14. Laukā **Pilsēta** atlasiet **·** Sia.
15. Atlasiet **Labi**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Iestatiet sava uzņēmuma PVN ID un uzņēmuma numura kodu

### <a name="create-registration-types-for-company-codes"></a>Izveidot uzņēmumu kodu reģistrācijas tipus

1. Dodieties uz **organizācijas** > **administrēšanas globālās adrešu** > **grāmatas reģistrācijas tipu reģistrācijas** > **·** tipiem.
2. Darbību rūtī atlasiet Jauns, **lai izveidotu PVN ID** (NRN koda) reģistrācijas tipu.
3. Dialoglodziņā **Ievadīt reģistrācijas veida** detaļas laukā **Nosaukums** ievadiet **·** NRN.
4. Laukā **Valsts/reģions** atlasiet **POL**.
5. Atlasiet **Izveidot**.
6. Darbību rūtī atlasiet Jauns, **lai izveidotu reģistrācijas tipu uzņēmuma** numuram (Regon kods).
7. Dialoglodziņā **Ievadīt reģistrācijas tipa detaļas** laukā Nosaukums **·** ievadiet **·** Regon.
8. Laukā **Valsts/reģions** atlasiet **POL**.
9. Atlasiet **Izveidot**.

### <a name="match-the-registration-types-with-registration-categories"></a>Saskaņot reģistrācijas tipus ar reģistrācijas kategorijām

1. Doties uz **organizācijas** > **administrēšanas globālās adrešu** > **grāmatas reģistrācijas tipu reģistrācijas** > **·** kategorijām.
2. Darbību rūtī atlasiet Jauns, **lai izveidotu saiti starp katru jūsu** izveidoto reģistrācijas tipu un reģistrācijas kategoriju.

    - NIP **·** reģistrācijas veidam atlasiet PVN ID reģistrācijas **·** kategoriju.
    - Regon **reģistrācijas** veidam atlasiet uzņēmuma ID **(COID)** reģistrācijas kategoriju.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Iestatiet sava uzņēmuma PVN ID un uzņēmuma numuru.

1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
2. Režģī atlasiet **DEMF**.
3. Darbību rūtī atlasiet **reģistrācijas** VISUS.
4. Kopsavilkuma **cilnē Reģistrācijas ID** atlasiet **·** Pievienot.
5. Laukā **Reģistrācijas tips atlasiet** **·** NRN.
6. Laukā **Reģistrācijas** numurs ievadiet **·** 1234567890.
7. Atlasiet **Pievienot**.
8. Laukā **Reģistrācijas tips atlasiet** **·** Regon.
9. Laukā **Reģistrācijas** numurs ievadiet **·** 12345678901234.

### <a name="set-up-a-number-sequence-code"></a>Numuru sērijas koda iestatīšana

1. Atveriet **Organizācijas administrēšana** > **Numuru sērijas** > **Numuru sērijas**.
2. Darbību rūts cilnes **Numuru sērija** grupā Jauna atlasiet **Numuru** **·** sērija.
3. Kopsavilkuma **cilnes Identifikācija** laukā **Numuru sērijas kods** ievadiet XML **\_** failu.
4. Kopsavilkuma cilnes **·** Tvēruma parametri laukā **·** Tvērums atlasiet **·** Uzņēmums.
5. Laukā **·** Uzņēmums atlasiet **·** DEMF.
6. Kopsavilkuma cilnes **·** Segmenti laukā Garums **ievadiet** **4 burtciparu** **·** segmentu.
7. Kopsavilkuma **cilnes** Vispārīgi sadaļā Iestatījumi iestatiet opciju Nepārtraukta uz **·** **·** **·** Nē.
8. Skaitļu **sadalījuma** sadaļas laukā **Vislielākais** ievadiet **9999.**

### <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
2. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **11**.
3. Kopsavilkuma **cilnes** Elektroniskie pārskati laukā **Failu formātu** kartēšana atlasiet Intrastat **·** (PL).
4. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
5. Kopsavilkuma cilnē **Preču kodu hierarhija** pārbaudiet, vai kategoriju **hierarhijas lauks ir** iestatīts uz **·** Intrastat.
6. Cilnē **Valsts/reģiona rekvizīti** atlasiet **Jauns**.
7. Laukā **Puses valsts/reģions** atlasiet **POL**. Pēc tam **laukā Valsts/reģiona** tips atlasiet **·** Iekšzemes.
8. Laukā **Puses valsts/reģions** atlasiet **DEU**. Pēc tam **laukā Valsts/reģiona** tips atlasiet **·** ES.
9. Cilnes Aģents kopsavilkuma cilnes Aģents sadaļā PVN laukā PVN reģistrācijas numurs **·** **·** **·** **·** ievadiet **420 000.**
10. Cilnes **Kontaktpersona** laukā Nosaukums **·** ievadiet **Manish** Chopra.
11. Laukā **·** Tālrunis ievadiet **·** 425-555-5068.
12. Laukā **Faksa** numurs ievadiet **·** 425-555-5049.
13. Laukā **·** E-pasts ievadiet **·** manishc@contoso.com.
14. Cilnē **Numuru sērijas** laukā **Numuru sērijas** kods XML faila **numura** atsaucei atlasiet XML **\_** failu.

### <a name="set-up-product-information"></a>Preces informācijas iestatīšana

1. Pārejiet uz **produktu informācijas pārvaldības** > **precēm** > **Izlaistās** **·** preces.
2. Režģī atlasiet **D0001**.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **100 200 30**.
4. Kopsavilkuma cilnes **Pārvaldīt krājumu** sadaļā **Svara mērījumi** laukā **Neto svars** ievadiet **2**.
5. Darbību rūtī atlasiet **Saglabāt**.
6. Režģī atlasiet **D0003**.
7. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **100 200 30**.
8. Sadaļas **Izcelsme** laukā **Valsts/reģions** atlasiet **DEU**.
9. Kopsavilkuma cilnes **Pārvaldīt krājumu** sadaļā **Svara mērījumi** laukā **Neto svars** ievadiet **5**.
10. Darbību rūtī atlasiet **Saglabāt**.

### <a name="change-the-site-address"></a>Vietnes adreses maiņa

1. Atveriet **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Vietnes**.
2. Režģī atlasiet **1**.
3. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
4. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **POL**.
5. Atlasiet **Labi**.

### <a name="set-up-a-transport-method"></a>Transportēšanas metodes iestatīšana

1. Izveidojiet transportēšanas metodi.

    1. Atveriet **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transportēšanas metode**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **·** Transportēšana ievadiet **·** 3.
    4. Laukā **Apraksts** ievadiet Informācija par **·** transportēšanu.

2. Piešķiriet jauno transportēšanas metodi piegādes režīmam. Šādā veidā jūs iestatāt noklusējuma vērtības, kas tiek izmantotas transportēšanas metodei, kad tiek izvēlēts atbilstošais piegādes veids.

    1. Pārejiet uz sadaļu **Sagāde un avoti** > **Iestatījumi** > **Izplatīšana** > **Piegādes veidi**.
    2. Režģī atlasiet **10**.
    3. Kopsavilkuma cilnes **Ārējā tirdzniecība** laukā **Transports** atlasiet **3**.

3. Atlasiet debitora noklusējuma piegādes veidu.

    1. Atveriet **Debitori** > **Debitori** > **Visi debitori**.
    2. Režģī atlasiet **DE-016.**
    3. Kopsavilkuma **cilnes Rēķins** un piegāde laukā **Piegādes veids** atlasiet **10.**

4. Atlasiet kreditora noklusējuma piegādes veidu.

    1. Dodieties **uz Kreditoru** > **parādiem visiem** > **·** kreditoriem.
    2. Režģī atlasiet **DE-001.**
    3. Kopsavilkuma **cilnes Rēķins** un piegāde laukā **Piegādes veids** atlasiet **10.**

### <a name="set-up-codes-for-terms-of-delivery"></a>Iestatīt piegādes nosacījumu kodus

1. Iestatiet piegādes nosacījumiem Intrastat kodu.

    1. Atveriet **sagādes un avotu** > **iestatīšanas** > **sadales piegādes** > **·** nosacījumus.
    2. Režģī atlasiet **CIF**.
    3. Kopsavilkuma **cilnes** Vispārīgi laukā **Intrastat kods** ievadiet **·** CIF.

2. Atlasiet debitora noklusējuma piegādes nosacījumus.

    1. Atveriet **Debitori** > **Debitori** > **Visi debitori**.
    2. Režģī atlasiet **DE-016.**
    3. Kopsavilkuma **cilnē Rēķins** un piegāde laukā **Piegādes nosacījumi** atlasiet **·** CIF.

3. Atlasiet kreditora noklusējuma piegādes nosacījumus.

    1. Dodieties **uz Kreditoru** > **parādiem visiem** > **·** kreditoriem.
    2. Režģī atlasiet **DE-001.**
    3. Kopsavilkuma **cilnē Rēķins** un piegāde laukā **Piegādes nosacījumi** atlasiet **·** CIF.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>ES debitora PVN reģistrācijas numura koda pārbaude

1. Atveriet **Debitori** > **Debitori** > **Visi debitori**.
2. Režģī atlasiet **DE-016.**
3. Kopsavilkuma cilnē Rēķins un piegāde sadaļā PVN pārbaudiet, vai PVN reģistrācijas numura lauks ir iestatīts **·** uz **·** **·** **DE9012.**

### <a name="create-a-sales-order-with-an-eu-customer"></a>Pārdošanas pasūtījuma izveide ar ES debitoru

1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņā **Izveidot pārdošanas pasūtījumu**, kopsavilkuma cilnē **Debitors**, sadaļā **Debitors**, laukā **Debitora konts** atlasiet **DE-016**.
4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Glabāšanas dimensijas** laukā **Vieta** atlasiet **1**.
5. Laukā **Noliktava** atlasiet **11**.
6. Cilnē Adrese pārbaudiet, vai lauks Adrese ir iestatīts uz **·** **·** **Latvijā lietoto 12, Argentīna, 24103, DEU, jo klients** ir no Vācijas.
7. Atlasiet **Labi**.
8. Cilnes Virsraksts kopsavilkuma cilnē Piegāde pārbaudiet, vai lauks Piegādes nosacījumi ir iestatīts uz CIF, un piegādes režīma lauks ir iestatīts **·** **uz** **·** **·** **·** **10.**
9. Cilnē **Rindas** kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **8**.
10. Kopsavilkuma cilnē Rindas detaļas cilnē Ārējā tirdzniecība pārbaudiet, vai darbības koda lauks ir iestatīts uz **·** **·** **·** **11,** **·** **·** **·** **·** lauks Prece ir iestatīts uz 100 200 30 un izcelsmes valsts/reģions ir iestatīts uz POL.
11. Darbību rūtī atlasiet **Saglabāt**.
12. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
13. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
14. Kopsavilkuma cilnē Iestatījumi laukā Pārdošanas datums atlasiet **·** **·** **10/18/2021** (2021. gada 18. oktobris).
15. Atlasiet **Labi**, lai iegrāmatotu rēķinu.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Pārsūtiet transakciju uz Intrastat žurnālu un pārskatiet rezultātu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**.
4. Atlasiet **Filtrēt**.
5. Intrastat filtra dialoglodziņa cilnē Diapazons atlasiet pirmo rindu un pārbaudiet, vai lauks **·** Lauks ir **·** **·** iestatīts uz **·** Datumu.
6. Laukā **Kritēriji** atlasiet pašreizējo datumu.
7. Lai aizvērtu dialoglodziņu **Intrastat filtrs**, atlasiet **Labi**.
8. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Intrastat (pārsūtīšana)** un pārskatiet rezultātu. Rindā atlasiet pirmo izveidoto pārdošanas pasūtījumu.

    ![Rinda, kas ataino pārdošanas pasūtījumu Intrastat lapā](media/intrastat_pl_1.png)

9. Atlasiet darbības rindu un tad atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju.

    ![Pārdošanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_pl_2.png)

10. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
11. Intrastat pārskata dialoglodziņa Kopsavilkuma cilnes Parametri sadaļā Datums laukā No datuma atlasiet **·** pašreizējā mēneša pirmo **·** **·** **·** dienu.
12. Sadaļā **Eksporta** **opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**. Pēc tam laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
13. Atlasiet opcijai **Izveidot pārskatu** iestatījumu **Jā**. Pēc tam laukā **Pārskata faila nosaukums** ievadiet nepieciešamo nosaukumu.
14. Laukā **Virziens** atlasiet **Nosūtīšana**.
15. Failu formāta **kartēšanas** sadaļā pārbaudiet, vai deklarācijas **tipa lauks ir** iestatīts uz **·** Deklarāciju.
16. Dokumenta **izveides pilsētas** laukā ievadiet **·** Sia.
17. Laukā **Dokumenta izveides datums atlasiet** **2021. gada 10. oktobris** (2021. gada 19. oktobris).
18. Laukā **Dokumenta** Nr. ievadiet **11.**
19. Laukā **Dokumenta versija** ievadiet **22.**
20. Atlasiet **·** Labi, un pārskatiet ģenerēto pārskatu XML formātā. Nākamajā tabulā ir parādītas vērtības atskaites piemērā.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Lauka nosaukums</strong></p>
    </td>
    <td>
    <p><strong>Lauka apraksts</strong></p>
    </td>
    <td>
    <p><strong>Vērtība</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informācija par dokumentu</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja dati</p>
    </td>
    <td>
    <p>Dokumenta izveidošanas datums.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Mīsu salas</p>
    </td>
    <td>
    <p>Pilsēta, kur dokuments tika izveidots.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPo papildmaksas</p>
    </td>
    <td>
    <p>Kopējais krājumu skaits.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Kopējā statistiskā vērtība.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur ;</p>
    </td>
    <td>
    <p>Kopējā rēķina vērtība.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Darba VIETU NOD.</p>
    </td>
    <td>
    <p>Vienības kods.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj (Rodzaj)</p>
    </td>
    <td>
    <p>Deklarācijas tips.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Versa</p>
    </td>
    <td>
    <p>Dokumenta versija.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numurs</p>
    </td>
    <td>
    <p>Dokumenta numurs.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Atsauces mēnesis.</p>
    </td>
    <td>
    <p>10.</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Ierašanās tiesības</p>
    </td>
    <td width="330">
    <p>Atsauces gads.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Darba tips</p>
    </td>
    <td width="330">
    <p>Pārskata virziens.</p>
    </td>
    <td>
    <p>T</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Laukuts NrWlas saskaņā ar</p>
    </td>
    <td width="330">
    <p>Deklarācijas identifikators.</p>
    </td>
    <td>
    <p>21ISTDEMF–0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informācija par uzņēmumu</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Mīsu salas</p>
    </td>
    <td width="330">
    <p>Pilsēta, kurā atrodas uzņēmums.</p>
    </td>
    <td>
    <p>Varšava</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regona (Regon)</p>
    </td>
    <td width="330">
    <p>Uzņēmuma Regona kods.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Uzņēmuma NRN kods.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztczk</p>
    </td>
    <td>
    <p>Uzņēmuma ASV pasta indekss/pasta indekss.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Iela, kurā atrodas uzņēmums.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa (Nazwa)</p>
    </td>
    <td>
    <p>Uzņēmuma nosaukums.</p>
    </td>
    <td>
    <p>Contoso izklaides sistēma Vācija</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informācija par labo</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>BratoscStatystyczna</p>
    </td>
    <td>
    <p>Statistiskā vērtība.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Ierašanās un spēcFaktury</p>
    </td>
    <td>
    <p>Rēķina vērtība.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Neto masa.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta (IdKontrahenta)</p>
    </td>
    <td>
    <p>Debitora PVN numurs.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowar arī</p>
    </td>
    <td>
    <p>Preces kods.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Darbības kods.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Karakidostas</p>
    </td>
    <td>
    <p>Piegādes veida nosacījumi.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nešopochodze ne, Unikos, Ne uz koki</p>
    </td>
    <td>
    <p>Kods nosūtīšanas/adresāta valstij vai reģionam.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru (opisTowaru)</p>
    </td>
    <td>
    <p>Preces apraksts.</p>
    </td>
    <td>
    <p>Aparatūras</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId (PozId)</p>
    </td>
    <td>
    <p>Krājuma numurs.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktinformācija</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-pasts</p>
    </td>
    <td>
    <p>Iesūtīēja e-pasta adrese.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Iesūtāja faksa numurs.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefons (Telefon)</p>
    </td>
    <td>
    <p>Ieslēga tālruņa numurs.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Iesaukēja vārds.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Pārskatiet ģenerēto pārskatu Excel formātā.

    ![Intrastat pārskats par nosūtīšanu](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pirkšanas pasūtījuma izveide** laukā **Kreditora konts** atlasiet **DE-001**.
4. Laukā **Vieta** atlasiet **·** 1.
5. Noliktavas **·** laukā atlasiet **11.**
6. Atlasiet **Labi**.
7. Kopsavilkuma cilnes Virsraksts cilnē Piegāde pārbaudiet, vai lauks Piegādes režīms ir iestatīts uz 10 un lauks Piegādes nosacījumi **·** **ir** **·** **·** **·** iestatīts uz **·** CIF.
8. Cilnē **Rindas** kopsavilkuma cilnes **Pirkšanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **D0003**. Laukā **Daudzums** ievadiet **6**.
9. Kopsavilkuma cilnē Detalizēta informācija par rindu cilnē Ārējā tirdzniecība pārbaudiet, vai darbības kods ir iestatīts uz **·** **·** **·** **11,** **·** **·** **·** **·** **·** **·** lauks Transports ir iestatīts uz 3, lauks Prece ir iestatīts uz 100 200 30 un izcelsmes valsts/reģions ir iestatīts kā DEU.
10. Darbību rūts cilnē **Pirkšana**, grupā **Darbības** atlasiet **Apstiprināt**.
11. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
12. Darbību rūtī atlasiet **Noklusējums un pēc tam** **laukā Noklusējuma daudzums rindām** atlasiet **Pasūtītais daudzums**. Pēc tam atlasiet **Labi**.
13. Kopsavilkuma cilnes **Kreditora** rēķins virsraksts sadaļas Rēķina **identifikācija** laukā Numurs **·** ievadiet **00010.**
14. Rēķina **datumu** sadaļas laukā **Rēķina datums atlasiet pašreizējo** datumu. Šis datums tiks izmantots Intrastat pārsūtīšanai.
15. Laukā **Saņemt dokumenta datumu atlasiet** **10/18/2021** (2021. gada 18. oktobris).
16. Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu žurnālu.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Intrastat deklarācijas izveide saņemšanas darbībām

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Kreditora rēķins** uz **Jā**.
4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

    ![Rinda, kas attēlo pirkšanas pasūtījumu Intrastat lapā](media/intrastat_pl_4.png)

5. Pārskatiet **pirkšanas pasūtījuma** informāciju cilnē Vispārīgi.

    ![Pirkšanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_pl_5.png)

6. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
7. Intrastat pārskata dialoglodziņa Kopsavilkuma cilnes Parametri sadaļā Datums laukā No datuma atlasiet **·** pašreizējā mēneša pirmo **·** **·** **·** dienu.
8. Sadaļā **Eksporta** **opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**. Pēc tam laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
9. Atlasiet opcijai **Izveidot pārskatu** iestatījumu **Jā**. Pēc tam laukā **Pārskata faila nosaukums** ievadiet nepieciešamo nosaukumu.
10. Laukā **Virziens** atlasiet **Saņemšana**.
11. Failu formāta **kartēšanas** sadaļā pārbaudiet, vai deklarācijas **tipa lauks ir** iestatīts uz **·** Deklarāciju.
12. Dokumenta **izveides pilsētas** laukā ievadiet **·** Sia.
13. Laukā **Dokumenta izveides datums atlasiet** **2021. gada 10. oktobris** (2021. gada 19. oktobris).
14. Laukā **Dokumenta** Nr. ievadiet **11.**
15. Laukā **Dokumenta versija** ievadiet **22.**
16. Atlasiet **·** Labi, un pārskatiet ģenerēto pārskatu XML formātā. Nākamajā tabulā ir parādītas vērtības atskaites piemērā.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Lauka nosaukums</strong></p>
    </td>
    <td>
    <p><strong>Lauka apraksts</strong></p>
    </td>
    <td>
    <p><strong>Vērtība</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Informācija par dokumentu</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja dati</p>
    </td>
    <td>
    <p>Dokumenta izveidošanas datums.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Mīsu salas</p>
    </td>
    <td>
    <p>Pilsēta, kur dokuments tika izveidots.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPo papildmaksas</p>
    </td>
    <td>
    <p>Kopējais krājumu skaits.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Kopējā statistiskā vērtība.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur ;</p>
    </td>
    <td>
    <p>Kopējā rēķina vērtība.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Darba VIETU NOD.</p>
    </td>
    <td>
    <p>Vienības kods.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj (Rodzaj)</p>
    </td>
    <td>
    <p>Deklarācijas tips.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Versa</p>
    </td>
    <td>
    <p>Dokumenta versija.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numurs</p>
    </td>
    <td>
    <p>Dokumenta numurs.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Atsauces mēnesis.</p>
    </td>
    <td>
    <p>10.</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Ierašanās tiesības</p>
    </td>
    <td width="332">
    <p>Atsauces gads.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Darba tips</p>
    </td>
    <td width="332">
    <p>Pārskata virziens.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Laukuts NrWlas saskaņā ar</p>
    </td>
    <td width="332">
    <p>Deklarācijas identifikators.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Informācija par uzņēmumu</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Mīsu salas</p>
    </td>
    <td width="332">
    <p>Pilsēta, kurā atrodas uzņēmums.</p>
    </td>
    <td>
    <p>Varšava</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regona (Regon)</p>
    </td>
    <td width="332">
    <p>Uzņēmuma Regona kods.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Uzņēmuma NRN kods.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztczk</p>
    </td>
    <td>
    <p>Uzņēmuma ASV pasta indekss/pasta indekss.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Iela, kurā atrodas uzņēmums.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa (Nazwa)</p>
    </td>
    <td>
    <p>Uzņēmuma nosaukums.</p>
    </td>
    <td>
    <p>Contoso izklaides sistēma Vācija</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Informācija par labo</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>BratoscStatystyczna</p>
    </td>
    <td>
    <p>Statistiskā vērtība.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Ierašanās un spēcFaktury</p>
    </td>
    <td>
    <p>Rēķina vērtība.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Neto masa.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nešopochodze saskaņā ar</p>
    </td>
    <td>
    <p>Izcelsmes valsts vai reģiona kods.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Transportēšanas veida kods.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowar arī</p>
    </td>
    <td>
    <p>Preces kods.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Darbības kods.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Karakidostas</p>
    </td>
    <td>
    <p>Piegādes veida nosacījumi.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nešopochodze ne, Unikos, Ne uz koki</p>
    </td>
    <td>
    <p>Kods nosūtīšanas/adresāta valstij vai reģionam.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru (opisTowaru)</p>
    </td>
    <td>
    <p>Preces apraksts.</p>
    </td>
    <td>
    <p>Aparatūras</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId (PozId)</p>
    </td>
    <td>
    <p>Krājuma numurs.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p style="text-align: center;"><strong>Kontaktinformācija</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-pasts</p>
    </td>
    <td>
    <p>Iesūtīēja e-pasta adrese.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Iesūtāja faksa numurs.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefons (Telefon)</p>
    </td>
    <td>
    <p>Ieslēga tālruņa numurs.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Iesaukēja vārds.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Pārskatiet ģenerēto pārskatu Excel formātā.

    ![Intrastat pārskats par ieejumēm](media/intrastat_pl_6.png)
