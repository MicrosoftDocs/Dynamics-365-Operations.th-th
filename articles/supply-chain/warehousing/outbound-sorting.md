---
title: การเรียงลำดับขาออก
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการเรียงลำดับขาออก ฟังก์ชันนี้ทำให้สามารถจัดการคอนเทนเนอร์ขนาดเล็กได้ง่ายขึ้น และช่วยให้ผู้ปฏิบัติงานในคลังสินค้าวางแผนและจัดระเบียบกำลังการผลิตของแท่นวางสินค้าในรถบรรทุกได้ดีขึ้น
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963421"
---
# <a name="outbound-sorting"></a><span data-ttu-id="0a108-104">การเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="0a108-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a108-105">ฟังก์ชันนี้ทำให้สามารถจัดการคอนเทนเนอร์ขนาดเล็กได้ง่ายขึ้น และช่วยให้ผู้ปฏิบัติงานในคลังสินค้าวางแผนและจัดระเบียบกำลังการผลิตของแท่นวางสินค้าในรถบรรทุกได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="0a108-106">เมื่อคุณใช้การเรียงลำดับขาออก คุณสามารถเรียงลำดับคอนเทนเนอร์ที่บรรจุไปยังแท่นวางสินค้าที่ถูกต้องได้ หลังจากที่อยู่ที่สถานีบรรจุแล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="0a108-107">นอกจากนี้ คุณยังสามารถสร้างลำดับชั้นการบรรจุได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="0a108-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="0a108-108">ฟังก์ชันนี้ช่วยให้คุณสามารถสร้างแท่นวางสินค้าจากคอนเทนเนอร์ที่บรรจุผ่านฟังก์ชันการบรรจุ</span><span class="sxs-lookup"><span data-stu-id="0a108-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="0a108-109">คอนเทนเนอร์จะไม่ถูกส่งไปยังสถานที่จัดส่งขั้นสุดท้าย เนื่องจากอยู่ในลำดับการบรรจุเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0a108-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="0a108-110">แต่ผู้ปฏิบัติงานสามารถปิดคอนเทนเนอร์และย้ายไปยังที่ตั้งชนิดการเรียงลำดับได้</span><span class="sxs-lookup"><span data-stu-id="0a108-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="0a108-111">จากนั้น สามารถเรียงลำดับคอนเทนเนอร์ไปยังตำแหน่งต่างๆ แต่ละตำแหน่งมีป้ายทะเบียน (LP)</span><span class="sxs-lookup"><span data-stu-id="0a108-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="0a108-112">หลังจากที่มีการเรียงลำดับคอนเทนเนอร์แล้ว คุณสามารถสร้างงานเพื่อส่ง LP ทั้งหมดไปยังท่าจัดส่งสินค้าหรือที่ตั้งระยะสุดท้าย โดยยึดตามคำสั่งสถานที่หรือความต้องการของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="0a108-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="0a108-113">นอกจากนี้ การดำเนินการปิดของตำแหน่งการเรียงลำดับสามารถย้ายสินค้าคงคลังไปยังสถานที่จัดส่งขั้นสุดท้ายและเบิกสินค้าไปยังใบสั่งได้ทันที</span><span class="sxs-lookup"><span data-stu-id="0a108-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="0a108-114">เปิดคุณลักษณะการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="0a108-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="0a108-115">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="0a108-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="0a108-116">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="0a108-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0a108-117">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0a108-118">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0a108-119">**ชื่อคุณลักษณะ:** *การเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="0a108-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="0a108-120">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0a108-120">Setup</span></span>

<span data-ttu-id="0a108-121">สำหรับสถานการณ์จำลองนี้ คุณต้องใช้ข้อมูลสาธิต **USMF** มาตรฐาน และคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="0a108-122">นอกจากนี้ คุณยังต้องดำเนินการการตั้งค่าที่อธิบายไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="0a108-123">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="0a108-123">Set up a wave template</span></span>

<span data-ttu-id="0a108-124">การตั้งค่านี้ประมวลผลเวฟโดยอัตโนมัติ และสร้างงานเมื่อบรรทัดถูกนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="0a108-125">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="0a108-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="0a108-126">ในรายการเท็มเพลต เลือก **คลังสินค้า 62**</span><span class="sxs-lookup"><span data-stu-id="0a108-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="0a108-127">บน FastTab **ทั่วไป** โปรดตรวจสอบให้แน่ใจว่า มีการตั้งค่าตัวเลือก **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="0a108-128">ตั้งค่าผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-128">Set up a worker</span></span>

<span data-ttu-id="0a108-129">สถานีบรรจุถือว่าเป็นที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0a108-129">The packing station is considered a location.</span></span> <span data-ttu-id="0a108-130">ผู้ปฏิบัติงานคลังสินค้าที่ลงชื่อเข้าใช้ที่สถานีบรรจุ ให้ดูและทำงานเฉพาะกับการจัดส่งและคอนเทนเนอร์ที่วางแผนไว้ที่สถานที่บรรจุที่ระบุนั้น</span><span class="sxs-lookup"><span data-stu-id="0a108-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="0a108-131">ผู้ใช้ที่ลงชื่อเข้าใช้ Microsoft Dynamics 365 ต้องได้รับการตั้งค่าเป็นผู้ปฏิบัติงานในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="0a108-132">ถ้าชื่อของผู้ใช้ไม่ปรากฏในรายชื่อผู้ใช้งาน ให้ใช้กระบวนงานต่อไปนี้เพื่อเพิ่มชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0a108-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="0a108-133">ขั้นตอนเหล่านี้สมมติว่ามีผู้ใช้อยู่แล้วในระบบและเชื่อมโยงกับพนักงานหรือผู้ปฏิบัติงานในโมดูล **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0a108-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="0a108-134">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="0a108-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="0a108-135">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0a108-135">Select **New**.</span></span>
1. <span data-ttu-id="0a108-136">ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกผู้ใช้เป้าหมายในรายชื่อพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="0a108-137">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="0a108-137">Select **Select**.</span></span>
1. <span data-ttu-id="0a108-138">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="0a108-139">บน FastTab **ผู้ใช้** ให้เลือก **สร้าง** เพื่อสร้างบัญชีอุปกรณ์เคลื่อนที่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="0a108-140">**รหัสผู้ใช้:** ป้อนรหัสที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="0a108-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="0a108-141">**ชื่อผู้ใช้:** ป้อนชื่อสำหรับรหัส</span><span class="sxs-lookup"><span data-stu-id="0a108-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="0a108-142">**คลังสินค้าเริ่มต้น:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-143">**ชื่อเมนู:** *หลัก*</span><span class="sxs-lookup"><span data-stu-id="0a108-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="0a108-144">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="0a108-145">กล่องโต้ตอบ **กำหนดรหัสผ่าน** ปรากฏขึ้น ที่ซึ่งคุณสามารถสร้างรหัสผ่านอย่างง่ายซึ่งผู้ใช้สามารถใช้เพื่อลงชื่อเข้าใช้ในแอปสำหรับอุปกรณ์เคลื่อนที่ได้</span><span class="sxs-lookup"><span data-stu-id="0a108-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="0a108-146">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-146">Set the following values:</span></span>

    - <span data-ttu-id="0a108-147">**รหัสผ่าน:** ป้อนรหัสผ่านอย่างง่าย</span><span class="sxs-lookup"><span data-stu-id="0a108-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="0a108-148">**ยืนยันรหัสผ่าน:** ป้อนรหัสผ่านเดียวกันอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0a108-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="0a108-149">เลือก **ตั้งค่าหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="0a108-149">Select **Set password**.</span></span>

    <span data-ttu-id="0a108-150">การแจ้งเตือนในศูนย์ปฏิบัติการจะแจ้งให้คุณทราบว่า มีการตั้งค่ารหัสผ่านสำหรับผู้ใช้ที่คุณสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="0a108-151">สร้างชนิดสถานที่</span><span class="sxs-lookup"><span data-stu-id="0a108-151">Create a location type</span></span>

