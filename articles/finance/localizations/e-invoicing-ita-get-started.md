---
title: เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับอิตาลี
description: หัวข้อนี้จะให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ อิตาลี ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: 08d41244d3ec785127db8f69e37dd522a463c388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988551"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="d1c12-103">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับอิตาลี</span><span class="sxs-lookup"><span data-stu-id="d1c12-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="d1c12-104">Add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับอิตาลีอาจไม่สนับสนุนฟังก์ชันทั้งหมดที่พร้อมใช้งานสำหรับใบแจ้งหนี้อิเล็กทรอนิกส์ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d1c12-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="d1c12-105">หัวข้อนี้ให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับอิตาลี</span><span class="sxs-lookup"><span data-stu-id="d1c12-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="d1c12-106">โดยจะแนะนำให้คุณทราบถึงขั้นตอนการตั้งค่าคอนฟิกที่มีประเทศขึ้นอยู่กับ ใน Regulatory Configuration Services (RCS) และ Finance</span><span class="sxs-lookup"><span data-stu-id="d1c12-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="d1c12-107">นอกจากนี้ยังสามารถแนะนำคุณผ่านกระบวนการสำหรับการส่งใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีการสร้างขึ้นในรูปแบบ **FatturaPA** เฉพาะของอิตาลี ผ่านทางบริการ และอธิบายวิธีการตรวจสอบผลลัพธ์ของการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="d1c12-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1c12-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d1c12-108">Prerequisites</span></span>

<span data-ttu-id="d1c12-109">ก่อนที่คุณจะดำเนินการขั้นตอนในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการขั้นตอนต่างๆ ใน [การเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-get-started.md) ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="d1c12-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="d1c12-110">การตั้งค่า RCS</span><span class="sxs-lookup"><span data-stu-id="d1c12-110">RCS setup</span></span>

