---
title: คำนวณการคาดการณ์สินค้า
description: หัวข้อนี้อธิบายวิธีการคำนวณการคาดการณ์สินค้าในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888724"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="95608-103">คำนวณการคาดการณ์สินค้า</span><span class="sxs-lookup"><span data-stu-id="95608-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95608-104">เช่นเดียวกับที่คุณสามารถคำนวณการใช้กำลังการผลิต ซึ่งอธิบายไว้ในส่วนก่อนหน้า คุณยังสามารถทำการคำนวณการคาดการณ์สินค้าบน:</span><span class="sxs-lookup"><span data-stu-id="95608-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="95608-105">รายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="95608-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="95608-106">ใบสั่งงานที่ยังไม่ได้ถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="95608-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="95608-107">ใบสั่งงานที่จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="95608-107">scheduled work orders</span></span>

<span data-ttu-id="95608-108">การทำเช่นนี้มีประโยชน์ถ้าคุณต้องการดูภาพรวมของรายการปริมาณการใช้ที่คาดไว้ (อะไหล่สำลอง และสินค้าอื่นๆที่จำเป็นสำหรับการดำเนินการใบสั่งงานให้เสร็จสมบูรณ์) สำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="95608-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="95608-109">การคำนวณการคาดการณ์สินค้าสามารถทำได้ในสินทรัพย์ทั้งหมดหรือสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="95608-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="95608-110">นอกจากนี้คุณยังสามารถทำการคำนวณบนกิจกรรมการหยุดทำงานของการบำรุงรักษา (**กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** หรือ **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่**) หรือ กลุ่มใบสั่งงาน (**กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่**)</span><span class="sxs-lookup"><span data-stu-id="95608-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="95608-111">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** / **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่** > เลือกใบสั่งงานกลุ่มในรายการปุ่ม > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กิจกรรมการหยุดทำงานของการบำรุงรักษา** > **กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** / **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่** > เลือกกิจกรรมการหยุดทำงานของการบำรุงรักษาในรายการปุ่ม > **การคาดการณ์สินค้า**</span><span class="sxs-lookup"><span data-stu-id="95608-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="95608-112">ในกล่องโต้ตอบ **คำนวณการคาดการณ์สินค้า** เลือกรอบระยะเวลาสำหรับการคำนวณในฟิลด์ **วัน/เวลาที่เริ่มต้น** เเละ **วัน/เวลาที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="95608-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="95608-113">เลือก "ใช่" บนปุ่มสลับ **รวมกำหนดการบำรุงรักษา** ถ้าคุณต้องการรวมรายการกำหนดการบำรุงรักษาในการคำนวณการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="95608-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="95608-114">เลือก "ใช่" บนปุ่มสลับ **รวมใบสั่งงาน** ถ้าคุณต้องการรวมรายการใบสั่งงานในการคำนวณการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="95608-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="95608-115">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการคาดการณ์สินค้าเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="95608-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="95608-116">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานสำหรับตำเเหน่งที่ทำงานจะเเสดงขึ้นบนระดับสูงสุด เเละดังนั้นชั่วโมงในรายการอาจมีการเพิ่มเติมจากตำเเหน่งที่ทำงานที่อยู่ในระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="95608-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="95608-117">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานทั้งหมดบนระดับตำเเหน่งที่อยู่ทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="95608-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="95608-118">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="95608-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="95608-119">ในกลุ่ม **กลุ่มโดย...** คลิกปุ่มที่เกี่ยวข้องเพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="95608-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="95608-120">ในภาพหน้าจอด้านล่าง ปุ่ม **กลุ่มที่** จะถูกเน้นด้วยสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="95608-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="95608-121">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="95608-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="95608-122">คลิกปุ่ม **เเสดงมิติ** ถ้าคุณต้องการดูผลิตภัณฑ์ การจัดเก็บ หรือมิติการติดตามที่เกี่ยวข้องกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="95608-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="95608-123">เลือกกล่องกาเครื่องหมายที่เกี่ยวข้อง เเละ คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="95608-123">Select the relevant check boxes, and click **OK**.</span></span>

![รูปที่ 1](media/02-capacity-planning.png)
