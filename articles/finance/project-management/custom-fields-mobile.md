---
title: Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android
description: Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080776"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="fec34-103">Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android</span><span class="sxs-lookup"><span data-stu-id="fec34-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fec34-104">Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus.</span><span class="sxs-lookup"><span data-stu-id="fec34-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="fec34-105">Ir aprakstītas tālāk norādītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="fec34-105">The following topics are covered:</span></span>

- <span data-ttu-id="fec34-106">Dažādie datu tipi, ko atbalsta pielāgoto lauku struktūra</span><span class="sxs-lookup"><span data-stu-id="fec34-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="fec34-107">Kā darba laika uzskaites tabulu ierakstos rādīt tikai lasāmus vai rediģējamus laukus un kā datu bāzē saglabāt lietotāja norādītas vērtības.</span><span class="sxs-lookup"><span data-stu-id="fec34-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="fec34-108">Kā darba laika uzskaites tabulas virsrakstā rādīt tikai lasāmus laukus</span><span class="sxs-lookup"><span data-stu-id="fec34-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="fec34-109">Kā integrēt citu pielāgoto biznesa loģiku, lai laukos ievadītu noklusējuma vērtības un veiktu papildu validēšanu</span><span class="sxs-lookup"><span data-stu-id="fec34-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="fec34-110">Mērķauditorija</span><span class="sxs-lookup"><span data-stu-id="fec34-110">Audience</span></span>

<span data-ttu-id="fec34-111">Šī tēma ir paredzēta izstrādātājiem, kas savus pielāgotos laukus integrē Microsoft Dynamics 365 Project Timesheet mobilajā programmā, kura ir pieejama operētājsistēmai Apple iOS un Google Android.</span><span class="sxs-lookup"><span data-stu-id="fec34-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="fec34-112">Tiek pieņemts, ka lasītāji pārzina X++ izstrādes un projektu darba laika uzskaites tabulu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="fec34-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="fec34-113">Datu līgums – TSTimesheetCustomField X++ klase</span><span class="sxs-lookup"><span data-stu-id="fec34-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="fec34-114">**TSTimesheetCustomField** klase ir X++ datu līguma klase, kas pārstāv informāciju par pielāgotu lauku darba laika uzskaites tabulas funkcionalitātei.</span><span class="sxs-lookup"><span data-stu-id="fec34-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="fec34-115">Pielāgoto lauku objektu saraksti tiek nodoti gan TSTimesheetDetails datu līgumam, gan TSTimesheetEntry datu līgumam, lai pielāgotus laukus rādītu mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="fec34-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="fec34-116">**TSTimesheetDetails** — darba laika uzskaites tabulas virsraksta līgums.</span><span class="sxs-lookup"><span data-stu-id="fec34-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="fec34-117">**TSTimesheetEntry** — darba laika uzskaites tabulas transakcijas līgums.</span><span class="sxs-lookup"><span data-stu-id="fec34-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="fec34-118">Šo objektu grupas, kam ir vienāda projekta informācija un vērtība **timesheetLineRecId**, veido vienu rindu.</span><span class="sxs-lookup"><span data-stu-id="fec34-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="fec34-119">fieldBaseType (tipi)</span><span class="sxs-lookup"><span data-stu-id="fec34-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="fec34-120">Rekvizīts **FieldBaseType** objektā **TsTimesheetCustom** nosaka programmā rādītā lauka tipu.</span><span class="sxs-lookup"><span data-stu-id="fec34-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="fec34-121">Tiek atbalstītas tālāk norādītās vērtības **Tipi**.</span><span class="sxs-lookup"><span data-stu-id="fec34-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="fec34-122">Vērtības Tipi</span><span class="sxs-lookup"><span data-stu-id="fec34-122">Types value</span></span> | <span data-ttu-id="fec34-123">Tips</span><span class="sxs-lookup"><span data-stu-id="fec34-123">Type</span></span>              | <span data-ttu-id="fec34-124">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="fec34-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="fec34-125">0</span><span class="sxs-lookup"><span data-stu-id="fec34-125">0</span></span>           | <span data-ttu-id="fec34-126">Virkne (un Uzskaitījums)</span><span class="sxs-lookup"><span data-stu-id="fec34-126">String (and Enum)</span></span> | <span data-ttu-id="fec34-127">Šis lauks izskatās kā teksta lauks.</span><span class="sxs-lookup"><span data-stu-id="fec34-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="fec34-128">1</span><span class="sxs-lookup"><span data-stu-id="fec34-128">1</span></span>           | <span data-ttu-id="fec34-129">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="fec34-129">Integer</span></span>           | <span data-ttu-id="fec34-130">Vērtība tiek rādīta kā skaitlis bez cipariem aiz komata.</span><span class="sxs-lookup"><span data-stu-id="fec34-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="fec34-131">2</span><span class="sxs-lookup"><span data-stu-id="fec34-131">2</span></span>           | <span data-ttu-id="fec34-132">Real</span><span class="sxs-lookup"><span data-stu-id="fec34-132">Real</span></span>              | <span data-ttu-id="fec34-133">Vērtība tiek rādīta kā skaitlis ar cipariem aiz komata.</span><span class="sxs-lookup"><span data-stu-id="fec34-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="fec34-134">Lai reālo skaitļu vērtības programmā radītu kā valūtu, izmantojiet rekvizītu **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="fec34-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="fec34-135">Varat arī izmantot rekvizītu **numberOfDecimals**, lai iestatītu, cik cipari aiz komata tiek rādīti.</span><span class="sxs-lookup"><span data-stu-id="fec34-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="fec34-136">3</span><span class="sxs-lookup"><span data-stu-id="fec34-136">3</span></span>           | <span data-ttu-id="fec34-137">Datums</span><span class="sxs-lookup"><span data-stu-id="fec34-137">Date</span></span>              | <span data-ttu-id="fec34-138">Datuma formātus nosaka lietotāja iestatījums **Datumu, laiku un skaitļu formāts**, kas ir norādīts iestatījumā **Valodas un valsts/reģiona preferences**, sadaļā **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="fec34-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="fec34-139">4.</span><span class="sxs-lookup"><span data-stu-id="fec34-139">4</span></span>           | <span data-ttu-id="fec34-140">Būla</span><span class="sxs-lookup"><span data-stu-id="fec34-140">Boolean</span></span>           | |
| <span data-ttu-id="fec34-141">15</span><span class="sxs-lookup"><span data-stu-id="fec34-141">15</span></span>          | <span data-ttu-id="fec34-142">GUID</span><span class="sxs-lookup"><span data-stu-id="fec34-142">GUID</span></span>              | |
| <span data-ttu-id="fec34-143">16</span><span class="sxs-lookup"><span data-stu-id="fec34-143">16</span></span>          | <span data-ttu-id="fec34-144">Int64</span><span class="sxs-lookup"><span data-stu-id="fec34-144">Int64</span></span>             | |

