---
title: ข้อมูลหลักของลูกค้าแบบรวม
description: ในหัวข้อนี้อธิบายการรวมข้อมูลลูกค้าระหว่าง Finance and Operations กับ Dataverse
author: RamaKrishnamoorthy
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
ms.openlocfilehash: 0015ca2ccbb0098a5a96bf56ff355fb2f9f8f626
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748934"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="c2ae2-103">ข้อมูลหลักของลูกค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="c2ae2-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="c2ae2-104">ข้อมูลลูกค้าสามารถทำเป็นต้นฉบับได้ในแอพลิเคชัน Dynamics 365 มากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="c2ae2-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="c2ae2-105">ตัวอย่างเช่น แถวลูกค้าสามารถเริ่มต้นได้ผ่านทางกิจกรรมการขายใน Dynamics 365 Sales (แอปที่เป็นแบบโมเดลใน Dynamics 365) หรือแถวสามารถเริ่มต้นได้ผ่านทางกิจกรรมการขายปลีกใน Dynamics 365 Commerce (แอป Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="c2ae2-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="c2ae2-106">ไม่ว่าข้อมูลลูกค้าที่มีต้นกำเนิดมาจากที่ใดก็ตาม จะมีการรวมอยู่เบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="c2ae2-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="c2ae2-107">ข้อมูลหลักของลูกค้าแบบรวมช่วยให้คุณมีความยืดหยุ่นในการเข้าถึงข้อมูลลูกค้าในแอพลิเคชัน Dynamics 365 และให้มุมมองที่ครอบคลุมของลูกค้าทั่วทั้งชุดแอพลิเคชัน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c2ae2-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="c2ae2-108">โฟลว์ข้อมูลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-108">Customer data flow</span></span>

<span data-ttu-id="c2ae2-109">*ลูกค้า* เป็นแนวคิดที่กำหนดไว้อย่างดีในแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="c2ae2-110">ดังนั้น การรวมของข้อมูลลูกค้าก็เกี่ยวข้องกับความสอดคล้องแนวคิดของลูกค้าระหว่างสองแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="c2ae2-111">ภาพประกอบต่อไปนี้แสดงโฟลว์ข้อมูลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-111">The following illustration shows the customer data flow.</span></span>

![โฟลว์ข้อมูลของลูกค้า](media/dual-write-customer-data-flow.png)

<span data-ttu-id="c2ae2-113">ลูกค้าสามารถแบ่งออกย่างกว้างๆ ได้เป็นสองประเภท: ลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c2ae2-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="c2ae2-114">ลูกค้าสองประเภทนี้ถูกจัดเก็บและจัดการแตกต่างกันไปใน Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="c2ae2-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="c2ae2-115">ใน Finance and Operations ทั้งลูกค้าเชิงพาณิชย์ / องค์กรและผู้บริโภค / ผู้ใช้จะเชี่ยวชาญในตารางเดียวที่มีชื่อว่า **CustTable** (CustCustomerV3Entity) และจะถูกแบ่งออกตามแอตทริบิวต์ **ชนิด**</span><span class="sxs-lookup"><span data-stu-id="c2ae2-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="c2ae2-116">(ถ้า **ชนิด** ถูกตั้งค่าเป็น **องค์กร** ลูกค้าเป็นลูกค้าเชิงพาณิชย์/เชิงองค์กร และถ้ามีการตั้งค่า **ชนิด** เป็น **บุคคล** ลูกค้าเป็นผู้บริโภค/ผู้ใช้) ข้อมูลผู้ติดต่อหลักจะได้รับการจัดการผ่านตาราง SMMContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="c2ae2-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="c2ae2-117">ใน Dataverse ลูกค้าเชิงพาณิชย์/เชิงองค์กรมีความเชี่ยวชาญในตารางบัญชี และถูกระบุเป็นลูกค้า เมื่อมีการตั้งค่าแอททริบิวต์ **RelationshipType** เป็น **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="c2ae2-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="c2ae2-118">ทั้งผู้บริโภค/ผู้ใช้และผู้ติดต่อจะถูกแสดงโดยตารางผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="c2ae2-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="c2ae2-119">เพื่อให้การแยกที่ชัดเจนระหว่างผู้บริโภค/ผู้ใช้ และผู้ติดต่อ ตาราง **ผู้ติดต่อ** มีแฟล็กบูลีนที่มีชื่อว่า **Sellable**</span><span class="sxs-lookup"><span data-stu-id="c2ae2-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="c2ae2-120">เมื่อ **Sellable** เป็น **จริง** ผู้ติดต่อเป็นผู้บริโภค/ผู้ใช้ และสามารถสร้างใบเสนอราคาและใบสั่งสำหรับผู้ติดต่อนั้นได้</span><span class="sxs-lookup"><span data-stu-id="c2ae2-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="c2ae2-121">เมื่อ **Sellable** เป็น **เท็จ** ผู้ติดต่อเป็นเพียงผู้ติดต่อหลักของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="c2ae2-122">เมื่อผู้ติดต่อที่ไม่ใช่ Sellable มีส่วนร่วมในกระบวนการใบเสนอราคาหรือใบสั่ง **Sellable** ถูกตั้งค่าเป็น **จริง** เพื่อแฟล็กผู้ติดต่อเป็นผู้ติดต่อ Sellable</span><span class="sxs-lookup"><span data-stu-id="c2ae2-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="c2ae2-123">ผู้ติดต่อที่กลายเป็นผู้ติดต่อที่สามารถขายได้ยังคงเป็นผู้ติดต่อ Sellable</span><span class="sxs-lookup"><span data-stu-id="c2ae2-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="c2ae2-124">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="c2ae2-124">Templates</span></span>