1. <span data-ttu-id="0a108-152">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> ชนิดสถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="0a108-153">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดสถานที่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="0a108-154">**ชนิดสถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="0a108-155">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="0a108-156">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="0a108-157">ตั้งค่าพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="0a108-158">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="0a108-159">บนแท็บ **ทั่วไป** บน FastTab **ชนิดสถานที่** ให้ตั้งค่าฟิลด์ **ชนิดสถานที่เรียงลำดับ** เป็น *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="0a108-160">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="0a108-161">ตั้งค่าโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="0a108-161">Set up a location profile</span></span>

1. <span data-ttu-id="0a108-162">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="0a108-163">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-164">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="0a108-165">**รหัสโพรไฟล์สถานที่:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="0a108-166">**ชื่อ:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="0a108-167">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-168">**รูปแบบสถานที่:** *ASRB* (ที่เก็บ ชั้นเก็บสินค้า ชั้นวาง และช่องเก็บ)</span><span class="sxs-lookup"><span data-stu-id="0a108-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="0a108-169">**ชนิดสถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="0a108-170">**ใช้การติดตามป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="0a108-171">**อนุญาตสินค้าผสม:** *ใช่* (เมื่อคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* ตัวเลือก **อนุญาตให้มีชุดงานสินค้าคงคลังผสม** จะถูกตั้งค่าเป็น *ใช่* โดยอัตโนมัติ และไม่สามารถเปลี่ยนแปลงได้โดยอิสระ)</span><span class="sxs-lookup"><span data-stu-id="0a108-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="0a108-172">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="0a108-173">ตั้งค่าสถานที่</span><span class="sxs-lookup"><span data-stu-id="0a108-173">Set up a location</span></span>

1. <span data-ttu-id="0a108-174">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> สถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="0a108-175">ในส่วนหัว ให้ยกเลิกการเลือกกล่องกาเครื่องหมาย **สร้างตัวเลขการตรวจสอบสำหรับสถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="0a108-176">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างสถานที่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="0a108-177">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-178">**สถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="0a108-179">**รหัสโพรไฟล์สถานที่:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="0a108-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="0a108-180">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="0a108-181">ตั้งค่าเท็มเพลตการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="0a108-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="0a108-182">เท็มเพลตการเรียงลำดับขาออกจะกำหนดว่างานจะถูกสร้างขึ้นจากที่ตั้งการเรียงลำดับหรือไม่ และจะมีการดำเนินการเรียงลำดับด้วยตนเองหรือโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0a108-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="0a108-183">สำหรับสถานการณ์นี้ คุณจะสร้างเท็มเพลตการเรียงลำดับขาออกเพื่อสร้างแท่นวางสินค้าหลังจากสถานีบรรจุ</span><span class="sxs-lookup"><span data-stu-id="0a108-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="0a108-184">ไปยัง **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> เท็มเพลตการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="0a108-185">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-186">ในส่วนหัวของเท็มเพลตใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="0a108-187">**รหัสเท็มเพลตการเรียงลำดับขาออก:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="0a108-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="0a108-188">**คำอธิบาย:** *การสร้างงานอัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="0a108-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="0a108-189">**ชนิดเท็มเพลตการเรียงลำดับขาออก:** *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="0a108-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="0a108-190">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-191">**สถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="0a108-192">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-193">**การยืนยันการเรียงลำดับ:** *การสแกนตำแหน่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="0a108-194">**สร้างงานในการปิดตำแหน่ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="0a108-195">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* เมื่อปิดตำแหน่ง จะมีการสร้างงานเพื่อย้ายสินค้าคงคลังไปยังสถานที่จัดส่งขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="0a108-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="0a108-196">ถ้ามีการตั้งค่าเป็น *ไม่* จะมีการเบิกสินค้าคงคลังไปยังใบสั่งนี้โดยทันที เมื่อมีการปิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0a108-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="0a108-197">**การมอบหมายตำแหน่ง:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="0a108-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="0a108-198">ถ้ามีการตั้งค่าฟิลด์นี้เป็น *ด้วยตนเอง* ผู้ใช้จะต้องระบุตำแหน่งที่ควรเรียงลำดับสินค้าคงคลังให้เสมอ</span><span class="sxs-lookup"><span data-stu-id="0a108-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="0a108-199">ถ้ามีการตั้งค่าเป็น *อัตโนมัติ* ระบบจะแนะนำสินค้าคงคลังไปยังตำแหน่งโดยอัตโนมัติ เมื่อใดก็ตามที่สามารถทำได้ โดยยึดตามการแบ่งเท็มเพลตการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="0a108-200">เลือก **บันทึก** เพื่อทำให้ปุ่ม **แก้ไขการสอบถาม** ในบานหน้าต่างการดำเนินการนั้นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="0a108-201">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="0a108-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="0a108-202">ในตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มบรรทัดที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="0a108-203">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="0a108-204">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="0a108-205">**ฟิลด์:** *บริการขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="0a108-206">เมื่อคุณเลือกค่านี้ คุณอาจได้รับข้อความต่อไปนี้: "บริการผู้ขนส่งฟิลด์ไม่ใช่ฟิลด์ดัชนี</span><span class="sxs-lookup"><span data-stu-id="0a108-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="0a108-207">คุณต้องการเพิ่มการเรียงลำดับหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="0a108-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="0a108-208">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0a108-208">Select **Yes**.</span></span>

    - <span data-ttu-id="0a108-209">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="0a108-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="0a108-210">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-210">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-211">คุณอาจได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดกลุ่มจะถูกรีเซ็ต ดำเนินการต่อหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="0a108-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="0a108-212">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0a108-212">Select **Yes**.</span></span>

    <span data-ttu-id="0a108-213">ปุ่ม **การแบ่งเท็มเพลตการเรียงลำดับขาออก** ในบานหน้าต่างการดำเนินการ จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="0a108-214">ในบานหน้าต่างการดำเนินการ ให้เลือก **การแบ่งเท็มเพลตการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="0a108-215">ในกล่องโต้ตอบ **เกณฑ์การเรียงลำดับขาออก** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a108-216">**ชื่อตารางอ้างอิง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="0a108-217">**ชื่อฟิลด์การอ้างอิง:** *บริการผู้ขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="0a108-218">**ฟิลด์จัดกลุ่มตาม:** เลือกกล่องกาเครื่องหมายนี้เพื่อจัดกลุ่มการจัดส่งตามบริการผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="0a108-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="0a108-219">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0a108-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="0a108-220">ตั้งค่านโยบายการบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-220">Set up container packing policies</span></span>

