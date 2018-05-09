---
title: "ประเมินใบสั่งผลิต"
description: "คุณสามารถรันขั้นตอนนี้ โดยใช้ข้อมูลบริษัทในการสาธิต USMF หรือชุดข้อมูลของคุณเอง "
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 90d6dd1886deb9ec5700e1db9b5a3aaf7f83bdf8
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="9d648-103">ประเมินใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9d648-103">Estimate a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d648-104">คุณสามารถรันขั้นตอนนี้ โดยใช้ข้อมูลบริษัทในการสาธิต USMF หรือชุดข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="9d648-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="9d648-105">ในทั้งสองกรณี คุณต้องมีใบสั่งผลิตที่มีสถานะสร้างขึ้นแล้วเปิดค้างไว้ </span><span class="sxs-lookup"><span data-stu-id="9d648-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="9d648-106">นี่เป็นขั้นตอนที่สองจากเจ็ดขั้นตอน ซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต</span><span class="sxs-lookup"><span data-stu-id="9d648-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="9d648-107">ประเมินใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9d648-107">Estimate a production order</span></span>
1. <span data-ttu-id="9d648-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="9d648-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="9d648-109">เลือกใบสั่งผลิตที่มีสถานะเป็นสร้างขึ้นแล้วในกริด </span><span class="sxs-lookup"><span data-stu-id="9d648-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="9d648-110">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9d648-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="9d648-111">คลิกประเมิน </span><span class="sxs-lookup"><span data-stu-id="9d648-111">Click Estimate.</span></span>
    * <span data-ttu-id="9d648-112">ในขั้นตอนนี้ ต้นทุนที่ถูกประเมินของใบสั่งผลิตแต่ละครั้งถูกคำนวณขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d648-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="9d648-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9d648-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="9d648-114">ดูรายละเอียดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9d648-114">View the calculation details</span></span>
1. <span data-ttu-id="9d648-115">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9d648-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="9d648-116">คลิกดูรายละเอียดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9d648-116">Click View calculation details.</span></span>
    * <span data-ttu-id="9d648-117">หน้านี้แสดงการแบ่งต้นทุน </span><span class="sxs-lookup"><span data-stu-id="9d648-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="9d648-118">ตัวอย่างเช่น คุณสามารถดูราคาต้นทุนรวมต่อหน่วยสำหรับสินค้าที่สำเร็จแล้วได้ในแถวแรก </span><span class="sxs-lookup"><span data-stu-id="9d648-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="9d648-119">ในแถวต่อมาประกอบด้วยต้นทุนตามสูตรการผลิต กระบวนการผลิต และต้นทุนทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="9d648-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  