- <span data-ttu-id="fec34-145">Ja objektā **TSTimesheetCustomField** nav norādīts rekvizīts **stringOptions**, lietotājam tiek nodrošināts brīva teksta lauks.</span><span class="sxs-lookup"><span data-stu-id="fec34-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="fec34-146">Var izmantot rekvizītu **stringLength**, lai iestatītu maksimālo virknes garumu, kādu lietotāji var ievadīt.</span><span class="sxs-lookup"><span data-stu-id="fec34-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="fec34-147">Ja objektā **TSTimesheetCustomField** ir norādīts rekvizīts **stringOptions**, šie saraksta elementi ir vienīgās vērtības, ko lietotāji var atlasīt, izmantojot opciju pogas (radiopogas).</span><span class="sxs-lookup"><span data-stu-id="fec34-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="fec34-148">Tādā gadījumā virknes lauks lietotāja ievades nolūkos var darboties kā uzskaitījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="fec34-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="fec34-149">Lai šo vērtību datu bāzē saglabātu kā uzskaitījumu, manuāli kartējiet virknes vērtību atpakaļ uz uzskaitījuma vērtību, pirms to saglabājat datu bāzē, izmantojot komandķēdi (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).</span><span class="sxs-lookup"><span data-stu-id="fec34-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="fec34-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="fec34-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="fec34-151">Šo rekvizītu varat izmantot, lai reālu skaitļu vērtības formatētu kā valūtu.</span><span class="sxs-lookup"><span data-stu-id="fec34-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="fec34-152">Šī pieeja ir piemērojama tikai tad, ja vienuma **fieldBaseType** vērtība ir **Real**.</span><span class="sxs-lookup"><span data-stu-id="fec34-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="fec34-153">**TSCustomFieldExtendedType:None** — netiek lietots nekāds formatējums.</span><span class="sxs-lookup"><span data-stu-id="fec34-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="fec34-154">**TSCustomFieldExtendedType::Valūta** — formatēt vērtību kā valūtu.</span><span class="sxs-lookup"><span data-stu-id="fec34-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="fec34-155">Kad ir aktīvs valūtas formatējums, var izmantot lauku **stringValue**, lai nodotu valūtas kodu, kas ir jārāda programmā.</span><span class="sxs-lookup"><span data-stu-id="fec34-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="fec34-156">Šī vērtība ir tikai lasāma vērtība.</span><span class="sxs-lookup"><span data-stu-id="fec34-156">The value is a read-only value.</span></span>

    <span data-ttu-id="fec34-157">Laukā **realValue** ir naudas summa, kas ir jāsaglabā datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="fec34-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="fec34-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="fec34-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="fec34-159">Šo rekvizītu varat izmantot, lai norādītu, kur šis pielāgotais lauks ir jārāda programmā.</span><span class="sxs-lookup"><span data-stu-id="fec34-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="fec34-160">**TSCustomFieldSection::Virsraksts** — šis lauks programmā tiek rādīts sadaļā **Skatīt vairāk informācijas**.</span><span class="sxs-lookup"><span data-stu-id="fec34-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="fec34-161">Šie lauki vienmēr ir tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="fec34-161">These fields are always read-only.</span></span>
