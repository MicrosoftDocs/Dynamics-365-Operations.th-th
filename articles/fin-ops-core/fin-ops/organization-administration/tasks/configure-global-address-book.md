---
title: ตั้งค่าคอนฟิกสมุดที่อยู่สากล
description: 'ใช้กระบวนงานนี้เพื่อตั้งค่าเริ่มต้นและนโยบายความปลอดภัยสำหรับสมุดที่อยู่สากล '
author: msftbrking
manager: AnnBe
ms.date: 07/23/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirParameters
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f31804b3988af44bad0cba28e8226e625d32148b
ms.sourcegitcommit: 7a855deed9f95ca2589f38db214890464b2b9061
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/13/2020
ms.locfileid: "2951243"
---
# <a name="configure-the-global-address-book"></a><span data-ttu-id="8c83f-103">ตั้งค่าคอนฟิกสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="8c83f-103">Configure the global address book</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c83f-104">ใช้กระบวนงานนี้เพื่อตั้งค่าเริ่มต้นและนโยบายความปลอดภัยสำหรับสมุดที่อยู่สากล </span><span class="sxs-lookup"><span data-stu-id="8c83f-104">Use this procedure to set the default values and security policies for the global address book.</span></span> 

<span data-ttu-id="8c83f-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8c83f-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8c83f-106">งานนี้มีไว้สำหรับทีมการวางแผนและการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="8c83f-106">This task is intended for the Planning and configuration team.</span></span>

1. <span data-ttu-id="8c83f-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการองค์กร > สมุดที่อยู่สากล > พารามิเตอร์ของสมุดที่อยู่สากล**</span><span class="sxs-lookup"><span data-stu-id="8c83f-107">In the Navigation pane, go to **Modules > Organization administration > Global address book > Global address book parameters**.</span></span>
2. <span data-ttu-id="8c83f-108">ในฟิลด์ **ลำดับชื่อ** ให้เลือกวิธีการแสดงชื่อ</span><span class="sxs-lookup"><span data-stu-id="8c83f-108">In the **Name sequence** field, select how names should be shown.</span></span>
3. <span data-ttu-id="8c83f-109">ใน **ลบฝ่ายโดยไม่มีบทบาท** ให้เลือกว่าจะลบฝ่ายที่ยังไม่ได้กำหนดบทบาทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8c83f-109">In **Delete parties with no roles**, select whether to delete parties with that have not been assigned a role.</span></span>
4. <span data-ttu-id="8c83f-110">ใน **ใช้การตรวจสอบข้อมูลซ้ำ** ให้เลือกว่าจะตรวจสอบเรกคอร์ดซ้ำหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8c83f-110">In **Use duplicate check**, select whether to check for duplicate records.</span></span>
5. <span data-ttu-id="8c83f-111">ใน **แสดงหมายเลข DUNS ในที่อยู่** ให้เลือกว่าจะแสดงหมายเลข DUNS ในที่อยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8c83f-111">In **Display DUNS number on addresses**, select whether to display the DUNS number on addresses.</span></span>
6. <span data-ttu-id="8c83f-112">ใน **ตรวจสอบหมายเลข DUNS เฉพาะ** ให้เลือกว่าจะตรวจสอบหมายเลข DUNS เฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8c83f-112">In **Check for unique DUNS number**, select whether to check for unique DUNS numbers.</span></span>
7. <span data-ttu-id="8c83f-113">ในฟิลด์ **ฝ่าย** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-113">In the **Party** field, select an option.</span></span>
8. <span data-ttu-id="8c83f-114">ในฟิลด์ **ลูกค้า** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-114">In the **Customer** field, select an option.</span></span>
9. <span data-ttu-id="8c83f-115">ในฟิลด์ **ผู้จัดจำหน่าย** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-115">In the **Vendor** field, select an option.</span></span>
10. <span data-ttu-id="8c83f-116">ในฟิลด์ **ผู้ที่มีแนวโน้มจะเป็นลูกค้า** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-116">In the **Prospect** field, select an option.</span></span>
11. <span data-ttu-id="8c83f-117">ในฟิลด์ **คู่แข่ง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-117">In the **Competitor** field, select an option.</span></span>
12. <span data-ttu-id="8c83f-118">คลิกแท็บ **ความปลอดภัยของที่ตั้งส่วนตัว**</span><span class="sxs-lookup"><span data-stu-id="8c83f-118">Click the **Private location security** tab.</span></span>
13. <span data-ttu-id="8c83f-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8c83f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="8c83f-120">กดคีย์ Shift เพื่อเลือกหลายบทบาทที่จะเพิ่มไปที่บานหน้าต่าง **บทบาทที่เลือก** และจากนั้น ให้คลิกลูกศรเพื่อเพิ่มบทบาทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8c83f-120">Press the Shift key to select multiple roles to add to the **Selected roles** pane and then click the arrow to add the selected roles.</span></span>  
14. <span data-ttu-id="8c83f-121">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8c83f-121">Click **Save**.</span></span>

