---
title: แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง
description: 'กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465401"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="c11f2-103">แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c11f2-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="c11f2-104">กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="c11f2-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="c11f2-105">ความสัมพันธ์การรายงานที่สามารถใช้สำหรับเอกสารการกำหนดเส้นทางโดยใช้ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="c11f2-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="c11f2-106">กระบวนงานยังแสดงวิธีการกำหนดพนักงานให้กับลำดับชั้นเพิ่มเติมอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="c11f2-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="c11f2-107">ตัวอย่างเช่น พนักงานอาจจะเป็นส่วนหนึ่งของทีมโครงการที่มีความสัมพันธ์การรายงานแบบไม่เป็นทางการกับหัวหน้างานโครงการ </span><span class="sxs-lookup"><span data-stu-id="c11f2-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="c11f2-108">คุณสามารถกำหนดความสัมพันธ์การรายงานเพิ่มเติมในตำแหน่งเพื่อรองรับโครงการหรือเมตริกซ์สถานการณ์ต่างๆ </span><span class="sxs-lookup"><span data-stu-id="c11f2-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="c11f2-109">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c11f2-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c11f2-110">ไปที่ทรัพยากรบุคคล > ตำแหน่ง > ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c11f2-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="c11f2-111">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="c11f2-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c11f2-112">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ตำแหน่งด้วยค่า '000091'</span><span class="sxs-lookup"><span data-stu-id="c11f2-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="c11f2-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c11f2-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c11f2-114">ขยายส่วนรายงานไปยังตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c11f2-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="c11f2-115">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c11f2-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c11f2-116">ในฟิลด์รายงานไปยัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c11f2-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="c11f2-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c11f2-117">Click Create.</span></span>
8. <span data-ttu-id="c11f2-118">ขยายส่วนความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="c11f2-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="c11f2-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="c11f2-119">Click Add.</span></span>
10. <span data-ttu-id="c11f2-120">เลือกกล่องกาเครื่องหมายทางซ้ายมือของกริด</span><span class="sxs-lookup"><span data-stu-id="c11f2-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="c11f2-121">ในฟิลด์ชื่อลำดับชั้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c11f2-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="c11f2-122">ตัวอย่าง: โครงการ</span><span class="sxs-lookup"><span data-stu-id="c11f2-122">Example: Project</span></span>  
12. <span data-ttu-id="c11f2-123">ในฟิลด์รายงานไปยังตำแหน่ง ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="c11f2-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="c11f2-124">ตัวอย่าง:  000437</span><span class="sxs-lookup"><span data-stu-id="c11f2-124">Example:  000437</span></span>
13. <span data-ttu-id="c11f2-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c11f2-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]