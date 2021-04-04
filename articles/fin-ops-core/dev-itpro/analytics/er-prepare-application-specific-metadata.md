---
title: จัดเตรียมข้อมูลเมตาเฉพาะของแอพลิเคชันสำหรับ RCS และ ER
description: หัวข้อนี้จะอธิบายถึงวิธีการจัดเตรียมข้อมูลเมตาเฉพาะแอพลิเคชันสำหรับ Regulatory configuration service (RCS) และการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 37da06f4ba86594c6368dcd1049456c58bf87e3a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565476"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="1ccec-103">จัดเตรียมข้อมูลเมตาเฉพาะของแอพลิเคชันสำหรับ RCS และ ER</span><span class="sxs-lookup"><span data-stu-id="1ccec-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1ccec-104">หัวข้อนี้จะนำคุณไปสู่ตัวอย่างของงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1ccec-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="1ccec-105">จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่สามารถใช้ได้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="1ccec-106">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="1ccec-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="1ccec-107">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="1ccec-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="1ccec-108">จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่สามารถใช้ได้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="1ccec-109">กระบวนการต่อไปนี้แสดงวิธีการที่ผู้ใช้ที่มีบทบาท **ผู้ดูแลระบบ** หรือ **ผู้พัฒนาการรายงานทางอิเล็กทรอนิกส์** สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีข้อมูลเมตาสำหรับแอพลิเคชัน และที่ใช้เพื่อออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ใน Regulatory configuration service (RCS)</span><span class="sxs-lookup"><span data-stu-id="1ccec-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="1ccec-110">การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ของตัวอย่างที่สร้างขึ้นในตัวอย่างนี้ จะใช้ในการเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="1ccec-111">สำหรับตัวอย่างนี้ คุณต้องการใช้ RCS เพื่อออกแบบโซลูชัน ER สำหรับแอพลิเคชั่น ที่จะใช้ในการสร้างเอกสารอิเล็กทรอนิกส์ที่มีข้อมูลจากโดเมนธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="1ccec-112">เมื่อต้องการระบุการแม็ประหว่างแบบจำลองข้อมูล ER และแหล่งที่มาของข้อมูลที่จำเป็น คุณต้องมีสิทธิเข้าถึงข้อมูลเมตาของแอพลิเคชันใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="1ccec-113">ดังนั้น ในฐานะที่เป็นส่วนหนึ่งของกระบวนการของการออกแบบโซลูชัน ER คุณต้องตั้งค่าคอนฟิกการตั้งค่าคอนฟิกข้อมูลเมตาของ ER ใหม่ที่มีข้อมูลเมตาทั้งหมดที่จำเป็นในปัจจุบัน เพื่อสร้างรายงาน ER สำหรับโดเมนธุรกิจที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1ccec-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="1ccec-114">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ</span><span class="sxs-lookup"><span data-stu-id="1ccec-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="1ccec-115">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="1ccec-116">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1ccec-117">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1ccec-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="1ccec-118">เลือก **การตั้งค่าคอนฟิกข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="1ccec-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="1ccec-119">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="1ccec-120">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="1ccec-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="1ccec-121">สำหรับตัวอย่างนี้ ให้ป้อน **ข้อมูลเมตาการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="1ccec-122">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="1ccec-123">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-123">Select **Designer**.</span></span>
8. <span data-ttu-id="1ccec-124">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-125">คุณสามารถเลือกข้อมูลเมตาทั้งหมดสำหรับแอพลิเคชันทั้งหมด หรือสำหรับแบบจำลองหรือโมดูลที่เลือก อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ccec-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="1ccec-126">ในทั้งสองกรณี โปรดทราบว่าข้อมูลเมตาต่อไปนี้จะถูกเพิ่มโดยอัตโนมัติ: ตารางของเรกคอร์ด การแจงนับ และชนิดข้อมูลแบบขยาย (EDTs)</span><span class="sxs-lookup"><span data-stu-id="1ccec-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="1ccec-127">เมื่อจำเป็นต้องใช้ข้อมูลเมตาชนิดอื่นๆ ต้องมีการเพิ่มด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1ccec-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="1ccec-128">คุณต้องเพิ่มข้อมูลเมตาบางอย่างที่เกี่ยวข้องกับธุรกรรมการค้าต่างประเทศ และเลือกรายการข้อมูลเมตาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1ccec-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="1ccec-129">เลือก **เพิ่มแหล่งข้อมูล \> เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="1ccec-130">กรองค่าของ **อินทราสแทต** ในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="1ccec-131">เลือกเรกคอร์ดตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="1ccec-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="1ccec-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-132">Select **OK**.</span></span>

    <span data-ttu-id="1ccec-133">คุณต้องเพิ่มข้อมูลเมตาเกี่ยวกับตารางอินทราสแทตของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1ccec-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="1ccec-134">ในแผนภูมิ ให้เลือก **อินทราสแทตเรกคอร์ดตาราง \> \>ความสัมพันธ์ \> IntrastatCommodity (ตารางเรกคอร์ด EcoResCategory)**</span><span class="sxs-lookup"><span data-stu-id="1ccec-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="1ccec-135">เลือก **เพิ่มข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="1ccec-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-136">ต้องมีการเพิ่มข้อมูลเมตาด้วยตนเองเกี่ยวกับความสัมพันธ์ที่จำเป็นสำหรับตารางของเรกคอร์ดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1ccec-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="1ccec-137">เลือก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1ccec-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="1ccec-138">เลือก **การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="1ccec-139">กรองค่าของ **IntrastatDirection** ในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="1ccec-140">เลือกเรกคอร์ดการแจงนับ **IntrastatDirection**</span><span class="sxs-lookup"><span data-stu-id="1ccec-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="1ccec-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-141">Select **OK**.</span></span>
