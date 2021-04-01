---
title: แสดงตัวอย่างและเผยแพร่การทดสอบ
description: หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองจาก Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b35af35f5d0347192ed94bed51dfd2484cfa481
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238593"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="7d54e-103">แสดงตัวอย่างและเผยแพร่การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="7d54e-103">Preview and publish an experiment</span></span>

<span data-ttu-id="7d54e-104">หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองใน Dynamics 365 Commerce หลังจากที่คุณ [เชื่อมต่อการทดลองและแก้ไขการเปลี่ยนแปลงของคุณแล้ว](experimentation-connect-edit.md)</span><span class="sxs-lookup"><span data-stu-id="7d54e-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="7d54e-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7d54e-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7d54e-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="7d54e-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="7d54e-107">[ ![การเดินทางของผู้ใช้การทดลอง - ดูตัวอย่างและเผยแพร่](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7d54e-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="7d54e-108">แสดงตัวอย่างการเปลี่ยนแปลงการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="7d54e-108">Preview your experiment variations</span></span>
<span data-ttu-id="7d54e-109">คุณสามารถแสดงตัวอย่างการเปลี่ยนแปลงของคุณ และแก้ไขต่อไปจนกว่าจะเหมือนแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d54e-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="7d54e-110">เมื่อต้องการแสดงตัวอย่างการเปลี่ยนแปลงการทดลองของคุณบนไซต์ของคุณในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7d54e-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7d54e-111">จากเมนูแบบหล่นลงของการเปลี่ยนแปลงด้านล่างแถบคำสั่ง เลือกเนื้อหาที่คุณต้องการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7d54e-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="7d54e-112">บนแถบคำสั่ง ให้เลือก **แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="7d54e-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="7d54e-113">ตัวอย่างของลักษณะเนื้อหาที่จะปรากฏเมื่อการเผยแพร่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7d54e-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="7d54e-114">เมื่อต้องการแสดงตัวอย่างรูปแบบอื่น ให้เลือกจากเมนูแบบหล่นลงของการเปลี่ยนแปลง และเลือก **แสดงตัวอย่าง** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7d54e-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="7d54e-115">เผยแพร่การทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="7d54e-115">Publish your experiment</span></span>
<span data-ttu-id="7d54e-116">ถ้าคุณไม่ได้ใช้กลุ่มเผยแพร่เพื่อกำหนดตารางเวลา เมื่อการทดลองของคุณใช้งานจริง และคุณต้องการเผยแพร่ทันที ให้เลือก **เผยแพร่** ในแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="7d54e-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="7d54e-117">การเปลี่ยนแปลงทั้งหมดที่เป็นของการทดลองจะถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="7d54e-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="7d54e-118">ถ้าหน้ามี URL ที่ยังไม่ได้เผยแพร่ คุณต้องเผยแพร่ URL ก่อน หรือไม่งั้นผู้ใช้เว็บไซต์ของคุณจะไม่สามารถมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="7d54e-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="7d54e-119">สำหรับรายละเอียด ให้ดูที่ [บันทึก แสดงตัวอย่าง และเผยแพร่หน้า](save-preview-publish-page.md)</span><span class="sxs-lookup"><span data-stu-id="7d54e-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="7d54e-120">ใช้กลุ่มเผยแพร่เพื่อกำหนดเวลาที่การทดลองของคุณใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="7d54e-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="7d54e-121">การเปลี่ยนแปลงที่สร้างขึ้นในตัวสร้างไซต์สามารถจัดกำหนดการสำหรับการเผยแพร่โดยใช้กลุ่มเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="7d54e-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="7d54e-122">ภายในกลุ่มเผยแพร่ คุณสามารถเชื่อมต่อหน้าหรือส่วนกับการทดลองของคุณได้โดยการเลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="7d54e-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="7d54e-123">นอกจากนี้คุณยังสามารถดำเนินการนี้ได้โดยเลือก **หน้า** หรือ **ส่วน** และปฏิบัติตามคำแนะนำใน [เชื่อมต่อการทดลองและแก้ไขการเปลี่ยนแปลง](experimentation-connect-edit.md)</span><span class="sxs-lookup"><span data-stu-id="7d54e-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="7d54e-124">สำหรับข้อมูลเกี่ยวกับกลุ่มเผยแพร่ ให้ดูที่ [ทำงานกับกลุ่มเผยแพร่](publish-groups.md)</span><span class="sxs-lookup"><span data-stu-id="7d54e-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="7d54e-125">เมื่อใช้กลุ่มเผยแพร่ที่มีการทดลอง มีข้อควรพิจารณาที่สำคัญบางประการที่ควรระวัง</span><span class="sxs-lookup"><span data-stu-id="7d54e-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="7d54e-126">เมื่อคุณเพิ่มหน้าหรือส่วนต่างๆ ที่มีการทดลองรันบนกลุ่มเผยแพร่ การทดลองจะถูกลบออกจากหน้าหรือส่วนในกลุ่มเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="7d54e-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="7d54e-127">การทดลองที่มีการเชื่อมต่อกับหน้าในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับหน้าภายในกลุ่มเผยแพร่ และในทางกลับกันด้วย</span><span class="sxs-lookup"><span data-stu-id="7d54e-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="7d54e-128">ในทำนองเดียวกัน หน้าที่มีการทดลองทำงานอยู่ในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับการทดลองอื่นๆ ในกลุ่มเผยแพร่ และในทางกลับกันด้วย</span><span class="sxs-lookup"><span data-stu-id="7d54e-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="7d54e-129">เมื่อคุณเผยแพร่หรือจัดกำหนดการกลุ่มเผยแพร่ เนื้อหาทั้งหมดในกลุ่มเผยแพร่จะถูกเผยแพร่โดยไม่คำนึงว่ามีการทดสอบที่เกี่ยวข้องกับกลุ่มเผยแพร่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d54e-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="7d54e-130">เนื่องจากกลุ่มเผยแพร่ยังคงแสดงหลังจากที่มีการเผยแพร่ไปยังไซต์ที่ใช้งานจริง การทดลองในกลุ่มเผยแพร่จะยังคงแสดงด้วย</span><span class="sxs-lookup"><span data-stu-id="7d54e-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="7d54e-131">ดังนั้น คุณจึงไม่สามารถเชื่อมโยงการทดลองอื่นๆ กับหน้าหรือส่วนเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="7d54e-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="7d54e-132">ถ้าต้องการหลีกเลี่ยงข้อจำกัดนี้ ให้ลบกลุ่มเผยแพร่ใดๆ ที่มีการทดลองการแสดง</span><span class="sxs-lookup"><span data-stu-id="7d54e-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="7d54e-133">ในทำนองเดียวกัน ถ้าคุณต้องการลบการทดลองในไซต์ที่ใช้งานจริงที่มีอยู่ในกลุ่มเผยแพร่ ให้ลบออกจากกลุ่มเผยแพร่ก่อน</span><span class="sxs-lookup"><span data-stu-id="7d54e-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="7d54e-134">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="7d54e-134">Previous step</span></span>
[<span data-ttu-id="7d54e-135">เชื่อมต่อและแก้ไขการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="7d54e-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="7d54e-136">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="7d54e-136">Next step</span></span>
[<span data-ttu-id="7d54e-137">รันและตรวจสอบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="7d54e-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]