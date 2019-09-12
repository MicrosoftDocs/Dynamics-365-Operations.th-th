---
title: เพิ่มข้อบกพร่องลงในใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการเพิ่มการลงทะเบียนข้อบกพร่องให้กับใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875929"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="5e0c6-103">เพิ่มข้อบกพร่องลงในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5e0c6-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="5e0c6-104">คุณสามารถเพิ่มข้อบกพร่องที่ตั้งค่าไว้ในโปรแกรมออกแบบข้อบกพร่องไปยังใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5e0c6-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="5e0c6-105">สินทรัพย์ที่เลือกไว้ในใบสั่งงานต้องมีชนิดของสินทรัพย์ที่มีเรกคอร์ดข้อบกพร่องอย่างน้อยหนึ่งรายการที่เชื่อมโยงอยู่</span><span class="sxs-lookup"><span data-stu-id="5e0c6-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="5e0c6-106">อ่านเพิ่มเติมเกี่ยวกับการตั้งค่าในส่วน [การจัดการข้อบกพร่อง](../setup-for-work-orders/fault-management.md)</span><span class="sxs-lookup"><span data-stu-id="5e0c6-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="5e0c6-107">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5e0c6-108">ในรายการ ให้เลือกใบสั่งงานที่คุณต้องการให้มีการลงทะเบียนข้อบกพร่อง แล้วคลิก **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="5e0c6-109">ในแท็บด่วน **อาการ** ให้คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="5e0c6-110">หมายเลขข้อบกพร่องจะถูกเพิ่มโดยอัตโนมัติตามลำดับในฟิลด์ **ข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="5e0c6-111">เลือกอาการที่เกี่ยวข้องในฟิลด์ **อาการข้อบกพร่อง** </span><span class="sxs-lookup"><span data-stu-id="5e0c6-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="5e0c6-112">เลือก **พื้นที่ข้อบกพร่อง** และ **ชนิดข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="5e0c6-113">ในฟิลด์ **วันที่ของข้อบกพร่อง** ถูกใส่เป็นวันที่ปัจจุบันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5e0c6-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="5e0c6-114">คุณสามารถเลือกวันที่อื่นได้ หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="5e0c6-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="5e0c6-115">บนแท็บด่วน **สาเหตุสำหรับอาการที่เลือก** ให้เพิ่มรายการที่อธิบายสาเหตุของปัญหา</span><span class="sxs-lookup"><span data-stu-id="5e0c6-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="5e0c6-116">บนแท็บด่วน **การแก้ไขสำหรับอาการที่เลือก** ให้เพิ่มรายการที่อธิบายวิธีการแก้ปัญหาที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="5e0c6-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="5e0c6-117">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-117">Click **Save**.</span></span>

![รูปที่ 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="5e0c6-119">ดูข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5e0c6-119">View asset faults</span></span>

<span data-ttu-id="5e0c6-120">ในรายการ **ข้อบกพร่องของสินทรัพย์** คุณสามารถดูภาพรวมของข้อบกพร่องทั้งหมดที่ลงทะเบียนไว้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5e0c6-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="5e0c6-121">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **ข้อบกพร่องของสินทรัพย์** เพื่อเปิดรายการ</span><span class="sxs-lookup"><span data-stu-id="5e0c6-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="5e0c6-122">พิมพ์รายงานข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5e0c6-122">Print asset fault report</span></span>

<span data-ttu-id="5e0c6-123">จากหน้า **รายการสินทรัพย์ทั้งหมด** คุณสามารถพิมพ์รายงานข้อบกพร่องของสินทรัพย์ที่แสดงการลงทะเบียนข้อบกพร่องทั้งหมดรวมทั้งภาพรวมของสถิติข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5e0c6-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="5e0c6-124">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="5e0c6-125">ในรายการ **สินทรัพย์** เลือกสินทรัพย์ที่คุณต้องการพิมพ์รายงานข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5e0c6-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="5e0c6-126">บนแท็บ **ทั่วไป** > **ส่วนรายงาน** คลิก **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="5e0c6-127">ใส่ช่วงเวลาที่ระบุ หรือเลือกชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5e0c6-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="5e0c6-128">คลิก **ตกลง** เพื่อพิมพ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="5e0c6-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="5e0c6-129">คุณยังสามารถพิมพ์รายงานข้อบกพร่องสำหรับสินทรัพย์หรือชนิดสินทรัพย์ต่างๆ ได้โดย คลิกที่ **การจัดการสินทรัพย์** > **รายงาน** > **สินทรัพย์** > **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5e0c6-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