1. <span data-ttu-id="0a108-221">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> นโยบายการบรรจุคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="0a108-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="0a108-222">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-223">ในส่วนหัวของนโยบายใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="0a108-224">**นโยบายการบรรจุคอนเทนเนอร์:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="0a108-225">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="0a108-226">บน FastTab **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-227">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-228">**สถานที่เริ่มต้นสำหรับการเรียงลำดับ:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="0a108-229">**น้ำหนักต่อหน่วย:** *กก.*</span><span class="sxs-lookup"><span data-stu-id="0a108-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="0a108-230">**นโยบายการปิดคอนเทนเนอร์:** *การนำออกใช้โดยอัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="0a108-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="0a108-231">**นโยบายการนำคอนเทนเนอร์ออกใช้:** *กำหนดคอนเทนเนอร์ให้กับตำแหน่งการเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="0a108-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="0a108-232">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="0a108-233">ตั้งค่าโพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="0a108-233">Set up packing profiles</span></span>

<span data-ttu-id="0a108-234">สร้างโพรไฟล์การบรรจุใหม่ซึ่งจะใช้ร่วมกับฟังก์ชันการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="0a108-235">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> โพรไฟล์การบรรจุ**</span><span class="sxs-lookup"><span data-stu-id="0a108-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="0a108-236">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างบรรทัด และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="0a108-237">**รหัสโพรไฟล์การบรรจุ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="0a108-238">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="0a108-239">**นโยบายการบรรจุคอนเทนเนอร์:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="0a108-240">**โหมดรหัสคอนเทนเนอร์:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="0a108-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="0a108-241">**ชนิดคอนเทนเนอร์:** *กล่อง-ใหญ่*</span><span class="sxs-lookup"><span data-stu-id="0a108-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="0a108-242">**สร้างคอนเทนเนอร์ที่การปิดคอนเทนเนอร์โดยอัตโนมัติ:** ยกเลิกการเลือก (= *ไม่*)</span><span class="sxs-lookup"><span data-stu-id="0a108-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="0a108-243">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="0a108-244">ตั้งค่าคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-244">Set up work classes</span></span>

<span data-ttu-id="0a108-245">ตั้งค่าคลาสงานที่จะใช้ร่วมกับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="0a108-246">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="0a108-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="0a108-247">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างคลาสงานสำหรับการเรียงลำดับ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="0a108-248">**รหัสคลาสงาน:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="0a108-249">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="0a108-250">**ชนิดของใบสั่งงาน:** *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="0a108-251">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="0a108-252">ตั้งค่ารายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0a108-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="0a108-253">ตั้งค่ารายการเมนูบนแท่นวางสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="0a108-254">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่เพื่อสร้างแท่นวางสินค้าในระหว่างการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="0a108-255">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="0a108-256">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-257">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="0a108-258">**ชื่อรายการเมนู:** *การสร้างแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="0a108-259">**ชื่อ:** *การสร้างแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="0a108-260">**โหมด:** *ทางอ้อม*</span><span class="sxs-lookup"><span data-stu-id="0a108-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="0a108-261">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="0a108-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="0a108-262">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-263">**รหัสกิจกรรม:** *การเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="0a108-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="0a108-264">เมื่อมีการตั้งค่าฟิลด์นี้เป็น *การเรียงลำดับขาออก* ฟิลด์ **รหัสเท็มเพลตการเรียงลำดับขาออก** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="0a108-265">**ใช้คู่มือกระบวนการ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="0a108-266">เมื่อมีการตั้งค่าฟิลด์ **รหัสกิจกรรม** เป็น *การเรียงลำดับขาออก* ตัวเลือกนี้จะถูกตั้งค่าเป็น *ใช่* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0a108-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="0a108-267">**รหัสเท็มเพลตการเรียงลำดับขาออก:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="0a108-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="0a108-268">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="0a108-269">ตั้งค่ารายการเมนูการโหลดใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-269">Set up a new loading menu item</span></span>

<span data-ttu-id="0a108-270">ถัดไป ให้สร้างรายการเมนูที่ช่วยให้ผู้ใช้สามารถย้ายสินค้าในสินค้าคงคลังที่เรียงลำดับไปยังสถานที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0a108-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="0a108-271">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="0a108-272">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-273">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="0a108-274">**ชื่อรายการเมนู:** *โหลดจากการเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="0a108-275">**ชื่อ:** *โหลดจากการเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="0a108-276">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="0a108-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="0a108-277">**ใช้งานที่มีอยู่:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="0a108-278">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **สั่งการโดย** เป็น *สั่งการโดยผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="0a108-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="0a108-279">บน FastTab **คลาสงาน** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="0a108-280">**รหัสคลาสงาน:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="0a108-281">**ชนิดของใบสั่งงาน:** *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="0a108-282">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="0a108-283">ตั้งค่าเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0a108-283">Set up the mobile device menu</span></span>

<span data-ttu-id="0a108-284">ขณะนี้คุณต้องเพิ่มรายการเมนูใหม่ลงในเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0a108-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="0a108-285">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="0a108-286">เลือกเมนู **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="0a108-287">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0a108-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0a108-288">ในคอลัมน์ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือก **การสร้างแท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="0a108-289">เลือกปุ่มลูกศรขวาเพื่อย้าย **การสร้างแท่นวางสินค้า** ไปยังคอลัมน์ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="0a108-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="0a108-290">ใช้ปุ่มลูกศรขึ้นและปุ่มลูกศรลงเพื่อใส่รายการเมนู **การสร้างแท่นวางสินค้า** ในตำแหน่งที่ต้องการบนเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0a108-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="0a108-291">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-291">Select **Save**.</span></span>
1. <span data-ttu-id="0a108-292">ทำซ้ำกระบวนงานนี้เพื่อเพิ่มรายการเมนู **โหลดจากการเรียงลำดับ** ไปยังเมนู **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="0a108-293">ตั้งค่าคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="0a108-293">Set up location directives</span></span>

<span data-ttu-id="0a108-294">*คำสั่งสถานที่* คือกฎซึ่งช่วยให้ระบุสถานที่เบิกสินค้าและส่งสินค้าสำหรับการย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0a108-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="0a108-295">ขณะนี้คุณต้องสร้างกฎเพื่อจัดการงานการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="0a108-296">ตั้งค่าคำสั่ง SKU เดียว</span><span class="sxs-lookup"><span data-stu-id="0a108-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="0a108-297">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="0a108-298">ในบานหน้าต่างด้านซ้าย ให้เปลี่ยนค่าของฟิลด์ **ชนิดของใบสั่งงาน** เป็น *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="0a108-299">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-300">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="0a108-301">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-302">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="0a108-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="0a108-303">บน FastTab **คำสั่งสถานที่** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-304">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="0a108-305">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="0a108-305">**Site:** *6*</span></span>
    - <span data-ttu-id="0a108-306">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-307">**SKU หลายรายการ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="0a108-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="0a108-308">เลือก **บันทึก** เพื่อทำให้แถบเครื่องมือบน FastTab **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="0a108-309">บน FastTab **รายการ** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้ในรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="0a108-310">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0a108-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="0a108-311">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-312">**จาก:** *0*</span><span class="sxs-lookup"><span data-stu-id="0a108-312">**From:** *0*</span></span>
    - <span data-ttu-id="0a108-313">**ถึง:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="0a108-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="0a108-314">เลือก **บันทึก** เพื่อทำให้แถบเครื่องมือบน FastTab **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="0a108-315">บน FastTab **การดำเนินการคำสั่งสถานที่** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้ในรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="0a108-316">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0a108-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="0a108-317">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-318">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="0a108-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="0a108-319">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-319">Select **Save**.</span></span>
