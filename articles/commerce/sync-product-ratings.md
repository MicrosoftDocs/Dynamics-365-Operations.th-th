---
title: ซิงค์การให้คะแนนผลิตภัณฑ์ใน Dynamics 365 Commerce
description: หัวข้อนี้จะอธิบายวิธีการซิงค์การจัดอันดับผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006296"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="c8c80-103">ซิงค์การให้คะแนนผลิตภัณฑ์ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8c80-104">หัวข้อนี้จะอธิบายวิธีการซิงค์การจัดอันดับผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8c80-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c8c80-105">Overview</span></span>

<span data-ttu-id="c8c80-106">เมื่อต้องการใช้การจัดอันดับผลิตภัณฑ์ในช่องทาง Omni เช่น ในการขายหน้าร้าน (POS) และในศูนย์บริการ ต้องนำเข้าการจัดอันดับผลิตภัณฑ์จากบริการจัดอันดับและการตรวจทานในฐานข้อมูลช่องทาง Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="c8c80-107">เมื่อการจัดอันดับผลิตภัณฑ์มีอยู่ในช่องทาง Omni ผู้ใช้จะสามารถช่วยเหลือลูกค้าทางอ้อมระหว่างการโต้ตอบกับสมาคมการขายได้</span><span class="sxs-lookup"><span data-stu-id="c8c80-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="c8c80-108">หัวข้อนี้อธิบายงานเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c8c80-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="c8c80-109">ตั้งค่าคอนฟิก **งานการซิงค์การจัดอันดับผลิตภัณฑ์** เป็นชุดงานเพื่อซิงโครไนส์การจัดอันดับผลิตภัณฑ์จาก **บริการจัดอันดับและการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="c8c80-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="c8c80-110">ตรวจสอบว่าชุดงานสำหรับการซิงโครไนส์การจัดอันดับผลิตภัณฑ์สำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c8c80-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="c8c80-111">ทำให้การจัดอันดับผลิตภัณฑ์พร้อมใช้งานที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="c8c80-112">ตั้งค่าคอนฟิกชุดงานเพื่อซิงโครไนส์การจัดอันดับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8c80-113">ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่ามีการติดตั้งรุ่น 10.0.6 หรือรุ่นที่ใหม่กว่าของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="c8c80-114">เริ่มต้นตัวกำหนดตารางทำงานการค้า</span><span class="sxs-lookup"><span data-stu-id="c8c80-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="c8c80-115">เพื่อเริ่มต้นตัวกำหนดตารางทำงานการค้า ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c8c80-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="c8c80-116">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการค้า \> เริ่มต้นตัวจัดกำหนดการการค้า**</span><span class="sxs-lookup"><span data-stu-id="c8c80-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="c8c80-117">หรือให้ค้นหา "เริ่มต้นตัวกำหนดตารางทำงานการค้า"</span><span class="sxs-lookup"><span data-stu-id="c8c80-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="c8c80-118">ในกล่องโต้ตอบ **เริ่มต้นตัวกำหนดตารางทำงานการค้า** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **ลบการตั้งค่าคอนฟิกที่มีอยู่** เป็น **ไม่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8c80-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="c8c80-119">ตรวจสอบความถูกต้องของ RetailProductRating ย่อย</span><span class="sxs-lookup"><span data-stu-id="c8c80-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="c8c80-120">เมื่อต้องการตรวจสอบว่ามี **RetailProductRating** ย่อยอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c8c80-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="c8c80-121">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการค้า \> งานย่อยของตัวกำหนดตารางทำงาน**</span><span class="sxs-lookup"><span data-stu-id="c8c80-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="c8c80-122">อีกทางหนึ่งคือค้นหา "งานย่อยของตัวกำหนดตารางทำงาน"</span><span class="sxs-lookup"><span data-stu-id="c8c80-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="c8c80-123">ในรายการย่อยให้ค้นหาหรือค้นหา **RetailProductRating** ย่อย</span><span class="sxs-lookup"><span data-stu-id="c8c80-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="c8c80-124">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายละเอียดของงานย่อยใน Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![รายละเอียดของ RetailProductRating ย่อย](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="c8c80-126">ถ้าคุณไม่พบงานย่อย **RetailProductRating** คุณอาจเรียกใช้งาน **ซิงค์การจัดอันดับผลิตภัณฑ์** และงาน **1040 CDX** ไปแล้ว ก่อนที่คุณจะเริ่มต้นตัวกำหนดตารางทำงาน Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="c8c80-127">ในกรณีนี้ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพื่อเรียกใช้งาน **งานการซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="c8c80-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="c8c80-128">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการค้า \> ฐานข้อมูลช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="c8c80-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="c8c80-129">อีกทางหนึ่งคือค้นหา "ฐานข้อมูลช่องทาง"</span><span class="sxs-lookup"><span data-stu-id="c8c80-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="c8c80-130">เลือกช่องสัญญาณ เพื่อซิงค์</span><span class="sxs-lookup"><span data-stu-id="c8c80-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="c8c80-131">ในบานหน้าต่างการดำเนินการ เลือก **การซิงค์ข้อมูลแบบสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="c8c80-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="c8c80-132">ในกล่องโต้ตอบแบบหล่นลง **กำหนดการกระจาย** เลือก **1040-ผลิตภัณฑ์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8c80-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="c8c80-133">ทำซ้ำขั้นตอนของกระบวนการก่อนหน้านี้เพื่อตรวจสอบว่ามีการสร้าง **RetailProductRating** ย่อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="c8c80-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="c8c80-134">นำเข้าการให้คะแนนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-134">Import product ratings</span></span>

<span data-ttu-id="c8c80-135">เมื่อต้องการนำเข้าการจัดอันดับผลิตภัณฑ์ไปยัง Commerce จากบริการการจัดอันดับและการตรวจทาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c8c80-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="c8c80-136">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานกาค้า \> ซิงค์งานการจัดอันดับผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c8c80-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="c8c80-137">หรือให้ค้นหา "ซิงค์งานการจัดอันดับผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="c8c80-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="c8c80-138">ในกล่องโต้ตอบการ **ดึงการจัดอันดับผลิตภัณฑ์** บนแท็บด่วน **การรันในพื้นหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="c8c80-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="c8c80-139">ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ให้ตั้งค่ารูปแบบการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c8c80-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="c8c80-140">(ค่าที่แนะนำคือสองชั่วโมง) อย่าจัดกำหนดการการเกิดซ้ำที่น้อยกว่าหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c8c80-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="c8c80-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8c80-141">Select **OK**.</span></span>
1. <span data-ttu-id="c8c80-142">ตั้งค่าตัวเลือก **ประมวลผลชุดงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c8c80-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="c8c80-143">การตั้งค่านี้จะช่วยรับประกันว่าคุณจะสามารถตรวจสอบล็อกและตรวจสอบสถานะของชุดงานที่รัน</span><span class="sxs-lookup"><span data-stu-id="c8c80-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="c8c80-144">เลือก **ตกลง** เพื่อตั้งกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c8c80-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="c8c80-145">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกชุดงานใน Commerce</span><span class="sxs-lookup"><span data-stu-id="c8c80-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![การตั้งค่าคอนฟิกของชุดงานการจัดอันดับผลิตภัณฑ์ที่มีการซิงค์](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="c8c80-147">ตรวจสอบว่าชุดงานสำหรับการซิงโครไนส์การจัดอันดับผลิตภัณฑ์สำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c8c80-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="c8c80-148">เมื่อต้องการตรวจสอบว่าชุดงาน **ซิงค์การให้คะแนนผลิตภัณฑ์** สำเร็จ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c8c80-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="c8c80-149">ไปที่ **Retail และ Commerce \> ผู้ดูแลระบบ \> การสอบถาม \> ชุดงาน** หรือถ้าคุณกำลังใช้หน่วยการเก็บสต็อกสินค้าเฉพาะ Commerce (SKU) **Retail และ Commerce \> การสอบถามและรายงาน \> ชุดงาน** แทน</span><span class="sxs-lookup"><span data-stu-id="c8c80-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="c8c80-150">อีกทางหนึ่งคือค้นหา "ชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="c8c80-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="c8c80-151">เมื่อต้องการดูรายละเอียดของชุดงานในรายการชุดงานในคอลัมน์ **คำอธิบายงาน** ให้ค้นหาคำอธิบายที่มี "ดึงการจัดอันดับผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="c8c80-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="c8c80-152">เลือกรหัสงานเพื่อดูรายละเอียดชุดงาน เช่น วันที่/เวลาเริ่มต้น ตามกำหนดการและข้อความการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c8c80-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="c8c80-153">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายละเอียดชุดงานใน Commerce เมื่อมีการจัดกำหนดการชุดงานให้รันในช่วงสองชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c8c80-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![รายละเอียดของชุดงานการจัดอันดับผลิตภัณฑ์ที่มีการซิงค์](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="c8c80-155">ทำให้การจัดอันดับผลิตภัณฑ์พร้อมใช้งานที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="c8c80-156">การจัดอันดับและการตรวจทานโซลูชันใน Dynamics 365 Commerce เป็นโซลูชันช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="c8c80-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="c8c80-157">อย่างไรก็ตาม ตามค่าเริ่มต้น การจัดอันดับผลิตภัณฑ์จะไม่แสดงที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="c8c80-158">เพื่อช่วยให้ลูกค้าในร้านค้าดูการจัดอันดับและการรีวิว เมื่อพวกเขากำลังได้รับการช่วยเหลือโดยสมาคมการขาย คุณต้องเปิดการจัดอันดับผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="c8c80-159">เมื่อต้องการเปิดใช้งานการจัดอันดับผลิตภัณฑ์ที่ POS ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c8c80-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="c8c80-160">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce**</span><span class="sxs-lookup"><span data-stu-id="c8c80-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="c8c80-161">อีกทางหนึ่งคือ ค้นหา "พารามิเตอร์ Commerce"</span><span class="sxs-lookup"><span data-stu-id="c8c80-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="c8c80-162">บนแท็บ **พารามิเตอร์การตั้งค่าคอนฟิก** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c8c80-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="c8c80-163">ป้อนชื่อเช่น **RatingsAndReviews.EnableProductRatingsForRetailStores** และตั้งค่าเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="c8c80-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="c8c80-164">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c8c80-164">Select **Save**.</span></span>
1. <span data-ttu-id="c8c80-165">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="c8c80-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="c8c80-166">อีกทางหนึ่งคือค้นหา "กำหนดการกระจาย"</span><span class="sxs-lookup"><span data-stu-id="c8c80-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="c8c80-167">ในรายการงานให้เลือก **1110** (**การตั้งค่าคอนฟิกส่วนกลาง**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="c8c80-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="c8c80-168">หลังจากที่ทำงานเสร็จเรียบร้อย แล้วให้ตรวจสอบว่าการจัดอันดับผลิตภัณฑ์แสดงอยู่ในขณะนี้ที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="c8c80-169">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกของพารามิเตอร์ Commerce เพื่อเปิดใช้งานการจัดอันดับผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![การตั้งค่าคอนฟิกของพารามิเตอร์ Commercel สำหรับการจัดอันดับผลิตภัณฑ์ที่ POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="c8c80-171">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการให้คะแนนผลิตภัณฑ์ที่ POS</span><span class="sxs-lookup"><span data-stu-id="c8c80-171">The following illustration shows an example of product ratings at the POS.</span></span>

![การให้คะแนนผลิตภัณฑ์ที่ POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="c8c80-173">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการให้คะแนนผลิตภัณฑ์ ในช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="c8c80-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![การให้คะแนนผลิตภัณฑ์ในช่องทางของศูนย์บริการ](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="c8c80-175">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c8c80-175">Additional resources</span></span>

[<span data-ttu-id="c8c80-176">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c8c80-177">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c8c80-178">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c8c80-179">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="c8c80-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
