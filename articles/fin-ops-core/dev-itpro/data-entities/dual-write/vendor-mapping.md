---
title: ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Dataverse
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 272962b58d8d654c2640a51ef2dbdcd1b05cf8c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560324"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="b2423-103">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม</span><span class="sxs-lookup"><span data-stu-id="b2423-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b2423-104">คำว่า *ผู้จัดจำหน่าย* อ้างอิงถึงองค์กรของซัพพลายเออร์ หรือเจ้าของรายเดียวที่จัดหาสินค้าหรือบริการให้กับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b2423-104">The term *vendor* refers to a supplier organization, or a sole proprietor who supplies goods or services to a business.</span></span> <span data-ttu-id="b2423-105">แม้ว่า *ผู้จัดจำหน่าย* เป็นแนวคิดที่สร้างขึ้นใน Microsoft Dynamics 365 Supply Chain Management จะไม่มีแนวคิดของผู้จัดจำหน่ายอยู่ในแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2423-105">Although *vendor* is an established concept in Microsoft Dynamics 365 Supply Chain Management, no vendor concept exists in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b2423-106">อย่างไรก็ตาม คุณสามารถโอเวอร์โหลดตาราง **บัญชี/ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-106">However, you can overload the **Account/Contact** table to store vendor information.</span></span> <span data-ttu-id="b2423-107">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวมจะแนะนำแนวคิดของผู้จัดจำหน่ายที่ชัดเจนในแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2423-107">The integrated vendor master introduces an explicit vendor concept in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b2423-108">คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายใหม่หรือข้อมูลผู้จัดจำหน่ายร้านค้าในตาราง **บัญชี/ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="b2423-108">You can either use the new vendor design or store vendor data in the **Account/Contact** table.</span></span> <span data-ttu-id="b2423-109">การรวมแบบสองทิศทางสนับสนุนทั้งสองวิธี</span><span class="sxs-lookup"><span data-stu-id="b2423-109">Dual-write supports both approaches.</span></span>

<span data-ttu-id="b2423-110">ในทั้งสองวิธีการ ข้อมูลผู้จัดจำหน่ายจะถูกรวมกันระหว่างพอร์ทัล Dynamics 365 Supply Chain Management Dynamics 365 Sales Dynamics 365 Field Service และ Power Apps</span><span class="sxs-lookup"><span data-stu-id="b2423-110">In both approaches, the vendor data is integrated between Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, and Power Apps portals.</span></span> <span data-ttu-id="b2423-111">ใน Supply Chain Management ข้อมูลจะพร้อมใช้งานสำหรับลำดับงาน เช่น ใบขอซื้อ และใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b2423-111">In Supply Chain Management, the data is available for workflows such as purchase requisitions and purchase orders.</span></span>

## <a name="vendor-data-flow"></a><span data-ttu-id="b2423-112">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-112">Vendor data flow</span></span>

<span data-ttu-id="b2423-113">ถ้าคุณไม่ต้องการจัดเก็บข้อมูลในตาราง **บัญชี/ผู้ติดต่อ** ใน Dataverse คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="b2423-113">If you don't want to store vendor data in the **Account/Contact** table in Dataverse, you can use the new vendor design.</span></span>

![โฟลว์ข้อมูลของผู้จัดจำหน่าย](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="b2423-115">ถ้าคุณไม่ต้องการจัดเก็บข้อมูลของผู้จัดจำหน่ายต่อในตาราง **บัญชี/ผู้ติดต่อ** คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายแบบขยายได้</span><span class="sxs-lookup"><span data-stu-id="b2423-115">If you want to continue to store vendor data in the **Account/Contact** table, you can use the extended vendor design.</span></span> <span data-ttu-id="b2423-116">เมื่อต้องการใช้การออกแบบของผู้จัดจำหน่ายแบบขยาย คุณต้องตั้งค่าคอนฟิกลำดับงานของผู้จัดจำหน่ายในแพคเกจโซลูชันการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="b2423-116">To use the extended vendor design, you must configure the vendor workflows in the dual-write solution package.</span></span> <span data-ttu-id="b2423-117">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สลับระหว่างการออกแบบของผู้จัดจำหน่าย](vendor-switch.md)</span><span class="sxs-lookup"><span data-stu-id="b2423-117">For more information, see [Switch between vendor designs](vendor-switch.md).</span></span>

![โฟลว์ข้อมูลของผู้จัดจำหน่ายแบบขยาย](media/dual-write-vendor-detail.jpg)

> [!TIP]
> <span data-ttu-id="b2423-119">ถ้าคุณกำลังใช้พอร์ทัล Power Apps สำหรับผู้จัดจำหน่ายแบบบริการตนเอง ข้อมูลของผู้จัดจำหน่ายสามารถโฟลว์ไปยังแอป Finance and Operations ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="b2423-119">If you're using Power Apps portals for self-service vendors, the vendor information can flow directly to Finance and Operations apps.</span></span>

## <a name="templates"></a><span data-ttu-id="b2423-120">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b2423-120">Templates</span></span>

