---
title: Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju
description: Šajā tēmā izskaidrots, kā atkļūdot izpildītā ER formāta datu avotus, lai labāk saprastu konfigurēto datu plūsmu un transformāciju.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ea8b99461ae741391198cc219651f6c2928f27daac94554ada3001f66674b78e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718457"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kad jūs [konfigurējat](tasks/er-format-configuration-2016-11.md) Elektronisko pārskatu veidošanas (ER) risinājumu, lai izveidotu izejošos dokumentus, jūs nosakat metodes, kas tiek izmantotas, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē. Lai nodrošinātu efektīvāku dzīves cikla atbalstu ER risinājumam, jūsu risinājumam jāsastāv no ER [datu modeļa](general-electronic-reporting.md#DataModelComponent) un tā [kartēšanas](general-electronic-reporting.md#ModelMappingComponent) komponentiem, kā arī ER [formāta](general-electronic-reporting.md#FormatComponentOutbound), un tās kartēšanas komponentiem, lai modeļa kartēšana būtu raksturīga lietojumprogrammai, turpretī citi komponenti saglabājas agnostiski programmā. Tāpēc vairāki ER komponenti var [ietekmēt](general-electronic-reporting.md#FormatComponentOutbound) datu ievades procesu ģenerētajā izvadē.

Dažkārt ģenerētās izvades dati izskatās citādi nekā tie paši dati programmas datu bāzē. Šādos gadījumos jums vēlēsieties noteikt, kurš ER komponents ir atbildīgs par datu pārveidošanu. ER datu avota atkļūdotāja līdzeklis ievērojami samazina šajā izmeklēšanā iesaistīto laiku un izmaksas. Jūs varat pārtraukt ER formāta izpildi un atvērt datu avota atkļūdotāja interfeisu. Tur varat pārlūkot pieejamos datu avotus un atlasīt atsevišķu datu avotu izpildei. Šī manuālā izpilde simulē datu avota izpildi, palaižot ER formāta patieso izpildi. Rezultāts ir parādīts lapā, kur varat analizēt saņemtos datus.

