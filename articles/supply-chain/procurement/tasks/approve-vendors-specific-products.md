---
title: อนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ
description: 'กระบวนงานนี้แสดงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ '
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383285"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="9816a-103">อนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="9816a-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9816a-104">กระบวนงานนี้แสดงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="9816a-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="9816a-105">ซึ่งจะช่วยให้คุณสามารถควบคุมว่าสามารถใช้ผู้จัดจำหน่ายใดเมื่อมีการเพิ่มผลิตภัณฑ์ลงในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="9816a-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="9816a-106">คุณสามารถใช้กระบวนงานนี้ในข้อมูลสาธิตของบริษัท USMF หรือข้อมูลของคุณเอง ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9816a-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="9816a-107">โดยทั่วไป งานนี้จะถูกดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="9816a-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="9816a-108">ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="9816a-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="9816a-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9816a-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9816a-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9816a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9816a-111">ขยายแท็บด่วน **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9816a-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="9816a-112">ถ้ามีผู้จัดจำหน่ายหลักแสดงอยู่ในฟิลด์ **ผู้จัดจำหน่าย** จากนั้น คุณต้องเพิ่มผู้จัดจำหน่ายนี้ให้เป็นผู้จัดจำหน่ายที่ได้รับอนุมัติในขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9816a-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="9816a-113">จดบันทึกหมายเลขผู้จัดจำหน่าย ถ้ามีการแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9816a-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="9816a-114">บนบานหน้าต่างการดำเนินการ คลิก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9816a-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="9816a-115">คลิก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="9816a-115">Click **Setup**.</span></span>
7. <span data-ttu-id="9816a-116">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9816a-116">Click **Add**.</span></span>
8. <span data-ttu-id="9816a-117">ในฟิลด์ผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9816a-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="9816a-118">เลือกผู้จัดจำหน่ายที่ได้รับอนุมัติ </span><span class="sxs-lookup"><span data-stu-id="9816a-118">Select the approved vendor.</span></span> <span data-ttu-id="9816a-119">ต้องมีอย่างน้อยหนึ่งบรรทัดที่มีผู้จัดจำหน่ายหลักถ้ามีผู้จัดจำหน่ายหลักอยู่ในเรกคอร์ดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9816a-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="9816a-120">ถ้าคุณจดบันทึกหมายเลขผู้จัดจำหน่ายไว้ก่อนหน้า ให้เลือกที่นี่</span><span class="sxs-lookup"><span data-stu-id="9816a-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="9816a-121">ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9816a-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9816a-122">เลือกวันที่ที่ล่วงหน้าหลายเดือน</span><span class="sxs-lookup"><span data-stu-id="9816a-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="9816a-123">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9816a-123">Click **Add**.</span></span>
11. <span data-ttu-id="9816a-124">ในฟิลด์ **ผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9816a-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="9816a-125">ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9816a-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9816a-126">เลือกวันที่ที่แตกต่างจากวันหมดอายุก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="9816a-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-127">Close the page.</span></span>
14. <span data-ttu-id="9816a-128">บนบานหน้าต่างการดำเนินการ คลิก **ผู้จัดจำหน่ายที่ได้รับอนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="9816a-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="9816a-129">ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9816a-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="9816a-130">วันที่นี้ทำหน้าที่เป็นตัวกรอง ดังนั้นคุณสามารถดูว่าใครคือผู้จัดจำหน่ายที่ได้รับอนุมัติ ถึงวันที่หนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="9816a-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="9816a-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-131">Close the page.</span></span>
17. <span data-ttu-id="9816a-132">บนบานหน้าต่างการดำเนินการ คลิก **รอบระยะเวลาที่บังคับใช้**</span><span class="sxs-lookup"><span data-stu-id="9816a-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="9816a-133">ในฟิลด์ **แสดงผู้จัดจำหน่ายที่หมดอายุตาม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9816a-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="9816a-134">คุณสามารถใช้หน้านี้เพื่อระบุผู้จัดจำหน่าย ที่สถานะการอนุมัติจะหมดอายุหลังจากวันที่หนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="9816a-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="9816a-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-135">Close the page.</span></span>
20. <span data-ttu-id="9816a-136">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9816a-136">Click **Edit**.</span></span>
21. <span data-ttu-id="9816a-137">ในฟิลด์ **วิธีตรวจสอบผู้จัดจำหน่ายที่ได้รับอนุมัติ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="9816a-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="9816a-138">ฟิลด์นี้อนุญาตให้คุณเลือกนโยบายสำหรับสิ่งที่ควรเกิดขึ้น หากผลิตภัณฑ์ถูกเพิ่มไปยังรายการใบสั่งซื้อ ที่ผู้จัดจำหน่ายไม่ใช่ผู้จัดจำหน่ายที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="9816a-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="9816a-139">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9816a-139">Click **Save**.</span></span>
23. <span data-ttu-id="9816a-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-140">Close the page.</span></span>
24. <span data-ttu-id="9816a-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-141">Close the page.</span></span>
25. <span data-ttu-id="9816a-142">ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ความสัมพันธ์ของผู้จัดจำหน่าย/สินค้า > รายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติตามสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9816a-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="9816a-143">หน้านี้แสดงภาพรวมของผลิตภัณฑ์และผู้จัดจำหน่ายที่ได้รับอนุมัติทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9816a-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="9816a-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-144">Close the page.</span></span>
27. <span data-ttu-id="9816a-145">ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9816a-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="9816a-146">คุณยังสามารถเริ่มต้นจากผู้จัดจำหน่าย แล้วไปที่รายการของผลิตภัณฑ์ที่ได้รับอนุมัติสำหรับบัญชีผู้จัดจำหน่ายนั้น</span><span class="sxs-lookup"><span data-stu-id="9816a-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="9816a-147">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9816a-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="9816a-148">บนบานหน้าต่างการดำเนินการ คลิก **การจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9816a-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="9816a-149">คลิก **รายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติตามผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9816a-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="9816a-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-150">Close the page.</span></span>
32. <span data-ttu-id="9816a-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9816a-151">Close the page.</span></span>

