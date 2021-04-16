---
title: ขั้นใบสั่งบริการ
description: โดยการกำหนดขั้นตอนสำหรับใบสั่งบริการ และการมอบหมายให้กับผู้ปฏิบัติงาน คุณสามารถควบคุมลำดับของใบสั่งบริการผ่านภารกิจที่บุคคลต่างๆ ดำเนินการในองค์กรการบริการ
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817520"
---
# <a name="service-order-stages"></a><span data-ttu-id="db1c9-103">ขั้นใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="db1c9-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="db1c9-104">คุณสามารถตั้งค่าขั้นสำหรับใบสั่งบริการเพื่อกำหนดงานที่ต้องเสร็จสมบูรณ์ ใบสั่งที่เสร็จและพนักงานที่รับผิดชอบการดำเนินการเหล่านั้น </span><span class="sxs-lookup"><span data-stu-id="db1c9-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="db1c9-105">โดยกำหนดขั้นสำหรับใบสั่งบริการ และกำหนดให้กับผู้ปฏิบัติงาน คุณสามารถควบคุมลำดับของใบสั่งบริการผ่านภารกิจที่บุคคลต่างๆ ทำในองค์กรการบริการ</span><span class="sxs-lookup"><span data-stu-id="db1c9-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="db1c9-106">ลำดับของขั้นต้องรวมเป็นระยะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="db1c9-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="db1c9-107">คุณยังสามารถกำหนดการดำเนินการที่จะได้รับอนุญาตในแต่ละขั้นตอน </span><span class="sxs-lookup"><span data-stu-id="db1c9-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="db1c9-108">ตัวอย่างเช่น ถ้าคุณยกเลิกการเลือกกล่องกาเครื่องหมาย **ลงรายการบัญชี** สำหรับขั้นตอนทั้งหมด ยกเว้นขั้นตอนสุดท้าย คุณจะป้องกันไม่ให้มีการลงรายการบัญชีใบสั่งบริการใดๆ ก่อนที่ใบสั่งบริการจะถูกประมวลผลผ่านลำดับของขั้นตอนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="db1c9-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="db1c9-109">การโยงหัวข้อในขั้นใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="db1c9-109">Branching in service order stages</span></span>

<span data-ttu-id="db1c9-110">เมื่อคุณตั้งค่าขั้นการบริการ คุณสามารถสร้างหลายตัวเลือกหรือสาขา เพื่อเลือกจากขั้นการบริการถัดไป</span><span class="sxs-lookup"><span data-stu-id="db1c9-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="db1c9-111">สาขาทั้งหมดที่คุณสร้างจะพร้อมใช้งานเพื่อเลือกจากขั้นแรกเริ่มเสร็จสมบูรณ์แล้ว </span><span class="sxs-lookup"><span data-stu-id="db1c9-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="db1c9-112">ตัวอย่างเช่น คุณตั้งค่า **การวางแผน** เป็นระยะเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="db1c9-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="db1c9-113">คุณสร้างขั้นที่สองที่มีชื่อว่า **ระหว่างดำเนินการ** และ **ยกเลิก** แล้วเลือก **การวางแผน** เป็นข้อมูลหลัก </span><span class="sxs-lookup"><span data-stu-id="db1c9-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="db1c9-114">คุณกำหนดขั้น **การวางแผน** ของใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="db1c9-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="db1c9-115">เมื่อเสร็จสิ้นขั้นการวางแผนสำหรับใบสั่งขาย คุณสามารถเลือกขั้น **ระหว่างดำเนินการ** ถ้าใบสั่งขายพร้อมที่จะทำงาน หรือคุณสามารถเลือกขั้น **ยกเลิก** ถ้าใบสั่งขายถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="db1c9-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="db1c9-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="db1c9-116">See also</span></span>

[<span data-ttu-id="db1c9-117">ตั้งค่าระยะใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="db1c9-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="db1c9-118">การเปลี่ยนขั้นของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="db1c9-118">Change the service order stage</span></span>](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]