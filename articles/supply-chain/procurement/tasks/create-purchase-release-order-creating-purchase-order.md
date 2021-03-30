---
title: สร้างใบสั่งซื้อที่นำออกใช้เมื่อสร้างใบสั่งซื้อ
description: 'ขั้นตอนนี้แสดงวิธีการใช้ข้อตกลงการซื้อเมื่อคุณสร้างใบสั่งซื้อ '
author: RichardLuan
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaa441318ed7d00ce205f4f59b983b25cf97f086
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211993"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="bdfeb-103">สร้างใบสั่งซื้อที่นำออกใช้เมื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-103">Create a purchase release order when creating the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdfeb-104">ขั้นตอนนี้แสดงวิธีการใช้ข้อตกลงการซื้อเมื่อคุณสร้างใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="bdfeb-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="bdfeb-105">ข้อตกลงการซื้อนั้นจะต้องนำไปใช้เมื่อคุณสร้างใบสั่งซื้อเนื่องจากมีเงื่อนไขทั่วไปที่ควรจะถูกคัดลอกไปยังหัวข้อใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="bdfeb-106">โดยปกติแล้วงานนี้จะถูกดำเนินการโดยตัวแทนจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="bdfeb-107">ตามข้อกำหนดเบื้องต้นสำหรับคำแนะนำนี้ คุณต้องมีข้อตกลงการซื้อที่มีผลบังคับใช้กับข้อผูกมัดเกี่ยวกับปริมาณผลิตภัณฑ์สำหรับผู้จัดจำหน่ายและสินค้า</span><span class="sxs-lookup"><span data-stu-id="bdfeb-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="bdfeb-108">สามารถใช้ขั้นตอนเดียวกันถ้าคุณมีข้อตกลงการซื้อกับชนิดข้อผูกมัดอื่น</span><span class="sxs-lookup"><span data-stu-id="bdfeb-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="bdfeb-109">คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="bdfeb-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="bdfeb-110">ถ้าคุณกำลังใช้ USMF คุณสามารถรันคำแนะนำ "สร้างข้อตกลงการซื้อ" ก่อน เพื่อตั้งค่าเงื่อนไขเบื้องต้นที่จำเป็นสำหรับคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="bdfeb-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bdfeb-111">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-111">Create a purchase order</span></span>
1. <span data-ttu-id="bdfeb-112">เปิดพื้นที่ทำงานสำหรับการจัดเตรียมใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="bdfeb-113">คลิกใบสั่งซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="bdfeb-113">Click New purchase order.</span></span>
3. <span data-ttu-id="bdfeb-114">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdfeb-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bdfeb-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bdfeb-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdfeb-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bdfeb-117">เปิดปิดการขยายของส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="bdfeb-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="bdfeb-118">ในฟิลด์ข้อตกลงการสั่งซื้อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdfeb-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdfeb-119">ข้อตกลงสำหรับผู้จัดจำหน่ายที่มีอยู่ทั้งหมดจะถูกแสดงไว้ที่นี่ </span><span class="sxs-lookup"><span data-stu-id="bdfeb-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="bdfeb-120">ค้นหาข้อตกลงที่มีผลบังคับใช้ตามที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="bdfeb-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="bdfeb-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdfeb-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bdfeb-122">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="bdfeb-122">Click Yes.</span></span>
10. <span data-ttu-id="bdfeb-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bdfeb-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="bdfeb-124">เพิมรายการ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-124">Add a line</span></span>
1. <span data-ttu-id="bdfeb-125">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bdfeb-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="bdfeb-126">ถ้ามีสินค้าคงคลังหรือขนาดของสถานที่ที่เฉพาะเจาะจงในข้อผูกมัด คุณต้องป้อนข้อมูลเดียวกับรายการใบสั่งซื้อเพื่อให้เป็นไปตามข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="bdfeb-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="bdfeb-127">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdfeb-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdfeb-128">ไซต์นั้นอาจถูกเติมข้อมูลด้วยค่าเริ่มต้นจากใบสั่งหรือจากผู้จัดจำหน่ายเป็นที่เรียบร้อยแล้ว </span><span class="sxs-lookup"><span data-stu-id="bdfeb-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="bdfeb-129">ถ้าเป็นกรณีเช่นนั้นให้ข้ามขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="bdfeb-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="bdfeb-130">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bdfeb-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdfeb-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bdfeb-132">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="bdfeb-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bdfeb-133">ตรวจสอบความถูกต้องว่าราคานั้นถูกคัดลอกมาจากข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="bdfeb-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="bdfeb-134">ค้นหาข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="bdfeb-134">Look up the commitment</span></span>
1. <span data-ttu-id="bdfeb-135">คลิก อัพเดตรายการ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-135">Click Update line.</span></span>
2. <span data-ttu-id="bdfeb-136">คลิก ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="bdfeb-136">Click Attached.</span></span>
    * <span data-ttu-id="bdfeb-137">คุณสามารถรับรายละเอียดสำหรับข้อตกลงการซื้อได้ที่นี่ </span><span class="sxs-lookup"><span data-stu-id="bdfeb-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="bdfeb-138">ตัวอย่างเช่น คุณสามารถดูราคาและราคาและส่วนลดนั้นคงที่หรือไม่ ซึ่งหมายความว่าถ้าคุณเปลี่ยนแปลงราคาหรือส่วนลดในใบสั่งซื้อไปเป็นค่าอื่นกว่าในข้อผูกมัดนั้น ระบบจะลบลิงค์ ดังนั้นรายการใบสั่งซื้อจะไม่ตอบสนองข้อผูกมัดนั้น </span><span class="sxs-lookup"><span data-stu-id="bdfeb-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="bdfeb-139">คุณยังสามารถดูถ้าตัวเลือกบังคับใช้ค่าสูงสุดถูกเลือก ซึ่งหมายความว่าปริมาณในข้อผูกมัดนั้นไม่สามารถเกินข้อจำกัดโดยการรวมการซื้อทั้งหมดที่ตอบสนองข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="bdfeb-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="bdfeb-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bdfeb-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="bdfeb-141">ค้นหาขัอตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="bdfeb-142">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="bdfeb-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="bdfeb-143">คลิกข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="bdfeb-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="bdfeb-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bdfeb-144">Close the page.</span></span>
4. <span data-ttu-id="bdfeb-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bdfeb-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]