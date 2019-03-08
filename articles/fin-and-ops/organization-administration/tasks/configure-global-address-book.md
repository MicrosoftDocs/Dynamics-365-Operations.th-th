---
title: ตั้งค่าคอนฟิกสมุดที่อยู่สากล
description: 'ใช้กระบวนงานนี้เพื่อตั้งค่าเริ่มต้นและนโยบายความปลอดภัยสำหรับสมุดที่อยู่สากล '
author: kfend
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 230d3c089189ddb6186bc2ca4b647b8ad5b003ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "328826"
---
# <a name="configure-the-global-address-book"></a><span data-ttu-id="6ce58-103">ตั้งค่าคอนฟิกสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="6ce58-103">Configure the global address book</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ce58-104">ใช้กระบวนงานนี้เพื่อตั้งค่าเริ่มต้นและนโยบายความปลอดภัยสำหรับสมุดที่อยู่สากล </span><span class="sxs-lookup"><span data-stu-id="6ce58-104">Use this procedure to set the default values and security policies for the global address book.</span></span> 

<span data-ttu-id="6ce58-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6ce58-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6ce58-106">งานนี้มีไว้สำหรับทีมการวางแผนและการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ce58-106">This task is intended for the Planning and configuration team.</span></span>

1. <span data-ttu-id="6ce58-107">ไปที่การจัดการองค์กร > สมุดที่อยู่สากล > พารามิเตอร์ของสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="6ce58-107">Go to Organization administration > Global address book > Global address book parameters.</span></span>
2. <span data-ttu-id="6ce58-108">ในฟิลด์ลำดับชื่อ ให้เลือกวิธีการแสดงชื่อ</span><span class="sxs-lookup"><span data-stu-id="6ce58-108">In the Name sequence field, select how names should be shown.</span></span>
3. <span data-ttu-id="6ce58-109">เลือกว่าจะลบฝ่ายที่ไม่ได้ถูกกำหนดบทบาทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6ce58-109">Select whether to delete parties with that have not been assigned a role.</span></span>
4. <span data-ttu-id="6ce58-110">เลือกว่าจะตรวจสอบเรกคอร์ดที่ซ้ำกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6ce58-110">Select whether to check for duplicate records.</span></span>
5. <span data-ttu-id="6ce58-111">เลือกว่าจะแสดงหมายเลข DUNS ในที่อยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6ce58-111">Select whether to display the DUNS number on addresses.</span></span>
6. <span data-ttu-id="6ce58-112">เลือกว่าจะตรวจสอบหมายเลข DUNS ที่ไม่ซ้ำกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6ce58-112">Select whether to check for unique DUNS numbers.</span></span>
7. <span data-ttu-id="6ce58-113">ในฟิลด์ฝ่าย ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-113">In the Party field, select an option.</span></span>
8. <span data-ttu-id="6ce58-114">ในฟิลด์ลูกค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-114">In the Customer field, select an option.</span></span>
9. <span data-ttu-id="6ce58-115">ในฟิลด์ผู้จัดจำหน่าย ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-115">In the Vendor field, select an option.</span></span>
10. <span data-ttu-id="6ce58-116">ในฟิลด์ผู้ที่มีแนวโน้มจะเป็นลูกค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-116">In the Prospect field, select an option.</span></span>
11. <span data-ttu-id="6ce58-117">ในฟิลด์คู่แข่ง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-117">In the Competitor field, select an option.</span></span>
12. <span data-ttu-id="6ce58-118">คลิกแท็บความปลอดภัยของที่ตั้งส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="6ce58-118">Click the Private location security tab.</span></span>
13. <span data-ttu-id="6ce58-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6ce58-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6ce58-120">กดคีย์ Shift เพื่อเลือกหลายบทบาทที่จะเพิ่มไปที่บานหน้าต่างบทบาทที่เลือก และจากนั้นให้คลิกลูกศรเพื่อเพิ่มบทบาทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6ce58-120">Press the Shift key to select multiple roles to add to the Selected roles pane and then click the arrow to add the selected roles.</span></span>  
14. <span data-ttu-id="6ce58-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ce58-121">Click Save.</span></span>

