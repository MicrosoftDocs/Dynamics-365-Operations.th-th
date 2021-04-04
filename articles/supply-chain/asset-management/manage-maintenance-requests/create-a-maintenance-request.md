---
title: สร้างคำขอการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการสร้างคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a85125853b3b69d33f07249e0d2aa7592de1cc8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253433"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="d2de4-103">สร้างคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d2de4-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d2de4-104">คำขอการบำรุงรักษาสามารถใช้ได้ ถ้าเจ้าหน้าที่บำรุงรักษาหรือผู้ปฏิบัติงานการผลิตพบว่าอุปกรณ์ต้องการการซ่อมแซม แต่งานการซ่อมแซมไม่สามารถทำได้ทันที</span><span class="sxs-lookup"><span data-stu-id="d2de4-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="d2de4-105">**ตัวอย่าง** ในขณะที่เจ้าหน้าที่บำรุงรักษากำลังทำการซ่อมแซม เธอพบว่าสินทรัพย์อื่นที่สถานที่เดียวกันต้องได้รับการบริการ</span><span class="sxs-lookup"><span data-stu-id="d2de4-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="d2de4-106">อย่างไรก็ตาม เจ้าหน้าที่บำรุงรักษาไม่มีเวลาหรืออะไหล่สำรองที่ต้องการในการทำงานการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="d2de4-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="d2de4-107">ดังนั้น เธอจึงสร้างคำขอการบำรุงรักษาในสินทรัพย์ และป้อนคำอธิบายย่อของปัญหา</span><span class="sxs-lookup"><span data-stu-id="d2de4-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="d2de4-108">ส่วน **คำขอการบำรุงรักษาของสินทรัพย์** ของบานหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** ทางด้านขวาของหน้า **สินทรัพย์ทั้งหมด** หรือหน้า **สินทรัพย์ที่ใช้งานอยู่** (**การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**) แสดงคำขอการบำรุงรักษาที่ใช้งานอยู่ที่แนบกับสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d2de4-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="d2de4-109">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="d2de4-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d2de4-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d2de4-110">Select **New**.</span></span>
3. <span data-ttu-id="d2de4-111">ในกล่องโต้ตอบ **สร้างคำขอ** ในฟิลด์ **ชนิดคำขอการบำรุงรักษา** ให้เลือกชนิดของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d2de4-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="d2de4-112">แนะนำให้ใช้ชนิดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2de4-112">A default type is suggested.</span></span>
4. <span data-ttu-id="d2de4-113">ในฟิลด์ **คำอธิบาย** ให้ป้อนชื่อหรือชื่อเรื่องที่อธิบายคำขอการบำรุงรักษาอย่างคร่าวๆ</span><span class="sxs-lookup"><span data-stu-id="d2de4-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="d2de4-114">ในฟิลด์ **ตำแหน่งที่ทำงาน** และ **สินทรัพย์** ให้เลือกตำแหน่งที่ทำงานหรือสินทรัพย์ หรือการรวมกันของตำแหน่งที่ทำงานและสินทรัพย์ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2de4-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="d2de4-115">คุณสามารถสร้างคำขอการบำรุงรักษาได้โดยไม่ต้องเลือกสินทรัพย์ และสามารถเพิ่มสินทรัพย์ลงในคำขอการบำรุงรักษาในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="d2de4-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="d2de4-116">ถ้าเจ้าหน้าที่บำรุงรักษาที่เข้าสู่ระบบเกี่ยวข้องกับทรัพยากรที่เกี่ยวข้องกับสินทรัพย์ ฟิลด์ **สินทรัพย์** จะถูกตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d2de4-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="d2de4-117">ถ้ามีการแนบคำขอการบำรุงรักษากับสินทรัพย์ที่เลือกแล้ว แถบข้อความจะปรากฏที่ด้านบนของกล่องโต้ตอบ **สร้างคำขอ** เพื่อแจ้งให้คุณทราบเกี่ยวกับรหัสของคำขอการบำรุงรักษาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d2de4-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="d2de4-118">นอกจากนี้ แถบข้อความจะแจ้งให้คุณทราบ หากสินทรัพย์ได้รับการคุ้มครองตามข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="d2de4-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="d2de4-119">ในฟิลด์ **ระดับการบริการ** ให้เลือกระดับการบริการที่บ่งชี้ความเร่งด่วนของคำขอ</span><span class="sxs-lookup"><span data-stu-id="d2de4-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="d2de4-120">ถ้าคุณได้เลือกสินทรัพย์ในขั้นตอนที่ 5 คุณสามารถใช้ฟิลด์ **อาการของข้อบกพร่อง** ฟิลด์ **พื้นที่ของข้อบกพร่อง** และฟิลด์ **ชนิดของข้อบกพร่อง** เพื่อสร้างการลงทะเบียนข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="d2de4-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="d2de4-121">ถ้าคำขอการบำรุงรักษาทำให้เกิดการหยุดทำงานของการบำรุงรักษา ให้ป้อนวันที่และเวลาเริ่มต้นของการหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="d2de4-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="d2de4-122">ฟิลด์ **เริ่มต้นโดย** จะถูกตั้งค่าเป็นชื่อของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d2de4-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="d2de4-123">ฟิลด์ **เริ่มต้นจริง** ถูกกำหนดเป็นวันที่และเวลาปัจจุบันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d2de4-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="d2de4-124">อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2de4-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="d2de4-125">ในฟิลด์ **บันทึกย่อ** ให้ป้อนบันทึกย่อเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="d2de4-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="d2de4-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d2de4-126">Select **OK**.</span></span>

