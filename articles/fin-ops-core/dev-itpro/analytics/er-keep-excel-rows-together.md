---
title: Veidot ER formātu, lai rindas paturētu kopā vienā Excel lapā
description: Šajā tēmā skaidrots, kā projektēt elektronisko pārskatu (ER) formātu, kas uztur rindas kopā vienā Microsoft Excel lapā.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 06782a4933fb5c3e86ad436b853f207fd3d5cddb
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612375"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Veidot ER formātu, lai rindas paturētu kopā vienā Excel lapā

[!include [banner](../includes/banner.md)]


Šajā tēmā skaidrots, kā lietotājs sistēmas administratora vai elektronisko pārskatu veidošanas funkcionālo konsultanta lomā var konfigurēt elektronisko pārskatu (ER) [...](general-electronic-reporting.md)[formātu, kas ģenerē izejošos](er-overview-components.md#format-component) dokumentus un pārvalda dokumenta lapu tā, lai izveidotās Microsoft Excel rindas būtu tajā pašā lapā.

Šajā piemērā tiks modificēts Microsoft nodrošinātais ER formāts, kas tiek izmantots brīva teksta rēķinu drukāšanai programmā Excel. Modifikācijas ļaus pārvaldīt ģenerētā brīvā teksta rēķina pārskata lapu tā, lai visas atsevišķas rēķina rindas rindas pēc iespējas būtu vienā lapā.

Šīs tēmas procedūras var pabeigt **USMF** uzņēmumā. Kodēšana nav nepieciešama.

Šajā piemērā izveidojat nepieciešamās ER konfigurācijas [uzņēmumam](general-electronic-reporting.md#Configuration)**Litware, Inc.** sample. Pārliecinieties, vai **Litware, Inc.** (`http://www.litware.com`) parauga uzņēmuma konfigurācijas nodrošinātājs ir norādīts ER struktūrā un vai tas ir atzīmēts kā **aktīvs**. Ja šī konfigurācijas nodrošinātāja nav **uzskaitīts** vai arī tas nav atzīmēts kā aktīvs, [izpildiet darbības, kas norādītas Sadaļā Konfigurācijas nodrošinātāja izveide un atzīmējiet to kā aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Ievadīt jaunu brīva teksta rēķinu

1. Izpildiet darbības, kas [sadaļā Izveidot brīva teksta rēķinu](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1), lai pievienotu brīva teksta rēķinu.

    1. Pievienot rēķinam vienu rindu.
    2. Pievienojiet piecas piezīmes rēķina rindai.

    ![Pārskata rēķina rindas piezīmes pielikumu lapā.](./media/er-keep-excel-rows-together-notes.png)

2. Sekojiet darbībām, [kas jāveic](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) kopēšanas rindās, lai izveidotu piecas papildu rēķina rindas, kas kopē rēķina rindu, kuru pievienojāt iepriekšējā darbībā.

    ![Brīvā teksta rēķina rindu pārskatīšana brīvā teksta rēķina lapā.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šī iestatīšana jāpabeidz, pirms varat sākt izmantot ER struktūru, lai veidotu standarta ER formāta pielāgotu versiju.

## <a name="import-the-standard-er-format-configuration"></a>Standarta ER formāta konfigurācijas importēšana

Izpildiet darbības [standarta ER](er-quick-start2-customize-report.md#ImportERSolution1) formāta konfigurācijas importēšanai, lai pievienotu standarta ER konfigurācijas pašreizējai Dynamics 365 finanšu instancei. Piemēram, brīvā teksta rēķina **(Excel)** formāta konfigurācijas importa versija 252.116 **·**. Pamata rēķina **modeļa konfigurācijas pamat versija 252** **tiek** automātiski importēta no repozitorija kopā ar nepieciešamo rēķina **modeļa kartēšanas** konfigurāciju.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Iestatīt drukas pārvaldību, lai lietotu standarta ER formātu

Izpildiet sadaļā Iestatīt [drukas](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1)**pārvaldību** norādītās darbības, lai konfigurētu debitoru parādu moduļa drukas pārvaldību, tādējādi standarta ER formāts tiek izmantots brīva teksta rēķinu drukāšanai.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Konfigurēt formāta mērķi standarta ER formātam

[...](er-quick-start1-new-solution.md#ConfigureDestination)[Izpildiet](er-destination-type-screen.md) darbības, kas jāveic, lai konfigurētu formāta mērķi ekrānā redzamais priekšskatījums, lai konfigurētu standarta ER formāta ekrāna ER mērķi, tādējādi ģenerētie pārskati tiek pārvērsti PDF formātā un priekšskatīti jaunā pārlūka cilnē.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Drukāt brīva teksta rēķinu, izmantojot standarta ER formātu

1. Lai pievienotā rēķinam [izveidotu brīvā teksta rēķina](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) pārskatu Excel formātā, izpildiet darbības, kas jāveic brīva teksta rēķina izdrukā, izmantojot standarta ER formātu.
2. Lejupielādējiet ģenerēto Excel darbgrāmatu un pārskatiet to Excel darbvirsmas programmā.

    Ievērojiet, ka rēķina 6. rinda sākas pārskata pirmajā lapā un turpinās otrajā lapā. Pēdējā piezīme parādās otrajā lapā, un tā nav tur, ka tā pieder 6. rēķina rindai. Tāpēc lappuses pārtraukums rēķina rindas satura vidū padara šo dokumentu vieglāk lasāmu.

    ![Pārskatiet ģenerētā brīvā teksta rēķina lapošanu Excel darbvirsmas programmā.](./media/er-keep-excel-rows-together-invoice1.gif)

Šajā tēmā atlikušās procedūras parāda, kā jūs variet noregulēt standarta ER formātu, lai uzlabotu rēķina pārskata izskatu un lasāmību, uzturot visu vienas rēķina rindas saturu tajā pašā lapā.

## <a name="create-a-custom-format"></a>Pielāgota formāta izveidošana

Izpildiet [sadaļā](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) Pielāgots formāts norādītās darbības, lai izgūtu formātu no importētā ER **formāta, un izveidojiet brīva teksta rēķina (Excel)** pielāgotu ER konfigurāciju, kas ir pieejama rediģēšanai un modificēšanai.

## <a name="edit-the-custom-format"></a>Pielāgotā formāta rediģēšana

1. Izpildiet sadaļā Pielāgots [formāts norādītās darbības,](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) lai atvērtu atvasināto ER formātu labošanai ER formāta veidotājā.
2. Formāta veidotāja **lapā** formāta komponentu kokā kreisajā rūtī **izvērsiet Brīvā teksta rēķina \>\> lapas InvoiceLines** **un atlasiet InvoiceLines_Values** komponentu.
3. Cilnē Formāts **iestatiet** opciju Paturēt rindas **kopā** uz **Jā**.

    ![Redi?ējamā ER formāta opcijas Paturēt rindas iestatīšana formāta veidotāja lapā.](./media/er-keep-excel-rows-together-format.png)

4. Atlasiet **Saglabāt** un aizveriet lapu.

## <a name="mark-the-custom-format-as-runnable"></a>Pielāgota formāta atzīmēšana kā izpildāms

Izpildiet darbības, [kas jāveic sadaļā Pielāgotais formāts,](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) kā palaižamo, lai pielāgoto ER formāta modificēto versiju padarītu palaižamu.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Iestatīt drukas pārvaldību, lai lietotu pielāgoto ER formātu

Izpildiet sadaļā [Iestatīt](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2)**drukas** pārvaldību norādītās darbības, lai konfigurētu debitoru parādu moduļa drukas pārvaldību, tādējādi pielāgotais ER formāts tiek lietots brīva teksta rēķinu drukāšanai.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Konfigurēt formāta mērķi pielāgotajam ER formātam

[...](er-quick-start1-new-solution.md#ConfigureDestination)**Izpildiet** darbības, kas jāveic, lai konfigurētu formāta mērķi ekrānā redzamais priekšskatījums, lai konfigurētu pielāgotā ER formāta ekrāna ER mērķi, tādējādi ģenerētie pārskati tiek pārvērsti PDF formātā un priekšskatīti jaunā pārlūka cilnē.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Drukāt brīva teksta rēķinu, izmantojot pielagoto ER formātu

1. Lai pievienotajam rēķinam [izveidotu brīvā teksta rēķina](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) pārskatu Excel formātā, izpildiet darbības, kas jāveic brīva teksta rēķina drukāšanai, izmantojot pielāgotu ER formātu.
2. Lejupielādējiet ģenerēto Excel darbgrāmatu un pārskatiet to Excel darbvirsmas programmā.

    Ievērojiet, ka rēķina 6. rinda sākas otrajā lapā, un visas Excel rindas, kas apzīmē šo rēķina rindu, tiek parādītas kopā šajā lapā.

    ![Pārskatot ģenerētā brīvā teksta rēķina atjaunināto lapu Excel darbvirsmas programmā.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Papildu resursi

[Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