20. <span data-ttu-id="1ccec-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-142">Select **Save**.</span></span>
21. <span data-ttu-id="1ccec-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ccec-143">Close the page.</span></span>
22. <span data-ttu-id="1ccec-144">ดำเนินการตั้งค่าคอนฟิกข้อมูลเมตารุ่นแบบร่างให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="1ccec-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="1ccec-145">เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="1ccec-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-146">Select **OK**.</span></span>
    3. <span data-ttu-id="1ccec-147">เลือกรุ่นที่เสร็จสมบูรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="1ccec-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="1ccec-148">ส่งออกการตั้งค่าคอนฟิกข้อมูลเมตารุ่นที่เสร็จสมบูรณ์จากแอพลิเคชันเป็นไฟล์ XML:</span><span class="sxs-lookup"><span data-stu-id="1ccec-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="1ccec-149">เลือก **แลกเปลี่ยน \> ส่งออกเป็นไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1ccec-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="1ccec-150">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-150">Select **OK**.</span></span>

<span data-ttu-id="1ccec-151">การตั้งค่าคอนฟิกข้อมูลเมตา ER ที่คุณสร้างขึ้นจะถูกบันทึกเป็นไฟล์ **Foreign trade metadata.xml**</span><span class="sxs-lookup"><span data-stu-id="1ccec-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="1ccec-152">ขณะนี้คุณสามารถนำเข้าไปยัง RCS เพื่อให้สามารถใช้เป็นแหล่งที่มาของข้อมูลเมตาสำหรับโดเมนธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="1ccec-153">ตามข้อมูลนี้ คุณสามารถระบุการแม็ประหว่างข้อมูลเมตาของแอพลิเคชันและแบบจำลองข้อมูล ER ได้</span><span class="sxs-lookup"><span data-stu-id="1ccec-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="1ccec-154">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="1ccec-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="1ccec-155">กระบวนงานต่อไปนี้แสดงวิธีการที่ผู้ใช้ RCS ที่มีบทบาท **ผู้ดูแลระบบ** หรือ **ผู้พัฒนารายงานอิเล็กทรอนิกส์** สามารถออกแบบการแม็ปแบบจำลอง ER ใหม่โดยใช้ข้อมูลเมตาจากแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="1ccec-156">ข้อมูลเมตาของแอพลิเคชันจะสามารถเข้าถึงได้โดยใช้การตั้งค่าคอนฟิกข้อมูลเมตา ER ซึ่งประกอบด้วยชุดตัวอย่างของข้อมูลเมตาเพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="1ccec-157">ก่อนที่คุณจะสามารถดำเนินกระบวนงานนี้ให้เสร็จสมบูรณ์ อันดับแรกคุณจะต้องดำเนินการกระบวนงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="1ccec-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="1ccec-158">สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายว่าใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1ccec-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="1ccec-159">จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่สามารถใช้ได้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="1ccec-160">ไปที่ **พื้นที่ทำงานทั้งหมด \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="1ccec-161">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1ccec-162">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1ccec-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="1ccec-163">นำเข้าการตั้งค่าคอนฟิกข้อมูลเมตา ER ซึ่งประกอบด้วยข้อมูลเมตาสำหรับแอพลิเคชั่น และที่ได้รับการตั้งค่าคอนฟิกเพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับโดเมนธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="1ccec-164">คุณได้สร้างการตั้งค่าคอนฟิกข้อมูลเมตา ER นี้ และส่งออกเป็นไฟล์ XML ในกระบวนงาน [จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่สามารถใช้ใน RCS](#prepare-application-metadata-that-can-be-used-in-rcs) ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="1ccec-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="1ccec-165">เลือก **การตั้งค่าคอนฟิกข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="1ccec-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="1ccec-166">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="1ccec-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="1ccec-167">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1ccec-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="1ccec-168">เรียกดูเพื่อเลือกไฟล์ **Foreign trade metadata.xml**</span><span class="sxs-lookup"><span data-stu-id="1ccec-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="1ccec-169">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-169">Select **OK**.</span></span>
    6. <span data-ttu-id="1ccec-170">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ccec-170">Close the page.</span></span>

