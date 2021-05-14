---
title: ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมิน Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce หลังจากจัดเตรียมแล้ว
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b291a6515c6a3ae7382ea2ad8024ca036489de19
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937049"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="c0cef-103">ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมิน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0cef-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce หลังจากจัดเตรียมแล้ว</span><span class="sxs-lookup"><span data-stu-id="c0cef-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="c0cef-105">ดำเนินการกระบวนงานในหัวข้อนี้ให้เสร็จสมบูรณ์ เฉพาะหลังจากที่มีการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="c0cef-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="c0cef-106">สำหรับข้อมูลเกี่ยวกับวิธีเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ของคุณ ดูที่ [เตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce](provisioning-guide.md)</span><span class="sxs-lookup"><span data-stu-id="c0cef-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="c0cef-107">หลังจากที่สภาพแวดล้อมการประเมินของ Commerce ของคุณถูกเตรียมใช้งานตั้งแต่ต้นจนจบ ขั้นตอนการตั้งค่าคอนฟิกหลังการเตรียมใช้งานเพิ่มเติมต้องเสร็จสมบูรณ์ ก่อนที่คุณจะสามารถเริ่มต้นการประเมินสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="c0cef-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="c0cef-108">เพื่อดำเนินการขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องใช้ Microsoft Dynamics Lifecycle Services (LCS) และ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="c0cef-109">ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="c0cef-109">Before you start</span></span>

