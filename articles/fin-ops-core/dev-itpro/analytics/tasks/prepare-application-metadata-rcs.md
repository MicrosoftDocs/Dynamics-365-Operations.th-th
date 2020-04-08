---
title: จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่จะใช้ใน RCS
description: ขั้นตอนในหัวข้อนี้จะอธิบายวิธีการที่ผู้ใช้สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ ซึ่งประกอบด้วยข้อมูลเมตาของแอพลิเคชันสำหรับการออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ใน Regulatory configuration service (RCS)
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d091cd835cfcb7164f83259b69e3bc1d7c09dc4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143165"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="6dec4-103">จัดเตรียมข้อมูลเมตาของแอพลิเคชันที่จะใช้ใน RCS</span><span class="sxs-lookup"><span data-stu-id="6dec4-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6dec4-104">ขั้นตอนต่อไปนี้จะอธิบายวิธีการที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ ซึ่งประกอบด้วยข้อมูลเมตาของแอพลิเคชัน สำหรับการออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ใน Regulatory configuration service (RCS)</span><span class="sxs-lookup"><span data-stu-id="6dec4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="6dec4-105">การตั้งค่าคอนฟิกนี้จะถูกใช้สำหรับการออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER เพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="6dec4-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="6dec4-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ</span><span class="sxs-lookup"><span data-stu-id="6dec4-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="6dec4-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในหัวข้อให้เสร็จสมบูรณ์ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="6dec4-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6dec4-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6dec4-108">Prerequisites</span></span>
1.    <span data-ttu-id="6dec4-109">ไปที่ **การจัดการองค์กร** > **พื้นที่ทำงาน** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="6dec4-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="6dec4-110">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="6dec4-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6dec4-111">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6dec4-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="6dec4-112">คลิก **การตั้งค่าคอนฟิกข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="6dec4-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="6dec4-113">สมมติว่า RCS จะถูกใช้เพื่อออกแบบโซลูชัน ER สำหรับแอพลิเคชัน Finance and Operation ที่จะสร้างเอกสารอิเล็กทรอนิกส์ที่มีข้อมูลจากโดเมนธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="6dec4-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="6dec4-114">เมื่อต้องการระบุการแม็ประหว่างแบบจำลองข้อมูล ER และแหล่งที่มาของข้อมูลที่จำเป็น ใน RCS เราต้องมีสิทธิเข้าถึงข้อมูลเมตาของแอพลิเคชัน Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="6dec4-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="6dec4-115">ดังนั้น ในฐานะที่เป็นส่วนหนึ่งของการของการออกแบบโซลูชัน ER เราตั้งค่าคอนฟิกการตั้งค่าคอนฟิกข้อมูลเมตาของ ER ใหม่ที่มีข้อมูลเมตาทั้งหมดที่จำเป็นในปัจจุบัน สำหรับการสร้างรายงาน ER สำหรับโดเมนธุรกิจที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6dec4-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="6dec4-116">การตั้งค่าคอนฟิกเพิ่มข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="6dec4-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="6dec4-117">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6dec4-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="6dec4-118">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ข้อมูลเมตาการค้าต่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="6dec4-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="6dec4-119">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6dec4-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="6dec4-120">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="6dec4-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="6dec4-121">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6dec4-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6dec4-122">คุณสามารถเลือกข้อมูลเมตาทั้งหมดสำหรับแอพลิเคชันทั้งหมด หรือแบบจำลองที่เลือกหรือโมดูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6dec4-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="6dec4-123">โปรดทราบว่าในกรณีนี้ ข้อมูลเมตาต่อไปนี้จะถูกเพิ่มโดยอัตโนมัติ: ตารางของเรกคอร์ด การแจงนับ และชนิดข้อมูลแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="6dec4-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="6dec4-124">เมื่อจำเป็นต้องใช้ข้อมูลเมตาชนิดอื่นๆ ต้องมีการเพิ่มด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6dec4-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="6dec4-125">เรามีข้อมูลเมตาบางอย่างที่เกี่ยวข้องกับธุรกรรมการค้าต่างประเทศ โดยการเลือกรายการข้อมูลเมตาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6dec4-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="6dec4-126">คลิก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6dec4-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="6dec4-127">คลิก **เรกคอร์ดของตาราง**</span><span class="sxs-lookup"><span data-stu-id="6dec4-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="6dec4-128">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์ **ชื่อ** ด้วยค่าของ 'อินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="6dec4-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="6dec4-129">เลือกเรกคอร์ดตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="6dec4-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="6dec4-130">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6dec4-130">Click **OK**.</span></span>
  
<span data-ttu-id="6dec4-131">คุณได้เพิ่มข้อมูลของข้อมูลเมตาเกี่ยวกับตารางอินทราสแทตของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6dec4-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="6dec4-132">ในแผนภูมิ ขยาย **อินทราสแทตของเรกคอร์ดตาราง**\>**ความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="6dec4-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="6dec4-133">ในแผนภูมิ ให้เลือก **อินทราสแทตของเรกคอร์ดตาราง**\>**ความสัมพันธ์\IntrastatCommodity (เรกคอร์ดตาราง EcoResCategory)**</span><span class="sxs-lookup"><span data-stu-id="6dec4-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="6dec4-134">คลิก **เพิ่มข้อมูลเมตา**</span><span class="sxs-lookup"><span data-stu-id="6dec4-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6dec4-135">ต้องมีการเพิ่มข้อมูลเมตาด้วยตนเองเกี่ยวกับความสัมพันธ์ที่จำเป็นสำหรับตารางของเรกคอร์ดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6dec4-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="6dec4-136">คลิก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6dec4-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="6dec4-137">คลิก **การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="6dec4-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="6dec4-138">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์ **ชื่อ** ด้วยค่าของ 'IntrastatDirection'</span><span class="sxs-lookup"><span data-stu-id="6dec4-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="6dec4-139">เลือกเรกคอร์ด **การแจงนับ IntrastatDirection**</span><span class="sxs-lookup"><span data-stu-id="6dec4-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="6dec4-140">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6dec4-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="6dec4-141">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6dec4-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="6dec4-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6dec4-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="6dec4-143">ดำเนินการตั้งค่าคอนฟิกข้อมูลเมตารุ่นแบบร่างให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6dec4-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="6dec4-144">คลิก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="6dec4-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="6dec4-145">คลิก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="6dec4-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="6dec4-146">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6dec4-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="6dec4-147">เลือกรุ่นที่เสร็จสมบูรณ์ **1**</span><span class="sxs-lookup"><span data-stu-id="6dec4-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="6dec4-148">ส่งออกการตั้งค่าคอนฟิกข้อมูลเมตารุ่นที่เสร็จสมบูรณ์จากแอพลิเคชันเป็นไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="6dec4-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="6dec4-149">คลิก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="6dec4-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="6dec4-150">คลิก **ส่งออกเป็นไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="6dec4-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="6dec4-151">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6dec4-151">Click **OK**.</span></span> 
    
<span data-ttu-id="6dec4-152">การตั้งค่าคอนฟิกข้อมูลเมตาของ ER ที่สร้างเป็นไฟล์ XML ที่สามารถนำเข้าไปยัง RCS และใช้เป็นแหล่งที่มาของข้อมูลเกี่ยวกับข้อมูลเมตาสำหรับโดเมนธุรกิจการค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="6dec4-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="6dec4-153">ตามข้อมูลนี้ เราสามารถระบุการแม็ประหว่างข้อมูลเมตาของแอพลิเคชันและแบบจำลองข้อมูล ER ได้</span><span class="sxs-lookup"><span data-stu-id="6dec4-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
