---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā rakstā sniegtas atbildes uz dažiem bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.
author: jinniew
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5981946a4bba2c58402f4cf566bfa008de67363b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901375"
---
# <a name="financial-reporting-faq"></a>Bieži uzdotie jautājumi par finanšu pārskatu veidošanu

Šajā rakstā sniegtas atbildes uz bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Kā var ierobežot piekļuvi pārskatam, izmantojot koka drošību?

Šajā piemērā parādīts, kā ierobežot piekļuvi pārskatam, izmantojot koka drošību.

USMF demonstrācijas uzņēmumam ir **bilances pārskats**, kuram nedrīkstētu piekļūt visi finanšu pārskatu lietotāji. Varat izmantot koka drošību, lai ierobežotu piekļuvi atsevišķam pārskatam, ļaujot piekļūt tikai konkrētiem lietotājiem.

1. Pierakstieties programmā Financial Reporter Report Designer.
2. Lai izveidotu jaunu koka definīciju, atlasiet **Fails \> Jauns \> Koka definīcija**.
3. Veiciet dubultskārienu vai dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.
4. Atlasiet **Lietotāji un grupas**.
5. Atlasiet lietotājus vai grupas, kam vajadzīga piekļuve šim pārskatam.
6. Atlasiet **Saglabāt**.
7. Pārskata definīcijā pievienojiet jaunu koka definīciju.
8. Koka definīcijā atlasiet **Iestatījums**. Pēc tam sadaļā **Pārskata vienību atlase** atlasiet **Iekļaut visas vienības**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Kā noteikt, kuri konti neatbilst manām bilancēm?

Ja jums ir pārskats, kurā nav atbilstošu bilanču, veiciet tālāk norādītās darbības, lai identificētu visus kontus un novirzes.

### <a name="in-financial-reporter-report-designer"></a>Programmā Financial Reporter Report Designer

1. Izveidojiet jaunu rindas definīciju.
2. Atlasiet **Rediģēt \> Ievietot rindas no dimensijām**.
3. Atlasiet **MainAccount**.
4. Atlasiet **Labi**.
5. Saglabājiet rindas definīciju.
6. Izveidojiet jaunu kolonnas definīciju.
7. Izveidojiet jaunu pārskata definīciju.
8. Atlasiet **Iestatījumi** un noņemiet atzīmi šai opcijai.
9. Ģenerējiet pārskatu. 
10. Eksportējiet pārskatu uz Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>Risinājumā Dynamics 365 Finance:

1. Dodieties uz **Virsgrāmata \> Pieprasījumi un pārskati \> Apgrozījuma bilance**.
2. Iestatiet tālāk norādītos laukus.

    - **Sākuma datums** — ievadiet finanšu gada sākuma datumu.
    - **Beigu datums** — ievadiet datumu, kuram ģenerējat pārskatu.
    - **Finanšu dimensija** — iestatiet šo lauku kā **Galvenā konta kopa**.

3. Atlasiet **Aprēķināt**.
4. Eksportējiet pārskatu uz programmu Excel.

Tagad jābūt iespējai no Financial Reporter Excel pārskata kopēt datus uz pārskatu **Apgrozījuma bilance**, lai varētu salīdzināt kolonnas **Beigu bilance**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Kad rīkā Report Designer izveidoju pārskatu vai ģenerēju finanšu pārskatu, saņemu šādu ziņojumu: “Operāciju neizdevās pabeigt datu nodrošinātāja struktūras problēmas dēļ.” Kā reaģēt?

Ziņojums norāda, ka radās problēma, sistēmai mēģinot izgūt finanšu metadatus no data mart laikā, kad izmantojāt rīku Financial Reporting. Uz šo problēmu var reaģēt divos tālāk norādītajos veidos.

- Pārskatiet datu integrācijas statusu, rīkā Report Designer dodoties uz **Rīki \> Integrācijas statuss**. Ja integrācija ir nepilnīga, uzgaidiet, līdz tā tiks pabeigta. Pēc tam vēlreiz mēģiniet veikt darbību, ko veicāt, kad saņēmāt ziņojumu.
- Sazinieties ar atbalsta dienestu, lai identificētu un novērstu šo problēmu. Iespējams, sistēmā ir nekonsekventi dati. Atbalsta tehniskie darbinieki var palīdzēt identificēt šo problēmu serverī un atrast konkrētos datus, kurus var būt nepieciešams atjaunināt.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Kā vēsturiskā kursa transformācijas atlase ietekmē pārskata veiktspēju?