1. <span data-ttu-id="0a108-320">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="0a108-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="0a108-321">ในตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้ค้นหาแถวที่มีการตั้งค่า **ฟิลด์** เป็น *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="0a108-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="0a108-322">ตั้งค่าฟิลด์ **เงื่อนไข** สำหรับแถวนี้เป็น *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="0a108-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="0a108-323">เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ และปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="0a108-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="0a108-324">ตั้งค่าคำสั่ง SKU หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="0a108-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="0a108-325">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="0a108-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="0a108-326">ในบานหน้าต่างด้านซ้าย ให้เปลี่ยนค่าของฟิลด์ **ชนิดของใบสั่งงาน** เป็น *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="0a108-327">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-328">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="0a108-329">**ลำดับ:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a108-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="0a108-330">**ชื่อ:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="0a108-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="0a108-331">บน FastTab **คำสั่งสถานที่** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-332">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="0a108-333">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="0a108-333">**Site:** *6*</span></span>
    - <span data-ttu-id="0a108-334">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-335">**SKU หลายรายการ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="0a108-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="0a108-336">เลือก **บันทึก** เพื่อทำให้แถบเครื่องมือบน FastTab **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="0a108-337">บน FastTab **รายการ** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้ในรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="0a108-338">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0a108-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="0a108-339">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-340">**จาก:** *0*</span><span class="sxs-lookup"><span data-stu-id="0a108-340">**From:** *0*</span></span>
    - <span data-ttu-id="0a108-341">**ถึง:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="0a108-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="0a108-342">เลือก **บันทึก** เพื่อทำให้แถบเครื่องมือบน FastTab **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="0a108-343">บน FastTab **การดำเนินการคำสั่งสถานที่** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้ในรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="0a108-344">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0a108-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="0a108-345">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-346">**ชื่อ:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="0a108-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="0a108-347">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-347">Select **Save**.</span></span>
1. <span data-ttu-id="0a108-348">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="0a108-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="0a108-349">ในตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้ค้นหาแถวที่มีการตั้งค่า **ฟิลด์** เป็น *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="0a108-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="0a108-350">ตั้งค่าฟิลด์ **เงื่อนไข** สำหรับแถวนี้เป็น *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="0a108-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="0a108-351">เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ และปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="0a108-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="0a108-352">ตั้งค่าเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-352">Set up work templates</span></span>

1. <span data-ttu-id="0a108-353">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="0a108-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0a108-354">เปลี่ยนค่าของฟิลด์ **ชนิดของใบสั่งงาน** เป็น *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="0a108-355">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="0a108-356">บนแท็บ **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="0a108-357">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="0a108-358">**เท็มเพลตงาน:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="0a108-359">**คำอธิบายเท็มเพลตงาน:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="0a108-360">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a108-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="0a108-361">บน FastTab **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัด แล้วจากนั้น ตั้งค่าค่าดังต่อไปนี้สำหรับบรรทัดนั้น:</span><span class="sxs-lookup"><span data-stu-id="0a108-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="0a108-362">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="0a108-363">**รหัสคลาสงาน:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="0a108-364">เลือก **สร้าง** อีกครั้งเพื่อเพิ่มบรรทัดที่สอง แล้วจากนั้น ตั้งค่าค่าต่อไปนี้สำหรับบรรทัดนั้น:</span><span class="sxs-lookup"><span data-stu-id="0a108-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="0a108-365">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0a108-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="0a108-366">**รหัสคลาสงาน:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="0a108-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="0a108-367">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0a108-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="0a108-368">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="0a108-368">Scenario</span></span>

<span data-ttu-id="0a108-369">สถานการณ์จำลองนี้จำลองสถานการณ์ ที่ซึ่งคอนเทนเนอร์ที่มีการบรรจุควรถูกเรียงลำดับเป็นตำแหน่งต่างๆ (แท่นวางสินค้า) โดยอัตโนมัติหลังจากสถานีบรรจุสินค้า ทั้งนี้ขึ้นอยู่กับบริการของผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="0a108-370">หลังจากที่มีการบรรจุสินค้าทั้งหมดจากโหลดและเรียงลำดับตามที่อยู่ แท่นวางสินค้าจะถูกย้ายไปที่พื้นที่ประตู</span><span class="sxs-lookup"><span data-stu-id="0a108-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="0a108-371">สร้างใบสั่งขายและงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="0a108-372">สร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="0a108-372">Create sales order 1</span></span>

1. <span data-ttu-id="0a108-373">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0a108-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0a108-374">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-375">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a108-376">**บัญชีลูกค้า:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="0a108-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="0a108-377">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="0a108-378">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0a108-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="0a108-379">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="0a108-380">สลับไปยังมุมมอง **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="0a108-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="0a108-381">บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="0a108-382">**ผู้ขนส่งสินค้า:** *สายการบิน*</span><span class="sxs-lookup"><span data-stu-id="0a108-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="0a108-383">**บริการขนส่ง:** *อากาศ*</span><span class="sxs-lookup"><span data-stu-id="0a108-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="0a108-384">สลับไปยังมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="0a108-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="0a108-385">ถ้ารายการใหม่ไม่ถูกเพิ่มโดยอัตโนมัติไปยังกริดบน FastTab **รายการใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="0a108-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="0a108-386">ในรายการใบสั่งใหม่ ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="0a108-387">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="0a108-388">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a108-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="0a108-389">ในขณะที่รายการใบสั่งใหม่ยังคงถูกเลือกอยู่บน FastTab **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** ข้างบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="0a108-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="0a108-390">บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="0a108-391">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="0a108-392">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="0a108-393">คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="0a108-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="0a108-394">จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0a108-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="0a108-395">ใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="0a108-395">Sales order 2</span></span>

