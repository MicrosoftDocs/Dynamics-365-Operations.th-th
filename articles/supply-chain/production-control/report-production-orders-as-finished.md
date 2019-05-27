---
title: รายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์
description: รายงานเมื่อเสร็จสมบุรณ์เป็นขั้นการผลิต ในขั้นนี้ ผลิตภัณฑ์สำเร็จรูปจะได้รับการรายงานและย้ายออกจากใบสั่งผลิตไปยังสินค้าคงคลัง
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c12ee3a831abcb46af18645eba55fe100c99c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567409"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="cc021-104">รายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc021-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc021-105">รายงานเมื่อเสร็จสมบุรณ์เป็นขั้นการผลิต</span><span class="sxs-lookup"><span data-stu-id="cc021-105">Report as finished is a production stage.</span></span> <span data-ttu-id="cc021-106">ในขั้นนี้ ผลิตภัณฑ์สำเร็จรูปจะได้รับการรายงานและย้ายออกจากใบสั่งผลิตไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cc021-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="cc021-107">เมื่อปริมาณของสินค้าสำเร็จรูปถูกบันทึกลงรายงานการเสร็จงานในใบสั่งผลิต ก็จะมีการอัพเดทคงเหลือในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cc021-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="cc021-108">และสามารถรายงานปริมาณบางส่วนตามใบสั่งผลิตที่วางแผนไว้ในตอนแรกเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc021-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="cc021-109">และยังสามารถรายงานปริมาณข้อผิดพลาดด้วยเหตุผลของข้อผิดพลาดซึ่งเกี่ยวเนื่องกันเมื่อการรายงานปริมาณเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="cc021-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="cc021-110">เมื่อใบสั่งผลิตไปถึงขั้นรายงานการเสร็จสมบูรณ์ ก็จะบ่งชี้ว่าจะไม่มีปริมาณอื่นใดที่จะรายงานอีกแล้วในการสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="cc021-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="cc021-111">ลักษณะต่อไปนี้จะเกี่ยวข้องกับการ **รายงานกระบวนการเสร็จงาน**</span><span class="sxs-lookup"><span data-stu-id="cc021-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="cc021-112">สามารถตั้งค่าปริมาณการใช้วัตถุดิบและเวลาที่เป็นสัดส่วนกับปริมาณที่รายงาน (การล้างย้อนกลับ)</span><span class="sxs-lookup"><span data-stu-id="cc021-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="cc021-113">คุณสามารถสร้างงานการสำรองสินค้าสำหรับสินค้าที่เปิดใช้งานสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cc021-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="cc021-114">มูลค่าต้นทุนที่วางแผนไว้หรือมาตรฐานของสินค้าสำเร็จรูปสามารถตั้งค่าที่จะรายงานไปยังบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="cc021-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="cc021-115">สามารถสร้างใบสั่งตรวจสอบคุณภาพสำหรับปริมาณที่รายงานโดยยึดตามการตั้งค่าความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cc021-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="cc021-116">ปริมาณสินค้าจะถูกรายงานไปยังที่ผลิตสินค้า</span><span class="sxs-lookup"><span data-stu-id="cc021-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="cc021-117">จากนั้นคลังสินค้าจะย้ายปริมาณสินค้าจากที่ผลิตสินค้าไปยังที่ตั้งปลายทางซึ่งกำหนดให้เป็นที่เก็บสินค้า</span><span class="sxs-lookup"><span data-stu-id="cc021-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="cc021-118">ใบสั่งตรวจสอบคุณภาพสามารถสร้างได้เมื่อใบสั่งผลิตเป็นรายงานการเสร็จงานในกรณีที่มีการตั่งค่าความเกี่ยวเนื่องด้านคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cc021-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="cc021-119">รายงานการการผลิตสินค้าที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="cc021-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="cc021-120">คุณสามารถตั้งค่าใบสั่งผลิตเป็น **รายงานการเสร็จงาน** ผ่านทาง ฟังก์ชันการอัพเดทใบสั่งผลิตมาตรฐาน หรือผ่าน ทางสมุดรายวันและบัตรกระบวนการผลิตตลอดจน บันทึกรายวัน **เมื่องานเสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cc021-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="cc021-121">คุณยังสามารถอัพเดทระยะสำหรับ **รายงานการเสร็จงาน** รวมถึงบัตรงานและหน้าอุปกรณ์บัตรงาน เมื่อรายงานงานล่าสุดของใบสั่งผลิตได้</span><span class="sxs-lookup"><span data-stu-id="cc021-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="cc021-122">ท้ายนี้ คุณสามารถใช้ **รายงานการเสร็จงาน** อันเป็นกระบวนการสำหรับบริการตอบคำถามที่เป็นอุปกรณ์บนมือถือคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="cc021-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  