Vēsturiskais kurss parasti tiek izmantots nesadalītās peļņas, īpašuma, ražotnes un aprīkojuma kontos, kā arī kapitāla kontos. Vēsturiskais kurss var būt obligāts, pamatojoties uz Finanšu grāmatvedības standartu padomes (Financial Accounting Standards Board — FASB) vadlīnijām vai vispārpieņemtiem grāmatvedības principiem (generally accepted accounting principles — GAAP). Papildinformāciju skatiet sadaļā [Valūtas iespējas finanšu pārskatos](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Cik valūtas maiņas kursu veidi ir pieejami?

Ir pieejami trīs tālāk aprakstītie veidi.

- **Pašreizējais kurss** — šo veidu parasti izmanto bilances kontos. To dēvē par *tūlītējo valūtas maiņas kursu*, un tas var būt kurss mēneša pēdējā dienā vai citā iepriekš noteiktā datumā.
- **Vidējais kurss** — šo veidu parasti izmanto ienākumu pārskata (peļņas/zaudējumu) kontos. Varat iestatīt vidējo kursu, lai noteiktu vienkāršu vidējo vai svērto vidējo vērtību.
- **Vēsturiskais kurss** — šo veidu parasti izmanto nesadalītās peļņas, īpašuma, ražotnes un aprīkojuma kontos, kā arī kapitāla kontos. Šie konti var būt obligāti, pamatojoties uz FASB vai GAAP vadlīnijām.

## <a name="how-does-historical-currency-translation-work"></a>Kā darbojas vēsturiskās valūtas pārrēķināšana?

Kursi ir atkarīgi no darījuma datuma. Tādēļ katrs darījums tiek pārrēķināts atsevišķi, pamatojoties uz tuvāko valūtas maiņas kursu.

Veicot vēsturiskās valūtas pārrēķināšanu, var izmantot iepriekš aprēķinātas periodu bilances, nevis individuālu darījumu informāciju. Šīs darbības atšķiras no pašreizējā kursa pārrēķina darbībām.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Kā vēsturiskās valūtas pārrēķināšana ietekmē veiktspēju?

Kad pārskatos iekļautie dati tiek atjaunināti, var rasties aizkave, jo summas ir jāpārrēķina, pārbaudot darījuma informāciju. Šī aizkave tiek aktivizēta katru reizi, kad tiek atjaunināti kursi vai iegrāmatoti papildu darījumi. Piemēram, ja ir iestatīta vairāku tūkstošu kontu vēsturiskā pārrēķināšana vairākas reizes dienā, pārskata datu atjaunināšana var aizkavēties līdz pat stundai. Savukārt, ja specifisku kontu skaits ir mazāks, pārskata datu atjaunināšanas laiku var samazināt līdz vairākām minūtēm vai mazāk.

Tāpat, kad pārskati tiek ģenerēti, izmantojot valūtas pārrēķināšanu vēsturiskā veida kontiem, tiks veikti papildu aprēķini katram darījumam. Atkarībā no kontu skaita pārskatu ģenerēšanas laiks var būt vairāk nekā divas reizes ilgāks.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Kādi ir paredzētie Data Mart integrācijas intervāli?

Financial Reporter izmanto 16 uzdevumus, lai kopētu Dynamics 365 Finance datus Financial Reporter datubāzē. Tālāk sniegtajā tabulā uzskaitīti šie 16 uzdevumi un parādīts intervāls, kas norāda, cik bieži katrs uzdevums tiek izpildīts. Intervālus nevar mainīt.

| Nosaukums                                                       | Intervāls | Intervāla hronometrāža |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 kontu kategorijas / konta kategorija            | 41       | Minūtes         |
| AX 2012 konti / konts                                | 7        | Minūtes         |
| AX 2012 uzņēmumi / uzņēmums                               | 300      | Sekundes         |
| AX 2012 uzņēmumi / organizācija                          | 23       | Minūtes         |
| AX 2012 dimensiju kombinācijas / dimensiju kombinācija    | 1        | Minūtes         |
| AX 2012 dimensiju vērtības / dimensijas vērtība                | 11       | Minūtes         |
| AX 2012 dimensijas / dimensija                            | 31       | Minūtes         |
| AX 2012 valūtu kursi / valūtas kurss                    | 17       | Minūtes         |
| AX 2012 finanšu gadi / finanšu gads                        | 13       | Minūtes         |
| AX 2012 virsgrāmatas darījumi / informācija                | 1        | Minūtes         |
| AX 2012 organizācijas hierarhijas / koks                   | 3600    | Sekundes         |
| AX 2012 scenāriji / scenārijs                              | 29       | Minūtes         |
| AX 2012 darījuma tipa kvalificētāji / informācijas tipa kvalificētāji | 19       | Minūtes         |
| Uzturēšanas uzdevums                                           | 1        | Minūtes         |
| MR pārskata definīcijas / AX7 finanšu pārskati             | 45       | Sekundes         |
| MR pārskatu versijas / AX finanšu pārskata versijas         | 45       | Sekundes         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
