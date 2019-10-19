---
title: เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER
description: ขั้นตอนในหัวข้อนี้จะอธิบายวิธีการที่ผู้ใช้ Regulatory configuration service (RCS) สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ โดยใช้ข้อมูลเมตาใน Finance and Operations
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bfe007995c894d6cc86d07ef2b52da65e32e950
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182749"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="c8de2-103">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="c8de2-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8de2-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ Regulatory configuration service (RCS) ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ โดยใช้ข้อมูลเมตาแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c8de2-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="c8de2-105">ข้อมูลเมตาของแอพลิเคชันจะสามารถเข้าถึงได้โดยใช้การตั้งค่าคอนฟิกข้อมูลเมตา ER ซึ่งประกอบด้วยชุดตัวอย่างของข้อมูลเมตาเพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="c8de2-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="c8de2-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ใน RCS อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในหัวข้อให้เสร็จสมบูรณ์ กระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="c8de2-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="c8de2-107">จากนั้น ให้ทำขั้นตอนต่างๆ ในหัวข้อให้เสร็จสมบูรณ์ [(ER) เตรียมข้อมูลเมตาของแอพลิเคชันที่จะใช้ใน RCS](prepare-application-metadata-rcs.md)</span><span class="sxs-lookup"><span data-stu-id="c8de2-107">Then complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8de2-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c8de2-108">Prerequisites</span></span>
1. <span data-ttu-id="c8de2-109">ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="c8de2-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="c8de2-110">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="c8de2-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="c8de2-111">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c8de2-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="c8de2-112">นำเข้าการตั้งค่าคอนฟิกข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="c8de2-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="c8de2-113">คลิก **การตั้งค่าคอนฟิกข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="c8de2-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="c8de2-114">นำเข้าการตั้งค่าคอนฟิกข้อมูลเมตา ER ซึ่งประกอบด้วยข้อมูลเมตาที่ได้รับการตั้งค่าคอนฟิกเพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="c8de2-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="c8de2-115">การตั้งค่าคอนฟิกข้อมูลเมตาของ ER นี้ได้ถูกส่งออกเป็นไฟล์ XML ในขณะที่ขั้นตอนในกระบวนงาน [(ER) เตรียมข้อมูลเมตาของแอพลิเคชันที่จะใช้ใน RCS](prepare-application-metadata-rcs.md) เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="c8de2-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="c8de2-116">คลิก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="c8de2-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="c8de2-117">คลิก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="c8de2-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="c8de2-118">คลิก **เรียกดู** และเลือกไฟล์ ‘Foreign trade metadata.xml’</span><span class="sxs-lookup"><span data-stu-id="c8de2-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="c8de2-119">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-119">Click **OK**.</span></span> 
7. <span data-ttu-id="c8de2-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="c8de2-121">สร้างการตั้งค่าคอนฟิกแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c8de2-121">Create data model configuration</span></span>
1. <span data-ttu-id="c8de2-122">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="c8de2-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="c8de2-123">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="c8de2-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'แบบจำลองการค้าต่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="c8de2-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="c8de2-125">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="c8de2-126">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="c8de2-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="c8de2-127">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="c8de2-128">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ราก'</span><span class="sxs-lookup"><span data-stu-id="c8de2-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="c8de2-129">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c8de2-129">Click **Add**.</span></span> 
9. <span data-ttu-id="c8de2-130">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="c8de2-131">ในฟิลด์ **ชื่อ** พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="c8de2-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="c8de2-132">ในฟิลด์ **ประเภทรายการ** ให้เลือก **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="c8de2-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="c8de2-133">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c8de2-133">Click **Add**.</span></span> 
13. <span data-ttu-id="c8de2-134">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="c8de2-135">ในฟิลด์ **ชื่อ** พิมพ์ 'รหัสโภคภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="c8de2-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="c8de2-136">ในฟิลด์ **ประเภทรายการ** ให้เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="c8de2-137">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c8de2-137">Click **Add**.</span></span> 
17. <span data-ttu-id="c8de2-138">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="c8de2-139">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'จำนวนเงินที่ออกใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="c8de2-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="c8de2-140">ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="c8de2-141">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c8de2-141">Click **Add**.</span></span> 
21. <span data-ttu-id="c8de2-142">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="c8de2-143">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="c8de2-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="c8de2-144">ในฟิลด์ **ประเภทรายการ** ให้เลือก **วันที่**</span><span class="sxs-lookup"><span data-stu-id="c8de2-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="c8de2-145">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c8de2-145">Click **Add**.</span></span> 
25. <span data-ttu-id="c8de2-146">คลิก **การอ้างอิงราก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="c8de2-147">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-147">Click **OK**.</span></span> 
27. <span data-ttu-id="c8de2-148">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-148">Click **Save**.</span></span> 
28. <span data-ttu-id="c8de2-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-149">Close the page.</span></span> 
29. <span data-ttu-id="c8de2-150">คลิก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="c8de2-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="c8de2-151">คลิก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="c8de2-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="c8de2-152">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="c8de2-153">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="c8de2-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="c8de2-154">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c8de2-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="c8de2-155">ในฟิลด์ **ใหม่** ป้อน 'การแม็ปแบบจำลองตามแบบจำลอง แบบจำลองการค้าต่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="c8de2-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="c8de2-156">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'การแม็ปการค้าต่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="c8de2-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="c8de2-157">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="c8de2-158">ขยายส่วน **ข้อกำหนดเบื้องต้น**</span><span class="sxs-lookup"><span data-stu-id="c8de2-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="c8de2-159">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c8de2-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="c8de2-160">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-160">Click **New**.</span></span> 
8. <span data-ttu-id="c8de2-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c8de2-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="c8de2-162">ในฟิลด์ **ชนิดส่วนประกอบสำหรับข้อกำหนดเบื้องต้น** ให้เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="c8de2-163">เลือกการตั้งค่าคอนฟิก **ข้อมูลเมตาการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="c8de2-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="c8de2-164">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-164">Click **Save**.</span></span> 
12. <span data-ttu-id="c8de2-165">เราได้เพิ่มการอ้างอิงถึงรุ่น 1 ของการตั้งค่าคอนฟิก ‘ข้อมูลเมตาการค้าต่างประเทศ’</span><span class="sxs-lookup"><span data-stu-id="c8de2-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="c8de2-166">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c8de2-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="c8de2-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-167">Close the page.</span></span> 
14. <span data-ttu-id="c8de2-168">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="c8de2-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="c8de2-169">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="c8de2-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="c8de2-170">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="c8de2-171">คลิก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="c8de2-172">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'อินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="c8de2-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="c8de2-173">เลือกเรกคอร์ดตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="c8de2-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="c8de2-174">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8de2-175">มีการเสนอตารางเพียง 2 ตารางเท่านั้น เนื่องจากมีการเพิ่มตารางเพียง 2 ตารางเข้าในชุดของข้อมูลเมตาที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c8de2-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="c8de2-176">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="c8de2-177">ในแผนภูมิ ให้ขยาย **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="c8de2-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="c8de2-178">ในแผนภูมิ เลือก **อินทราสแทต\AmountMST**</span><span class="sxs-lookup"><span data-stu-id="c8de2-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="c8de2-179">ในแผนภูมิ ให้ขยาย **ธุรกรรม = อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="c8de2-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="c8de2-180">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต\จำนวนเงินที่ออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="c8de2-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="c8de2-181">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="c8de2-182">ในแผนภูมิ เลือก **อินทราสแทต\TransDate**</span><span class="sxs-lookup"><span data-stu-id="c8de2-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="c8de2-183">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต\วันที่**</span><span class="sxs-lookup"><span data-stu-id="c8de2-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="c8de2-184">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="c8de2-185">ในแผนภูมิ ขยาย **อินทราสแทต\>ความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="c8de2-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="c8de2-186">ในแผนภูมิ ขยาย **อินทราสแทต\>ความสัมพันธ์\IntrastatCommodity**</span><span class="sxs-lookup"><span data-stu-id="c8de2-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="c8de2-187">ในแผนภูมิ เลือก **อินทราสแทต\>ความสัมพันธ์\IntrastatCommodity\รหัส**</span><span class="sxs-lookup"><span data-stu-id="c8de2-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="c8de2-188">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต\รหัสโภคภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c8de2-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="c8de2-189">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="c8de2-190">คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="c8de2-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8de2-191">เราประสบความสำเร็จในการผูกองค์ประกอบของแบบจำลองข้อมูลที่มีรายการของแหล่งข้อมูลที่อธิบายโดยใช้รายละเอียดของข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกข้อมูลเมตาของ ER ที่อ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c8de2-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="c8de2-192">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c8de2-192">Click **Save**.</span></span> 
37. <span data-ttu-id="c8de2-193">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-193">Close the page.</span></span> 
38. <span data-ttu-id="c8de2-194">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-194">Close the page.</span></span> 
39. <span data-ttu-id="c8de2-195">เมื่อจำเป็น คุณสามารถขยายชุดของข้อมูลเมตาที่มีอยู่ แล้วส่งออกการตั้งค่าคอนฟิกข้อมูลเมตา ER รุ่นใหม่ที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="c8de2-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="c8de2-196">คุณสามารถนำเข้าไปยัง RCS และอัพเดตข้อกำหนดเบื้องต้นของการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตาเวอร์ชันใหม่ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="c8de2-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8de2-197">วิธีในการรับข้อมูลเกี่ยวกับข้อมูลเมตาของแอพลิเคชันวิธีนี้ เป็นเพียงวิธีเดียวที่มีให้ใช้งานสำหรับแอพลิเคชันที่ปรับใช้เฉพาะที่ (เมื่อมีการใช้งานข้อมูลธุรกิจแบบภายในเครื่อง (LBD), แบบในสถานที่ หรือแบบการปรับใช้ที่เป็นแบบโมเดล)</span><span class="sxs-lookup"><span data-stu-id="c8de2-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
