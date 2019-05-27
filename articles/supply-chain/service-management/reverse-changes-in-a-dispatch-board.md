---
title: การกลับรายการการเปลี่ยนแปลงในบอร์ดการจัดส่ง
description: 'หัวข้อนี้อธิบายวิธีการกลับรายการที่ยังไม่ได้บันทึกการปรับเปลี่ยนที่คุณทำในบอร์ดการจัดส่ง '
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMADispatchBoard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc55c1ab0a9ad7af3b55e49079185062fd119cc7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546167"
---
# <a name="reverse-changes-in-a-dispatch-board"></a><span data-ttu-id="1ec94-103">การกลับรายการการเปลี่ยนแปลงในบอร์ดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="1ec94-103">Reverse changes in a dispatch board</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1ec94-104">หัวข้อนี้อธิบายวิธีการกลับรายการที่ยังไม่ได้บันทึกการปรับเปลี่ยนที่คุณทำในบอร์ดการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="1ec94-104">This topic describes how to reverse unsaved modifications that you make in a dispatch board.</span></span> <span data-ttu-id="1ec94-105">ตัวอย่างเช่น คุณกำหนดผู้ปฏิบัติงานให้กับกิจกรรมการบริการ บันทึกข้อมูล และจากนั้นกำหนดผู้ปฏิบัติงานที่แตกต่างกันให้กับกิจกรรมการบริการ </span><span class="sxs-lookup"><span data-stu-id="1ec94-105">For example, you assign a worker to a service activity, save the information, and then later decide to assign a different worker to the service activity.</span></span> <span data-ttu-id="1ec94-106">คุณปรับเปลี่ยนผู้ปฏิบัติงานในบอร์ดการจัดส่ง และจากนั้นก่อนที่จะบันทึกการเปลี่ยนแปลง เรียนรู้ว่า ผู้ปฏิบัติงานที่เพิ่งกำหนดให้ไม่พร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="1ec94-106">You modify the worker in the dispatch board, and then, before saving the change, learn that the worker just assigned is not available.</span></span> <span data-ttu-id="1ec94-107">คุณสามารถกลับรายการการเปลี่ยนแปลงที่ไม่ได้บันทึกไว้เพื่อให้ผู้ปฏิบัติงานเดียวกันถูกมอบหมายไปยังใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="1ec94-107">You can reverse the unsaved modification so that the original worker is reassigned to the service order.</span></span>

<span data-ttu-id="1ec94-108">ใช้ขั้นตอนต่อไปนี้เพื่อกลับรายการยังไม่ได้บันทึกการเปลี่ยนแปลงในบอร์ดการจัดส่ง:</span><span class="sxs-lookup"><span data-stu-id="1ec94-108">Use the following steps to reverse unsaved changes in a dispatch board:</span></span>

1.  <span data-ttu-id="1ec94-109">คลิก **การจัดการงานบริการ** \> **งานประจำงวด** \> **บอร์ดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="1ec94-109">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>

2.  <span data-ttu-id="1ec94-110">ในแบบฟอร์ม **บอร์ดการจัดส่ง** ป้อนข้อมูลที่เกี่ยวข้องในฟิลด์ และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ec94-110">In the **Dispatch board** form, enter relevant information in the fields, and then click **OK**.</span></span> 

3.  <span data-ttu-id="1ec94-111">เมื่อต้องการกลับรายการเปลี่ยนแปลงล่าสุดที่ไม่ได้บันทึกไว้ ให้คลิก **เลิกทำ**</span><span class="sxs-lookup"><span data-stu-id="1ec94-111">To reverse the most recent change that is not saved, click **Undo**.</span></span>

4.  <span data-ttu-id="1ec94-112">เมื่อต้องการกลับรายการชุดของการเปลี่ยนแปลงซึ่งยังไม่ได้บันทึก ให้คลิก **เลิกทำ** ต่อไป จนกว่าการเปลี่ยนแปลงแต่ละรายการที่คุณต้องการยกเลิกจะถูกกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="1ec94-112">To reverse a series of changes that are not saved, continue clicking **Undo** until each change that you want to discard is reversed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ec94-113">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1ec94-113">See also</span></span>

[<span data-ttu-id="1ec94-114">บอร์ดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="1ec94-114">Dispatch board</span></span>](dispatch-board.md)

[<span data-ttu-id="1ec94-115">กิจกรรมการบริการ</span><span class="sxs-lookup"><span data-stu-id="1ec94-115">Service activities</span></span>](service-activities.md)

 