1. <span data-ttu-id="0a108-396">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0a108-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0a108-397">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0a108-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a108-398">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a108-399">**บัญชีลูกค้า:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="0a108-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="0a108-400">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="0a108-401">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0a108-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="0a108-402">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-402">The new sales order is opened.</span></span> <span data-ttu-id="0a108-403">ฟิลด์นี้ควรมีบรรทัดใหม่ว่างเปล่าในกริดบนแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="0a108-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0a108-404">ตั้งค่าค่าต่อไปนี้ในรายการใบสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="0a108-405">**สินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="0a108-406">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="0a108-407">บน FastTab **รายละเอียดของรายการ** บนแท็บ **การจัดส่ง** ให้ตั้งค่าฟิลด์ **โหมดการจัดส่ง** เป็น *Flowe-STD*</span><span class="sxs-lookup"><span data-stu-id="0a108-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="0a108-408">บน FastTab **รายการใบสั่งขาย** ให้เลือก **เพิ่มรายการ** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้ในรายการใบสั่งที่สอง:</span><span class="sxs-lookup"><span data-stu-id="0a108-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="0a108-409">**สินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a108-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="0a108-410">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="0a108-411">บน FastTab **รายละเอียดของรายการ** บนแท็บ **การจัดส่ง** ให้เปลี่ยนค่าของฟิลด์ **โหมดการจัดส่ง** เป็น *Air C-Air*</span><span class="sxs-lookup"><span data-stu-id="0a108-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="0a108-412">บน FastTab **รายการใบสั่งขาย** เลือกรายการใบสั่งแรก</span><span class="sxs-lookup"><span data-stu-id="0a108-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="0a108-413">จากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="0a108-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="0a108-414">บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="0a108-415">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="0a108-416">บน FastTab **รายการใบสั่งขาย** เลือกรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="0a108-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="0a108-417">จากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="0a108-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="0a108-418">บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="0a108-419">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="0a108-420">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="0a108-421">คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="0a108-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="0a108-422">โปรดสังเกตว่ามีการสร้างหมายเลขรหัสเวฟสองหมายเลขและหมายเลขรหัสการจัดส่งสองหมายเลข หนึ่งหมายเลขสำหรับโหมดการจัดส่งแต่ละโหมดสำหรับรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="0a108-423">เรียกดูรหัสงานจากรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="0a108-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="0a108-424">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="0a108-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="0a108-425">หน้าแสดงรหัสงานที่สร้างขึ้นจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="0a108-426">ใช้รหัสคลื่นและรหัสการจัดส่งจากใบสั่งขายที่คุณสร้างขึ้น เพื่อหารหัสงานสำหรับเวฟและการจัดส่งแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="0a108-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="0a108-427">จดบันทึกรหัสงานเหล่านั้น เนื่องจากคุณจะต้องใช้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0a108-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="0a108-428">โปรดสังเกตว่ามีการสร้างรหัสงานสองรหัสสำหรับใบสั่งขายที่สอง</span><span class="sxs-lookup"><span data-stu-id="0a108-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="0a108-429">ถ้ามีการเบิกสินค้าที่แตกต่างกันจากสถานที่เก็บที่แตกต่างกัน จะมีการสร้างรหัสงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="0a108-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="0a108-430">เบิกสินค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-430">Pick items for the sales orders</span></span>