<span data-ttu-id="d1c12-111">ในระหว่างการตั้งค่า RCS คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="d1c12-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="d1c12-112">นำเข้าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับการส่งออกใบแจ้งหนี้อิเล็กทรอนิกส์ของลูกค้าในรูปแบบ **FatturaPA**</span><span class="sxs-lookup"><span data-stu-id="d1c12-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="d1c12-113">ตรวจทานการตั้งค่าคอนฟิกรูปแบบที่จำเป็นสำหรับการสร้าง ส่ง และรับการตอบสนอง เกี่ยวกับใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="d1c12-114">ตั้งค่าคอนฟิกเหตุการณ์ที่สนับสนุนสถานการณ์การส่งใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="d1c12-115">เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="d1c12-116">"คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์" คือชื่อทั่วไปสำหรับทรัพยากรที่มีการตั้งค่าคอนฟิกและเผยแพร่ เพื่อใช้เซิร์ฟเวอร์ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="d1c12-117">ในกรณีนี้ การนำเข้าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ คือคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่คุณจะตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="d1c12-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="d1c12-118">นำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="d1c12-119">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d1c12-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="d1c12-120">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **คุณลักษณะ** ให้เลือกไทล์ **ใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="d1c12-121">บนหน้า **คุณลักษณะ e-Invoicing** ให้เลือก **นำเข้า** เพื่อนำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์จากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="d1c12-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1c12-122">ถ้าคุณไม่เห็นรายการของคุณลักษณะที่พร้อมใช้งานให้เลือก **ซิงโครไนส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="d1c12-123">เลือกคุณลักษณะ **ส่งออก e-Invoices (IT)** แล้วเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="d1c12-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![การนำเข้าคุณลักษณะส่งออก e-Invoices (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="d1c12-125">เมื่อคุณนำเข้าคุณลักษณะ **ส่งออก e-Invoices (IT)** จากที่เก็บส่วนกลาง การตั้งค่าทั้งหมดที่อธิบายไว้ในส่วนถัดไปจะถูกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="d1c12-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="d1c12-126">สร้างคุณลักษณะส่งออก e-Invoices (IT) เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="d1c12-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="d1c12-127">บนหน้า **คุณลักษณะ e-Invoicing** บนแท็บ **เวอร์ชัน** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![การเพิ่มคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์เวอร์ชันใหม่](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="d1c12-129">ถัดไป คุณจะตั้งค่าคอนฟิกรูปแบบการรายงานอิเล็กทรอนิกส์ (ER) ที่เกี่ยวข้องกับคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="d1c12-130">บนแท็บ **การตั้งค่าคอนฟิก** ให้เลือก **เพิ่ม** เพื่อจัดการเวอร์ชันการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="d1c12-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![การจัดการเวอร์ชันการตั้งค่าคอนฟิกคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="d1c12-132">ในขั้นตอนนี้ คุณกำลังเพิ่มและตั้งค่าคอนฟิกรูปแบบ ER ของไฟล์ที่แตกต่างกัน ที่ใช้ในการส่งออกใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี</span><span class="sxs-lookup"><span data-stu-id="d1c12-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="d1c12-133">สำหรับใบแจ้งหนี้อิเล็กทรอนิกส์ FatturaPA ของอิตาลี ให้ใช้การตั้งค่าคอนฟิกมาตรฐานต่อไปนี้ หรือการตั้งค่าคอนฟิกที่กำหนดเองจริงที่คุณใช้สำหรับใบแจ้งหนี้อิเล็กทรอนิกส์:</span><span class="sxs-lookup"><span data-stu-id="d1c12-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="d1c12-134">ใบแจ้งหนี้การขาย (IT)</span><span class="sxs-lookup"><span data-stu-id="d1c12-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="d1c12-135">ใบแจ้งหนี้ของโครงการ (IT)</span><span class="sxs-lookup"><span data-stu-id="d1c12-135">Project invoice (IT)</span></span>

    <span data-ttu-id="d1c12-136">เมื่อคุณสร้างคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่ได้รับมาจากคุณลักษณะของใบแจ้งหนี้อื่น รูปแบบ ER ทั้งหมดจะถูกสืบทอดมาจากคุณลักษณะดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="d1c12-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="d1c12-137">เลือกการตั้งค่าคอนฟิกไฟล์รูปแบบ ER เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d1c12-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="d1c12-138">เลือก **แก้ไข** หรือ **ดู** เพื่อเปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="d1c12-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![การเปิดหน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="d1c12-140">ใช้หน้า **ตัวออกแบบรูปแบบ** เพื่อแก้ไขหรือดูการตั้งค่าคอนฟิกไฟล์รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="d1c12-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![หน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="d1c12-142">จัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="d1c12-143">บนหน้า **คุณลักษณะของ ใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ให้เลือก **เพิ่ม** **ลบ** หรือ **แก้ไข** เพื่อจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![การจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="d1c12-145">ในขั้นตอนนี้ คุณตั้งค่าคอนฟิกเหตุการณ์ที่เกี่ยวข้องกับใบแจ้งหนี้อิเล็กทรอนิกส์ร วมถึงการสร้างไฟล์เอาต์พุต XML ในรูปแบบ **FatturaPA** และการเซ็นชื่อแบบดิจิตอล (ถ้าจำเป็น)</span><span class="sxs-lookup"><span data-stu-id="d1c12-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="d1c12-146">ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะของใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="d1c12-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="d1c12-147">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="d1c12-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="d1c12-148">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d1c12-148">Select **Edit**.</span></span>
3. <span data-ttu-id="d1c12-149">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="d1c12-150">การดำเนินการจะกำหนดรายการของการดำเนินงานที่ต้องรันตามลำดับ เพื่อทำให้การดำเนินการทั้งหมดของเหตุการณ์มีความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="d1c12-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![แท็บการดำเนินการ](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="d1c12-152">รหัสการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-152">Action ID</span></span> | <span data-ttu-id="d1c12-153">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-153">Action name</span></span>        | <span data-ttu-id="d1c12-154">คำอธิบายการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="d1c12-155">1</span><span class="sxs-lookup"><span data-stu-id="d1c12-155">1</span></span>         | <span data-ttu-id="d1c12-156">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d1c12-156">Transform document</span></span> | <span data-ttu-id="d1c12-157">สร้างไฟล์ XML ของใบแจ้งหนี้อิเล็กทรอนิกส์ ในรูปแบบ **FatturaPA**</span><span class="sxs-lookup"><span data-stu-id="d1c12-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="d1c12-158">2</span><span class="sxs-lookup"><span data-stu-id="d1c12-158">2</span></span>         | <span data-ttu-id="d1c12-159">ลงชื่อในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d1c12-159">Sign document</span></span>      | <span data-ttu-id="d1c12-160">ใช้ลายเซ็นดิจิทัลกับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="d1c12-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="d1c12-161">เลือกแท็บ **กฎการบังคับใช้** เพื่อดูและรักษากฎการบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d1c12-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="d1c12-162">กฎการบังคับใช้จะกำหนดบริบทที่จะมีการรันการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-162">Applicability rules define the context where the action will be run.</span></span>

    ![แท็บกฎการบังคับใช้](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="d1c12-164">เลือกแท็บ **ตัวแปร** เพื่อดูและรักษาตัวแปร</span><span class="sxs-lookup"><span data-stu-id="d1c12-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![แท็บตัวแปร](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="d1c12-166">กำหนดตัวแปรสาธารณะที่จำเป็นสำหรับการรันการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="d1c12-167">ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะของใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="d1c12-168">ขั้นตอนและการตั้งค่าที่จำเป็นในการตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะของ **ใบแจ้งหนี้โครงการ** จะคล้ายกับขั้นตอนและการตั้งค่าสำหรับการตั้งค่าคุณลักษณะ **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="d1c12-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="d1c12-169">เมื่อคุณทำงานกับใบแจ้งหนี้โครงการ ให้ดูที่ขั้นตอนสำหรับใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="d1c12-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="d1c12-170">กำหนดคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d1c12-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="d1c12-171">บนหน้า **e-Invoicing Features** บนแท็บ **สภาพแวดล้อม** ให้เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d1c12-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="d1c12-172">ในฟิลด์ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d1c12-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="d1c12-173">ในฟิลด์ **มีผลบังคับใช้ตั้งแต่** ให้เลือกวันที่ที่สภาพแวดล้อมควรจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d1c12-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="d1c12-174">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d1c12-174">Select **Enable**.</span></span> 

![การเปิดใช้งานสภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="d1c12-176">เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="d1c12-177">คุณสามารถเผยแพร่คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ โดยการเปลี่ยนสถานะเวอร์ชันเป็น **เสร็จสมบูรณ์** หรือ **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="d1c12-178">เปลี่ยนสถานะของเวอร์ชันเป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d1c12-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="d1c12-179">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="d1c12-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="d1c12-180">เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="d1c12-181">เปลี่ยนสถานะของเวอร์ชันเป็นเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d1c12-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="d1c12-182">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="d1c12-183">เลือก **เปลี่ยนแปลงสถานะ \> เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-183">Select **Change status \> Publish**.</span></span>

![การเปลี่ยนสถานะของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="d1c12-185">ตั้งค่าการรวม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance</span><span class="sxs-lookup"><span data-stu-id="d1c12-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="d1c12-186">ในระหว่างการตั้งค่าของ Finance คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="d1c12-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="d1c12-187">นำเข้าแบบจำลองข้อมูล ER การแม็ปแบบจำลองข้อมูล ER และการตั้งค่าคอนฟิกบริบทสำหรับใบแจ้งหนี้ FatturaPA</span><span class="sxs-lookup"><span data-stu-id="d1c12-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="d1c12-188">ตั้งค่าคอนฟิกใบรับรองที่จำเป็นสำหรับการเซ็นชื่อแบบดิจิทัลในใบแจ้งหนี้อิเล็กทรอนิกส์อิตาลี</span><span class="sxs-lookup"><span data-stu-id="d1c12-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="d1c12-189">นำเข้าแบบจำลองข้อมูล ER การแม็ปแบบจำลองข้อมูล และรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d1c12-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="d1c12-190">ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้ตรวจสอบว่ามีการตั้งค่าผู้ให้บริการ **บริการเอกสารทางธุรกิจ** เป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="d1c12-191">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="d1c12-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="d1c12-192">เลือก **ทรัพยากรส่วนกลาง \> เปิด**</span><span class="sxs-lookup"><span data-stu-id="d1c12-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="d1c12-193">นำเข้า **แบบจำลองใบแจ้งหนี้** **การแม็ปแบบจำลองใบแจ้งหนี้** และ **แบบจำลองบริบทใบแจ้งหนี้ของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d1c12-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="d1c12-194">เปิดใช้งานคุณลักษณะสำหรับการส่งออกใบแจ้งหนี้อิเล็กทรอนิกส์ของลูกค้าสำหรับอิตาลี</span><span class="sxs-lookup"><span data-stu-id="d1c12-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="d1c12-195">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d1c12-196">บนแท็บ **คุณลักษณะ** ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** ในแถวสำหรับการอ้างอิงคุณลักษณะ **IT00036**</span><span class="sxs-lookup"><span data-stu-id="d1c12-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![การเปิดใช้งานคุณลักษณะ FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="d1c12-198">การตั้งค่าคอนฟิกเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-198">Configure electronic documents</span></span>

1. <span data-ttu-id="d1c12-199">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d1c12-200">บนแท็บ **เอกสารอิเล็กทรอนิกส์** ให้เลือก **เพิ่ม** แล้วป้อนตารางที่จำเป็นในการสร้างใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี ดังนี้</span><span class="sxs-lookup"><span data-stu-id="d1c12-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="d1c12-201">**ชื่อตาราง:** สมุดรายวันใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d1c12-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="d1c12-202">**ชื่อตาราง:** ใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="d1c12-203">สำหรับแต่ละตาราง ให้กำหนดบริบทเอกสารที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="d1c12-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="d1c12-204">สำหรับ **สมุดรายวันใบแจ้งหนี้ของลูกค้า** ให้เลือก **บริบทใบแจ้งหนี้ของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d1c12-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="d1c12-205">สำหรับ **ใบแจ้งหนี้โครงการ** ให้เลือก **บริบทใบแจ้งหนี้โครงการ**</span><span class="sxs-lookup"><span data-stu-id="d1c12-205">For **Project invoice**, select **Project invoice context**.</span></span>

![การตั้งค่าชนิดของการตอบสนอง](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="d1c12-207">การประมวลผลใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-207">Electronic invoice processing</span></span>

<span data-ttu-id="d1c12-208">ในระหว่างการประมวลผลใน Finance คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="d1c12-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="d1c12-209">สร้างใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี โดยใช้ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="d1c12-210">ดูล็อกการดำเนินการและตรวจสอบผลลัพธ์ของการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="d1c12-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="d1c12-211">สร้างใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-211">Generate electronic invoices</span></span>

<span data-ttu-id="d1c12-212">หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** และเปิดใช้งานคุณลักษณะ **IT00036** กระบวนการ Finance เดิมสำหรับการสร้างใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี จะไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d1c12-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="d1c12-213">ซึ่งถูกแทนที่โดยกระบวนการใหม่ที่ชื่อ **ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="d1c12-214">คุณสามารถส่งเอกสารด้วยตนเอง ตามความต้องการของเอกสารใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="d1c12-215">ก่อนที่คุณจะดำเนินการต่อ ให้ตรวจสอบว่าการตั้งค่าที่จำเป็นสำหรับใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="d1c12-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="d1c12-216">สำหรับข้อมูลเพิ่มเติม ให้ดู [ใบแจ้งหนี้อิเล็กทรอนิกส์ของลูกค้า](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices)</span><span class="sxs-lookup"><span data-stu-id="d1c12-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="d1c12-217">โปรดทราบว่าขั้นตอนการตั้งค่าบางอย่างที่อธิบายไว้ในหัวข้อดังกล่าวอาจไม่พร้อมใช้งาน เนื่องจากการเรียกใช้ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="d1c12-218">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="d1c12-219">สำหรับการส่งเอกสารฉบับแรกของเอกสารใดๆ ให้ตั้งค่าตัวเลือก **ส่งเอกสารใหม่** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="d1c12-220">ถ้าคุณต้องส่งเอกสารผ่านทางบริการอีกครั้ง ให้กำหนดตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d1c12-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="d1c12-221">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบ **การสอบถาม** ซึ่งคุณสามารถสร้างการสอบถามเพื่อเลือกเอกสารสำหรับการส่งได้</span><span class="sxs-lookup"><span data-stu-id="d1c12-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![ส่งกล่องโต้ตอบเอกสารอิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="d1c12-223">กรองการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="d1c12-223">Filter query</span></span>

1. <span data-ttu-id="d1c12-224">ในกล่องโต้ตอบ **การสอบถาม** ให้ตั้งค่าคอนฟิกเงื่อนไขการกรองข้อมูลสำหรับทั้งใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ หรือปล่อยเงื่อนไขให้ว่างไว้เพื่อรวมใบแจ้งหนี้ที่ไม่ได้ส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d1c12-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![การตั้งค่าเงื่อนไขการกรองข้อมูลการส่ง](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="d1c12-226">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="d1c12-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="d1c12-227">เลือก **ตกลง** ส่งเอกสารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d1c12-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="d1c12-228">![หมายเหตุ] ในระหว่างความพยายามครั้งแรกของคุณในการส่งเอกสารผ่านทางบริการ คุณจะได้รับพร้อมท์ให้ยืนยันการเชื่อมต่อกับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="d1c12-229">เลือก **คลิกที่นี่เพื่อเชื่อมต่อกับ Electronic Document Submission Service**</span><span class="sxs-lookup"><span data-stu-id="d1c12-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="d1c12-230">ดูล็อกการส่ง</span><span class="sxs-lookup"><span data-stu-id="d1c12-230">View submission logs</span></span>

<span data-ttu-id="d1c12-231">คุณสามารถดูล็อกการส่งสำหรับเอกสารที่ส่งแล้วทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d1c12-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="d1c12-232">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d1c12-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="d1c12-233">ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **สมุดรายวันใบแจ้งหนี้ของลูกค้า** หรือ **ใบแจ้งหนี้โครงการ** ที่จะกรองข้อมูลเอกสารอิเล็กทรอนิกส์ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![การเลือกชนิดเอกสารเพื่อดูล็อกการส่ง](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="d1c12-235">ค่าที่แสดงในคอลัมน์ **สถานะการส่ง** แสดงสถานะของกระบวนการส่ง</span><span class="sxs-lookup"><span data-stu-id="d1c12-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="d1c12-236">บ่งชี้ว่ากระบวนการรันตามการตั้งค่าคอนฟิก และจำเป็นต้องมีการดำเนินการเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d1c12-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="d1c12-237">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="d1c12-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![การดูรายละเอียดล็อกการส่ง](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="d1c12-239">บนแท็บด่วน **การดำเนินการประมวลผล** คุณสามารถดูล็อกการดำเนินการสำหรับการดำเนินการที่ได้รับการตั้งค่าคอนฟิกในเวอร์ชันของคุณลักษณะที่ตั้งค่าไว้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="d1c12-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="d1c12-240">คอลัมน์ **สถานะ** แสดงว่ามีการรันการดำเนินการเสร็จเรียบร้อยแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d1c12-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="d1c12-241">บนแท็บด่วน **ไฟล์การดำเนินการ** คุณสามารถดูไฟล์กลางที่สร้างขึ้นในระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d1c12-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="d1c12-242">คุณสามารถเลือก **ดู** เพื่อดาวน์โหลดไฟล์ XML ผลลัพธ์ในรูปแบบ **FatturaPA** และดูเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="d1c12-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1c12-243">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="d1c12-243">Related topics</span></span>

- [<span data-ttu-id="d1c12-244">ภาพรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="d1c12-245">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="d1c12-246">ตั้งค่า add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1c12-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
