---
title: เปลี่ยนแปลงความเป็นเจ้าของของสินค้าคงคลังที่มีการส่งมอบที่ยึดตามความต้องการการผลิต
description: 'กระบวนงานนี้แสดงวิธีการเปลี่ยนเจ้าของของสินค้าคงคลังที่มีการส่งมอบจากผู้จัดจำหน่ายเป็นนิติบุคคลของคุณเมื่อต้องการสินค้าคงคลังในการผลิต '
author: perlynne
manager: AnnBe
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8200e0235fa78cbef4fdadd1d1c124446b89e72a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145899"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="e702c-103">เปลี่ยนแปลงความเป็นเจ้าของของสินค้าคงคลังที่มีการส่งมอบที่ยึดตามความต้องการการผลิต</span><span class="sxs-lookup"><span data-stu-id="e702c-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e702c-104">กระบวนงานนี้แสดงวิธีการเปลี่ยนเจ้าของของสินค้าคงคลังที่มีการส่งมอบจากผู้จัดจำหน่ายเป็นนิติบุคคลของคุณเมื่อต้องการสินค้าคงคลังในการผลิต </span><span class="sxs-lookup"><span data-stu-id="e702c-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="e702c-105">การเปลี่ยนแปลงความเป็นเจ้าของนี้จะดำเนินการโดยการสร้างและลงรายการบัญชีสมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e702c-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="e702c-106">รายการในสมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของนี้สามารถสร้างขึ้นได้ด้วยตนเอง หรือดังที่แสดงในบันทึกนี้ ตามความต้องของการผลิตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e702c-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="e702c-107">โดยทั่วไปหัวหน้างานฝ่ายผลิตเป็นผู้ดำเนินงานนี้</span><span class="sxs-lookup"><span data-stu-id="e702c-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="e702c-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="e702c-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="e702c-109">ถ้าคุณใช้ข้อมูลของคุณเอง ให้ตรวจสอบให้มั่นใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้: ชื่อสมุดรายวันสินค้าคงคลังที่มีการตั้งค่าไว้สำหรับการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง สินค้าคงคลังคงเหลือที่ผู้จัดจำหน่ายเป็นเจ้าของซึ่งมีการบันทึกไว้จริง และมีรายการใบสั่งผลิตสำหรับวัสดุอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="e702c-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="e702c-110">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="e702c-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="e702c-111">กระบวนการส่งมอบขาออกไม่ได้รับการสนับสนุนแบบสำเร็จรูป และไม่สนับสนุนการประมวลผลสมุดรายวันการเป็นเจ้าของแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e702c-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="e702c-112">สร้างสมุดรายวันความเป็นเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e702c-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="e702c-113">ไปที่ การบริหารสินค้าคงคลัง > รายการสมุดบันทึกรายวัน > สินค้า > การเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e702c-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="e702c-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e702c-114">Click New.</span></span>
    * <span data-ttu-id="e702c-115">สมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลังจะถูกใช้เพื่อเปลี่ยนเจ้าของของสินค้าคงคลังที่มีการส่งมอบจากผู้จัดจำหน่ายเป็นนิติบุคคลปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="e702c-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="e702c-116">การเปลี่ยนแปลงความเป็นเจ้าของนี้จะดำเนินการโดยการนำปริมาณคงคลังคงเหลือที่ผู้จัดจำหน่ายเป็นเจ้าของออกใช้ และรับสินค้าคงคลังนั้นในนิติบุคคลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e702c-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="e702c-117">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e702c-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="e702c-118">คุณสามารถเลือกเฉพาะชื่อสมุดรายวันสินค้าคงคลังที่มีชนิดสมุดรายวันเป็นการเปลี่ยนแปลงความเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="e702c-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="e702c-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e702c-119">Click OK.</span></span>
5. <span data-ttu-id="e702c-120">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="e702c-120">Click Functions.</span></span>
6. <span data-ttu-id="e702c-121">คลิก สร้างรายการสมุดรายวันจากใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e702c-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="e702c-122">คุณสามารถเริ่มต้นกระบวนการเปลี่ยนแปลงความเป็นเจ้าได้โดยสอบถามบรรทัดการผลิตทั้งหมดที่มีความต้องการสำหรับปริมาณการใช้วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="e702c-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="e702c-123">ในฟิลด์สถานะการออกสินค้าคงคลังที่จะรวม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e702c-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="e702c-124">ตัวเลือกนี้ช่วยให้คุณสามารถกรองข้อมูลตามสถานะการตัดสินค้าจากรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e702c-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="e702c-125">ตัวอย่างเช่น คุณสามารถสร้างบรรทัดสมุดรายวันสำหรับสินค้าคงคลังที่มีสถานะการเบิกและที่จองสินค้าที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="e702c-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="e702c-126">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="e702c-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="e702c-127">ส่วนนี้ช่วยให้คุณสามารถใช้การกรองเพิ่มเติม </span><span class="sxs-lookup"><span data-stu-id="e702c-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="e702c-128">ตัวอย่างเช่น คุณสามารถเลือกวันที่จัดหาวัตถุดิบที่เฉพาะเจาะจงได้</span><span class="sxs-lookup"><span data-stu-id="e702c-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="e702c-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e702c-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="e702c-130">ลงรายการบัญชีสมุดรายวันการเปลี่ยนแปลงความเป็นเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e702c-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="e702c-131">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e702c-131">Click Post.</span></span>
    * <span data-ttu-id="e702c-132">เมื่อลงรายการบัญชีสมุดรายวัน สินค้าคงคลังซึ่งมีผู้จัดจำหน่ายเป็นเจ้าของจะถูกนำออกใช้โดยใช้การอ้างอิง "การเปลี่ยนแปลงความเป็นเจ้าของ" </span><span class="sxs-lookup"><span data-stu-id="e702c-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="e702c-133">จากนั้นจะได้รับสินค้าคงคลังเป็นปริมาณคงคลังคงเหลือโดยใช้รายการความเคลื่อนไหวของสินค้าคงคลังที่มีการอัพเดตด้วยใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e702c-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="e702c-134">โปรดทราบว่าจะมีการสร้างเฉพาะรายการความเคลื่อนไหวที่เกี่ยวข้องกับสมุดรายวันที่ลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="e702c-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="e702c-135">และจะไม่มีการสร้างรายการความเคลื่อนไหวของสินค้าคงคลังที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="e702c-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="e702c-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e702c-136">Click OK.</span></span>
3. <span data-ttu-id="e702c-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e702c-137">Close the page.</span></span>