<span data-ttu-id="0a108-431">ทำงานที่สร้างขึ้นให้เสร็จสมบูรณ์โดยใช้อุปกรณ์เคลื่อนที่เพื่อย้ายสินค้าไปยังสถานีบรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a108-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="0a108-432">บนอุปกรณ์เคลื่อนที่ ให้ลงชื่อเข้าใช้คลังสินค้า *62* โดยใช้รหัสผู้ใช้ที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ (หรือรหัสผู้ใช้ของผู้ใช้ข้อมูลสาธิตที่มีอยู่)</span><span class="sxs-lookup"><span data-stu-id="0a108-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="0a108-433">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="0a108-434">บนเมนู **ขาออก** ให้เลือก **การเบิกสินค้าขาย**</span><span class="sxs-lookup"><span data-stu-id="0a108-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="0a108-435">ในฟิลด์ **รหัส** ให้ป้อนรหัสงานที่สร้างไว้สำหรับใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="0a108-436">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-436">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-437">บนหน้า **ใบสั่งขาย - เบิกสินค้า** ให้ป้อน LP เป้าหมายที่สร้างไว้สำหรับใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="0a108-438">โปรดสังเกตว่าสถานที่เบิกสินค้า (*bulk-001*) สินค้า (*A0001*) และปริมาณ (*2 pcs*) จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="0a108-439">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-439">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-440">รีวิวข้อมูลในหน้า **ใบสั่งขาย - ส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="0a108-441">ฟิลด์ **Loc** ควรบ่งชี้ว่าสินค้าที่เบิกจะไปที่สถานที่ *บรรจุ*</span><span class="sxs-lookup"><span data-stu-id="0a108-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="0a108-442">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-442">Select **OK**.</span></span>

    <span data-ttu-id="0a108-443">บนหน้า **สแกนรหัสงาน / รหัสป้ายทะเบียน** คุณจะได้รับข้อความ "งานเสร็จสมบูรณ์" ซึ่งบ่งชี้ว่ารหัสงานจากใบสั่งขายที่ 1 เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="0a108-444">ขณะนี้คุณจะเบิกสินค้าตามใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="0a108-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="0a108-445">ในฟิลด์ **รหัส** ให้ป้อนรหัสงานที่สร้างไว้สำหรับใบสั่งขายที่ 2 ขณะที่รายการที่ 1 มีสินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="0a108-446">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-446">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-447">บนหน้า **ใบสั่งขาย - เบิกสินค้า** ให้ป้อน LP เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="0a108-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="0a108-448">โปรดสังเกตว่าสถานที่เบิกสินค้า (*bulk-001*) สินค้า (*A0001*) และปริมาณ (*1 pcs*) จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="0a108-449">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-449">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-450">รีวิวข้อมูลในหน้า **ใบสั่งขาย - ส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="0a108-451">ฟิลด์ **Loc** ควรบ่งชี้ว่าสินค้าที่เบิกจะไปที่สถานที่ *บรรจุ*</span><span class="sxs-lookup"><span data-stu-id="0a108-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="0a108-452">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-452">Select **OK**.</span></span>

    <span data-ttu-id="0a108-453">บนหน้า **สแกนรหัสงาน / รหัสป้ายทะเบียน** คุณจะได้รับข้อความ "งานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="0a108-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="0a108-454">ข้อความนี้บ่งชี้ว่ารหัสงานจากบรรทัดที่ 1 ของใบสั่งขายที่ 2 เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="0a108-455">ในฟิลด์ **รหัส** ให้ป้อนรหัสงานที่สร้างไว้สำหรับใบสั่งขายที่ 2 ขณะที่รายการที่ 2 มีสินค้า *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a108-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="0a108-456">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-456">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-457">บนหน้า **ใบสั่งขาย - เบิกสินค้า** ให้ป้อน LP เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="0a108-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="0a108-458">โปรดสังเกตว่าสถานที่เบิกสินค้า (*bulk-002*) สินค้า (*A0001*) และปริมาณ (*1 pcs*) จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="0a108-459">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-459">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-460">รีวิวข้อมูลในหน้า **ใบสั่งขาย - ส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="0a108-461">ฟิลด์ **Loc** ควรบ่งชี้ว่าสินค้าที่เบิกจะไปที่สถานที่ *บรรจุ*</span><span class="sxs-lookup"><span data-stu-id="0a108-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="0a108-462">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-462">Select **OK**.</span></span>

    <span data-ttu-id="0a108-463">บนหน้า **สแกนรหัสงาน / รหัสป้ายทะเบียน** คุณจะได้รับข้อความ "งานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="0a108-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="0a108-464">ข้อความนี้บ่งชี้ว่ารหัสงานจากรายการที่ 2 ของใบสั่งขายที่ 2 เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="0a108-465">บรรจุใบสั่งขายลงในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="0a108-466">บรรจุใบสั่งขายที่ 1 ลงในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="0a108-467">ไปที่ **การจัดการคลังสินค้า \> การบรรจุและการบรรจุลงตู้บรรจุสินค้า \> บรรจุ**</span><span class="sxs-lookup"><span data-stu-id="0a108-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="0a108-468">กล่องโต้ตอบ **เลือกสถานีบรรจุสินค้า** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="0a108-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="0a108-469">โดยค่าเริ่มต้น ควรมีการตั้งค่าฟิลด์ **ผู้ปฏิบัติงาน** เป็นชื่อของผู้ปฏิบัติงานที่คุณตั้งค่าไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0a108-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="0a108-470">ตั้งค่าค่าต่อไปนี้เพื่อดูและทำงานกับการจัดส่งและคอนเทนเนอร์ที่วางแผนไว้ที่สถานที่บรรจุที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="0a108-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="0a108-471">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="0a108-471">**Site:** *6*</span></span>
    - <span data-ttu-id="0a108-472">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="0a108-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="0a108-473">**สถานที่:** *บรรจุ*</span><span class="sxs-lookup"><span data-stu-id="0a108-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="0a108-474">**รหัสโพรไฟล์การบรรจุ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="0a108-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="0a108-475">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0a108-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="0a108-476">บนหน้า **บรรจุ** ในฟิลด์ **ป้ายทะเบียนหรือการจัดส่ง** ให้ป้อน LP เป้าหมายสำหรับใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="0a108-477">แล้วเลือก **แท็บ** หรือ **ป้อน** คีย์บนแป้นพิมพ์เพื่อย้ายออกจากฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0a108-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="0a108-478">บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0a108-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="0a108-479">ยอมรับการตั้งค่าเริ่มต้นทั้งหมด และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="0a108-480">จดบันทึกรหัสคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="0a108-481">บน FastTab **การบรรจุสินค้า** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-482">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="0a108-483">**ตัวระบุ:** สินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="0a108-484">บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="0a108-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="0a108-485">ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้เลือก **ดูน้ำหนักของระบบ** เพื่อให้ระบบปรับปรุงฟิลด์ **น้ำหนักรวม**</span><span class="sxs-lookup"><span data-stu-id="0a108-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="0a108-486">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-486">Select **OK**.</span></span> <span data-ttu-id="0a108-487">คอนเทนเนอร์ถูกย้ายไปสถานที่ *SORT* และพร้อมสำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="0a108-488">สร้างคอนเทนเนอร์ที่สองเพื่อเพิ่มสินค้าที่สองจาก LP สำหรับใบสั่งขายที่ 1 ไปยังคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="0a108-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="0a108-489">บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0a108-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="0a108-490">ยอมรับการตั้งค่าเริ่มต้นทั้งหมด และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="0a108-491">จดบันทึกรหัสคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="0a108-492">บน FastTab **การบรรจุสินค้า** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-493">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="0a108-494">**ตัวระบุ:** สินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="0a108-495">บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="0a108-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="0a108-496">ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้เลือก **ดูน้ำหนักของระบบ** เพื่อให้ระบบปรับปรุงฟิลด์ **น้ำหนักรวม**</span><span class="sxs-lookup"><span data-stu-id="0a108-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="0a108-497">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-497">Select **OK**.</span></span> <span data-ttu-id="0a108-498">คอนเทนเนอร์ถูกย้ายไปสถานที่ *SORT* และพร้อมสำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="0a108-499">บรรจุใบสั่งขายที่ 2 ลงในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="0a108-500">บนหน้า **บรรจุ** ในฟิลด์ **ป้ายทะเบียนหรือการจัดส่ง** ให้ป้อน LP เป้าหมายสำหรับรายการที่ 1 ของใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="0a108-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="0a108-501">แล้วเลือก **แท็บ** หรือ **ป้อน** คีย์บนแป้นพิมพ์เพื่อย้ายออกจากฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0a108-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="0a108-502">บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0a108-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="0a108-503">ยอมรับการตั้งค่าเริ่มต้นทั้งหมด และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="0a108-504">จดบันทึกรหัสคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="0a108-505">บน FastTab **การบรรจุสินค้า** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-506">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="0a108-507">**ตัวระบุ:** สินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="0a108-508">บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="0a108-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="0a108-509">ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้เลือก **ดูน้ำหนักของระบบ** เพื่อให้ระบบปรับปรุงฟิลด์ **น้ำหนักรวม**</span><span class="sxs-lookup"><span data-stu-id="0a108-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="0a108-510">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-510">Select **OK**.</span></span> <span data-ttu-id="0a108-511">คอนเทนเนอร์ถูกย้ายไปสถานที่ *SORT* และพร้อมสำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="0a108-512">ในฟิลด์ **ป้ายทะเบียนหรือการจัดส่ง** ให้ป้อน LP เป้าหมายสำหรับรายการที่ 2 ของใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="0a108-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="0a108-513">แล้วเลือก **แท็บ** หรือ **ป้อน** คีย์บนแป้นพิมพ์เพื่อย้ายออกจากฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0a108-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="0a108-514">บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0a108-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="0a108-515">ยอมรับการตั้งค่าเริ่มต้นทั้งหมด และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="0a108-516">จดบันทึกรหัสคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="0a108-517">บน FastTab **การบรรจุสินค้า** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a108-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0a108-518">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="0a108-519">**ฟิลด์ตัวระบุ:** สินค้า *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a108-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="0a108-520">บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="0a108-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="0a108-521">ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้เลือก **ดูน้ำหนักของระบบ** เพื่อให้ระบบปรับปรุงฟิลด์ **น้ำหนักรวม**</span><span class="sxs-lookup"><span data-stu-id="0a108-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="0a108-522">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-522">Select **OK**.</span></span> <span data-ttu-id="0a108-523">คอนเทนเนอร์ถูกย้ายไปสถานที่ *SORT* และพร้อมสำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="0a108-524">ถ้าต้องการดูรายละเอียดคอนเทนเนอร์ ให้ไปที่ **การจัดการคลังสินค้า \> การบรรจุและการบรรจุลงตู้บรรจุสินค้า \> คอนเทนเนอร์** และค้นหารหัสคอนเทนเนอร์ที่สร้างขึ้นในระหว่างการบรรจุ</span><span class="sxs-lookup"><span data-stu-id="0a108-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="0a108-525">เรียงลำดับคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a108-526">เมื่อคุณเข้าถึงรายการเมนู **การสร้างแท่นวางสินค้า** บนแอปสำหรับอุปกรณ์เคลื่อนที่เพื่อทำการเรียงลำดับขาออก คุณจะเห็นปุ่มที่ติดป้ายชื่อ **แบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="0a108-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="0a108-527">*อย่าใช้ปุ่ม **แบบเต็ม** เพื่อเรียงลำดับหรือปิดตำแหน่ง*</span><span class="sxs-lookup"><span data-stu-id="0a108-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="0a108-528">ปุ่ม **แบบเต็ม** จะระบุโดยค่าเริ่มต้น และไม่สามารถปิดใช้งานหรือลบออกจากหน้าได้</span><span class="sxs-lookup"><span data-stu-id="0a108-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="0a108-529">ซึ่งไม่มีการใช้สำหรับคุณลักษณะ *การเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="0a108-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="0a108-530">เรียงลำดับคอนเทนเนอร์แรก</span><span class="sxs-lookup"><span data-stu-id="0a108-530">Sort the first container</span></span>

