---
title: เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็กซิโก
description: หัวข้อนี้จะให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็กซิโกใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: ec7417d44a7c2aa413a9cda75996c153727632dd
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592657"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="0ff77-103">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="0ff77-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="0ff77-104">Add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็กซิโก อาจไม่สนับสนุนฟังก์ชันทั้งหมดที่พร้อมใช้งานใน Comprobante Fiscal Digital for Internet (CFDI) และในการรวมที่เกี่ยวข้องที่สร้างขึ้นใน Microsoft Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0ff77-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0ff77-105">หัวข้อนี้ให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="0ff77-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="0ff77-106">โดยจะแนะนำให้คุณทราบถึงขั้นตอนการตั้งค่าคอนฟิกที่มีประเทศขึ้นอยู่กับ ใน Regulatory Configuration Services (RCS) และ Finance</span><span class="sxs-lookup"><span data-stu-id="0ff77-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="0ff77-107">นอกจากนี้ยังสามารถแนะนำขั้นตอนต่างๆ ที่คุณต้องทำตามใน Finance เพื่อส่งใบแจ้งหนี้ CFDI ผ่านทางบริการ และอธิบายวิธีการตรวจทานผลลัพธ์การประมวลผลและสถานะของใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ff77-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0ff77-108">Prerequisites</span></span>

<span data-ttu-id="0ff77-109">ก่อนที่คุณจะดำเนินการขั้นตอนในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการขั้นตอนต่างๆ ใน [การเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-get-started.md) ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="0ff77-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="0ff77-110">การตั้งค่า RCS</span><span class="sxs-lookup"><span data-stu-id="0ff77-110">RCS setup</span></span>

