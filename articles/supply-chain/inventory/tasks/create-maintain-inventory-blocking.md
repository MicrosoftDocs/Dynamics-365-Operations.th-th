---
title: สร้างและรักษาการบล็อคสินค้าคงคลัง
description: หัวข้อนี้อธิบายวิธีการใช้การบล็อคสินค้าคงคลังเพื่อป้องกันสินค้าคงคลังคงเหลือทางกายภาพจากการสำรองไว้โดยเอกสารต้นทางขาออกอื่นๆ
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956169"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="687e2-103">สร้างและรักษาการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="687e2-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="687e2-104">หัวข้อนี้อธิบายวิธีการใช้การบล็อคสินค้าคงคลังเพื่อป้องกันสินค้าคงคลังคงเหลือทางกายภาพจากการสำรองไว้โดยเอกสารต้นทางขาออกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="687e2-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="687e2-105">ก่อนที่คุณจะเริ่มต้นกระบวนงานนี้ คุณต้องมีสินค้าที่สินค้าคงคลังคงเหลือทางกายภาพพร้อมให้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="687e2-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="687e2-106">บล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="687e2-106">Block inventory</span></span>

<span data-ttu-id="687e2-107">หากต้องการสร้างเรกคอร์ดการบล็อคสินค้าคงคลังเพื่อให้สินค้าคงคลังถูกบล็อค ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="687e2-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="687e2-108">ไปยัง **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การบล็อคสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="687e2-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="687e2-109">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="687e2-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="687e2-110">บนส่วนหัวของเรกคอร์ดการบล็อคใหม่ ให้ตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็นสินค้าที่คุณต้องการบล็อค และป้อนข้อความอธิบาย</span><span class="sxs-lookup"><span data-stu-id="687e2-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="687e2-111">บน FastTab **ทั่วไป** ในฟิลด์ **ปริมาณ** ให้ป้อนจำนวนของสินค้าที่จะบล็อค</span><span class="sxs-lookup"><span data-stu-id="687e2-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="687e2-112">บน FastTab **มิติสินค้าคงคลัง** ให้ระบุไซต์และคลังสินค้าที่ซึ่งมีสินค้าที่คุณต้องการบล็อคอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="687e2-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="687e2-113">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="687e2-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="687e2-114">ปรับปรุงเงื่อนไขของการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="687e2-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="687e2-115">หากต้องการอัพเดตเรกคอร์ดการบล็อคสินค้าคงคลัง ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="687e2-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="687e2-116">ไปยัง **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การบล็อคสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="687e2-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="687e2-117">ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดการบล็อคที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="687e2-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="687e2-118">แก้ไขเรกคอร์ดตามความจําเป็น</span><span class="sxs-lookup"><span data-stu-id="687e2-118">Edit the record as required.</span></span> <span data-ttu-id="687e2-119">ตัวอย่างเช่น คุณอาจเปลี่ยนแปลงค่าของฟิลด์ **วันที่คาดไว้** เพื่อระบุเวลาที่สินค้าคงคลังที่ถูกบล็อคถูกคาดว่าจะพร้อมใช้งานสำหรับการจอง</span><span class="sxs-lookup"><span data-stu-id="687e2-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="687e2-120">ถ้ามีการเลือกตัวเลือก **การรับสินค้าที่คาดไว้** วันที่จะปรากฏในธุรกรรมที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="687e2-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="687e2-121">(มีการเลือกตัวเลือก **การรับสินค้าที่คาดไว้** โดยค่าเริ่มต้น เมื่อคุณสร้างเรกคอร์ดการบล็อคด้วยตนเอง)</span><span class="sxs-lookup"><span data-stu-id="687e2-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="687e2-122">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="687e2-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="687e2-123">ยกเลิกการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="687e2-123">Unblock inventory</span></span>

<span data-ttu-id="687e2-124">หากต้องการลบเรกคอร์ดการบล็อคสินค้าคงคลังเพื่อให้สินค้าคงคลังถูกยกเลิกบล็อค ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="687e2-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="687e2-125">ไปยัง **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การบล็อคสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="687e2-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="687e2-126">ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดการบล็อคที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="687e2-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="687e2-127">บนบานหน้าต่างการดำเนินการ ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="687e2-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="687e2-128">คุณได้รับพร้อมต์เพื่อยืนยันการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="687e2-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="687e2-129">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="687e2-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="687e2-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="687e2-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
