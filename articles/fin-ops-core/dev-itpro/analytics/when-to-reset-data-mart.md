---
title: คำถามที่ถามบ่อยเกี่ยวกับการรีเซ็ต Data Mart
description: หัวข้อนี้แสดงคําตอบของบางคําถามที่ถามบ่อยเกี่ยวกับการรีเซ็ต Data Mart
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266620"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="7dbcf-103">คำถามที่ถามบ่อยเกี่ยวกับการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="7dbcf-103">Data mart resets FAQ</span></span>

<span data-ttu-id="7dbcf-104">หัวข้อนี้แสดงคําตอบของบางคําถามที่ถามบ่อยเกี่ยวกับการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="7dbcf-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="7dbcf-105">การรีเซ็ต Data Mart อาจเป็นกระบวนการที่ใช้เวลานาน และขึ้นอยู่กับสถานการณ์ที่อาจไม่ใช่โซลูชันที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="7dbcf-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="7dbcf-106">ดังนั้นหัวข้อนี้จึงรวมถึงข้อมูลเกี่ยวกับสถานการณ์ที่การรีเซ็ต Data Mart อาจช่วยและสถานการณ์ที่อาจเป็นไปได้ว่าไม่อาจช่วยเหลือได้</span><span class="sxs-lookup"><span data-stu-id="7dbcf-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="7dbcf-107">การรีเซ็ต Data Mart คืออะไร</span><span class="sxs-lookup"><span data-stu-id="7dbcf-107">What is a data mart reset?</span></span>

<span data-ttu-id="7dbcf-108">การรีเซ็ต Data Mart จะปิดใช้งานงานการรวม ลบ Data Mart ทั้งหมด แล้วเปิดใช้งานการรวมอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7dbcf-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="7dbcf-109">เพื่อให้แน่ใจว่าไม่ได้แทรกข้อมูลเก่า สามารถเริ่มต้นการรีเซ็ต Data Mart ได้เฉพาะหลังจากที่งานที่มีอยู่เสร็จสมบูรณ์แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7dbcf-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="7dbcf-110">ถ้าคุณพยายามรีเซ็ต Data Mart ก่อนที่งานทั้งหมดจะเสร็จสิ้น คุณอาจได้รับข้อความ เช่น "การรีเซ็ต Data Mart ไม่สามารถประมวลผลได้เนื่องจากมีงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="7dbcf-111">กรุณาลองใหม่อีกครั้งในภายหลัง"</span><span class="sxs-lookup"><span data-stu-id="7dbcf-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="7dbcf-112">ฉันต้องรีเซ็ต Data Mart เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="7dbcf-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="7dbcf-113">ถ้าข้อความต่อไปนี้อย่างน้อยหนึ่งรายการใช้กับสถานการณ์ของคุณ องค์กรของคุณสามารถได้รับประโยชน์จากการรีเซ็ต Data Mart:</span><span class="sxs-lookup"><span data-stu-id="7dbcf-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="7dbcf-114">ฐานข้อมูลแอปพลิเคชันคืนค่า</span><span class="sxs-lookup"><span data-stu-id="7dbcf-114">The application database was restored.</span></span>
- <span data-ttu-id="7dbcf-115">คุณได้เปิดตั๋วการสนับสนุนและวิศวกรฝ่ายสนับสนุนแนะนำให้คุณสามารถรีเซ็ต Data Mart โดยเป็นส่วนหนึ่งของขั้นตอนการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="7dbcf-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="7dbcf-116">เวลาใดที่การรีเซ็ต Data Mart ไม่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7dbcf-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="7dbcf-117">นี่คือบางสถานการณ์ที่เราไม่แนะนำให้รีเซ็ต Data Mart:</span><span class="sxs-lookup"><span data-stu-id="7dbcf-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="7dbcf-118">คุณประสบปัญหาด้านประสิทธิภาพที่เกี่ยวข้องกับการซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7dbcf-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="7dbcf-119">คุณมีรูปแบบการรีเซ็ตที่เกิดเหตุการณ์ที่เกิดขึ้นเป็นชุดเนื่องจากเหตุผลใด ๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dbcf-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="7dbcf-120">**ข้อมูลขาดหายไป** – ถ้าคุณสังเกตเห็นว่าข้อมูลขาดหายไป ให้เปิดตั๋วสนับสนุนกับ Microsoft เพื่อตรวจทานรูปแบบรายงานของคุณและปัญหาการซิงโครไนส์ข้อมูลที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="7dbcf-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="7dbcf-121">**สถานะการรวมที่ติดขัด**</span><span class="sxs-lookup"><span data-stu-id="7dbcf-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="7dbcf-122">**เรกคอร์ดเก่า** – เรกคอร์ดเก่าอย่างเดียวไม่อาจพิสูจน์ได้ว่าควรรีเซ็ต Data Mart หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="7dbcf-123">ถ้าคุณมีชุดข้อมูลขนาดใหญ่ กระบวนการรีเซ็ตจะใช้เวลาในกรเรียกใช้ แต่ไม่อาจส่งผลต่อการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="7dbcf-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="7dbcf-124">ถ้าฉันรีเซ็ต Data Mart ฉันจะสูญเสียรายงานที่ออกแบบไว้แล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="7dbcf-125">ไม่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-125">No.</span></span> <span data-ttu-id="7dbcf-126">รายงานของคุณถูกจัดเก็บไว้ในตาราง SQL ที่ไม่ได้รับผลกระทบจากการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="7dbcf-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="7dbcf-127">ถ้าคุณกังวลเกี่ยวกับการสูญเสียรายงานใด ๆ ที่คุณออกแบบ คุณสามารถสำรองข้อมูลการออกแบบที่คุณไม่ต้องการสูญเสียได้</span><span class="sxs-lookup"><span data-stu-id="7dbcf-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="7dbcf-128">เมื่อต้องการสำรองการออกแบบ ให้เปิดตัวออกแบบรายงาน และไปที่ **บริษัท \> บริษัท \> ส่วนประกอบ \> ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="7dbcf-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="7dbcf-129">ผู้ใช้ทั้งหมดต้องออกจากระบบก่อน จึงจะสามารถรีเซ็ต Data Mart ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="7dbcf-130">ไม่</span><span class="sxs-lookup"><span data-stu-id="7dbcf-130">No.</span></span> <span data-ttu-id="7dbcf-131">ผู้ใช้สามารถทำงานในระบบต่อไปได้ในระหว่างการรีเซ็ต Data Mart</span><span class="sxs-lookup"><span data-stu-id="7dbcf-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="7dbcf-132">อย่างไรก็ตาม จนกว่าการรีเซ็ตจะเสร็จสิ้น ผู้ใช้จะไม่สามารถเข้าถึงรายงานใด ๆ ที่สร้างขึ้นด้วยโปรแกรมรายงานทางการเงินได้</span><span class="sxs-lookup"><span data-stu-id="7dbcf-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
