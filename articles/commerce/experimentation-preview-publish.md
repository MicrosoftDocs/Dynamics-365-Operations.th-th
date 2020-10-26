---
title: แสดงตัวอย่างและเผยแพร่การทดสอบ
description: หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองจาก Dynamics 365 Commerce
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930301"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="eb2cc-103">แสดงตัวอย่างและเผยแพร่การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="eb2cc-103">Preview and publish an experiment</span></span>

<span data-ttu-id="eb2cc-104">หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองใน Dynamics 365 Commerce หลังจากที่คุณ [เชื่อมต่อการทดลองและแก้ไขการเปลี่ยนแปลงของคุณแล้ว](experimentation-connect-edit.md)</span><span class="sxs-lookup"><span data-stu-id="eb2cc-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="eb2cc-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="eb2cc-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="eb2cc-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="eb2cc-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="eb2cc-107">[ ![การเดินทางของผู้ใช้การทดลอง - ดูตัวอย่างและเผยแพร่](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="eb2cc-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="eb2cc-108">แสดงตัวอย่างการเปลี่ยนแปลงการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="eb2cc-108">Preview your experiment variations</span></span>
<span data-ttu-id="eb2cc-109">คุณสามารถแสดงตัวอย่างการเปลี่ยนแปลงของคุณ และแก้ไขต่อไปจนกว่าจะเหมือนแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="eb2cc-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="eb2cc-110">ในโปรแกรมสร้างไซต์ ให้ใช้เมนูแบบหล่นลงของการเปลี่ยนแปลงด้านล่างแถบคำสั่ง เพื่อเลือกเนื้อหาที่คุณต้องการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="eb2cc-111">เลือก **การแสดงตัวอย่าง** ในแถบด้านบน</span><span class="sxs-lookup"><span data-stu-id="eb2cc-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="eb2cc-112">ตัวอย่างของลักษณะเนื้อหาที่จะปรากฏเมื่อการเผยแพร่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="eb2cc-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="eb2cc-113">เมื่อต้องการแสดงตัวอย่างรูปแบบอื่น ให้เลือกจากแบบหล่นลงของการเปลี่ยนแปลง และเลือก **แสดงตัวอย่าง** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="eb2cc-114">เผยแพร่การทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="eb2cc-114">Publish your experiment</span></span>
<span data-ttu-id="eb2cc-115">ถ้าคุณไม่ได้ใช้กลุ่มเผยแพร่เพื่อกำหนดตารางเวลา เมื่อการทดลองของคุณใช้งานจริง และคุณต้องการเผยแพร่ทันที ให้เลือก **เผยแพร่** ในแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="eb2cc-116">การเปลี่ยนแปลงทั้งหมดที่เป็นของการทดลองจะถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="eb2cc-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="eb2cc-117">ถ้าหน้ามี URL ที่ยังไม่ได้เผยแพร่ คุณต้องเผยแพร่ URL ก่อน หรือไม่งั้นผู้ใช้เว็บไซต์ของคุณจะไม่สามารถมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="eb2cc-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="eb2cc-118">สำหรับรายละเอียด ให้ดูที่ [บันทึก แสดงตัวอย่าง และเผยแพร่หน้า](save-preview-publish-page.md)</span><span class="sxs-lookup"><span data-stu-id="eb2cc-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="eb2cc-119">ใช้กลุ่มเผยแพร่เพื่อกำหนดเวลาที่การทดลองของคุณใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="eb2cc-120">การเปลี่ยนแปลงที่สร้างขึ้นในตัวสร้างไซต์สามารถจัดกำหนดการสำหรับการเผยแพร่โดยใช้กลุ่มเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="eb2cc-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="eb2cc-121">ภายในกลุ่มเผยแพร่ คุณสามารถเชื่อมต่อหน้าหรือส่วนกับการทดลองของคุณได้ โดยไปที่แท็บ **การทดลอง** หรือแท็บ **หน้า** หรือ **ส่วน** สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อ [เชื่อมต่อการทดสอบและแก้ไขการเปลี่ยนแปลง](experimentation-connect-edit.md)</span><span class="sxs-lookup"><span data-stu-id="eb2cc-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="eb2cc-122">สำหรับข้อมูลเกี่ยวกับกลุ่มเผยแพร่ ให้ดูที่ [ทำงานกับกลุ่มเผยแพร่](publish-groups.md)</span><span class="sxs-lookup"><span data-stu-id="eb2cc-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="eb2cc-123">เมื่อใช้กลุ่มเผยแพร่ที่มีการทดลอง มีข้อควรพิจารณาที่สำคัญบางประการที่ควรระวัง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="eb2cc-124">เมื่อคุณเพิ่มหน้าหรือส่วนต่างๆ ที่มีการทดลองรันบนกลุ่มเผยแพร่ การทดลองจะถูกลบออกจากหน้าหรือส่วนในกลุ่มเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="eb2cc-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="eb2cc-125">การทดลองที่มีการเชื่อมต่อกับหน้าในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับหน้าภายในกลุ่มเผยแพร่ และในทางกลับกันด้วย</span><span class="sxs-lookup"><span data-stu-id="eb2cc-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="eb2cc-126">ในทำนองเดียวกัน หน้าที่มีการทดลองทำงานอยู่ในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับการทดลองอื่นๆ ในกลุ่มเผยแพร่ และในทางกลับกันด้วย</span><span class="sxs-lookup"><span data-stu-id="eb2cc-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="eb2cc-127">เมื่อคุณเผยแพร่หรือจัดกำหนดการกลุ่มเผยแพร่ เนื้อหาทั้งหมดในกลุ่มเผยแพร่จะถูกเผยแพร่โดยไม่คำนึงว่ามีการทดสอบที่เกี่ยวข้องกับกลุ่มเผยแพร่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="eb2cc-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="eb2cc-128">เนื่องจากกลุ่มเผยแพร่ยังคงแสดงหลังจากที่มีการเผยแพร่ไปยังไซต์ที่ใช้งานจริง การทดลองในกลุ่มเผยแพร่จะยังคงแสดงด้วย</span><span class="sxs-lookup"><span data-stu-id="eb2cc-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="eb2cc-129">ดังนั้น คุณจึงไม่สามารถเชื่อมโยงการทดลองอื่นๆ กับหน้าหรือส่วนเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="eb2cc-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="eb2cc-130">ถ้าต้องการหลีกเลี่ยงข้อจำกัดนี้ ให้ลบกลุ่มเผยแพร่ใดๆ ที่มีการทดลองการแสดง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="eb2cc-131">ในทำนองเดียวกัน ถ้าคุณต้องการลบการทดลองในไซต์ที่ใช้งานจริงที่มีอยู่ในกลุ่มเผยแพร่ ให้ลบออกจากกลุ่มเผยแพร่ก่อน</span><span class="sxs-lookup"><span data-stu-id="eb2cc-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="eb2cc-132">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="eb2cc-132">Previous step</span></span>
[<span data-ttu-id="eb2cc-133">เชื่อมต่อและแก้ไขการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="eb2cc-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="eb2cc-134">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="eb2cc-134">Next step</span></span>
[<span data-ttu-id="eb2cc-135">รันและตรวจสอบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="eb2cc-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