<span data-ttu-id="0ff77-111">ในระหว่างการตั้งค่า RCS คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="0ff77-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="0ff77-112">นำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับประมวลผลใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="0ff77-113">ตรวจทานการตั้งค่าคอนฟิกรูปแบบที่จำเป็นสำหรับการสร้าง ส่ง และรับการตอบสนองเกี่ยวกับใบแจ้งหนี้ CFDI และเพื่อส่ง และรับการตอบสนองเกี่ยวกับการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0ff77-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="0ff77-114">ตั้งค่าคอนฟิกเหตุการณ์ที่สนับสนุนสถานการณ์การส่งใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="0ff77-115">เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff77-116">"คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์" คือชื่อทั่วไปสำหรับทรัพยากรที่มีการตั้งค่าคอนฟิกและเผยแพร่ เพื่อใช้เซิร์ฟเวอร์ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="0ff77-117">ในกรณีนี้ ใบแจ้งหนี้ CFDI (MX) เป็นคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่คุณจะตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0ff77-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="0ff77-118">นำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="0ff77-119">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0ff77-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0ff77-120">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **คุณลักษณะ** ให้เลือกไทล์ **ใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="0ff77-121">บนหน้า **คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์** ให้เลือก **นำเข้า** เพื่อนำเข้าคุณลักษณะ **ใบแจ้งหนี้ CFDI (MX)** จากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="0ff77-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ff77-122">ถ้าคุณไม่เห็นคุณลักษณะในรายการ ให้เลือก **ซิงโครไนส์** แแล้วทำซ้ำขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="0ff77-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![กำลังนำเข้าคุณลักษณะของใบแจ้งหนี้ CFDI (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="0ff77-124">เมื่อคุณนำเข้าคุณลักษณะ **ใบแจ้งหนี้ CFDI (MX)** จากที่เก็บส่วนกลาง การตั้งค่าคุณลักษณะทั้งหมด รวมถึงการตั้งค่าคอนฟิกและการดำเนินการ จะถูกนำเข้าด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="0ff77-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="0ff77-125">การสร้างคุณลักษณะของใบแจ้งหนี้ CFDI (MX) เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="0ff77-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="0ff77-126">คุณสามารถสร้างเวอร์ชันใหม่ได้ถ้าหาก ตัวอย่างเช่น ต้องอัพเดต Url</span><span class="sxs-lookup"><span data-stu-id="0ff77-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="0ff77-127">สำหรับข้อมูลเพิ่มเติม โปรดดู [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md)</span><span class="sxs-lookup"><span data-stu-id="0ff77-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="0ff77-128">บนหน้า **คุณลักษณะ e-Invoicing** บนแท็บ **เวอร์ชัน** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![การเพิ่มคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์เวอร์ชันใหม่](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="0ff77-130">อัพเดตเวอร์ชันการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="0ff77-130">Update the configuration version</span></span>

1. <span data-ttu-id="0ff77-131">บนหน้า **คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่าคอนฟิก** ให้เลือก **เพิ่ม** หรือ **ลบ** เพื่อจัดการเวอร์ชันการตั้งค่าคอนฟิก (การตั้งค่าคอนฟิกรูปแบบไฟล์ ER)</span><span class="sxs-lookup"><span data-stu-id="0ff77-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![การจัดการการตั้งค่าคอนฟิกคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="0ff77-133">เมื่อคุณสร้างเวอร์ชันใหม่ การตั้งค่าคอนฟิกทั้งหมดจะถูกสืบทอดมาจากเวอร์ชันที่เผยแพร่ครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="0ff77-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="0ff77-134">การประมวลผลใบแจ้งหนี้ CFDI จำเป็นต้องมีการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff77-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="0ff77-135">ใบแจ้งหนี้ CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="0ff77-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="0ff77-136">การนำเข้าข้อความตอบสนอง CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-136">CFDI response message import</span></span>
    - <span data-ttu-id="0ff77-137">การนำเข้าล็อกข้อผิดพลาด CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-137">CFDI error log import</span></span>
    - <span data-ttu-id="0ff77-138">การร้องขอการยกเลิก CFDI (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="0ff77-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="0ff77-139">ใบแจ้งหนี้ CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="0ff77-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="0ff77-140">ในรายการ ให้เลือกเวอร์ชันการตั้งค่าคอนฟิก แล้วเลือก **แก้ไข** หรือ **ดู** เพื่อเปิดหน้า **ตัวออกแบบรูปแบบ** ซึ่งคุณสามารถแก้ไขหรือดูการตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="0ff77-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![การเปิดหน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="0ff77-142">ใช้หน้า **ตัวออกแบบรูปแบบ** เพื่อแก้ไขหรือดูการตั้งค่าคอนฟิกไฟล์รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="0ff77-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="0ff77-143">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างการตั้งค่าคอนฟิกเอกสารอิเล็กทรอนิกส์](../../dev-itpro/analytics/electronic-reporting-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="0ff77-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![หน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="0ff77-145">จัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="0ff77-146">บนหน้า **คุณลักษณะของ ใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ให้เลือก **เพิ่ม** **ลบ** หรือ **แก้ไข** เพื่อจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![การจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="0ff77-148">เมื่อต้องการส่งใบแจ้งหนี้ CFDI สำหรับการตรวจสอบ (สร้างไฟล์ XML ส่งไฟล์ XML และประมวลผลการตอบสนอง) จำเป็นต้องมีการตั้งค่าคุณลักษณะ **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="0ff77-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="0ff77-149">เมื่อต้องการส่งการยกเลิกใบแจ้งหนี้ CFDI ต้องมีการตั้งค่าคุณลักษณะ **การยกเลิก** และ **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="0ff77-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="0ff77-150">ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะของใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="0ff77-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="0ff77-151">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="0ff77-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="0ff77-152">เลือก **แก้ไข** เพื่อตั้งค่าคอนฟิกการดำเนินการ กฎการบังคับใช้ และตัวแปร</span><span class="sxs-lookup"><span data-stu-id="0ff77-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![การแก้ไขการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="0ff77-154">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="0ff77-155">การดำเนินการจะกำหนดรายการของการดำเนินงานที่ต้องรันตามลำดับ เพื่อทำให้การดำเนินการทั้งหมดของเหตุการณ์มีความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="0ff77-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![แท็บการดำเนินการ](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="0ff77-157">รหัสการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-157">Action ID</span></span> | <span data-ttu-id="0ff77-158">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-158">Action</span></span>                   | <span data-ttu-id="0ff77-159">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-159">Action name</span></span>                                  | <span data-ttu-id="0ff77-160">คำอธิบายการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="0ff77-161">1</span><span class="sxs-lookup"><span data-stu-id="0ff77-161">1</span></span>         | <span data-ttu-id="0ff77-162">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="0ff77-162">Transform document</span></span>       | <span data-ttu-id="0ff77-163">สร้างใบแจ้งหนี้ E CFDI โดยไม่มีลายเซ็ฯดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="0ff77-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="0ff77-164">สร้างใบแจ้งหนี้อิเล็กทรอนิกส์ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="0ff77-165">2</span><span class="sxs-lookup"><span data-stu-id="0ff77-165">2</span></span>         | <span data-ttu-id="0ff77-166">ลงชื่อในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="0ff77-166">Sign document</span></span>            | <span data-ttu-id="0ff77-167">ลายเซ็นดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="0ff77-167">Digital sign</span></span>                                 | <span data-ttu-id="0ff77-168">ลายเซ็นแบบดิจิทัลสำหรับการส่งใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="0ff77-169">3</span><span class="sxs-lookup"><span data-stu-id="0ff77-169">3</span></span>         | <span data-ttu-id="0ff77-170">บริการ Call Mexican PAC</span><span class="sxs-lookup"><span data-stu-id="0ff77-170">Call Mexican PAC service</span></span> | <span data-ttu-id="0ff77-171">ส่ง CFDI E-Invoice</span><span class="sxs-lookup"><span data-stu-id="0ff77-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="0ff77-172">ไคลเอนต์ Windows Communication Foundation (WCF) ส่งใบแจ้งหนี้อิเล็กทรอนิกส์ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="0ff77-173">4</span><span class="sxs-lookup"><span data-stu-id="0ff77-173">4</span></span>         | <span data-ttu-id="0ff77-174">ประมวลผลการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="0ff77-174">Process response</span></span>         | <span data-ttu-id="0ff77-175">วิเคราะห์การตอบสนองการบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="0ff77-175">Analyze web service response</span></span>                 | <span data-ttu-id="0ff77-176">วิเคราะห์การตอบสนองการบริการเว็บ และส่งคืนล็อกข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="0ff77-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="0ff77-177">ตั้งค่า URL สำหรับบริการเว็บ Mexican PAC</span><span class="sxs-lookup"><span data-stu-id="0ff77-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="0ff77-178">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** บนแท็บ **การดำเนินการ** บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Mexican PAC**</span><span class="sxs-lookup"><span data-stu-id="0ff77-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="0ff77-179">บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ สำหรับการส่งใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff77-180">ใช้ขั้นตอนเดียวกันเพื่ออัพเดต URL สำหรับ **บริการ Call Mexican PAC** สำหรับการตั้งค่าคุณลักษณะ **ยกเลิก** และ **คำขอยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="0ff77-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="0ff77-181">กำหนดเวอร์ชันแบบร่างให้กับสภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="0ff77-182">บนหน้า **e-Invoicing Features** บนแท็บ **สภาพแวดล้อม** ให้เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="0ff77-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="0ff77-183">ในฟิลด์ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="0ff77-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="0ff77-184">ในฟิลด์ **มีผลบังคับใช้ตั้งแต่** ให้เลือกวันที่ที่สภาพแวดล้อมควรจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="0ff77-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="0ff77-185">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="0ff77-185">Select **Enable**.</span></span>

![การเปิดใช้งานสภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="0ff77-187">เปลี่ยนสถานะของเวอร์ชันเป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0ff77-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="0ff77-188">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="0ff77-189">เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="0ff77-190">เปลี่ยนสถานะของเวอร์ชันเป็นเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="0ff77-190">Change the version status to Published</span></span>

- <span data-ttu-id="0ff77-191">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือก **เปลี่ยนสถานะ \> เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="0ff77-192">เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="0ff77-193">บนหน้า **คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์** ให้เลือกแท็บ **เวอร์ชัน** เพื่อจัดการสถานะของคุณลักษณะ **ใบแจ้งหนี้ CFDI (MX)**</span><span class="sxs-lookup"><span data-stu-id="0ff77-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="0ff77-194">เลือก **เปลี่ยนสถานะ** เพื่อเปลี่ยนสถานะของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="0ff77-194">Select **Change status** to change the status of the feature.</span></span>

![การเปลี่ยนสถานะของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="0ff77-196">ตั้งค่าการรวม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance</span><span class="sxs-lookup"><span data-stu-id="0ff77-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="0ff77-197">เมื่อต้องการตั้งค่า add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0ff77-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="0ff77-198">นำเข้าแบบจำลองข้อมูล ER การแม็ปแบบจำลองข้อมูล ER และรูปแบบที่จำเป็นสำหรับใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="0ff77-199">ตั้งค่าคอนฟิกชนิดของการตอบสนองสำหรับการอัพเดตใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="0ff77-200">ชนิดของการตอบสนองเหล่านี้จะใช้สำหรับการตอบสนองจากเซิร์ฟเวอร์ของผู้ให้บริการใบรับรองที่ได้รับอนุญาต (PAC)</span><span class="sxs-lookup"><span data-stu-id="0ff77-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="0ff77-201">นำเข้าแบบจำลองข้อมูล ER การแม็ปแบบจำลองข้อมูล ER และการตั้งค่าคอนฟิกบริบทสำหรับใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="0ff77-202">เข้าสู่ระบบ Finance</span><span class="sxs-lookup"><span data-stu-id="0ff77-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="0ff77-203">ในพื้นที่ทำงาน **รายงานทางอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกชื่อ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="0ff77-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="0ff77-204">ตรวจสอบให้แน่ใจว่ามีการตั้งค่าผู้ให้บริการการตั้งค่าคอนฟิกนี้เป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="0ff77-205">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าผู้ให้บริการเป็น **ใช้งานอยู่** ให้ดู [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</span><span class="sxs-lookup"><span data-stu-id="0ff77-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="0ff77-206">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="0ff77-207">เลือก **ทรัพยากรส่วนกลาง \> เปิด**</span><span class="sxs-lookup"><span data-stu-id="0ff77-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="0ff77-208">นำเข้า **แบบจำลองใบแจ้งหนี้** **การแม็ปแบบจำลองใบแจ้งหนี้** **รูปแบบใบแจ้งหนี้ CFDI (MX)** **รูปแบบคำขอยกเลิกใบแจ้งหนี้ CFDI (MX)** และ **รูปแบบยกเลิกใบแจ้งหนี้ CFDI (MX)**</span><span class="sxs-lookup"><span data-stu-id="0ff77-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="0ff77-209">เปิดใช้งานคุณลักษณะสำหรับการประมวลผลใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="0ff77-210">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0ff77-211">บนแท็บ **คุณลักษณะ** ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** ในแถวสำหรับการอ้างอิงคุณลักษณะ **MX-00010** และ **MX-00016**</span><span class="sxs-lookup"><span data-stu-id="0ff77-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![การเปิดใช้งานคุณลักษณะสำหรับการประมวลผลใบแจ้งหนี้ CFDI](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="0ff77-213">นำเข้าการตั้งค่าคอนฟิก ER และตั้งค่าชนิดของการตอบสนองสำหรับการอัพเดตใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="0ff77-214">นำเข้าการตั้งค่าคอนฟิกของ ER</span><span class="sxs-lookup"><span data-stu-id="0ff77-214">Import ER configurations</span></span>

1. <span data-ttu-id="0ff77-215">ในพื้นที่ทำงาน **รายงานทางอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกชื่อ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="0ff77-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="0ff77-216">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="0ff77-217">เลือก **ทรัพยากรส่วนกลาง \> เปิด**</span><span class="sxs-lookup"><span data-stu-id="0ff77-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="0ff77-218">นำเข้า **แบบจำลองข้อความตอบสนอง** **การนำเข้าล็อกข้อผิดพลาด CFDI (MX)** และ **การนำเข้าข้อความตอบสนอง CFDI (MX)**</span><span class="sxs-lookup"><span data-stu-id="0ff77-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="0ff77-219">ตั้งค่าชนิดของการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="0ff77-219">Set up the response types</span></span>

1. <span data-ttu-id="0ff77-220">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0ff77-221">บนแท็บ **เอกสารอิเล็กทรอนิกส์** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="0ff77-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="0ff77-222">ป้อนสมุดรายวันใบแจ้งหนี้ของลูกค้า จากนั้น ในฟิลด์ **ชื่อตาราง** ให้เลือก ใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="0ff77-223">สำหรับแต่ละตาราง ให้กำหนดบริบทเอกสารที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="0ff77-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="0ff77-224">สำหรับ **สมุดรายวันใบแจ้งหนี้ของลูกค้า** ให้ป้อน **บริบทใบแจ้งหนี้ของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="0ff77-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="0ff77-225">สำหรับ **ใบแจ้งหนี้โครงการ** ให้ป้อน **บริบทใบแจ้งหนี้โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="0ff77-226">เลือก **ชนิดของการตอบสนอง** เพื่อตั้งค่าคอนฟิกชนิดของการตอบสนองที่สามารถส่งคืนจาก add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ และรวมอยู่ในสมุดรายวันใบแจ้งหนี้ของลูกค้า หรือใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="0ff77-227">เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** เลือก **การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="0ff77-228">ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="0ff77-229">ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อความตอบสนอง – การแม็ปแบบจำลองจากข้อความตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="0ff77-230">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0ff77-230">Select **Save**.</span></span>
9. <span data-ttu-id="0ff77-231">เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** เลือก **ResponseData**</span><span class="sxs-lookup"><span data-stu-id="0ff77-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="0ff77-232">ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="0ff77-233">ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อมูลการตอบสนอง CFDI (รายละเอียด) – การนำเข้าข้อมูลการตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="0ff77-234">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0ff77-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="0ff77-235">ประมวลผลใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance</span><span class="sxs-lookup"><span data-stu-id="0ff77-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="0ff77-236">ระหว่างการประมวลผลใบแจ้งหนี้ CFDI ใน Finance โดยใช้ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ คุณสามารถดำเนินการงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff77-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="0ff77-237">ส่งใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="0ff77-238">ดูล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff77-238">View the submission execution logs.</span></span>
- <span data-ttu-id="0ff77-239">ส่งการยกเลิกของใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="0ff77-240">ส่งใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-240">Submit CFDI invoices</span></span>

<span data-ttu-id="0ff77-241">หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการ **ใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับการส่งออก/การนำเข้า** (**บัญชีลูกหนี้ \> ใบแจ้งหนี้ \> ใบแจ้งหนี้อิเล็กทรอนิกส์**) สำหรับการส่งใบแจ้งหนี้ CFDI ไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="0ff77-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="0ff77-242">ซึ่งถูกแทนที่โดยกระบวนการใหม่ที่ชื่อ **ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff77-243">ก่อนที่คุณจะใช้กระบวนการ **ส่งเอกสารอิเล็กทรอนิกส์** ใหม่ ให้ตรวจสอบว่าการตั้งค่าที่จำเป็นสำหรับใบแจ้งหนี้อิเล็กทรอนิกส์ของเม็กซิโกเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0ff77-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="0ff77-244">สำหรับข้อมูลเพิ่มเติม ให้ดู [โครงร่าง CFDI เวอรชัน 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3)</span><span class="sxs-lookup"><span data-stu-id="0ff77-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="0ff77-245">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="0ff77-246">สำหรับการส่งเอกสารฉบับแรกของเอกสารใดๆ ให้ตั้งค่าตัวเลือก **ส่งเอกสารใหม่** เป็น **ไม่** เสมอ</span><span class="sxs-lookup"><span data-stu-id="0ff77-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="0ff77-247">ถ้าคุณต้องส่งเอกสารผ่านทางบริการอีกครั้ง ให้กำหนดตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0ff77-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="0ff77-248">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบ **การสอบถาม** ซึ่งคุณสามารถสร้างการสอบถามเพื่อเลือกเอกสารสำหรับการส่งได้</span><span class="sxs-lookup"><span data-stu-id="0ff77-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![การส่งเอกสาร CFDI](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="0ff77-250">ในระหว่างความพยายามครั้งแรกของคุณในการส่งเอกสารผ่านทางบริการ คุณจะได้รับพร้อมท์ให้ยืนยันการเชื่อมต่อกับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="0ff77-251">เลือก **คลิกที่นี่เพื่อเชื่อมต่อกับ Electronic Document Submission Service**</span><span class="sxs-lookup"><span data-stu-id="0ff77-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="0ff77-252">ดูล็อกการส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff77-252">View submission logs</span></span>

<span data-ttu-id="0ff77-253">คุณสามารถดูบันทึกการส่งสำหรับเอกสารที่ส่งทั้งหมด หรือสำหรับเอกสารที่ส่งเพียงรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="0ff77-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="0ff77-254">ดูล็อกการส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0ff77-254">View all submission logs</span></span>

<span data-ttu-id="0ff77-255">หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** หน้าใหม่จะพร้อมใช้งาน ซึ่งช่วยให้คุณสามารถติดตามผลในกระบวนการส่งเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="0ff77-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="0ff77-256">คุณสามารถใช้หน้านี้เพื่อดูล็อกการส่งสำหรับเอกสารที่ส่งแล้วทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0ff77-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="0ff77-257">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="0ff77-258">ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **สมุดรายวันใบแจ้งหนี้ของลูกค้า** ที่จะกรองข้อมูลเอกสารอิเล็กทรอนิกส์ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![การเลือกชนิดเอกสารเพื่อดูล็อกการส่ง](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="0ff77-260">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff77-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![การดูรายละเอียดล็อกการส่ง](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="0ff77-262">รายละเอียดในล็อกการส่งจะถูกแบ่งระหว่างแท็บด่วนสามแท็บต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff77-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="0ff77-263">**การดำเนินการประมวลผล** – แท็บด่วนนี้แสดงล็อกการดำเนินการสำหรับการดำเนินการที่ได้รับการตั้งค่าคอนฟิกในเวอร์ชันของคุณลักษณะที่ตั้งค่าไว้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="0ff77-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="0ff77-264">คอลัมน์ **สถานะ** แสดงว่ามีการรันการดำเนินการเสร็จเรียบร้อยแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff77-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="0ff77-265">**ไฟล์การดำเนินการ** – แท็บด่วนนี้แสดงไฟล์กลางที่สร้างขึ้นในระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ff77-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="0ff77-266">คุณสามารถเลือก **มุมมอง** เพื่อดาวน์โหลดและดูไฟล์ได้</span><span class="sxs-lookup"><span data-stu-id="0ff77-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="0ff77-267">**ล็อกการดำเนินการการประมวลผล** – แท็บด่วนนี้แสดงผลลัพธ์ของการสื่อสารระหว่าง add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ และบริการเว็บเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="0ff77-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="0ff77-268">นอกจากนี้ยังแสดงสิ่งที่ส่งคืนโดยการประมวลผลจากบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="0ff77-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="0ff77-269">คอลัมน์ **รหัสข้อผิดพลาด** จะแสดงรหัสส่งคืน ที่ส่งคืนโดยบริการเว็บของการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="0ff77-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="0ff77-270">เมื่อใบแจ้งหนี้ CFDI ที่ส่งได้รับอนุญาตให้ใช้ สถานะจะได้รับการอัพเดตเป็น **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="0ff77-271">ดูล็อกการส่งจากใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="0ff77-272">หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ใบแจ้งหนี้ ConfigurableElectronic** คุณยังสามารถดูล็อกการส่งจากใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="0ff77-273">ไปที่ การสอบถาม **บัญชีลูกหนี้ \> และรายงาน \> CFDI (ใบแจ้งหนี้อิเล็กทรอนิกส์)**</span><span class="sxs-lookup"><span data-stu-id="0ff77-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="0ff77-274">เลือกใบแจ้งหนี้ CFDI ที่ส่งหลังจากเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="0ff77-275">บนบานหน้าต่างการดำเนินการ บนแท็บ **ประวัติ** เลือก **ล็อกเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![การดูล็อกการส่งจากใบแจ้งหนี้ CFDI](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="0ff77-277">สำหรับใบแจ้งหนี้ CFDI ที่ส่งก่อนที่จะเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** ปุ่ม **ประวัติ** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0ff77-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="0ff77-278">ปุ่ม **ประวัติ** ไม่พร้อมใช้งานสำหรับใบแจ้งหนี้ CFDI ที่ส่งหลังจากเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ**</span><span class="sxs-lookup"><span data-stu-id="0ff77-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="0ff77-279">ส่งการยกเลิกของใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="0ff77-280">หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการเก่าสำหรับการยกเลิกใบแจ้งหนี้ CFDI จะไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="0ff77-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="0ff77-281">ซึ่งจะถูกแทนที่โดยกระบวนการยกเลิกใหม่ที่ฝังอยู่บนหน้า **ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="0ff77-282">ไปที่ การสอบถาม **บัญชีลูกหนี้ \> และรายงาน \> CFDI (ใบแจ้งหนี้อิเล็กทรอนิกส์)**</span><span class="sxs-lookup"><span data-stu-id="0ff77-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="0ff77-283">ถ้าใบแจ้งหนี้ CFDI มีสถานะเป็น **อนุมัติ** ให้เลือก **ฟังก์ชัน \> ยกเลิก CFDI**</span><span class="sxs-lookup"><span data-stu-id="0ff77-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="0ff77-284">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="0ff77-285">เลือกใบแจ้งหนี้ CFDI แล้วเลือก **ฟังก์ชัน \> ส่งการส่งที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="0ff77-286">ป้อนคำอธิบายสำหรับการส่งที่เกี่ยวข้อง แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="0ff77-287">ดูล็อกการส่งการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0ff77-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="0ff77-288">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="0ff77-289">ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **สมุดรายวันใบแจ้งหนี้ของลูกค้า** ที่จะกรองข้อมูลสำหรับเอกสารสมุดรายวันใบแจ้งหนี้ลูกค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff77-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="0ff77-290">เลือกใบแจ้งหนี้ CFDI จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> การส่งที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="0ff77-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="0ff77-291">หน้า **การส่งที่เกี่ยวข้อง** จะแสดงการส่งที่เกี่ยวข้องทั้งหมด และสถานะการส่ง สำหรับใบแจ้งหนี้ที่กำหนดให้กับใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="0ff77-292">ในภาพประกอบต่อไปนี้ บรรทัดแรกแสดงถึงการส่งที่ร้องขอการอนุมัติของใบแจ้งหนี้ CFDI</span><span class="sxs-lookup"><span data-stu-id="0ff77-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="0ff77-293">บรรทัดที่สองแสดงถึงการส่งที่ยกเลิกใบแจ้งหนี้ CFDI นั้น</span><span class="sxs-lookup"><span data-stu-id="0ff77-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![การดูล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="0ff77-295">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff77-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![การดูรายละเอียดล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="0ff77-297">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="0ff77-297">Privacy notice</span></span>
<span data-ttu-id="0ff77-298">การเปิดใช้งานคุณลักษณะ **CFDI ใบแจ้งหนี้อิเลคทรอนิคส์เม็กซิกัน (MX)** อาจจำเป็นต้องส่งข้อมูลที่จำกัด ซึ่งรวมถึงการลงทะเบียนภาษีขององค์กร</span><span class="sxs-lookup"><span data-stu-id="0ff77-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="0ff77-299">การทำเช่นนี้จะถูกส่งไปยังหน่วยงานของบุคคลที่สามที่ได้รับอนุมัติจากหน่วยงานจัดเก็บภาษี เพื่อวัตถุประสงค์ในการส่งใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับหน่วยงานจัดเก็บภาษี ในรูปแบบที่กำหนดไว้ล่วงหน้าซึ่งจำเป็นสำหรับการรวมกับเว็บเซอร์วิสของรัฐ</span><span class="sxs-lookup"><span data-stu-id="0ff77-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="0ff77-300">ผู้ดูแลระบบสามารถเปิดและปิดใช้งานคุณลักษณะ **CFDI ใบแจ้งหนี้อิเล็กทรอนิกส์เม็กซิกัน (MX)** ได้โดยไปยัง **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0ff77-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="0ff77-301">เลือกแท็บ **คุณลักษณะ**  เลือกแถวที่มีคุณลักษณะ **CFDI ใบแจ้งหนี้อิเล็กทรอนิกส์เม็กซิกัน (MX)** แล้วทำการเลือกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="0ff77-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="0ff77-302">ข้อมูลที่นำเข้าจากระบบภายนอกเหล่านี้ไปยังบริการออนไลน์ของ Dynamics 365 อยู่ภายใต้ [คำชี้แจงสิทธิส่วนบุคคล](https://go.microsoft.com/fwlink/?LinkId=512132) ของเรา</span><span class="sxs-lookup"><span data-stu-id="0ff77-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="0ff77-303">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อประกาศเกี่ยวกับความเป็นส่วนตัวในเอกสารประกอบลักษณะเฉพาะของประเทศ</span><span class="sxs-lookup"><span data-stu-id="0ff77-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ff77-304">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0ff77-304">Additional resources</span></span>

- [<span data-ttu-id="0ff77-305">ภาพรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="0ff77-306">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="0ff77-307">ตั้งค่า add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0ff77-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
