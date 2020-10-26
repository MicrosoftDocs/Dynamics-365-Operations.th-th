---
title: รันและตรวจสอบการทดสอบ
description: หัวข้อนี้อธิบายวิธีการรันและตรวจสอบการทดลองในบริการของบุคคลที่สาม นอกจากนี้ยังอธิบายถึงวิธีการทำการเปลี่ยนแปลงรูปแบบหลังจากที่เริ่มต้นการทดลอง
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930299"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="c632c-104">รันและตรวจสอบการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c632c-104">Run and monitor an experiment</span></span>

<span data-ttu-id="c632c-105">หัวข้อนี้อธิบายวิธีการรันและตรวจสอบการทดลองของคุณในแอปของบุคคลที่สาม และเปลี่ยนแปลงรูปแบบถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="c632c-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="c632c-106">ก่อนที่คุณจะดำเนินการขั้นตอนในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณจะต้อง [เผยแพร่](experimentation-preview-publish.md) การทดลองของคุณใน Commerce</span><span class="sxs-lookup"><span data-stu-id="c632c-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="c632c-107">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c632c-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c632c-108">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c632c-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="c632c-109">[ ![การเดินทางของผู้การทดสอบใช้ - รันและตรวจสอบ](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c632c-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="c632c-110">หลังจากที่คุณเผยแพร่การเปลี่ยนแปลงแล้ว ขั้นตอนทั้งหมดที่คุณต้องทำใน Commerce เพื่อรันการทดลองของคุณเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="c632c-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="c632c-111">ขั้นตอนต่อไปคือการกำหนดรูปแบบที่จะแสดงให้กับผู้ใช้แต่ละคนเมื่อร้องขอหน้า</span><span class="sxs-lookup"><span data-stu-id="c632c-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="c632c-112">บริการของบุคคลที่สามทำให้เกิดการกำหนดนั้น แต่ก่อนอื่น คุณจะต้องเรียกใช้งานการทดลองภายในบริการ</span><span class="sxs-lookup"><span data-stu-id="c632c-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="c632c-113">เนื่องจากขั้นตอนสำหรับการเรียกใช้การทดลองจะแตกต่างกันไปในแต่ละบริการ คุณจะต้องทำตามคำแนะนำที่มาพร้อมกับบริการหรือผู้ให้บริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="c632c-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="c632c-114">ถ้าไม่ได้เรียกใช้งานการทดลอง ผู้ใช้จะเห็นเฉพาะรุ่นเริ่มต้นของหน้า - ไม่มีการเปลี่ยนแปลงแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c632c-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="c632c-115">คุณจำเป็นต้องให้การทดลองรันนานพอที่จะรวบรวมข้อมูล เพื่อให้ได้ผลลัพธ์ที่ถูกต้องทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="c632c-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="c632c-116">ใช้บริการของบุคคลที่สามเพื่อตรวจสอบข้อมูลที่เกี่ยวข้องกับการทดลองและการวิเคราะห์ ในขณะที่กำลังรันการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c632c-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="c632c-117">ปรับปรุงการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="c632c-117">Adjust your variations</span></span>
<span data-ttu-id="c632c-118">ถ้าคุณต้องการแก้ไขความเปลี่ยนแปลงใดๆ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c632c-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c632c-119">ถ้าคุณทำการเปลี่ยนแปลงการทดลองใช้งานจริงใน Commerce หรือบริการของบุคคลที่สาม ผลลัพธ์ของคุณอาจได้รับผลกระทบอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="c632c-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="c632c-120">พิจารณาให้ทดลองรันหลักสูตรของการทดลอง และสร้างการทดลองใหม่สำหรับการเปลี่ยนแปลงที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="c632c-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="c632c-121">ไปที่แท็บ **การทดลอง** ในโปรแกรมสร้างไซต์ แล้วเลือกการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c632c-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="c632c-122">เลือกการเปลี่ยนแปลงที่คุณต้องการอัปเดตจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c632c-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="c632c-123">ทำการเปลี่ยนแปลงที่จำเป็น แล้วแสดงตัวอย่าง และเผยแพร่การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c632c-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="c632c-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [แสดงตัวอย่างและเผยแพร่การทดลอง](experimentation-preview-publish.md)</span><span class="sxs-lookup"><span data-stu-id="c632c-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="c632c-125">ไปที่บริการของบุคคลที่สามเพื่อทำการเปลี่ยนแปลงที่เกี่ยวข้องกับการตั้งค่าการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c632c-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="c632c-126">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="c632c-126">Previous step</span></span>
[<span data-ttu-id="c632c-127">แสดงตัวอย่างและเผยแพร่การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c632c-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="c632c-128">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="c632c-128">Next step</span></span>
[<span data-ttu-id="c632c-129">โปรโมทการเปลี่ยนแปลงและทำการทดสอบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c632c-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
