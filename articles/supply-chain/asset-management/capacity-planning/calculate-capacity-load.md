---
title: คำนวณการใช้กำลังการผลิต
description: หัวข้อนี้อธิบายวิธีการคำนวณการใช้กำลังการผลิตในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a9b235ecedf3399c79ee081a9fe7e2423045fa5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260069"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="d8b84-103">คำนวณการใช้กำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="d8b84-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="d8b84-104">ในการจัดการสินทรัพย์ คุณสามารถคำนวณปริมาณการใช้กำลังการผลิตใน:</span><span class="sxs-lookup"><span data-stu-id="d8b84-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="d8b84-105">รายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d8b84-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="d8b84-106">ใบสั่งงานที่ยังไม่ได้ถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d8b84-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="d8b84-107">ใบสั่งงานที่จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d8b84-107">scheduled work orders</span></span>

<span data-ttu-id="d8b84-108">การทำเช่นนี้มีประโยชน์ ถ้าคุณต้องการดูภาพรวมของการใช้กำลังการผลิตที่คาดไว้สำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d8b84-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="d8b84-109">การคำนวณของการใช้กำลังการผลิตสามารถทำได้ในสินทรัพย์ทั้งหมด หรือสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d8b84-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="d8b84-110">นอกจากนี้ คุณยังสามารถทำการคำนวณในกิจกรรมการหยุดทำงานของการบำรุงรักษาหรือกลุ่มใบสั่งงานได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d8b84-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="d8b84-111">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **การใช้กำลังการผลิต** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** / **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่** > เลือกใบสั่งงานกลุ่มในรายการ > ปุ่ม **การใช้กำลังการผลิต** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กิจกรรมการหยุดทำงานของการบำรุงรักษา** > **กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** / **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่** > เลือกกิจกรรมการหยุดทำงานของการบำรุงรักษาในรายการ > ปุ่ม **การใช้กำลังการผลิต**</span><span class="sxs-lookup"><span data-stu-id="d8b84-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="d8b84-112">ในกล่องโต้ตอบ **คำนวณการใช้กำลังการผลิต** เลือกรอบระยะเวลาสำหรับการคำนวณในฟิลด์ **วันที่/เวลาที่เริ่มต้น** เเละ **วันที่/เวลาที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="d8b84-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="d8b84-113">เลือก "ใช่" บนปุ่มสลับ **รวมกำหนดการบำรุงรักษา** ถ้าคุณต้องการรวมรายการกำหนดการบำรุงรักษาในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="d8b84-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="d8b84-114">เลือก "ใช่" บนปุ่มสลับ **รวมใบสั่งงาน** ถ้าคุณต้องการรวมงานของใบสั่งงานในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="d8b84-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="d8b84-115">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการของการใช้กำลังการผลิตเกี่ยวข้องกับตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d8b84-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="d8b84-116">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานสำหรับตำเเหน่งที่ทำงานจะเเสดงขึ้นบนระดับสูงสุด เเละดังนั้นชั่วโมงในรายการอาจมีการเพิ่มเติมจากตำเเหน่งที่ทำงานที่อยู่ในระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="d8b84-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="d8b84-117">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดที่แสดงรายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานทั้งหมดบนระดับตำแหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="d8b84-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="d8b84-118">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="d8b84-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="d8b84-119">ในกลุ่ม **กลุ่มโดย...** คลิกปุ่มที่เกี่ยวข้องเพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="d8b84-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d8b84-120">ในภาพหน้าจอด้านล่าง ปุ่ม **กลุ่มที่** จะถูกเน้นด้วยสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="d8b84-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="d8b84-121">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d8b84-121">Click on a button to activate or deactivate it.</span></span>

    ![รูปที่ 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="d8b84-123">ถ้าคุณต้องการโฟกัสเฉพาะการวางแผนกำลังการผลิตที่เกี่ยวกับใบสั่งงานที่จัดกำหนดการ ดูที่ [คำนวณการใช้กำลังการผลิตในใบสั่งงานที่จัดกำหนดการ](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md)</span><span class="sxs-lookup"><span data-stu-id="d8b84-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]