--- 
title: "กำหนดฝ่ายใหม่"
description: "ในแผนกจะมีหน่วยปฏิบัติงานที่แสดงในพื้นที่ในการทำงานของธุรกิจนั้น เช่นการขายหรือการบัญชี "
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6dedddf305e303de5b284b34420cd0eda5170ed1
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="define-new-departments"></a><span data-ttu-id="8707f-103">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="8707f-103">Define new departments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8707f-104">ในแผนกจะมีหน่วยปฏิบัติงานที่แสดงในพื้นที่ในการทำงานของธุรกิจนั้น เช่นการขายหรือการบัญชี </span><span class="sxs-lookup"><span data-stu-id="8707f-104">Departments are operating units that represent a functional area of a business, such as sales or accounting.</span></span> <span data-ttu-id="8707f-105">หลายๆ บริษัทมีลำดับชั้นขององค์กรที่แสดงแผนกต่าง ๆ ภายในธุรกิจ </span><span class="sxs-lookup"><span data-stu-id="8707f-105">Many companies have organizational hierarchies that display the various departments within a business.</span></span> <span data-ttu-id="8707f-106">ขั้นตอนนี้นำไปสู่ขั้นตอนการสร้างแผนก และเพิ่มแผนกเหล่านั้นอยู่ในลำดับชั้นขององค์กร </span><span class="sxs-lookup"><span data-stu-id="8707f-106">This procedure walks through the process of creating departments, and adding those departments to an organizations departmental hierarchy.</span></span> <span data-ttu-id="8707f-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8707f-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8707f-108">ไปที่ ทรัพยากรบุคคล > แผนก > แผนก</span><span class="sxs-lookup"><span data-stu-id="8707f-108">Go to Human resources > Departments > Departments.</span></span>
2. <span data-ttu-id="8707f-109">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="8707f-109">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="8707f-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="8707f-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8707f-111">ตัวอย่าง: โครงการ/กฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="8707f-111">Example: Project billing</span></span>  
4. <span data-ttu-id="8707f-112">ในฟิลด์บันทึก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8707f-112">In the Memo field, type a value.</span></span>
    * <span data-ttu-id="8707f-113">ตัวอย่าง: โครงการ/กฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="8707f-113">Example: Project billing</span></span>  
5. <span data-ttu-id="8707f-114">ในฟิลด์ผู้จัดการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8707f-114">In the Manager field, enter or select a value.</span></span>
    * <span data-ttu-id="8707f-115">ตัวอย่าง: Jodi Christiansen</span><span class="sxs-lookup"><span data-stu-id="8707f-115">Example: Jodi Christiansen</span></span>  
6. <span data-ttu-id="8707f-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8707f-116">Click Save.</span></span>
7. <span data-ttu-id="8707f-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8707f-117">Close the page.</span></span>
8. <span data-ttu-id="8707f-118">ไปที่ ทรัพยากรบุคคล > แผนก > ลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="8707f-118">Go to Human resources > Departments > Department hierarchy.</span></span>
9. <span data-ttu-id="8707f-119">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="8707f-119">Click Edit.</span></span>
10. <span data-ttu-id="8707f-120">คลิก แทรก</span><span class="sxs-lookup"><span data-stu-id="8707f-120">Click Insert.</span></span>
11. <span data-ttu-id="8707f-121">คลิกแผนก</span><span class="sxs-lookup"><span data-stu-id="8707f-121">Click Department.</span></span>
12. <span data-ttu-id="8707f-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8707f-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8707f-123">ตัวอย่าง: โครงการ/กฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="8707f-123">Example: Project billing</span></span>  
13. <span data-ttu-id="8707f-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8707f-124">Click OK.</span></span>
14. <span data-ttu-id="8707f-125">คลิกที่เผยแพร่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="8707f-125">Click Publish to open the drop dialog.</span></span>
15. <span data-ttu-id="8707f-126">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8707f-126">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="8707f-127">เมื่อมีการเผยแพร่ลำดับชั้นของแผนก คุณสามารถเลือกให้การเปลี่ยนแปลงนั้นมีผลบังคับใช้ </span><span class="sxs-lookup"><span data-stu-id="8707f-127">When publishing the department hierarchy, you can select when to make the changes effective.</span></span> <span data-ttu-id="8707f-128">การเปลี่ยนแปลงอาจเป็นวันที่ในอนาคต </span><span class="sxs-lookup"><span data-stu-id="8707f-128">Changes can be future dated.</span></span> <span data-ttu-id="8707f-129">ตัวอย่างเช่น คุณอาจทราบว่า คุณจะสามารถเพิ่มแผนกเพิ่มเติมในช่วงแรกของปีบัญชี </span><span class="sxs-lookup"><span data-stu-id="8707f-129">For example, you may know that at the beginning of your fiscal year you will be adding an additional department.</span></span> <span data-ttu-id="8707f-130">คุณสามารถตั้งค่าวันที่มีผลบังคับใช้ให้เป็นจุดเริ่มต้นของปีบัญชี และการเปลี่ยนแปลงกับลำดับชั้นจะมีผลบังคับใช้ในวันนั้น</span><span class="sxs-lookup"><span data-stu-id="8707f-130">You can set your effective date to the beginning of the fiscal year, and the changes to the hierarchy will be effective on that date.</span></span>  
16. <span data-ttu-id="8707f-131">ในฟิลด์อธิบายการเปลี่ยนแปลง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8707f-131">In the Describe changes field, type a value.</span></span>
17. <span data-ttu-id="8707f-132">คลิกที่เผยแพร่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8707f-132">Click Publish.</span></span>