<span data-ttu-id="c2ae2-125">ข้อมูลลูกค้ารวมถึงข้อมูลทั้งหมดเกี่ยวกับลูกค้า เช่น กลุ่มลูกค้า ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และสถานะบัตรสมาชิก</span><span class="sxs-lookup"><span data-stu-id="c2ae2-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="c2ae2-126">ชุดของแผนผังตารางทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c2ae2-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c2ae2-127">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c2ae2-127">Finance and Operations apps</span></span> | <span data-ttu-id="c2ae2-128">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c2ae2-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="c2ae2-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="c2ae2-130">ผู้ติดต่อ CDS V2</span><span class="sxs-lookup"><span data-stu-id="c2ae2-130">CDS Contacts V2</span></span>             | <span data-ttu-id="c2ae2-131">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="c2ae2-131">contacts</span></span>                        | <span data-ttu-id="c2ae2-132">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลการติดต่อหลัก ทุติยภูมิ และตติยภูมิสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-133">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-133">Customer groups</span></span>             | <span data-ttu-id="c2ae2-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="c2ae2-134">msdyn_customergroups</span></span>            | <span data-ttu-id="c2ae2-135">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="c2ae2-136">วิธีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c2ae2-136">Customer payment method</span></span>     | <span data-ttu-id="c2ae2-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="c2ae2-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="c2ae2-138">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="c2ae2-139">ลูกค้า V3</span><span class="sxs-lookup"><span data-stu-id="c2ae2-139">Customers V3</span></span>                | <span data-ttu-id="c2ae2-140">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c2ae2-140">accounts</span></span>                        | <span data-ttu-id="c2ae2-141">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับลูกค้าเชิงพาณิชย์และเชิงองค์กร</span><span class="sxs-lookup"><span data-stu-id="c2ae2-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="c2ae2-142">ลูกค้า V3</span><span class="sxs-lookup"><span data-stu-id="c2ae2-142">Customers V3</span></span>                | <span data-ttu-id="c2ae2-143">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="c2ae2-143">contacts</span></span>                        | <span data-ttu-id="c2ae2-144">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับผู้บริโภคและผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="c2ae2-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="c2ae2-145">ส่วนเพิ่มของชื่อ</span><span class="sxs-lookup"><span data-stu-id="c2ae2-145">Name affixes</span></span>                | <span data-ttu-id="c2ae2-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="c2ae2-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="c2ae2-147">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของส่วนเพิ่มของชื่อสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-148">รายการแสดงวันที่ในการชำระเงินของ CDS V2</span><span class="sxs-lookup"><span data-stu-id="c2ae2-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="c2ae2-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="c2ae2-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="c2ae2-150">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของบรรทัดวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-151">CDS จำนวนวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-151">Payment days CDS</span></span>            | <span data-ttu-id="c2ae2-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="c2ae2-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="c2ae2-153">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-154">รายการกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-154">Payment schedule lines</span></span>      | <span data-ttu-id="c2ae2-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="c2ae2-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="c2ae2-156">ซิงค์ข้อมูลอ้างอิงของบรรทัดกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-157">กำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-157">Payment schedule</span></span>            | <span data-ttu-id="c2ae2-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="c2ae2-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="c2ae2-159">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c2ae2-160">เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2ae2-160">Terms of payment</span></span>            | <span data-ttu-id="c2ae2-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="c2ae2-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="c2ae2-162">เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของเงื่อนไขการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c2ae2-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]