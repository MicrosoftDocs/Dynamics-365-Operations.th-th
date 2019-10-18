---
title: การเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ถาวรหลายรายการ
description: 'งานนี้อัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มสินทรัพย์ถาวรที่ระบุ '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180130"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="c474b-103">การเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ถาวรหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c474b-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c474b-104">งานนี้อัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มสินทรัพย์ถาวรที่ระบุ </span><span class="sxs-lookup"><span data-stu-id="c474b-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="c474b-105">คู่มือของงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="c474b-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="c474b-106">ไปที่สินทรัพย์ถาวร > งานประจำงวด > การอัพเดตโดยรวม</span><span class="sxs-lookup"><span data-stu-id="c474b-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="c474b-107">ในฟิลด์สมุดบัญชีค่าเสื่อมราคา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c474b-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c474b-108">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c474b-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c474b-109">ในฟิลด์การเริ่มต้นการใช้งาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c474b-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="c474b-110">ในฟิลด์การสิ้นสุดการใช้งาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c474b-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="c474b-111">เฉพาะสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีค่าเสื่อมราคาที่คุณเลือกและที่ได้เสนอในบริการระหว่างวันที่ดังกล่าวจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="c474b-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="c474b-112">ในฟิลด์แบบแผนการคิดค่าเสื่อมราคาปัจจุบัน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c474b-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c474b-113">จะมีการอัพเดตเฉพาะสินทรัพย์ที่มีแบบแผนการคิดค่าเสื่อมราคาปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c474b-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="c474b-114">ในฟิลด์แบบแผนการคิดค่าเสื่อมราคาใหม่ ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c474b-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c474b-115">ตรวจสอบรายงานที่จะพิมพ์ไปยังปลายทางที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c474b-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="c474b-116">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="c474b-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="c474b-117">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="c474b-117">Click Filter.</span></span>
10. <span data-ttu-id="c474b-118">ในรายการ ให้เลือกกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="c474b-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="c474b-119">ในฟิลด์เงื่อนไข ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c474b-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c474b-120">เลือกกลุ่มสินทรัพย์ถาวรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c474b-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="c474b-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c474b-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c474b-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c474b-122">Click OK.</span></span>
15. <span data-ttu-id="c474b-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c474b-123">Click OK.</span></span>
    *  <span data-ttu-id="c474b-124">ผลลัพธ์ของกระบวนจะปรากฏบนรายงานการอัพเดตโดยรวม</span><span class="sxs-lookup"><span data-stu-id="c474b-124">Results of the process are shown on the Mass update report.</span></span>     

