---
title: การจัดกลุ่มเท็มเพลตเวฟ
description: การจัดกลุ่มเท็มเพลตเวฟช่วยให้ระบบสามารถใช้การตั้งค่าเท็มเพลตเวฟเพื่อกำหนด โดยยึดตามเงื่อนไขที่คุณกำหนด วิธีการที่ควรแบ่งรายการที่นำออกใช้และกำหนดให้กับเวฟใหม่หรือเวฟที่มีอยู่ คุณลักษณะนี้อาจเป็นประโยชน์ในคลังสินค้าที่มีการสร้างเวฟตามเงื่อนไขที่ระบุ แต่ผู้จัดการต้องการสร้างเวฟโดยอัตโนมัติ แทนที่จะเป็นแบบด้วยตนเอง
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dd188cbd17cfed372283ecb3389633b0c0021eb
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530477"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="f510a-104">การจัดกลุ่มเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f510a-105">การจัดกลุ่มเท็มเพลตเวฟช่วยให้ระบบสามารถใช้การตั้งค่า [เท็มเพลตเวฟ](tasks/configure-wave-processing.md) เพื่อกำหนด โดยยึดตามเงื่อนไขที่คุณกำหนด วิธีการที่ควรแบ่งรายการที่นำออกใช้และกำหนดให้กับเวฟใหม่หรือเวฟที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f510a-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="f510a-106">คุณลักษณะนี้อาจเป็นประโยชน์ในคลังสินค้าที่มีการสร้างเวฟตามเงื่อนไขที่ระบุ แต่ผู้จัดการต้องการสร้างเวฟโดยอัตโนมัติ แทนที่จะเป็นแบบด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f510a-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="f510a-107">ซึ่งจะช่วยให้ระบบสามารถเพิ่มการจัดส่งที่นำออกใช้ใหม่แต่ละครั้งไปยังเวฟแรกที่พบว่ามีค่าฟิลด์การจัดกลุ่มที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f510a-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="f510a-108">ถ้าไม่พบรายการที่ตรงกัน ระบบจะสร้างเวฟใหม่สำหรับการจัดส่งใหม่</span><span class="sxs-lookup"><span data-stu-id="f510a-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f510a-109">ไม่สนับสนุนการจัดกลุ่มเท็มเพลตเวฟสำหรับชนิดงาน *การเบิกวัตถุดิบในการผลิต* หรือ *การเบิกสินค้าคัมบัง*</span><span class="sxs-lookup"><span data-stu-id="f510a-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="f510a-110">ทั้งนี้เนื่องจากการจัดกลุ่มเวฟจะขึ้นอยู่กับการจัดส่ง และชนิดงานเหล่านี้ไม่ได้ใช้การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f510a-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="f510a-111">เปิดคุณลักษณะการจัดกลุ่มเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="f510a-112">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การจัดกลุ่มเท็มเพลตเวฟ* ต้องมีการเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="f510a-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f510a-113">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f510a-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f510a-114">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f510a-115">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f510a-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f510a-116">**ชื่อคุณลักษณะ:** *การจัดกลุ่มเท็มเพลตเวฟ*</span><span class="sxs-lookup"><span data-stu-id="f510a-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="f510a-117">ตั้งค่าเท็มเพลตเวฟเพื่อใช้การจัดกลุ่มเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="f510a-118">เมื่อต้องการทำให้การจัดกลุ่มเท็มเพลตเวฟพร้อมใช้งาน ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่า [เท็มเพลตเวฟ](tasks/configure-wave-processing.md) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f510a-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="f510a-119">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="f510a-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="f510a-120">ในบานหน้าต่างด้านซ้าย ให้เลือกเท็มเพลตเวฟเพื่อตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f510a-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="f510a-121">ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองในภายหลังในหัวข้อนี้โดยใช้ข้อมูลสาธิต ให้เลือกเท็มเพลต **62 ค่าเริ่มต้นของการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="f510a-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="f510a-122">ให้เลือก **แก้ไข** เพื่อเปลี่ยนหน้าไปในโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f510a-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="f510a-123">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f510a-124">**ทำให้การสร้างเวฟเป็นแบบอัตโนมัติ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="f510a-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="f510a-125">**กำหนดให้เปิดเวฟ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="f510a-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="f510a-126">**ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="f510a-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="f510a-127">ในบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f510a-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="f510a-128">ในกล่องโต้ตอบการสอบถาม บนแท็บ **การเรียงลำดับ** ให้รีวิวเงื่อนไขการเรียงลำดับ และตรวจสอบให้แน่ใจว่ามีกฎที่มีฟิลด์ที่คุณต้องการใช้ในการจัดกลุ่มเวฟของคุณ</span><span class="sxs-lookup"><span data-stu-id="f510a-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="f510a-129">ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองโดยใช้ข้อมูลสาธิต ให้เพิ่มแถวที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="f510a-130">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="f510a-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="f510a-131">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="f510a-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="f510a-132">**ฟิลด์:** *บริการขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="f510a-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="f510a-133">หลังจากที่คุณเลือกค่านี้ คุณอาจได้รับข้อความต่อไปนี้: "บริการผู้ขนส่งฟิลด์ไม่ใช่ฟิลด์ดัชนี</span><span class="sxs-lookup"><span data-stu-id="f510a-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="f510a-134">คุณต้องการเพิ่มการเรียงลำดับหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="f510a-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="f510a-135">เลือก **ใช่** เพื่อเพิ่มการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="f510a-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="f510a-136">**ทิศทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="f510a-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f510a-137">เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ และปิดกล่องโต้ตอบการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f510a-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="f510a-138">ในบานหน้าต่างการดำเนินการ ให้เลือก **การจัดกลุ่มเท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="f510a-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="f510a-139">บนหน้า **การจัดกลุ่มเท็มเพลตเวฟ** ให้เลือกกล่องกาเครื่องหมาย **จัดกลุ่มโดย** สำหรับแถวแต่ละแถวที่คุณต้องการใช้ในการจัดกลุ่มรายการใบสั่งของคุณเป็นเวฟตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="f510a-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="f510a-140">ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองโดยใช้ข้อมูลสาธิต ให้เลือกกล่องกาเครื่องหมาย **จัดกลุ่มโดย** สำหรับแถว *บริการขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="f510a-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="f510a-141">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f510a-141">Select **Save**.</span></span>
1. <span data-ttu-id="f510a-142">ปิดหน้า **การจัดกลุ่มเท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="f510a-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="f510a-143">เลือก **บันทึก** เพื่อบันทึกเท็มเพลตของคุณ</span><span class="sxs-lookup"><span data-stu-id="f510a-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="f510a-144">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="f510a-144">Scenario</span></span>

