---
title: E-pasta ziņojuma ER adresāta tips
description: Šajā tēmā ir sniegta informācija par to, kā konfigurēt e-pasta ziņojuma adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019886"
---
# <span data-ttu-id="17bbe-103"><a name="EmailDestinationType">E-pasta galamērķis</a></span><span class="sxs-lookup"><span data-stu-id="17bbe-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17bbe-104">Varat konfigurēt e-pasta ziņojuma adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="17bbe-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="17bbe-105">Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek piegādāts kā elektroniskā pasta pielikums.</span><span class="sxs-lookup"><span data-stu-id="17bbe-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="17bbe-106">Opciju **Iespējots** iestatiet uz **Jā**, lai izvades failu sūtītu pa e-pastu.</span><span class="sxs-lookup"><span data-stu-id="17bbe-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="17bbe-107">Kad šī opcija ir iespējota, varat norādīt e-pasta ziņojumu adresātus, kā arī rediģēt tēmu un e-pasta ziņojuma pamattekstu.</span><span class="sxs-lookup"><span data-stu-id="17bbe-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="17bbe-108">E-pasta ziņojuma tēmai un pamattekstam varat iestatīt konstantus tekstus, vai arī varat lietot ER- [formulas](er-formula-language.md), lai e-pasta tekstus izveidotu dinamiski.</span><span class="sxs-lookup"><span data-stu-id="17bbe-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="17bbe-109">E-pasta adreses lietošanai ar ER varat konfigurēt divos veidos.</span><span class="sxs-lookup"><span data-stu-id="17bbe-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="17bbe-110">Konfigurāciju var pabeigt tādā pašā veidā, kā to pabeidz drukāšanas pārvaldības līdzeklis, vai arī varat atrisināt e-pasta adresi, izmantojot tiešu atsauci uz ER konfigurāciju ar formulas palīdzību.</span><span class="sxs-lookup"><span data-stu-id="17bbe-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="17bbe-111">[![E-pasta ziņojuma galamērķa iespējošana](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="17bbe-112">E-pasta adrešu tipi</span><span class="sxs-lookup"><span data-stu-id="17bbe-112">Email address types</span></span>

<span data-ttu-id="17bbe-113">Kad atlasāt **Rediģēt** laukos **Kam** vai **Kopija**, tiek parādīts dialoglodziņš **E-pasta ziņojuma adresāts**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="17bbe-114">Pēc tam varat atlasīt izmantojamo e-pasta adreses tipu.</span><span class="sxs-lookup"><span data-stu-id="17bbe-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="17bbe-115">Pašlaik tiek atbalstīti e-pasta tipi **Konfigurācijas e-pasts** un **Drukāšanas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="17bbe-116">[![E-pasta ziņojuma tipa atlasīšana](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="17bbe-117">Drukāšanas iestatījumi</span><span class="sxs-lookup"><span data-stu-id="17bbe-117">Print management</span></span>

<span data-ttu-id="17bbe-118">Ja atlasāt e-pasta ziņojuma tipu **Drukāšanas pārvaldība**, varat laukā **Kam** ievadīt fiksētas e-pasta adreses.</span><span class="sxs-lookup"><span data-stu-id="17bbe-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="17bbe-119">[![Fiksēto e-pasta adresu konfigurēšana](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="17bbe-120">Lai lietotu e-pasta adreses, kas nav fiksētas, jums faila galamērķim ir jāatlasa e-pasta avota tips.</span><span class="sxs-lookup"><span data-stu-id="17bbe-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="17bbe-121">Tiek atbalstītas šādas vērtības: **Debitors**, **Kreditors**, **Potenciālais klients**, **Kontaktpersona**, **Konkurents**, **Nodarbinātais**, **Kandidāts**, **Potenciālais piegādātājs** un **Neatļauts piegādātājs**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="17bbe-122">Kad e-pasta avota tips ir atlasīts, izmantojiet pogu blakus laukam **E-pasta ziņojuma avota konts**, lai atvērtu formu **Formulas veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="17bbe-123">Varat izmantot šo formu, lai pievienotu formulu, kas atgriežas izpildlaikā, atlasītā avota tipa **puses kontu** no apstrādātā dokumenta līdz e-pasta ziņojuma adresātam.</span><span class="sxs-lookup"><span data-stu-id="17bbe-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="17bbe-124">[![E-pasta ziņojuma avota konta konfigurācija](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="17bbe-125">Formulas ir atkarīgas no ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="17bbe-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="17bbe-126">Laukā **Formula** ievadiet dokumentam specifisko atsauci uz debitora vai kreditora puses tipu.</span><span class="sxs-lookup"><span data-stu-id="17bbe-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="17bbe-127">Tā vietā, lai rakstītu, varat atrast datu avota mezglu, kas apzīmē debitora vai kreditora kontu, un pēc tam atlasīt **Pievienot datu avotu**, lai atjauninātu šo formulu.</span><span class="sxs-lookup"><span data-stu-id="17bbe-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="17bbe-128">Piemēram, ja izmantojat konfigurāciju **ISO 20022 kredīta pārskaitījums**, tad kreditora kontu apzīmē mezgls `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="17bbe-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="17bbe-129">Ja ievadāt virknes vērtību, piemēram `"DE-001"`, un saglabājat formulu, e-pasta ziņojums tiks nosūtīts kreditora kontaktpersonai **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="17bbe-130">[![ER formulas veidotāja lapa](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="17bbe-131">[![E-pasta ziņojuma avota konta konfigurācija](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="17bbe-132">Konfigurācijas e-pasta ziņojums</span><span class="sxs-lookup"><span data-stu-id="17bbe-132">Configuration email</span></span>

<span data-ttu-id="17bbe-133">Izmantojiet šo e-pasta ziņojuma tipu, ja izmantotajā konfigurācijā ir datu avotu mezgls, kas atgriež **e-pasta adresi**.</span><span class="sxs-lookup"><span data-stu-id="17bbe-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="17bbe-134">Formulu veidotājā varat izmantot datu avotus un funkcijas, lai iegūtu pareizi formatētu e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="17bbe-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="17bbe-135">Piemēram, ja izmantojat konfigurāciju **ISO 20022 kredīta pārskaitījums**, tad kreditora kontaktpersonas e-pasta adresi apzīmē mezgls `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="17bbe-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="17bbe-136">[![E-pasta adreses avota konfigurācija](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="17bbe-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17bbe-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="17bbe-137">Additional resources</span></span>

- [<span data-ttu-id="17bbe-138">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="17bbe-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="17bbe-139">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="17bbe-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="17bbe-140">Formulas veidotājs elektronisko pārskatu veidošanā (ER)</span><span class="sxs-lookup"><span data-stu-id="17bbe-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