- <span data-ttu-id="fec34-162">**TSCustomFieldSection::Rinda** — šis lauks tiek rādīts pēc visiem darba laika uzskaites tabulu ierakstu standarta komplektācijas rindu laukiem.</span><span class="sxs-lookup"><span data-stu-id="fec34-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="fec34-163">Šie lauki var būt rediģējami vai tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="fec34-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="fec34-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="fec34-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="fec34-165">Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="fec34-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="fec34-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="fec34-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="fec34-167">Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="fec34-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="fec34-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="fec34-168">isEditable (NoYes)</span></span>

<span data-ttu-id="fec34-169">Iestatiet šo rekvizītu uz **Jā**, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošo lauku lietotājiem ir jāvar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="fec34-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="fec34-170">Iestatiet šo rekvizītu uz **Nē**, lai lauku padarītu par tikai lasāmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="fec34-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="fec34-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="fec34-172">Iestatiet šo rekvizītu uz **Jā**, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošajam laukam ir jābūt obligātam.</span><span class="sxs-lookup"><span data-stu-id="fec34-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="fec34-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="fec34-173">label (str)</span></span>

<span data-ttu-id="fec34-174">Šis rekvizīts norāda etiķeti, kas programmā tiek rādīta blakus šim laukam.</span><span class="sxs-lookup"><span data-stu-id="fec34-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="fec34-175">stringOptions (virkņu saraksts)</span><span class="sxs-lookup"><span data-stu-id="fec34-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="fec34-176">Šis rekvizīts ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **String**.</span><span class="sxs-lookup"><span data-stu-id="fec34-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="fec34-177">Ja ir iestatīts vienums **stringOptions**, ar virknēm šajā sarakstā tiek norādītas virkņu vērtības, kas ir pieejamas atlasei, izmantojot opciju pogas (radiopogas).</span><span class="sxs-lookup"><span data-stu-id="fec34-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="fec34-178">Ja nav norādīta neviena virkne, ir atļauta brīvā teksta ievadīšana virknes laukā (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).</span><span class="sxs-lookup"><span data-stu-id="fec34-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="fec34-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="fec34-179">stringLength (int)</span></span>

<span data-ttu-id="fec34-180">Šis rekvizīts norāda virknes lauka maksimālo garumu.</span><span class="sxs-lookup"><span data-stu-id="fec34-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="fec34-181">Tas ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **String**.</span><span class="sxs-lookup"><span data-stu-id="fec34-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="fec34-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="fec34-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="fec34-183">Šis rekvizīts norāda ciparu skaitu aiz komata, kas tiek rādīti reāla skaitļa laukam.</span><span class="sxs-lookup"><span data-stu-id="fec34-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="fec34-184">Tas ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **Real**.</span><span class="sxs-lookup"><span data-stu-id="fec34-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="fec34-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="fec34-185">orderSequence (int)</span></span>

