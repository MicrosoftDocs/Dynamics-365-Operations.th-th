---
title: ซิงค์การให้คะแนนผลิตภัณฑ์ใน Dynamics 365 Retail
description: หัวข้อนี้จะอธิบายวิธีการซิงค์การจัดอันดับผลิตภัณฑ์ใน Microsoft Dynamics 365 Retail
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698176"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="cd3c2-103">ซิงค์การให้คะแนนผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cd3c2-104">หัวข้อนี้จะอธิบายวิธีการซิงค์การจัดอันดับผลิตภัณฑ์ใน Microsoft Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="cd3c2-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="cd3c2-105">Overview</span></span>

<span data-ttu-id="cd3c2-106">เมื่อต้องการใช้การจัดอันดับผลิตภัณฑ์ในช่องทาง Omni เช่น ในการขายหน้าร้าน (POS) และในศูนย์การผลิตการจัดอันดับผลิตภัณฑ์จากการจัดอันดับและการตรวจสอบความถูกต้อง ต้องนำเข้าในฐานข้อมูลช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cd3c2-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="cd3c2-107">เมื่อการจัดอันดับผลิตภัณฑ์มีอยู่ในช่องทาง Omni ผู้ใช้จะสามารถช่วยเหลือลูกค้าทางอ้อมระหว่างการโต้ตอบกับสมาคมการขายได้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="cd3c2-108">หัวข้อนี้อธิบายงานเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cd3c2-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="cd3c2-109">ตั้งค่าคอนฟิกชุดงาน Retail เพื่อนำเข้าการจัดอันดับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="cd3c2-110">ตรวจสอบว่าชุดงานสำหรับการซิงโครไนส์การจัดอันดับผลิตภัณฑ์สำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cd3c2-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="cd3c2-111">ทำให้การจัดอันดับผลิตภัณฑ์พร้อมใช้งานที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="cd3c2-112">ตั้งค่าคอนฟิกชุดงาน Retail เพื่อนำเข้าการจัดอันดับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd3c2-113">ก่อนที่คุณจะเริ่มต้นโปรดตรวจสอบให้แน่ใจว่าได้ติดตั้งเวอร์ชัน 10.0.6 หรือใหม่กว่าของ Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="cd3c2-114">เริ่มต้นตัวกำหนดตารางทำงาน Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="cd3c2-115">เพื่อเริ่มการตั้งค่าตัวกำหนดตารางงานการขายปลีก ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="cd3c2-116">ไปที่ **Retail \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการขายปลีก \> เริ่มต้นตัวกำหนดตารางทำงานการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="cd3c2-117">หรือให้ค้นหา "เริ่มต้นตัวกำหนดตารางทำงาน Retail"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="cd3c2-118">ในกล่องโต้ตอบ **เริ่มต้นตัวกำหนดตารางทำงาน Retail** ตรวจสอบให้แน่ใจว่าได้ตั้งค่า **ลบการตั้งค่าคอนฟิกที่มีอยู่** เป็น **ไม่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="cd3c2-119">ตรวจสอบความถูกต้องของ RetailProductRating ย่อย</span><span class="sxs-lookup"><span data-stu-id="cd3c2-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="cd3c2-120">เมื่อต้องการตรวจสอบว่ามี **RetailProductRating** ย่อยอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="cd3c2-121">ไปที่ **Retail \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการขายปลีก \> งานย่อยของตัวกำหนดตารางทำงาน**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="cd3c2-122">อีกทางหนึ่งคือค้นหา "งานย่อยของตัวกำหนดตารางทำงาน"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="cd3c2-123">ในรายการย่อยให้ค้นหาหรือค้นหา **RetailProductRating** ย่อย</span><span class="sxs-lookup"><span data-stu-id="cd3c2-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="cd3c2-124">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า รายละเอียดของงานย่อยใน Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![รายละเอียดของ RetailProductRating ย่อย](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="cd3c2-126">ถ้าคุณไม่พบ **RetailProductRating** ย่อย คุณอาจเรียกใช้งาน **ซิงค์การจัดอันดับผลิตภัณฑ์** และงาน **1040 CDX** ไปแล้วก่อนที่คุณจะเริ่มต้นตัวกำหนดตารางทำงาน Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="cd3c2-127">ในกรณีนี้ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพื่อเรียกใช้งาน **งานการซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="cd3c2-128">ไปที่ **Retail \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการขายปลีก \> ฐานข้อมูลช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="cd3c2-129">อีกทางหนึ่งคือค้นหา "ฐานข้อมูลช่องทาง"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="cd3c2-130">เลือกช่องสัญญาณ เพื่อซิงค์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="cd3c2-131">ในบานหน้าต่างการดำเนินการ เลือก **การซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="cd3c2-132">ในกล่องโต้ตอบแบบหล่นลง **กำหนดการกระจาย** เลือก **1040-ผลิตภัณฑ์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="cd3c2-133">ทำซ้ำขั้นตอนของกระบวนการก่อนหน้านี้เพื่อตรวจสอบว่ามีการสร้าง **RetailProductRating** ย่อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="cd3c2-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="cd3c2-134">นำเข้าการให้คะแนนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-134">Import product ratings</span></span>

