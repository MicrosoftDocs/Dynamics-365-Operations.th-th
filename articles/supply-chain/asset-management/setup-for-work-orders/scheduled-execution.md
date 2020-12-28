---
title: การดำเนินการที่จัดกำหนดการไว้
description: หัวข้อนี้อธิบายถึงการดำเนินการที่จัดกำหนดการไว้ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438513"
---
# <a name="scheduled-execution"></a><span data-ttu-id="6c0e7-103">การดำเนินการที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="6c0e7-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6c0e7-104">คุณสามารถใช้ระดับการบริการใบสั่งงานเพื่อตั้งค่าการดำเนินการที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="6c0e7-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="6c0e7-105">(หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับระดับการบริการใบสั่งงาน ดู [ระดับการบริการและคำอธิบาย](service-level-and-description.md)) การดำเนินการที่จัดกำหนดการไว้ ให้ความยืดหยุ่นในการวางแผนงานสำหรับเจ้าหน้าที่บำรุงรักษา เนื่องจากคุณสามารถตั้งค่าข้อกำหนดที่มีรายละเอียดเพิ่มเติมหรือน้อยกว่าสำหรับช่วงเวลาที่ใบสั่งงานควรจะดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6c0e7-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="6c0e7-106">ตัวอย่าง เช่น เจ้าหน้าที่บำรุงรักษาที่ทำงานให้สำเร็จเร็วกว่าที่คาดไว้ในศูนย์การผลิต อาจสามารถย้ายไปยังงานอื่นๆ ที่อยู่ใกล้เคียงที่วางแผนไว้สำหรับสัปดาห์ปัจจุบัน แต่ไม่จำเป็นต้องใช้สำหรับวันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="6c0e7-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="6c0e7-107">วิธีการนี้อนุญาตให้มีการเพิ่มประสิทธิภาพของการวางแผนผู้ปฏิบัติงานและความสมบูรณ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="6c0e7-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="6c0e7-108">การตั้งค่าการดำเนินการที่จัดกำหนดการไว้ซึ่งเกี่ยวข้องกับใบสั่งงานอาจเป็นแบบทั่วไปหรือเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6c0e7-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="6c0e7-109">คุณสามารถตั้งค่ารายการทั่วไปที่ไม่มีการจำกัดเฉพาะชนิดของใบสั่งงาน ชนิดสินทรัพย์ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6c0e7-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="6c0e7-110">หรืออีกทางหนึ่ง คุณสามารถสร้างรายการการดำเนินการที่จัดกำหนดการไว้ซึ่งใช้กับชนิดของใบสั่งงานหนึ่งๆ ชนิดสินทรัพย์ ชนิดงานบำรุงรักษา และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6c0e7-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="6c0e7-111">เลือก **การจัดการสินทรัพย์** \> **ตั้งค่า** \> **ใบสั่งงาน** \> **การดำเนินการที่จัดกำหนดการไว้**</span><span class="sxs-lookup"><span data-stu-id="6c0e7-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="6c0e7-112">เลือก **ใหม่** เพื่อสร้างรายการการดำเนินการที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="6c0e7-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="6c0e7-113">ใน **ตำแหน่งที่ทำงาน** **ชนิดของใบสั่งงาน** **ชนิดของสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** **ประเภทชนิดงานการบำรุงรักษา** **ชนิดงานการบำรุงรักษา** **ตัวแปรชนิดงานการบำรุงรักษา** และฟิลด์ **ความเชี่ยวชาญ** เลือกค่าตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c0e7-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="6c0e7-114">ในฟิลด์ **ระดับการบริการ** เลือกระดับการบริการของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="6c0e7-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="6c0e7-115">หากคุณปล่อยฟิลด์นี้ว่างไว้ คุณจะสร้างชนิดทั่วไปทั้งหมดของรายการการดำเนินการที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="6c0e7-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="6c0e7-116">ตัวอย่างของรายการทั่วไปให้ดูที่เรกคอร์ดแรกในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6c0e7-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="6c0e7-117">รายการดังกล่าวจะเปิดใช้งานใบสั่งงานทั้งหมดที่ไม่มีระดับการบริการใบสั่งงานที่จัดกำหนดการไว้สำหรับวันที่และเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="6c0e7-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="6c0e7-118">ในฟิลด์ **การดำเนินการที่จัดกำหนดการไว้** เลือกช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="6c0e7-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="6c0e7-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6c0e7-119">Select **Save**.</span></span>

![การดำเนินการที่จัดกำหนดการไว้](media/20-setup-for-work-orders.png)
