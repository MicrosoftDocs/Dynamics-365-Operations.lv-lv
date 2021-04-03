---
title: Elektronisko rēķinu izrakstīšanas pievienojumprogrammas konfigurēšana Regulatory Configuration Services (RCS)
description: Šajā tēmā skaidrots, kā konfigurēt Elektronisko rēķinu izrakstīšanas pievienojumprogrammu Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 99fac9a42dc2b180c220612c66fe753d43e5bd7f
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592626"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>Elektronisko rēķinu izrakstīšanas pievienojumprogrammas konfigurēšana Regulatory Configuration Services (RCS)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta informācija par Elektronisko rēķinu izrakstīšanas pievienojumprogrammas konfigurācijas iespējām Dynamics 365 Regulatory Configuration Services (RCS).

Izmantojot konfigurācijas iespējas, Elektronisko rēķinu izrakstīšanas pievienojumprogramma palīdz jums izpildīt uzņēmējdarbības un regulēšanas prasības elektroniskajiem rēķiniem bez nepieciešamības veikt kodēšanu. Un scenārijos, kuros elektroniskie rēķini ir elektroniski jāapstiprina tīmekļa pakalpojumiem, konfigurācijas iespējas palīdz arī izpildīt pakalpojumu prasības ziņojumu apmaiņai ar tīmekļa pakalpojumiem, neveicot nekādu kodēšanu.

## <a name="electronic-reporting"></a>Elektroniskie pārskati

Elektroniskie pārskati (EP) atbalsta Elektronisko rēķinu izrakstīšanas lietojumprogrammu.

