---
title: ฟิลด์น้ําหนักบนรายการสินค้าไม่ตรงกับฟิลด์น้ําหนักบนสินค้า
description: ฟิลด์น้ําหนักบนรายการสินค้าไม่ตรงกับฟิลด์น้ําหนักบนสินค้า
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924362"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="48b25-103">ฟิลด์น้ําหนักบนรายการสินค้าไม่ตรงกับฟิลด์น้ําหนักบนสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="48b25-104">รหัสข้อผิดพลาด: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="48b25-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="48b25-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="48b25-105">Symptoms</span></span>

<span data-ttu-id="48b25-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="48b25-106">The system shows the following error message:</span></span>

> <span data-ttu-id="48b25-107">ฟิลด์น้ําหนักบนรายการสินค้าไม่ตรงกับฟิลด์น้ําหนักบนสินค้า %1</span><span class="sxs-lookup"><span data-stu-id="48b25-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="48b25-108">รันการตรวจสอบความสอดคล้องของน้ําหนักของปริมาณงานในคลังสินค้าเพื่อคำนวณฟิลด์น้ําหนักอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="48b25-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="48b25-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="48b25-109">Cause</span></span>

<span data-ttu-id="48b25-110">ฟิลด์ **น้ําหนักสุทธิ** และ **น้ำหนักหีบห่อ** ถูกตั้งค่าเป็น *0* (ศูนย์) ในรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="48b25-111">อย่างไรก็ตาม ไม่ได้ตั้งค่าฟิลด์น้ําหนักเป็น *0* เพื่อการวัดน้ําหนักในผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="48b25-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="48b25-112">เมื่อไม่ได้ตั้งค่าฟิลด์น้ําหนักบนรายการสินค้า การแก้ไขใด ๆ ของปริมาณบนรายการสินค้าอาจทําให้การคํานวณน้ําหนักของสินค้าไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="48b25-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="48b25-113">ปัญหานี้อาจเกิดขึ้นถ้ามีการเปลี่ยนน้ําหนักของผลิตภัณฑ์นับตั้งแต่สร้างรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="48b25-114">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="48b25-114">Resolution</span></span>

<span data-ttu-id="48b25-115">โดยค่าเริ่มต้น เมื่อมีการสร้างรายการสินค้า ฟิลด์น้ําหนักจากผลิตภัณฑ์จะถูกป้อนลงไป</span><span class="sxs-lookup"><span data-stu-id="48b25-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="48b25-116">หากน้ําหนักเป็นศูนย์ คุณสามารถคำนวณใหม่ได้โดยใช้ฟังก์ชัน *การตรวจสอบความสอดคล้องของน้ําหนักของสินค้าในคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="48b25-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="48b25-117">ไปที่ **การจัดการระบบ \> งานประจำงวด \> ฐานข้อมูล \> การตรวจสอบความสอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="48b25-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="48b25-118">ในกล่องโต้ตอบ **การตรวจสอบความสอดคล้องกัน** ให้ตั้งค่าฟิลด์ **โมดูล** เป็น *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="48b25-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="48b25-119">ให้ตั้งค่าฟิลด์ **ตรวจสอบ/แก้ไข** เพื่อ *แก้ไขข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="48b25-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="48b25-120">ในรายการกล่องกาเครื่องหมาย ให้เลือกกล่องกาเครื่องหมาย **ความสอดคล้องของน้ําหนักของสินค้าในคลังสินค้า** และตรวจสอบให้แน่ใจว่ามีการเน้นเฉพาะแถวของกล่องกาเครื่องหมายนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="48b25-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="48b25-121">ที่ด้านบนของรายการกล่องกาเครื่องหมาย ให้เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **กล่องโต้ตอบ** บนเมนู</span><span class="sxs-lookup"><span data-stu-id="48b25-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="48b25-122">ในกล่องโต้ตอบการตรวจสอบ **ความสอดคล้องของน้ําหนักของสินค้าในคลังสินค้า** ให้ตั้งค่าฟิลด์ต่อไปนี้เพื่อระบุเกณฑ์ที่ควรรันการตรวจสอบความสอดคล้องกันของน้ําหนักของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="48b25-123">**รหัสสินค้า:** ระบุรหัสสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="48b25-124">ปล่อยฟิลด์นี้ว่างไว้เพื่อตรวจสอบรหัสสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="48b25-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="48b25-125">**หมายเลขสินค้า:** ระบุหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="48b25-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="48b25-126">ปล่อยฟิลด์นี้ว่างไว้เพื่อตรวจสอบสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="48b25-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="48b25-127">**คำนวณน้ําหนักในสินค้าอีกครั้งเสมอ:** ตั้งค่าตัวเลือกนี้เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="48b25-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="48b25-128">**อนุญาตให้เขียนทับน้ําหนักบนรายการสินค้า:** ตั้งค่าตัวเลือกนี้เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="48b25-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="48b25-129">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การตรวจสอบความสอดคล้องกันของน้ําหนักสินค้าในคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="48b25-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="48b25-130">เลือกปุ่มจุดไข่ปลา แล้วเลือก **ดำเนินการ** บนเมนู</span><span class="sxs-lookup"><span data-stu-id="48b25-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="48b25-131">น้ําหนักจะถูกคำนวณใหม่ตามเกณฑ์ที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="48b25-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="48b25-132">เลือกลิงค์ **รายละเอียดข้อความ** เพื่อดูผลลัพธ์ของการตรวจสอบความสอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="48b25-132">Select the **Message details** link to view the result of the consistency check.</span></span>
