---
title: ส่งเสริมการเปลี่ยนแปลงและทำการทดลองให้เสร็จสมบูรณ์
description: หัวข้อนี้อธิบายวิธีการส่งเสริมการเปลี่ยนแปลงที่ประสบความสำเร็จ และทำการทดลองให้เสร็จสมบูรณ์ใน Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/22/2020
ms.locfileid: "4416272"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="96f99-103">ส่งเสริมการเปลี่ยนแปลงและทำการทดลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="96f99-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="96f99-104">หัวข้อนี้อธิบายวิธีกาส่งเสริมการเปลี่ยนแปลงที่ให้ผลลัพธ์ที่ดีที่สุดในการทดลองของคุณ และทำการทดลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="96f99-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="96f99-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="96f99-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="96f99-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="96f99-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="96f99-107">[ ![การเดินทางของผู้ใช้การทดลอง - ทบทวน & เสร็จสมบูรณ์](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="96f99-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="96f99-108">หลังจากที่คุณ [รันการทดลองแล้ว](experimentation-run-monitor.md) และรวบรวมข้อมูลเพียงพอเพื่อตรวจสอบว่าคุณต้องการใช้การปรับเปลี่ยนแบบใดบนไซต์ของคุณ คุณจะส่งเสริมการเปลี่ยนแปลงนั้น และจบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="96f99-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="96f99-109">ส่งเสริมการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="96f99-109">Promote a variation</span></span>
<span data-ttu-id="96f99-110">ใช้ข้อมูลและการวิเคราะห์ที่เกี่ยวข้องกับการทดลองในบริการของบุคคลที่สาม เพื่อตัดสินใจว่าการเปลี่ยนแปลงใดที่ให้ผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="96f99-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="96f99-111">คุณสามารถส่งเสริมโดยการแทนที่เนื้อหาปัจจุบันบนไซต์ที่ถ่ายทอดสดที่มีการเปลี่ยนแปลงที่ดีที่สุด เพื่อให้สามารถใช้งานได้กับผู้ใช้ทั้งหมดของเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="96f99-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="96f99-112">เมื่อต้องการส่งเสริมการเปลี่ยนแปลงที่ดีที่สุด ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96f99-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="96f99-113">ในโปรแกรมสร้างไซต์ Commerce เลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือกการทดลอง</span><span class="sxs-lookup"><span data-stu-id="96f99-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="96f99-114">บนแถบคำสั่ง เลือก **ทำการทดลองให้เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="96f99-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="96f99-115">ในกล่องโต้ตอบ **ทำการทดลองให้เสร็จสมบูรณ์** ให้เลือก **ตรวจสอบข้อมูลการทดลอง**</span><span class="sxs-lookup"><span data-stu-id="96f99-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="96f99-116">บริการของบุคคลที่สามเปิดให้คุณสามารถตรวจสอบความถูกต้องของการวัด และกำหนดว่าการเปลี่ยนแปลงใดที่ดำเนินการดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="96f99-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="96f99-117">ในเมนูกล่องโต้ตอบ **ทำการทดลองให้เสร็จสมบูรณ์** ให้เลือกการเปลี่ยนแปลงที่ดีที่สุด แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="96f99-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="96f99-118">เปิดบริการของบุคคลที่สาม และหยุดการทดลอง</span><span class="sxs-lookup"><span data-stu-id="96f99-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="96f99-119">ในโปรแกรมสร้างไซต์ ให้เลือก **เสร็จสมบูรณ์** เพื่อเขียนทับหน้าที่ใช้งานจริงเดิม และเผยแพร่การเปลี่ยนแปลงที่ดีที่สุดเพื่อให้สามารถใช้งานได้กับผู้ใช้ทั้งหมดในเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="96f99-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="96f99-120">ถ้าคุณเลือกที่จะเก็บหน้าปัจจุบันไว้ และไม่เผยแพร่การเปลี่ยนแปลง ให้เลือก **เผยแพร่หน้าเดิมอีกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="96f99-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="96f99-121">ลบการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="96f99-121">Delete your experiment</span></span>
<span data-ttu-id="96f99-122">แม้ว่าคุณจะไม่จำเป็นต้องลบการทดลองที่เสร็จสมบูรณ์ใน Commerce คุณอาจเลือกที่จะลบเพื่อประหยัดพื้นที่หรือล้างพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="96f99-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="96f99-123">หากต้องการลบการทดลองในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="96f99-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="96f99-124">เลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือกการทดลอง</span><span class="sxs-lookup"><span data-stu-id="96f99-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="96f99-125">ถ้าการทดลองยังคงใช้งานอยู่ โปรดหยุดการทดลองในบริการของบุคคลที่สามก่อนดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="96f99-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="96f99-126">ในแถบคำสั่ง เลือก **ยกเลิกการเผยแพร่**  เพื่อลบเนื้อหาของการเปลี่ยนแปลงออกจากเว็บไซต์ที่ใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="96f99-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="96f99-127">เลือก **ลบ** เพื่อลบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="96f99-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="96f99-128">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="96f99-128">Previous step</span></span>
[<span data-ttu-id="96f99-129">รันและตรวจสอบการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="96f99-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
