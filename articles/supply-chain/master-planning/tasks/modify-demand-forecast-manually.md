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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca6b881bc094b68d1bbf8c7c20b65418e42b28e3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835892"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="71e8c-103">แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="71e8c-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71e8c-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="71e8c-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="71e8c-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="71e8c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71e8c-106">การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต </span><span class="sxs-lookup"><span data-stu-id="71e8c-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="71e8c-107">แก้ไขการคาดการณ์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="71e8c-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="71e8c-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="71e8c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="71e8c-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="71e8c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71e8c-110">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="71e8c-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="71e8c-111">ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001</span><span class="sxs-lookup"><span data-stu-id="71e8c-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="71e8c-112">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="71e8c-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="71e8c-113">คลิก การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="71e8c-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="71e8c-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="71e8c-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="71e8c-115">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดย</span><span class="sxs-lookup"><span data-stu-id="71e8c-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="71e8c-116">การคลิกสร้างบนแถบแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="71e8c-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="71e8c-117">ในฟิลด์ปริมาณการขาย ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="71e8c-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="71e8c-118">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="71e8c-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="71e8c-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="71e8c-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="71e8c-120">แก้ไขการคาดการณ์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="71e8c-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="71e8c-121">คลิกเปิดใน Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="71e8c-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="71e8c-122">คลิกแก้ไขการคาดการณ์ความต้องการใน Excel </span><span class="sxs-lookup"><span data-stu-id="71e8c-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="71e8c-123">ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้ </span><span class="sxs-lookup"><span data-stu-id="71e8c-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="71e8c-124">ถ้าคุณไม่สามารถดูข้อมูลใน Excel ได้ คุณต้องลงชื่อเข้าใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise edition ด้วยตัวเลือก "คงการลงชื่อเข้าใช้ของฉันไว้" ที่เปิดใช้งานและคุณต้องเชื่อแอปการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="71e8c-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

