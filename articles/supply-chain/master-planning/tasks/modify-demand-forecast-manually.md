---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "323605"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="c0d6e-103">แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c0d6e-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0d6e-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="c0d6e-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="c0d6e-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c0d6e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c0d6e-106">การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต </span><span class="sxs-lookup"><span data-stu-id="c0d6e-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="c0d6e-107">แก้ไขการคาดการณ์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c0d6e-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="c0d6e-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="c0d6e-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c0d6e-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c0d6e-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c0d6e-110">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="c0d6e-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="c0d6e-111">ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001</span><span class="sxs-lookup"><span data-stu-id="c0d6e-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="c0d6e-112">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="c0d6e-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="c0d6e-113">คลิก การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="c0d6e-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="c0d6e-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c0d6e-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c0d6e-115">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดย</span><span class="sxs-lookup"><span data-stu-id="c0d6e-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="c0d6e-116">การคลิกสร้างบนแถบแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c0d6e-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="c0d6e-117">ในฟิลด์ปริมาณการขาย ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="c0d6e-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="c0d6e-118">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="c0d6e-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="c0d6e-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c0d6e-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="c0d6e-120">แก้ไขการคาดการณ์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="c0d6e-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="c0d6e-121">คลิกเปิดใน Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="c0d6e-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="c0d6e-122">คลิกแก้ไขการคาดการณ์ความต้องการใน Excel </span><span class="sxs-lookup"><span data-stu-id="c0d6e-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="c0d6e-123">ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้ </span><span class="sxs-lookup"><span data-stu-id="c0d6e-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="c0d6e-124">ถ้าคุณไม่สามารถดูข้อมูลใน Excel ได้ คุณต้องลงชื่อเข้าใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise edition ด้วยตัวเลือก "คงการลงชื่อเข้าใช้ของฉันไว้" ที่เปิดใช้งานและคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c0d6e-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

