---
title: ชนิดของปลายทาง ER อีเมล
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกปลายทางของปลายทางอีเมลสำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก
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
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020026"
---
# <span data-ttu-id="873f6-103"><a name="EmailDestinationType">ปลายทางของอีเมล</a></span><span class="sxs-lookup"><span data-stu-id="873f6-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="873f6-104">คุณสามารถตั้งค่าคอนฟิกปลายทางอีเมลของไฟล์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="873f6-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="873f6-105">เอกสารที่สร้างขึ้นจะถูกส่งเป็นเอกสารแนบของข้อความทางอิเล็กทรอนิกส์ โดยยึดตามการตั้งค่าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="873f6-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="873f6-106">ตั้งค่า **เปิดใช้งานอยู่**เป็น **ใช่** เพื่อส่งไฟล์เอาท์พุททางอีเมล</span><span class="sxs-lookup"><span data-stu-id="873f6-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="873f6-107">หลังจากที่เปิดใช้งานตัวเลือกนี้ คุณสามารถระบุผู้รับอีเมลและแก้ไขชื่อเรื่องและเนื้อหาอีเมลได้</span><span class="sxs-lookup"><span data-stu-id="873f6-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="873f6-108">คุณสามารถตั้งค่าข้อความค่าคงที่สำหรับชื่อเรื่องและเนื้อหาอีเมล หรือคุณสามารถใช้ [สูตร](er-formula-language.md) ER เพื่อสร้างข้อความอีเมลแบบไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="873f6-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="873f6-109">คุณสามารถตั้งค่าคอนฟิกที่อยู่อีเมลสำหรับ ER ได้สองวิธี</span><span class="sxs-lookup"><span data-stu-id="873f6-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="873f6-110">คุณสามารถดำเนินการตั้งค่าคอนฟิกให้เสร็จสมบูรณ์ได้ในลักษณะเดียวกับที่ใช้คุณสมบัติการจัดการการพิมพ์ หรือคุณสามารถแก้ไขที่อยู่อีเมลโดยใช้การอ้างอิงโดยตรงกับการตั้งค่าคอนฟิก ER ผ่านสูตร</span><span class="sxs-lookup"><span data-stu-id="873f6-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="873f6-111">[![เปิดใช้งานปลายทางของอีเมล](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="873f6-112">ชนิดของที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="873f6-112">Email address types</span></span>

<span data-ttu-id="873f6-113">เมื่อคุณเลือก **แก้ไข** ในฟิลด์ **ถึง** หรือ **Cc** กล่องโต้ตอบ **อีเมลถึง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="873f6-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="873f6-114">จากนั้นคุณสามารถเลือกชนิดของที่อยู่อีเมลที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="873f6-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="873f6-115">**อีเมลการตั้งค่าคอนฟิก** และ **การจัดการการพิมพ์** ได้รับการสนับสนุนในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="873f6-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="873f6-116">[![เลือกชนิดของอีเมล](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="873f6-117">การจัดการงานพิมพ์</span><span class="sxs-lookup"><span data-stu-id="873f6-117">Print management</span></span>

<span data-ttu-id="873f6-118">ถ้าคุณเลือกชนิดอีเมล **การจัดการการพิมพ์** คุณสามารถป้อนที่อยู่อีเมลถาวรในฟิลด์ **ถึง**</span><span class="sxs-lookup"><span data-stu-id="873f6-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="873f6-119">[![ตั้งค่าคอนฟิกที่อยู่อีเมลที่คงที่](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="873f6-120">เมื่อต้องการใช้ที่อยู่อีเมลที่คุณยังไม่ได้แก้ไข คุณต้องเลือกชนิดแหล่งที่มาของอีเมลสำหรับปลายทางของไฟล์</span><span class="sxs-lookup"><span data-stu-id="873f6-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="873f6-121">ค่าต่อไปนี้ได้รับการสนับสนุน: **ลูกค้า** **ผู้จัดจำหน่าย** **ผู้ที่มีแนวโน้มจะเป็นลูกค้า** **ผู้ติดต่อ** **คู่แข่ง** **ผู้ปฏิบัติงาน** **ผู้สมัคร** **ผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่าย**และ **ผู้จัดจำหน่ายที่ไม่ได้รับอนุญาต**</span><span class="sxs-lookup"><span data-stu-id="873f6-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="873f6-122">หลังจากที่คุณเลือกชนิดแหล่งที่มาของอีเมลแล้ว ให้ใช้ปุ่มที่อยู่ติดกับฟิลด์ **อีเมลบัญชีต้นทาง** เพื่อเปิดแบบฟอร์ม **โปรแกรมออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="873f6-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="873f6-123">คุณสามารถใช้แบบฟอร์มนี้เพื่อแนบสูตรที่ส่งคืนขณะรันไทม์ **บัญชีฝ่าย** ของชนิดแหล่งที่มาที่เลือกจากเอกสารที่ประมวลผลไปยังปลายทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="873f6-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="873f6-124">[![ตั้งค่าคอนฟิกบัญชีแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="873f6-125">สูตรการตั้งค่าคอนฟิก ER โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="873f6-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="873f6-126">ในฟิลด์ **สูตร** ให้ป้อนการอ้างอิงเฉพาะเอกสารไปยังลูกค้าหรือชนิดของฝ่ายผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="873f6-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="873f6-127">แทนที่จะพิมพ์ คุณสามารถค้นหาโหนดแหล่งข้อมูลที่แสดงถึงบัญชีลูกค้าหรือผู้จัดจำหน่าย และจากนั้น เลือก **เพิ่มแหล่งข้อมูล** เพื่อปรับปรุงสูตร</span><span class="sxs-lookup"><span data-stu-id="873f6-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="873f6-128">ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิก **การโอนย้ายเครดิต ISO 20022** โหนดที่แสดงบัญชีผู้จัดจำหน่ายคือ `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`</span><span class="sxs-lookup"><span data-stu-id="873f6-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="873f6-129">ถ้าคุณป้อนค่าสตริงเช่น `"DE-001"` และบันทึกสูตร จะมีการส่งอีเมลไปยังผู้ติดต่อของผู้จัดจำหน่าย **DE-001**</span><span class="sxs-lookup"><span data-stu-id="873f6-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="873f6-130">[![หน้าตัวออกแบบสูตร ER](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="873f6-131">[![ตั้งค่าคอนฟิกบัญชีแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="873f6-132">อีเมลการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="873f6-132">Configuration email</span></span>

<span data-ttu-id="873f6-133">ใช้ชนิดอีเมลนี้ถ้าการตั้งค่าคอนฟิกที่คุณใช้มีโหนดในแหล่งมาของข้อมูลที่ส่งคืน **ที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="873f6-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="873f6-134">คุณสามารถใช้แหล่งข้อมูลและฟังก์ชันในโปรแกรมออกแบบสูตรเพื่อดูที่อยู่อีเมลที่จัดรูปแบบอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="873f6-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="873f6-135">ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิก **การโอนย้ายเครดิต ISO 20022** โหนดที่แสดงที่อยู่อีเมลของผู้ติดต่อของผู้จัดจำหน่าย คือ `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`</span><span class="sxs-lookup"><span data-stu-id="873f6-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="873f6-136">[![ตั้งค่าคอนฟิกแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="873f6-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="873f6-137">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="873f6-137">Additional resources</span></span>

- [<span data-ttu-id="873f6-138">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="873f6-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="873f6-139">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="873f6-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="873f6-140">โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="873f6-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
