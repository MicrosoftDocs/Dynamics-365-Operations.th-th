---
title: เมื่อใดที่จะรีเซ็ต Data Mart
description: หัวข้อนี้แสดงรายการสถานการณ์ที่อาจมีการปรับปรุงด้วยการรีเซ็ต Data Mart และสถานการณ์ที่การรีเซ็ต Data Mart เป็นไปได้ยาก
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2021
ms.locfileid: "5989003"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="a7e93-103">เมื่อใดที่จะรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-103">When to reset a data mart</span></span>

<span data-ttu-id="a7e93-104">การรีเซ็ต Data Mart อาจใช้เวลานาน</span><span class="sxs-lookup"><span data-stu-id="a7e93-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="a7e93-105">ทั้งนี้ขึ้นอยู่กับสถานการณ์ การดำเนินการนี้อาจรจะไม่ใช่โซลูชันที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a7e93-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="a7e93-106">หัวข้อนี้แสดงรายการสถานการณ์ที่อาจมีการปรับปรุงด้วยการรีเซ็ต Data Mart และสถานการณ์ที่การรีเซ็ต Data Mart เป็นไปได้ยาก</span><span class="sxs-lookup"><span data-stu-id="a7e93-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="a7e93-107">ฉันต้องรีเซ็ต Data Mart เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="a7e93-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="a7e93-108">พิจารณาคำถามต่อไปนี้ก่อนการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="a7e93-109">การตอบว่าใช่กับคําถามหนึ่งคําถามหรือมากกว่าอาจบ่งชี้ว่าองค์กรของคุณสามารถได้รับประโยชน์จากการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="a7e93-110">ฐานข้อมูลแอปพลิเคชันคืนค่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7e93-110">Was the application database restored?</span></span>
- <span data-ttu-id="a7e93-111">หากคุณได้เปิดเหตุการณ์สนับสนุนและวิศวกรฝ่ายสนับสนุนแนะนำให้คุณสามารถรีเซ็ต Data Mart โดยเป็นส่วนหนึ่งของขั้นตอนการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a7e93-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="a7e93-112">เมื่อใดที่การรีเซ็ต Data Mart ไม่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="a7e93-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="a7e93-113">มีบางสถานการณ์ที่เราไม่แนะนำให้รีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="a7e93-114">ได้แก่สิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a7e93-114">These include the following.</span></span> 

- <span data-ttu-id="a7e93-115">คุณประสบปัญหาด้านประสิทธิภาพที่เกี่ยวข้องกับการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a7e93-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="a7e93-116">ถ้าคุณมีรูปแบบการรีเซ็ตที่เกิดเหตุการณ์ที่เกิดขึ้นเป็นชุดเนื่องจากเหตุผลใด ๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7e93-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="a7e93-117">**ข้อมูลขาดหาย**</span><span class="sxs-lookup"><span data-stu-id="a7e93-117">**Missing data**</span></span> 
  - <span data-ttu-id="a7e93-118">**สถานะการรวมที่ติดขัด**</span><span class="sxs-lookup"><span data-stu-id="a7e93-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="a7e93-119">**เรกคอร์ดเก่า** - เรกคอร์ดเก่าอย่างเดียวไม่อาจพิสูจน์ได้ว่าควรรีเซ็ต Data Mart หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7e93-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="a7e93-120">ถ้าคุณมีชุดข้อมูลขนาดใหญ่ กระบวนการรีเซ็ตจะใช้เวลาในกรเรียกใช้ แต่ไม่อาจส่งผลต่อการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a7e93-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="a7e93-121">การรีเซ็ต Data Mart คืออะไร</span><span class="sxs-lookup"><span data-stu-id="a7e93-121">What is a data mart reset?</span></span>
- <span data-ttu-id="a7e93-122">การรีเซ็ตจะเริ่มต้นเฉพาะเมื่องานที่มีอยู่เสร็จสมบูรณ์แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a7e93-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="a7e93-123">ซึ่งช่วยให้มั่นใจว่าจะไม่แทรกข้อมูลเก่าเข้ามา</span><span class="sxs-lookup"><span data-stu-id="a7e93-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="a7e93-124">ณ จุดนี้ คุณอาจเห็นข้อความ เช่น "ไม่สามารถประมวลผลการรีเซ็ต Data Mart เนื่องจากงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="a7e93-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="a7e93-125">โปรดลองอีกครั้งในภายหลัง"</span><span class="sxs-lookup"><span data-stu-id="a7e93-125">Please try again later.”</span></span>
- <span data-ttu-id="a7e93-126">การรีเซ็ตจะปิดใช้งานงานการรวมและลบข้อมูล Data Mart ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a7e93-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="a7e93-127">การรวมจะเปิดใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a7e93-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="a7e93-128">ถ้าฉันรีเซ็ต Data Mart ฉันจะสูญเสียรายงานที่ออกแบบไว้แล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7e93-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="a7e93-129">ไม่ รายงานของคุณถูกจัดเก็บไว้ในตาราง SQL ที่ไม่ได้รับผลกระทบจากการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="a7e93-130">ถ้าคุณกังวลเกี่ยวกับการสูญเสียรายงานใด ๆ ที่คุณออกแบบ คุณสามารถสำรองข้อมูลการออกแบบที่คุณไม่ต้องการสูญเสียได้</span><span class="sxs-lookup"><span data-stu-id="a7e93-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="a7e93-131">เมื่อต้องการสำรองข้อมูล ให้เปิดตัวออกแบบรายงาน และไปที่ **บริษัท > บริษัท > ส่วนประกอบ > ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="a7e93-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="a7e93-132">ผู้ใช้ทั้งหมดต้องออกจากระบบเพื่อรีเซ็ต Data Mart หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7e93-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="a7e93-133">ไม่ ผู้ใช้สามารถทำงานในระบบต่อไปได้ในระหว่างการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="a7e93-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="a7e93-134">อย่างไรก็ตาม ผู้ใช้จะไม่สามารถเข้าถึงรายงานใด ๆ ที่สร้างขึ้นด้วยโปรแกรมรายงานทางการเงินได้จนกว่าการรีเซ็ตจะเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="a7e93-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
