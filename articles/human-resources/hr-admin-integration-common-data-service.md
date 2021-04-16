---
title: ตั้งค่าคอนฟิกการรวม Dataverse
description: คุณสามารถเปิดหรือปิดการรวม Microsoft Dataverse กับ Dynamics 365 Human Resources นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ลบข้อมูลการติดตาม และรีซิงค์ตารางเพื่อช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมของทั้งสองได้
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 080f66e4e13df44a77f0499c6d69686f0e3d7021
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801202"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="3f185-104">ตั้งค่าคอนฟิกการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f185-105">คุณสามารถเปิดหรือปิดการรวม Microsoft Dataverse กับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3f185-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="3f185-106">นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ลบข้อมูลการติดตาม และรีซิงค์ตารางเพื่อช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมของทั้งสองได้</span><span class="sxs-lookup"><span data-stu-id="3f185-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="3f185-107">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="3f185-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="3f185-108">เมื่อคุณปิดการรวม ผู้ใช้สามารถทำการเปลี่ยนแปลงในทรัพยากรบุคคลหรือ Dataverse แต่การเปลี่ยนแปลงดังกล่าวจะไม่มีการซิงค์ระหว่างสภาพแวดล้อมทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="3f185-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="3f185-109">ตามค่าเริ่มต้น การรวมข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse จะถูกปิดไว้</span><span class="sxs-lookup"><span data-stu-id="3f185-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="3f185-110">คุณอาจต้องการปิดการรวมในสถานการณ์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3f185-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="3f185-111">คุณกำลังกรอกข้อมูลโดยใช้กรอบงานการจัดการข้อมูลและต้องนำเข้าข้อมูลหลายครั้งเพื่อให้ได้รับเป็นสถานะที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3f185-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="3f185-112">แต่ก็ยังมีปัญหากับข้อมูลในทรัพยากรบุคคลหรือ Dataverse อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3f185-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="3f185-113">ถ้าคุณปิดการรวมคุณสามารถลบเรกคอร์ดในสภาพแวดล้อมหนึ่งได้โดยไม่ต้องลบเรกคอร์ดนั้นออกจากเรกคอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="3f185-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="3f185-114">เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดในสภาพแวดล้อมที่ไม่มีการลบออกจะซิงค์กลับไปยังสภาพแวดล้อมที่มีการลบออก</span><span class="sxs-lookup"><span data-stu-id="3f185-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="3f185-115">การซิงโครไนส์เริ่มต้นในครั้งถัดไปที่มีการรวม **Dataverse ที่พลาดการซิงค์** การร้องขอรันชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3f185-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="3f185-116">เมื่อคุณปิดการรวมข้อมูลโปรดตรวจสอบให้แน่ใจว่าคุณไม่ได้แก้ไขเรกคอร์ดที่เหมือนกันในสภาพแวดล้อมทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="3f185-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="3f185-117">เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดที่คุณแก้ไขครั้งสุดท้ายจะถูกซิงค์</span><span class="sxs-lookup"><span data-stu-id="3f185-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="3f185-118">ดังนั้น ถ้าคุณไม่ได้ทำการเปลี่ยนแปลงที่เหมือนกันบนเรกคอร์ดในสภาพแวดล้อมทั้งสอง การสูญเสียข้อมูลอาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3f185-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="3f185-119">เข้าถึงหน้าการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="3f185-120">ในอินสแตนซ์ทรัพยากรบุคคลซึ่งคุณต้องการดูหรือตั้งค่าคอนฟิกการตั้งค่าสำหรับการรวมกับ Dataverse เลือกไทล์ **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="3f185-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="3f185-121">[![ไทล์การจัดการระบบ](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="3f185-122">เลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="3f185-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="3f185-123">[![แท็บลิงค์](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="3f185-124">ภายใต้ **การรวม** เลือก **การตั้งค่าคอนฟิก Dataverse**</span><span class="sxs-lookup"><span data-stu-id="3f185-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="3f185-125">[![Dataverse ลิงค์การตั้งค่าคอนฟิก](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="3f185-126">เปิดหรือปิดการรวมข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="3f185-127">เมื่อต้องการเปิดการรวมให้ตั้งค่าตัวเลือก **การเปิดใช้การรวม Dataverse** เป็น **ใช่** บนหน้า **การรวม Microsoft Dataverse**</span><span class="sxs-lookup"><span data-stu-id="3f185-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f185-128">เมื่อคุณเปิดการรวม ข้อมูลจะถูกซิงค์ในครั้งถัดไปที่การรวม **Dataverse พลาดการซิงค์** รันชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3f185-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="3f185-129">ข้อมูลทั้งหมดควรพร้อมใช้งานหลังจากชุดงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3f185-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="3f185-130">เมื่อต้องการปิดใช้งานการรวมให้ตั้งตัวเลือกเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="3f185-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="3f185-131">[![การเปิดหรือปิด Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="3f185-132">เราขอแนะนำให้ปิดการรวม Dataverse ในขณะที่ทำงานการย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f185-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="3f185-133">การอัพโหลดข้อมูลขนาดใหญ่อาจส่งผลกระทบต่อประสิทธิภาพการทำงานได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="3f185-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="3f185-134">ตัวอย่างเช่นการอัพโหลดผู้ปฏิบัติงาน 2000 คน สามารถใช้เวลาหลายชั่วโมงเมื่อมีการเปิดใช้งานการรวม และน้อยกว่าหนึ่งชั่วโมงเมื่อปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3f185-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="3f185-135">ตัวเลขที่ระบุในตัวอย่างนี้ใช้เพื่อวัตถุประสงค์ในการสาธิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3f185-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="3f185-136">จำนวนเวลาที่ใช้ในการนำเข้าเรกคอร์ดมีความแตกต่างกันอย่างมากตามปัจจัยหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="3f185-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="3f185-137">ภาพรวมของรายละเอียดการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f185-137">View data integration details</span></span>

<span data-ttu-id="3f185-138">บนแท็บด่วน **การจัดการ** ของหน้า **การรวม Microsoft Dataverse** คุณสามารถดูวิธีการเชื่อมโยงแถวร่วมกันระหว่างทรัพยากรบุคคลและ Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="3f185-139">เมื่อต้องการดูแถวของตาราง ให้เลือกฟิลด์ **ตาราง Dataverse**</span><span class="sxs-lookup"><span data-stu-id="3f185-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="3f185-140">กริดแสดงแถวทั้งหมดที่เชื่อมโยงกับตารางที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3f185-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="3f185-141">ไม่ใช่ตาราง Dataverse ทั้งหมดที่แสดงอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3f185-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="3f185-142">เฉพาะตารางที่สนับสนุนการใช้ฟิลด์ที่กำหนดเองเท่านั้นที่จะปรากฏในกริด</span><span class="sxs-lookup"><span data-stu-id="3f185-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="3f185-143">ตารางใหม่จะพร้อมใช้งานโดยผ่านการเผยแพร่ของทรัพยากรบุคคลอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="3f185-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="3f185-144">กริดประกอบด้วยฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f185-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="3f185-145">**ตาราง Dataverse** – ชื่อตารางใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="3f185-146">**การอ้างอิงตาราง Dataverse** – ตัวระบุที่ Dataverse ใช้ในการระบุเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="3f185-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="3f185-147">ค่านี้เทียบเท่ากับค่า **RecId** ของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3f185-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="3f185-148">คุณสามารถค้นหาตัวระบุเมื่อคุณเปิดตาราง Dataverse ใน Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="3f185-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="3f185-149">**ชื่อเอนทิตีทรัพยากรบุคคล** – เอนทิตี Human Resources ที่มีการซิงค์ข้อมูลครั้งล่าสุดกับ Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="3f185-150">เอนทิตี้สามารถมีคำนำหน้า Dataverse หรือคำนำหน้าอื่น</span><span class="sxs-lookup"><span data-stu-id="3f185-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="3f185-151">**การอ้างอิงทรัพยากรบุคคล** – ค่า **RecId** ที่เชื่อมโยงกับเรกคอร์ดในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3f185-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="3f185-152">**ลบออกจาก Dataverse แล้ว** – ค่าที่บ่งชี้ว่าแถวถูกลบออกจาก Dataverse หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3f185-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="3f185-153">เรกคอร์ดในทรัพยากรบุคคลจะตรงกับแถวใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="3f185-154">ลบการเชื่อมโยงของเรกคอร์ดในทรัพยากรบุคคลออกจากแถว Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="3f185-155">ถ้าคุณประสบปัญหาในระหว่างการซิงโครไนส์ข้อมูลระหว่างทรัพยากรบุคคลและ Dataverse คุณอาจสามารถแก้ไขปัญหาเหล่านั้นได้ด้วยการล้างการติดตามและปล่อยให้ตารางการติดตามถูกรีซิงค์</span><span class="sxs-lookup"><span data-stu-id="3f185-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="3f185-156">ถ้าคุณลบการเชื่อมโยงออกแล้วเปลี่ยนหรือลบแถวใน Dataverse การเปลี่ยนแปลงจะไม่ถูกซิงค์กับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3f185-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="3f185-157">ถ้าคุณทำการเปลี่ยนแปลงในทรัพยากรบุคคลเรกคอร์ดการติดตามใหม่จะถูกสร้างขึ้นและแถวจะถูกอัพเดตใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="3f185-158">เมื่อต้องการลบการเชื่อมโยงของเรกคอร์ดทรัพยากรบุคคลและแถว Dataverse เลือกตารางในฟิลด์ **ตาราง Dataverse** แล้วเลือก **ล้างข้อมูลการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="3f185-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="3f185-159">[![การล้างข้อมูลการติดตาม](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="3f185-160">เมื่อต้องการรันการซิงโครไนส์แบบสมบูรณ์บนตารางหลังจากที่คุณล้างการติดตามแล้วให้ดูที่กระบวนงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="3f185-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="3f185-161">ซิงค์ตารางระหว่างทรัพยากรบุคคลและ Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="3f185-162">ใช้ขั้นตอนนี้เมื่อ:</span><span class="sxs-lookup"><span data-stu-id="3f185-162">Use this procedure when:</span></span>

- <span data-ttu-id="3f185-163">การเปลี่ยนแปลงจาก Dataverse ใช้เวลานานเกินไปกว่าที่จะปรากฏในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3f185-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="3f185-164">คุณต้องรีเฟรชตารางการติดตามหลังจากล้างการติดตาม</span><span class="sxs-lookup"><span data-stu-id="3f185-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="3f185-165">เมื่อต้องการรันการซิงโครไนส์ทั้งหมดในตารางระหว่างทรัพยากรบุคคลและ Dataverse:</span><span class="sxs-lookup"><span data-stu-id="3f185-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="3f185-166">เลือกตารางในฟิลด์ **ตาราง Dataverse**</span><span class="sxs-lookup"><span data-stu-id="3f185-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="3f185-167">เลือก **ซิงค์เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="3f185-167">Select **Sync now**.</span></span>

<span data-ttu-id="3f185-168">[![การรันการซิงโครไนส์แบบสมบูรณ์](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="3f185-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="3f185-169">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3f185-169">See also</span></span>

[<span data-ttu-id="3f185-170">ตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="3f185-171">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3f185-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="3f185-172">FAQ เกี่ยวกับตารางเสมือนสำหรับ Human Resources</span><span class="sxs-lookup"><span data-stu-id="3f185-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="3f185-173">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3f185-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="3f185-174">การอัปเดตศัพท์</span><span class="sxs-lookup"><span data-stu-id="3f185-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]