4. <span data-ttu-id="1ccec-171">สร้างการตั้งค่าคอนฟิกแบบจำลองข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="1ccec-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="1ccec-172">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="1ccec-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="1ccec-173">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="1ccec-174">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **แบบจำลองการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="1ccec-175">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="1ccec-176">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="1ccec-177">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="1ccec-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="1ccec-178">ในฟิลด์ **ชื่อ** ให้พิมพ์ **ราก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="1ccec-179">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="1ccec-180">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="1ccec-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="1ccec-181">ในฟิลด์ **ชื่อ** พิมพ์ **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="1ccec-182">ในฟิลด์ **ประเภทรายการ** ให้เลือก **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="1ccec-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="1ccec-183">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="1ccec-184">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="1ccec-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="1ccec-185">ในฟิลด์ **ชื่อ** พิมพ์ **รหัสโภคภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="1ccec-186">ในฟิลด์ **ประเภทรายการ** ให้เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="1ccec-187">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-187">Select **Add**.</span></span>

    9. <span data-ttu-id="1ccec-188">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="1ccec-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="1ccec-189">ในฟิลด์ชื่อ ให้พิมพ์ **จำนวนเงินที่ออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="1ccec-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="1ccec-190">ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="1ccec-191">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-191">Select **Add**.</span></span>

    10. <span data-ttu-id="1ccec-192">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="1ccec-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="1ccec-193">ในฟิลด์ **ชื่อ** ให้พิมพ์ **วันที่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="1ccec-194">ในฟิลด์ **ประเภทรายการ** ให้เลือก **วันที่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="1ccec-195">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1ccec-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="1ccec-196">เลือก **เพิ่ม \> การอ้างอิงราก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="1ccec-197">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-197">Select **OK**.</span></span>
    13. <span data-ttu-id="1ccec-198">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-198">Select **Save**.</span></span>
    14. <span data-ttu-id="1ccec-199">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ccec-199">Close the page.</span></span>
    15. <span data-ttu-id="1ccec-200">เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="1ccec-201">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-201">Select **OK**.</span></span>