<span data-ttu-id="fec34-186">Šis rekvizīts kontrolē secību, kādā programmā tiek rādīti pielāgoti lauki, ja ir norādīti vairāki pielāgoti lauki.</span><span class="sxs-lookup"><span data-stu-id="fec34-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="fec34-187">Vispirms tiek rādīti lauki, kuru skaitļi ir mazāki.</span><span class="sxs-lookup"><span data-stu-id="fec34-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="fec34-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="fec34-188">booleanValue (boolean)</span></span>

<span data-ttu-id="fec34-189">Laukiem, kuru tips ir **Būla**, šis rekvizīts nodod lauka Būla vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="fec34-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="fec34-190">guidValue (guid)</span></span>

<span data-ttu-id="fec34-191">Laukiem, kuru tips ir **GUID**, šis rekvizīts nodod lauka globāli unikālā identifikatora (GUID) vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="fec34-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="fec34-192">int64Value (int64)</span></span>

<span data-ttu-id="fec34-193">Laukiem, kuru tips ir **Int64**, šis rekvizīts nodod lauka int64 vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="fec34-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="fec34-194">intValue (int)</span></span>

<span data-ttu-id="fec34-195">Laukiem, kuru tips ir **Int**, šis rekvizīts nodod lauka int vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="fec34-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="fec34-196">realValue (real)</span></span>

<span data-ttu-id="fec34-197">Laukiem, kuru tips ir **Real**, šis rekvizīts nodod lauka reālā skaitļa vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="fec34-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="fec34-198">stringValue (str)</span></span>

<span data-ttu-id="fec34-199">Laukiem, kuru tips ir **String**, šis rekvizīts nodod lauka virknes vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="fec34-200">Tas tiek izmantots arī laukiem ar tipu **Real**, kuri ir formatēti kā valūta.</span><span class="sxs-lookup"><span data-stu-id="fec34-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="fec34-201">Šiem laukiem šis rekvizīts tiek izmantots, lai valūtas kodu nodotu programmai.</span><span class="sxs-lookup"><span data-stu-id="fec34-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="fec34-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="fec34-202">dateValue (date)</span></span>

<span data-ttu-id="fec34-203">Laukiem, kuru tips ir **Datums**, šis rekvizīts nodod lauka datuma vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="fec34-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="fec34-204">Pielāgotu lauku rādīšana un saglabāšana darba laika uzskaites tabulas ieraksta sadaļā</span><span class="sxs-lookup"><span data-stu-id="fec34-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="fec34-205">Tālāk ir ekrānuzņēmums no laika uzskaites tabulas ieraksta izveides mobilās lietotnes.</span><span class="sxs-lookup"><span data-stu-id="fec34-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="fec34-206">Tajā ir redzami standarta komplektācijā esošie lauki un pielāgots lauks sadaļā “Laika ievade” ar nosaukumu “Testa virkne”, kuram jau ir iestatīta uzskaitījuma vērtība “Otrā opcija”.</span><span class="sxs-lookup"><span data-stu-id="fec34-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testa virknes pielāgotais lauks programmā](media/timesheet-entry.jpg)



<span data-ttu-id="fec34-208">Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kas atlasa vienu no uzskaitījuma opcijām, kuras ir pieejamas pielāgotajam laukam “Testa virkne”.</span><span class="sxs-lookup"><span data-stu-id="fec34-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="fec34-209">Abas opcijas ir “Pirmā opcija” un “Otrā opcija” un tiek rādītas kā radiopogas.</span><span class="sxs-lookup"><span data-stu-id="fec34-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="fec34-210">Pašlaik ir atlasīta otrā opcija.</span><span class="sxs-lookup"><span data-stu-id="fec34-210">The second option is currently selected.</span></span>

