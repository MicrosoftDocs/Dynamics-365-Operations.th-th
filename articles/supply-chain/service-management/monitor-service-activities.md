---
title: การติดตามกิจกรรมการบริการ
description: แบบฟอร์มบอร์ดการจัดส่งจะให้การอัพเดตสถานะแบบทันทีสำหรับกิจกรรมบริการตามกำหนดการต่างๆ และเครื่องมือสำหรับการติดตามขั้นตอนทั่วไปของใบสั่งบริการในบริษัทของคุณ
author: ShylaThompson
manager: tfehr
ms.date: 05/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687768ac8891b778f7d8d0eb6e3dcd9a4aa3298a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202249"
---
# <a name="monitor-service-activities"></a><span data-ttu-id="0f99c-103">การติดตามกิจกรรมการบริการ</span><span class="sxs-lookup"><span data-stu-id="0f99c-103">Monitor service activities</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0f99c-104">แบบฟอร์ม **บอร์ดการจัดส่ง** จะให้การอัพเดตสถานะแบบทันทีสำหรับกิจกรรมบริการตามกำหนดการต่างๆ และเครื่องมือสำหรับการติดตามขั้นตอนทั่วไปของใบสั่งบริการในบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="0f99c-104">The **Dispatch board** form provides an at-a-glance status update for the various scheduled service activities, and tools for tracking the general flow of service orders in your company.</span></span>


> [!TIP]
> <P><span data-ttu-id="0f99c-105">ถ้าต้องการดูรายละเอียดเกี่ยวกับกิจกรรมการบริการ ให้เลือกกิจกรรมนั้นในแผนภูมิ Gantt ที่ด้านบนของแบบฟอร์ม <STRONG>บอร์ดการจัดส่ง</STRONG> คลิกขวา และจากนั้นคลิก <STRONG>ข้อมูล</STRONG></span><span class="sxs-lookup"><span data-stu-id="0f99c-105">To view details about a service activity, select it in the Gantt chart at the top of the <STRONG>Dispatch board</STRONG> form, right-click, and then click <STRONG>Information</STRONG>.</span></span></P>


<span data-ttu-id="0f99c-106">โดยใช้เครื่องมือบนแบบฟอร์มนี้ คุณจะสามารถเรียงลำดับใบสั่งบริการตามวันที่ ระดับความสำคัญ หรือชนิดของกิจกรรมการบริการ สามารถดูระดับความสำคัญที่กำหนดให้กับใบสั่งบริการ และตรวจสอบกิจกรรมที่กำหนดให้กับใบสั่งบริการแต่ละใบได้</span><span class="sxs-lookup"><span data-stu-id="0f99c-106">By using the tools in this form, you can sort service orders by date, priority, or type of service activity, view the priority levels that are assigned to service orders, and review which activities are assigned to individual service orders.</span></span>

<span data-ttu-id="0f99c-107">ถ้าคุณต้องการกระจายการกำหนดกิจกรรมการบริการอีกครั้ง คุณสามารถย้ายการแสดงด้วยรูปภาพของกิจกรรมบริการเพื่อกำหนดให้กับพนักงานอื่นหรือวันและเวลาอื่นได้</span><span class="sxs-lookup"><span data-stu-id="0f99c-107">If you must redistribute service activity assignments, you can move the graphical representation of a service activity to assign it to a different employee or a different date and time.</span></span>

## <a name="example"></a><span data-ttu-id="0f99c-108">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0f99c-108">Example</span></span>

<span data-ttu-id="0f99c-109">ในขณะที่ติดตามกิจกรรมการบริการของวัน </span><span class="sxs-lookup"><span data-stu-id="0f99c-109">While monitoring the day's service activity, you notice that John, a service technician, is running behind schedule on assigned service calls.</span></span> <span data-ttu-id="0f99c-110">คุณยังจะสังเกตได้ว่าการให้บริการครั้งสุดในรายการของเขาจะต้องเสร็จสิ้นเมื่อสิ้นสุดวัน เพื่อให้ตรงกับข้อกำหนดของข้อตกลงระดับการบริการ </span><span class="sxs-lookup"><span data-stu-id="0f99c-110">You also notice that the last call in his list must be completed by the end of the day to meet service level agreement requirements.</span></span> <span data-ttu-id="0f99c-111">โดยใช้ฟังก์ชันการลากและปล่อยของแผนภูมิ Gantt คุณจึงสามารถกำหนดใหม่ให้ Meg รับผิดชอบการให้บริการนั้นแทน ซึ่งทำงานบริการของตัวเองเสร็จก่อนกำหนด</span><span class="sxs-lookup"><span data-stu-id="0f99c-111">By using the drag-and-drop functionality of the Gantt chart, you can reassign that service call to Meg, who has completed her own service calls ahead of schedule.</span></span>

## <a name="open-the-dispatch-board-form"></a><span data-ttu-id="0f99c-112">การเปิดแบบฟอร์มบอร์ดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0f99c-112">Open the Dispatch board form</span></span>

<span data-ttu-id="0f99c-113">คลิก **การจัดการงานบริการ** \> **งานประจำงวด** \> **บอร์ดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="0f99c-113">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f99c-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="0f99c-114">See also</span></span>

[<span data-ttu-id="0f99c-115">การจัดระดับความสำคัญของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="0f99c-115">Prioritize service orders</span></span>](prioritize-service-orders.md)

[<span data-ttu-id="0f99c-116">ดูสถานะของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="0f99c-116">View the status of service orders</span></span>](view-the-status-of-service-orders.md)

<span data-ttu-id="0f99c-117">[บอร์ดการจัดส่ง (แบบฟอร์ม)](https://technet.microsoft.com/library/hh242789\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="0f99c-117">[Dispatch board (form)](https://technet.microsoft.com/library/hh242789\(v=ax.60\))</span></span>

  


