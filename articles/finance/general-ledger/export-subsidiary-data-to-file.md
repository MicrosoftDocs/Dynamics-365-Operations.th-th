---
title: การส่งออกข้อมูลบริษัทในเครือไปยังไฟล์อื่น
description: หัวข้อนี้อธิบายวิธีการเตรียมการส่งออกข้อมูลจาก Microsoft Dynamics 365 Finance และจากนั้นนําเข้ามายังเอนทิตี้นิติบุคคลที่รวมบัญชี
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968690"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="75cdf-103">การส่งออกข้อมูลบริษัทในเครือไปยังไฟล์อื่น</span><span class="sxs-lookup"><span data-stu-id="75cdf-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75cdf-104">คุณใช้หน้า **การส่งออก** (**การจัดการระบบ \> พื้นที่ทำงาน \> การนําเข้า/ส่งออก**) เพื่อจัดเตรียมการส่งออกข้อมูลบริษัทในเครือไปยังไฟล์ที่สามารถนําเข้าไปยังนิติบุคคลที่รวมบัญชีแล้วได้</span><span class="sxs-lookup"><span data-stu-id="75cdf-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="75cdf-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการการนำเข้าและส่งออกข้อมูล ให้ดูที่ [ภาพรวมของงานการนำเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)</span><span class="sxs-lookup"><span data-stu-id="75cdf-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="75cdf-106">สร้างนิติบุคคลสำหรับใช้ในกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="75cdf-107">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างนิติบุคคล ให้ดูที่ [สร้างนิติบุคคล](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md)</span><span class="sxs-lookup"><span data-stu-id="75cdf-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="75cdf-108">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดเตรียมนิติบุคคลที่จะใช้ในกระบวนการรวมบัญชี](prepare-company-for-consolidation.md) และ [ตั้งค่านิติบุคคลของบริษัทในเครือเพื่อการรวมบัญชี](set-up-subsidiary-company-for-consolidation.md)</span><span class="sxs-lookup"><span data-stu-id="75cdf-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="75cdf-109">ไปที่ **การรวมบัญชี \> ส่งออกยอดดุลของบริษัท**</span><span class="sxs-lookup"><span data-stu-id="75cdf-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="75cdf-110">บนหน้า **ส่งออกยอดดุลของบริษัท** บนแท็บ **เงื่อนไข** ให้ระบุรายละเอียดของการรวมบัญชีโดยการตั้งค่าฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="75cdf-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="75cdf-111">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="75cdf-111">Field</span></span>                             | <span data-ttu-id="75cdf-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="75cdf-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="75cdf-113">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="75cdf-113">Main account</span></span>                      | <span data-ttu-id="75cdf-114">ระบุบัญชีที่จะรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="75cdf-115">เมื่อต้องการรวมบัญชีทั้งหมด ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="75cdf-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="75cdf-116">ใช้บัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-116">Use consolidation account</span></span>         | <span data-ttu-id="75cdf-117">ถ้าคุณระบุบัญชีหลักในการรวมบัญชีไว้ ให้ตั้งค่าตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="75cdf-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="75cdf-118">เลือกบัญชีการรวมบัญชีจาก</span><span class="sxs-lookup"><span data-stu-id="75cdf-118">Select consolidation account from</span></span> | <span data-ttu-id="75cdf-119">เลือก **บัญชีหลัก** หรือ **บัญชีหลักในการรวมบัญชี**</span><span class="sxs-lookup"><span data-stu-id="75cdf-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="75cdf-120">กลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-120">Consolidation account group</span></span>       | <span data-ttu-id="75cdf-121">เลือกกลุ่มบัญชีหลักในการรวมบัญชีสำหรับบัญชีหลักในการรวมบัญชีที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="75cdf-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="75cdf-122">รอบระยะเวลาการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-122">Consolidation period</span></span>              | <span data-ttu-id="75cdf-123">ระบุวันที่ "จาก" และ "ถึง" สำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="75cdf-124">รวมยอดเงินจริง</span><span class="sxs-lookup"><span data-stu-id="75cdf-124">Include actual amounts</span></span>            | <span data-ttu-id="75cdf-125">ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อรวมยอดเงินจริง</span><span class="sxs-lookup"><span data-stu-id="75cdf-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="75cdf-126">รวมยอดเงินงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="75cdf-126">Include budget amounts</span></span>            | <span data-ttu-id="75cdf-127">ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อรวมยอดเงินงบประมาณในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="75cdf-128">แบบจำลองงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="75cdf-128">Budget models</span></span>                     | <span data-ttu-id="75cdf-129">ระบุรูปแบบงบประมาณที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="75cdf-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="75cdf-130">บนแท็บ **มิติทางการเงิน** ระบุรายละเอียดของการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="75cdf-131">ระบุข้อมูลมิติทางการเงินที่ควรจะโอนย้ายจากธุรกรรมในบัญชีบริษัทในเครือไปยังธุรกรรมในนิติบุคคลที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="75cdf-132">เลือกมิติทางการเงินในรายการ</span><span class="sxs-lookup"><span data-stu-id="75cdf-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="75cdf-133">ระบุข้อมูลจำเพาะระบุที่ถูกต้องสำหรับมิติทางการเงินแต่ละมิติที่มีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="75cdf-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="75cdf-134">ตัวเลือกที่พร้อมใช้งานได้แก่ **มิติ** **มิติกลุ่ม** **บัญชีบริษัท** และ **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="75cdf-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="75cdf-135">ตัวเลือก **มิติกลุ่ม** ช่วยให้คุณกําหนดค่ามิติที่ใช้โดยกลุ่มของบริษัทที่จะรวมบัญชีเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="75cdf-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="75cdf-136">ระบุใบสั่งเซ็กเมนต์ที่จะรวมบัญชีไปด้วย</span><span class="sxs-lookup"><span data-stu-id="75cdf-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="75cdf-137">บนแท็บ **นิติบุคคล** ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อระบุนิติบุคคลที่คุณส่งออก</span><span class="sxs-lookup"><span data-stu-id="75cdf-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="75cdf-138">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="75cdf-138">Select **New**.</span></span>
    2. <span data-ttu-id="75cdf-139">ในฟิลด์ **แหล่งที่มานิติบุคคล** ให้ป้อนนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="75cdf-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="75cdf-140">หากใช้เงื่อนไขเดียวกันกับบริษัทในเครือหลายบริษัทที่อยู่ในฐานข้อมูลเดียวกัน คุณสามารถโอนย้ายข้อมูลจากบริษัทในเครือเหล่านั้นไปยังไฟล์การส่งออกที่แยกต่างหากในการดำเนินการครั้งเดียวได้</span><span class="sxs-lookup"><span data-stu-id="75cdf-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="75cdf-141">สร้างบรรทัดสำหรับแต่ละนิติบุคคลบริษัทในเครือแต่ละบริษัทที่มีบัญชีซึ่งจะส่งออกไปยังไฟล์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="75cdf-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="75cdf-142">ไฟล์เหล่านี้จะถูกนำเข้าไปรวมบัญชีนิติบุคคลภายหลัง</span><span class="sxs-lookup"><span data-stu-id="75cdf-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="75cdf-143">สำหรับบริษัทในเครือแต่ละบริษัท ให้ป้อนชื่อบริษัทในเครือและชื่อไฟล์ส่งออกที่จะสร้างขึ้นระหว่างงานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="75cdf-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="75cdf-144">ในฟิล์ด **ชนิดบัญชีของความต่างของการแปลง** เลือก **กําไรขาดทุน** หรือ **งบดุล**</span><span class="sxs-lookup"><span data-stu-id="75cdf-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="75cdf-145">ป้อนชื่อไฟล์สำหรับไฟล์การนำออกที่จะสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="75cdf-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="75cdf-146">เลือก **ตกลง** เพื่อเรียกใช้การนำออก</span><span class="sxs-lookup"><span data-stu-id="75cdf-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="75cdf-147">เมื่อการส่งออกเสร็จสมบูรณ์ คุณจะได้รับข้อความที่แสดงหมายเลขของเรกคอร์ดต่างๆซึ่งถูกบันทึกไว้ในแต่ละไฟล์</span><span class="sxs-lookup"><span data-stu-id="75cdf-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="75cdf-148">จากนั้นคุณจะสามารถนำเข้าไฟล์ต่างๆไปยังนิติบุคคลที่ได้รวมบัญชีไว้</span><span class="sxs-lookup"><span data-stu-id="75cdf-148">You can then import the files into the consolidated legal entity.</span></span>