![Opciju pogas (radiopogas) testa virknes pielāgotajam laukam](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="fec34-212">Tabulas TSTimesheetLine paplašināšana, lai tai būtu pielāgots lauks</span><span class="sxs-lookup"><span data-stu-id="fec34-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="fec34-213">Tipiskos scenārijos darba laika uzskaites tabulas ieraksta sadaļas pielāgotā lauka dati visticamāk tiks saglabāti tabulā TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="fec34-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="fec34-214">Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTrans ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).</span><span class="sxs-lookup"><span data-stu-id="fec34-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="fec34-215">Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fec34-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="fec34-216">Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku.</span><span class="sxs-lookup"><span data-stu-id="fec34-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="fec34-217">Šī pieeja var būt noderīga tikai lasāmos scenārijos (dinamiski ģenerētu pielāgotu lauku vērtību piemēru skatiet sadaļā “Komandķēdes lietošana klasē TSTimesheetDetails, metodē buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju”.)</span><span class="sxs-lookup"><span data-stu-id="fec34-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="fec34-218">Tālāk ir ekrānuzņēmums no programmas objektu koka Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fec34-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="fec34-219">Tajā ir redzams TSTimesheetLine tabulas paplašinājumu ar lauku TestLineString, kas ir pievienots kā pielāgots lauks.</span><span class="sxs-lookup"><span data-stu-id="fec34-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Rindas virkne](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="fec34-221">Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai darba laika uzskaites tabulas ieraksta sadaļā rādītu kādu lauku</span><span class="sxs-lookup"><span data-stu-id="fec34-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="fec34-222">Šis kods kontrolē programmas lauka rādīšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="fec34-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="fec34-223">Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="fec34-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="fec34-224">Nākamajā piemērā ir parādīts virknes lauks laika ierakstos.</span><span class="sxs-lookup"><span data-stu-id="fec34-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="fec34-225">Šim laukam ir divas opcijas, **Pirmā opcija** un **Otrā opcija**, un tās ir pieejamas, izmantojot opciju pogas (radiopogas).</span><span class="sxs-lookup"><span data-stu-id="fec34-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="fec34-226">Šis lauks programmā ir saistīts ar lauku **TestLineString**, kas ir pievienots tabulai TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="fec34-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="fec34-227">Ņemiet vērā metodes **TSTimesheetCustomField::newFromMetatdata()** lietošanu, lai vienkāršotu inicializēšanu pielāgotajiem lauku rekvizītiem: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** un **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="fec34-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="fec34-228">Šos parametrus varat iestatīt arī manuāli, ja vēlaties.</span><span class="sxs-lookup"><span data-stu-id="fec34-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="fec34-229">Komandķēdes lietošana klases TSTimesheetEntry metodei buildCustomFieldListForEntry, lai darba laika uzskaites tabulas ierakstā ievadītu vērtības</span><span class="sxs-lookup"><span data-stu-id="fec34-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="fec34-230">Metode **buildCustomFieldListForEntry** tiek lietota, lai ievadītu vērtības mobilajā programmā saglabātajās darba laika uzskaites tabulas rindās.</span><span class="sxs-lookup"><span data-stu-id="fec34-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="fec34-231">Šī metode kā parametru izmanto ierakstu TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="fec34-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="fec34-232">Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību.</span><span class="sxs-lookup"><span data-stu-id="fec34-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="fec34-233">Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē</span><span class="sxs-lookup"><span data-stu-id="fec34-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="fec34-234">Lai pielāgotu lauku saglabātu atpakaļ datu bāzē tipiskā lietojumā, jums ir jāpaplašina vairākas metodes.</span><span class="sxs-lookup"><span data-stu-id="fec34-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="fec34-235">Metode **timesheetLineNeedsUpdating** tiek lietota, lai noteiktu, vai lietotājs ir mainījis rindas ierakstu programmā un vai tas ir jāsaglabā datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="fec34-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="fec34-236">Ja nav jāraizējas par veiktspēju, šo metodi var vienkāršot, lai tā vienmēr atgrieztu vērtību **true**.</span><span class="sxs-lookup"><span data-stu-id="fec34-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="fec34-237">Metodi **populateTimesheetLineFromEntryDuringCreate** un **populateTimesheetLineFromEntryDuringUpdate** var paplašināt tā, lai tās ievadītu vērtības TSTimesheetLine datu bāzes ierakstā no nodrošinātā TSTimesheetEntry datu līguma ieraksta.</span><span class="sxs-lookup"><span data-stu-id="fec34-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="fec34-238">Nākamajā piemērā pievērsiet uzmanību tam, kā kartēšana starp datu bāzes lauku un ieraksta lauku tiek manuāli veikta, izmantojot X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="fec34-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="fec34-239">Metodi **populateTimesheetWeekFromEntry** var arī paplašināt, ja pielāgotajam laukam, kas ir kartēts uz **TSTimesheetEntry** objektu, būtu jāraksta atpakaļ uz TSTimesheetLineweek datu bāzes tabulu.</span><span class="sxs-lookup"><span data-stu-id="fec34-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="fec34-240">Nākamajā piemērā lietotāja atlasītā vērtība **firstOption** vai **secondOption** tiek saglabāta datu bāzē kā neapstrādātas virknes vērtība.</span><span class="sxs-lookup"><span data-stu-id="fec34-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="fec34-241">Ja datu bāzes lauks ir lauks ar tipu **Uzskaitījums**, šīs vērtības var manuāli kartēt uz uzskaitījuma vērtību un pēc tam saglabāt datu bāzes tabulas uzskaitījuma laukā.</span><span class="sxs-lookup"><span data-stu-id="fec34-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="fec34-242">Pielāgotu lauku rādīšana darba laika uzskaites tabulas virsraksta sadaļā</span><span class="sxs-lookup"><span data-stu-id="fec34-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="fec34-243">Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kurš apskata darba laika uzskaites tabulu.</span><span class="sxs-lookup"><span data-stu-id="fec34-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="fec34-244">Augšējā labajā stūrī ir atlasīta poga “Papildinformācija”, lai rādītu opciju “Skatīt vairāk informācijas”.</span><span class="sxs-lookup"><span data-stu-id="fec34-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Komanda Skatīt vairāk informācijas](media/show-more.png)