5. <span data-ttu-id="1ccec-202">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง:</span><span class="sxs-lookup"><span data-stu-id="1ccec-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="1ccec-203">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="1ccec-204">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **สร้าง** ป้อน **การแม็ปแบบจำลองตามแบบจำลองการค้าต่างประเทศของแบบจำลองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1ccec-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="1ccec-205">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ปการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="1ccec-206">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="1ccec-207">บน FastTab **ข้อกำหนดเบื้องต้น** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1ccec-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="1ccec-208">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-208">Select **New**.</span></span>
    7. <span data-ttu-id="1ccec-209">ในฟิลด์ **ชนิดส่วนประกอบสำหรับข้อกำหนดเบื้องต้น** ให้เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="1ccec-210">เลือกการตั้งค่าคอนฟิก **ข้อมูลเมตาการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="1ccec-211">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-211">Select **Save**.</span></span> <span data-ttu-id="1ccec-212">โปรดสังเกตว่ามีการเพิ่มการอ้างอิงไปยังการตั้งค่าคอนฟิก **ข้อมูลเมตาการค้าต่างประเทศ** รุ่น 1</span><span class="sxs-lookup"><span data-stu-id="1ccec-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="1ccec-213">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="1ccec-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="1ccec-214">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ccec-214">Close the page.</span></span>
    11. <span data-ttu-id="1ccec-215">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="1ccec-216">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="1ccec-217">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations \> เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="1ccec-218">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="1ccec-219">ในฟิลด์ **ชื่อ** ให้ป้อน **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="1ccec-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="1ccec-220">เลือกเรกคอร์ดตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="1ccec-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="1ccec-221">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1ccec-222">มีการเสนอตารางเพียง 2 ตารางเท่านั้น เนื่องจากมีการเพิ่มตารางเพียง 2 ตาราไปยังชุดของข้อมูลเมตาที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="1ccec-223">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="1ccec-224">ในแผนภูมิ เลือก **อินทราสแทต \> AmountMST**</span><span class="sxs-lookup"><span data-stu-id="1ccec-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="1ccec-225">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต \> จำนวนเงินที่ออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="1ccec-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="1ccec-226">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="1ccec-227">ในแผนภูมิ เลือก **อินทราสแทต \> TransDate**</span><span class="sxs-lookup"><span data-stu-id="1ccec-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="1ccec-228">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต \> วันที่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="1ccec-229">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="1ccec-230">ในแผนภูมิ เลือก **อินทราสแทต \> \>ความสัมพันธ์ \> IntrastatCommodity \> รหัส**</span><span class="sxs-lookup"><span data-stu-id="1ccec-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="1ccec-231">ในแผนภูมิ เลือก **ธุรกรรม = อินทราสแทต \> รหัสโภคภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="1ccec-232">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="1ccec-233">เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1ccec-234">หลังจากที่การตรวจสอบเสร็จสมบูรณ์แล้ว เราประสบความสำเร็จในการผูกองค์ประกอบของแบบจำลองข้อมูลกับรายการของแหล่งข้อมูล ซึ่งอธิบายโดยใช้รายละเอียดของข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกข้อมูลเมตาของ ER ที่อ้างอิง</span><span class="sxs-lookup"><span data-stu-id="1ccec-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="1ccec-235">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-235">Select **Save**.</span></span>