<span data-ttu-id="b2423-121">ข้อมูลผู้จัดจำหน่ายรวมถึงข้อมูลทั้งหมดเกี่ยวกับผู้จัดจำหน่าย เช่น กลุ่มผู้จัดจำหน่าย ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และโพรไฟล์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b2423-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="b2423-122">คอเลคชันของแม็บตารางทำงานร่วมกันในขณะการรวมข้อมูลผู้จัดจำหน่าย ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b2423-122">A collection of table maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b2423-123">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2423-123">Finance and Operations apps</span></span> | <span data-ttu-id="b2423-124">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2423-124">Other Dynamics 365 apps</span></span>     | <span data-ttu-id="b2423-125">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b2423-125">Description</span></span>
----------------------------|-----------------------------|------------
<span data-ttu-id="b2423-126">ผู้จัดจำหน่าย V2</span><span class="sxs-lookup"><span data-stu-id="b2423-126">Vendor V2</span></span>                   | <span data-ttu-id="b2423-127">บัญชี</span><span class="sxs-lookup"><span data-stu-id="b2423-127">Account</span></span>                     | <span data-ttu-id="b2423-128">ธุรกิจที่ใช้ตารางบัญชีเพื่อจัดเก็บข้อมูลผู้จัดจำหน่ายสามารถใช้ต่อไปได้ในลักษณะเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b2423-128">Businesses that use the Account table to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="b2423-129">นอกจากนี้ ยังสามารถใช้ประโยชน์จากฟังก์ชันของผู้จัดจำหน่ายที่ชัดเจนซึ่งกำลังจะมา เนื่องจากการรวมของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2423-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="b2423-130">ผู้จัดจำหน่าย V2</span><span class="sxs-lookup"><span data-stu-id="b2423-130">Vendor V2</span></span>                   | <span data-ttu-id="b2423-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="b2423-131">Msdyn\_vendors</span></span>              | <span data-ttu-id="b2423-132">ธุรกิจที่ใช้โซลูชันแบบกำหนดเองสำหรับผู้จัดจำหน่ายสามารถใช้ประโยชน์จากแนวคิดผู้จัดจำหน่ายแบบสำเร็จรูปที่ถูกนำมาใช้ใน Dataverse เนื่องจากการรวมของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2423-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Dataverse because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="b2423-133">กลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-133">Vendor groups</span></span>               | <span data-ttu-id="b2423-134">msdyn\_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="b2423-134">msdyn\_vendorgroups</span></span>         | <span data-ttu-id="b2423-135">เท็มเพลตนี้รวมข้อมูลกลุ่มผู้จัดจำหน่ายเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="b2423-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="b2423-136">วิธีการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-136">Vendor payment method</span></span>       | <span data-ttu-id="b2423-137">msdyn\_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="b2423-137">msdyn\_vendorpaymentmethods</span></span> | <span data-ttu-id="b2423-138">เท็มเพลตนี้รวมข้อมูลวิธีการชำระเงินของผู้จัดจำหน่วยเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="b2423-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="b2423-139">ผู้ติดต่อ CDS V2</span><span class="sxs-lookup"><span data-stu-id="b2423-139">CDS Contacts V2</span></span>             | <span data-ttu-id="b2423-140">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="b2423-140">contacts</span></span>                    | <span data-ttu-id="b2423-141">เท็มเพลต [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) รวมข้อมูลผู้ติดต่อ ปฐมภูม ทุติยภูมิ ตติยภูมิ ทั้งหมดเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="b2423-142">รายการกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b2423-142">Payment schedule lines</span></span>      | <span data-ttu-id="b2423-143">msdyn\_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="b2423-143">msdyn\_paymentschedulelines</span></span> | <span data-ttu-id="b2423-144">เท็มเพลต [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) รวมข้อมูลอ้างอิงสำหรับลูกค้าและผู้จัดจำหน่ายเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="b2423-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="b2423-145">กำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b2423-145">Payment schedule</span></span>            | <span data-ttu-id="b2423-146">msdyn\_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="b2423-146">msdyn\_paymentschedules</span></span>     | <span data-ttu-id="b2423-147">เท็มเพลต [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) รวมข้อมูลอ้างอิงกำหนดการชำระิิเงินเข้าด้วยกัน ทั้งสำหรับลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2423-148">รายการแสดงวันที่ในการชำระเงินของ CDS V2</span><span class="sxs-lookup"><span data-stu-id="b2423-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="b2423-149">msdyn\_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="b2423-149">msdyn\_paymentdaylines</span></span>      | <span data-ttu-id="b2423-150">เท็มเพลต [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) รวมข้อมูลอ้างอิงกำหนดการชำระเงินเข้าด้วยกัน สำหรับลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="b2423-151">CDS จำนวนวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b2423-151">Payment days CDS</span></span>            | <span data-ttu-id="b2423-152">msdyn\_paymentdays</span><span class="sxs-lookup"><span data-stu-id="b2423-152">msdyn\_paymentdays</span></span>          | <span data-ttu-id="b2423-153">เท็มเพลต [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) รวมข้่อมูลอ้างอิงวันชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2423-154">เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b2423-154">Terms of payment</span></span>            | <span data-ttu-id="b2423-155">msdyn\_paymentterms</span><span class="sxs-lookup"><span data-stu-id="b2423-155">msdyn\_paymentterms</span></span>         | <span data-ttu-id="b2423-156">เท็มเพลต [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) รวมข้อมูลอ้างอิงเงื่อนไขการชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2423-157">ส่วนเพิ่มของชื่อ</span><span class="sxs-lookup"><span data-stu-id="b2423-157">Name affixes</span></span>                | <span data-ttu-id="b2423-158">msdyn\_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="b2423-158">msdyn\_nameaffixes</span></span>          | <span data-ttu-id="b2423-159">เท็มเพลต [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) รวมข้อมูลอ้างอิงส่วนเพิ่มของชื่อเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b2423-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]