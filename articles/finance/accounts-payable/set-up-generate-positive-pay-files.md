---
title: Pozitīvo maksājumu failu iestatīšana un izveidošana
description: Šajā rakstā ir izskaidrots, kā iestatīt pozitīvo maksājumu un izveidot pozitīvo maksājumu failus.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: d54e246b175c81b5d161ea35f141fc7dea9c6f1f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070730"
---
# <a name="set-up-and-generate-positive-pay-files"></a>Pozitīvo maksājumu failu iestatīšana un ģenerēšana

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šī funkcionalitāte tiks nolietota 2022. gada septembrī, jaunajiem lietotājiem būs jāizmanto elektroniskie pārskati. Papildinformāciju skatiet pozitīvo [maksājumu failu iestatīšana, izmantojot elektroniskos pārskatus](set-up-positive-pay-er.md).

Šajā rakstā ir izskaidrots, kā iestatīt pozitīvo maksājumu un izveidot pozitīvo maksājumu failus. 

Iestatiet pozitīvo maksājumu, lai izveidotu elektronisku čeku sarakstu, kas tiek iesniegts bankai. Kad čeks ir iesniegts bankai, banka to salīdzina ar čeku sarakstu. Ja čeks atbilst čekam sarakstā, banka to dzēš. Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.

## <a name="security-for-positive-pay-files"></a>Pozitīvā maksājuma failu drošība
Pozitīvo maksājumu faili var saturēt konfidenciālu informāciju par maksājumu saņēmējiem un čeku summām. Šī iemesla dēļ nodrošiniet, lai no failu ģenerēšanas, līdz to saņemšanai bankā, tiek veikti atbilstoši drošības pasākumi. Pozitīvo maksājumu faili tiek lejupielādēti atrašanās vietā, kas ir norādīta tīmekļa pārlūkprogrammā. Tā kā pozitīvo maksājumu faili var saturēt jutīgu informāciju, ir svarīgi, lai tikai autorizētiem lietotājiem būtu piekļuve šīs Microsoft Dynamics informācijas ģenerēšanu un skatīšanu 365 Finansēs. Izmantojiet nākamo tabulu, kas palīdzēs noskaidrot nepieciešamās privilēģijas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Uzdevums</th>
<th>Privilēģija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izveidot pozitīvo maksājumu failus, izmantojot sarakstu lapu <strong>Bankas konti</strong> vai lapu <strong>Bankas konti</strong>.</td>
<td><ul>
<li><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un bankas kontiem, izmantojot lapu <strong>Izveidot pozitīvā maksājuma failu</strong>.</td>
<td><ul>
<li><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skatīt pozitīvo maksājumu failus lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</td>
<td><strong>Skatīt vairākām juridiskām personām izveidotos bankas pozitīvo maksājumu datus</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Apstiprināt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</td>
<td><strong>Apstiprināt pozitīvā maksājuma failu</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Atsaukt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma faila kopsavilkums</strong>.</td>
<td><strong>Atsaukt pozitīvā maksājuma failu</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Iestatīt pozitīvā maksājuma formātu
Pozitīvā maksājuma faili tiek izveidoti, izmantojot datu elementus. Lai varētu ģenerēt pozitīvā maksājuma failu, vispirms ir jāiestata transformācijas ievades formāts, kas tiks izmantots, lai pārvērstu čeka datus formātā, kas ir saprotams bankai. Lapā **Pozitīvā maksājuma formāts** var izveidot faila formāta identifikatoru un aprakstu. Jāizmanto XML veida transformācijas ievades formāts Konkrēts formāts ir atkarīgs no izmantotā transformācijas faila. Piemēram, pieejamais parauga paplašināmās stila lapas valodas transformācijas (XSLT) fails izmanto formātu **XML elements**. Izmantojiet darbību **Augšupielādēt transformācijai izmantojamo failu**, lai norādītu bankai nepieciešamā formāta transformācijas faila atrašanās vietu.

