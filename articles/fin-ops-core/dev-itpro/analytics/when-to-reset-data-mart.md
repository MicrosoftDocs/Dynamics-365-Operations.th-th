---
title: เมื่อใดที่จะรีเซ็ต Data Mart
description: หัวข้อนี้แสดงรายการสถานการณ์ที่อาจมีการปรับปรุงด้วยการรีเซ็ต Data Mart และสถานการณ์ที่การรีเซ็ต Data Mart เป็นไปได้ยาก
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093223"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="e05c1-103">เมื่อใดที่จะรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="e05c1-103">When to reset a data mart</span></span>

<span data-ttu-id="e05c1-104">การรีเซ็ต Data Mart อาจใช้เวลานาน</span><span class="sxs-lookup"><span data-stu-id="e05c1-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="e05c1-105">ทั้งนี้ขึ้นอยู่กับสถานการณ์ การดำเนินการนี้อาจรจะไม่ใช่โซลูชันที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e05c1-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="e05c1-106">หัวข้อนี้แสดงรายการสถานการณ์ที่อาจมีการปรับปรุงด้วยการรีเซ็ต Data Mart และสถานการณ์ที่การรีเซ็ต Data Mart เป็นไปได้ยาก</span><span class="sxs-lookup"><span data-stu-id="e05c1-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="e05c1-107">คุณต้องการรีเซ็ต Data Mart เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="e05c1-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="e05c1-108">พิจารณาคำถามต่อไปนี้ก่อนการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="e05c1-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="e05c1-109">การตอบว่าใช่กับคําถามหนึ่งคําถามหรือมากกว่าอาจบ่งชี้ว่าองค์กรของคุณสามารถได้รับประโยชน์จากการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="e05c1-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="e05c1-110">มีการคืนค่าฐานข้อมูลใบสมัคร แต่ไม่ได้รับการคืนค่าฐานข้อมูล Data Mart</span><span class="sxs-lookup"><span data-stu-id="e05c1-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="e05c1-111">คุณจะเห็นข้อมูลที่ไม่ถูกต้องในรอบระยะเวลาทางบัญชี ซึ่งไม่ใช่ผลลัพธ์ของการตัดสินค้าจากคลังที่มีการออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="e05c1-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="e05c1-112">คุณจะเห็นข้อมูลที่ไม่ถูกต้องในรอบระยะเวลาทางบัญชี และเรกคอร์ดแสดงรายการอยู่ภายใต้ความพยายามในการรวมในหน้า **สถานะการรวม** ในรายงานผู้ออกแบบรายงาน (เริ่มต้นโปรแกรมออกแบบรายงาน และเลือก **เครื่องมือ > สถานะการรวม**)</span><span class="sxs-lookup"><span data-stu-id="e05c1-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="e05c1-113">คุณได้เปิดเหตุการณ์สนับสนุนและวิศวกรฝ่ายสนับสนุนแนะนำให้คุณสามารถรีเซ็ต Data Mart โดยเป็นส่วนหนึ่งของขั้นตอนการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="e05c1-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="e05c1-114">เมื่อใดที่การรีเซ็ต Data Mart ไม่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e05c1-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="e05c1-115">มีบางสถานการณ์ที่เราไม่แนะนำให้รีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="e05c1-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="e05c1-116">ได้แก่สิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e05c1-116">These include the following.</span></span> 

- <span data-ttu-id="e05c1-117">เมื่อใดก็ตามที่เหตุผลไม่ปรากฏอยู่ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="e05c1-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="e05c1-118">คุณประสบปัญหาด้านประสิทธิภาพที่เชื่อมโยงกับการซิงค์ข้อมูล ในกรณีนี้ การรีเซ็ต Data Mart อาจไม่ช่วย</span><span class="sxs-lookup"><span data-stu-id="e05c1-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="e05c1-119">ถ้าคุณมีรูปแบบการรีเซ็ตที่เกิดเหตุการณ์ที่เกิดขึ้นเป็นชุดเนื่องจากเหตุผลใด ๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e05c1-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="e05c1-120">**ข้อมูลขาดหาย** - ก่อนอื่น ให้ตัดปัญหาการออกแบบรายงานและปัญหาการซิงค์ข้อมูล ตัวอย่างเช่น คุณสังเกตว่ายังไม่ได้รันแผนผังข้อเท็จจริง เนื่องจากไม่มีการลงรายการบัญชีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e05c1-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="e05c1-121">**สถานะการรวมที่ติดขัด** - ถ้าการรวมช้าหรือที่ติดขัด การรีเซ็ต Data Mart เป็นไปได้ที่จะไม่แก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="e05c1-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="e05c1-122">**ความพยายามที่จะรีเซ็ตไม่สำเร็จ** - ถ้ามีความพยายามหลายครั้งในการรีเซ็ตให้เสร็จสมบูรณ์ และไม่สำเร็จเนื่องจากข้อมูลขาดหายไป เราขอแนะนำให้เปิดเหตุการณ์สนับสนุนและทำงานกับวิศวกรฝ่ายสนับสนุนเพื่อวิเคราะห์สถานการณ์ของคุณก่อนที่จะพยายามรีเซ็ตข้อมูลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e05c1-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="e05c1-123">**เรกคอร์ดเก่า** - เรกคอร์ดเก่าอย่างเดียวไม่อาจพิสูจน์ได้ว่าควรรีเซ็ต Data Mart หรือไม่</span><span class="sxs-lookup"><span data-stu-id="e05c1-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="e05c1-124">ถ้าคุณมีชุดข้อมูลขนาดใหญ่ กระบวนการรีเซ็ตจะใช้เวลาในกรเรียกใช้ แต่ไม่อาจส่งผลต่อการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="e05c1-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="e05c1-125">สิ่งที่การรีเซ็ต Data Mart ไม่ทำ</span><span class="sxs-lookup"><span data-stu-id="e05c1-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="e05c1-126">การรีเซ็ตจะเริ่มต้นเฉพาะเมื่องานที่มีอยู่เสร็จสมบูรณ์แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e05c1-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="e05c1-127">ซึ่งช่วยให้มั่นใจว่าจะไม่แทรกข้อมูลเก่าเข้ามา</span><span class="sxs-lookup"><span data-stu-id="e05c1-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="e05c1-128">ณ จุดนี้ คุณอาจเห็นข้อความ เช่น "ไม่สามารถประมวลผลการรีเซ็ต Data Mart เนื่องจากงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e05c1-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="e05c1-129">โปรดลองอีกครั้งในภายหลัง"</span><span class="sxs-lookup"><span data-stu-id="e05c1-129">Please try again later.”</span></span>
- <span data-ttu-id="e05c1-130">การรีเซ็ตจะปิดใช้งานงานการรวมและลบข้อมูล Data Mart ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e05c1-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="e05c1-131">การรวมจะเปิดใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e05c1-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="e05c1-132">จุดต่อไปนี้จะระบุสองสิ่งที่การรีเซ็ต Data Mart *ไม่* ทำ</span><span class="sxs-lookup"><span data-stu-id="e05c1-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="e05c1-133">การรีเซ็ตไม่ลบการออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="e05c1-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="e05c1-134">การรีเซ็ตจะไม่ล้างข้อมูลบริษัทหรือข้อมูลผู้ใช้ยกเว้นว่าเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="e05c1-134">Resets do not clear company data or user data unless selected.</span></span>
