--- 
title: "แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง"
description: "กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน "
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 32d32cc969548168ce736b18918ce86d9965c4a5
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="841f3-103">แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="841f3-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="841f3-104">กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="841f3-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="841f3-105">ความสัมพันธ์การรายงานที่สามารถใช้สำหรับเอกสารการกำหนดเส้นทางโดยใช้ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="841f3-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="841f3-106">กระบวนงานยังแสดงวิธีการกำหนดพนักงานให้กับลำดับชั้นเพิ่มเติมอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="841f3-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="841f3-107">ตัวอย่างเช่น พนักงานอาจจะเป็นส่วนหนึ่งของทีมโครงการที่มีความสัมพันธ์การรายงานแบบไม่เป็นทางการกับหัวหน้างานโครงการ </span><span class="sxs-lookup"><span data-stu-id="841f3-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="841f3-108">คุณสามารถกำหนดความสัมพันธ์การรายงานเพิ่มเติมในตำแหน่งเพื่อรองรับโครงการหรือเมตริกซ์สถานการณ์ต่างๆ </span><span class="sxs-lookup"><span data-stu-id="841f3-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="841f3-109">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="841f3-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="841f3-110">ไปที่ทรัพยากรบุคคล > ตำแหน่ง > ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="841f3-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="841f3-111">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="841f3-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="841f3-112">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ตำแหน่งด้วยค่า '000091'</span><span class="sxs-lookup"><span data-stu-id="841f3-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="841f3-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="841f3-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="841f3-114">ขยายส่วนรายงานไปยังตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="841f3-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="841f3-115">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="841f3-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="841f3-116">ในฟิลด์รายงานไปยัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="841f3-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="841f3-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="841f3-117">Click Create.</span></span>
8. <span data-ttu-id="841f3-118">ขยายส่วนความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="841f3-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="841f3-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="841f3-119">Click Add.</span></span>
10. <span data-ttu-id="841f3-120">เลือกกล่องกาเครื่องหมายทางซ้ายมือของกริด</span><span class="sxs-lookup"><span data-stu-id="841f3-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="841f3-121">ในฟิลด์ชื่อลำดับชั้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="841f3-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="841f3-122">ตัวอย่าง: โครงการ</span><span class="sxs-lookup"><span data-stu-id="841f3-122">Example: Project</span></span>  
12. <span data-ttu-id="841f3-123">ในฟิลด์รายงานไปยังตำแหน่ง ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="841f3-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="841f3-124">ตัวอย่าง:  000437</span><span class="sxs-lookup"><span data-stu-id="841f3-124">Example:  000437</span></span>
13. <span data-ttu-id="841f3-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="841f3-125">Click Save.</span></span>


