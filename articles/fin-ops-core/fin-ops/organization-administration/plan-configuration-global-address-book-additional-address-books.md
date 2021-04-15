---
title: แผนงานสำหรับสมุดที่อยู่สากลและสมุดที่อยู่อื่นๆ
description: หัวข้อนี้อธิบายข้อควรพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการการวางแผน
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d3a476a183453f170dae9b812949822ea60edd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747620"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="5e555-103">แผนงานสำหรับค่าสมุดที่อยู่สากลและสมุดที่อยู่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5e555-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e555-104">หัวข้อนี้อธิบายการพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผน ก่อนที่คุณจะตั้งค่าและตั้งค่าคอนฟิกสมุดที่อยู่สากลและสมุดที่อยู่เพิ่มเติมใดๆ</span><span class="sxs-lookup"><span data-stu-id="5e555-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="5e555-105">การตัดสินใจบางอย่างจะต้องให้คุณยืนยันการตัดสินใจสำหรับพื้นที่อื่นๆ ของผลิตภัณฑ์ เช่นลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5e555-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="5e555-106">สมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="5e555-106">Global address book</span></span>

<span data-ttu-id="5e555-107">ก่อนที่คุณจะเริ่มการทำงานกับสมุดที่อยู่สากล คุณต้องกำหนดค่าเริ่มต้นเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="5e555-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="5e555-108">ค่าเริ่มต้นเหล่านี้ใช้สำหรับสมุดรายชื่อเพิ่มเติมใด ๆ ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5e555-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="5e555-109">**การตัดสินใจ**</span><span class="sxs-lookup"><span data-stu-id="5e555-109">**Decisions**</span></span>

- <span data-ttu-id="5e555-110">ลำดับใดที่ควรมีชื่อแสดงในเรกคอร์ดฝ่ายในประเภท **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="5e555-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="5e555-111">ตัวอย่างเช่น ลำดับหนึ่งคือ นามสกุล ชื่อกลาง ชื่อ</span><span class="sxs-lookup"><span data-stu-id="5e555-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="5e555-112">เรกคอร์ดฝ่ายควรลบออกจากสมุดอยู่เมื่อลบเรกคอร์ดบทบาทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e555-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="5e555-113">ตัวอย่างเช่น ถ้าลบเรกคอร์ดลูกค้า เรกคอร์ดฝ่ายควรถูกลบด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e555-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="5e555-114">เมื่อสร้างเรกคอร์ดใหม่ ผู้ใช้ควรได้รับการแจ้งหากพบเรกคอร์ดที่ซ้ำกันในสมุดที่อยู่สากลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e555-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="5e555-115">ควรรวมระบบหมายเลขสากลข้อมูล (DUNS) ในข้อมูลของเรกคอร์ดฝ่ายหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="5e555-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="5e555-116">ถ้าหมายเลข DUNS ถูกรวมในเรกคอร์ดฝ่าย ควรตรวจสอบการไม่ซ้ำกันของหมายเลขหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e555-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="5e555-117">เมื่อสร้างเรกคอร์ดฝ่ายในสมุดที่อยู่สากล คุณต้องการค่าเริ่มต้นของชนิดฝ่าย บุคคล หรือองค์กรหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e555-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="5e555-118">บทบาทผู้ใช้ใดที่ควรมีสิทธิเข้าถึงที่อยู่ส่วนตัว และข้อมูลติดต่อของเรกคอร์ดฝ่าย</span><span class="sxs-lookup"><span data-stu-id="5e555-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="5e555-119">สมุดที่อยู่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5e555-119">Additional address books</span></span>

<span data-ttu-id="5e555-120">หลังจากที่คุณสร้างสมุดที่อยู่สากล คุณสามารถสร้างสมุดที่อยู่เพิ่มเติมตามที่คุณต้องการ เช่น สมุดที่อยู่ที่แยกต่างหาก สำหรับแต่ละบริษัทในองค์กรของคุณ หรือ สำหรับแต่ละสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5e555-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="5e555-121">ตัวอย่างเช่น Fabrikam คือ องค์กรระหว่างประเทศที่มีหลายบริษัทและหลายสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5e555-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="5e555-122">Fabrikam วางแผนจะสร้างสมุดอยู่สำหรับแต่ละสายงานของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5e555-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="5e555-123">สำหรับสายงานของธุรกิจที่เกิดขึ้นมากกว่าหนึ่งสถานที่ เช่นธุรกิจเครื่องมือนิวเมติกส์ Fabrikam วางแผนจะสร้างสมุดอยู่สำหรับสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="5e555-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="5e555-124">Chris ผู้จัดการฝ่าย IT ใน Fabrikam ได้สร้างสมุดที่อยู่ที่จำเป็นดังรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5e555-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="5e555-125">นอกจากนี้ รายการนี้ยังอธิบายเรกคอร์ดฝ่ายที่สมุดที่อยู่แต่ละเล่มต้องรวมอยู่</span><span class="sxs-lookup"><span data-stu-id="5e555-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="5e555-126">**สัญญาภาครัฐ (PubSC)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องในสัญญาของภาครัฐที่ Fabrikam มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5e555-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="5e555-127">**สัญญาภาคเอกชน (PriSC)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องในสัญญาของภาคเอกชนที่ Fabrikam มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5e555-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="5e555-128">**เครื่องมืออิเล็กทรอนิกส์ (อ)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมืออิเล็กทรอนิกส์ หรือฝ่ายที่ทำงานกับเครื่องมืออิเล็กทรอนิกส์ที่ที่จัดเตรียมไว้หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="5e555-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="5e555-129">**เครื่องมือ pneumatic (PTJPN)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมือ pneumatic หรือฝ่ายที่ทำงานกับเครื่องมือ pneumatic ที่ที่จัดเตรียมไว้หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="5e555-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="5e555-130">**เครื่องมือ pneumatic (PTUSA)** – เรกคอร์ดฝ่ายสำหรับทุกฝ่ายที่เกี่ยวข้องกับการซื้อหรือการขายเครื่องมือ pneumatic หรือฝ่ายที่ทำงานกับเครื่องมือ pneumatic ที่ที่จัดเตรียมไว้ หรือถูกซื้อสำหรับ Fabrikam ใน Fabrikam - บริษัทสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="5e555-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="5e555-131">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="5e555-131">**Decision:**</span></span>

- <span data-ttu-id="5e555-132">คุณจะสร้างสมุดที่อยู่เพิ่มเติมจำนวนเท่าไหร่</span><span class="sxs-lookup"><span data-stu-id="5e555-132">How many additional address books will you create?</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]