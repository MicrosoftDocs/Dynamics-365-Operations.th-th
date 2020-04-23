---
title: สร้างข้อตกลงการซื้อ
description: หัวข้อนี้นำคุณผ่านการสร้างข้อตกลงการซื้อ
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207749"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="9da08-103">สร้างข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="9da08-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9da08-104">หัวข้อนี้นำคุณผ่านการสร้างข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="9da08-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="9da08-105">ซึ่งโดยทั่วไปสามารถทำได้โดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="9da08-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="9da08-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="9da08-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9da08-107">คุณต้องตั้งค่าการจัดประเภทข้อตกลงการซื้อก่อนที่คุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9da08-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="9da08-108">เมื่อคุณสร้างข้อตกลงแล้ว คุณสามารถใช้เมื่อคุณสร้างใบสั่งซื้อ และนี่จะคัดลอกเงื่อนไขข้อตกลงการซื้อไปยังหัวข้อและรายการที่อยู่ในใบสั่งที่ได้รับผลกระทบโดยข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="9da08-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="9da08-109">สร้างข้อตกลงการซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="9da08-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="9da08-110">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > ข้อตกลงใบสั่งซื้อ > ข้อตกลงใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9da08-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="9da08-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9da08-111">Click **New**.</span></span>
3. <span data-ttu-id="9da08-112">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือกเมนูแบบหล่นลง และเลือกแถวของเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9da08-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="9da08-113">ในฟิลด์ **การจัดประเภทข้อตกลงการซื้อ** ให้เลือกเมนูแบบหล่นลง และเลือกแถวของเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9da08-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="9da08-114">ขยาย FastTab **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="9da08-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="9da08-115">ในฟิลด์ **วันหมดอายุ** ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9da08-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="9da08-116">วันหมดอายุนี้จะเป็นค่าเริ่มต้นสำหรับรายการข้อผูกมัดทั้งหมด และจะกำหนดระยะเวลาที่ข้อผูกมัดเฉพาะแต่ละรายการจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="9da08-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="9da08-117">ในฟิลด์ **ชื่อเอกสาร** ให้พิมพ์ชื่อสำหรับข้อตกลงการซื้อของคุณ</span><span class="sxs-lookup"><span data-stu-id="9da08-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="9da08-118">ปล่อยให้ฟิลด์ **ข้อผูกมัดเริ่มต้น** ถูกตั้งค่าเป็น **ข้อผูกมัดปริมาณผลิตภัณฑ์** (หรือเปลี่ยนแปลง ถ้าไม่มีการตั้งค่าเป็นรายการนี้)</span><span class="sxs-lookup"><span data-stu-id="9da08-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="9da08-119">ค่าเริ่มต้นข้อผูกมัดกำหนดตัวเลือกรายการข้อตกลง </span><span class="sxs-lookup"><span data-stu-id="9da08-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="9da08-120">ถ้าคุณต้องการชนิดข้อผูกมัดใหม่ เมื่อคุณกำลังสร้างข้อตกลง คุณจำเป็นต้องเปลี่ยนข้อผูกมัดเริ่มต้นบนส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="9da08-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="9da08-121">มีข้อผูกมัด 4 ชนิด: **ข้อผูกมัดปริมาณผลิตภัณฑ์** - สำหรับปริมาณที่ระบุของผลิตภัณฑ์ **ข้อผูกมัดมูลค่าผลิตภัณฑ์** - สำหรับจำนวนสกุลเงินที่ระบุของผลิตภัณฑ์ **ข้อผูกมัดมูลค่าประเภทผลิตภัณฑ์** - สำหรับจำนวนสกุลเงินที่ระบุในประเภทการจัดซื้อที่จำนวนเงินสามารถเป็นยอดเงินสำหรับแค็ตตาล็อกสินค้าหรือสินค้าไม่มีในแค็ตตาล็อก **ข้อผูกมัดมูลค่า** - สำหรับจำนวนสกุลเงินที่ระบุซึ่งสามารถเติมสินค้าโดยผลิตภัณฑ์ใดๆ หรือโดยประเภทการจัดซื้อใดๆ</span><span class="sxs-lookup"><span data-stu-id="9da08-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="9da08-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9da08-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="9da08-123">เพิ่มข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="9da08-123">Add a commitment</span></span>
1. <span data-ttu-id="9da08-124">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="9da08-124">Select **Add line**.</span></span>
2. <span data-ttu-id="9da08-125">ในฟิลด์ **หมายเลขสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="9da08-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="9da08-126">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9da08-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="9da08-127">นี่คือปริมาณรวมที่คุณได้ตกลงที่จะซื้อจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9da08-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="9da08-128">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="9da08-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="9da08-129">ขยายส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="9da08-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="9da08-130">ตั้งค่า **บังคับใช้ค่าสูงสุด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9da08-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="9da08-131">ตัวเลือก **บังคับใช้ค่าสูงสุด** จำกัดการใช้ข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="9da08-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="9da08-132">คุณสามารถซื้อจนถึงปริมาณที่ระบุในฟิลด์ **ปริมาณ** สำหรับรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9da08-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="9da08-133">เพิ่มเงื่อนไขส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="9da08-133">Add header conditions</span></span>
1. <span data-ttu-id="9da08-134">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="9da08-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="9da08-135">เลือก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="9da08-135">Select **Change view**.</span></span>
3. <span data-ttu-id="9da08-136">เลือก **มุมมองส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="9da08-136">Select **Header view**.</span></span>
4. <span data-ttu-id="9da08-137">ขยายส่วน **ข้อกำหนด**</span><span class="sxs-lookup"><span data-stu-id="9da08-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="9da08-138">ในฟิลด์ **วิธีการชำระเงิน** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="9da08-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="9da08-139">เงื่อนไขการชำระเงินจากบัญชีผู้จัดจำหน่ายจะแสดงไว้ที่นี่โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9da08-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="9da08-140">ในฟิลด์ **โหมดของการจัดส่ง** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="9da08-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="9da08-141">ในฟิลด์ **เงื่อนไขการจัดส่ง** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9da08-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="9da08-142">ยืนยันและเรียกใช้ข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="9da08-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="9da08-143">ในบานหน้าต่างการดำเนินการ เลือก **ข้อตกลงการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9da08-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="9da08-144">เลือก **การยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="9da08-144">Select **Confirmation**.</span></span> <span data-ttu-id="9da08-145">ตั้งค่าตัวเลือก **ทำเครื่องหมายข้อตกลงเป็นมีผลบังคับใช้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9da08-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="9da08-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9da08-146">Select **OK**.</span></span>
4. <span data-ttu-id="9da08-147">ในบานหน้าต่างการดำเนินการ เลือก **ข้อตกลงการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9da08-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="9da08-148">เลือก **การยืนยันข้อตกลงการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9da08-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="9da08-149">ตัวเลือก **การแสดงตัวอย่าง/พิมพ์** อนุญาตให้คุณสร้างเอกสารสำหรับข้อตกลงการซื้อ ซึ่งคุณสามารถพิมพ์หรือส่งไปยังผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="9da08-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="9da08-150">ถ้าคุณอัพเดตข้อตกลงในภายหลัง และยืนยันอีกครั้ง เวอร์ชันทั้งสองจะถูกแสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="9da08-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="9da08-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9da08-151">Close the page.</span></span>