<span data-ttu-id="f510a-145">ส่วนนี้จะให้สคริปต์ที่คุณสามารถทำงานผ่านการเรียนรู้ว่าคุณลักษณะนี้คืออะไรและทำงานกับคุณลักษณะนี้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f510a-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="f510a-146">ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f510a-146">Make sample data available</span></span>

<span data-ttu-id="f510a-147">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f510a-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f510a-148">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f510a-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="f510a-149">นอกจากนี้ คุณยังสามารถใช้สถานการณ์จำลองนี้เป็นคำแนะนำสำหรับการใช้คุณลักษณะ เมื่อคุณทำงานในระบบการผลิต</span><span class="sxs-lookup"><span data-stu-id="f510a-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="f510a-150">อย่างไรก็ตาม ในกรณีดังกล่าว คุณต้องแทนที่ค่าของคุณเอง และคุณอาจขาดเรกคอร์ดที่จำเป็นบางชนิดที่ข้อมูลสาธิตมาตรฐานมีให้</span><span class="sxs-lookup"><span data-stu-id="f510a-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="f510a-151">สถานการณ์จำลอง: การจัดกลุ่มเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="f510a-152">สถานการณ์นี้แสดงวิธีการใช้การจัดกลุ่มเท็มเพลตเวฟเพื่อสร้างเวฟหลายรายการโดยอัตโนมัติ โดยยึดตามเงื่อนไขการจัดกลุ่มที่กำหนดไว้ในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="f510a-153">ในสถานการณ์สมมตินี้ เท็มเพลตเวฟถูกตั้งค่าในระบบเพื่อสร้างหนึ่งเวฟต่อหนึ่งบริการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f510a-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="f510a-154">ก่อนที่คุณจะเริ่มต้น ให้เตรียมเท็มเพลตเวฟตามที่อธิบายไว้ในส่วน [ตั้งค่าเท็มเพลตเวฟเพื่อใช้การจัดกลุ่มเท็มเพลตเวฟ](#set-up-template) ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f510a-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="f510a-155">ถ้าคุณจะทำงานกับข้อมูลสาธิตสำหรับสถานการณ์นี้ โปรดตรวจสอบให้แน่ใจว่าได้ใช้ค่าข้อมูลสาธิตที่แนะนำไว้ในกระบวนงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="f510a-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="f510a-156">การตั้งค่านี้จะจัดกลุ่มเวฟของคุณตามบริการขนส่งที่ตั้งค่าไว้สำหรับใบสั่งขายแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="f510a-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="f510a-157">สร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="f510a-157">Create sales order 1</span></span>

