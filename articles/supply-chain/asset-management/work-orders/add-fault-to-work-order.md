---
title: เพิ่มข้อบกพร่องลงในใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการเพิ่มการลงทะเบียนข้อบกพร่องให้กับใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 083ceca9605ad044c172ba7aa23739d170f8c301
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019315"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="7016b-103">เพิ่มข้อบกพร่องลงในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7016b-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7016b-104">คุณสามารถเพิ่มข้อบกพร่องที่มีการตั้งค่าไว้ในโปรแกรมออกแบบข้อบกพร่องไปยังใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7016b-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="7016b-105">หนึ่งเรกคอร์ดข้อบกพร่องหรือมากกว่าต้องมีการเชื่อมต่อไปยังชนิดสินทรัพย์ที่ใช้สำหรับสินทรัพย์ที่เลือกในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7016b-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="7016b-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่า ดูที่ [การจัดการข้อบกพร่อง](../setup-for-work-orders/fault-management.md)</span><span class="sxs-lookup"><span data-stu-id="7016b-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="7016b-107">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="7016b-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="7016b-108">เลือกใบสั่งงานเพื่อทำการลงทะเบียนข้อบกพร่องบน จากนั้นบนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งงาน** ในกลุ่ม **สินทรัพย์** เลือก **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="7016b-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="7016b-109">บนแท็บด่วน **อาการ** เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="7016b-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="7016b-110">หมายเลขข้อบกพร่องจะถูกป้อนโดยอัตโนมัติตามลำดับในฟิลด์ **ข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="7016b-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="7016b-111">ในฟิลด์ **อาการข้อบกพร่อง** เลือกอาการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7016b-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="7016b-112">ในฟิลด์ **พื้นที่ข้อบกพร่อง** และ **ชนิดข้อบกพร่อง** ให้เลือกค่าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7016b-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="7016b-113">ในฟิลด์ **วันที่ของข้อบกพร่อง** ถูกใส่เป็นวันที่ปัจจุบันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7016b-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="7016b-114">คุณสามารถเลือกวันที่อื่นได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="7016b-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="7016b-115">บนแท็บด่วน **สาเหตุสำหรับอาการที่เลือก** ให้เพิ่มรายการที่อธิบายสาเหตุของปัญหา</span><span class="sxs-lookup"><span data-stu-id="7016b-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="7016b-116">บนแท็บด่วน **การแก้ไขสำหรับอาการที่เลือก** ให้เพิ่มรายการที่อธิบายวิธีการแก้ปัญหาที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="7016b-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="7016b-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7016b-117">Select **Save**.</span></span>

<span data-ttu-id="7016b-118">ในแผนภาพด้านล่างแสดงตัวอย่างของการลงทะเบียนข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="7016b-118">The illustration below shows an example of a fault registration.</span></span>

![รูปที่ 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="7016b-120">ดูข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7016b-120">View asset faults</span></span>

<span data-ttu-id="7016b-121">ในรายการ **ข้อบกพร่องของสินทรัพย์** คุณสามารถดูภาพรวมของข้อบกพร่องทั้งหมดที่ลงทะเบียนไว้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7016b-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="7016b-122">ในหน้ารายการ **ข้อบกพร่องของสินทรัพย์** คุณสามารถดูภาพรวมของข้อบกพร่องทั้งหมดที่มีการลงทะเบียนไว้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7016b-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="7016b-123">ในการเปิดรายการ ให้เลือก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="7016b-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="7016b-124">พิมพ์รายงานข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7016b-124">Print asset fault report</span></span>

<span data-ttu-id="7016b-125">จากหน้ารายการ **สินทรัพย์ทั้งหมด** คุณสามารถพิมพ์รายงานข้อบกพร่องของสินทรัพย์ที่แสดงการลงทะเบียนข้อบกพร่องทั้งหมดรวมทั้งภาพรวมในลักษณะรูปภาพของสถิติข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="7016b-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="7016b-126">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7016b-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="7016b-127">เลือกสินทรัพย์ที่จะพิมพ์รายงานข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="7016b-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="7016b-128">บนบานหน้าต่างการดำเนินการ ในแท็บ **ทั่วไป** ในกลุ่ม **รายงาน** เลือก **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="7016b-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="7016b-129">ป้อนช่วงเวลาที่ระบุ หรือเลือกชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="7016b-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="7016b-130">เลือก **ตกลง** เพื่อพิมพ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="7016b-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="7016b-131">ในการพิมพ์รายงานข้อบกพร่องสำหรับสินทรัพย์หรือชนิดสินทรัพย์ต่างๆ เลือก **การจัดการสินทรัพย์** > **รายงาน** > **สินทรัพย์** > **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="7016b-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

