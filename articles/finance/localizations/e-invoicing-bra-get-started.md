---
title: เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับ บราซิล
description: หัวข้อนี้จะให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับบราซิล ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/19/2020
ms.locfileid: "4448592"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="a83d2-103">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับ บราซิล</span><span class="sxs-lookup"><span data-stu-id="a83d2-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="a83d2-104">Add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับบราซิล ไม่สนับสนุนฟังก์ชันทั้งหมดที่พร้อมใช้งานใน การรวมเอกสารทางการเงินที่สร้างขึ้นใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a83d2-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a83d2-105">หัวข้อนี้ให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็บราซิล</span><span class="sxs-lookup"><span data-stu-id="a83d2-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="a83d2-106">โดยจะแนะนำให้คุณทราบถึงขั้นตอนการตั้งค่าคอนฟิกที่มีประเทศขึ้นอยู่กับ ใน Regulatory Configuration Services (RCS) และ ใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a83d2-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="a83d2-107">นอกจากนี้คุณยังสามารถใช้กระบวนการในการส่งเอกสารทางการเงิน NF-E (แบบจำลองเอกสารทางการเงินอิเล็กทรอนิกส์ 55) โดยผ่านทางบริการ และอธิบายวิธีการตรวจทานผลลัพธ์การประมวลผลและสถานะของเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a83d2-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a83d2-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a83d2-108">Prerequisites</span></span>

<span data-ttu-id="a83d2-109">ก่อนที่คุณจะดำเนินการขั้นตอนในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการขั้นตอนต่างๆ ใน [การเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-get-started.md) ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="a83d2-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="a83d2-110">การตั้งค่า RCS</span><span class="sxs-lookup"><span data-stu-id="a83d2-110">RCS setup</span></span>

