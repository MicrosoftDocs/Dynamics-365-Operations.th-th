---
title: สร้างงบประมาณการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการสร้างงบประมาณการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2aaba8794bf0025f0449509752e4f197d3bf3db4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889708"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="4e5ce-103">สร้างงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4e5ce-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="4e5ce-104">งบประมาณการบำรุงรักษาใช้เพื่อแสดงภาพรวมของต้นทุนที่คาดไว้สำหรับการบำรุงรักษาเชิงป้องกัน</span><span class="sxs-lookup"><span data-stu-id="4e5ce-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="4e5ce-105">รายการงบประมาณจะถูกคำนวณตามรายการกำหนดการบำรุงรักษาที่มีวันที่เริ่มต้นที่คาดไว้ระหว่างรอบระยะเวลางบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4e5ce-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="4e5ce-106">งบประมาณการบำรุงรักษาจะขึ้นอยู่กับชนิดของต้นทุนที่ใช้ในการจัดการสินทรัพย์ **เชิงป้องกัน** **การเเก้ไข** เเละ **การลงทุน**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="4e5ce-107">ต้นทุนตามงบประมาณสำหรับการบำรุงรักษาการลงทุนจะรวมอยู่ในสินทรัพย์ที่ใช้งานอยู่ ซึ่งมีวันที่เปลี่ยนทดเเทนในระหว่างรอบระยะเวลางบประมาณ และค่าการแทนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4e5ce-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="4e5ce-108">ต้นทุนตามงบประมาณสำหรับการรักษาเชิงแก้ไขจะถูกรวม หากวันที่เเก้ไขในอดีตถูกรวมอยู่ในการคำนวนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4e5ce-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="4e5ce-109">ในกรณีดังกล่าว ต้นทุนที่มีการเเก้ไขจากรอบระยะเวลาก่อนหน้าจะถูกคำนวณสำหรับรอบระยะเวลาเดียวกันในอนาคตที่คุณคำนวณงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4e5ce-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="4e5ce-110">สร้างงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4e5ce-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="4e5ce-111">เลือก **การจัดการสินทรัพย์** \> **การสอบถาม** \> **การบำรุงรักษางบประมาณ** \> **งบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="4e5ce-112">เลือก **สร้างงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="4e5ce-113">ในฟิลด์ **งบประมาณการบำรุงรักษา** ให้ป้อนรหัสงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4e5ce-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="4e5ce-114">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4e5ce-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="4e5ce-115">บนเเท็บด่วน **รอบระยะเวลา** ในฟิลด์ **วันที่เริ่มต้น** เเละ **วันที่สิ้นสุด** ป้อนวันเริ่มต้น และวันที่สิ้นสุดของรอบระยะเวลางบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4e5ce-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="4e5ce-116">เมื่อต้องการรวมต้นทุนงบประมาณเชิงแก้ไขซึ่งคำนวณตามข้อมูลพื้นฐานของต้นทุนจริงจากรอบระยะเวลาก่อนหน้า ในฟิลด์ **การเเก้ไขจากวันที่** ป้อนวันที่เริ่มต้นของรอบระยะเวลาที่ต้นทุนดังกล่าวควรถูกรวม</span><span class="sxs-lookup"><span data-stu-id="4e5ce-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="4e5ce-117">ทั้งนี้ขึ้นอยู่กับระดับของรายละเอียดที่จำเป็นในงบประมาณ กำหนดตัวเลือกที่เกี่ยวข้องบนห้า **กลุ่มโดย** เเท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="4e5ce-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="4e5ce-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-118">Select **OK**.</span></span>
8. <span data-ttu-id="4e5ce-119">เลือก **รายการงบประมาณ** ที่เปิดหน้า **รายการงบประมาณการบำรุงรักษา** ซึ่งคุณสามารถดูรายการงบประมาณทั้งหมดที่สร้างขึ้นสำหรับรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="4e5ce-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="4e5ce-120">ถ้าต้องการอนุมัติงบประมาณ เลือกหน้า **งบประมาณการบำรุงรักษา** เเละจากนั้น เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="4e5ce-121">จากนั่น ในกล่องโต้ตอบ **อนุมัติงบประมาณ** เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="4e5ce-122">ชื่อของคุณถูกป้อนใน **อนุมัติโดย** ฟิลด์บนหน้า **งบประมาณการบำรุงรักษา** </span><span class="sxs-lookup"><span data-stu-id="4e5ce-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4e5ce-123">หลังจากที่คุณได้อนุมัติงบประมาณการบำรุงรักษาแล้ว คุณจะไม่สามารถคำนวณใหม่ หรือปรับปรุงรายการที่เกี่ยวข้องบนหน้า **รายการงบประมาณการบำรุงรักษา** เว้นเเต่คุณจะลบการอนุมัติเป็นครั้งเเรก</span><span class="sxs-lookup"><span data-stu-id="4e5ce-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="4e5ce-124">ถ้าต้องการลบการอนุมัติของงบประมาณการบำรุงรักษา เลือกบนหน้า **งบประมาณการบำรุงรักษา** เเละจากนั้น เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="4e5ce-125">จากนั่น ในกล่องโต้ตอบ **อนุมัติงบประมาณ** เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![งบประมาณการบำรุงรักษา](media/01-maintenance-budgets.png)

<span data-ttu-id="4e5ce-127">คุณยังสามารถสร้างงบประมาณการบำรุงรักษาใหม่ได้โดยการคัดลอกงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4e5ce-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="4e5ce-128">บนหน้า **งบประมาณการบำรุงรักษา** เลือก งบประมาณเพื่อคัดลอก เเละจากนั้น เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="4e5ce-129">วิธีการนี้มีประโยชน์ ตัวอย่างเช่น ถ้าคุณได้สร้างงบประมาณเป็นเวลาหนึ่งเดือน เเละต้องการคัดลอกงบประมาณไปยังอีกเดือนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4e5ce-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="4e5ce-130">งบประมาณการบำรุงรักษาจะคำนวณเฉพาะต้นทุนงบประมาณตามรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4e5ce-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="4e5ce-131">เมื่อต้องการคำนวณต้นทุนจริงสำหรับรอบระยะเวลาเดียวกัน คุณสามารถทำการคำนวณบนหน้า **การควบคุมต้นทุนสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="4e5ce-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
