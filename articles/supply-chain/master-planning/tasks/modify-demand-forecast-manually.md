---
title: 'คู่มือ: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224021"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="1602d-103">คู่มือ: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1602d-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1602d-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="1602d-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="1602d-105">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="1602d-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="1602d-106">แก้ไขการคาดการณ์สำหรับสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1602d-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="1602d-107">หากต้องการแก้ไขการคาดการณ์สำหรับสินค้าที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="1602d-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="1602d-108">ไปยัง **โมดูล \> การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="1602d-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1602d-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1602d-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="1602d-110">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="1602d-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="1602d-111">บนบานหน้าต่างการ เปิดแท็บ **แผน** และเลือก **การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="1602d-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="1602d-112">ในรายการ ให้เลือกแถว</span><span class="sxs-lookup"><span data-stu-id="1602d-112">In the list, select a row.</span></span> <span data-ttu-id="1602d-113">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดยเลือก **สร้าง** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1602d-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="1602d-114">ในฟิลด์ **ปริมาณการขาย** ให้ป้อนตัวเลขค่าบวก</span><span class="sxs-lookup"><span data-stu-id="1602d-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="1602d-115">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="1602d-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="1602d-116">ข้อผิดพลาดจะแสดงขึ้นถ้าคุณป้อนตัวเลขค่าลบ</span><span class="sxs-lookup"><span data-stu-id="1602d-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="1602d-117">กรอกข้อมูลในฟิลด์อื่น ๆ ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="1602d-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="1602d-118">เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1602d-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="1602d-119">แก้ไขการคาดการณ์ของสินค้าด้วย Microsoft Excel หนึ่งรายการหรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="1602d-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="1602d-120">หากต้องการแก้ไขการคาดการณ์ของสินค้าด้วย Microsoft Excel หนึ่งรายการหรือมากกว่า:</span><span class="sxs-lookup"><span data-stu-id="1602d-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="1602d-121">ดำเนินการตามข้อใดข้อหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1602d-121">Do one of the following:</span></span>
    - <span data-ttu-id="1602d-122">เปิดหน้า **การคาดการณ์ความต้องการ** ของสินค้าใด ๆ (ไม่ว่าสินค้าใด) ตามที่อธิบายไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1602d-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="1602d-123">ไปยัง **การวางแผนหลัก \> การคาดการณ์ \> รายการการคาดการณ์ด้วยตนเอง \> รายการการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="1602d-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="1602d-124">บนบานหน้าต่างการ เลือก **เปิดใน Microsoft Office \> รายการการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="1602d-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="1602d-125">เลือกที่ตั้งการดาวน์โหลด บันทึก แล้วเปิดไฟล์ที่ดาวน์โหลดใน Excel</span><span class="sxs-lookup"><span data-stu-id="1602d-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="1602d-126">ถ้าคุณเห็นคําเตือน ให้เลือกเพื่อ **เปิดใช้งานการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1602d-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="1602d-127">ใน Excel เข้าสู่ระบบ Supply Chain Management โดยใช้บานหน้าต่างงาน Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="1602d-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="1602d-128">คุณต้องเข้าสู่ระบบด้วยตัวเลือก **ให้ฉันลงชื่อเข้าใช้เสมอ** และคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1602d-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="1602d-129">ขณะนี้ แผ่นตาราง Excel จะแสดงรายการการคาดการณ์ความต้องการปัจจุบันทั้งหมดของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="1602d-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="1602d-130">เพิ่ม ลบ และแก้ไขรายการการคาดการณ์ความต้องการได้</span><span class="sxs-lookup"><span data-stu-id="1602d-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="1602d-131">เลือก **เผยแพร่** ในบานหน้าต่างงาน Microsoft Dynamics เพื่ออัปโหลดการเปลี่ยนแปลงของคุณกลับไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1602d-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