1. <span data-ttu-id="0a108-531">บนอุปกรณ์เคลื่อนที่ ให้ลงชื่อเข้าใช้คลังสินค้า *62* โดยใช้รหัสผู้ใช้ที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ (หรือรหัสผู้ใช้ของผู้ใช้ข้อมูลสาธิตที่มีอยู่)</span><span class="sxs-lookup"><span data-stu-id="0a108-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="0a108-532">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="0a108-533">บนเมนู **ขาออก** ให้เลือก **การสร้างแท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="0a108-534">ในฟิลด์ **LP/Con** ให้ป้อนรหัสคอนเทนเนอร์แรกที่สัมพันธ์กับใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="0a108-535">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-535">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-536">เนื่องจากไม่มีตำแหน่งการเรียงลำดับอยู่ในขณะนี้ คุณต้องระบุหนึ่งตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0a108-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="0a108-537">ในฟิลด์ **รหัสตำแหน่งการเรียงลำดับ** ให้ป้อน *SP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="0a108-538">เนื่องจากไม่มี LP ที่เชื่อมโยงกับตำแหน่งการเรียงลำดับ *SP01* อยู่ในขณะนี้ คุณต้องระบุหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="0a108-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="0a108-539">ในฟิลด์ **LP** ป้อน *PLP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="0a108-540">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-540">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-541">เนื่องจากมีการเปิดใช้งานการตรวจสอบความถูกต้องของตำแหน่งการเรียงลำดับ คุณต้องป้อนรหัสตำแหน่งการเรียงลำดับอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0a108-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="0a108-542">ในฟิลด์ **รหัสตำแหน่งการเรียงลำดับ** ให้ป้อน *SP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="0a108-543">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-543">Select **OK**.</span></span>

    <span data-ttu-id="0a108-544">คุณได้รับข้อความ "งานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="0a108-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="0a108-545">เมื่อต้องการดูตำแหน่งการเรียงลำดับและ LP ในนั้น ให้ไปที่ **การจัดการคลังสินค้า \> การบรรจุและการบรรจุลงตู้บรรจุสินค้า \> การกำหนดตำแหน่งการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="0a108-546">หน้า **การกำหนดตำแหน่งการเรียงลำดับขาออก** จะแสดงตำแหน่งการเรียงลำดับทั้งหมดที่ใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="0a108-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="0a108-547">ฟิลด์ **ธุรกรรมตำแหน่งการเรียงลำดับ** จะแสดง LP ที่สัมพันธ์กับแต่ละตำแหน่งการเรียงลำดับแต่ละตำแหน่ง และคอนเทนเนอร์ที่อยู่ในตำแหน่งการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="0a108-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="0a108-548">โปรดสังเกตว่าตำแหน่งการเรียงลำดับหนึ่งตำแหน่งมีอยู่ในขณะนี้ และ FastTab **เกณฑ์ตำแหน่งการเรียงลำดับ** จะแสดงเกณฑ์ของ **การจัดส่ง – บริการผู้ขนส่ง - อากาศ**</span><span class="sxs-lookup"><span data-stu-id="0a108-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="0a108-549">เรียงลำดับคอนเทนเนอร์ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="0a108-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="0a108-550">บนอุปกรณ์เคลื่อนที่ ให้ลงชื่อเข้าใช้คลังสินค้า *62* โดยใช้รหัสผู้ใช้ที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ (หรือรหัสผู้ใช้ของผู้ใช้ข้อมูลสาธิตที่มีอยู่)</span><span class="sxs-lookup"><span data-stu-id="0a108-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="0a108-551">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="0a108-552">บนเมนู **ขาออก** ให้เลือก **การสร้างแท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="0a108-553">ในฟิลด์ **LP/Con** ให้ป้อนรหัสคอนเทนเนอร์ที่สองที่สัมพันธ์กับใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="0a108-554">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-554">Select **OK**.</span></span> <span data-ttu-id="0a108-555">เนื่องจากมีการตั้งค่าเท็มเพลตการเรียงลำดับเพื่อเรียงลำดับโดยอัตโนมัติ และมีตำแหน่งการเรียงลำดับที่มีเงื่อนไขที่ตรงกันอยู่แล้ว คุณจะถูกส่งไปยังตำแหน่งการเรียงลำดับที่ถูกต้องโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0a108-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="0a108-556">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-556">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-557">ยืนยันรหัสตำแหน่งการเรียงลำดับเพื่อระบุว่าสินค้าคงคลังอยู่ในสถานที่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0a108-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="0a108-558">ในฟิลด์ **รหัสตำแหน่งการเรียงลำดับ** ให้ป้อน *SP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="0a108-559">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-559">Select **OK**.</span></span>

    <span data-ttu-id="0a108-560">งานจะเสร็จสมบูรณ์บในคอนเทนเนอร์ที่สองจากใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="0a108-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="0a108-561">ขณะนี้คุณจะเรียงลำดับคอนเทนเนอร์ที่เหลือจากใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="0a108-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="0a108-562">ในฟิลด์ **LP/Con** ให้ป้อนรหัสคอนเทนเนอร์ของคอนเทนเนอร์จากใบสั่งขายที่ 2 ที่มีสินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a108-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="0a108-563">เนื่องจากบริการของผู้ขนส่งแตกต่างกัน คุณจะได้รับพร้อมท์ให้ป้อนตำแหน่งการเรียงลำดับใหม่และกำหนด LP ให้กับตำแหน่งดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0a108-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="0a108-564">ใช้ตำแหน่งการเรียงลำดับ *SP02* และ LP *PLP02*</span><span class="sxs-lookup"><span data-stu-id="0a108-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="0a108-565">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-565">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-566">ยืนยันตำแหน่งการเรียงลำดับโดยป้อน *SP02* ในฟิลด์ **รหัสตำแหน่งการเรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="0a108-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="0a108-567">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-567">Select **OK**.</span></span>

    <span data-ttu-id="0a108-568">งานเสร็จสมบูรณ์ในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="0a108-569">ในฟิลด์ **LP/Con** ให้ป้อนรหัสคอนเทนเนอร์สำหรับคอนเทนเนอร์ที่เหลือจากใบสั่งขายที่ 2 ที่มีสินค้า *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a108-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="0a108-570">เนื่องจากบริการของผู้ขนส่งเหมือนกับบริการของผู้ขนส่งสำหรับใบสั่งขายที่ 1 ระบบจะแสดงตำแหน่งการเรียงลำดับที่มีอยู่ที่มีเกณฑ์ที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="0a108-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="0a108-571">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-571">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-572">ยืนยันตำแหน่งการเรียงลำดับโดยป้อน *SP01* ในฟิลด์ **รหัสตำแหน่งการเรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="0a108-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="0a108-573">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-573">Select **OK**.</span></span>

    <span data-ttu-id="0a108-574">งานเสร็จสมบูรณ์ในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0a108-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="0a108-575">ปิดตำแหน่งการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="0a108-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="0a108-576">เมื่อมีการเรียงลำดับสินค้าคงคลังทั้งหมดแล้ว ต้องปิดตำแหน่งก่อนจึงจะสามารถสร้างงานได้</span><span class="sxs-lookup"><span data-stu-id="0a108-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="0a108-577">งานการเบิกสินค้าคงคลังที่เรียงลำดับจะถูกสร้างขึ้นเพื่อให้มีการจัดเก็บสินค้าคงคลังไปที่พื้นที่ประตู</span><span class="sxs-lookup"><span data-stu-id="0a108-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="0a108-578">ปิดตำแหน่งจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0a108-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="0a108-579">บนอุปกรณ์เคลื่อนที่ ให้ลงชื่อเข้าใช้คลังสินค้า *62* โดยใช้รหัสผู้ใช้ที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ (หรือรหัสผู้ใช้ของผู้ใช้ข้อมูลสาธิตที่มีอยู่)</span><span class="sxs-lookup"><span data-stu-id="0a108-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="0a108-580">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="0a108-581">บนเมนู **ขาออก** ให้เลือก **การสร้างแท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0a108-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="0a108-582">ในฟิลด์ **LP/Con** ให้ป้อนรหัสคอนเทนเนอร์ที่มีการเรียงลำดับเพื่อเรียงลำดับตำแหน่ง *SP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="0a108-583">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-583">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-584">คุณได้รับข้อความต่อไปนี้: "คอนเทนเนอร์ถูกเรียงลำดับให้กับตำแหน่ง SP01 แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="0a108-585">ปิดตำแหน่งหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="0a108-585">Close the position?"</span></span> <span data-ttu-id="0a108-586">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="0a108-586">Select **Close**.</span></span>

    <span data-ttu-id="0a108-587">งานเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="0a108-588">ปิดตำแหน่งงานจากการกำหนดตำแหน่งการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="0a108-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="0a108-589">ไปที่ **การจัดการคลังสินค้า \> การบรรจุและการบรรจุลงตู้บรรจุสินค้า \> การกำหนดตำแหน่งการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="0a108-590">ในคอลัมน์ด้านซ้าย เลือก **SP02**</span><span class="sxs-lookup"><span data-stu-id="0a108-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="0a108-591">แถวตำแหน่งการเรียงลำดับขาออกนี้เป็นแถวที่คุณจะปิด</span><span class="sxs-lookup"><span data-stu-id="0a108-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="0a108-592">บนหน้าต่างการดำเนินการ เลือก **ปิดตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="0a108-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="0a108-593">เรกคอร์ดตำแหน่งการเรียงลำดับถูกปิด และไม่มีการแสดงไว้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="0a108-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="0a108-594">เมื่อต้องการแสดงเรกคอร์ดตำแหน่งที่ปิดอยู่ทั้งหมด ให้เลือกกล่องกาเครื่องหมาย **แสดงที่ปิด**</span><span class="sxs-lookup"><span data-stu-id="0a108-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="0a108-595">การเบิกสินค้าคงคลังที่จัดเรียง</span><span class="sxs-lookup"><span data-stu-id="0a108-595">Sorted inventory picking</span></span>