## <a name="example-xslt-file-for-positive-pay-file"></a>Piemērs: pozitīvā maksājuma faila XSLT fails.

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

> [!NOTE]
> XML nosaukumiem XSLT ir jāatbilst XML mezglu apvalkam. Gan XSLT, gan XML faili ir reģistrjutīgi. 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Piešķirt pozitīvā maksājuma formātu bankas kontam
Katram bankas kontam, kuram vēlaties izveidot pozitīvā maksājuma datus, ir jāpiešķir iepriekšējā sadaļā norādīto pozitīvā maksājuma formāts. Lapā **Bankas konti** atlasiet pozitīvā maksājuma formātu, kas atbilst bankas kontam. Laukā **Pozitīvā maksājuma sākuma datums** ievadiet pozitīvo maksājumu failu izveides sākuma datumu. Šajā laukā obligāti jāievada datums. Pretējā gadījumā pirmais izveidotais pozitīvā maksājuma fails ietvers visus čekus, kas jebkad ir izveidoti šim bankas kontam.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Piešķirt pozitīvo maksājumu failu numerāciju
Katram pozitīvo maksājumu failam ir nepieciešams unikāls numurs. Izmantojiet cilni **Numerācija** lapā **Skaidras naudas un bankas pārvaldības parametri**, lai izveidotu pozitīvo maksājumu failu numerāciju.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Izveidot pozitīvā maksājuma failu vienam bankas kontam
Pozitīvā maksājuma failu var izveidot vienai juridiskajai personai un vienam bankas kontam. Lai iegūtu informāciju par to, kā vienlaicīgi izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un banku kontiem, skatiet nākamo sadaļu. Lai izveidotu pozitīvā maksājuma failu vienai juridiskajai personai un vienam bankas kontam, atveriet dialoglodziņu **Izveidot pozitīvā maksājuma failu** lapā **Bankas konti**. Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā. Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Izveidot pozitīvā maksājuma failu vairākiem bankas kontam
Lai izveidotu pozitīvā maksājuma failu vairākiem bankas kontiem, izmantojiet periodisko uzdevumu **Izveidot pozitīvā maksājuma failu**. Atlasiet pozitīvā maksājuma faila formātu un norādiet, vai izveidot failu visām juridiskajām personām vai tikai atlasītajai juridiskajai personai. Var izveidot arī pozitīvā maksājuma failu visiem bankas kontiem, kas izmanto norādīto pozitīvā maksājuma formātu, vai tikai atlasītajam bankas kontam. Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā. Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Skatīt pozitīvā maksājuma faila izveides rezultātus
Kad pozitīvā maksājuma fails ir izveidots, lapā **Pozitīvā maksājuma faila kopsavilkums** var skatīt rezultātus. Lai skatītu detalizētu informāciju par atsevišķiem čekiem, izmantojiet detalizētās informācijas lapu **Pozitīvā maksājuma fails**.

## <a name="confirm-a-positive-pay-file"></a>Pozitīvā maksājuma faila apstiprināšana
Kad čeki ir ievietoti sarakstā un pozitīvā maksājuma fails ir apmaksāts, banka jums nosūta apstiprinājuma numuru. Pēc tam pozitīvā maksājuma failu var apstiprināt. Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Ievadīt apstiprinājumu**. Apstiprinot pozitīvā maksājuma failu, tiek reģistrēts no bankas saņemtais apstiprinājuma numurs.

## <a name="recall-a-positive-pay-file"></a>Pozitīva maksājuma faila atsaukšana
Ja pozitīvā maksājuma fails ir jāmaina, to var atsaukt. Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Atsaukt**. Katrā pozitīvā maksājuma failā tiek atiestatīts lauks, kas norāda, vai šis čeks ir iekļauts pozitīvā maksājuma failā. Pēc tam var izveidot jaunu pozitīvā maksājuma failu, kurā ir iekļauts atsauktais čeks.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
