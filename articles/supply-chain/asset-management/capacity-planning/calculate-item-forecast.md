---
title: คำนวณการคาดการณ์สินค้า
description: หัวข้อนี้อธิบายวิธีการคำนวณการคาดการณ์สินค้าในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886781"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="6f00c-103">คำนวณการคาดการณ์สินค้า</span><span class="sxs-lookup"><span data-stu-id="6f00c-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6f00c-104">เช่นเดียวกับที่คุณสามารถคำนวณการใช้กำลังการผลิต ซึ่งอธิบายไว้ในส่วนก่อนหน้า คุณยังสามารถทำการคำนวณการคาดการณ์สินค้าบน</span><span class="sxs-lookup"><span data-stu-id="6f00c-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on</span></span>

- <span data-ttu-id="6f00c-105">รายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="6f00c-105">Maintenance schedule lines</span></span>  
- <span data-ttu-id="6f00c-106">ใบสั่งงานที่ยังไม่ได้จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="6f00c-106">Work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="6f00c-107">ใบสั่งงานที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="6f00c-107">Scheduled work orders</span></span>

<span data-ttu-id="6f00c-108">การทำเช่นนี้มีประโยชน์ถ้าคุณต้องการดูภาพรวมของรายการปริมาณการใช้ที่คาดไว้ (อะไหล่สำลอง และสินค้าอื่นๆที่จำเป็นสำหรับการดำเนินการใบสั่งงานให้เสร็จสมบูรณ์) สำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="6f00c-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="6f00c-109">การคำนวณการคาดการณ์สินค้าสามารถทำได้ในสินทรัพย์ทั้งหมดหรือสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6f00c-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="6f00c-110">นอกจากนี้คุณยังสามารถทำการคำนวณบนกิจกรรมการหยุดทำงานของการบำรุงรักษา (**กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** หรือ **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่**) หรือ กลุ่มใบสั่งงาน (**กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่**)</span><span class="sxs-lookup"><span data-stu-id="6f00c-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="6f00c-111">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** / **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่** > เลือกใบสั่งงานกลุ่มในรายการปุ่ม > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กิจกรรมการหยุดทำงานของการบำรุงรักษา** > **กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** / **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่** > เลือกกิจกรรมการหยุดทำงานของการบำรุงรักษาในรายการปุ่ม > **การคาดการณ์สินค้า**</span><span class="sxs-lookup"><span data-stu-id="6f00c-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="6f00c-112">ในกล่องโต้ตอบ **คำนวณการคาดการณ์สินค้า** เลือกรอบระยะเวลาสำหรับการคำนวณในฟิลด์ **วัน/เวลาที่เริ่มต้น** เเละ **วัน/เวลาที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="6f00c-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="6f00c-113">เลือก "ใช่" บนปุ่มสลับ **รวมกำหนดการบำรุงรักษา** ถ้าคุณต้องการรวมรายการกำหนดการบำรุงรักษาในการคำนวณการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="6f00c-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="6f00c-114">เลือก "ใช่" บนปุ่มสลับ **รวมใบสั่งงาน** ถ้าคุณต้องการรวมรายการใบสั่งงานในการคำนวณการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="6f00c-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="6f00c-115">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการคาดการณ์สินค้าเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="6f00c-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> <span data-ttu-id="6f00c-116">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานสำหรับตำเเหน่งที่ทำงานจะเเสดงขึ้นบนระดับสูงสุด เเละดังนั้นชั่วโมงในรายการอาจมีการเพิ่มเติมจากตำเเหน่งที่ทำงานที่อยู่ในระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="6f00c-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="6f00c-117">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานทั้งหมดบนระดับตำเเหน่งที่อยู่ทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6f00c-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="6f00c-118">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6f00c-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="6f00c-119">ในกลุ่มบานหน้าต่างการดำเนินการ **กลุ่มโดย...** คลิกปุ่มที่เกี่ยวข้องเพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6f00c-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6f00c-120">ปุ่มบานหน้าต่างการดำเนินการที่เลือกจะถูกเน้นในสีฟ้า</span><span class="sxs-lookup"><span data-stu-id="6f00c-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="6f00c-121">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6f00c-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="6f00c-122">คลิกปุ่ม **เเสดงมิติ** ถ้าคุณต้องการดูผลิตภัณฑ์ การจัดเก็บ หรือมิติการติดตามที่เกี่ยวข้องกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6f00c-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="6f00c-123">เลือกกล่องกาเครื่องหมายที่เกี่ยวข้อง เเละ คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6f00c-123">Select the relevant check boxes, and click **OK**.</span></span>

<span data-ttu-id="6f00c-124">รูปด้านล่างแสดงภาพหน้าจอของอินเทอร์เฟส</span><span class="sxs-lookup"><span data-stu-id="6f00c-124">The figure below shows a screenshot of the interface.</span></span>

![รูปที่ 1](media/02-capacity-planning.png)
