---
title: เชื่อมต่อการทดลองและแก้ไขรูปแบบการทดลอง
description: หัวข้อนี้อธิบายวิธีการเชื่อมต่อการทดลองในบริการของบุคคลที่สามกับ Dynamics 365 Commerce และวิธีการแก้ไขรูปแบบการทดลอง
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4c9c9463162f21cdaf40f1c4ed6d5ae51e97cb88
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799097"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="c7cd2-103">เชื่อมต่อการทดลองและแก้ไขรูปแบบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="c7cd2-104">หัวข้อนี้อธิบายวิธีการเชื่อมต่อการทดลองของคุณใน Commerce และทำการเปลี่ยนแปลงรูปแบบของคุณ เพื่อให้สอดคล้องกับสมมติฐานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="c7cd2-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c7cd2-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c7cd2-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c7cd2-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="c7cd2-107">[ ![การเดินทางของผู้การทดสอบใช้ - เชื่อมต่อและแก้ไข](./media/experimentation_connect_edit.svg)](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c7cd2-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="c7cd2-108">หลังจากที่คุณ [ตั้งค่าการทดลองของคุณ](experimentation-setup.md) ในบริการของบุคคลที่สามแล้ว คุณจะเชื่อมต่อการทดลองใน Dynamics 365 Commerce และแก้ไขรูปแบบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="c7cd2-109">ข้อควรพิจารณาสำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c7cd2-109">Planning considerations</span></span>

<span data-ttu-id="c7cd2-110">ก่อนที่คุณจะเชื่อมต่อการทดลองของคุณใน Commerce คุณจะต้องทำการตัดสินใจบางอย่างที่ส่งผลกระทบต่อวิธีการที่ Commerce จัดการเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="c7cd2-111">กำหนดขอบเขตของการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="c7cd2-112">เมื่อคุณเชื่อมต่อการทดลอง คุณจะได้รับแจ้งให้กำหนดขอบเขตของการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="c7cd2-113">การทดลองมีการกำหนดเป็นขอบเขต **บางส่วน** หรือ **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="c7cd2-114">เลือก **บางส่วน** ถ้าคุณต้องการดำเนินการทดลองบนส่วนเฉพาะของหน้า</span><span class="sxs-lookup"><span data-stu-id="c7cd2-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="c7cd2-115">ถ้าคุณเลือกตัวเลือกนี้ คุณต้องระบุว่าโมดูลใดจะรวมอยู่ในการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="c7cd2-116">การเปลี่ยนแปลงที่เกิดขึ้นกับส่วนของหน้าหรือส่วนเริ่มต้นที่ไม่เกี่ยวข้องกับการทดลองจะถูกซิงโครไนส์ระหว่างรูปแบบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="c7cd2-117">เลือก **ทั้งหมด** ถ้าคุณต้องการดำเนินการทดลองบนหน้าหรือส่วนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7cd2-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="c7cd2-118">มีการสร้างสำเนาของหน้าหรือส่วนเริ่มต้นที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c7cd2-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="c7cd2-119">คุณไม่จำเป็นต้องเลือกโมดูลที่จะรวมอยู่ในการทดลอง เนื่องจากพื้นที่การแก้ไขทั้งหมดสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="c7cd2-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="c7cd2-120">คุณสามารถเพิ่ม ลบ หรือโมดูลการสั่งใหม่ได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="c7cd2-121">อย่างไรก็ตาม ถ้ามีการเปลี่ยนแปลงใดๆ เกิดขึ้นกับหน้าหรือส่วนเริ่มต้นที่การทดลองเชื่อมโยง การเปลี่ยนแปลงเหล่านั้นต้องมีการซิงโครไนส์ด้วยตนเองระหว่างรูปแบบทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7cd2-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="c7cd2-122">ถ้าคุณเชื่อมโยงการทดลองของคุณกับหน้าซึ่งใช้โครงร่าง คุณจะสามารถกำหนดขอบเขตการทดลองเป็น **ทั้งหมด** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c7cd2-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="c7cd2-123">ตัดสินใจว่าคุณต้องการกำหนดตารางเวลาให้มีการเผยแพร่การทดลองของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c7cd2-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="c7cd2-124">ถ้าคุณต้องการกำหนดตารางเวลาเมื่อมีการเผยแพร่การทดลองของคุณไปยังไซต์ที่ใช้งานจริง ให้ตรวจสอบให้แน่ใจว่าเนื้อหาที่คุณต้องการเชื่อมโยงกับการทดลองมีอยู่ในกลุ่มเผยแพร่ *ก่อน* ที่คุณจะเชื่อมต่อการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="c7cd2-125">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มเผยแพร่ ให้อ้างอิงถึง [ทำงานกับกลุ่มเผยแพร่](publish-groups.md)</span><span class="sxs-lookup"><span data-stu-id="c7cd2-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="c7cd2-126">เชื่อมต่อการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-126">Connect your experiment</span></span>
<span data-ttu-id="c7cd2-127">เมื่อต้องการเชื่อมต่อการทดลองของคุณ คุณจะเปิดใช้งานตัวช่วยสร้าง **การทดสอบการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="c7cd2-128">ตัวช่วยสร้างจะแนะนำให้คุณทราบถึงขั้นตอนต่างๆ ที่จำเป็นในการเชื่อมต่อการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="c7cd2-129">เมื่อคุณดำเนินการตัวช่วยสร้าง การทดลองของคุณจะได้รับการเชื่อมต่อและมีการสร้างรูปแบบ และพร้อมที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c7cd2-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="c7cd2-130">เมื่อต้องการเริ่มต้นใช้งานเชื่อมต่อการทดลองของคุณบนไซต์ของคุณในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c7cd2-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7cd2-131">เมื่อต้องการเปิดใช้งานตัวช่วยสร้าง **การทดลองการเชื่อมต่อ** ให้เลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="c7cd2-132">อีกทางหนึ่งคือ คุณสามารถเข้าถึงตัวช่วยสร้างจากหน้าหรือตัวแก้ไขส่วน โดยการแก้ไขและเลือก **การทดสอบการเชื่อมต่อ** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7cd2-133">หน้าสามารถเชื่อมต่อกับหนึ่งการทดลองเท่านั้นในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="c7cd2-134">เมื่อต้องการเชื่อมต่อหน้ากับการทดลองอื่น ให้ลบการทดลองที่มีการเชื่อมต่อกับหน้าในขณะนี้ก่อน</span><span class="sxs-lookup"><span data-stu-id="c7cd2-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="c7cd2-135">เลือกหน้าหรือส่วนที่คุณต้องการรันการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="c7cd2-136">กำหนดขอบเขตการทดลองเป็น **บางส่วน** หรือ **ทั้งหมด** ตามตัวเลือกที่คุณทำไว้ในส่วน [การกำหนดขอบเขตของการทดลองของคุณ](#determine-the-scope-of-your-experiment) ข้างบน</span><span class="sxs-lookup"><span data-stu-id="c7cd2-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="c7cd2-137">แฟล็กลักษณะการทำงาน **การทดลองบนหน้าหรือส่วน** ต้องเปิดใช้งาน ถ้าคุณต้องการทดลองใช้งานบนหน้าหรือส่วนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7cd2-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="c7cd2-138">ให้อ้างอิงถึงหัวข้อ [การทดสอบใน Dynamics 365 Commerce](experimentation-overview.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c7cd2-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="c7cd2-139">ในขั้นตอนสุดท้ายของตัวช่วยสร้าง ให้เลือก **สร้างรูปแบบและออกจากตัวช่วยสร้าง**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="c7cd2-140">การเปลี่ยนแปลงสร้างสำหรับการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="c7cd2-141">แก้ไขการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-141">Edit your variations</span></span>
<span data-ttu-id="c7cd2-142">เมื่อคุณออกจากตัวช่วยสร้าง จะมีการสร้างการเปลี่ยนแปลงให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="c7cd2-143">ถัดไป คุณจะแก้ไขการเปลี่ยนแปลงเพื่อให้สะท้อนถึงตัวเลือกที่คุณต้องการตรวจสอบในสมมติฐานการทดลอง</span><span class="sxs-lookup"><span data-stu-id="c7cd2-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="c7cd2-144">เลือกขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้ที่สอดคล้องกับขอบเขตที่คุณเลือกสำหรับการทดลองของคุณในส่วน [การกำหนดขอบเขตของการทดลองของคุณ](#determine-the-scope-of-your-experiment) ข้างบน</span><span class="sxs-lookup"><span data-stu-id="c7cd2-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="c7cd2-145">แก้ไขการเปลี่ยนแปลงสำหรับการทดลองโดยมีขอบเขตบางส่วน</span><span class="sxs-lookup"><span data-stu-id="c7cd2-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="c7cd2-146">ทำตามขั้นตอนต่อไปนี้ถ้าคุณกำหนดขอบเขตของการทดลองของคุณเป็น **บางส่วน** ในตัวช่วยสร้าง **เชื่อมต่อการทดลอง**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="c7cd2-147">ในมุมมองตัวแก้ไข ให้ใช้เมนูแบบหล่นลงของการเปลี่ยนแปลงใต้แถบคำสั่งเพื่อแก้ไขคการเปลี่ยนแปลงแต่ละแบบตามสมมติฐานดั้งเดิมของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="c7cd2-148">นอกจากนี้คุณอาจต้องการสร้างรูปแบบการควบคุมหรือพื้นฐานโดยไม่ทำการเปลี่ยนแปลงหนึ่งรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="c7cd2-149">เลือกโมดูลที่จะทดลอง ให้เลือกจุดไข่ปลา (...) แล้วเลือก **เพิ่มในการทดลอง**</span><span class="sxs-lookup"><span data-stu-id="c7cd2-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="c7cd2-150">แก้ไขการเปลี่ยนแปลงสำหรับการทดลองโดยมีขอบเขตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7cd2-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="c7cd2-151">ถ้าคุณกำหนดขอบเขตการทดลองของคุณเป็น **ทั้งหมด** ในตัวช่วยสร้าง **เชื่อมต่อการทดลอง** ขณะที่อยู่ในมุมมองตัวแก้ไข ให้ใช้เมนูแบบหล่นลงของรูปแบบที่อยู่ใต้แถบคำสั่ง เพื่อแก้ไขรูปแบบแต่ละแบบตามสมมติฐานดั้งเดิมของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="c7cd2-152">ในทั้งสองกรณี คุณอาจต้องการสร้างรูปแบบการควบคุมหรือพื้นฐานโดยไม่ทำการเปลี่ยนแปลงหนึ่งรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c7cd2-153">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="c7cd2-153">Previous step</span></span>
[<span data-ttu-id="c7cd2-154">การตั้งค่าการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="c7cd2-155">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="c7cd2-155">Next step</span></span>
[<span data-ttu-id="c7cd2-156">แสดงตัวอย่างและเผยแพร่การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c7cd2-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]