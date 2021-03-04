---
title: ภาพรวมของการรับรู้รายได้
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับคุณลักษณะการรับรู้รายได้ คุณลักษณะนี้มีกรอบงานที่มีความยืดหยุ่นซึ่งช่วยให้คุณสามารถกำหนดกฎเฉพาะบริษัทสำหรับการรับรู้ราคาสำหรับรายได้และกำหนดการรายได้สำหรับใบสั่งที่มีหลายองค์ประกอบ
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a7e37a0800ec7909f79e5a2354f59c7450995641
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995625"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="43b0e-104">ภาพรวมของการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b0e-105">บริษัทต่างๆ ในอุตสาหกรรมที่จำหน่ายองค์ประกอบหลายอย่าง เช่น ผลิตภัณฑ์ บริการ การสมัครใช้งาน และอื่นๆ ต้องสามารถจำแนกใบสั่งที่มีหลายองค์ประกอบเพื่อให้สามารถรับรู้รายได้ตามชุดหลักเกณฑ์เฉพาะบริษัทหรือเฉพาะอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="43b0e-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="43b0e-106">คุณลักษณะการรับรู้รายได้ไม่สามารถเปิดผ่านทางการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="43b0e-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="43b0e-107">ในตอนนี้ คุณต้องใช้คีย์การตั้งค่าคอนฟิกในการเปิด</span><span class="sxs-lookup"><span data-stu-id="43b0e-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="43b0e-108">การรับรู้รายได้ รวมถึงฟังก์ชันการขายรวมยังไม่รองรับให้ใช้งานในช่องทาง Commerce (อีคอมเมิร์ซ, POS, ศูนย์บริการ)</span><span class="sxs-lookup"><span data-stu-id="43b0e-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="43b0e-109">ไม่ควรเพิ่มสินค้าที่ตั้งค่าคอนฟิกด้วยการรับรู้รายได้ให้กับใบสั่งหรือธุรกรรมที่สร้างในช่องทาง Commerce</span><span class="sxs-lookup"><span data-stu-id="43b0e-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="43b0e-110">โดยทั่วไปแล้ว กระบวนการรับรู้รายได้สามารถใช้ในการดำเนินงานเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="43b0e-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="43b0e-111">ปันส่วนรายได้เพื่อช่วยรับรองว่ามีการรับรู้ราคาสำหรับรายได้ที่เหมาะสมตามมูลค่าของส่วนประกอบต่างๆ ในใบสั่งที่มีหลายองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="43b0e-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="43b0e-112">รอตัดบัญชีรายได้ตามกำหนดการของรายได้ที่แสดงถึงกรอบเวลาตามสัญญาและเปอร์เซ็นต์สำหรับการรับรู้รายได้ตลอดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="43b0e-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="43b0e-113">วิดีโอ [วิธีใช้การรับรู้รายได้ใน Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (ที่แสดงข้างต้น) รวมไว้ใน [เพลย์ลิสต์ Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) ที่อยู่บน YouTube</span><span class="sxs-lookup"><span data-stu-id="43b0e-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="43b0e-114">คุณลักษณะการรับรู้รายได้มีกรอบงานที่มีความยืดหยุ่นซึ่งช่วยให้คุณสามารถกำหนดกฎเฉพาะบริษัทสำหรับการรับรู้ราคาสำหรับรายได้และกำหนดการรายได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="43b0e-115">ผลิตภัณฑ์ที่นำออกใช้แล้วใช้เพื่อสนับสนุนการรับรู้รายได้ในเอกสารของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="43b0e-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="43b0e-116">ผลิตภัณฑ์ที่นำออกใช้แล้วมีการตั้งค่าที่ต้องใช้เพื่อกำหนดราคาสำหรับรายได้และกำหนดการของรายได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="43b0e-117">ใบสั่งขายสามารถเริ่มต้นจากโครงการเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="43b0e-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="43b0e-118">บริษัทต่างๆ สามารถใช้ฟังก์ชันกำหนดการของรายได้ได้โดยไม่ต้องใช้ฟังก์ชันราคาสำหรับรายได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="43b0e-119">ดังนั้น ราคาในรายการของใบสั่งขายจะใช้เป็นรายได้หรือรายได้รอการตัดบัญชีอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="43b0e-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="43b0e-120">หากมีกำหนดการของรายได้อยู่ในรายการของใบสั่งขาย ราคาในรายการของใบสั่งขายจะใช้เป็นรอการตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="43b0e-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="43b0e-121">หากไม่มีกำหนดการของรายได้อยู่ในรายการของใบสั่งขาย ราคาในรายการของใบสั่งขายจะได้รับการลงรายการบัญชีในบัญชีรายได้เมื่อมีการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="43b0e-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="43b0e-122">ราคาสำหรับรายได้จะมีการคำนวณเมื่อใบสั่งขายได้รับการยืนยันหรือเมื่อมีการลงรายการบัญชีใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="43b0e-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="43b0e-123">หากต้องการดูตัวอย่างราคาสำหรับรายได้ก่อนที่จะลงรายการบัญชีใบแจ้งหนี้ คุณต้องยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="43b0e-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="43b0e-124">เมื่อใบสั่งขายได้รับการยืนยันแล้ว กำหนดการของรายได้ที่คาดไว้จะได้รับการสร้างด้วยหากรายการของใบสั่งขายมีกำหนดการของรายได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="43b0e-125">เมื่อใบสั่งขายได้รับการออกใบแจ้งหนี้แล้ว จะมีการลบกำหนดการของรายได้ที่คาดไว้ และมีการแทนที่กำหนดการของรายได้ที่คาดไว้ด้วยกำหนดการการรับรู้รายได้จริง</span><span class="sxs-lookup"><span data-stu-id="43b0e-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="43b0e-126">รายละเอียดของกำหนดการการรับรู้รายได้สำหรับรายการของใบสั่งขายแต่ละรายการยังสามารถรักษาไว้ได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="43b0e-127">ดังนั้น ผู้จัดการฝ่ายการรับรู้รายได้จะสามารถดูรายละเอียดและสามารถปล่อยรายการไปสู่รายได้เมื่ข้อผูกมัดตามสัญญาเสร็จสมบูรณ์ลง</span><span class="sxs-lookup"><span data-stu-id="43b0e-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="43b0e-128">เมื่อสิ้นสุดรอบระยะเวลาแต่ละรอบ ผู้จัดการฝ่ายการรับรู้รายได้สามารถสร้างสมุดรายวันรายได้เพื่อปลดรายการในกำหนดการที่ถึงกำหนดในวันที่หรือก่อนวันที่ซึ่งพวกเขากำหนดได้</span><span class="sxs-lookup"><span data-stu-id="43b0e-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="43b0e-129">สมุดรายวันรายได้นี้จะไม่ได้รับการลงรายการบัญชีในทันที</span><span class="sxs-lookup"><span data-stu-id="43b0e-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="43b0e-130">ดังนั้น ผู้จัดการฝ่ายการรับรู้รายได้จะสามารถตรวจสอบว่าจำนวนเงินที่ปล่อยออกจากรายได้รอการตัดบัญชีไปยังรายได้จริงนั้นถูกต้องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="43b0e-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="43b0e-131">หากการเปลี่ยนแปลงตามสัญญาทำให้มีการเพิ่มรายการของใบสั่งขายลงในใบสั่งขายที่มีอยู่หรือใบสั่งขายใหม่ สามารถดำเนินกระบวนการในการปันส่วนใหม่เพื่อแก้ไขราคาสำหรับรายได้ในรายการทั้งหมดของใบสั่งขายให้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="43b0e-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
