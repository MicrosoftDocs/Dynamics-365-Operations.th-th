---
title: สถานะการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการคำนวณสถานะการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5bac42d5cdc62361ee9a562e59bafa09ca7a215
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018507"
---
# <a name="maintenance-status"></a><span data-ttu-id="c0b24-103">สถานะการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c0b24-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c0b24-104">ในการจัดการสินทรัพย์ คุณสามารถทำการคำนวณภาพรวมสำหรับรอบระยะเวลาที่ระบุสำหรับคำขอการบำรุงรักษาใหม่ ที่ใช้งานอยู่ และที่เสร็จสมบูรณ์ ใบสั่งงาน และกิจกรรมการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c0b24-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="c0b24-105">คุณยังสามารถดูจำนวนของการประเมินเงื่อนไขที่เสร็จสมบูรณ์สำหรับรอบระยะเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c0b24-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="c0b24-106">ใช้การคำนวณนี้เพื่อดูภาพรวมของปริมาณงานสำหรับคำขอการบำรุงรักษาที่เข้ามาและที่เสร็จสมบูรณ์ และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="c0b24-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="c0b24-107">ทำการคำนวณสถานะการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c0b24-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="c0b24-108">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **สถานะการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c0b24-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="c0b24-109">ในกล่องโต้ตอบ **สถานะการคำนวณ** เลือกช่วงเวลาที่คุณต้องการทำการคำนวณในฟิลด์ **วันที่เริ่มต้น** เเละฟิลด์ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="c0b24-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="c0b24-110">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้การบำรุงรักษษเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="c0b24-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="c0b24-111">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการการบำรุงรักษาทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุดดังนั้นสถานะในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="c0b24-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="c0b24-112">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการการบำรุงรักษาทั้งหมดบนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c0b24-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c0b24-113">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c0b24-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="c0b24-114">คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c0b24-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c0b24-115">ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="c0b24-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c0b24-116">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c0b24-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="c0b24-117">อย่าลืมคลิกปุ่ม **อัพเดต** เพื่ออัพเดตการคำนวณแต่ละครั้งที่คุณทำการเปลี่ยนแปลงโดยการเปิดใช้งานหรือปิดใช้งานปุ่ม **จัดกลุ่มโดย** หรือโดยการทำการคำนวณสำหรับรอบระยะเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="c0b24-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="c0b24-118">คลิก **สถานะ** หากคุณต้องการสร้างการคำนวณสถานะการบำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="c0b24-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="c0b24-119">ผลลัพธ์แสดงใน **สถานะการบำรุงรักษา** เท่านั้น รวมถึงคำขอบำรุงรักษาและใบสั่งงานที่มีวันที่และเวลาเริ่มต้นจริง</span><span class="sxs-lookup"><span data-stu-id="c0b24-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="c0b24-120">วันที่และเวลาที่สิ้นสุดอาจว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="c0b24-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0b24-121">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="c0b24-121">Example 1</span></span>

<span data-ttu-id="c0b24-122">ในภาพหน้าจอด้านล่าง ปุ่ม **ปี** และปุ่ม **เดือน** ถูกเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c0b24-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="c0b24-123">ด้วยตัวเลือก **จัดกลุ่มโดย** ที่เลือกเหล่านี้ คุณจะได้ภาพรวมทั่วไปของปริมาณงานรายเดือน และปริมาณที่สามารถประมวลผลได้ที่เกี่ยวข้องกับคำขอบำรุงรักษาและใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="c0b24-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![ตัวอย่างของปริมาณงานรายเดือน](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="c0b24-125">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="c0b24-125">Example 2</span></span>

<span data-ttu-id="c0b24-126">ในภาพหน้าจอด้านล่าง ข้อมูลเกี่ยวกับตำแหน่งที่ทำงานถูกเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="c0b24-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="c0b24-127">ขณะนี้ คุณสามารถเปรียบเทียบปริมาณงานและปริมาณที่สามารถประมวลผลได้ระหว่างตำแหน่งที่ทำงาน ซึ่งอาจแสดงถึงสถานที่ตั้งทางภูมิศาสตร์ โรงงาน หรือพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c0b24-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![ตัวอย่างของปริมาณงานรายเดือนที่มีตำแหน่งที่ทำงาน](media/14-controlling-and-reporting.png)