1. <span data-ttu-id="f510a-158">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f510a-159">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f510a-160">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f510a-161">บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-004*</span><span class="sxs-lookup"><span data-stu-id="f510a-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="f510a-162">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*</span><span class="sxs-lookup"><span data-stu-id="f510a-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="f510a-163">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="f510a-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="f510a-164">ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="f510a-165">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="f510a-166">สลับไปยังมุมมอง **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="f510a-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="f510a-167">บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="f510a-168">**ผู้ขนส่งสินค้า:** *สายการบิน*</span><span class="sxs-lookup"><span data-stu-id="f510a-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="f510a-169">**บริการขนส่ง:** *อากาศ*</span><span class="sxs-lookup"><span data-stu-id="f510a-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="f510a-170">สลับกลับไปยังมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="f510a-171">ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f510a-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="f510a-172">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f510a-173">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f510a-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f510a-174">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="f510a-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="f510a-175">เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="f510a-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f510a-176">บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f510a-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="f510a-177">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="f510a-178">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f510a-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f510a-179">คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="f510a-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="f510a-180">จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f510a-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="f510a-181">ดูเวฟที่สร้างขึ้นจากใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="f510a-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="f510a-182">ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="f510a-183">เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="f510a-184">เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="f510a-185">โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ**</span><span class="sxs-lookup"><span data-stu-id="f510a-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="f510a-186">สร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="f510a-186">Create sales order 2</span></span>

1. <span data-ttu-id="f510a-187">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f510a-188">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f510a-189">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f510a-190">บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-005*</span><span class="sxs-lookup"><span data-stu-id="f510a-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="f510a-191">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*</span><span class="sxs-lookup"><span data-stu-id="f510a-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="f510a-192">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="f510a-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="f510a-193">ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="f510a-194">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="f510a-195">สลับไปยังมุมมอง **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="f510a-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="f510a-196">บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="f510a-197">**ผู้ขนส่งสินค้า:** *Flower moving*</span><span class="sxs-lookup"><span data-stu-id="f510a-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="f510a-198">**บริการขนส่ง:** *Std*</span><span class="sxs-lookup"><span data-stu-id="f510a-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="f510a-199">สลับกลับไปยังมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="f510a-200">ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f510a-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="f510a-201">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f510a-202">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f510a-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f510a-203">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="f510a-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="f510a-204">เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="f510a-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f510a-205">บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f510a-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="f510a-206">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="f510a-207">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f510a-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f510a-208">คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="f510a-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="f510a-209">จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f510a-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="f510a-210">โปรดสังเกตว่ารหัสเวฟแตกต่างจากรหัสเวฟของใบสั่งขายแรก</span><span class="sxs-lookup"><span data-stu-id="f510a-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="f510a-211">ดูเวฟที่สร้างขึ้นจากใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="f510a-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="f510a-212">ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="f510a-213">เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขายที่สอง</span><span class="sxs-lookup"><span data-stu-id="f510a-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="f510a-214">เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="f510a-215">โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ**</span><span class="sxs-lookup"><span data-stu-id="f510a-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="f510a-216">เวฟใหม่ถูกสร้างขึ้นสำหรับการจัดส่งนี้ เนื่องจากมีการใช้บริการขนส่งอื่นที่แตกต่างจากใบสั่งขายแรก</span><span class="sxs-lookup"><span data-stu-id="f510a-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="f510a-217">สร้างใบสั่งขาย 3</span><span class="sxs-lookup"><span data-stu-id="f510a-217">Create sales order 3</span></span>

1. <span data-ttu-id="f510a-218">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f510a-219">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f510a-220">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f510a-221">บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-006*</span><span class="sxs-lookup"><span data-stu-id="f510a-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="f510a-222">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*</span><span class="sxs-lookup"><span data-stu-id="f510a-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="f510a-223">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="f510a-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="f510a-224">ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="f510a-225">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="f510a-226">สลับไปยังมุมมอง **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="f510a-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="f510a-227">บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="f510a-228">**ผู้ขนส่งสินค้า:** *สายการบิน*</span><span class="sxs-lookup"><span data-stu-id="f510a-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="f510a-229">**บริการขนส่ง:** *อากาศ*</span><span class="sxs-lookup"><span data-stu-id="f510a-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="f510a-230">สลับกลับไปยังมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f510a-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="f510a-231">ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f510a-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="f510a-232">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f510a-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f510a-233">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f510a-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f510a-234">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="f510a-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="f510a-235">เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="f510a-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f510a-236">บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f510a-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="f510a-237">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f510a-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="f510a-238">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f510a-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f510a-239">คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="f510a-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="f510a-240">จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f510a-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="f510a-241">การจัดส่งได้รับการกำหนดให้กับเวฟที่มีอยู่จากใบสั่งขายแรก</span><span class="sxs-lookup"><span data-stu-id="f510a-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="f510a-242">ดูเวฟสำหรับใบสั่งขาย 1 และ 3</span><span class="sxs-lookup"><span data-stu-id="f510a-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="f510a-243">ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f510a-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="f510a-244">เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขายที่สาม</span><span class="sxs-lookup"><span data-stu-id="f510a-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="f510a-245">เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ</span><span class="sxs-lookup"><span data-stu-id="f510a-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="f510a-246">โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ** พร้อมกับการจัดส่งสำหรับใบสั่งขายแรก</span><span class="sxs-lookup"><span data-stu-id="f510a-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