<span data-ttu-id="cd3c2-135">เมื่อต้องการนำเข้าการจัดอันดับผลิตภัณฑ์ไปยัง Retail จากบริการการจัดอันดับและการตรวจทาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="cd3c2-136">ไปที่ **Retail \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการขายปลีก \> ซิงค์งานการจัดอันดับผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="cd3c2-137">หรือให้ค้นหา "ซิงค์งานการจัดอันดับผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="cd3c2-138">ในกล่องโต้ตอบการ **ดึงการจัดอันดับผลิตภัณฑ์** บนแท็บด่วน **การรันในพื้นหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="cd3c2-139">ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ให้ตั้งค่ารูปแบบการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="cd3c2-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="cd3c2-140">(ค่าที่แนะนำคือสองชั่วโมง) อย่าจัดกำหนดการการเกิดซ้ำที่น้อยกว่าหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="cd3c2-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="cd3c2-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-141">Select **OK**.</span></span>
1. <span data-ttu-id="cd3c2-142">ตั้งค่าตัวเลือก **ประมวลผลชุดงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="cd3c2-143">การตั้งค่านี้จะช่วยรับประกันว่าคุณจะสามารถตรวจสอบล็อกและตรวจสอบสถานะของชุดงานที่รัน</span><span class="sxs-lookup"><span data-stu-id="cd3c2-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="cd3c2-144">เลือก **ตกลง** เพื่อตั้งกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cd3c2-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="cd3c2-145">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า การตั้งค่าคอนฟิกของลำดับงาน Retail</span><span class="sxs-lookup"><span data-stu-id="cd3c2-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![การตั้งค่าคอนฟิกของชุดงานการจัดอันดับผลิตภัณฑ์ที่มีการซิงค์](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="cd3c2-147">ตรวจสอบว่าชุดงานสำหรับการซิงโครไนส์การจัดอันดับผลิตภัณฑ์สำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cd3c2-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="cd3c2-148">เมื่อต้องการตรวจสอบว่าชุดงาน **ซิงค์การให้คะแนนผลิตภัณฑ์** สำเร็จ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="cd3c2-149">ไปที่ **Retail \> ผู้ดูแลระบบ \> การสอบถาม \> ชุดงาน** หรือถ้าคุณกำลังใช้หน่วยการเก็บสินค้าคงคลังที่มีการจัดเก็บสินค้าคงคลังเท่านั้น (SKU) **Retail \> การสอบถามและรายงาน \> ชุดงาน** แทน</span><span class="sxs-lookup"><span data-stu-id="cd3c2-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="cd3c2-150">อีกทางหนึ่งคือค้นหา "ชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="cd3c2-151">เมื่อต้องการดูรายละเอียดของชุดงานในรายการชุดงานในคอลัมน์ **คำอธิบายงาน** ให้ค้นหาคำอธิบายที่มี "ดึงการจัดอันดับผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="cd3c2-152">เลือกรหัสงานเพื่อดูรายละเอียดชุดงาน เช่น วันที่/เวลาเริ่มต้น ตามกำหนดการและข้อความการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="cd3c2-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="cd3c2-153">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายละเอียดชุดงานใน Retail เมื่อมีการจัดกำหนดการชุดงานให้รันในช่วงสองชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="cd3c2-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![รายละเอียดของชุดงานการจัดอันดับผลิตภัณฑ์ที่มีการซิงค์](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="cd3c2-155">ทำให้การจัดอันดับผลิตภัณฑ์พร้อมใช้งานที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="cd3c2-156">การจัดอันดับและการตรวจทานโซลูชันใน Dynamics 365 Commerce เป็นโซลูชันช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="cd3c2-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="cd3c2-157">อย่างไรก็ตาม ตามค่าเริ่มต้น การจัดอันดับผลิตภัณฑ์จะไม่แสดงที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="cd3c2-158">เพื่อช่วยให้ลูกค้าในร้านค้าดูการจัดอันดับและการรีวิว เมื่อพวกเขากำลังได้รับการช่วยเหลือโดยสมาคมการขาย คุณต้องเปิดการจัดอันดับผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="cd3c2-159">เมื่อต้องการเปิดใช้งานการจัดอันดับผลิตภัณฑ์ที่ POS ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cd3c2-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="cd3c2-160">ไปที่ **การขายปลีก \> การตั้งค่า Retail \> พารามิเตอร์ \> พารามิเตอร์การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="cd3c2-161">อีกทางหนึ่งคือค้นหา "พารามิเตอร์ Retail"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="cd3c2-162">บนแท็บ **พารามิเตอร์การตั้งค่าคอนฟิก** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="cd3c2-163">ป้อนชื่อเช่น **RatingsAndReviews.EnableProductRatingsForRetailStores** และตั้งค่าเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="cd3c2-164">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-164">Select **Save**.</span></span>
1. <span data-ttu-id="cd3c2-165">ไปที่ **การขายปลีก \> ฝ่ายไอทีระบบขายปลีก \> กำหนดการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="cd3c2-166">อีกทางหนึ่งคือค้นหา "กำหนดการกระจาย"</span><span class="sxs-lookup"><span data-stu-id="cd3c2-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="cd3c2-167">ในรายการงานให้เลือก **1110** (**การตั้งค่าคอนฟิกส่วนกลาง**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="cd3c2-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="cd3c2-168">หลังจากที่ทำงานเสร็จเรียบร้อย แล้วให้ตรวจสอบว่าการจัดอันดับผลิตภัณฑ์แสดงอยู่ในขณะนี้ที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="cd3c2-169">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกของพารามิเตอร์ Retail เพื่อเปิดใช้งานการจัดอันดับผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![การตั้งค่าคอนฟิกของพารามิเตอร์ Retail สำหรับการจัดอันดับผลิตภัณฑ์ที่ POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="cd3c2-171">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการให้คะแนนผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="cd3c2-171">The following illustration shows an example of product ratings at the POS.</span></span>

![การให้คะแนนผลิตภัณฑ์ที่ POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="cd3c2-173">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการให้คะแนนผลิตภัณฑ์ ในช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cd3c2-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![การให้คะแนนผลิตภัณฑ์ในช่องทางของศูนย์บริการ](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="cd3c2-175">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cd3c2-175">Additional resources</span></span>

[<span data-ttu-id="cd3c2-176">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="cd3c2-177">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="cd3c2-178">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="cd3c2-179">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="cd3c2-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
