---
title: กำหนดค่าสภาพแวดล้อมการแสดงตัวอย่างของ Commerce
description: หัวข้อนี้อธิบายวิธีการกำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการดูตัวอย่างของ Microsoft Dynamics 365 Commerce หลังจากเตรียมใช้งาน
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906150"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="a9d79-103">กำหนดค่าสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a9d79-104">หัวข้อนี้อธิบายวิธีการกำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการดูตัวอย่างของ Microsoft Dynamics 365 Commerce หลังจากเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a9d79-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="a9d79-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="a9d79-105">Overview</span></span>

<span data-ttu-id="a9d79-106">ทำตามขั้นตอนในหัวข้อนี้เฉพาะหลังจากที่มีการเตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่าง Commerce แล้ว</span><span class="sxs-lookup"><span data-stu-id="a9d79-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="a9d79-107">สำหรับข้อมูลเกี่ยวกับวิธีจัดเตรียมสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ ดูที่ [เตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](provisioning-guide.md)</span><span class="sxs-lookup"><span data-stu-id="a9d79-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="a9d79-108">หลังจากที่สภาพแวดล้อมการแสดงตัวอย่าง Commerce ของคุณถูกเตรียมใช้งานอย่างทั่วถึง ขั้นตอนการตั้งค่าคอนฟิกการจัดสรรหลังการเตรียมใช้งานเพิ่มเติมต้องเสร็จสมบูรณ์ก่อนที่คุณจะสามารถเริ่มต้นการประเมินสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a9d79-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="a9d79-109">เพื่อทำตามขั้นตอนเหล่านี้ คุณต้องใช้ Lifecycle Services (LCS) Microsoft Dynamics, Dynamics 365 Commerce และ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="a9d79-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="a9d79-110">ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="a9d79-110">Before you start</span></span>