<span data-ttu-id="a83d2-111">ในระหว่างการตั้งค่า RCS คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="a83d2-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="a83d2-112">นำเข้าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับเอกสารทางการเงิน NF-E</span><span class="sxs-lookup"><span data-stu-id="a83d2-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="a83d2-113">ตรวจทานรูปแบบไฟล์ที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a83d2-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="a83d2-114">ตรวจทานรูปแบบไฟล์ที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a83d2-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="a83d2-115">ตั้งค่าคอนฟิกเหตุการณ์ที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a83d2-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="a83d2-116">ตั้งค่าคอนฟิกเหตุการณ์ที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a83d2-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="a83d2-117">กำหนดคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับสภาพแวดล้อม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="a83d2-118">เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="a83d2-119">"คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์" คือชื่อทั่วไปสำหรับทรัพยากรที่มีการตั้งค่าคอนฟิกและเผยแพร่ เพื่อใช้เซิร์ฟเวอร์ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="a83d2-120">การตั้งค่าของคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์ ซึ่งรวมถึงการใช้รูปแบบการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ (ER) เพื่อสร้างไฟล์การส่งออกและการนำเข้าที่สามารถจัดโครงแบบได้ และการใช้การดำเนินการและการดำเนินการขั้นตอน เพื่อเปิดใช้งานการสร้างกฎที่สามารถจัดโครงแบบได้ เพื่อส่งคำขอ นำเข้าการตอบสนอง และแยกเนื้อหาที่ตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="a83d2-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="a83d2-121">นำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="a83d2-122">ลงชื่อเข้าใช้บัญชี RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a83d2-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="a83d2-123">ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **คุณลักษณะ** ให้เลือกไทล์ **ใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="a83d2-124">บนหน้า **คุณลักษณะ e-Invoicing** ให้เลือก **นำเข้า** เพื่อนำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์เอกสารทางการเงิน NF-E จากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="a83d2-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![ปุ่มนำเข้า](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="a83d2-126">เลือกคุณลักษณะเอกสารทางการเงิน NF-E แล้วเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="a83d2-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![กำลังนำเข้าคุณลักษณะ NF-E](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="a83d2-128">สร้างคุณลักษณะของเอกสารทางการเงิน NF-E เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="a83d2-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="a83d2-129">บนหน้า **คุณลักษณะ e-Invoicing** บนแท็บ **เวอร์ชัน** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![การเพิ่มคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์เวอร์ชันใหม่](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="a83d2-131">อัพเดตเวอร์ชันการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="a83d2-131">Update the configuration version</span></span>

1. <span data-ttu-id="a83d2-132">บนหน้า **คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่าคอนฟิก** ให้เลือก **เพิ่ม** หรือ **ลบ** เพื่อจัดการเวอร์ชันการตั้งค่าคอนฟิก (การตั้งค่าคอนฟิกรูปแบบไฟล์ ER)</span><span class="sxs-lookup"><span data-stu-id="a83d2-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![การจัดการการตั้งค่าคอนฟิกคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="a83d2-134">เมื่อคุณสร้างเวอร์ชันใหม่ของคุณลักษณะเอกสารทางการเงิน NF-E เวอร์ชันการตั้งค่าคอนฟิกทั้งหมด (รูปแบบไฟล์ ER) จะถูกสืบทอดมาจากเวอร์ชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="a83d2-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="a83d2-135">ถ้าต้องการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ ต้องใช้เวอร์ชันการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a83d2-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="a83d2-136">รูปแบบการส่งออก NFe</span><span class="sxs-lookup"><span data-stu-id="a83d2-136">NFe submit export format</span></span>
        - <span data-ttu-id="a83d2-137">การนำเข้าข้อความตอบสนอง NFe</span><span class="sxs-lookup"><span data-stu-id="a83d2-137">NFe response message import</span></span>
        - <span data-ttu-id="a83d2-138">การนำเข้าล็อกข้อผิดพลาด NFe</span><span class="sxs-lookup"><span data-stu-id="a83d2-138">NFe error log import</span></span>

    - <span data-ttu-id="a83d2-139">เมื่อต้องการส่งการยกเลิก NF-E ต้องใช้เวอร์ชันการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a83d2-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="a83d2-140">รูปแบบการส่งออกการยกเลิก NFe</span><span class="sxs-lookup"><span data-stu-id="a83d2-140">NFe cancel export format</span></span>

2. <span data-ttu-id="a83d2-141">ในรายการ ให้เลือกเวอร์ชันการตั้งค่าคอนฟิก แล้วเลือก **แก้ไข** หรือ **ดู** เพื่อเปิดหน้า **ตัวออกแบบรูปแบบ** ซึ่งคุณสามารถแก้ไขหรือดูการตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="a83d2-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![การเปิดหน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="a83d2-143">ใช้หน้า **ตัวออกแบบรูปแบบ** เพื่อแก้ไข หรือดูการตั้งค่าคอนฟิกไฟล์รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a83d2-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="a83d2-144">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างการตั้งค่าคอนฟิกเอกสารอิเล็กทรอนิกส์](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)</span><span class="sxs-lookup"><span data-stu-id="a83d2-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![หน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="a83d2-146">จัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="a83d2-147">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ให้เลือก **เพิ่ม** หรือ **ลบ** เพื่อจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ (นั่นคือ เหตุการณ์ NF-E)</span><span class="sxs-lookup"><span data-stu-id="a83d2-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![การจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="a83d2-149">เมื่อคุณสร้างเวอร์ชันใหม่ของคุณลักษณะเอกสารทางการเงิน NF-E ที่สืบทอดมาจากคุณลักษณะของใบแจ้งหนี้อื่นๆ การตั้งค่าคุณลักษณะทั้งหมด (เหตุการณ์ NF-E) จะถูกสืบทอดมาจากเวอร์ชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="a83d2-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="a83d2-150">การส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ จำเป็นต้องมีการตั้งค่าคุณลักษณะ **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="a83d2-151">เมื่อต้องการส่งการยกเลิก NF-E จำเป็นต้องมีการตั้งค่าคุณลักษณะ **การยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="a83d2-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="a83d2-152">ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="a83d2-153">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="a83d2-154">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a83d2-154">Select **Edit**.</span></span>

    ![แก้ไขคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="a83d2-156">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![แท็บการดำเนินการ](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="a83d2-158">ตรวจทานการดำเนินการที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a83d2-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="a83d2-159">รหัสการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-159">Action ID</span></span> | <span data-ttu-id="a83d2-160">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-160">Action name</span></span>                  | <span data-ttu-id="a83d2-161">คำอธิบายการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="a83d2-162">1</span><span class="sxs-lookup"><span data-stu-id="a83d2-162">1</span></span>         | <span data-ttu-id="a83d2-163">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-163">Transform document</span></span>           | <span data-ttu-id="a83d2-164">สร้างไฟล์ XML ของ NF-E สำหรับการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="a83d2-165">2</span><span class="sxs-lookup"><span data-stu-id="a83d2-165">2</span></span>         | <span data-ttu-id="a83d2-166">ลงชื่อในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-166">Sign document</span></span>                | <span data-ttu-id="a83d2-167">ใช้ใบรับรองดิจิทัลกับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="a83d2-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="a83d2-168">3</span><span class="sxs-lookup"><span data-stu-id="a83d2-168">3</span></span>         | <span data-ttu-id="a83d2-169">บริการ Call Brazilian SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a83d2-170">ส่งไฟล์ XML ที่เซ็นรับรองแล้วไปยังบริการเว็บสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a83d2-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="a83d2-171">4</span><span class="sxs-lookup"><span data-stu-id="a83d2-171">4</span></span>         | <span data-ttu-id="a83d2-172">ประมวลผลการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="a83d2-172">Process response</span></span>             | <span data-ttu-id="a83d2-173">รับการตอบสนองการบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="a83d2-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="a83d2-174">5</span><span class="sxs-lookup"><span data-stu-id="a83d2-174">5</span></span>         | <span data-ttu-id="a83d2-175">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-175">Transform document</span></span>           | <span data-ttu-id="a83d2-176">แยกวิเคราะห์เนื้อหาของไฟล์ที่ได้รับเป็นการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="a83d2-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="a83d2-177">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="a83d2-177">6</span></span>         | <span data-ttu-id="a83d2-178">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-178">Transform document</span></span>           | <span data-ttu-id="a83d2-179">สร้างไฟล์ XML เพื่อสอบถามเกี่ยวกับสถานะของการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="a83d2-180">7</span><span class="sxs-lookup"><span data-stu-id="a83d2-180">7</span></span>         | <span data-ttu-id="a83d2-181">บริการ Call Brazilian SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a83d2-182">ส่งไฟล์ XML ที่ร้องขอสถานะการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="a83d2-183">8</span><span class="sxs-lookup"><span data-stu-id="a83d2-183">8</span></span>         | <span data-ttu-id="a83d2-184">ประมวลผลการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="a83d2-184">Process response</span></span>             | <span data-ttu-id="a83d2-185">รับการตอบสนองการบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="a83d2-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="a83d2-186">ตั้งค่า URL สำหรับบริการเว็บ SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="a83d2-187">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** บนแท็บ **การดำเนินการ** บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **3**)</span><span class="sxs-lookup"><span data-stu-id="a83d2-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="a83d2-188">บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการส่ง NF-E</span><span class="sxs-lookup"><span data-stu-id="a83d2-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="a83d2-189">บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **7**)</span><span class="sxs-lookup"><span data-stu-id="a83d2-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="a83d2-190">บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการส่ง NF-E</span><span class="sxs-lookup"><span data-stu-id="a83d2-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="a83d2-191">ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a83d2-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="a83d2-192">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **การยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="a83d2-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="a83d2-193">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a83d2-193">Select **Edit**.</span></span>
3. <span data-ttu-id="a83d2-194">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="a83d2-195">ตรวจทานการดำเนินการที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a83d2-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="a83d2-196">รหัสการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-196">Action ID</span></span> | <span data-ttu-id="a83d2-197">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-197">Action name</span></span>                  | <span data-ttu-id="a83d2-198">คำอธิบายการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a83d2-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="a83d2-199">1</span><span class="sxs-lookup"><span data-stu-id="a83d2-199">1</span></span>         | <span data-ttu-id="a83d2-200">แปลงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-200">Transform document</span></span>           | <span data-ttu-id="a83d2-201">สร้างไฟล์ XML การยกเลิกของ NF-E สำหรับการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="a83d2-202">2</span><span class="sxs-lookup"><span data-stu-id="a83d2-202">2</span></span>         | <span data-ttu-id="a83d2-203">ลงชื่อในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a83d2-203">Sign document</span></span>                | <span data-ttu-id="a83d2-204">ใช้ใบรับรองดิจิทัลกับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="a83d2-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="a83d2-205">3</span><span class="sxs-lookup"><span data-stu-id="a83d2-205">3</span></span>         | <span data-ttu-id="a83d2-206">บริการ Call Brazilian SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="a83d2-207">ส่งไฟล์ XML ที่เซ็นรับรองแล้วไปยังบริการเว็บสำหรับการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a83d2-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="a83d2-208">4</span><span class="sxs-lookup"><span data-stu-id="a83d2-208">4</span></span>         | <span data-ttu-id="a83d2-209">ประมวลผลการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="a83d2-209">Process response</span></span>             | <span data-ttu-id="a83d2-210">รับการตอบสนองการบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="a83d2-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="a83d2-211">ตั้งค่า URL สำหรับบริการเว็บ SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="a83d2-212">ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** บนแท็บ **การดำเนินการ** บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **3**)</span><span class="sxs-lookup"><span data-stu-id="a83d2-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="a83d2-213">บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการยกเลิก NF-E ที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="a83d2-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="a83d2-214">ทำให้สภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์มีอยู่ และกำหนดเวอร์ชันแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="a83d2-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="a83d2-215">บนหน้า **e-Invoicing Features** บนแท็บ **สภาพแวดล้อม** ให้เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="a83d2-216">ในฟิลด์ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a83d2-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="a83d2-217">ในฟิลด์ **มีผลบังคับใช้ตั้งแต่** ให้เลือกวันที่ที่สภาพแวดล้อมควรจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="a83d2-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="a83d2-218">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-218">Select **Enable**.</span></span>

![การเปิดใช้งานสภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="a83d2-220">เปลี่ยนสถานะเป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a83d2-220">Change the status to Completed</span></span>

1. <span data-ttu-id="a83d2-221">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="a83d2-222">เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="a83d2-223">เปลี่ยนสถานะเป็นเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="a83d2-223">Change the status to Publish</span></span>

1. <span data-ttu-id="a83d2-224">บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="a83d2-225">เลือก **เปลี่ยนแปลงสถานะ \> เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-225">Select **Change status \> Publish**.</span></span>

![เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="a83d2-227">ตั้งค่าการรวม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance หรือ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a83d2-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="a83d2-228">ในระหว่างขั้นตอน คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="a83d2-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="a83d2-229">เปิดใช้งานคุณลักษณะของ NF-E ของรัฐบาลกลางสำหรับบราซิล</span><span class="sxs-lookup"><span data-stu-id="a83d2-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="a83d2-230">นำเข้าแบบจำลองข้อมูล ER เฉพาะ การแม็ปแบบจำลองข้อมูล ER และรูปแบบที่จำเป็นสำหรับเอกสารทางการเงิน NF-e</span><span class="sxs-lookup"><span data-stu-id="a83d2-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="a83d2-231">นำเข้าการตั้งค่าคอนฟิก ER และตั้งค่าชนิดของการตอบสนองที่จำเป็นในการอัพเดตสถานะของเอกสารทางการเงิน หลังจากกระบวนการส่งถูกส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a83d2-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="a83d2-232">เปิดใช้งานคุณลักษณะของ NF-E สำหรับบราซิล</span><span class="sxs-lookup"><span data-stu-id="a83d2-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="a83d2-233">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="a83d2-234">บนแท็บ **คุณลักษณะ** ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** ในแถวสำหรับการอ้างอิงคุณลักษณะ **BR00053**</span><span class="sxs-lookup"><span data-stu-id="a83d2-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="a83d2-235">นำเข้าการแม็ปแบบจำลองข้อมูล ER ที่จำเป็นสำหรับเอกสารทางการเงิน NF-E</span><span class="sxs-lookup"><span data-stu-id="a83d2-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="a83d2-236">เข้าสู่ระบบ Finance</span><span class="sxs-lookup"><span data-stu-id="a83d2-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="a83d2-237">ในพื้นที่ทำงาน **รายงานอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือก **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a83d2-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="a83d2-238">ตรวจสอบให้แน่ใจว่ามีการตั้งค่าผู้ให้บริการการตั้งค่าคอนฟิกนี้เป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="a83d2-239">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าผู้ให้บริการเป็น **ใช้งานอยู่** ให้ดู [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</span><span class="sxs-lookup"><span data-stu-id="a83d2-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="a83d2-240">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="a83d2-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="a83d2-241">เลือก **ทรัพยากรส่วนกลาง \> เปิด**</span><span class="sxs-lookup"><span data-stu-id="a83d2-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="a83d2-242">นำเข้าการตั้งค่าคอนฟิก **การแม็ปเอกสารทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="a83d2-243">นำเข้าการตั้งค่าคอนฟิก ER และตั้งค่าชนิดของการตอบสนองสำหรับเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a83d2-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="a83d2-244">ในพื้นที่ทำงาน **รายงานอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือก **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a83d2-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="a83d2-245">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="a83d2-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="a83d2-246">เลือก **ทรัพยากรส่วนกลาง \> เปิด**</span><span class="sxs-lookup"><span data-stu-id="a83d2-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="a83d2-247">นำเข้า **การนำเข้าล็อกข้อผิดพลาด NF-e (BR)** **รูปแบบการนำเข้าข้อมูลการตอบสนอง NF-e (BR)** และ **การนำเข้าข้อความตอบสนอง NF-e (BR)**</span><span class="sxs-lookup"><span data-stu-id="a83d2-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="a83d2-248">ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="a83d2-249">บนแท็บ **เอกสารอิเล็กทรอนิกส์** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a83d2-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="a83d2-250">ในฟิลด์ **ชื่อตาราง** ให้ป้อน **ส่วนหัวของเอกสารทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="a83d2-251">ในฟิลด์ **บริบทของเอกสาร** ให้เลือก **รูปแบบบริบทของใบแจ้งหนี้ของลูกค้า – บริบทเอกสารทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="a83d2-252">เลือก **ชนิดของการตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-252">Select **Response types**.</span></span>
9. <span data-ttu-id="a83d2-253">เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** เลือก **การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="a83d2-254">ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="a83d2-255">ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อความตอบสนอง – การแม็ปแบบจำลองจากข้อความตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="a83d2-256">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a83d2-256">Select **Save**.</span></span>
13. <span data-ttu-id="a83d2-257">เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** ป้อน **ResponseData**</span><span class="sxs-lookup"><span data-stu-id="a83d2-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="a83d2-258">ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="a83d2-259">ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อมูลการตอบสนอง NFe – การนำเข้าข้อมูลการตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="a83d2-260">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a83d2-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="a83d2-261">การประมวลผลใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-261">Electronic invoice processing</span></span>

<span data-ttu-id="a83d2-262">ในระหว่างการประมวลผลใน Finance คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="a83d2-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="a83d2-263">ส่งเอกสารทางการเงินผ่านทาง add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="a83d2-264">ดูล็อกการดำเนินการการส่งและตรวจสอบผลลัพธ์ของการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="a83d2-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="a83d2-265">ส่งการยกเลิกของเอกสารทางการเงินผ่านทาง add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="a83d2-266">ส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="a83d2-267">หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการเก่าสำหรับการส่งเอกสารทางการเงิน NF-e สำหรับการตรวจสอบ (**กระบวนการ NF-e ส่งออก/นำเข้า**) จะไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="a83d2-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="a83d2-268">ซึ่งถูกแทนที่โดยกระบวนการใหม่ที่ชื่อ **ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="a83d2-269">ก่อนที่คุณจะดำเนินการต่อไป โปรดตรวจสอบให้แน่ใจว่าคุณมีเอกสารทางการเงินของลูกค้ารุ่น 55 อย่างน้อยหนึ่งรายการ ซึ่งออกโดยสถานที่จัดทำงบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a83d2-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="a83d2-270">ต้องมีการตั้งค่าทิศทางสำหรับเอกสารทางการเงินเหล่านี้เป็น **ขาออก** และต้องมีการ **สร้าง** สถานะ</span><span class="sxs-lookup"><span data-stu-id="a83d2-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="a83d2-271">สำหรับข้อมูลเพิ่มเติม ให้ดู [การออกเอกสารทางการเงินของลูกค้า (บราซิล)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document)</span><span class="sxs-lookup"><span data-stu-id="a83d2-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="a83d2-272">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="a83d2-273">สำหรับการส่งเอกสารฉบับแรกของเอกสารใดๆ ให้ตั้งค่าตัวเลือก **ส่งเอกสารใหม่** เป็น **ไม่** เสมอ</span><span class="sxs-lookup"><span data-stu-id="a83d2-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="a83d2-274">ถ้าคุณต้องส่งเอกสารผ่านทางบริการอีกครั้ง ให้กำหนดตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a83d2-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="a83d2-275">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบ **การสอบถาม** ซึ่งคุณสามารถสร้างการสอบถามเพื่อเลือกเอกสารสำหรับการส่งได้</span><span class="sxs-lookup"><span data-stu-id="a83d2-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="a83d2-276">บนแท็บ **การกำหนดช่วง** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a83d2-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="a83d2-277">ในฟิลด์ **ตาราง** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="a83d2-278">ในฟิลด์ **ตารางสืบทอด** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a83d2-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="a83d2-279">ในฟิลด์ **ฟิลด์** ให้เลือก **หมายเลข**</span><span class="sxs-lookup"><span data-stu-id="a83d2-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="a83d2-280">ในฟิลด์ **เงื่อนไข** ให้ป้อนหมายเลขของเอกสารทางการเงินที่ควรจะส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="a83d2-281">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="a83d2-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="a83d2-282">เลือก **ตกลง** เพื่อส่งเอกสารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83d2-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="a83d2-283">ในระหว่างความพยายามครั้งแรกของคุณในการส่งเอกสารผ่านทางบริการ คุณจะได้รับพร้อมท์ให้ยืนยันการเชื่อมต่อกับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="a83d2-284">เลือก **คลิกที่นี่เพื่อเชื่อมต่อกับ Electronic Document Submission Service**</span><span class="sxs-lookup"><span data-stu-id="a83d2-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="a83d2-285">ดูล็อกการส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a83d2-285">View all submission logs</span></span>

<span data-ttu-id="a83d2-286">หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** หน้าใหม่จะพร้อมใช้งาน ซึ่งช่วยให้คุณสามารถติดตามผลในกระบวนการส่งเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="a83d2-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="a83d2-287">คุณสามารถใช้หน้านี้เพื่อดูล็อกการส่งสำหรับเอกสารที่ส่งแล้วทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a83d2-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="a83d2-288">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a83d2-289">ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน** ที่จะกรองข้อมูลสำหรับเอกสารทางการเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a83d2-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="a83d2-290">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![การดูรายละเอียดล็อกการส่ง](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="a83d2-292">สำหรับเอกสารทางการเงิน NF-e คอลัมน์ **รหัสข้อผิดพลาด** จะแสดงรหัสส่งคืน ที่ส่งคืนโดยบริการเว็บ SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="a83d2-293">ดูล็อกการส่งผ่านหน้าเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a83d2-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="a83d2-294">หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่จัดโครงแบบ** คุณยังสามารถดูล็อกการส่งผ่านทางหน้าเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a83d2-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="a83d2-295">ไปที่ **บัญชีแยกประเภททั่วไป \> การสอบถามและรายงาน \> เอกสารทางการเงิน \> เอกสารทางการเงินทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a83d2-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="a83d2-296">เลือกเอกสารทางการเงินที่มีการส่งมาก่อนหน้านี้บน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="a83d2-297">บนบานหน้าต่างการดำเนินการ บนแท็บ **ภาครัฐ NF-e** เลือก **ล็อกเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![การดูล็อกการส่งจากหน้าเอกสารทางการเงิน](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="a83d2-299">ส่งเอกสารทางการเงิน NF-E ที่อนุมัติ สำหรับการยกเลิก SEFAZ</span><span class="sxs-lookup"><span data-stu-id="a83d2-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="a83d2-300">หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการเก่าสำหรับการยกเลิกเอกสารทางการเงิน NF-e จะไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="a83d2-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="a83d2-301">ซึ่งจะถูกแทนที่โดยกระบวนการยกเลิกใหม่ที่ฝังอยู่บนหน้า **ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="a83d2-302">ตรวจสอบให้แน่ใจว่าคุณได้รันการยกเลิกเอกสารทางการเงินของลูกค้าสำหรับเอกสารทางการเงิน NF-E ที่ได้รับอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="a83d2-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="a83d2-303">สำหรับข้อมูลเพิ่มเติม ให้ดู [ยกเลิกเอกสารทางการเงินของลูกค้า (บราซิล)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents)</span><span class="sxs-lookup"><span data-stu-id="a83d2-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="a83d2-304">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a83d2-305">เลือกเอกสารทางการเงิน แล้วเลือก **ฟังก์ชัน \> ส่งการส่งที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="a83d2-306">ป้อนคำอธิบายสำหรับการส่งที่เกี่ยวข้อง แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="a83d2-307">ดูล็อกการส่งการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a83d2-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="a83d2-308">ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="a83d2-309">ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน** ที่จะกรองข้อมูลสำหรับเอกสารทางการเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a83d2-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="a83d2-310">เลือกเอกสารทางการเงิน จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> การส่งที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="a83d2-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="a83d2-311">การส่งที่เกี่ยวข้องจะมีการส่งที่เกี่ยวข้องกับการส่งหลักที่ทำก่อน</span><span class="sxs-lookup"><span data-stu-id="a83d2-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="a83d2-312">ตัวอย่างเช่น การส่งที่อนุมัติ NF-E เฉพาะคือการส่งหลัก</span><span class="sxs-lookup"><span data-stu-id="a83d2-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="a83d2-313">การส่งที่ร้องขอการยกเลิก NF-E เดียวกันใน SEFAZ เป็นการส่งที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a83d2-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="a83d2-314">ซึ่งมีอยู่เนื่องจากกำลังร้องขอการยกเลิกงานที่ทำเสร็จแล้วผ่านการส่งอื่น</span><span class="sxs-lookup"><span data-stu-id="a83d2-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="a83d2-315">หน้า **การส่งที่เกี่ยวข้อง** จะแสดงการส่งที่เกี่ยวข้องทั้งหมด และสถานะการส่ง สำหรับเอกสารทางการเงินที่ให้</span><span class="sxs-lookup"><span data-stu-id="a83d2-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="a83d2-316">ในภาพประกอบต่อไปนี้ บรรทัดแรกแสดงถึงการส่งที่ร้องขอการอนุมัติของเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a83d2-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="a83d2-317">บรรทัดที่สองแสดงถึงการส่งที่ยกเลิกเอกสารทางการเงินนั้น</span><span class="sxs-lookup"><span data-stu-id="a83d2-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![การดูล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="a83d2-319">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง</span><span class="sxs-lookup"><span data-stu-id="a83d2-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![การดูรายละเอียดล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="a83d2-321">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="a83d2-321">Privacy notice</span></span>
<span data-ttu-id="a83d2-322">การเปิดใช้งานคุณลักษณะ BR-00053 (NF-e Federal) อาจจำเป็นต้องใช้การส่งข้อมูลที่จำกัด ซึ่งรวมถึงรหัสทะเบียนภาษีขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a83d2-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="a83d2-323">การทำเช่นนี้จะถูกส่งไปยังหน่วยงานของบุคคลที่สามที่ได้รับอนุมัติจากหน่วยงานจัดเก็บภาษี เพื่อวัตถุประสงค์ในการส่งใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับหน่วยงานจัดเก็บภาษี ในรูปแบบที่กำหนดไว้ล่วงหน้าซึ่งจำเป็นสำหรับการรวมกับเว็บเซอร์วิสของรัฐ</span><span class="sxs-lookup"><span data-stu-id="a83d2-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="a83d2-324">ผู้ดูแลระบบสามารถเปิดใช้งานและปิดใช้งานคุณลักษณะ BR-00053 (NF-e Federal) โดยนำทางไปยัง **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a83d2-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="a83d2-325">เลือกแท็บ **คุณลักษณะ** เลือกแถวที่มีคุณลักษณะของ BR-00053 แล้วทำการเลือกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="a83d2-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="a83d2-326">ข้อมูลที่นำเข้าจากระบบภายนอกเหล่านี้ไปยังบริการออนไลน์ของ Dynamics 365 อยู่ภายใต้ [คำชี้แจงสิทธิส่วนบุคคล](https://go.microsoft.com/fwlink/?LinkId=512132) ของเรา</span><span class="sxs-lookup"><span data-stu-id="a83d2-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="a83d2-327">กรุณาดูที่หัวข้อประกาศเกี่ยวกับความเป็นส่วนตัวในเอกสารประกอบลักษณะเฉพาะของประเทศ สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a83d2-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a83d2-328">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a83d2-328">Additional resources</span></span>

- [<span data-ttu-id="a83d2-329">ภาพรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="a83d2-330">เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="a83d2-331">ตั้งค่า add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a83d2-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