<span data-ttu-id="fec34-246">Tālāk ir ekrānuzņēmums no mobilās lietotnes, kur ir redzama darba laika uzskaites tabulas sadaļa “Vairāk”.</span><span class="sxs-lookup"><span data-stu-id="fec34-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="fec34-247">Darba laika uzskaites tabulas virsraksta sadaļai ir pievienots pielāgots lauks ar nosaukumu “Šīs darba laika uzskaites tabulas lietojuma koeficients (aprēķināts pielāgots lauks)”.</span><span class="sxs-lookup"><span data-stu-id="fec34-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="fec34-248">Pielāgotajā laukā ir iestatīta tikai lasāma vērtība “0,667”.</span><span class="sxs-lookup"><span data-stu-id="fec34-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sadaļa Vairāk](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="fec34-250">Tabulas TSTimesheetTable paplašināšana, lai tai būtu pielāgots lauks</span><span class="sxs-lookup"><span data-stu-id="fec34-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="fec34-251">Tipiskos scenārijos virsraksta sadaļas pielāgotā lauka dati visticamāk tiks izgūti no tabulas TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="fec34-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="fec34-252">Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTable ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).</span><span class="sxs-lookup"><span data-stu-id="fec34-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="fec34-253">Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fec34-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="fec34-254">Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku.</span><span class="sxs-lookup"><span data-stu-id="fec34-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="fec34-255">Šī pieeja ir parādīta nākamajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="fec34-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="fec34-256">Programmā lauki virsraksta sadaļā vienmēr ir tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="fec34-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="fec34-257">Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai virsraksta sadaļā rādītu kādu lauku</span><span class="sxs-lookup"><span data-stu-id="fec34-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="fec34-258">Šis kods kontrolē programmas lauka rādīšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="fec34-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="fec34-259">Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="fec34-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="fec34-260">Nākamajā piemērā ir parādīta aprēķināta vērtība programmas virsraksta sadaļā.</span><span class="sxs-lookup"><span data-stu-id="fec34-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="fec34-261">Komandķēdes lietošana klases TSTimesheetDetails metodei buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju</span><span class="sxs-lookup"><span data-stu-id="fec34-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="fec34-262">Metode **buildCustomFieldListForHeader** tiek lietota, lai mobilajā programmā aizpildītu darba laika uzskaites tabulas virsraksta informāciju.</span><span class="sxs-lookup"><span data-stu-id="fec34-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="fec34-263">Šī metode kā parametru izmanto ierakstu TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="fec34-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="fec34-264">Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību.</span><span class="sxs-lookup"><span data-stu-id="fec34-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="fec34-265">Nākamajā piemērā no datu bāzes netiek nolasītas nekādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="fec34-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="fec34-266">Tā vietā tiek izmantota X++ loģika, lai ģenerētu aprēķinātu vērtību, kura pēc tam tiek rādīta programmā.</span><span class="sxs-lookup"><span data-stu-id="fec34-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="fec34-267">Citas konfigurēšanas/paplašināšanas iespējas</span><span class="sxs-lookup"><span data-stu-id="fec34-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="fec34-268">Papildu validēšanas pievienošana programmai</span><span class="sxs-lookup"><span data-stu-id="fec34-268">Adding additional validation for the app</span></span>

