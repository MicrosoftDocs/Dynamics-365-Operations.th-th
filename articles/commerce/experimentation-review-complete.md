---
title: ส่งเสริมการเปลี่ยนแปลงและทำการทดลองให้เสร็จสมบูรณ์
description: หัวข้อนี้อธิบายวิธีการส่งเสริมการเปลี่ยนแปลงที่ประสบความสำเร็จ และทำการทดลองให้เสร็จสมบูรณ์ใน Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930296"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="971be-103">ส่งเสริมการเปลี่ยนแปลงและทำการทดลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="971be-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="971be-104">หัวข้อนี้อธิบายวิธีกาส่งเสริมการเปลี่ยนแปลงที่ให้ผลลัพธ์ที่ดีที่สุดในการทดลองของคุณ และทำการทดลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="971be-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="971be-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="971be-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="971be-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="971be-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="971be-107">[ ![การเดินทางของผู้ใช้การทดลอง - ทบทวน & เสร็จสมบูรณ์](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="971be-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="971be-108">หลังจากที่คุณ [รันการทดลองแล้ว](experimentation-run-monitor.md) และรวบรวมข้อมูลเพียงพอเพื่อตรวจสอบว่าคุณต้องการใช้การปรับเปลี่ยนแบบใดบนไซต์ของคุณ คุณจะส่งเสริมการเปลี่ยนแปลงนั้น และจบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="971be-109">ส่งเสริมการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="971be-109">Promote a variation</span></span>
<span data-ttu-id="971be-110">ใช้ข้อมูลและการวิเคราะห์ที่เกี่ยวข้องกับการทดลองในบริการของบุคคลที่สาม เพื่อตัดสินใจว่าการเปลี่ยนแปลงใดที่ให้ผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="971be-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="971be-111">เมื่อต้องการแทนที่เนื้อหาปัจจุบันบนไซต์ที่ถ่ายทอดสดที่มีการเปลี่ยนแปลงที่ดีที่สุด เพื่อให้สามารถใช้งานได้กับผู้ใช้ทั้งหมดของเว็บไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="971be-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="971be-112">ไปที่แท็บ **การทดลอง** ในโปรแกรมสร้างไซต์ แล้วเลือกการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="971be-113">เลือก **ทำการทดลองให้เสร็จสมบูรณ์** บนแถบด้านบน</span><span class="sxs-lookup"><span data-stu-id="971be-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="971be-114">ในเมนูกล่องโต้ตอบ **ทำการทดลองให้เสร็จสมบูรณ์** ให้เลือก **ตรวจสอบข้อมูลการทดลอง**</span><span class="sxs-lookup"><span data-stu-id="971be-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="971be-115">บริการของบุคคลที่สามเปิดให้คุณสามารถตรวจสอบความถูกต้องของการวัด และกำหนดว่าการเปลี่ยนแปลงใดที่ดำเนินการดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="971be-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="971be-116">ในเมนูกล่องโต้ตอบ **ทำการทดลองให้เสร็จสมบูรณ์** ในโปรแกรมสร้างไซต์ ให้เลือกการเปลี่ยนแปลงที่ดีที่สุด แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="971be-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="971be-117">เปิดบริการของบุคคลที่สาม และหยุดการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="971be-118">ในโปรแกรมสร้างไซต์ ให้เลือก **เสร็จสมบูรณ์** เพื่อเขียนทับหน้าที่ใช้งานจริงเดิม และเผยแพร่การเปลี่ยนแปลงที่ดีที่สุดเพื่อให้สามารถใช้งานได้กับผู้ใช้ทั้งหมดในเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="971be-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="971be-119">ถ้าคุณเลือกที่จะเก็บหน้าปัจจุบันไว้ และไม่เผยแพร่การเปลี่ยนแปลง ให้เลือก **เผยแพร่หน้าเดิมอีกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="971be-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="971be-120">ลบการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="971be-120">Delete your experiment</span></span>
<span data-ttu-id="971be-121">แม้ว่าคุณจะไม่จำเป็นต้องลบการทดลองที่เสร็จสมบูรณ์ใน Commerce คุณอาจเลือกที่จะลบเพื่อประหยัดพื้นที่หรือล้างพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="971be-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="971be-122">เมื่อต้องการลบการทดลอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="971be-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="971be-123">ไปที่แท็บ **การทดลอง** ในโปรแกรมสร้างไซต์ แล้วเลือกการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="971be-124">ถ้าการทดลองยังคงใช้งานอยู่ โปรดหยุดการทดลองในบริการของบุคคลที่สามก่อนดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="971be-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="971be-125">เลือก **ยกเลิกการเผยแพร่** ในแถบคำสั่ง เพื่อลบเนื้อหาของการเปลี่ยนแปลงออกจากเว็บไซต์ที่ใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="971be-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="971be-126">เลือก **ลบ** ในแถบคำสั่ง เพื่อลบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="971be-127">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="971be-127">Previous step</span></span>
[<span data-ttu-id="971be-128">รันและตรวจสอบการทดลอง</span><span class="sxs-lookup"><span data-stu-id="971be-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
