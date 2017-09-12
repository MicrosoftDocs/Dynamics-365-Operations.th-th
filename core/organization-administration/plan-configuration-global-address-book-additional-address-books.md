---
title: "ตั้งค่าคอนฟิกสมุดที่อยู่สากล"
description: "บทความนี้อธิบายถึงการพิจารณาและตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะตั้งค่าคอนฟิกกระบวนการวางแผนงบประมาณและสมุดที่อยู่เพิ่มเติมใน Microsoft Dynamics 365 for Finance and Operations การตัดสินใจบางอย่างจะต้องให้คุณยืนยันการตัดสินใจสำหรับพื้นที่อื่นๆ ของผลิตภัณฑ์ เช่นลำดับชั้นขององค์กร"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: c71d54d311f7e2b9afdfb3af5ebee490c60ee4bf
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="configure-global-address-books"></a><span data-ttu-id="fd6b3-104">ตั้งค่าคอนฟิกสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="fd6b3-104">Configure global address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fd6b3-105">บทความนี้อธิบายถึงการพิจารณาและตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะตั้งค่าคอนฟิกกระบวนการวางแผนงบประมาณและสมุดที่อยู่เพิ่มเติมใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fd6b3-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fd6b3-106">การตัดสินใจบางอย่างจะต้องให้คุณยืนยันการตัดสินใจสำหรับพื้นที่อื่นๆ ของผลิตภัณฑ์ เช่นลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="fd6b3-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="fd6b3-107">สมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="fd6b3-107">Global address book</span></span>
-------------------

<span data-ttu-id="fd6b3-108">ก่อนที่คุณจะเริ่มการทำงานกับสมุดที่อยู่สากล คุณต้องกำหนดค่าเริ่มต้นเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="fd6b3-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="fd6b3-109">ค่าเริ่มต้นเหล่านี้ใช้สำหรับสมุดรายชื่อเพิ่มเติมใด ๆ ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd6b3-109">These default values are then used for any additional address books that you create.</span></span> <span data-ttu-id="fd6b3-110">**การตัดสินใจ**</span><span class="sxs-lookup"><span data-stu-id="fd6b3-110">**Decisions:**</span></span>

-   <span data-ttu-id="fd6b3-111">ลำดับใดที่ควรมีชื่อแสดงในเรกคอร์ดฝ่ายในประเภท **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="fd6b3-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="fd6b3-112">ตัวอย่างเช่น ลำดับหนึ่งคือ นามสกุล ชื่อกลาง ชื่อ</span><span class="sxs-lookup"><span data-stu-id="fd6b3-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="fd6b3-113">เรกคอร์ดฝ่ายควรลบออกจากสมุดอยู่เมื่อลบเรกคอร์ดบทบาทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="fd6b3-114">ตัวอย่างเช่น ถ้าลบเรกคอร์ดลูกค้า เรกคอร์ดฝ่ายควรถูกลบด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="fd6b3-115">เมื่อสร้างเรกคอร์ดใหม่ ผู้ใช้ควรได้รับการแจ้งหากพบเรกคอร์ดที่ซ้ำกันในสมุดที่อยู่สากลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="fd6b3-116">ควรรวมระบบหมายเลขสากลข้อมูล (DUNS) ในข้อมูลของเรกคอร์ดฝ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="fd6b3-117">ถ้าหมายเลข DUNS ถูกรวมในเรกคอร์ดฝ่าย ควรตรวจสอบการไม่ซ้ำกันของหมายเลขหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="fd6b3-118">เมื่อสร้างเรกคอร์ดฝ่ายในสมุดที่อยู่สากล คุณต้องการค่าเริ่มต้นของชนิดฝ่าย บุคคล หรือองค์กรหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="fd6b3-119">บทบาทผู้ใช้ใดที่ควรมีสิทธิเข้าถึงที่อยู่ส่วนตัว และข้อมูลติดต่อของเรกคอร์ดฝ่าย</span><span class="sxs-lookup"><span data-stu-id="fd6b3-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="fd6b3-120">สมุดที่อยู่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd6b3-120">Additional address books</span></span>
<span data-ttu-id="fd6b3-121">หลังจากที่คุณสร้างสมุดที่อยู่สากล คุณสามารถสร้างสมุดที่อยู่เพิ่มเติมตามที่คุณต้องการ เช่น สมุดที่อยู่ที่แยกต่างหาก สำหรับแต่ละบริษัทในองค์กรของคุณ หรือ สำหรับแต่ละสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fd6b3-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="fd6b3-122">ตัวอย่างเช่น Fabrikam คือ องค์กรระหว่างประเทศที่มีหลายบริษัทและหลายสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fd6b3-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="fd6b3-123">Fabrikam วางแผนจะสร้างสมุดอยู่สำหรับแต่ละสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fd6b3-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="fd6b3-124">สำหรับสายงานของธุรกิจที่เกิดขึ้นมากกว่าหนึ่งสถานที่ เช่นธุรกิจเครื่องมือนิวเมติกส์ Fabrikam วางแผนจะสร้างสมุดอยู่สำหรับสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="fd6b3-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="fd6b3-125">Chris ผู้จัดการฝ่าย IT ใน Fabrikam ได้สร้างสมุดที่อยู่ที่จำเป็นดังรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fd6b3-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="fd6b3-126">นอกจากนี้ รายการนี้ยังอธิบายเรกคอร์ดฝ่ายที่สมุดที่อยู่แต่ละเล่มต้องรวม</span><span class="sxs-lookup"><span data-stu-id="fd6b3-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="fd6b3-127">**สัญญาภาครัฐ (PubSC)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องในสัญญาของภาครัฐที่ Fabrikam มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="fd6b3-128">**สัญญาภาคเอกชน (PriSC)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องในสัญญาของภาคเอกชนที่ Fabrikam มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="fd6b3-129">**เครื่องมืออิเล็กทรอนิกส์ (อ)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมืออิเล็กทรอนิกส์ หรือฝ่ายที่ทำงานกับเครื่องมืออิเล็กทรอนิกส์ที่ที่จัดเตรียมไว้หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="fd6b3-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="fd6b3-130">**เครื่องมือ pneumatic (PTJPN)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมือ pneumatic หรือฝ่ายที่ทำงานกับเครื่องมือ pneumatic ที่ที่จัดเตรียมไว้หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="fd6b3-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="fd6b3-131">**เครื่องมือ pneumatic (PTUSA)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมือ pneumatic หรือฝ่ายที่ทำงานกับเครื่องมือ pneumatic ที่ที่จัดเตรียมไว้ หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="fd6b3-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="fd6b3-132">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="fd6b3-132">**Decision:**</span></span>

