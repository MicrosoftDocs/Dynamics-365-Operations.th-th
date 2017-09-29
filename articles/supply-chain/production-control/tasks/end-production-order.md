--- 
title: "ใบสั่งผลิตสิ้นสุด"
description: "กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต "
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="end-a-production-order"></a><span data-ttu-id="ac403-103">ใบสั่งผลิตสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="ac403-103">End a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac403-104">กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="ac403-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="ac403-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ac403-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ac403-106">นี่เป็นขั้นตอนสุดท้ายจากเจ็ดขั้นตอนซึ่งอธิบายวงจรชีวิตของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="ac403-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="ac403-107">ใบสั่งผลิตสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="ac403-107">End a production order</span></span>
1. <span data-ttu-id="ac403-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="ac403-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="ac403-109">เลือกใบสั่งผลิตที่มีสถานะรายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ac403-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="ac403-110">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="ac403-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="ac403-111">คลิกสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="ac403-111">Click End.</span></span>
    * <span data-ttu-id="ac403-112">ในหน้านี้ คุณสามารถยืนยันว่าคุณต้องการสิ้นสุดใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="ac403-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="ac403-113">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="ac403-113">Click the General tab.</span></span>
5. <span data-ttu-id="ac403-114">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ac403-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="ac403-115">ในฟิลด์วิธีการคิดค่าของเสีย ให้เลือก'การปันส่วน' </span><span class="sxs-lookup"><span data-stu-id="ac403-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="ac403-116">เมื่อคุณเลือกวิธีการปันส่วน ต้นทุนจากวัสดุที่เป็นของเสียจะถูกเพิ่มไปยังสินค้าที่สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="ac403-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="ac403-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ac403-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="ac403-118">ตรวจสอบความถูกต้องของผลลัพธ์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="ac403-118">Validate calculation results</span></span>
1. <span data-ttu-id="ac403-119">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ac403-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="ac403-120">คลิกดูการเปรียบเทียบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ac403-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="ac403-121">หลังจากที่คุณสิ้นสุดใบสั่งผลิตแล้ว คุณสามารถเปรียบเทียบราคาต้นทุนประมาณกับราคาต้นทุนที่รับรู้ได้ เพื่อเรียกดูภาพรวมของผลต่างการผลิต</span><span class="sxs-lookup"><span data-stu-id="ac403-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