<span data-ttu-id="fec34-269">Pastāvošā darba laika uzskaites tabulas funkcionalitātes loģika datu bāzes līmenī joprojām darbosies paredzētajā veidā.</span><span class="sxs-lookup"><span data-stu-id="fec34-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="fec34-270">Lai pārtrauktu saglabāšanas vai iesniegšanas operāciju pabeigšanu un parādītu konkrētu kļūdas ziņojumu, varat kodam pievienot **throw error("ziņojums lietotājam")**, izmantojot komandķēdes paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="fec34-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="fec34-271">Tālāk ir trīs noderīgu paplašināmu metožu piemēri.</span><span class="sxs-lookup"><span data-stu-id="fec34-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="fec34-272">Ja **validateWrite** tabulā TSTimesheetLine atgriež **false** kādas darba laika uzskaites tabulas rindas saglabāšanas operācijas laikā, mobilajā programmā tiek parādīta kļūda.</span><span class="sxs-lookup"><span data-stu-id="fec34-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="fec34-273">Ja **validateSubmit** tabulā TSTimesheetTable atgriež **false** laikā, kad darba laika uzskaites tabula tiek iesniegta programmā, lietotājam tiek parādīta kļūda.</span><span class="sxs-lookup"><span data-stu-id="fec34-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="fec34-274">Joprojām darbosies loģika, kas aizpilda laukus (piemēram, **Rindas rekvizīts**) tabulai TSTimesheetLine metodes **ievietot** laikā.</span><span class="sxs-lookup"><span data-stu-id="fec34-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="fec34-275">Standarta komplektācijā ietverto lauku slēpšana un atzīmēšana kā tikai lasāmus, izmantojot konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="fec34-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="fec34-276">No projekta parametriem standarta komplektācijā ietvertos laukus mobilajā programmā varat padarīt par tikai lasāmiem vai paslēptiem.</span><span class="sxs-lookup"><span data-stu-id="fec34-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="fec34-277">Iestatiet opcijas lapas **Projektu vadības un uzskaites parametri** cilnes **Darba laika uzskaites tabula** sadaļā **Mobilās darba laika uzskaites tabulas**.</span><span class="sxs-lookup"><span data-stu-id="fec34-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektu parametri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="fec34-279">Tādu aktivitāšu maiņa, kuras ir pieejamas atlasīšanai, izmantojot paplašinājumus</span><span class="sxs-lookup"><span data-stu-id="fec34-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="fec34-280">Aktivitātes, kas projektam ir pieejamas atlasīšanai, tiek aizpildītas, izmantojot metodi **getActivitiesForProject()** un **getActivityQuery()** klasē **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fec34-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="fec34-281">Varat izmantot komandķēdi, lai mainītu šo uzvedību un padarītu to atbilstošu jūsu biznesa scenārijam attiecība uz aktivitātēm, kas ir pieejamas atlasīšanai kādam noteiktam projektam.</span><span class="sxs-lookup"><span data-stu-id="fec34-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="fec34-282">Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos</span><span class="sxs-lookup"><span data-stu-id="fec34-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="fec34-283">Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos notiek trīs līmeņos.</span><span class="sxs-lookup"><span data-stu-id="fec34-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="fec34-284">Lai sasniegtu vēlamo uzvedību, varat izmantot komandķēdi, lai paplašinātu šo uzvedību jebkurā līmenī vai visos šajos līmeņos.</span><span class="sxs-lookup"><span data-stu-id="fec34-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="fec34-285">Tiek izmantota tālāk aprakstītā hierarhija.</span><span class="sxs-lookup"><span data-stu-id="fec34-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="fec34-286">Programma mēģina ievietot noklusējuma kategoriju no projekta resursa.</span><span class="sxs-lookup"><span data-stu-id="fec34-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="fec34-287">Šī noklusējuma kategorija ir iestatīta metodē **getCurrentUserResource** un **getDelegatedResourcesForCurrentUser**, klasē **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="fec34-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="fec34-288">Ja noklusējuma kategorija nav norādīta projekta resursa līmenī, programma mēģina to izgūt no projekta aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="fec34-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="fec34-289">Šī noklusējuma kategorija ir iestatīta metodē **getActivitiesForProject**, klasē **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fec34-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="fec34-290">Ja noklusējuma kategorija nav norādīta projekta aktivitātes līmenī, noklusējuma kategorija tiek ņemta no projekta parametriem.</span><span class="sxs-lookup"><span data-stu-id="fec34-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="fec34-291">Šī noklusējuma kategorija ir iestatīta metodē **getProjectDetailsbyRule**, klasē **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fec34-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
