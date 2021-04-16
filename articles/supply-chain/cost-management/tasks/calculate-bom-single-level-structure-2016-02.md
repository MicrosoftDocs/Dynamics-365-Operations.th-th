---
title: คำนวณ BOM โดยใช้โครงสร้างระดับเดียว (กุมภาพันธ์ 2016)
description: กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายระดับเดียวจากในแผ่นงานการคิดต้นทุน
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821404"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="fb234-103">คำนวณ BOM โดยใช้โครงสร้างระดับเดียว (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="fb234-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb234-104">กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายระดับเดียวจากในแผ่นงานการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fb234-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="fb234-105">นี่คืองานที่หกในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="fb234-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="fb234-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="fb234-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="fb234-107">ไปที่ผลิตภัณฑ์ที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="fb234-107">Go to Released products.</span></span>
2. <span data-ttu-id="fb234-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fb234-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fb234-109">เลือก ผลิตภัณฑ์ BOM_1</span><span class="sxs-lookup"><span data-stu-id="fb234-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="fb234-110">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fb234-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="fb234-111">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="fb234-111">Click Item price.</span></span>
5. <span data-ttu-id="fb234-112">คลิก คำนวณต้นทุนสินค้า</span><span class="sxs-lookup"><span data-stu-id="fb234-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="fb234-113">คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="fb234-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="fb234-114">ในฟิลด์เวอร์ชันการคิดต้นทุน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fb234-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fb234-115">สำหรับการสาธิตนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="fb234-115">For this demo, select 10.</span></span> <span data-ttu-id="fb234-116">นี่คือเวอร์ชันการคิดต้นทุนเดียวกันซึ่งใช้สำหรับการเพิ่มราคาต้นทุนไปยังส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="fb234-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="fb234-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fb234-117">Click OK.</span></span>
8. <span data-ttu-id="fb234-118">คลิกดูรายละเอียดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb234-118">Click View calculation details.</span></span>
    * <span data-ttu-id="fb234-119">คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="fb234-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="fb234-120">นี่คือส่วนประกอบของต้นทุน:  \*    10 ได้รับมาจาก ITEM_A 10 จาก ITEM_B 10 จาก BOM_2</span><span class="sxs-lookup"><span data-stu-id="fb234-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="fb234-121">ในกรณีนี้ ไม่มีรายละเอียดสำหรับ BOM_2 เนื่องจากมีการป้อนเป็นต้นทุนมาตรฐานของ 10 แต่ไม่ได้ดำเนินการโดยใช้การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb234-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="fb234-122">\*    7 ได้รับมาจากเวลาเซ็ตอัพ ซึ่งเป็นต้นทุนคงที่ และอีก 7 ได้รับมาจากการดำเนินงานเวลาที่ใช้ในการผลิต (กระบวนการ)</span><span class="sxs-lookup"><span data-stu-id="fb234-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="fb234-123">\*    นอกจากนี้ยังมียอดเงินอื่นๆ ที่เกี่ยวข้องกับต้นทุนทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="fb234-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="fb234-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="fb234-124">@SysTaskRecorder:_RequestClose</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]