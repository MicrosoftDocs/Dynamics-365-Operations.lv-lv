---
title: Izveidot un palaist apstrādi, lai izsauktu vienkāršu eksporta ER formātu Excel pārskatu ģenerēšanai
description: Šajā tēmā sniegts piemērs par elektronisko ziņojumu iestatīšanas un lietošanas veidu.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a5fd466c98e0855f7a33929eeee42b9147d26ba19780b4ae7c8eb895ac27ea5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737681"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Izveidot un palaist apstrādi, lai izsauktu vienkāršu eksporta ER formātu Excel pārskatu ģenerēšanai

[!include [banner](../includes/banner.md)]

Pēc tam, kad ER formāts ir izveidots, kartēts uz datu avotiem un pabeigts, to var palaist no darbvietas **Elektr. pārskatu veidošana**. Pēc atskaites ģenerēšanas varat to saglabāt lokāli.

Lai kontrolētu šādus pārskatu veidošanas procesa aspektus, iestatiet elektronisko ziņojumu apstrādi:

- Reģistrējiet inf. par to, kas ģenerējis pārsk.
- Reģistrējiet informāciju par to, kad tika ģenerēts pārskats.
- Saglabājiet pārsk., kas tika ģenerēti par iepr. periodiem.

Šajā piemērā parādīts, kā var iestatīt elektronisko ziņojumapmaiņu, lai ģenerētu pārskatu, kas balstās uz eksportēšanas ER formātu programmai Microsoft Excel. Ja vēlaties sekot šim piemēram, ER Excel eksportēšanas ER formātam programmai Excel jau jābūt izveidotam, kartētam uz datu avotiem un pabeigtam. Turklāt numuru virknei jau jābūt iestatītai elektroniskajiem ziņojumiem.

Veidojot apstrādi, ir noderīgi vispirms definēt apstrādes darbības un statusus, kas tiks iestatīti. Šis attēls parāda šī piemēra apstrādi.

![Apstrādes shēma](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Ziņoj. statusu izveide

1. Dodieties uz **Nodoklis** \> **Iestatījums** \> **Elektroniskie ziņojumi** \> **Ziņu statusi**.
2. Izveidojiet šādus ziņojumu statusus:

    - Jauns
    - Sagatavots
    - Ģenerēts

    ![Ziņojuma statusi](media/message-statuses.png)

3. Statusa **Jauns** rindā atzīmējiet izv. rūtiņu **Atļaut dzēšanu**, lai ļautu lietotājiem dzēst ziņoj., kuriem ir šis statuss.

## <a name="create-additional-fields"></a>Papildu lauku izveide

1. Dodieties uz **Nodoklis** \> **Iestatījums** \> **Elektroniskie ziņojumi** \> **Papildu lauki**.
2. Pievienojiet pap. lauku un tā vērtību.
3. Opc. **Lietot. laboj.** iest. **Jā**, lai ļautu lietot. red. lauku.

![Papildlauki](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Ziņoj. apstrādes darbību izveide

Šajā piemērā tiks izveidotas šādas ziņojumu apstrādes darbības:

- **Izveidot ziņojumu**
- **Atjaun. uz Sagat.**
- **Ģenerēt pārsk.**
- **Atjaun. uz sākotn. statusu** (neobl.)

Lai izveidotu darbības, rīkojieties šādi.

1. Dodieties uz **Nodoklis** \> **Iestatījums** \> **Elektroniskie ziņojumi** \> **Ziņojumu apstrādes darbības**.
2. Izveidojiet darbību ar nosauk. **Izveidot ziņ**. Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Izveidot ziņoj**.
3. Izveidojiet darb. ar nosauk. **Atjaunināt uz Sagatavots** un iestatiet šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Ziņoj. līmeņa lietotāja apstrāde**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Jauns**.
    - Kopsav. cilnes **Beigu statusi** laukā **Ziņojuma statuss** atlasiet **Sagatavots**. Laukā **Atbildes tips** ievadiet **Izpildīts veiksmīgi**.

4. Izveidojiet darbību ar nosaukumu **Ģenerēt pārskatu** un iestatiet šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atl. **Elektr. pārsk. veidoš. eksports**. Laukā **Formāta kartēšana** atlasiet eksportēšanas ER formātu. Opcijas ir: **Excel**, **XML**, **JSON**, **Teksts** un **Cits**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Sagatavots**.
    - Kopsav. cilnes **Beigu statusi** laukā **Ziņojuma statuss** atlasiet **Ģenerēts**. Laukā **Atbildes tips** ievadiet **Izpildīts veiksmīgi**.

    ![Pārsk. darbības ģener.](media/generate-report-action.png)

5. Neobligāti: lai ļautu lietotājiem atkārtoti ģenerēt pārskatu vairākas reizes, izveidojiet darbību ar nosaukumu **Atjaunināt uz sākotnējo statusu** un iestiet šādus laukus:

    - Kopsav. cilnes **Vispārīgi** laukā **Darbības tips** atlasiet **Ziņoj. līmeņa lietotāja apstrāde**.
    - Kopsav. cilnes **Sākotnējie statusi** laukā **Ziņojuma statuss** atlasiet **Ģenerēts**.
    - Kopsavilkuma cilnē **Beigu statusi** pievienojiet atsevišķu rindu katram no abiem ziņojumu statusiem (**Sagatavots** un **Jauns**). Abām rindām iestatiet laukā **Atbildes tips** vienumu **Izpildīts veiksmīgi**.

## <a name="electronic-message-processing"></a>Elektroniska ziņojuma apstrāde

Šīm piemēram visas darbības jāiestata tā, lai tās tiktu palaistas atsevišķi. Tiek pieņemts, ka lietotājs sāks katru darbību.

1. Dodieties uz **Nodoklis** \> **Iestatījums** \> **Elektronisko ziņojumu** \> **Elektroniskā ziņojuma apstrāde**.
2. Pievienojiet ierakstu apstrādei, un pievienojiet visas iepriekš defin. darbības un papildu lauku.
3. Neobligāti: kopsavilkuma cilnē **Drošības lomas** definējiet drošības lomas apstrādei, lai ierobežotu piekļuvi noteiktiem pārskatiem.
4. Dodieties uz **Nodoklis** \> **Uzziņas un pārskati** \> **Elektroniskie ziņojumi** \> **Elektroniskie ziņojumi**.
5. Atl. **Jauns**, lai izveidotu ziņ. Šajā brīdī varat pievienot datumus un aprakstu. Varat arī atjaunināt papildu lauka vērtību, ja nepieciešams.

    ![Elektrononisko ziņojuma izveide](media/create-electronic-message.png)

    Režģis kopsav. cilnē **Darbību žurnāls** tiek automātiski aizpildīts ar visu darbību žurnālu, kuras veiktas ar ziņojumu.

    Tagad varat vai nu dzēst vai atjaunināt ziņojuma statusu. 

6. Lai atjauninātu ziņojuma statusu, atlasiet vienumu **Atjaunināt statusu**. Laukā **Jauns statuss** atlasiet **Sagatavots** un pēc tam atlasiet **Labi**.

    ![Ziņojuma statusa atjaunināšana](media/update-status.png)

    Ziņojuma statuss ir atjaunināts uz **Sagatavots**.

7. Ģenerējiet pārskatu, atlasot **Ģenerēt pārskatu**.

    Tiek ģenerēts pārskats, un ziņoj. statuss un darb. žurn. tiek atjaunināti.

8. Lai skatītu ģenerēto pārskatu, atlasiet pogu **Pielikums** (papīra saspraudes simbols) lapas augšējā labajā stūrī.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
