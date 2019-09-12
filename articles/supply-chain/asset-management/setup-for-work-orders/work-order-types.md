---
title: ชนิดใบสั่งงาน
description: หัวข้อนี้อธิบายชนิดของใบสั่งานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 57120b51c069e49697f8ec4357265974a0d3afb4
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874589"
---
# <a name="work-order-types"></a><span data-ttu-id="e8ce6-103">ชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e8ce6-104">ชนิดของใบสั่งงานใช้ในการจัดประเภทใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="e8ce6-105">ตัวอย่าง เช่น คุณอาจมีใบสั่งงานที่เกี่ยวข้องกับการบำรุงรักษาเชิงป้องกันหรือการบำรุงรักษาเชิงแก้ไข</span><span class="sxs-lookup"><span data-stu-id="e8ce6-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="e8ce6-106">ชนิดของใบสั่งงานจะกำหนดสังกัดกับแบบจำลองวงจรงานของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="e8ce6-107">แบบจำลองวงจรงานของใบสั่งงานกำหนดสถานะวงจรงานของใบสั่งงานที่สามารถกำหนดบนใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="e8ce6-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="e8ce6-108">(ตัวอย่างของสถานะวงจรของใบสั่งงานรวม **สร้างแล้ว** **อยู่ระหว่างดำเนินการ** และ **เสร็จสิ้น**)</span><span class="sxs-lookup"><span data-stu-id="e8ce6-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="e8ce6-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสถานะวงจรของใบสั่งงานและขั้นโครงการ ดู [สถานะวงจรงานของใบสั่งงาน](work-order-lifecycle-states.md)</span><span class="sxs-lookup"><span data-stu-id="e8ce6-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="e8ce6-110">เลือก **การจัดการสินทรัพย์** \> **ตั้งค่า** \> **ใบสั่งงาน** \> **ชนิดของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="e8ce6-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="e8ce6-111">เลือก **ใหม่** เพื่อสร้างชนิดของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="e8ce6-112">ในฟิลด์ **ชนิดของใบสั่งงาน** ให้ป้อนรหัสสำหรับชนิดของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="e8ce6-113">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="e8ce6-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="e8ce6-114">ในฟิลด์ **แบบจำลองวงจรของใบสั่งงาน** เลือกแบบจำลองวงจร</span><span class="sxs-lookup"><span data-stu-id="e8ce6-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="e8ce6-115">ตั้งค่าตัวเลือก **เจ้าหน้าที่บำรุงรัษาหนึ่งคน** เป็น **ใช่** หากงานใบสั่งงานทั้งหมดที่เกี่ยวข้องกับใบสั่งงานชนิดนี้ ควรมีการจัดกำหนดการให้กับเจ้าหน้าที่บำรุงรักษาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="e8ce6-116">ในฟิลด์ **ชนิดต้นทุน** ให้เลือก **การแก้ไข** **การป้องกัน** หรือ **การลงทุน** ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e8ce6-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="e8ce6-117">งานของใบสั่งงานทั้งหมดในใบสั่งงานต้องมีชนิดต้นทุนเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="e8ce6-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="e8ce6-118">ในส่วน **ข้อบังคับ** ให้ตั้งค่าตัวเลือกที่เกี่ยวข้อง เป็น **ใช่** เพื่อระบุว่าข้อบกพร่องที่เกี่ยวข้องหรือการหยุดทำงานของการบำรุงรักษาที่เกี่ยวข้องใด จะเพิ่มไปยังใบสั่งงานของชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="e8ce6-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8ce6-119">ตัวเลือกในส่วน **ข้อบังคับ** ซึ่งเกี่ยวข้องกับตัวเลือกบนแท็บด่วน **ตรวจสอบความถูกต้อง** ของหน้า **สถานะวงจรของใบสั่งงาน** (**การจัดการสินทรัพย์** \> **ตั้งค่า** \> **ใบสั่งงาน** \> **สถานะวงจร**)</span><span class="sxs-lookup"><span data-stu-id="e8ce6-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="e8ce6-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e8ce6-120">Select **Save**.</span></span>

![รูปที่ 1](media/16-setup-for-work-orders.png)
