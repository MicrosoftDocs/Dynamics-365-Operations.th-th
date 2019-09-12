---
title: สร้างกลุ่มสิทธิ์ของ POS
description: หัวข้อนี้อธิบายวิธีการสร้างกลุ่มสิทธิ์ของ POS
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914845"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="75370-103">สร้างกลุ่มสิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="75370-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="75370-104">หัวข้อนี้อธิบายวิธีการสร้างกลุ่มสิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="75370-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="75370-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="75370-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="75370-106">งานนี้มีไว้สำหรับบทบาทผู้จัดการการดำเนินงานขายปลีก</span><span class="sxs-lookup"><span data-stu-id="75370-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="75370-107">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การขายปลีก > พนักงาน > กลุ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="75370-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="75370-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="75370-108">Select **New**.</span></span>
3. <span data-ttu-id="75370-109">ในฟิลด์ **รหัสกลุ่มสิทธิ์ของ POS** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75370-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="75370-110">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75370-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="75370-111">เลือก **ใช่** ในฟิลด์ **ดูรายการของนาฬิกาตอกบัตร**</span><span class="sxs-lookup"><span data-stu-id="75370-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="75370-112">ขณะนี้คุณสามารถเปิดใช้งานหรือปิดใช้งานสิทธิ์ต่างๆ สำหรับกลุ่มสิทธิ์ของ POS ของคุณ </span><span class="sxs-lookup"><span data-stu-id="75370-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="75370-113">สำหรับบางสิทธิ์คุณสามารถตั้งค่าที่จะใช้เพื่อประเมินว่าผู้ใช้ POS สามารถดำเนินการได้หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="75370-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="75370-114">คำแนะนำของงานนี้เปิดใช้งานสิทธิ์ส่วนหนึ่งที่อาจโอนให้กับพนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="75370-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="75370-115">เลือก **ใช่** ในฟิลด์ **อนุญาตให้สร้างใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="75370-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="75370-116">เลือก **ใช่** ในฟิลด์ **อนุญาตให้แก้ไขใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="75370-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="75370-117">เลือก **ใช่** ในฟิลด์ **อนุญาตให้ดึงข้อมูลใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="75370-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="75370-118">เลือก **ใช่** ในฟิลด์ **อนุญาตให้เปลี่ยนแปลงรหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="75370-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="75370-119">เลือก **ใช่** ในฟิลด์ **อนุญาตให้ปิดซ่อน**</span><span class="sxs-lookup"><span data-stu-id="75370-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="75370-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="75370-120">Select **Save**.</span></span> <span data-ttu-id="75370-121">หลังจากที่มีบันทึกการเปลี่ยนแปลง คุณต้องรันกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="75370-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="75370-122">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > ทรัพยากรบุคคล > งาน > งาน**</span><span class="sxs-lookup"><span data-stu-id="75370-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="75370-123">ถัดไป เราจะกำหนดกลุ่มสิทธิ์ของ POS ให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="75370-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="75370-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="75370-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="75370-125">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="75370-125">Select **Edit**.</span></span>
15. <span data-ttu-id="75370-126">ขยายส่วน **การจัดประเภทงาน**</span><span class="sxs-lookup"><span data-stu-id="75370-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="75370-127">ในฟิลด์สิทธิ์ของ POS ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75370-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="75370-128">ผู้ปฏิบัติงานทั้งหมดในตำแหน่งงานนี้จะใช้การตั้งค่าของกลุ่มสิทธิ์ของ POS ยกเว้นว่ามีการแทนสิทธิ์ของ POS ของผู้ปฏิบัติงานในระดับของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="75370-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="75370-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="75370-129">Select **Save**.</span></span> <span data-ttu-id="75370-130">หลังจากที่มีบันทึกการเปลี่ยนแปลง คุณต้องรันกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="75370-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

