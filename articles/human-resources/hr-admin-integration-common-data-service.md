---
title: ตั้งค่าคอนฟิกการรวม Common Data Service
description: คุณสามารถเปิดหรือปิดการรวม Common Data Service กับอินสแตนซ์ของ Microsoft Dynamics 365 Human Resources ได้ นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ข้อมูลการติดตาม และรีซิงค์เอนทิตี้ที่จะช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมสองอย่างได้
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010704"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="cf484-104">ตั้งค่าคอนฟิกการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="cf484-105">คุณสามารถเปิดหรือปิดการรวม Common Data Service กับอินสแตนซ์ของ Microsoft Dynamics 365 Human Resources ได้</span><span class="sxs-lookup"><span data-stu-id="cf484-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="cf484-106">นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ข้อมูลการติดตาม และรีซิงค์เอนทิตี้ที่จะช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมสองอย่างได้</span><span class="sxs-lookup"><span data-stu-id="cf484-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="cf484-107">เมื่อคุณปิดการรวม ผู้ใช้สามารถทำการเปลี่ยนแปลงในทรัพยากรบุคคลหรือ Common Data Service แต่การเปลี่ยนแปลงดังกล่าวจะไม่มีการซิงค์ระหว่างสภาพแวดล้อมทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="cf484-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="cf484-108">โดยค่าเริ่มต้นการรวมระหว่างทรัพยากรบุคคลและ Common Data Service จะเปิดหรือปิดทั้งนี้ขึ้นอยู่กับการมีอยู่ของข้อมูลการสาธิตในสภาพแวดล้อม:</span><span class="sxs-lookup"><span data-stu-id="cf484-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="cf484-109">**ปิด** สำหรับสภาพแวดล้อมใหม่ที่ไม่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cf484-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="cf484-110">**เปิด** สำหรับสภาพแวดล้อมใหม่ที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cf484-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="cf484-111">สภาพแวดล้อมใหม่ที่รวมข้อมูลสาธิตจะเริ่มต้นการซิงค์ข้อมูลเมื่อมีการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cf484-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="cf484-112">คุณอาจต้องการปิดการรวมในสถานการณ์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cf484-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="cf484-113">คุณกำลังกรอกข้อมูลโดยใช้กรอบงานการจัดการข้อมูลและต้องนำเข้าข้อมูลหลายครั้งเพื่อให้ได้รับเป็นสถานะที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cf484-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="cf484-114">แต่ก็ยังมีปัญหากับข้อมูลในทรัพยากรบุคคลหรือ Common Data Service อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf484-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="cf484-115">ถ้าคุณปิดการรวมคุณสามารถลบเรกคอร์ดในสภาพแวดล้อมหนึ่งได้โดยไม่ต้องลบเรกคอร์ดนั้นออกจากเรกคอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="cf484-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="cf484-116">เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดในสภาพแวดล้อมที่ไม่มีการลบออกจะถูกซิงค์กลับไปยังสภาพแวดล้อมที่มีการลบออก</span><span class="sxs-lookup"><span data-stu-id="cf484-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="cf484-117">การซิงโครไนส์เริ่มต้นในครั้งถัดไปที่มีการรวม **Common Data Service ที่พลาดการซิงค์** การร้องขอรันชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cf484-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="cf484-118">เมื่อคุณปิดการรวมข้อมูลโปรดตรวจสอบให้แน่ใจว่าคุณไม่ได้แก้ไขเรกคอร์ดที่เหมือนกันในสภาพแวดล้อมทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="cf484-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="cf484-119">เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดที่คุณแก้ไขครั้งสุดท้ายจะถูกซิงค์</span><span class="sxs-lookup"><span data-stu-id="cf484-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="cf484-120">ดังนั้น ถ้าคุณไม่ได้ทำการเปลี่ยนแปลงที่เหมือนกันบนเรกคอร์ดในสภาพแวดล้อมทั้งสอง การสูญเสียข้อมูลอาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cf484-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="cf484-121">เข้าถึงหน้าการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="cf484-122">ในอินสแตนซ์ทรัพยากรบุคคลซึ่งคุณต้องการดูหรือตั้งค่าคอนฟิกการตั้งค่าสำหรับการรวมกับ Common Data Service เลือกไทล์ **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="cf484-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="cf484-123">[![ไทล์การจัดการระบบ](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="cf484-124">เลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="cf484-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="cf484-125">[![แท็บลิงค์](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="cf484-126">ภายใต้ **การรวม** เลือก **การตั้งค่าคอนฟิก Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="cf484-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="cf484-127">[![Common Data Service ลิงค์การตั้งค่าคอนฟิก](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="cf484-128">เปิดหรือปิดการรวมข้อมูลระหว่างทรัพยากรบุคคลและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="cf484-129">เมื่อต้องการเปิดการรวมให้ตั้งค่า **การเปิดใช้การรวมสำหรับตัวเลือก Common Data Service** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cf484-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cf484-130">เมื่อคุณเปิดการรวม ข้อมูลจะถูกซิงค์ในครั้งถัดไปที่การรวม **Common Data Service พลาดการซิงค์** รันชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cf484-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="cf484-131">ข้อมูลทั้งหมดควรพร้อมใช้งานหลังจากชุดงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cf484-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="cf484-132">เมื่อต้องการปิดใช้งานการรวมให้ตั้งตัวเลือกเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="cf484-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="cf484-133">[![การเปิดหรือปิด Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="cf484-134">ภาพรวมของรายละเอียดการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf484-134">View data integration details</span></span>

<span data-ttu-id="cf484-135">บนแท็บด่วน **การจัดการ** ของหน้า **การรวม Common Data Service** คุณสามารถดูวิธีการเชื่อมโยงเรกคอร์ดร่วมกันระหว่างทรัพยากรบุคคลและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="cf484-136">ถ้าต้องการดูเรกคอร์ดสำหรับเอนทิตี้ให้เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS**</span><span class="sxs-lookup"><span data-stu-id="cf484-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="cf484-137">กริดแสดงเรกคอร์ดทั้งหมดที่เชื่อมโยงกับเอนทิตี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cf484-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="cf484-138">[![การดูเรกคอร์ดสำหรับเอนทิตี้](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cf484-139">ไม่ใช่เอนทิตี้ Common Data Service ทั้งหมดที่แสดงอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="cf484-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="cf484-140">เฉพาะเอนทิตี้ที่สนับสนุนการใช้ฟิลด์ที่กำหนดเองเท่านั้นที่จะปรากฏในกริด</span><span class="sxs-lookup"><span data-stu-id="cf484-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="cf484-141">เอนทิตี้ใหม่จะพร้อมใช้งานโดยผ่านการเผยแพร่ของทรัพยากรบุคคลอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cf484-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="cf484-142">กริดประกอบด้วยฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cf484-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="cf484-143">**ชื่อของเอนทิตี้ CDS** – ชื่อของเอนทิตี้ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="cf484-144">**การอ้างอิงเอนทิตี้ CDS** – ตัวระบุที่ Common Data Service ใช้ในการระบุเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="cf484-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="cf484-145">ค่านี้เทียบเท่ากับค่า **RecId** ของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cf484-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="cf484-146">คุณสามารถค้นหาตัวระบุเมื่อคุณเปิดเอนทิตี้ Common Data Service ใน Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="cf484-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="cf484-147">**ชื่อเอนทิตี้ทรัพยากรบุคคล** – เอนทิตี้ที่มีการซิงค์ข้อมูลครั้งล่าสุดกับ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="cf484-148">เอนทิตี้สามารถมีคำนำหน้า Common Data Service หรือคำนำหน้าอื่น</span><span class="sxs-lookup"><span data-stu-id="cf484-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="cf484-149">**การอ้างอิงทรัพยากรบุคคล** – ค่า **RecId** ที่เชื่อมโยงกับเรกคอร์ดในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cf484-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="cf484-150">**ลบออกจาก CDS แล้ว** – ค่าที่บ่งชี้ว่าเรกคอร์ดถูกลบออกจาก Common Data Service หรือไม่</span><span class="sxs-lookup"><span data-stu-id="cf484-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="cf484-151">ลบการเชื่อมโยงของเรกคอร์ดในทรัพยากรบุคคลออกจาก Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="cf484-152">ถ้าคุณประสบปัญหาในระหว่างการซิงโครไนส์ข้อมูลระหว่างทรัพยากรบุคคลและ Common Data Service คุณอาจสามารถแก้ไขปัญหาเหล่านั้นได้ด้วยการล้างการติดตามและปล่อยให้ตารางการติดตามถูกรีซิงค์</span><span class="sxs-lookup"><span data-stu-id="cf484-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="cf484-153">ถ้าคุณลบการเชื่อมโยงออกแล้วเปลี่ยนหรือลบเรกคอร์ดใน Common Data Service การเปลี่ยนแปลงจะไม่ถูกซิงค์กับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cf484-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="cf484-154">ถ้าคุณทำการเปลี่ยนแปลงในทรัพยากรบุคคลเรกคอร์ดการติดตามใหม่จะถูกสร้างขึ้นและเรกคอร์จะถูกอัพเดตใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="cf484-155">เมื่อต้องการลบการเชื่อมโยงของเรกคอร์ดระหว่างทรัพยากรบุคคลและ Common Data Service เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS** แล้วเลือก **ล้างข้อมูลการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="cf484-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="cf484-156">[![การล้างข้อมูลการติดตาม](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="cf484-157">เมื่อต้องการรันการซิงโครไนส์แบบสมบูรณ์บนเอนทิตี้หลังจากที่คุณล้างการติดตามแล้วให้ดูที่กระบวนงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="cf484-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="cf484-158">ซิงค์เอนทิตี้ระหว่างทรัพยากรบุคคลและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf484-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="cf484-159">ใช้กระบวนงานนี้ถ้าการเปลี่ยนแปลงจาก Common Data Service ใช้เวลานานเกินไปที่จะปรากฏในทรัพยากรบุคคลหรือถ้าคุณต้องรีเฟรชตารางการติดตามหลังจากที่คุณล้างข้อมูลการติดตาม</span><span class="sxs-lookup"><span data-stu-id="cf484-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="cf484-160">เมื่อต้องการรันการซิงโครไนส์แบบสมบูรณ์บนเอนทิตี้ระหว่างทรัพยากรบุคคลและ Common Data Service เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS** แล้วเลือก **ซิงค์เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="cf484-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="cf484-161">[![การรันการซิงโครไนส์แบบสมบูรณ์](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="cf484-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


