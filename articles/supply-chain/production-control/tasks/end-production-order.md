---
title: ใบสั่งผลิตสิ้นสุด
description: 'กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 994f4ca578de970876f714bb397afeea1f39c15c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240352"
---
# <a name="end-a-production-order"></a><span data-ttu-id="984b8-103">ใบสั่งผลิตสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="984b8-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="984b8-104">กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="984b8-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="984b8-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="984b8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="984b8-106">นี่เป็นขั้นตอนสุดท้ายจากเจ็ดขั้นตอนซึ่งอธิบายวงจรชีวิตของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="984b8-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="984b8-107">ใบสั่งผลิตสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="984b8-107">End a production order</span></span>
1. <span data-ttu-id="984b8-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="984b8-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="984b8-109">เลือกใบสั่งผลิตที่มีสถานะรายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="984b8-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="984b8-110">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="984b8-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="984b8-111">คลิกสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="984b8-111">Click End.</span></span>
    * <span data-ttu-id="984b8-112">ในหน้านี้ คุณสามารถยืนยันว่าคุณต้องการสิ้นสุดใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="984b8-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="984b8-113">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="984b8-113">Click the General tab.</span></span>
5. <span data-ttu-id="984b8-114">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="984b8-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="984b8-115">ในฟิลด์วิธีการคิดค่าของเสีย ให้เลือก'การปันส่วน' </span><span class="sxs-lookup"><span data-stu-id="984b8-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="984b8-116">เมื่อคุณเลือกวิธีการปันส่วน ต้นทุนจากวัสดุที่เป็นของเสียจะถูกเพิ่มไปยังสินค้าที่สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="984b8-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="984b8-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="984b8-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="984b8-118">ตรวจสอบความถูกต้องของผลลัพธ์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="984b8-118">Validate calculation results</span></span>
1. <span data-ttu-id="984b8-119">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="984b8-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="984b8-120">คลิกดูการเปรียบเทียบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="984b8-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="984b8-121">หลังจากที่คุณสิ้นสุดใบสั่งผลิตแล้ว คุณสามารถเปรียบเทียบราคาต้นทุนประมาณกับราคาต้นทุนที่รับรู้ได้ เพื่อเรียกดูภาพรวมของผลต่างการผลิต</span><span class="sxs-lookup"><span data-stu-id="984b8-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]