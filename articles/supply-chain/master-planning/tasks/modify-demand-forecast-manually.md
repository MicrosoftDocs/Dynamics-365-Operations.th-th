---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: หัวข้อนี้อธิบายวิธีการแก้ไขการคาดการณ์สำหรับสินค้า
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889035"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="a32bc-103">แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a32bc-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a32bc-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="a32bc-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="a32bc-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="a32bc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a32bc-106">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="a32bc-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="a32bc-107">แก้ไขการคาดการณ์สำหรับสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a32bc-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="a32bc-108">หากต้องการแก้ไขการคาดการณ์สำหรับสินค้าที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="a32bc-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="a32bc-109">ไปยัง **โมดูล \> การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a32bc-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a32bc-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a32bc-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="a32bc-111">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="a32bc-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="a32bc-112">บนบานหน้าต่างการ เปิดแท็บ **แผน** และเลือก **การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a32bc-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="a32bc-113">ในรายการ ให้เลือกแถว</span><span class="sxs-lookup"><span data-stu-id="a32bc-113">In the list, select a row.</span></span> <span data-ttu-id="a32bc-114">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดยเลือก **สร้าง** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a32bc-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="a32bc-115">ในฟิลด์ **ปริมาณการขาย** ให้ป้อนตัวเลขค่าบวก</span><span class="sxs-lookup"><span data-stu-id="a32bc-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="a32bc-116">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="a32bc-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="a32bc-117">ข้อผิดพลาดจะแสดงขึ้นถ้าคุณป้อนตัวเลขค่าลบ</span><span class="sxs-lookup"><span data-stu-id="a32bc-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="a32bc-118">กรอกข้อมูลในฟิลด์อื่น ๆ ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a32bc-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="a32bc-119">เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a32bc-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="a32bc-120">แก้ไขการคาดการณ์ของสินค้า Microsoft Excel หนึ่งรายการหรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="a32bc-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="a32bc-121">หากต้องการแก้ไขการคาดการณ์ของสินค้า Microsoft Excel หนึ่งรายการหรือมากกว่า:</span><span class="sxs-lookup"><span data-stu-id="a32bc-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="a32bc-122">ดำเนินการตามข้อใดข้อหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a32bc-122">Do one of the following:</span></span>
    - <span data-ttu-id="a32bc-123">เปิดหน้า **การคาดการณ์ความต้องการ** ของสินค้าใด ๆ (ไม่ว่าสินค้าใด) ตามที่อธิบายไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a32bc-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="a32bc-124">ไปยัง **การวางแผนหลัก \> การคาดการณ์ \> รายการการคาดการณ์ด้วยตนเอง \> รายการการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a32bc-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="a32bc-125">บนบานหน้าต่างการ เลือก **เปิดใน Microsoft Office \> รายการการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a32bc-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="a32bc-126">เลือกที่ตั้งการดาวน์โหลด บันทึก แล้วเปิดไฟล์ที่ดาวน์โหลดใน Excel</span><span class="sxs-lookup"><span data-stu-id="a32bc-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="a32bc-127">ถ้าคุณเห็นคําเตือน ให้เลือกเพื่อ **เปิดใช้งานการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a32bc-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="a32bc-128">ใน Excel เข้าสู่ระบบ Supply Chain Management โดยใช้บานหน้าต่างงาน Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="a32bc-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="a32bc-129">คุณต้องเข้าสู่ระบบด้วยตัวเลือก **ให้ฉันลงชื่อเข้าใช้เสมอ** และคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a32bc-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="a32bc-130">ขณะนี้ แผ่นตาราง Excel จะแสดงรายการการคาดการณ์ความต้องการปัจจุบันทั้งหมดของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="a32bc-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="a32bc-131">เพิ่ม ลบ และแก้ไขรายการการคาดการณ์ความต้องการได้</span><span class="sxs-lookup"><span data-stu-id="a32bc-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="a32bc-132">เลือก **เผยแพร่** ในบานหน้าต่างงาน Microsoft Dynamics เพื่ออัปโหลดการเปลี่ยนแปลงของคุณกลับไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a32bc-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
