---
title: คำนวณการใช้กำลังการผลิตในใบสั่งงานที่จัดกำหนดการไว้
description: หัวข้อนี้จะอธิบายถึงวิธีการคำนวณการใช้กำลังการผลิตในใบสั่งงานที่จัดกำหนดการไว้ในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887170"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="a20fe-103">คำนวณการใช้กำลังการผลิตในใบสั่งงานที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="a20fe-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a20fe-104">คุณสามารถคำนวณการใช้กำลังการผลิตในใบสั่งงานที่จัดกำหนดการไว้ เพื่อดูภาพรวมของจำนวนงานในทรัพยากรสำหรับช่วงเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a20fe-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="a20fe-105">การคำนวณสามารถทำสำหรับทรัพยากรต่อไปนี้: เจ้าหน้าที่บำรุงรักษา กลุ่มผู้ปฏิบัติงาน เครื่องมือ และสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="a20fe-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="a20fe-106">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **กำหนดการ** > **การใช้กำลังการผลิต**</span><span class="sxs-lookup"><span data-stu-id="a20fe-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="a20fe-107">ในกล่องโต้ตอบ **คำนวณการใช้กำลังการผลิต** > ฟิลด์ **แสดง** เลือกชนิดจำนวนงานที่คุณต้องการคำนวณ: "กำลังการผลิต" "จองไว้แล้ว" หรือ "ยอดคงเหลือ"</span><span class="sxs-lookup"><span data-stu-id="a20fe-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: "Capacity", "Reserved", or "Remainder".</span></span>

3. <span data-ttu-id="a20fe-108">เลือก "ใช่" บนปุ่มสลับ **ข้ามเลขศูนย์** ถ้าคุณไม่ต้องการแสดงผลลัพธ์ที่มีค่าเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="a20fe-108">Select "Yes" on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="a20fe-109">เลือกชนิดของทรัพยากรที่คุณต้องการคำนวณปริมาณการใช้กำลังการผลิตโดยการเลือก "ใช่" บนปุ่มสลับ **ผู้ปฏิบัติงาน** **กลุ่มเจ้าหน้าที่บำรุงรักษา** **เครื่องมือ** และ **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="a20fe-109">Select the resource types for which you want to calculate capacity load by selecting "Yes" on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="a20fe-110">เลือกวันที่เริ่มต้นของการคำนวณในฟิลด์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="a20fe-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="a20fe-111">ในฟิลด์ **ชนิดของช่วง** เลือกช่วงเวลาสำหรับการคำนวณ: "วัน" "สัปดาห์" "เดือน" หรือ "ไตรมาส"</span><span class="sxs-lookup"><span data-stu-id="a20fe-111">In the **Interval type** field, select the interval for the calculation: "Day", "Week", "Month", or "Quarter".</span></span>

7. <span data-ttu-id="a20fe-112">ในฟิลด์ **ความถี่ของรอบระยะเวลา** ให้ใส่จำนวนของช่วงเวลาที่คุณต้องการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="a20fe-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="a20fe-113">ตัวอย่าง เช่น หากคุณได้เลือก "Day" เป็นชนิดช่วงและคุณใส่หมายเลข "5" ในฟิลด์นี้ การคำนวณเป็นเวลาห้าวันนับจากวันที่เริ่มต้นจะถูกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a20fe-113">For example, if you have selected "Day" as the interval type, and you insert the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="a20fe-114">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="a20fe-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="a20fe-115">ภาพด้านล่างแสดงให้เห็นถึงผลลัพธ์ของการคำนวณที่ครอบคลุมสามสัปดาห์สำหรับชนิดจำนวนงานในศูนย์การผลิต "จองแล้ว"</span><span class="sxs-lookup"><span data-stu-id="a20fe-115">The figure below shows the result of a calculation covering three weeks for the load type "Reserved".</span></span>

![รูปที่ 1](media/08-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="a20fe-117">หากคุณเลือกชนิดจำนวนงานในศูนย์การผลิต "กำลังการผลิต" หรือ "ยอดคงเหลือ" สำหรับการคำนวณของคุณ ผลลัพธ์เดียวกันจะแสดงขึ้นหากไม่มีการจองทรัพยากรในรอบระยะเวลาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a20fe-117">If you select the load types "Capacity" or "Remainder" for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="a20fe-118">อ้างอิง [คำนวณการใช้กำลังการผลิต](../capacity-planning/calculate-capacity-load.md) สำหรับข้อมูลเกี่ยวกับวิธีการคำนวณการใช้กำลังการผลิตในรายการกำหนดการบำรุงรักษาและใบสั่งงานที่ไม่มีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="a20fe-118">Refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md) for information on how to calculate capacity load on maintenance schedule lines and not scheduled work orders.</span></span>