1. <span data-ttu-id="c0cef-110">ลงชื่อเข้าใช้ [พอร์ทัล LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="c0cef-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="c0cef-111">ไปที่โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-111">Go to your project.</span></span>
1. <span data-ttu-id="c0cef-112">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="c0cef-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c0cef-113">เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="c0cef-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="c0cef-114">ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **เข้าสู่ระบบสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="c0cef-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="c0cef-115">คุณจะถูกส่งไปยังศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="c0cef-116">ตรวจสอบให้มั่นใจว่านิติบุคคล **USRT** ถูกเลือกไว้แล้วในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="c0cef-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="c0cef-117">ในระหว่างกิจกรรมหลังการเตรียมใช้งานในศูนย์ควบคุม Commerce ตรวจสอบให้แน่ใจว่ามีการเลือกนิติบุคคล **USRT** เสมอ</span><span class="sxs-lookup"><span data-stu-id="c0cef-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="c0cef-118">ตั้งค่าคอนฟิกการขายหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="c0cef-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="c0cef-119">เชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-119">Associate a worker with your identity</span></span>

<span data-ttu-id="c0cef-120">เพื่อเชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณ ให้ทำตามขั้นตอนเหล่านี้ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="c0cef-121">ใช้เมนูบนด้านซ้าย ไปที่ **โมดูล \> Retail และ commerce \> พนักงาน \> ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="c0cef-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="c0cef-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดต่อไปนี้ **000713 - Andrew Collette**</span><span class="sxs-lookup"><span data-stu-id="c0cef-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="c0cef-123">บนบานหน้าต่างการดำเนินการ เลือก **Commerce**</span><span class="sxs-lookup"><span data-stu-id="c0cef-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="c0cef-124">เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="c0cef-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="c0cef-125">ในฟิลด์ **อีเมล** ทางขวาของ **ค้นหาโดยใช้อีเมล** ให้ป้อนที่อยู่อีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="c0cef-126">เลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="c0cef-126">Select **Search**.</span></span>
1. <span data-ttu-id="c0cef-127">เลือกเรกคอร์ดที่มีชื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="c0cef-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-128">Select **OK**.</span></span>
1. <span data-ttu-id="c0cef-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c0cef-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="c0cef-130">เรียกใช้ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="c0cef-130">Activate Cloud POS</span></span>

<span data-ttu-id="c0cef-131">ถ้าต้องการเปิดใช้งาน Cloud POS ให้ทำตามขั้นตอนเหล่านี้ใน LCS</span><span class="sxs-lookup"><span data-stu-id="c0cef-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="c0cef-132">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="c0cef-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c0cef-133">เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="c0cef-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="c0cef-134">ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **เข้าสู่ระบบการขายหน้าร้านระบบคลาวด์**</span><span class="sxs-lookup"><span data-stu-id="c0cef-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="c0cef-135">เลือก **ถัดไป** เพื่อเปิดกล่องโต้ตอบ **ก่อนที่คุณจะเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="c0cef-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="c0cef-136">ปล่อยฟิลด์ **URL ของเซิร์ฟเวอร์** ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="c0cef-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="c0cef-137">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c0cef-137">Select **Next**.</span></span>
1. <span data-ttu-id="c0cef-138">เข้าสู่ระบบโดยใช้บัญชี Microsoft Azure Active Directory (Azure AD) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="c0cef-139">ภายใต้ **ชื่อร้านค้า** เลือก **San Francisco** แล้วจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c0cef-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="c0cef-140">ภายใต้ **ลงทะเบียนและอุปกรณ์** เลือก **SANFRAN-1**</span><span class="sxs-lookup"><span data-stu-id="c0cef-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="c0cef-141">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="c0cef-141">Select **Activate**.</span></span> <span data-ttu-id="c0cef-142">คุณได้ออกจากระบบและนำไปยังหน้าลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="c0cef-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="c0cef-143">ขณะนี้คุณสามารถลงชื่อเข้าสู่ประสบการณ์ Cloud POS ได้โดยใช้รหัสผู้ปฏิบัติงาน **000713** และรหัสผ่าน **123**</span><span class="sxs-lookup"><span data-stu-id="c0cef-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="c0cef-144">ตั้งค่าไซต์ของคุณใน Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-144">Set up your site in Commerce</span></span>

<span data-ttu-id="c0cef-145">หากต้องการเริ่มตั้งค่าไซต์การประเมินใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c0cef-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c0cef-146">ลงชื่อเข้าใช้ตัวสร้างไซต์โดยใช้ URL ที่คุณจดบันทึกเวลาที่คุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [เริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))</span><span class="sxs-lookup"><span data-stu-id="c0cef-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="c0cef-147">เลือกไซต์ **Fabrikam** เพื่อเปิดกล่องโต้ตอบการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="c0cef-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="c0cef-148">เลือกโดเมนที่คุณป้อนเมื่อคุณเริ่มต้นอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="c0cef-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="c0cef-149">เลือก **ร้านค้าออนไลน์แบบขยายของ Fabrikam** เป็นช่องทางเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0cef-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="c0cef-150">(ตรวจสอบให้แน่ใจว่าคุณได้เลือกร้านค้าออนไลน์ **แบบขยาย**)</span><span class="sxs-lookup"><span data-stu-id="c0cef-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="c0cef-151">เลือก **en-us** เป็นภาษาเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="c0cef-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="c0cef-152">ปล่อยให้ค่าของฟิลด์ **พาธ** เป็นตามเดิม</span><span class="sxs-lookup"><span data-stu-id="c0cef-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="c0cef-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-153">Select **OK**.</span></span> <span data-ttu-id="c0cef-154">รายการของหน้าบนไซต์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c0cef-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="c0cef-155">เปิดใช้งานงานต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c0cef-155">Enable jobs</span></span>

<span data-ttu-id="c0cef-156">ในการเปิดใช้งานงานใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c0cef-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c0cef-157">ลงชื่อเข้าสู่สภาพแวดล้อม (HQ)</span><span class="sxs-lookup"><span data-stu-id="c0cef-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="c0cef-158">ใช้เมนูด้านซ้ายเพื่อไปที่ **Retail และ commerce \> การสอบถามและรายงาน \> ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="c0cef-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="c0cef-159">ขั้นตอนที่เหลือของขั้นตอนนี้ต้องเสร็จสมบูรณ์สำหรับแต่ละงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0cef-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="c0cef-160">ประมวลผลการแจ้งเตือนทางอีเมลของใบสั่งของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="c0cef-160">Process retail order email notification</span></span>
    * <span data-ttu-id="c0cef-161">ความพร้อมใช้งานของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0cef-161">Product availability</span></span>
    * <span data-ttu-id="c0cef-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="c0cef-162">P-0001</span></span>
    * <span data-ttu-id="c0cef-163">ซิงโครไนส์งานใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="c0cef-163">Synchronize orders job</span></span>

1. <span data-ttu-id="c0cef-164">ใช้ตัวกรองด่วนเพื่อค้นหางานโดยใช้ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c0cef-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="c0cef-165">ถ้าสถานะของงานคือ **กำลังดำเนินการ** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c0cef-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="c0cef-166">เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c0cef-166">Select the record.</span></span>
    1. <span data-ttu-id="c0cef-167">ในบานหน้าต่างการดำเนินการ บนแท็บ **ชุดงาน** เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="c0cef-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="c0cef-168">เลือก **การยกเลิก** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="c0cef-169">อีกทางหนึ่งคือ คุณยังสามารถตั้งค่าช่วงการเกิดซ้ำเป็นหนึ่ง (1) นาทีสำหรับงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0cef-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="c0cef-170">ประมวลผลงานการแจ้งเตือนทางอีเมลของใบสั่งการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="c0cef-170">Process retail order email notification job</span></span>
* <span data-ttu-id="c0cef-171">งาน P-0001</span><span class="sxs-lookup"><span data-stu-id="c0cef-171">P-0001 job</span></span>
* <span data-ttu-id="c0cef-172">ซิงโครไนส์งานใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="c0cef-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="c0cef-173">รันการซิงโครไนส์ข้อมูลแบบสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c0cef-173">Run full data synchronization</span></span>

<span data-ttu-id="c0cef-174">หากต้องการรันการซิงโครไนส์ข้อมูลแบบสมบูรณ์ใน Commerce ให้ทำตามขั้นตอนเหล่านี้ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="c0cef-175">ใช้เมนูด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและคอมเมิร์ซ \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดการของคอมเมิร์ซ \> ฐานข้อมูลช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="c0cef-176">เลือกช่องทางที่ชื่อ **scXXXXXXXXX**</span><span class="sxs-lookup"><span data-stu-id="c0cef-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="c0cef-177">ในบานหน้าต่างการดำเนินการ เลือก **การซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="c0cef-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="c0cef-178">ป้อนค่า **9999** ที่กำหนดการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c0cef-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="c0cef-179">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-179">Select **OK**.</span></span>
1. <span data-ttu-id="c0cef-180">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0cef-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="c0cef-181">ทดสอบข้อมูลบัตรเครดิตเพื่อทำการทดสอบการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c0cef-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="c0cef-182">เมื่อต้องการทำการทดสอบธุรกรรมบนไซต์ คุณสามารถใช้ข้อมูลบัตรเครดิตทดสอบดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0cef-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="c0cef-183">**หมายเลขบัตร:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="c0cef-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="c0cef-184">**วันหมดอายุ:** 10/20</span><span class="sxs-lookup"><span data-stu-id="c0cef-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="c0cef-185">**รหัสค่าการตรวจสอบความถูกต้องของบัตร (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="c0cef-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0cef-186">ห้ามลองใช้ข้อมูลบัตรเครดิตจริงในไซต์ทดสอบไม่ว่าในสถานการณ์ใดๆ ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="c0cef-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c0cef-187">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c0cef-187">Next steps</span></span>

<span data-ttu-id="c0cef-188">หลังจากขั้นตอนการเตรียมใช้งานและการตั้งค่าคอนฟิกเสร็จสมบูรณ์แล้ว คุณสามารถเริ่มใช้สภาพแวดล้อมการประเมินของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0cef-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="c0cef-189">ใช้ URL ของตัวสร้างไซต์ Commerce เพื่อไปยังประสบการณ์การสร้าง</span><span class="sxs-lookup"><span data-stu-id="c0cef-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="c0cef-190">ใช้ URL ของไซต์ Commerce เพื่อไปยังประสบการณ์ไซต์ของลูกค้าขายปลีก</span><span class="sxs-lookup"><span data-stu-id="c0cef-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="c0cef-191">หากต้องการตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการประเมินของ Commerce ของคุณ ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการประเมินของ Commerce](cpe-optional-features.md)</span><span class="sxs-lookup"><span data-stu-id="c0cef-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0cef-192">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c0cef-192">Additional resources</span></span>

[<span data-ttu-id="c0cef-193">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="c0cef-194">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="c0cef-195">ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="c0cef-196">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="c0cef-197">FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="c0cef-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c0cef-198">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="c0cef-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="c0cef-199">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="c0cef-200">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="c0cef-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="c0cef-201">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0cef-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]