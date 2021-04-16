---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า '
author: ShylaThompson
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 518a49441a9d73d9da5ab90400e0b7482692d374
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829677"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="77338-103">แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="77338-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77338-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="77338-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="77338-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="77338-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="77338-106">การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต </span><span class="sxs-lookup"><span data-stu-id="77338-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="77338-107">แก้ไขการคาดการณ์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="77338-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="77338-108">ใน **บานหน้าต่างนำทาง** ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="77338-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="77338-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77338-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="77338-110">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="77338-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="77338-111">ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001</span><span class="sxs-lookup"><span data-stu-id="77338-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="77338-112">ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="77338-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="77338-113">คลิก **การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="77338-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="77338-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="77338-114">In the list, mark the selected row.</span></span> <span data-ttu-id="77338-115">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดยคลิกสร้างบนแถบแอป</span><span class="sxs-lookup"><span data-stu-id="77338-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="77338-116">ในฟิลด์ **ปริมาณการขาย** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="77338-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="77338-117">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="77338-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="77338-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="77338-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="77338-119">แก้ไขการคาดการณ์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="77338-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="77338-120">คลิก **เปิด** ใน Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="77338-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="77338-121">คลิก **แก้ไขการคาดการณ์ความต้องการ** ใน Excel</span><span class="sxs-lookup"><span data-stu-id="77338-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="77338-122">ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้ </span><span class="sxs-lookup"><span data-stu-id="77338-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="77338-123">ถ้าคุณไม่สามารถดูข้อมูลใน Excel คุณจำเป็นต้องลงชื่อเข้าใช้ด้วยการเปิดใช้งานตัวเลือก "ให้ฉันลงชื่อเข้าใช้เสมอ" และคุณจำเป็นต้องเชื่อแอพลิเคชันการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="77338-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]