-   <span data-ttu-id="fd6b3-133">คุณจะสร้างสมุดที่อยู่เพิ่มเติมจำนวนเท่าไหร่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="fd6b3-134">การรักษาความปลอดภัยสมุดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-134">Address book security</span></span>

<span data-ttu-id="fd6b3-135">คุณสามารถสร้างสมุดที่อยู่ได้ตลอดเวลา และคุณยังสามารถตั้งค่าพารามิเตอร์ความปลอดภัยสำหรับสมุดที่อยู่ได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="fd6b3-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="fd6b3-136">คุณไม่จำเป็นในการตั้งค่าสิทธิ์ความปลอดภัยสำหรับสมุดอยู่ แต่ถ้าคุณไม่ตั้งค่า พนักงานทั้งหมดในองค์กรของคุณจะสามารถดูเรกคอร์ดฝ่ายทั้งหมดในสมุดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="fd6b3-137">คุณสามารถตั้งค่าสิทธิ์ความปลอดภัยให้กับเรกคอร์ดฝ่ายโดยใช้สมุดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="fd6b3-138">สิทธิ์ความปลอดภัยจะขึ้นอยู่กับทีมงาน</span><span class="sxs-lookup"><span data-stu-id="fd6b3-138">Security privileges are based on teams.</span></span> <span data-ttu-id="fd6b3-139">วิธีการนี้รับรองว่า เฉพาะผู้ปฏิบัติงานที่ถูกกำหนดให้เป็นทีมงานเท่านั้นจึงมีสิทธิ์เข้าถึงสมุดอยู่ สามารถดูเรกคอร์ดฝ่ายในสมุดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="fd6b3-140">คุณต้องเลือกทีมงานที่มีการเข้าถึงแต่ละสมุดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fd6b3-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="fd6b3-141">สำหรับแต่ละสมุดที่อยู่ คุณสามารถตั้งค่าสิทธิ์ความปลอดภัยที่อนุญาต หรือปฏิเสธการเข้าถึงทีมงานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="fd6b3-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="fd6b3-142">ถ้าคุณอนุญาตให้สิทธิ์ทีมงานในสมุดอยู่ สมาชิกทั้งหมดของทีมงานนั้นจะสามารถดูเรกคอร์ดในสมุดที่อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="fd6b3-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="fd6b3-143">ถ้าคุณไม่อนุญาตให้สิทธิ์ทีมงานในสมุดอยู่ สมาชิกทั้งหมดของทีมงานนั้นจะไม่สามารถดูสมุดที่อยู่หรือเนื้อหาในสมุดที่อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="fd6b3-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> <span data-ttu-id="fd6b3-144">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="fd6b3-144">**Decision:**</span></span>

-   <span data-ttu-id="fd6b3-145">ทีมงานใดที่ควรมีสิทธิเข้าถึงแต่ละสมุดที่อยู่ใหม่ที่คุณจะสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd6b3-145">Which teams should have access to each new address book that you will create?</span></span>