<span data-ttu-id="0a108-596">คุณต้องทำงานการเบิกสินค้าคงคลังที่เรียงลำดับให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0a108-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="0a108-597">เมื่อเสร็จสมบูรณ์ ระบบจะเบิกสินค้าคงคลังไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0a108-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="0a108-598">ณ จุดนั้น กระบวนการคลังสินค้าอื่นๆ ทั้งหมดจะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="0a108-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="0a108-599">บนอุปกรณ์เคลื่อนที่ ให้ลงชื่อเข้าใช้คลังสินค้า *62* โดยใช้รหัสผู้ใช้ที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ (หรือรหัสผู้ใช้ของผู้ใช้ข้อมูลสาธิตที่มีอยู่)</span><span class="sxs-lookup"><span data-stu-id="0a108-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="0a108-600">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="0a108-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="0a108-601">บนเมนู **ขาออก** ให้เลือก **โหลดจากการเรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="0a108-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="0a108-602">ป้อนรหัส LP เป้าหมายจากตำแหน่งการเรียงลำดับแรก *SP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="0a108-603">ตั้งค่าฟิลด์ **รหัส** เป็น *PLP01*</span><span class="sxs-lookup"><span data-stu-id="0a108-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="0a108-604">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-604">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-605">หน้า **การเบิกสินค้าคงคลังที่เรียงลำดับ: เบิกสินค้า** จะแสดงงานการเบิกสินค้าที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="0a108-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="0a108-606">เบิกสินค้าจากสถานที่ *SORT* และเป้าหมาย LP *PLP01* ซึ่งมีสินค้าหลายรายการและปริมาณเท่ากับ *3*</span><span class="sxs-lookup"><span data-stu-id="0a108-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="0a108-607">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-607">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-608">หน้า **การเบิกสินค้าคงคลังที่เรียงลำดับ: ส่งสินค้า** จะแสดงงานการส่งสินค้าที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="0a108-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="0a108-609">ส่งสินค้าไปยังสถานที่ *Baydoor* และเป้าหมาย LP *PLP01* ซึ่งมีสินค้าหลายรายการและปริมาณเท่ากับ *3*</span><span class="sxs-lookup"><span data-stu-id="0a108-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="0a108-610">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-610">Select **OK**.</span></span>

    <span data-ttu-id="0a108-611">งานเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-611">Work is completed.</span></span>

1. <span data-ttu-id="0a108-612">ป้อนรหัสป้ายทะเบียนเป้าหมายจากตำแหน่งการเรียงลำดับที่สอง *SP02*</span><span class="sxs-lookup"><span data-stu-id="0a108-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="0a108-613">ตั้งค่าฟิลด์ **รหัส** เป็น *PLP02*</span><span class="sxs-lookup"><span data-stu-id="0a108-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="0a108-614">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-614">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-615">หน้า **การเบิกสินค้าคงคลังที่เรียงลำดับ: เบิกสินค้า** จะแสดงงานการเบิกสินค้าที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="0a108-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="0a108-616">เบิกสินค้าจากสถานที่ *SORT* และเป้าหมาย LP *PLP02* ซึ่งมีสินค้าหลายรายการและปริมาณเท่ากับ *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="0a108-617">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-617">Select **OK**.</span></span>
1. <span data-ttu-id="0a108-618">หน้า **การเบิกสินค้าคงคลังที่เรียงลำดับ: ส่งสินค้า** จะแสดงงานการส่งสินค้าที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="0a108-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="0a108-619">ส่งสินค้าไปยังสถานที่ *Baydoor* และเป้าหมาย LP *PLP02* ซึ่งมีสินค้าหลายรายการและปริมาณเท่ากับ *1*</span><span class="sxs-lookup"><span data-stu-id="0a108-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="0a108-620">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0a108-620">Select **OK**.</span></span>

    <span data-ttu-id="0a108-621">งานเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="0a108-621">Work is completed.</span></span>

<span data-ttu-id="0a108-622">ตั้งแต่จุดนี้เป็นต้นไป กระบวนการคลังสินค้าอื่นๆ ทั้งหมดจะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="0a108-622">From this point forward, all other warehouse processes apply.</span></span>
