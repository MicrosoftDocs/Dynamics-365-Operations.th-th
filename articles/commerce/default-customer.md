---
title: สร้างลูกค้าเริ่มต้น
description: หัวข้อนี้อธิบายวิธีสร้างลูกค้าเริ่มต้นเพื่อใช้เมื่อสร้างช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799190"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="6b4cb-103">สร้างลูกค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6b4cb-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b4cb-104">หัวข้อนี้อธิบายวิธีสร้างลูกค้าเริ่มต้นเพื่อใช้เมื่อสร้างช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6b4cb-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b4cb-105">เมื่อสร้างช่องทาง คุณจะต้องระบุลูกค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6b4cb-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="6b4cb-106">ลูกค้าเริ่มต้นสามารถสร้างได้อย่างง่ายดายหลังจากสร้างกลุ่มลูกค้าและสมุดรายชื่อลูกค้าครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="6b4cb-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="6b4cb-107">การสร้างกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-107">Create a customer group</span></span>

<span data-ttu-id="6b4cb-108">หากยังไม่มีกลุ่มลูกค้าอยู่ คุณสามารถสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="6b4cb-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="6b4cb-109">ตัวอย่างอาจเป็นกลุ่มเพื่อเป็นตัวแทนกลุ่มลูกค้าที่แตกต่างกัน เช่น การขายส่ง การขายปลีก อินเทอร์เน็ต พนักงาน ฯลฯ</span><span class="sxs-lookup"><span data-stu-id="6b4cb-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="6b4cb-110">ทำตามขั้นตอนเหล่านี้เพื่อสร้างกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="6b4cb-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ลูกค้า \> กลุ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="6b4cb-112">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b4cb-113">ในกล่อง **กลุ่มลูกค้า** ป้อนรหัสสำหรับกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="6b4cb-114">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายที่เหมาะสมลงไป</span><span class="sxs-lookup"><span data-stu-id="6b4cb-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="6b4cb-115">ในกล่อง **เงื่อนไขการชำระเงิน** ป้อนค่าที่เหมาะสมลงไป</span><span class="sxs-lookup"><span data-stu-id="6b4cb-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6b4cb-116">ในกล่อง **เวลาระหว่างวันที่ครบกำหนดชำระของใบแจ้งหนี้และวันที่ชำระเงิน** ป้อนค่าที่เหมาะสมลงไป</span><span class="sxs-lookup"><span data-stu-id="6b4cb-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6b4cb-117">ในกล่อง **กลุ่มภาษีเริ่มต้น** ป้อนกลุ่มภาษีลงไปหากเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6b4cb-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="6b4cb-118">เลือกกล่องกาเครื่องหมาย **ราคารวมภาษีการขาย** หากเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6b4cb-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="6b4cb-119">ในกล่อง **เหตุผลการตัดค่าเริ่มต้น** ป้อนค่าที่เหมาะสมลงไปหากเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6b4cb-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="6b4cb-120">รูปภาพต่อไปนี้แสดงกลุ่มลูกค้าที่กำหนดค่าต่างๆไว้</span><span class="sxs-lookup"><span data-stu-id="6b4cb-120">The following image shows several configured customer groups.</span></span>

