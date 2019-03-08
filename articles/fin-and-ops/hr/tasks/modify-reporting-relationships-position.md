---
title: แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง
description: 'กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน '
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e779a337ff8f8e0199a60e094f4bec9eba49e701
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "322708"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="9fb4e-103">แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fb4e-104">กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="9fb4e-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="9fb4e-105">ความสัมพันธ์การรายงานที่สามารถใช้สำหรับเอกสารการกำหนดเส้นทางโดยใช้ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="9fb4e-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="9fb4e-106">กระบวนงานยังแสดงวิธีการกำหนดพนักงานให้กับลำดับชั้นเพิ่มเติมอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="9fb4e-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="9fb4e-107">ตัวอย่างเช่น พนักงานอาจจะเป็นส่วนหนึ่งของทีมโครงการที่มีความสัมพันธ์การรายงานแบบไม่เป็นทางการกับหัวหน้างานโครงการ </span><span class="sxs-lookup"><span data-stu-id="9fb4e-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="9fb4e-108">คุณสามารถกำหนดความสัมพันธ์การรายงานเพิ่มเติมในตำแหน่งเพื่อรองรับโครงการหรือเมตริกซ์สถานการณ์ต่างๆ </span><span class="sxs-lookup"><span data-stu-id="9fb4e-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="9fb4e-109">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="9fb4e-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="9fb4e-110">ไปที่ทรัพยากรบุคคล > ตำแหน่ง > ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="9fb4e-111">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="9fb4e-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9fb4e-112">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ตำแหน่งด้วยค่า '000091'</span><span class="sxs-lookup"><span data-stu-id="9fb4e-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="9fb4e-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9fb4e-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9fb4e-114">ขยายส่วนรายงานไปยังตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="9fb4e-115">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="9fb4e-116">ในฟิลด์รายงานไปยัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9fb4e-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="9fb4e-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-117">Click Create.</span></span>
8. <span data-ttu-id="9fb4e-118">ขยายส่วนความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="9fb4e-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="9fb4e-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9fb4e-119">Click Add.</span></span>
10. <span data-ttu-id="9fb4e-120">เลือกกล่องกาเครื่องหมายทางซ้ายมือของกริด</span><span class="sxs-lookup"><span data-stu-id="9fb4e-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="9fb4e-121">ในฟิลด์ชื่อลำดับชั้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9fb4e-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="9fb4e-122">ตัวอย่าง: โครงการ</span><span class="sxs-lookup"><span data-stu-id="9fb4e-122">Example: Project</span></span>  
12. <span data-ttu-id="9fb4e-123">ในฟิลด์รายงานไปยังตำแหน่ง ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="9fb4e-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="9fb4e-124">ตัวอย่าง:  000437</span><span class="sxs-lookup"><span data-stu-id="9fb4e-124">Example:  000437</span></span>
13. <span data-ttu-id="9fb4e-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9fb4e-125">Click Save.</span></span>

