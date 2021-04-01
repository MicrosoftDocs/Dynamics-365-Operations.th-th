---
title: แก้ไขการคาดการณ์ความต้องการด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า '
author: ShylaThompson
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31c057d686edc97a11027f156b9c14ff453294ec
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240400"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="98b78-103">แก้ไขการคาดการณ์ความต้องการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="98b78-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98b78-104">กระบวนงานนี้แสดงวิธีการแก้ไขการคาดการณ์สำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="98b78-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="98b78-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="98b78-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="98b78-106">การบันทึกนี้มีไว้สำหรับผู้วางแผนการผลิต </span><span class="sxs-lookup"><span data-stu-id="98b78-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="98b78-107">แก้ไขการคาดการณ์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="98b78-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="98b78-108">ใน **บานหน้าต่างนำทาง** ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="98b78-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="98b78-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="98b78-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="98b78-110">เลือกสินค้าที่คุณต้องการแก้ไขการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="98b78-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="98b78-111">ตัวอย่างเช่น คุณสามารถเลือกสินค้า D0001</span><span class="sxs-lookup"><span data-stu-id="98b78-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="98b78-112">ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="98b78-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="98b78-113">คลิก **การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="98b78-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="98b78-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="98b78-114">In the list, mark the selected row.</span></span> <span data-ttu-id="98b78-115">ถ้าไม่มีรายการการคาดการณ์ สร้างรายการใหม่โดยคลิกสร้างบนแถบแอป</span><span class="sxs-lookup"><span data-stu-id="98b78-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="98b78-116">ในฟิลด์ **ปริมาณการขาย** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="98b78-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="98b78-117">ตัวเลขนี้จะแสดงถึงปริมาณที่คาดการณ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="98b78-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="98b78-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="98b78-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="98b78-119">แก้ไขการคาดการณ์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="98b78-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="98b78-120">คลิก **เปิด** ใน Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="98b78-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="98b78-121">คลิก **แก้ไขการคาดการณ์ความต้องการ** ใน Excel</span><span class="sxs-lookup"><span data-stu-id="98b78-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="98b78-122">ใน Excel คุณสามารถเพิ่ม ลบ และแก้ไขบรรทัดการคาดการณ์ความต้องการได้ </span><span class="sxs-lookup"><span data-stu-id="98b78-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="98b78-123">ถ้าคุณไม่สามารถดูข้อมูลใน Excel คุณจำเป็นต้องลงชื่อเข้าใช้ด้วยการเปิดใช้งานตัวเลือก "ให้ฉันลงชื่อเข้าใช้เสมอ" และคุณจำเป็นต้องเชื่อแอพลิเคชันการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="98b78-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]