Lai ieslēgtu datu avota atkļūdošanas līdzekli, iestatiet opciju **Iespējot datu atkļūdošanu, kad formāts tiek palaists** uz **Jā** ER lietotāja parametros. Pēc tam varat sākt datu avota atkļūdošanu, kamēr tiek palaists ER formāts, lai izveidotu izejošos dokumentus. Jūs varat arī izmantot opciju **Sākt atkļūdošanu**, lai iniciētu datu avota atkļūdošanu ER formātā, kas ir konfigurēts [ER operāciju veidotājā](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Šī tēma sniedz vadlīnijas datu avota atkļūdošanas uzsākšanai izpildītiem ER formātiem. Tajā ir paskaidrots, kā informācija var palīdzēt saprast datu plūsmu un datu transformācijas. Šīs tēmas piemēri izmanto biznesa procesu kreditoru maksājumu apstrādei.

## <a name="limitations"></a>Ierobežojumi

Datu avota atkļūdotāju var izmantot, lai piekļūtu datu avotu datiem, kas tiek izmantoti ER formātos, kas tiek palaisti, lai ģenerētu izejošos dokumentus. To nevar izmantot, lai atkļūdotu datu avotus no ER formātiem, kas ir paredzēti, lai analizētu ienākošos dokumentus.

Šādi ER formātu iestatījumi pašlaik nav pieejami datu avota atkļūdošanai:

- Formātu pārveidošanas
- Apstiprināšanas noteikumu formatēšana un kartēšana
- Izteiksmju iespējošana
- Detalizēta informācija par atmiņas datu apkopošanu

## <a name="prerequisites"></a>Priekšnosacījumi

- Lai izpildītu šīs tēmas piemērus, jums ir jābūt piekļuvei vienai no šādām [lomām](../sysadmin/tasks/assign-users-security-roles.md):

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Uzņēmumam jābūt iestatītam uz **DEMF**.

- Izpildiet šīs tēmas [1. papildinājumā](#appendix1) norādītās darbības, lai lejupielādētu Microsoft ER risinājuma komponentus, kas nepieciešami, lai apstrādātu kreditoru maksājumus.
- Izpildiet šīs tēmas [2. papildinājumā](#appendix2) norādītās darbības, lai sagatavotu kreditoru maksājumu parādu apstrādi, izmantojot ER risinājumu, ko lejupielādēsit.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Apstrādāt kreditora maksājumu, lai iegūtu maksājuma failu

1. Izpildiet šīs tēmas [3. papildinājumā](#appendix3) norādītās darbības, lai apstrādātu kreditoru maksājumus.

    ![Kreditora maksājumu apstrāde notiek.](./media/er-data-debugger-process-payment.png)

2. Lejupielādējiet un saglabājiet zip failu vietējā datorā.
3. Izvelciet **ISO20022 Credit transfer.xml** maksājuma failu no zip faila.
4. Atveriet izgūto maksājuma failu, izmantojot XML failu skatītāju.

    Maksājuma failā bankas konta starptautiskais bankas konta numurs (IBAN) nesatur atstarpes. Tāpēc tas atšķiras no vērtības, kas tika [ievadīta](#enteredIBANcode) lapā **Bankas konti**.

    ![IBAN kods bez atstarpēm.](./media/er-data-debugger-payment-file.png)

    Jūs varat izmantot ER datu avota atkļūdotāju, lai uzzinātu, kurš ER risinājuma komponents tiek izmantots, lai saīsinātu atstarpes IBAN kodā.

## <a name="turn-on-data-source-debugging"></a>Ieslēgt datu avota atkļūdošanu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Iestatiet opciju **Iespējot datu atkļūdošanu, kad formāts tiek palaists** uz **Jā**.

    > [!NOTE]
    > Šis parametrs ir lietotājam raksturīgs un uzņēmumam raksturīgs.

    ![Lietotāja parametru dialoglodziņš.](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Apstrādāt kreditora maksājumu atkļūdošanai

1. Izpildiet šīs tēmas [3. papildinājumā](#appendix3) norādītās darbības, lai apstrādātu kreditoru maksājumus.
2. Ziņojuma lodziņā atlasiet **Jā**, lai apstiprinātu, ka vēlaties pārtraukt kreditora maksājumu apstrādi, un tā vietā startējiet datu avota atkļūdošanu lapā **Atkļūdot datu avotus**.

    ![Apstiprinājuma ziņojuma lodziņš.](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Atkļūdot datu avotus, kas tiek izmantoti maksājuma apstrādei

### <a name="debug-the-model-mapping"></a>Atkļūdot modeļa kartējumu

1. Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Modeļa kartēšanu**, lai sāktu atkļūdot no šī ER komponenta.
2. Kreisajā pusē esošajā datu avota rūtī atlasiet **\$notSentTransactions** datu avotu un pēc tam atlasiet **Lasīt visus ierakstus**.

    Jūs varat izvēlēties **Lasīt 1 ierakstu**, **Lasīt 10 ierakstus**, **Lasīt 100 ierakstus** vai **Lasīt visus ierakstus**, lai piespiestu atbilstošo ierakstu skaitu, kas jālasa no atlasītā datu avota. Šādā veidā jūs varat simulēt piekļuvi datu avotam no "Running ER" formāta.

3. Datu rūts labajā pusē atlasiet rekvizītu **Izvērst visus**.

    Jūs varat redzēt, ka **Ierakstu saraksta** veida atlasītais datu avots satur vienu ierakstu.

4. Paplašiniet **\$notSentTransactions** datu avotu un atlasiet ligzdoto **vendBankAccountInTransactionCompany()** metodi.
5. Paplašiniet **vendBankAccountInTransactionCompany()** metodi un atlasiet ligzdoto **IBAN** lauku.
6. Atlasiet **Iegūt vērtību**.

    Jūs varat izvēlēties **Iegūt vērtību**, lai piespiestu atlasītā datu avota atlasītā lauka vērtību lasīšanai. Šādā veidā jūs varat simulēt piekļuvi laukam no "Running ER" formāta.

7. Atlasiet **Izvērst visas**.

    ![IBAN lauka vērtība modeļa kartēšanā.](./media/er-data-debugger-debugging-model-mapping.png)

    Kā redzat, modeļa kartēšana nav atbildīga par saīsinātajām atstarpēm, jo IBAN kods, ko tā atgriež kreditora bankas kontam, ietver atstarpes. Tāpēc ir jāturpina datu avota atkļūdošana.

### <a name="debug-the-format-mapping"></a>Formāta kartēšanas atkļūdošana

1. Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Formāta kartēšanu**, lai turpinātu atkļūdot no šī ER komponenta.
2. Atlasiet **\$PaymentByDebtor** datu avotu un pēc tam atlasiet **Lasīt visus ierakstus**.
3. Izvērsiet **\$PaymentByDebtor**.
4. Izvērsiet **\$PaymentByDebtor.Lines** un pēc tam atlasiet **Lasīt visus ierakstus**.
5. Izvērsiet **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Izvērsiet **\$PaymentByDebtor.Lines.CreditorAccount.Identification** un tad atlasiet **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Atlasiet **Iegūt vērtību**.
8. Atlasiet **Izvērst visas**.

    ![IBAN lauka vērtība formāta kartēšanā.](./media/er-data-debugger-debugging-format-mapping.png)

    Kā redzat, formāta kartēšanas datu avoti nav atbildīgi par saīsinātajām atstarpēm, jo IBAN kods, ko tie atgriež kreditora bankas kontam, ietver atstarpes. Tāpēc ir jāturpina datu avota atkļūdošana.

### <a name="debug-the-format"></a>Formāta atkļūdošana

1. Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Formāts**, lai turpinātu atkļūdot no šī ER komponenta.
2. Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports** \> **XMLHeader** \> **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** un pēc tam atlasiet **Lasīt visus ierakstus**.
3. Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports** \> **XMLHeader** \> **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** un tad atlasiet **Lasīt visus ierakstus**.
4. Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports** \> **XMLHeader** \> **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** un tad atlasiet **Iegūt vērtību**.
5. Atlasiet **Izvērst visas**.

    ![IBAN lauka vērtība formātā.](./media/er-data-debugger-debugging-format.png)

   Kā redzat, formāta saistīšana nav atbildīga par saīsinātajām atstarpēm, jo IBAN kods, ko tā atgriež kreditora bankas kontam, ietver atstarpes. Tāpēc **BankIBAN** elements ir konfigurēts tā, lai izmantotu formāta transformāciju, kas saīsina atstarpes.

6. Aizveriet datu avota atkļūdotāju.

### <a name="review-the-format-transformations"></a>Pārskatiet formāta transformācijas

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārskaitījums**.
3. Atlasiet **Noformētājs** un tad izvērsiet elementus, lai atlasītu **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN elements lapā Formāta veidotājs.](./media/er-data-debugger-referred-transformation.png)

    Kā redzat, **BankIBAN** elements ir konfigurēts, lai izmantotu **noņemt, kas nav burtcipari** transformāciju.

4. Atlasiet cilni **Transformācijas**.

    ![BankIBAN elementa transformāciju cilne.](./media/er-data-debugger-transformation.png)

    Kā redzat, **noņemt, kas nav burtcipari** transformācija ir konfigurēta, lai izmantotu izteiksmi, kas saīsina atstarpes no nodrošinātās teksta virknes.

## <a name="start-to-debug-in-the-operation-designer"></a>Sākt atkļūdot Operāciju noformētājā

Konfigurējot ER formāta melnraksta versiju, ko var palaist tieši no Operāciju noformētāja, varat piekļūt datu avota atkļūdotājam, darbības rūtī atlasot **Sākt atkļūdošanu**.

![Sākt atkļūdošanu poga lapā Formāta veidotājs.](./media/er-data-debugger-run-from-designer.png)

Atkļūdošanai ir pieejami rediģējamā ER formāta kartēšanas un formāta komponenti.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Sākt atkļūdot Modeļa kartēšanas noformētājā

Konfigurējot ER modeļa kartēšanu, ko var palaist tieši no **Modeļa kartēšanas** lapas, varat piekļūt datu avota atkļūdotājam, darbības rūtī atlasot **Sākt atkļūdošanu**.

![Sākt atkļūdošanu poga noformētāja lapā Modeļa kartēšana.](./media/er-data-debugger-run-from-designer-mapping.png)

Rediģējamā ER kartēšanas komponenta modeļa komponents ir pieejams atkļūdošanai.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>1. papildinājums: Saņemiet ER risinājumu

### <a name="download-an-er-solution"></a>ER risinājuma lejupielāde

Ja vēlaties izmantot ER risinājumu, lai ģenerētu elektronisko maksājumu failu kreditora maksājumam, kas tiek apstrādāts, jūs varat [lejupielādēt](download-electronic-reporting-configuration-lcs.md) **ISO20022 kredīta pārvedumu** ER maksājuma formātu, kas ir pieejams no koplietojamo līdzekļu bibliotēkas Microsoft Dynamics Lifecycle Services (LCS) pakalpojumos vai no Globālās krātuves.

![ER maksājuma formātu importēšana lapā Konfigurācijas krātuve.](./media/er-data-debugger-import-from-repo.png)

Papildus atlasītajam ER formātam sekojošajām [konfigurācijām](general-electronic-reporting.md#Configuration) ir jābūt automātiski importētām jūsu Microsoft Dynamics 365 Finance instancē kā daļai no **ISO20022 kredīta pārveduma** ER risinājuma:

- **Maksājuma modelis** [ER datu modeļa konfigurācija](general-electronic-reporting.md#DataModelComponent)
- **ISO20022 kredīta pārvedums** [ER formāta konfigurācija](general-electronic-reporting.md#FormatComponentOutbound)
- **Maksājuma modeļa kartēšana 1611** [ER modeļa kartēšanas konfigurācija](general-electronic-reporting.md#ModelMappingComponent)
- **Maksājumu modeļa kartēšana uz ISO20022 galapunktu** ER modeļa kartēšanas konfigurācija

Šīs konfigurācijas ir iespējams atrast ER struktūras lapā **Konfigurācijas** (**Organizācijas administrēšana** \> **Elektroniskā ziņošana** \> **Konfigurācijas**).

![Importētās konfigurācijas Konfigurāciju lapā.](./media/er-data-debugger-configurations.png)

Ja konfigurācijas kokā trūkst kādas no iepriekš uzskaitītajām konfigurācijām, tās ir manuāli jālejupielādē no koplietojamā līdzekļa bibliotēkas tādā pašā veidā, kā lejupielādējat ER maksājuma formātu **ISO20022 kredīta pārvedums**.

### <a name="analyze-the-downloaded-er-solution"></a>Analizēt lejupielādējamo ER risinājumu

#### <a name="review-the-model-mapping"></a>Pārskatīt modeļa kartēšanu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Maksājuma modelis** \> **Maksājuma modeļa kartēšana 1611**.
3. Atlasiet **Noformētājs**.
4. Atlasiet **Maksājuma modeļa kartēšana ISO20022 CT** kartēšanas ierakstu.
5. Atlasiet **Noformētāju** un pēc tam pārskatiet atvērto modeļa kartējumu.

    Ievērojiet, ka datu modeļa **Maksājumu** lauks ir saistīts ar **\$notSentTransactions** datu avotu, kas atgriež to kreditoru maksājumu rindu sarakstu, kuras tiek apstrādātas.

    ![Maksājumu lauks Modeļa kartēšanas noformētāja lapā.](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Pārskatīt formāta kartēšanu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārvedums**.
3. Atlasiet **Noformētājs**.
4. Cilnē **Kartēšana** pārskatiet atvērto formāta kartēšanu.

    Ievērojiet, ka **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** elements failam **ISO20022CTReports** \> **XMLHeader** ir piesaistīts **\$PaymentByDebtor** datu avotam, kas ir konfigurēts datu modeļa **Maksājumu** lauka ierakstu grupēšanai.

    ![PmtInf elements lapā Formāta veidotājs.](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Pārskatīt formātu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārvedums**.
3. Atlasiet **Noformētāju** un pēc tam pārskatiet atvērto formātu.

    Ievērojiet, ka formāta elements sadaļā **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** ir konfigurēts, lai maksājuma failā ievadītu kreditora konta IBAN kodu.

    ![BankIBAN elements lapā Formāta veidotājs.](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>2.papildinājums: Konfigurēt kreditorus

### <a name="modify-a-vendor-property"></a>Pārveidot kreditora rekvizītu

1. Dodieties uz **Kreditori** \> **Kreditori** \> **Visi kreditori**.
2. Atlasiet kreditoru **DE-01002** un pēc tam darbību rūts cilnē **Kreditors** grupā **Uzstādīt** atlasiet **Banku konti**.
3. Kopsavilkuma cilnē **Identifikācija** laukā **IBAN** <a name="enteredIBANcode"></a>ievadiet **GB33 BUKB 2020 1555 5555 55**.
4. Atlasiet **Saglabāt**.

![IBAN lauks uzstādīts lapā Kreditora bankas konti.](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Maksāšanas metodes iestatīšana

1. Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.
2. Atlasiet **SEPA CT** maksāšanas metodi.
3. Kopsavilkuma cilnē **Failu formāti** sadaļā **Failu formāti** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.
4. Laukā **Eksporta formāta konfigurācija** atlasiet **ISO20022 kredīta pārveduma** ER formātu.
5. Atlasiet **Saglabāt**.

![Faila formāta iestatījumi lapā Maksājuma metodes.](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Kreditora maksājuma pievienošana

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Pievienot jaunu maksājumu žurnālu.
3. Atlasiet **Rindas** un pievienojiet jaunu maksājuma rindu.
4. Laukā **Konts** atlasiet kreditoru **DE-01002**.
5. Laukā **Debets** ievadiet kādu vērtību.
6. Laukā **Maksājuma metode** atlasiet **SEPA CT**.
7. Atlasiet **Saglabāt**.

![Kreditora maksājums ir pievienots lapā Kreditora maksājumi.](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>3. papildinājums: Kreditora maksājumu apstrāde

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.
2. Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.
3. Atlasiet maksājuma rindu un pēc tam atlasiet **Maksājuma statuss** \> **Nav**.
4. Atlasiet **Ģenerēt maksājumus**.
5. Laukā **Maksājuma metode** atlasiet **SEPA CT**.
6. Laukā **Bankas konts** atlasiet **DEMF OPER**.
7. Dialoglodziņā **Ģenerēt maksājumus** atlasiet **Labi**.
8. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]