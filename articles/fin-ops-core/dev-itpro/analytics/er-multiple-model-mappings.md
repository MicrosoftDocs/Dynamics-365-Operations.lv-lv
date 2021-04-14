---
title: Pārvaldīt vairākus atvasinātos kartējumus viena modeļa saknei
description: Šajā tēmā skaidrots, kā pārvaldīt vairākus atvasinātus kartējumus, kas tika konfigurēti atsevišķam modeļa saknei.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a774a0edf00a17be674b7a1bb07f6494e90554c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743683"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Pārvaldīt vairākus atvasinātos kartējumus viena modeļa saknei

[!include [banner](../includes/banner.md)]

[Elektronisko pārskatu (ER)](general-electronic-reporting.md) datu [modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) komponents tiek izmantots katrā konfigurētajā ER [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentā kā datu avots izejošo dokumentu ģenerēšanai. Lai aprakstītu vienu biznesa domēnu, konfigurējiet datu modeļa komponentu, kam ir daudz saknes definīciju. 

Katra saknes definīcija ļauj jums attēlot šī domēna datus tādā veidā, kas ir piemērots īpašiem pārskatu nolūkiem. Katrai saknes definīcijai jūs varat konfigurēt ER [modeļa kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu kā Microsoft Dynamics 365 Finance specifisku datu modeļa implementēšanu. Šādā veidā aprakstiet, kā izpildlaikā tiks aizpildīts datu modelis.

ER modeļa kartēšanas komponenti var atrasties ER datu modeļa [konfigurācijās](general-electronic-reporting.md#Configuration) un ER modeļa kartēšanas konfigurācijās. Viena ER konfigurācija var ietvert daudzus kartēšanas komponentus, katrs no tiem ir konfigurēts vienai saknes definīcijai. Viena ER konfigurācija var ietvert daudzus kartēšanas komponentus, katrs no tiem ir konfigurēts vienai saknes definīcijai.

Daudzi konfigurācijas nodrošinātāji var piedāvāt ER modeļa kartēšanas konfigurācijas tam pašam ER datu modelim. Šīs modeļa kartēšanas konfigurācijas var ietvert kartēšanas komponentus dažādām saknes definīcijām. Jūs varat izmantot modeļa kartējumu vienai saknes definīcijai, ko piedāvā viens [nodrošinātājs](general-electronic-reporting.md#Provider), un izmantot modeļa kartēšanu citai saknes definīcijai, ko piedāvā cits nodrošinātājs.

Šīs tēmas procedūrās skaidrots, kā pārvaldīt vairākas ER modeļa kartēšanas konfigurācijas no ER datu modeļa, ja tās satur dažādus modeļu kartēšanas komponentus, kas konfigurēti tai pašai saknes definīcijai. 

Lai pabeigtu šajā tēmā minētās darbības, ir jābūt piešķirtai sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.

Visas tālāk norādītās procedūras var veikt uzņēmumā USMF. Kodēšana nav nepieciešama.

## <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Kā lietotājam Elektronisko pārskatu attīstības lomā, jums ir [jākonfigurē minimāls ER parametru kopums](er-quick-start2-customize-report.md#ConfigureFramework), pirms varat sākt izmantot ER struktūru, lai veidotu jaunu ER risinājumu.

## <a name="import-the-standard-er-format-configurations"></a>Standarta ER formāta konfigurāciju importēšana

Lai pievienotu standarta ER konfigurācijas savai pašreizējai Finance instancei, jums tās ir jāimportē no ER repozitorija, kas konfigurēts šai instancei. Veiciet darbības, kas jāveic, [lejupielādējot ER konfigurācijas no konfigurācijas pakalpojuma Globālā repozitorija,](er-download-configurations-global-repo.md), lai importētu šādas ER formāta konfigurācijas:

- **Brīva teksta rēķins** (Excel), versija 220.106
- **Projekta rēķins** (Excel), versija 226.27

## <a name="review-the-imported-er-configurations"></a>Importēto ER konfigurāciju pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**.

    ![Importētās konfigurācijas pārskatīšana Konfigurāciju lapā](./media/er-multiple-model-mappings-image1.png)

4. Pārskatiet **Brīvā teksta rēķina (Excel)** formātu:

    1. Konfigurācijas koka skata kreisajā rūtī atlasiet **Brīva teksta rēķins (Excel)**.
    2. Darbību rūtī atlasiet **Noformētājs**.
    3. Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet datu avotu sarakstā **Modelis**.
    4. Atlasiet **Skatīt**.
    
       Thecurrent ER formāts ir konfigurēts **Rēķina modeļa** saknes definīcijas **InvoiceCustomer** izmantošanai. Kad šis formāts tiek palaists un tiek izsaukts **Modeļa** datu avots, modeļa kartēšana, kas ir konfigurēta **InvoiceCustomer** saknes definīcijai, tiek izmantota, lai piekļūtu programmas datiem un aizpildītu datu modeli.

        ![Datu avota pārskatīšana lapā Formāta noformētājs](./media/er-multiple-model-mappings-image2.png)

    6. Aizveriet lapu **Formāta veidotājs**.

5. Pārskatiet **Rēķina modeļa kartēšanas** konfigurācijas saturu:

    1. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modeļa kartēšana**.
    2. Darbību rūtī atlasiet **Noformētājs**.
    3. Lapā **Modelis datu avota kartēšanai** ievērojiet, ka pašreizējā ER modeļa kartēšanas konfigurācijā ir vairāki modeļa kartēšanas komponenti:

        + **Debitora rēķina** modeļa kartēšana ir konfigurēta **InvoiceCustomer** saknes **Rēķina modeļa** definīcijai. Tāpēc, kad darbojas **Brīvā teksta rēķina (Excel)** ER formāts, šīs ER konfigurācijas **Debitora rēķina** modeļa kartēšanu var izvēlēties, lai piekļūtu programmas datiem un aizpildītu datu modeli.
        + **Debitora rēķina** modeļa kartēšana ir konfigurēta **InvoiceCustomer** saknes **Rēķina modeļa** definīcijai. Tāpēc, kad darbojas **Brīvā teksta rēķina (Excel)** ER formāts, šīs ER konfigurācijas **Debitora rēķina** modeļa kartēšanu var izvēlēties, lai piekļūtu programmas datiem un aizpildītu datu modeli.

        ![Rēkinu modeļa kartēšana Modeļa datu avotu kartēšanas lapā](./media/er-multiple-model-mappings-image3.png)

    4. Aizveriet lapu **Datu avota kartējuma modelis**.
    5. Kopsavilkuma cilnē **Versijas** atlasiet **Dzēst**, lai dzēstu visas tās ER konfigurācijas versijas, kas ir jaunākas par versiju 240.175.

6. Pārskatiet **Projekta rēķina modeļa kartēšanas (RDP)** konfigurācijas saturu:

    1. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modeļa kartēšana**.
    2. Darbību rūtī atlasiet **Noformētājs**.
    3. Lapā **Modelis uz datu avotu kartēšanu** ievērojiet, ka pašreizējā ER modeļa kartēšanas konfigurācija ietver **InvoiceProject** modeļa kartējumu un ka šī modeļa kartēšana ir konfigurēta rēķina modeļa **InvoiceProject** saknes **InvoiceProject** definīcijai. Tāpēc, kad darbojas **Brīvā teksta rēķina (Excel)** ER formāts, atlasiet ER konfigurācijas **InvoiceProject** modeļa kartēšanu, lai piekļūtu programmas datiem un aizpildītu datu modeli.

        ![Projektu rēķinu modeļa kartēšana Modeļa datu avotu kartēšanas lapā](./media/er-multiple-model-mappings-image4.png)

    4. Aizveriet lapu **Datu avota kartējuma modelis**.
    5. Kopsavilkuma cilnē **Versijas** atlasiet **Dzēst**, lai dzēstu visas tās ER konfigurācijas versijas, kas ir vēlākas par versiju 226.35.

## <a name="customize-the-imported-er-configurations"></a>Importēto ER konfigurāciju pielāgošana

Šajā sadaļā skaidrots, kā [pielāgot](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) Microsoft nodrošinātos modeļu kartējumus. Piemēram, pielāgošanai var būt nepieciešams ieviest pielāgoto loģiku vai pievienot trūkstošos saistījumus.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Rēķinu modeļa kartēšanas konfigurācijas pielāgošana

1. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī atlasiet **Rēķina modeļa kartēšana**.
2. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
3. Nolaižamajā dialoglodziņā **Izveidot konfigurāciju**, laukā **Jauns** atlasiet **Atvasināt no nosaukuma: Rēķinu modeļa kartēšana, Microsoft**.
4. Laukā **Nosaukums** ievadiet **Rēķina modeļa kartēšana Litware**.
5. Atlasiet **Izveidot konfigurāciju**.
6. [Atzīmējiet](er-quick-start2-customize-report.md#MarkFormatRunnable) atvasinātā kartējuma [melnraksta](general-electronic-reporting.md#component-versioning) versiju kā pieejamu lietošanai izpildlaikā:

    1. Darbību rūts cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet **Lietotāja parametri**.
    2. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.
    3. Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.
    4. **Rēķina modeļa kartēšanas Litware** konfigurācijai, kas pašlaik ir atlasīta konfigurācijas kokā, iestatiet opciju **Palaist melnrakstu** uz **Jā**.

7. Darbību rūtī atlasiet **Veidotājs**, lai pārskatītu šīs konfigurācijas modeļa kartējumus.

    ![Projektu rēķinu modeļa kartēšanas pārskatīšana Modeļa datu avotu kartēšanas lapā](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Tagad varat atvērt jebkuru no šī ER konfigurācijas ER modeļa kartēšanas komponentiem veidotājā, lai konfigurētu savu pielāgoto loģiku. Papildinformāciju skatiet modeļa [Kartēšanas konfigurācijas pielāgošana](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Aizveriet lapu **Datu avota kartējuma modelis**.

Tagad ir **Rēķinu modeļu kartēšana** un **Rēķina modeļa kartēšanas Litware** konfigurācijas, kur katrai no tām ir modeļa kartēšana, kas ir konfigurēta **InvoiceCustomer** saknes definīcijai. Skaidri piešķiriet vienu no modeļa kartējumiem kā noklusējuma modeļa kartēšanu, ko izmanto kāds no ER formātiem, piemēram, **Brīva teksta rēķina (Excel)** formāts, kas ietver modeļa datu avotu, kam ir **InvoiceCustomer** saknes definīcija. Pretējā gadījumā, palaižot, rediģējot vai validējot kādu no ER formātiem, tiek parādīts šāds izņēmums, lai jūs paziņotu, ka neviens noklusējuma modeļa kartējums nav skaidri piešķirts:
 
> Konfigurācijās datu modelim pastāv vairāk '\<model name\> (\<root descriptor\>)' nekā viens modeļa \<configuration names separated by commas\>kartējums. Iestatiet vienu no konfigurācijām kā noklusējumu.

![Atver formātu rediģēšanai konfigurāciju lapā](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Projekta rēķinu modeļa kartēšanas (RDP) konfigurācijas pielāgošana

1. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī atlasiet **Projekta rēķina modeļa kartēšana (RDP)**.
2. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
3. Nolaižamajā dialoglodziņā **Izveidot konfigurāciju**, laukā **Jauns** atlasiet **Atvasināt no nosaukuma: Rēķinu modeļa kartēšana (RDP), Microsoft**.
4. Laukā **Nosaukums** ievadiet **Rēķina modeļa kartēšana (Litware)**.
5. Atlasiet **Izveidot konfigurāciju**.
6. **Rēķina modeļa kartēšanas Litware** konfigurācijai, kas pašlaik ir atlasīta konfigurācijas kokā, iestatiet opciju **Palaist melnrakstu** uz **Jā**.
7. Darbību rūtī atlasiet **Veidotājs**, lai pārskatītu šīs konfigurācijas modeļa kartējumus.

    ![Projektu rēķinu modeļa kartēšanas pārskatīšana Modeļa datu avotu kartēšanas lapā](./media/er-multiple-model-mappings-image7.png)

8. Aizveriet lapu **Datu avota kartējuma modelis**.

Tagad ir **Rēķina modeļa kartēšana**, **Projekta rēķina modeļa kartēšana (RDP)** un **Projekta rēķina modeļa kartēšana Litware** konfigurācijas. Katrai no šīm konfigurācijām ir modeļa kartēšana, kas konfigurēta **invoiceProject** saknes definīcijai. Skaidri piešķiriet vienu no modeļa kartējumiem kā noklusējuma modeļa kartējumu, ko izmanto kāds no ER formātiem. Piemēram, izmantojiet **Projekta rēķina (Excel)** formātu, kas satur modeļa datu avotu, kam ir **InvoiceProject** saknes definīcija. Pretējā gadījumā, palaižot, rediģējot vai validējot kādu no ER formātiem, tiek parādīts šāds izņēmums, lai jūs paziņotu, ka neviens noklusējuma modeļa kartējums nav skaidri piešķirts:

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Atlasiet atvasinātā Rēķina modeļa kartēšanas Litware konfigurāciju kā konfigurāciju, kas ietver noklusējuma modeļa kartējumus

1. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī atlasiet **Rēķina modeļa kartēšana Litware**.
2. Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.

    ![Modeļa kartēšanas iestatīšana kā noklusējuma modeļa kartēšana lapā Konfigurācijas](./media/er-multiple-model-mappings-image8.png)

    Šī iestatījuma dēļ **Debitora rēķina kopijas** modeļa kartēšana tiek izmantota, palaižot **Brīvā teksta rēķinu (Excel)** vai labojot, vai validējot to. **Debitoru rēķina** modeļa kartēšana no **Debitora rēķina modeļa kartēšanas** tiek ignorēta.

    Tagad varat atvērt **Brīvā teksta rēķina (Excel)** formātu pārskatīšanai formāta veidotājā.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Atlasiet atvasinātā Rēķina modeļa kartēšanas Litware konfigurāciju kā konfigurāciju, kas ietver noklusējuma modeļa kartējumus

1. Lapā **Konfigurācijas** konfigurācijas koka skata kreisajā rūtī atlasiet **Rēķina modeļa kartēšana Litware**.
2. Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.

    Šajā gadījumā atšķirībā no gadījuma, kas ir aprakstīts **Rēķinu modeļa kartēšanas Litware** konfigurācijai iepriekšējā sadaļā, jūs nevarat sākt izmantot **InvoiceProject kopijas** modeļa kartējumu no **Projekta rēķina modeļa kartēšanas Litware** konfigurācijas. Divas konfigurācijas, kurās ir modeļa kartēšana **InvoiceProject** saknes definīcijai, pašlaik ir atzīmētas kā noklusējuma konfigurācija. Tāpēc to lietošanas prioritāte ir vienāda. Lai atrisinātu šo problēmu, izpildiet šīs procedūras atlikušos soļus.

3. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Rēķina modeļa kartēšana Litware**.
4. Darbību rūtī atlasiet **Noformētājs**.
5. Lapā **Modelis datu avota kartēšanai** atlasiet **Rediģēt**, lai padarītu lapu rediģējamu pēc nepieciešamības.
6. Atlasiet **Projekta rēķina kopēšanas** modeļa kartējumu un pēc tam atzīmējiet izvēles rūtiņu **Dzēsts**.

    ![Modeļa kartēšanas iestatīšana kā faktiski dzēsta Modeļa datu avota kartēšanas lapā](./media/er-multiple-model-mappings-image9.png)

    Šī iestatījuma dēļ **Rēķina modeļa kartēšanas Litware** konfigurācija tiek apstrādāta, it kā tai nav modeļa kartēšanas **InvoiceProject** saknes definīcijai. **InvoiceProject kopijas** modeļa kartējums, kas izdots pēc noklusējuma. Konfigurācija **Rēķina modeļa kartēšanas Litware**, kas ietver noklusējuma modeļa kartējumus, ir atzīmēta kā noklusējuma konfigurācija. Tā kā šī vērtība ir atzīmēta kā noklusētā, tai ir augstāka prioritāte nekā **InvoiceProject** modeļa kartēšanai no **Projekta rēķina modeļa kartēšanas (RDP)** konfigurācijas.

## <a name="other-considerations"></a>Citi apsvērumi

**InvoiceProject kopijas** modeļa kartēšana konfigurācijai **Projekta rēķina modeļa kartēšanas Litware**, lai izmantotu **ReportDataProvider** datu avotu. Datu avots ir daļa no tipa *Objekts*, kas attiecas uz programmas klasi **PsaProjInvoiceDP**. Šī klase ir ieviesta kā datu nodrošinātājs projekta rēķina SQL Server pārskatu izveides pakalpojumu (SSRS) pārskatam drukas pārvaldības struktūrā. Atlasiet šo datu avotu kā ER [integrācijas punktu](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Šis iestatījums tiek ņemts vērā, pašreizējā ER ieviešana drukas pārvaldības pārskatiem. Plašāku informāciju skatiet programmas klases **ERPrintMgmtDataProviderReport** avota kodā. Izpildlaikā **ReportDataProvider** datu avota piešķiršana kā modeļa kartēšanas integrācijas punkts liek pakalpojumam Finance apstrādāt šo kartēšanas komponentu ar lielāku prioritāti nekā **InvoiceProject** kartēšanas komponents no **Projekta rēķina modeļa kartēšanas (RDP)** konfigurācijas.

## <a name="see-also"></a>Skatiet arī

- [Elektronisko pārskatu modeļa kartēšanas pārvaldība atsevišķās elektronisko pārskatu konfigurācijās](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [No valsts konteksta atkarīgu elektronisko pārskatu modeļu kartējumu konfigurēšana](er-country-dependent-model-mapping.md)
- [Elektronisko pārskatu veidošanas (ER) API izmaiņas](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]