1. <span data-ttu-id="a9d79-111">ลงชื่อเข้าใช้ [พอร์ทัล LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="a9d79-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="a9d79-112">ไปที่โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-112">Go to your project.</span></span>
1. <span data-ttu-id="a9d79-113">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="a9d79-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a9d79-114">เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="a9d79-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="a9d79-115">ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="a9d79-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="a9d79-116">เลือก **ล็อกอิน** เพื่อเปิดเมนู จากนั้นเลือก **ล็อกออนเข้าสู่สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="a9d79-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="a9d79-117">ตรวจสอบให้มั่นใจว่านิติบุคคล **USRT** ถูกเลือกไว้แล้วในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="a9d79-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="a9d79-118">ตั้งค่าคอนฟิกการขายหน้าร้านใน LCS</span><span class="sxs-lookup"><span data-stu-id="a9d79-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="a9d79-119">เชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-119">Associate a worker with your identity</span></span>

<span data-ttu-id="a9d79-120">เพื่อเชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a9d79-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a9d79-121">ใช้เมนูบนด้านซ้าย ไปที่ **โมดูล \> การขายปลีก \> พนักงาน \> ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="a9d79-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="a9d79-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดต่อไปนี้ **000713 - Andrew Collette**</span><span class="sxs-lookup"><span data-stu-id="a9d79-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="a9d79-123">บนบานหน้าต่างการดำเนินการ เลือก **การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="a9d79-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="a9d79-124">เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="a9d79-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="a9d79-125">ในฟิลด์ **อีเมล** ทางขวาของ **ค้นหาโดยใช้อีเมล** ให้ป้อนที่อยู่อีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="a9d79-126">เลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="a9d79-126">Select **Search**.</span></span>
1. <span data-ttu-id="a9d79-127">เลือกเรกคอร์ดที่มีชื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="a9d79-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-128">Select **OK**.</span></span>
1. <span data-ttu-id="a9d79-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a9d79-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="a9d79-130">เรียกใช้ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="a9d79-130">Activate Cloud POS</span></span>

<span data-ttu-id="a9d79-131">ถ้าต้องการเปิดใช้งาน Cloud POS ใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a9d79-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a9d79-132">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="a9d79-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a9d79-133">เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="a9d79-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="a9d79-134">ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="a9d79-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="a9d79-135">เลือก **เข้าสู่ระบบ** เพื่อเปิดเมนู และจากนั้น เลือก **ล็อกออนเข้าสู่ Cloud Point of Sale** เพื่อเปิดจุดขาย (POS)</span><span class="sxs-lookup"><span data-stu-id="a9d79-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="a9d79-136">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="a9d79-136">Select **Next**.</span></span>
1. <span data-ttu-id="a9d79-137">เข้าสู่ระบบโดยใช้บัญชี Microsoft Azure Active Directory (Azure AD) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="a9d79-138">ภายใต้ **ชื่อร้านค้า** ให้เลือก **San Francisco**</span><span class="sxs-lookup"><span data-stu-id="a9d79-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="a9d79-139">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="a9d79-139">Select **Next**.</span></span>
1. <span data-ttu-id="a9d79-140">ภายใต้ **ลงทะเบียนและอุปกรณ์** เลือก **SANFRAN-1**</span><span class="sxs-lookup"><span data-stu-id="a9d79-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="a9d79-141">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a9d79-141">Select **Activate**.</span></span> <span data-ttu-id="a9d79-142">คุณได้ออกจากระบบและนำไปยังหน้าลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="a9d79-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="a9d79-143">ขณะนี้คุณสามารถลงชื่อเข้าสู่ประสบการณ์ Cloud POS ได้โดยใช้รหัสผู้ปฏิบัติงาน **000713** และรหัสผ่าน **123**</span><span class="sxs-lookup"><span data-stu-id="a9d79-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="a9d79-144">ตั้งค่าไซต์ของคุณใน Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-144">Set up your site in Commerce</span></span>

<span data-ttu-id="a9d79-145">หากต้องการเริ่มตั้งค่าไซต์แสดงตัวอย่างใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a9d79-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a9d79-146">ล็อกอินเข้าสู่เครื่องมือการจัดการไซต์ โดยใช้ URL ที่คุณจดบันทึกเมื่อคุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [การเริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))</span><span class="sxs-lookup"><span data-stu-id="a9d79-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="a9d79-147">เลือกไซต์ **Fabrikam** เพื่อเปิดกล่องโต้ตอบการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="a9d79-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="a9d79-148">เลือกโดเมนที่คุณป้อนเมื่อคุณเริ่มต้นอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="a9d79-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="a9d79-149">เลือก **ร้านค้าออนไลน์แบบขยายของ Fabrikam** เป็นช่องทางเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a9d79-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="a9d79-150">(ตรวจสอบให้แน่ใจว่าคุณได้เลือกร้านค้าออนไลน์ **แบบขยาย**)</span><span class="sxs-lookup"><span data-stu-id="a9d79-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="a9d79-151">เลือก **en-us** เป็นภาษาเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="a9d79-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="a9d79-152">ปล่อยให้ค่าของฟิลด์ **พาธ** เป็นตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a9d79-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="a9d79-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-153">Select **OK**.</span></span> <span data-ttu-id="a9d79-154">รายการของหน้าบนไซต์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a9d79-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="a9d79-155">เปิดใช้งานในการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="a9d79-155">Enable jobs in Retail</span></span>

<span data-ttu-id="a9d79-156">ในการเปิดใช้งานในการขายปลีก ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a9d79-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="a9d79-157">ลงชื่อเข้าสู่สภาพแวดล้อม (HQ)</span><span class="sxs-lookup"><span data-stu-id="a9d79-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="a9d79-158">ใช้เมนูด้านซ้ายเพื่อไปที่ **การขายปลีก \> การสอบถามและรายงาน \> ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="a9d79-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="a9d79-159">ขั้นตอนที่เหลือของขั้นตอนนี้ต้องเสร็จสมบูรณ์สำหรับแต่ละงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a9d79-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="a9d79-160">ประมวลผลการแจ้งเตือนทางอีเมลของใบสั่งของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="a9d79-160">Process retail order email notification</span></span>
    * <span data-ttu-id="a9d79-161">ความพร้อมใช้งานของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a9d79-161">Product availability</span></span>
    * <span data-ttu-id="a9d79-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="a9d79-162">P-0001</span></span>
    * <span data-ttu-id="a9d79-163">ซิงโครไนส์งานใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a9d79-163">Synchronize orders job</span></span>

1. <span data-ttu-id="a9d79-164">ใช้ตัวกรองด่วนเพื่อค้นหางานโดยใช้ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a9d79-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="a9d79-165">ถ้าสถานะของงานคือ **ระงับ** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a9d79-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="a9d79-166">เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a9d79-166">Select the record.</span></span>
    1. <span data-ttu-id="a9d79-167">ในบานหน้าต่างการดำเนินการ บนแท็บ **ชุดงาน** เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="a9d79-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="a9d79-168">เลือก **กำลังรอ** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="a9d79-169">รันการซิงโครไนส์ข้อมูลแบบเต็มใน Retail</span><span class="sxs-lookup"><span data-stu-id="a9d79-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="a9d79-170">หากต้องการรันการซิงโครไนส์ข้อมูลแบบเต็มใน Retail ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a9d79-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="a9d79-171">ใช้เมนูด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีก \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการขายปลีก \> ฐานข้อมูลช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="a9d79-172">ในรายการบนด้านซ้าย ช่องทาง **เริ่มต้น** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="a9d79-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="a9d79-173">เลือกช่องอื่นๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a9d79-173">Select the other available channel.</span></span> <span data-ttu-id="a9d79-174">ช่องนี้มีชื่อว่า **scXXXXXXXXX**</span><span class="sxs-lookup"><span data-stu-id="a9d79-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="a9d79-175">ในบานหน้าต่างการดำเนินการ เลือก **การซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a9d79-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="a9d79-176">ป้อนค่า **9999** ที่กำหนดการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="a9d79-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="a9d79-177">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-177">Select **OK**.</span></span>
1. <span data-ttu-id="a9d79-178">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a9d79-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="a9d79-179">ทดสอบข้อมูลบัตรเครดิตเพื่อทำการทดสอบการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a9d79-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="a9d79-180">เมื่อต้องการทำการทดสอบธุรกรรมบนไซต์ คุณสามารถใช้ข้อมูลบัตรเครดิตทดสอบดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a9d79-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="a9d79-181">**หมายเลขบัตร:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="a9d79-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="a9d79-182">**วันหมดอายุ:** 10/20</span><span class="sxs-lookup"><span data-stu-id="a9d79-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="a9d79-183">**รหัสค่าการตรวจสอบความถูกต้องของบัตร (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="a9d79-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9d79-184">ห้ามลองใช้ข้อมูลบัตรเครดิตจริงในไซต์ทดสอบไม่ว่าในสถานการณ์ใดๆ ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="a9d79-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a9d79-185">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a9d79-185">Next steps</span></span>

<span data-ttu-id="a9d79-186">หลังจากขั้นตอนการจัดเตรียมและการกำหนดค่าเสร็จสมบูรณ์แล้ว คุณก็พร้อมที่จะประเมินสภาพแวดล้อมการแสดงตัวอย่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9d79-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="a9d79-187">ใช้ URL ของเครื่องมือการจัดการไซต์ Commerce เพื่อไปยังประสบการณ์การเขียนแก้</span><span class="sxs-lookup"><span data-stu-id="a9d79-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="a9d79-188">ใช้ URL ของเครื่องมือการจัดการไซต์ Commerce เพื่อไปยังประสบการณ์ไซต์ลูกค้าขายปลีก</span><span class="sxs-lookup"><span data-stu-id="a9d79-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="a9d79-189">หากต้องการตั้งค่าคอนฟิกคุณสมบัติเพิ่มเติมของสภาพแวดล้อมการแสดงตัวอย่างของ Commerce ของคุณ ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](cpe-optional-features.md)</span><span class="sxs-lookup"><span data-stu-id="a9d79-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9d79-190">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a9d79-190">Additional resources</span></span>

[<span data-ttu-id="a9d79-191">ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a9d79-192">เตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="a9d79-193">กำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="a9d79-194">FAQ เกี่ยวกับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a9d79-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a9d79-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a9d79-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a9d79-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a9d79-197">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="a9d79-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a9d79-198">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a9d79-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="a9d79-199">แหล่งข้อมูลความช่วยเหลือสำหรับ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="a9d79-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