![กลุ่มลูกค้า](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="6b4cb-122">สร้างสมุดรายชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-122">Create a customer address book</span></span>

<span data-ttu-id="6b4cb-123">ลูกค้าจำเป็นต้องสัมพันธ์กับสมุดรายชื่อ</span><span class="sxs-lookup"><span data-stu-id="6b4cb-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="6b4cb-124">ถ้ายังไม่ได้ถูกสร้าง คุณจะต้องสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6b4cb-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="6b4cb-125">ทำตามขั้นตอนเหล่านี้เพื่อสร้างสมุดรายชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="6b4cb-126">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> สมุดรายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="6b4cb-127">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b4cb-128">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="6b4cb-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="6b4cb-129">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="6b4cb-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="6b4cb-130">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6b4cb-131">ภาพต่อไปนี้แสดงตัวอย่างของสมุดรายชื่อ</span><span class="sxs-lookup"><span data-stu-id="6b4cb-131">The following image shows an example address book.</span></span>

![สมุดที่อยู่](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;6b4cb-133&quot;>สร้างลูกค้าเริ่มต้น</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b4cb-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;6b4cb-134&quot;>ทำตามขั้นตอนเหล่านี้เพื่อสร้างลูกค้าเริ่มต้น</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b4cb-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;6b4cb-135&quot;>ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b4cb-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;6b4cb-136&quot;>บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b4cb-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;6b4cb-137&quot;>ในรายการแบบหล่นลง **ชนิด** ให้เลือก &quot;บุคคล&quot;</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b4cb-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;6b4cb-138&quot;>ในรายการแบบหล่นลง **บัญชีของลูกค้า** เลือกหรือป้อนหมายเลขลูกค้าองค์กร (ตัวอย่างเช่น &quot;100001")</span><span class="sxs-lookup"><span data-stu-id="6b4cb-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="6b4cb-139">ในรายการแบบหล่นลง **ชื่อ** เลือกหรือป้อนชื่อ (ตัวอย่างเช่น "ค่าเริ่มต้น")</span><span class="sxs-lookup"><span data-stu-id="6b4cb-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="6b4cb-140">ในรายการแบบหล่นลง **ชื่อกลาง** เลือกหรือป้อนชื่อ (ตัวอย่างเช่น "การขายปลีก")</span><span class="sxs-lookup"><span data-stu-id="6b4cb-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="6b4cb-141">ในรายการแบบหล่นลง **นามสกุล** เลือกหรือป้อนชื่อ (ตัวอย่างเช่น "ลูกค้า")</span><span class="sxs-lookup"><span data-stu-id="6b4cb-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="6b4cb-142">ในรายการแบบหล่นลง **สกุลเงิน** เลือกหรือป้อนสกุลเงิน (ตัวอย่างเช่น "USD")</span><span class="sxs-lookup"><span data-stu-id="6b4cb-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="6b4cb-143">ในรายการแบบหล่นลง **สกุลเงิน** เลือกกลุ่มลูกค้าที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6b4cb-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="6b4cb-144">ในรายการแบบหล่นลง **สมุดรายชื่อ** เลือกสมุดรายชื่อลูกค้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6b4cb-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="6b4cb-145">เลือก **บันทึก** เพื่อบันทึกและกลับไปยังหน้าจอรายละเอียดลูกค้าสำหรับลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="6b4cb-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="6b4cb-146">ไม่จำเป็นต้องเพิ่มที่อยู่สำหรับลูกค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6b4cb-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="6b4cb-147">ภาพต่อไปนี้แสดงตัวอย่างของการสร้างลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-147">The following image shows an example of customer creation.</span></span>

![การสร้างลูกค้าเริ่มต้น](media/default-customer-creation.png)

<span data-ttu-id="6b4cb-149">ภาพต่อไปนี้แสดงตัวอย่างของการกำหนดค่าลูกค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6b4cb-149">The following image shows a default customer configuration.</span></span>

![ตัวอย่างการกำหนดค่าลูกค้า](media/default-customer-configuration1.png)

<span data-ttu-id="6b4cb-151">ค่าเริ่มต้นส่วนใหญ่ในหน้าจอรายละเอียดลูกค้าสามารถคงไว้ได้ แต่ควรเปลี่ยนค่าสองค่า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="6b4cb-152">บนหน้าจอรายละเอียดลูกค้า ให้ขยาย **ค่าเริ่มต้นใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="6b4cb-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="6b4cb-153">ในรายการแบบหล่นลง **ไซต์** เลือกหรือป้อนไซต์ที่กำหนดค่าไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="6b4cb-154">ในรายการแบบหล่นลง **คลังสินค้า** และเลือกหรือป้อนคลังสินค้าที่กำหนดค่าไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="6b4cb-155">ภาพต่อไปนี้แสดงตัวอย่างของการกำหนดค่าลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6b4cb-155">The following image shows an example customer configuration.</span></span>

![ตัวอย่างการกำหนดค่าลูกค้า](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="6b4cb-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6b4cb-157">Additional resources</span></span>

[<span data-ttu-id="6b4cb-158">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6b4cb-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6b4cb-159">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6b4cb-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