![สร้างคำขอการบำรุงรักษา](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="d2de4-128">การประมวลผลในภายหลังของคำขอบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d2de4-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="d2de4-129">หลังจากที่มีการสร้างคำขอการบำรุงรักษา แต่ก่อนที่จะมีการแปลงเป็นใบสั่งงาน จะมีการปรับปรุงข้อมูลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d2de4-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="d2de4-130">โดยทั่วไปแล้ว ผู้วางแผนหรือพนักงานระดับผู้ดูแลอื่นจะปฏิบัติงานนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d2de4-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="d2de4-131">บนหน้า **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่** เลือกคำขอที่จะทำงานด้วย และจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d2de4-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="d2de4-132">ในมุมมองรายละเอียด คุณสามารถปรับปรุงข้อมูลต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="d2de4-132">In the details view, you can update various information.</span></span> <span data-ttu-id="d2de4-133">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="d2de4-133">Here are some examples:</span></span>

- <span data-ttu-id="d2de4-134">เลือกและตรวจสอบความถูกต้องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="d2de4-134">Select and verify the asset.</span></span> <span data-ttu-id="d2de4-135">ถ้าคุณต้องเลือกสินทรัพย์อื่นในภายหลัง คุณสามารถตั้งค่าตัวเลือก **ตรวจสอบความถูกต้องของสินทรัพย์แล้ว** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="d2de4-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="d2de4-136">เลือกกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบและ/หรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="d2de4-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="d2de4-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าที่จำเป็น ดู [เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](../setup-for-maintenance-requests/responsible-workers.md)</span><span class="sxs-lookup"><span data-stu-id="d2de4-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="d2de4-138">เลือกชนิดงานการบำรุงรักษา และถ้าข้อมูลนี้เกี่ยวข้อง ตัวแปรงานการบำรุงรักษาที่เกี่ยวข้องและการแลกเปลี่ยนงาน</span><span class="sxs-lookup"><span data-stu-id="d2de4-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="d2de4-139">ในฟิลด์ **ละติจูด** และ **ลองจิจูด** ให้ป้อนพิกัดทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="d2de4-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="d2de4-140">พิกัดใดๆ ที่ถูกเพิ่มลงในคำขอการบำรุงรักษาจะถูกโอนย้ายไปยังใบสั่งงานที่เกี่ยวข้องโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d2de4-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![อัพเดตคำขอการบำรุงรักษา](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="d2de4-142">ถ้าคุณเลือกสินทรัพย์เมื่อคุณสร้างคำขอการบำรุงรักษา คุณสามารถเพิ่มข้อบกพร่องหนึ่งรายการไปยังสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="d2de4-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="d2de4-143">หลังจากที่มีการสร้างคำขอการบำรุงรักษาแล้ว คุณสามารถเพิ่มข้อบกพร่องเพิ่มเติมได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2de4-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="d2de4-144">เมื่อต้องการเพิ่มข้อบกพร่อง ให้เลือก **ข้อบกพร่องของสินทรัพย์** ในหน้า **คำขอการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d2de4-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]