Datu modeļa kartēšana un formāti ir konfigurējami komponenti, kas tiek izveidoti un uzturēti ar ER un izmantoti Elektronisko rēķinu izrakstīšanas pievienojumprogrammā. ER formāta veidotājs ir rīks failu formātu izveidošanai un uzturēšanai. Tas tiek izmantots, lai konfigurētu elektronisko rēķinu izrakstīšanas funkcijas.

Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu (EP) veidošanu](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektroniskās rēķinu izveides funkcijas

Elektronisko rēķinu izrakstīšanas funkcijas ir atbildīgas par elektronisko rēķinu ģenerēšanu, izmantojot Elektronisko rēķinu izrakstīšanas pievienojumprogrammu. Tās iekapsulē konfigurācijas noteikumus un izmanto tos, lai apstrādātu datus, ko Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management nosūta elektronisko rēķinu izrakstīšanas pievienojumprogrammai un elektroniskajiem rēķiniem.

Funkcijas atbalsta arī scenārijus, kuros ir nepieciešama atbilstība failu formāta specifikācijām un izvade ir atsevišķs elektronisks fails. Vairākumā gadījumu failu formāta specifikācijas publicē nodokļu iestāde.

Visbeidzot, funkcijas atbalsta ziņojumu apmaiņu ar ārējiem tīmekļa pakalpojumiem, ko vieso nodokļu iestāde vai kāda atsevišķa akreditēta puse, un pieprasa autorizāciju vai apstiprinājuma zīmogu elektroniskajā rēķinā.

### <a name="availability-of-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkciju pieejamība

Elektronisko rēķinu izrakstīšanas funkciju pieejamība ir atkarīga no valsts vai reģiona. Lai arī dažas funkcijas parasti ir pieejamas, citas ir pieejamas tikai priekšskatījumā.

#### <a name="preview-features"></a>Priekšskatījuma līdzekļi

Šajā tabulā parādītas elektronisko rēķinu izrakstīšanas funkcijas, kas pašlaik ir pieejamas priekšskatījumā.

| Valsts/reģions | Līdzekļa nosaukums                         | Biznesa dokuments |
|----------------|--------------------------------------|-------------------|
| Austrija        | Austrijas elektroniskie rēķini (AT)    | Pārdošanas un projektu rēķini |
| Beļģija        | Beļģijas elektroniskais rēķins (BE)      | Pārdošanas un projektu rēķini |
| Brazīlija         | Brazīlijas NF-e (BR)                  | 55. finanšu dokumenta modelis, labojumu vēstules, atcelšanas un anulēšanas |
| Brazīlija         | Brazīlijas NFS-e ABRASF Curitiba (BR) | Pakalpojuma finanšu dokumenti |
| Dānija        | Dānijas elektroniskais rēķins (DK)       | Pārdošanas un projektu rēķini |
| Ēģipte          | Ēģiptes elektroniskais rēķins (EG) | Pārdošanas un projektu rēķini |
| Igaunija        | Igaunijas elektroniskais rēķins (EE)     | Pārdošanas un projektu rēķini |
| Somija        | Somijas elektroniskais rēķins (FI)      | Pārdošanas un projektu rēķini |
| Francija         | Francijas elektroniskais rēķins (FR)       | Pārdošanas un projektu rēķini |
| Vācija        | Vācijas elektroniskais rēķins (DE)       | Pārdošanas un projektu rēķini |
| Itālija          | FatturaPA (IT)                       | Pārdošanas un projektu rēķini |
| Meksika         | Meksikas CFDI (MX)                    | Pārdošanas rēķini, pavadzīmes, krājumu pārsūtījumi, maksājumu papildinājumi un atcelšanas |
| Nīderlande    | Nīderlandes elektroniskais rēķins (NL)        | Pārdošanas un projektu rēķini |
| Norvēģija         | Norvēģijas elektroniskais rēķins (NO)    | Pārdošanas un projektu rēķini |
| Spānija          | Spānijas elektroniskais rēķins (ES)      | Pārdošanas un projektu rēķini |
| Eiropa         | PEPPOL elektroniskais rēķins            | PEPPOL pārdošanas un projektu rēķini |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkciju konfigurējami komponenti

Elektronisko rēķinu izrakstīšanas funkcijas sastāv no šādām konfigurējamu komponentu grupām:

- **Formāti** – formāti ļauj jums konfigurēt, kas elektronisko rēķinu izrakstīšanas pievienojumprogrammai ir jāizveido, kad elektroniskais dokuments kļūst par elektronisku rēķinu. Formāti ietver formāta konfigurāciju elektroniskajam rēķinam, kā arī failiem un ziņojumiem, kas tiek lietoti, lai iesniegtu pieprasījumus un saņemtu atbildes, kad nepieciešama komunikācija ar ārēju tīmekļa pakalpojumu.
- **Darbības** – darbības ļauj konfigurēt, kā elektronisko rēķinu izrakstīšanas pievienojumprogramma ģenerē elektroniskā dokumenta pārveidošanu, ko Finance un Supply Chain Management instances iesniedza elektroniskajā rēķinā.
- **Piemērojamības noteikumi** – piemērojamības noteikumi ļauj konfigurēt kontekstu, kuru elektronisko rēķinu izrakstīšanas pievienojumprogrammai ir jāapsver, lai apstrādātu elektronisko rēķinu izrakstīšanas līdzekli.
- **Mainīgie** – mainīgie ļauj konfigurēt atbalstu konfigurācijas loģikas uzbūvei. Mainīgie var darboties kā vērtību ievade, lai veiktu noteiktu darbību. Alternatīvi tie var darboties kā vērtību apmaiņa starp Finance un Supply Chain Management instancēm un Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
- **Elektronisko dokumentu modeļu kartēšana** – elektronisko dokumentu modeļa kartēšana ļauj konfigurēt EP modeļa kartēšanu. Modeļa kartēšana definē abstraktā rēķina datu kartēšanu, kas ir integrēta Elektronisko rēķinu pievienojumprogrammā, kad tiek iesniegti elektroniskie dokumenti.
- **Rēķina konteksta modelis** - rēķina konteksta modelis ļauj konfigurēt EP rēķina konteksta modeli un definēt elektroniskās rēķinu izrakstīšanas funkcijas kontekstu.
- **Atbilžu tipi** – atbilžu tipi ļauj jums konfigurēt, ko Elektronisko rēķinu izrakstīšanas pievienojumprogrammai jāatjaunina Finance un Supply Chain Management instancēs kā elektroniskā rēķina apstrādes rezultāts.

### <a name="formats"></a>Formāti

Šie saraksti parāda EP formāta konfigurācijas, kas pieejamas elektroniskajiem rēķinu izrakstīšanas līdzekļiem.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Austrijas (AT) elektroniskie rēķini: pārdošanas un projekta rēķini Austrijai

- OIOUBL pārdošanas rēķins
- OIOUBL projekta rēķins
- OIOUBL pārdošanas kredīta nota
- OIOUBL projekta kredīta nota

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Beļģijas (BE) elektroniskais rēķins: pārdošanas un projekta rēķini Beļģijai

- UBL Pārdošanas rēķins BE
- UBL Projekta rēķins BE
- UBL projekta kredīta nota BE
- UBL pārdošanas kredīta nota BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brazīlijas (BR) NF-e: NF-e Federal (Brazīlija)

- NF-e iesniegšanas eksporta formāts (BR)
- NF-e labojuma vēstules eksporta formāts (BR)
- NF-e atcelšanas eksporta formāts (BR)
- NF-e anulēšanas eksporta formāts (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brazīlijas NFS-e (BR): NFS-e ABRASF Kuritibas pilsēta

- NFS-e ABRASF Kuritiba (BR)
- NFS-e ABRASF Uzzināt Kuritibu (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Dānijas (DK) elektroniskais rēķins: pārdošanas un projekta rēķini Dānijai

- OIOUBL pārdošanas rēķins
- OIOUBL projekta rēķins
- OIOUBL pārdošanas kredīta nota
- OIOUBL projekta kredīta nota

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Holandes (NL) elektroniskais rēķins: pārdošanas un projekta rēķini Nīderlandei

- UBL Pārdošanas rēķins NL
- UBL Projekta rēķins NL
- UBL projekta kredīta nota NL
- UBL pārdošanas kredīta nota NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Ēģiptes (EG) elektroniskais rēķins: pārdošanas un projekta rēķini Ēģiptei

- Pārdošanas rēķins (EG) (rēķina izrakstīšana)
- Projekta rēķins (EG) (rēķina izrakstīšana)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Igaunijas (EE) elektroniskais rēķins: pārdošanas un projekta rēķini Igaunijai

- Pārdošanas rēķins (EE)
- Projekta rēķins (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Somijas (FI) elektroniskais rēķins: pārdošanas un projekta rēķini Somijai

- Pārdošanas rēķins (FI)
- Projekta rēķins (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Francijas (FR) elektroniskais rēķins: pārdošanas un projekta rēķini Francijai

- UBL Pārdošanas rēķins FR
- UBL Projekta rēķins FR
- UBL projekta kredīta nota FR
- UBL pārdošanas kredīta nota FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Vācijas (DE) elektroniskais rēķins: pārdošanas un projekta rēķini Vācijai

- Pārdošanas rēķins (DE)
- Projekta rēķins (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Itālijas (IT) elektroniskais rēķins: pārdošanas un projekta rēķini Itālijai

- Pārdošanas rēķins (IT)
- Projekta rēķins (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Meksikas (MX) CFDI: CFDI Meksikai

- CFDI rēķina formāts (MX)
- CFDI Pavadzīme (MX)
- CFDI Krājumu pārsūtīšana (MX)
- CFDI maksājuma formāts (MX)
- CFDI rēķina atcelšanas formāts (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norvēģijas (NO) elektroniskais rēķins: pārdošanas un projekta rēķini Norvēģijai

- OIOUBL pārdošanas rēķins
- OIOUBL projekta rēķins
- OIOUBL pārdošanas kredīta nota
- OIOUBL projekta kredīta nota

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektroniskais rēķins: PEPPOL pārdošanas un projekta rēķini

- PEPPOL pārdošanas rēķins
- PEPPOL projekta rēķins
- PEPPOL pārdošanas kredīta nota
- PEPPOL Projekta kredīta nota

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spānijas (ES) elektroniskais rēķins: pārdošanas un projekta rēķini Spānijai

- Pārdošanas rēķins (ES)
- Projekta rēķins (ES)

### <a name="actions"></a>Darbības

Šajā tabulā uzskaitītas pieejamās darbības un tas, vai tās pašlaik ir pieejamas vai joprojām tiek priekšskatītas.

| Darbība                                        | Apraksts                                                                  | Pieejamība         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Transformējiet dokumentu                            | Lai pārveidotu dokumentu, palaidiet elektronisko pārskatu formātu.                   | Vispārēji pieejams  |
| Parakstīt xml dokumentu                             | Parakstīt xml dokumentus ar digitālo parakstu.                                   | Priekšskatījumā           |
| Parakstīt json dokumentu Ēģiptes nodokļu iestādei | Parakstīt json dokumentus ar digitālo parakstu Ēģiptes nodokļu iestādei.       | Vispārēji pieejams  |
| Integrēt ar Ēģiptes ETA pakalpojumu           | Sazināties ar Ēģiptes nodokļu iestādi.                                     | Vispārēji pieejams  |
| Izsauciet Brazīlijas SEFAZ pakalpojumu                  | Integrēt ar Brazīlijas SEFAZ pakalpojumu finanšu dokumenta iesniegšanai.       | Priekšskatījumā           |
| Izsaukt Meksikas PAC pakalpojumu                      | Integrēt ar Meksikas PAC pakalpojumu CFDI iesniegšanai.                      | Priekšskatījumā           |
| Apstrādāt atbildi                              | Analizējiet atbildi, kas saņemta no tīmekļa pakalpojumu zvana.                     | Vispārēji pieejams  |
| Izmantot MS Power Automate                         | Integrējiet ar Microsoft Power Automate iebūvētu plūsmu.                       | Priekšskatījumā           |

## <a name="configuration-providers"></a>Konfigurācijas nodrošinātāji

Konfigurācijas nodrošinātāji nodrošina elektronisko rēķinu izrakstīšanas līdzekļus un to EP komponentus, piemēram, modeļa kartēšanu, formāta konfigurāciju un konteksta modeli. Tās publicē elektroniskos rēķinu izrakstīšanas līdzekļus un EP komponentus saistītajā globālajā repozitorijā. No turienes citas organizācijas var tās lejupielādēt.

Pirms konfigurējat elektronisko rēķinu izrakstīšanas līdzekļus, izmantojot RCS, jums jākonfigurē sava organizācija kā konfigurācijas nodrošinātājs **Elektronisko pārskatu** modulī. Papildinformāciju par to, ka iestatīt konfigurācijas nodrošinātāju kā **Aktīvs** skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Elektronisko rēķinu izrakstīšanas funkciju skatīšana Globālajā repozitorijā

Lai pārlūkotu elektronisko rēķinu izrakstīšanas līdzekļus, kas ir pieejami noteikta konfigurācijas nodrošinātāja Globālajā repozitorijā, sinhronizējiet savas organizācijas RCS instanci. Pēc sinhronizācijas pabeigšanas tiek atjaunināts pieejamo elektronisko rēķinu izrakstīšanas funkciju saraksts.

## <a name="importing-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkcijas importēšana

Pirms izmantojat vai konfigurējat elektronisko rēķinu izrakstīšanas līdzekļus, jums tie jāimportē jūsu organizācijas RCS instancē. Importa operācija izveido funkciju lokālo kopiju un kopē visus EP artefaktus, ko funkcijas izmanto (piemēram, formāta konfigurācijas un modeļa konfigurācijas) uz jūsu organizācijas RCS instanci.

Jūs varat importēt Elektronisko rēķinu izrakstīšanas līdzekli no jebkura konfigurācijas nodrošinātāja.

## <a name="creating-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkcijas izveidošana

Varat izveidot elektronisko rēķinu izrakstīšanas līdzekli no sākuma, vai arī iegūt to no cita elektronisko rēķinu izrakstīšanas līdzekļa.

Veidojot elektronisko rēķinu izrakstīšanas līdzekli no jauna, manuāli jāpievieno EP komponenti (piemēram, līdzekļa versiju konfigurācijas un citas konfigurācijas, piemēram, līdzekļa versijas iestatīšana un programmas iestatīšana). Kad tiek izveidota funkcija, iegūstot to no citas funkcijas, jaunā funkcija manto visas konfigurācijas no sākotnējās. 

## <a name="electronic-invoicing-feature-version"></a>Elektroniskās rēķinu izrakstīšanas funkcijas versija

Elektroniskās rēķinu izrakstīšanas funkcijām ir versijas. Veidojot jaunu versiju, versijas numurs tiek automātiski palielināts. Jaunajai versijai var definēt datumu "spēkā no".

Elektronisko rēķinu izrakstīšanas līdzekļa versijas seko dzīves ciklam, kam var būt trīs statusi:

- **Melnraksts** – ja funkcijas versija ir ar šo statusu, varat labot tās konfigurācijas atribūtus un jebkuru no tās artefaktiem (piemēram, faila formāta konfigurācijas).
- **Pabeigts** - ja funkcijas versija ir ar šo statusu, tā ir publicēta Globālajā repozitorijā, kas ir saistīts ar jūsu organizāciju. Funkcijas versiju vai jebkuru no EP komponentiem vairs nevar rediģēt.
- **Publicēts** - ja funkcijas versija ir ar šo statusu, tā ir publicēta Elektronisko rēķinu izrakstīšanas pievienojumprogrammā. Funkcijas versiju vai jebkuru no EP komponentiem vairs nevar rediģēt.

### <a name="feature-configurations"></a>Līdzekļa konfigurācijas

Līdzekļu konfigurācijās ir visas EP formāta konfigurācijas, ko izmanto elektroniskās rēķinu izrakstīšanas funkcijas. Visi elektroniskie faili, ko izmanto elektronisko rēķinu izrakstīšanas funkcija apstrādes laikā, nāk no formāta konfigurācijām, kas pievienotas šī līdzekļa funkciju konfigurācijām.

No funkciju konfigurācijām varat piekļūt EP formāta veidotājam, kas ir EP rīks, ko izmanto formāta konfigurāciju izveidošanai.

### <a name="feature-setup"></a>Līdzekļa iestatīšana

Līdzekļa iestatījumi tiek izmantoti kombinācijā ar līdzekļa konfigurācijām. Katrā funkciju iestatījumā ir ietvertas darbību kopas, piemērojamības noteikumi un mainīgie, kas nodrošina paredzamās darbības, lai elektronisko rēķinu izrakstīšanas funkcija atbilstu noteiktai elektroniskā rēķina prasībai.

### <a name="application-setup"></a>Programmas iestatījumi

Programmas iestatījumam ir jābūt saistītam ar iepriekš izveidotu pievienoto programmu.

Izmantojot programmas iestatījumus, jūs varat konfigurēt daļu no elektronisko rēķinu izrakstīšanas funkcijas, kas jāveic Finance un Supply Chain Management instancēs. Vismaz trīs konfigurējami komponenti ir obligāti, neatkarīgi no elektronisko rēķinu izrakstīšanas funkcijas:

- **Tabulas nosaukums** – Finance un Supply Chain Management elements, kurā atrodas grāmatotie rēķini un uz kā ir balstīta elektronisko rēķinu izrakstīšanas funkcija.
- **Konteksts** - rēķina konteksta modeļa nosaukums, kas tika konfigurēts, izmantojot EP.
- **Biznesa dokumenta kartēšana** - rēķina kartēšanas modeļa nosaukums, kas tika konfigurēts, izmantojot EP.

> [!IMPORTANT]
> Konfigurāciju, kas ir ievadīta programmas iestatījumā, var skatīt Finance un Supply Chain Management instancēs. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametrs**. Cilnē **Elektronisks dokuments** atlasiet **Izvietot** un pēc tam atlasiet opciju **Savienotā programma**.

### <a name="deploying-feature-versions"></a>Līdzekļa versiju izvietošana

Pakalpojumā RCS izmantojiet komandu **Izvietot**, lai publicētu elektronisko rēķinu izrakstīšanas līdzekļa versiju. Atlasiet **Izvietot** un pēc tam atlasiet vienu no šīm opcijām, lai definētu izvietošanas mērķi: 

- **Pakalpojuma vide** – kad izvietošanas mērķis ir pakalpojumu vide, elektroniskā rēķina līdzekļa versija tiek publicēta pakalpojuma vidē. Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir gatava saņemt un apstrādāt elektroniskos dokumentus, ko sūta Finance un Supply Chain Management instances.
- **Saistītā programma** - Kad izvietošanas mērķis ir saistītā programma, konfigurācija, ko nodrošina programmas iestatīšana, tiek rakstīta Finance un Supply Chain Management instancēs, kas iepriekš saistīta ar to.

Tikai elektronisko rēķinu izrakstīšanas līdzekļu versijas ar statusu **Pabeigts** var izvietot pakalpojumu vidē vai savienotā programmā.

### <a name="removing-feature-versions"></a>Līdzekļa versiju noņemšana

Pakalpojumā RCS izmantojiet komandu **Atcelt izvietošanu**, lai noņemtu noteiktu elektronisko rēķinu izrakstīšanas līdzekļa versiju no pakalpojumu vides Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.

> [!IMPORTANT]
> Komanda **Atcelt izvietošanu** darbojas tikai pakalpojumu vidēs. Tā nenoņem elektronisko rēķinu izrakstīšanas līdzekļu versijas no savienotajām pievienojumprogrammām.

### <a name="rebasing-electronic-invoicing-features"></a>Elektronisko rēķinu izrakstīšanas funkcijas pārvērtēšana

Kad viens elektroniskais rēķinu izrakstīšanas līdzeklis ir atvasināts no cita, komanda **Pārvērtēt** atjaunina atvasināto līdzekli ar izmaiņām, kas ieviestas sākotnējā funkcionalitātē.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