<span data-ttu-id="1ccec-236">เมื่อคุณต้องการ คุณสามารถขยายชุดข้อมูลเมตาที่มีอยู่ในแอพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="1ccec-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="1ccec-237">หลังจากนั้น คุณสามารถส่งออกการตั้งค่าคอนฟิกข้อมูลเมตา ER รุ่นใหม่ที่เสร็จสมบูรณ์ นำเข้าไปยัง RCS และปรับปรุงข้อกำหนดเบื้องต้นของการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่ตั้งค่าคอนฟิก เพื่ออ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตาที่นำเข้ารุ่นใหม่</span><span class="sxs-lookup"><span data-stu-id="1ccec-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="1ccec-238">วิธีนี้สำหรับการรับข้อมูลเกี่ยวกับข้อมูลเมตาของแอพลิเคชันจะพร้อมใช้งานเฉพาะสำหรับแอพลิเคชันที่ปรับใช้เฉพาะที่ (นั่นคือ เมื่อมีการใช้แบบจำลองการปรับใช้แบบข้อมูลธุรกิจเฉพาะที่ \[LBD\] หรือแบบ on-premises สำหรับแอพลิเคชั่น)</span><span class="sxs-lookup"><span data-stu-id="1ccec-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="1ccec-239">เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="1ccec-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="1ccec-240">กระบวนงานต่อไปนี้แสดงวิธีการที่ผู้ใช้ RCS ที่มีบทบาท **ผู้ดูแลระบบ** หรือ **ผู้พัฒนารายงานอิเล็กทรอนิกส์** สามารถออกแบบการแม็ปแบบจำลอง ER ใหม่โดยใช้ข้อมูลเมตาของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="1ccec-241">จะมีการเข้าถึงข้อมูลเมตาของแอพลิเคชันแบบออนไลน์โดยใช้แอพลิเคชันที่เชื่อมต่อ RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="1ccec-242">จะมีการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ตัวอย่าง เพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1ccec-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="1ccec-243">เพื่อทำให้กระบวนงานนี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์ใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="1ccec-244">ถ้าคุณยังไม่ได้ดำเนินการกระบวนงาน [เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER](#access-application-metadata-by-using-an-er-configuration) ในหัวข้อนี้ให้เสร็จสมบูรณ์ก่อนหน้านี้ ให้ไปที่หน้า [คู่มืองานการรายงานทางอิเล็กทรอนิกส์สำหรับ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) เพื่อดาวน์โหลดไฟล์การตั้งค่าคอนฟิก ER ต่อไปนี้ล่วงหน้า และบันทึกไว้เฉพาะที่: **Foreign trade metadata.xml** **Foreign trade model.xml** และ **Foreign trade mapping.xml**</span><span class="sxs-lookup"><span data-stu-id="1ccec-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="1ccec-245">รับการตั้งค่าคอนฟิก ER ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="1ccec-245">Get required ER configurations</span></span>

<span data-ttu-id="1ccec-246">ถ้าคุณดำเนินกระบวนงาน [เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER](#access-application-metadata-by-using-an-er-configuration) เสร็จสมบูรณ์แล้ว ก่อนหน้านี้ในหัวข้อนี้ คุณมีการตั้งค่าคอนฟิก ER ที่จำเป็นทั้งหมดแล้ว (ข้อมูลเมตาการค้าต่างประเทศ การตั้งค่าคอนฟิกแบบจำลองและการแม็ป) ในอินสแตนซ์ RCS ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="1ccec-247">ในกรณีนั้น คุณสามารถข้ามกระบวนงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="1ccec-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="1ccec-248">ไปที่ **พื้นที่ทำงานทั้งหมด \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="1ccec-249">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="1ccec-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="1ccec-250">โหลดไฟล์การตั้งค่าคอนฟิก **Foreign trade metadata.xml** **Foreign trade model.xml** และ **Foreign trade mapping.xml** ที่ทำซ้ำกลุ่มของขั้นตอนต่อไปนี้สำหรับแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="1ccec-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="1ccec-251">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="1ccec-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="1ccec-252">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1ccec-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="1ccec-253">เลือก **เรียกดู** และเลือกไฟล์</span><span class="sxs-lookup"><span data-stu-id="1ccec-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="1ccec-254">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="1ccec-255">ลงทะเบียนการเชื่อมต่อกับแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-255">Register the connection with the application</span></span>

1. <span data-ttu-id="1ccec-256">ไปที่ **พื้นที่ทำงานทั้งหมด \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="1ccec-257">เลือก **แอพลิเคชันที่เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="1ccec-258">ตรวจสอบให้แน่ใจว่าแอพลิเคชันที่ตั้งค่าคอนฟิกเป็นไปตาม Microsoft Azure และเข้าถึงได้โดยทั่วไปสำหรับผู้ใช้ RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="1ccec-259">ผู้ใช้ RCS ปัจจุบันต้องมีสิทธิ์เข้าถึงโปรแกรมประยุกต์ที่ตั้งค่าคอนฟิกที่มีการลงทะเบียนเป็นผู้ใช้ของโปรแกรมประยุกต์นี้ ในบทบาทที่ให้พวกเขามีสิทธิ์ในการเข้าถึงข้อมูลเมตาของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="1ccec-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="1ccec-260">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ccec-260">Select **New**.</span></span>
5. <span data-ttu-id="1ccec-261">ในฟิลด์ **ชื่อ** ให้ป้อน **MyConnectedApp** เป็นชื่อของแอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="1ccec-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="1ccec-262">ในฟิลด์ **แอพลิเคชัน** ให้ระบุ URL ของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="1ccec-263">ในฟิลด์ **ผู้เช่า** ให้ระบุผู้ให้บริการของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="1ccec-264">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-264">Select **Save**.</span></span> 
9. <span data-ttu-id="1ccec-265">เมื่อคุณตรวจสอบการเชื่อมต่อไปยังแอพลิเคชันที่ตั้งค่าคอนฟิก บนหน้า **เชื่อมต่อกับแอพลิเคชันระยะไกล** เลือกลิงค์ **เลือกที่นี่เพื่อเชื่อมต่อกับแอพลิเคชันระยะไกลที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="1ccec-266">เลือก **ตรวจสอบการเชื่อมต่อ** เพื่อตรวจสอบความถูกต้องของการเข้าถึงแอพลิเคชันที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="1ccec-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="1ccec-267">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="1ccec-267">Select **Close**.</span></span>

<span data-ttu-id="1ccec-268">หลังจากที่คุณดำเนินการกระบวนงานนี้เสร็จสมบูรณ์แล้ว และการตรวจสอบความถูกต้องของการเชื่อมต่อประสบความสำเร็จ จะมีการปรับปรุงรุ่นและรายละเอียดผู้เช่าสำหรับแอพลิเคชันที่ตั้งค่าคอนฟิกในกริดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1ccec-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="1ccec-269">ตรวจทานการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1ccec-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="1ccec-270">ไปที่ **พื้นที่ทำงานทั้งหมด \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1ccec-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="1ccec-271">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="1ccec-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="1ccec-272">ในแผนภูมิ ให้เลือก **แบบจำลองการค้าต่างประเทศ \> การแม็ปการค้าต่างประเทศ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="1ccec-273">เลือก FastTab **ข้อกำหนดเบื้องต้น**</span><span class="sxs-lookup"><span data-stu-id="1ccec-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-274">ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="1ccec-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1ccec-275">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="1ccec-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="1ccec-276">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-276">Select **Designer**.</span></span>
5. <span data-ttu-id="1ccec-277">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-277">Select **Designer**.</span></span>
6. <span data-ttu-id="1ccec-278">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations \> เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="1ccec-279">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-279">Select **Add root**.</span></span>
8. <span data-ttu-id="1ccec-280">ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1ccec-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-281">ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="1ccec-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1ccec-282">ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ</span><span class="sxs-lookup"><span data-stu-id="1ccec-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="1ccec-283">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="1ccec-284">กำหนดแอพลิเคชันที่เชื่อมต่อให้กับการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="1ccec-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="1ccec-285">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1ccec-285">Select **Edit**.</span></span>
2. <span data-ttu-id="1ccec-286">ใน **ฟิลด์แอพลิเคชันที่เชื่อมต่อ** ให้เลือกแอพลิเคชัน **MyConnectedApp**</span><span class="sxs-lookup"><span data-stu-id="1ccec-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-287">การแม็ปนี้อ้างอิงถึงข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1ccec-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="1ccec-288">ถ้าการแม็ปอ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตาและแอพลิเคชันที่เชื่อมต่อในเวลาเดียวกัน จะมีการใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="1ccec-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="1ccec-289">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-289">Select **Designer**.</span></span>
4. <span data-ttu-id="1ccec-290">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1ccec-290">Select **Designer**.</span></span>
5. <span data-ttu-id="1ccec-291">ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations \> เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="1ccec-292">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-292">Select **Add root**.</span></span>
7. <span data-ttu-id="1ccec-293">ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1ccec-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ccec-294">ณ จุดนี้ มีการนำเสนอตารางแอพลิเคชันมากกว่าสองตาราง เนื่องจากการแม็ปนี้ใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อทั้งหมดที่ได้รับการกำหนดไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="1ccec-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="1ccec-295">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="1ccec-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="1ccec-296">เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="1ccec-296">Select **Validate**.</span></span>

<span data-ttu-id="1ccec-297">ขณะนี้คุณได้ผูกองค์ประกอบของแบบจำลองข้อมูลกับรายการของแหล่งข้อมูลที่อธิบายโดยใช้รายละเอียดของข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อ ซึ่งได้รับการกำหนดสำหรับการแม็ปนี้</span><span class="sxs-lookup"><span data-stu-id="1ccec-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="1ccec-298">เมื่อคุณต้องประเมินการแม็ปแบบจำลองนี้โดยใช้ข้อมูลเมตาของแอพลิเคชันรุ่นอื่น ลงทะเบียนแอพลิเคชันอื่นที่เชื่อมต่อ กำหนดให้กับการแม็ปแบบจำลองนี้ และตรวจสอบความถูกต้องเทียบกับข้อมูลเมตาใหม่</span><span class="sxs-lookup"><span data-stu-id="1ccec-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ccec-299">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1ccec-299">Additional resources</span></span>

<span data-ttu-id="1ccec-300">อีกทางหนึ่งคือ คุณสามารถเล่นคู่มืองาน **จัดเตรียมข้อมูลเมตาของแอพลิเคชันซึ่งสามารถใช้ใน RCS** ในแอพลิเคชั่น เช่นเดียวกับคู่มืองาน **เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้การตั้งค่าคอนฟิก ER** และ **เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ** ใน RCS</span><span class="sxs-lookup"><span data-stu-id="1ccec-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="1ccec-301">คู่มืองานเหล่านี้สามารถดาวน์โหลดได้จากหน้า [คู่มืองานการรายงานอิเล็กทรอนิกส์สำหรับ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739)</span><span class="sxs-lookup"><span data-stu-id="1ccec-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]