---
title: Regulatory Configuration Services (RCS) - คุณลักษณะแบบโลกาภิวัตน์
description: หัวข้อนี้จะอธิบายถึงวิธีการใช้ Microsoft Regulatory Configuration Services (RCS) และที่เก็บส่วนกลางในการสร้างและใช้คุณลักษณะแบบโลกาภิวัตน์
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002809"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="f8fe2-103">Regulatory Configuration Services (RCS) - คุณลักษณะแบบโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8fe2-104">คุณสามารถใช้ Microsoft Regulatory Configuration Services (RCS) เพื่อสร้างคุณลักษณะแบบโลกาภิวัฒน์ ซึ่งสามารถใช้ในการบริการโลกาภิวัตน์ เช่น บริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="f8fe2-105">RCS ช่วยให้คุณสามารถดำเนินการงานเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="f8fe2-106">กำหนดส่วนประกอบที่เกี่ยวข้องของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-106">Define related components of a feature.</span></span>
- <span data-ttu-id="f8fe2-107">จัดการวงจรการใช้ของคุณลักษณะผ่านสถานะของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="f8fe2-108">ทำให้คุณลักษณะพร้อมใช้งานสำหรับสภาพแวดล้อมที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f8fe2-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="f8fe2-109">ใช้คุณลักษณะร่วมกับองค์กรอื่น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="f8fe2-110">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ใน RCS สามารถเพิ่มลักษณะการทำงานโลกาภิวัตน์และส่วนประกอบที่เกี่ยวข้อง อัปเดตสถานะของคุณลักษณะ และทำให้คุณลักษณะพร้อมใช้งานเพื่อให้สามารถใช้งานได้ในบริการโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="f8fe2-111">ก่อนที่คุณจะดำเนินการขั้นตอนนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการขั้นตอนที่เกี่ยวข้องกับงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="f8fe2-112">การเข้าถึงอินสแตนซ์ RCS</span><span class="sxs-lookup"><span data-stu-id="f8fe2-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="f8fe2-113">การสร้างและการเปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="f8fe2-114">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="f8fe2-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="f8fe2-115">ในอินสแตนซ์ของแอป Finance and Operations ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="f8fe2-116">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f8fe2-117">ถ้าไม่มีสภาพแวดล้อม RCS ที่จัดเตรียมสำหรับบริษัทของคุณ ให้เลือก **Regulatory Services – การตั้งค่าคอนฟิก** และทำตามคำแนะนำเพื่อจัดเตรียมสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f8fe2-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fe2-118">ถ้ามีการจัดเตรียมสภาพแวดล้อม RCS ให้กับบริษัทของคุณแล้ว ให้ใช้ URL ของหน้าเพื่อเข้าถึงสภาพแวดล้อมโดยเลือกตัวเลือกการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="f8fe2-119">เปิดใช้งานคุณลักษณะแบบโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="f8fe2-120">ในอินสแตนซ์ RCS ของคุณ ให้เลือกไทล์ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="f8fe2-121">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เลือก **คุณลักษณะแบบโลกาภิวัฒน์** ในรายการ แล้วเลือก **เปิดใช้งานเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![คุณลักษณะแบบโลกาภิวัตน์ในการจัดการคุณลักษณะ](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="f8fe2-123">คุณลักษณะที่ใช้ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-123">Globalization features</span></span>

<span data-ttu-id="f8fe2-124">เมื่อต้องการใช้คุณลักษณะแบบโลกาภิวัตน์ คุณต้องนำเข้าจากที่เก็บส่วนกลางและสร้างเวอร์ชันของคุณเองเป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="f8fe2-125">การเพิ่มคุณลักษณะแบบโลกาภิวัตน์มีอยู่สองวิธีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="f8fe2-126">เพิ่มคุณลักษณะที่สืบทอดมาซึ่งยึดตามคุณลักษณะที่มีอยู่ที่เผยแพร่แล้วหรือใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f8fe2-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="f8fe2-127">เพิ่มคุณลักษณะใหม่ที่คุณสร้างขึ้นตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="f8fe2-128">เข้าถึงคุณลักษณะแบบโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-128">Access Globalization features</span></span>

1. <span data-ttu-id="f8fe2-129">ตรวจสอบให้แน่ใจว่าคุณ **คุณลักษณะแบบโลกาภิวัฒน์** เปิดใช้งานในการจัดการคุณลักษณะ ดังที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="f8fe2-130">เปิดพื้นที่ทำงาน **คุณลักษณะแบบโลกาภิวัฒน์** จากนั้นภายใต้ **คุณลักษณะ** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![พื้นที่ทำงานของคุณลักษณะส่วนกลาง](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="f8fe2-132">หน้า **คุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="f8fe2-132">The **e-Invoicing Features** page is opened.</span></span>

    ![หน้าคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="f8fe2-134">เพิ่มคุณลักษณะแบบโลกาภิวัตน์ที่ได้รับมา</span><span class="sxs-lookup"><span data-stu-id="f8fe2-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="f8fe2-135">คุณสามารถเพิ่มคุณลักษณะแบบโลกาภิวัตน์ใหม่โดยรับมาจากคุณลักษณะที่มีอยู่ซึ่งเผยแพร่หรือใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f8fe2-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="f8fe2-136">เลือก **นำเข้า** เพื่อเปิดหน้า **นำเข้าคุณลักษณะจากหน้าที่เก็บส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![นำเข้าคุณลักษณะจากหน้าที่เก็บส่วนกลาง](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="f8fe2-138">เลือก **ซิงโครไนส์** เพื่อรับคุณลักษณะล่าสุด</span><span class="sxs-lookup"><span data-stu-id="f8fe2-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="f8fe2-139">รายการที่ซิงค์มีคุณลักษณะที่พร้อมใช้งานสำหรับคุณเนื่องจากมีการเผยแพร่โดย Microsoft หรือเนื่องจากมีการใช้ร่วมกับคุณโดยผู้ให้บริการการตั้งค่าคอนฟิกอื่น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![รายการของคุณลักษณะที่ซิงค์](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="f8fe2-141">ในรายการ ให้เลือกคุณลักษณะที่จะนำเข้า แล้วเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="f8fe2-142">คุณได้รับข้อความเมื่อคุณลักษณะที่เลือกนำเข้าเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="f8fe2-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![ข้อความการนำเข้าสำเร็จ](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="f8fe2-144">เลือก **เพิ่ม** จากนั้นในกล่องโต้ตอบแบบหล่นลง ให้เลือกตัวเลือก **ตามเวอร์ชันที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="f8fe2-145">ป้อนชื่อและคำอธิบายสำหรับคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="f8fe2-146">ในรายการของคุณลักษณะที่พร้อมใช้งาน ให้เลือกเวอร์ชันพื้นฐานของคุณลักษณะแล้วเลือก **สร้างคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![การเพิ่มคุณลักษณะที่ได้รับมา](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="f8fe2-148">คุณลักษณะที่คุณเพิ่มจะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![คุณลักษณะที่ได้รับมาที่มีสถานะแบบร่าง](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="f8fe2-150">ตรวจทานส่วนประกอบของคุณลักษณะเพื่อตรวจสอบว่ามีการอัปเดตที่จำเป็นหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="f8fe2-151">ตรวจทานการตั้งค่าคอนฟิก ในกรณีที่คุณจำเป็นต้องเลือกกำหนดรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) และการผูกข้อมูลกับการแม็ปรูปแบบสำหรับเวอร์ชันของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="f8fe2-152">ตรวจทานการตั้งค่า ในกรณีที่คุณต้องการเลือกกำหนดแท็บ **การดำเนินการ** แท็บ **กฎการใช้งาน** หรือแท็บ **ตัวแปร** สำหรับเวอร์ชันของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="f8fe2-153">บนแท็บ **เวอร์ชัน** ให้เลือก **วันที่เริ่มต้นที่มีผลบังคับใช้** และป้อนคำอธิบายถ้าฟิลด์ **คำอธิบาย** ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f8fe2-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="f8fe2-154">เลือก **เปลี่ยนสถานะ** เพื่อดำเนินการคุณลักษณะให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="f8fe2-155">คุณลักษณะที่เสร็จสมบูรณ์สามารถใช้งานได้สำหรับสภาพแวดล้อมเฉพาะ เพื่อให้สามารถใช้ในบริการโลกาภิวัตน์หรือสามารถเผยแพร่ไปยังที่เก็บส่วนกลางได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fe2-156">คุณลักษณะที่มีค่า **สถานะเวอร์ชันคุณลักษณะ** เป็น **เผยแพร่แล้ว** สามารถใช้ร่วมกันกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="f8fe2-157">เพิ่มคุณลักษณะแบบโลกาภิวัตน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="f8fe2-157">Add a new Globalization feature</span></span>

<span data-ttu-id="f8fe2-158">คุณสามารถเพิ่มคุณลักษณะโลกาภิวัตน์ใหม่ได้โดยการสร้างคุณลักษณะตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="f8fe2-159">บนหน้า **นำเข้าคุณลักษณะจากที่เก็บส่วนกลาง** ให้เลือก **เพิ่ม** แล้วในกล่องโต้ตอบแบบหล่นลงให้เลือกตัวเลือก **คุณลักษณะใหม่**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="f8fe2-160">ป้อนชื่อและคำอธิบายสำหรับคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="f8fe2-161">เลือก **สร้างคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-161">Select **Create feature**.</span></span>

    ![การเพิ่มคุณลักษณะใหม่](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="f8fe2-163">บนแท็บ **เวอร์ชัน** ให้เลือก **วันที่เริ่มต้นที่มีผลบังคับใช้** แล้วเลือก **เปลี่ยนสถานะ** เพื่อทำให้คุณลักษณะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="f8fe2-164">คุณลักษณะที่เสร็จสมบูรณ์สามารถใช้งานได้สำหรับสภาพแวดล้อมเฉพาะ เพื่อให้สามารถใช้ในบริการโลกาภิวัตน์หรือสามารถเผยแพร่ไปยังที่เก็บส่วนกลางได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fe2-165">คุณลักษณะที่มีค่า **สถานะเวอร์ชันคุณลักษณะ** เป็น **เผยแพร่แล้ว** สามารถใช้ร่วมกันกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="f8fe2-166">ภาพรวมส่วนประกอบคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-166">Feature component overview</span></span>

<span data-ttu-id="f8fe2-167">คุณลักษณะแบบโลกาภิวัฒน์มีส่วนประกอบหลายอย่างดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-167">Globalization features have several components:</span></span>

- <span data-ttu-id="f8fe2-168">**เวอร์ชัน** – ส่วนประกอบนี้สนับสนุนการจัดการวงจรการใช้ของคุณลักษณะ และช่วยให้ผู้ใช้สามารถจัดการสถานะสำหรับคุณลักษณะเวอร์ชันต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="f8fe2-169">**การตั้งค่าคอนฟิก** – ส่วนประกอบนี้ช่วยให้ผู้ใช้สามารถจัดการ ดู และแก้ไขรูปแบบ ER และการแม็ปรูปแบบที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="f8fe2-170">**การตั้งค่า** – ส่วนประกอบนี้จะช่วยให้ผู้ใช้ของบริการโลกาภิวัตน์ เช่น บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์ จัดการการตั้งค่าเวอร์ชันของเวอร์ชันคุณลักษณะที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f8fe2-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="f8fe2-171">ดังนั้นจึงสนับสนุนโครงสร้างการสื่อสารและกฎการตอบสนองที่ยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="f8fe2-172">**สภาพแวดล้อม** – ส่วนประกอบนี้ช่วยให้ผู้ใช้ของบริการโลกาภิวัตน์ เช่น บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์ จัดการสภาพแวดล้อมที่มีการใช้การตั้งค่าเวอร์ชันของคุณลักษณะและอนุญาตให้ผู้ใช้ที่สามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="f8fe2-173">**องค์กร** – ส่วนประกอบนี้ช่วยให้ผู้ใช้สามารถใช้คุณลักษณะร่วมกันกับองค์กรภายนอกได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="f8fe2-174">การตั้งค่าคอนฟิกส่วนประกอบของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="f8fe2-175">สถานะและรุ่น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-175">Version and status</span></span>

<span data-ttu-id="f8fe2-176">เวอร์ชันนี้ใช้ในการจัดการวงจรการใช้ของคุณลักษณะแบบโลกาภิวัฒน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="f8fe2-177">สถานะสามารถเปลี่ยนแปลงได้ในฟิลด์ **สถานะ** บนแท็บ **เวอร์ชัน** สถานะที่พร้อมใช้งานมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="f8fe2-178">**แบบร่าง** – สามารถแก้ไขคุณลักษณะได้เฉพาะเมื่ออยู่ในสถานะนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="f8fe2-179">**เสร็จสมบูรณ์** – คุณลักษณะและส่วนประกอบที่เกี่ยวข้องทั้งหมดได้รับการกำหนดขั้นสุดท้ายแล้ว (เสร็จสมบูรณ์) และไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="f8fe2-180">**เผยแพร่** – คุณลักษณะและส่วนประกอบที่เกี่ยวข้องทั้งหมดได้รับการเผยแพร่ไปยังที่เก็บส่วนกลางแล้ว</span><span class="sxs-lookup"><span data-stu-id="f8fe2-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="f8fe2-181">**ใช้ร่วมกัน** – คุณลักษณะและส่วนประกอบที่เกี่ยวข้องทั้งหมดถูกใช้ร่วมกันกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="f8fe2-182">**เปิดใช้งาน** – มีการเปิดใช้งานคุณลักษณะและส่วนประกอบที่เกี่ยวข้องทั้งหมดสำหรับใช้ในบริการโลกาภิวัตน์ เช่น บริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fe2-183">คุณลักษณะต้องย้ายตามลำดับผ่านบางสถานะเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="f8fe2-184">ดังนั้นจึงไม่สามารถใช้งานได้ทุกสถานะในทุกขั้นของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="f8fe2-185">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-185">Configurations</span></span>

<span data-ttu-id="f8fe2-186">การดำเนินการต่อไปนี้พร้อมใช้งานสำหรับการตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="f8fe2-187">**มุมมอง** – ดูการตั้งค่าคอนฟิกคุณลักษณะพื้นฐานที่ไม่จำเป็นต้องมีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="f8fe2-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="f8fe2-188">**แก้ไข** – สร้างเวอร์ชันแบบร่างของการตั้งค่าคอนฟิกที่เลือก เพื่อให้คุณสามารถแก้ไขรูปแบบหรือการแม็ปรูปแบบในโปรแกรมออกแบบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="f8fe2-189">**ลบ** – ลบการตั้งค่าคอนฟิกที่เลือกจากคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="f8fe2-190">**ปรับใช้ซ้ำ** – ปรับใช้คุณลักษณะซ้ำ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="f8fe2-191">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วนของ [คุณลักษณะแบบโลกาภิวัตน์ที่ได้รับมา](#rebase) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="f8fe2-192">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f8fe2-192">Setups</span></span>

<span data-ttu-id="f8fe2-193">การดำเนินการต่อไปนี้พร้อมใช้งานสำหรับการตั้งค่าคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="f8fe2-194">**เพิ่ม** – สร้างการตั้งค่าคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="f8fe2-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="f8fe2-195">การตั้งค่าคุณลักษณะนี้สามารถได้รับมาจากการตั้งค่าคุณลักษณะที่มีอยู่หรือสร้างขึ้นตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="f8fe2-196">**ลบ** – ลบการตั้งค่าคุณลักษณะที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="f8fe2-197">**มุมมอง** – ดูการตั้งค่าคุณลักษณะพื้นฐานที่ไม่จำเป็นต้องมีการเปลี่ยนแปลงใดๆ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="f8fe2-198">**แก้ไข** – สร้าง ลบ หรือปรับเปลี่ยนแอตทริบิวต์ของส่วนประกอบหลักสามรายการของการตั้งค่าคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="f8fe2-199">การดำเนินการและพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-199">Actions and their parameters</span></span>
    - <span data-ttu-id="f8fe2-200">กฎการนำไปใช้ได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-200">Applicability rules</span></span>
    - <span data-ttu-id="f8fe2-201">ตัวแปร</span><span class="sxs-lookup"><span data-stu-id="f8fe2-201">Variables</span></span>

![หน้าการตั้งค่าเวอร์ชันของคุณลักษณะ](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="f8fe2-203">สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f8fe2-203">Environments</span></span>

<span data-ttu-id="f8fe2-204">การดำเนินการต่อไปนี้พร้อมใช้งานสำหรับสภาพแวดล้อม:</span><span class="sxs-lookup"><span data-stu-id="f8fe2-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="f8fe2-205">**เปิดใช้งาน** – สำหรับเวอร์ชันของคุณลักษณะที่เลือก ให้เลือกสภาพแวดล้อมที่เผยแพร่ แล้วเลือก **วันที่เริ่มต้นที่มีผลบังคับใช้** เมื่อควรจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f8fe2-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="f8fe2-206">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ตั้งค่าคอนฟิกสภาพแวดล้อมสำหรับการเปิดใช้งาน](#configureenvironment) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="f8fe2-207">**ยกเลิก** – ลบสภาพแวดล้อมสำหรับการตั้งค่าคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="f8fe2-208">องค์กร</span><span class="sxs-lookup"><span data-stu-id="f8fe2-208">Organizations</span></span>

<span data-ttu-id="f8fe2-209">ให้ทำตามขั้นตอนต่อไปนี้เพื่อใช้คุณลักษณะโลกาภิวัตน์ร่วมกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="f8fe2-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="f8fe2-210">บนหน้าคุณลักษณะ **คุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ให้เลือกคุณลักษณะและเวอร์ชันของคุณลักษณะที่จะใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f8fe2-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="f8fe2-211">บนแท็บ **องค์กร** ให้เลือก **ใช้ร่วมกัน** จากนั้นในกล่องโต้ตอบแบบหล่นลง ให้ป้อนชื่อโดเมนขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f8fe2-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="f8fe2-212">เลือก **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-212">Select **Share**.</span></span>

    ![การใช้คุณลักษณะร่วมกับองค์กร](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="f8fe2-214">ใช้คุณลักษณะร่วมกันกับองค์กรที่เลือกและพร้อมใช้งานสำหรับองค์กรนั้นในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f8fe2-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="f8fe2-215">จากที่นี่สามารถนำเข้าคุณลักษณะไปยังอินสแตนซ์ขององค์กรของ RCS หรือ Dynamics 365 Finance เพื่อให้สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="f8fe2-216">ปรับใช้คุณลักษณะแบบโลกาภิวัตน์ที่ได้รับมาซ้ำ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="f8fe2-217">คุณสามารถปรับใช้คุณลักษณะแบบโลกาภิวัตน์ที่ได้รับมาไปยังเวอร์ชันของคุณลักษณะพื้นฐานใหม่หรือที่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="f8fe2-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="f8fe2-218">ด้วยวิธีนี้คุณสามารถอัปเดตการเปลี่ยนแปลงที่เกิดขึ้นในเวอร์ชันพื้นฐานโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="f8fe2-219">เวอร์ชันของคุณลักษณะพื้นฐานที่มีการอัปเดตจะถูกสร้างขึ้นโดยผู้ให้บริการการตั้งค่าคอนฟิกต้นทาง แล้วจึงเผยแพร่หรือใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f8fe2-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![เวอร์ชันของคุณลักษณะพื้นฐานที่อัปเดต](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="f8fe2-221">ตัวอย่างเช่น ถ้าคุณต้องการปรับใช้เวอร์ชันที่ได้รับมาของคุณลักษณะที่คุณสร้างขึ้น ก่อนอื่นคุณจะได้รับคุณลักษณะเวอร์ชันล่าสุดนี้โดยการนำเข้าจากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f8fe2-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="f8fe2-222">บนหน้า **คุณลักษณะของการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ให้เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="f8fe2-223">เลือก **ซิงโครไนส์** เพื่อรับคุณลักษณะล่าสุด</span><span class="sxs-lookup"><span data-stu-id="f8fe2-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="f8fe2-224">ในรายการของคุณลักษณะ ให้เลือกคุณลักษณะที่จะนำเข้า แล้วเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![การนำเข้าเวอร์ชันล่าสุดของคุณลักษณะ](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="f8fe2-226">ในรายการของคุณลักษณะ ให้เลือกคุณลักษณะที่จะปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="f8fe2-227">บนแท็บ **เวอร์ชัน** ให้เลือก **สร้าง** เพื่อสร้างเวอร์ชันแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="f8fe2-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![สร้างเวอร์ชันแบบร่างใหม่แล้ว](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="f8fe2-229">เลือก **ปรับใช้ซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="f8fe2-230">ในกล่องโต้ตอบ **ปรับใช้ซ้ำ** ให้เลือกคุณลักษณะเวอร์ชันล่าสุดเพื่อปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![กล่องโต้ตอบการปรับใช้ซ้ำ](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="f8fe2-232">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-232">Select **OK**.</span></span>
9. <span data-ttu-id="f8fe2-233">ตรวจทานส่วนประกอบของคุณลักษณะ และทำการเปลี่ยนแปลงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f8fe2-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="f8fe2-234">เลือก **เปลี่ยนสถานะ** เพื่อดำเนินการคุณลักษณะที่ปรับใช้ซ้ำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="f8fe2-235">เมื่อการปรับใช้ซ้ำเสร็จสมบูรณ์ คุณสามารถทำการดำเนินการเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="f8fe2-236">ตัวอย่างเช่น คุณสามารถเผยแพร่คุณลักษณะและทำให้พร้อมใช้งานสำหรับการใช้งานในบริการโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![สถานะคุณลักษณะที่อัปเดตเป็นเสร็จสมบูรณ์](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="f8fe2-238">ตั้งค่าคอนฟิกสภาพแวดล้อมสำหรับคุณลักษณะแบบโลกาภิวัตน์</span><span class="sxs-lookup"><span data-stu-id="f8fe2-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="f8fe2-239">ผู้ใช้ของบริการโลกาภิวัตน์สามารถจัดการสภาพแวดล้อมเพื่อตั้งค่าคุณลักษณะแบบโลกาภิวัฒน์และอนุญาตให้ผู้ใช้รายอื่นเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="f8fe2-240">ในพื้นที่ทำงาน **คุณลักษณะแบบโลกาภิวัฒน์** ภายใต้ **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="f8fe2-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![พื้นที่ทำงานของคุณลักษณะแบบโลกาภิวัตน์](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="f8fe2-242">เลือก **พารามิเตอร์ Key Vault** แล้วเลือก **สร้าง** เพื่อสร้างข้อมูลลับของ Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="f8fe2-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="f8fe2-243">ป้อนชื่อและคำอธิบายสำหรับ Key Vault จากนั้นในฟิลด์ **URI ของ Key Vault** ให้ป้อน URL ที่ระบุทรัพยากร Key Vault ใน Azure</span><span class="sxs-lookup"><span data-stu-id="f8fe2-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="f8fe2-244">บนแท็บด่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรอง และป้อนชื่อและคำอธิบายสำหรับใบรับรองแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![ใบรับรองถูกเพิ่ม](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="f8fe2-246">เลือก **สร้าง** เพื่อสร้างสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="f8fe2-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="f8fe2-247">ป้อนชื่อ คำอธิบาย และข้อมูลลับของโทเคนลายเซ็นที่ใช้การเข้าถึงร่วมกันที่จำเป็นสำหรับการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f8fe2-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="f8fe2-248">บนแท็บด่วน **ผู้ใช้** ให้เลือก **สร้าง** เพื่อเพิ่มผู้ใช้ที่จะมีสิทธิการได้รับอนุญาตให้เข้าถึงสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="f8fe2-249">ป้อนรหัสผู้ใช้และที่อยู่อีเมลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f8fe2-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="f8fe2-250">ให้ทำซ้ำขั้นตอนที่ 7 และ 8 เพื่อเพิ่มผู้ใช้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f8fe2-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="f8fe2-251">เลือก **เผยแพร่** เพื่อเผยแพร่สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f8fe2-251">Select **Publish** to publish the environment.</span></span>

    ![สภาพแวดล้อมที่เผยแพร่](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
