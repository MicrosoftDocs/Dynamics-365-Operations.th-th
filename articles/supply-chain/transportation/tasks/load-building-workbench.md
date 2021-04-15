---
title: เวิร์กเบนช์การสร้างการบรรทุก
description: หัวข้อนี้อธิบายวิธีการทำงานกับเวิร์กเบนช์การสร้างอาคารโหลด
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809049"
---
# <a name="load-building-workbench"></a><span data-ttu-id="792dc-103">เวิร์กเบนช์การสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="792dc-103">Load building workbench</span></span>

<span data-ttu-id="792dc-104">เวิร์กเบนช์สร้างงานบรรทุกช่วยให้คุณสามารถใช้กลยุทธ์การสร้างจำนวนงานในศูนย์การผลิตได้เมื่อคุณสร้างการโหลด</span><span class="sxs-lookup"><span data-stu-id="792dc-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="792dc-105">สร้างกลยุทธ์การสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="792dc-105">Create a load building strategy</span></span>

<span data-ttu-id="792dc-106">คุณสามารถใช้กลยุทธ์การสร้างจำนวนงานในศูนย์การผลิตเพื่อสร้างโหลดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="792dc-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="792dc-107">ความสามารถนี้อาจเป็นประโยชน์ในกรณีต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="792dc-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="792dc-108">ถ้าคุณจัดส่งสินค้าชุดเฉพาะของผลิตภัณฑ์อย่างสม่ำเสมอ กลยุทธ์จำนวนงานในศูนย์การผลิตจะช่วยประหยัดเวลาได้ เนื่องจากคุณไม่จำเป็นต้องสร้างโหลดเดียวกันทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="792dc-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="792dc-109">ถ้าคุณต้องการหลีกเลี่ยงการโหลดแบบเต็มครึ่งเพื่อให้ประสิทธิภาพการทำงานสูงสุด กลยุทธ์จำนวนงานในศูนย์การผลิตสามารถช่วยเติมแต่ละโหลดให้มากที่สุดเท่าที่จะเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="792dc-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="792dc-110">คลาสของกลยุทธ์การสร้างการบรรทุกที่มีการตั้งชื่อ `TMSLoadBuildingVolumeStrategy` ให้กลยุทธ์การสร้างการบรรทุกที่มีชื่อว่า  *กลยุทธ์การสร้างการบรรทุกตามปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="792dc-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="792dc-111">กลยุทธ์นี้ช่วยให้คุณสามารถใช้ค่าสูงสุดที่ระบุสำหรับความสูงและน้ำหนักในเท็มเพลตของโหลด หรือคุณสามารถแทนที่การตั้งค่าโดยการป้อนค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="792dc-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="792dc-112">กลยุทธ์นี้เป็นกลยุทธ์เดียวที่รวมอยู่ในสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="792dc-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="792dc-113">(อย่างไรก็ตาม คุณอาจมีกลยุทธ์ที่กำหนดเองบางอย่าง)</span><span class="sxs-lookup"><span data-stu-id="792dc-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="792dc-114">เมื่อต้องการใช้กลยุทธ์ *กลยุทธ์การสร้างการบรรทุกตามปริมาณ* สำเร็จรูป ให้เลือกฟิลด์ **กลยุทธ์การสร้างการบรรทุก** บนหน้า **เวิร์กเบนช์การสร้างงานบรรทุก** (**การจัดการการขนส่ง &gt; การวางแผน &gt; เวิร์กเบนช์การสร้างงานบรรทุก**)</span><span class="sxs-lookup"><span data-stu-id="792dc-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="792dc-115">เมื่อต้องการสร้างกลยุทธ์การสร้างการบรรทุก ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="792dc-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="792dc-116">ไปที่ **การจัดการการขนส่ง &gt; การตั้งค่า &gt; การสร้างการบรรทุก &gt; กลยุทธ์การสร้างการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="792dc-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="792dc-117">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้างรายการคลาส** เพื่อตรวจสอบให้แน่ใจว่าคุณมีคลาสที่พร้อมใช้งานทั้งหมดของรุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="792dc-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="792dc-118">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="792dc-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="792dc-119">ป้อนชื่อที่ไม่ซ้ำกันสำหรับกลยุทธ์ ให้เลือกคลาสกลยุทธ์การสร้างการบรรทุกสำหรับฟิลด์นี้ และป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="792dc-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="792dc-120">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="792dc-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="792dc-121">บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="792dc-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="792dc-122">บนหน้า **พารามิเตอร์กลยุทธ์การสร้างการบรรทุก** ให้เลือก **กำลังการผลิตตามปริมาณ** ในรายการ จากนั้นในฟิลด์ **ค่า** ให้ป้อนเปอร์เซ็นต์ของกำลังการผลิตปริมาณรวมของจำนวนงานในศูนย์การผลิตที่ควรจะใช้สำหรับกลยุทธ์การสร้างการบรรทุกใหม่</span><span class="sxs-lookup"><span data-stu-id="792dc-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="792dc-123">ให้เลือก **กำลังการผลิตตามน้ำหนัก** ในรายการ จากนั้นในฟิลด์ **ค่า** ให้ป้อนเปอร์เซ็นต์ของกำลังการผลิตน้ำหนักรวมของจำนวนงานในศูนย์การผลิตที่ควรจะใช้สำหรับกลยุทธ์การสร้างการบรรทุกใหม่</span><span class="sxs-lookup"><span data-stu-id="792dc-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="792dc-124">ปิดหน้า **พารามิเตอร์กลยุทธ์การสร้างการบรรทุกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="792dc-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="792dc-125">ปิดหน้า **กลยุทธ์การสร้างการบรรทุกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="792dc-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="792dc-126">ขณะนี้คุณสามารถกำหนดกลยุทธ์การสร้างการบรรทุกให้กับแม่แบบการสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="792dc-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="792dc-127">อีกทางหนึ่งคือ คุณสามารถใช้ได้โดยตรงในเวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="792dc-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="792dc-128">ใช้กลยุทธ์การสร้างการบรรทุกในเวิร์กเบนช์การสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="792dc-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="792dc-129">ไปที่ **การจัดการการขนส่ง &gt; การวางแผน &gt; เวิร์กเบนช์การสร้างการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="792dc-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="792dc-130">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="792dc-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="792dc-131">เลือกกลยุทธ์ในฟิลด์ **กลยุทธ์การสร้างการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="792dc-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="792dc-132">ถ้าคุณได้กำหนดแม่แบบการสร้างการบรรทุกและกำหนดกลยุทธ์การสร้างการบรรทุกไว้ บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการแม่แบบ** ให้เลือก **ใช้แม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="792dc-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="792dc-133">จากนั้น ในกล่องโต้ตอบแบบหล่นลง **ใช้แม่แบบการสร้างการบรรทุก** เลือกแม่แบบในฟิลด์ **ชื่อแม่แบบการสร้างการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="792dc-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="792dc-134">บนแท็บด่วน **ลำดับแม่แบบการบรรทุก** ให้เลือกหนึ่ง [แม่แบบการบรรทุก](load-template.md) ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="792dc-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="792dc-135">เวิร์กเบนช์จะพยายามให้การบรรทุกพอดีกับชนิดคอนเทนเนอร์เหล่านี้ ในลำดับที่ระบุไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="792dc-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="792dc-136">โดยทั่วไป คุณควรวางคอนเทนเนอร์ที่เล็กที่สุดที่ด้านบนของรายการ เพื่อให้แน่ใจว่ามีการเลือกคอนเทนเนอร์ที่มีขนาดเล็กที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="792dc-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="792dc-137">ในบานหน้าต่างการดำเนินการ เลือก **เสนอการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="792dc-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="792dc-138">ตรวจทานการบรรทุกที่นำเสนอและรายการการบรรทุกที่นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="792dc-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="792dc-139">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้างการบรรทุก** เพื่อสร้างการบรรทุกที่ยึดตามบรรทัดเอกสารต้นทางในแท็บด่วน **รายการการบรรทุกที่นำเสนอ**</span><span class="sxs-lookup"><span data-stu-id="792dc-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="792dc-140">ปิดหน้า **เวิร์กเบนช์การสร้างการบรรทุกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="792dc-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]