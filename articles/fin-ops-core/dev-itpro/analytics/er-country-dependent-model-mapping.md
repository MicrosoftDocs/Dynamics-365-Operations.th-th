---
title: ตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER ที่ขึ้นกับบริบทของประเทศ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการแม็ปแบบจำลอง ER เพื่อให้ขึ้นอยู่กับบริบทของประเทศ/ภูมิภาคของนิติบุคคลที่ควบคุมการใช้งาน
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 6c4b18a3cf2ba313756d5f761ef1beb2c3015516
ms.sourcegitcommit: 56add4c49c35c65a75fa2ca5234927e7f7cd66ef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781156"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="109cb-103">ตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER ที่ขึ้นกับบริบทของประเทศ</span><span class="sxs-lookup"><span data-stu-id="109cb-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="109cb-104">คุณสามารถตั้งค่าคอนฟิกการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อให้ใช้แบบจำลองข้อมูล ER ทั่วไป แต่เฉพาะกับ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="109cb-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="109cb-105">หัวข้อนี้อธิบายถึงวิธีการออกแบบการแม็ปแบบจำลอง ER ต่างๆ สำหรับแบบจำลองข้อมูล ER เพื่อควบคุมวิธีการใช้โดยรูปแบบ ER ที่สอดคล้องกัน ซึ่งรันจากบริษัทที่มีบริบทของประเทศ/ภูมิภาคแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="109cb-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="109cb-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-106">Prerequisites</span></span>

<span data-ttu-id="109cb-107">เพื่อทำตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องมีการเข้าถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="109cb-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="109cb-108">การเข้าถึง Finance สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="109cb-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="109cb-109">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="109cb-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="109cb-110">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="109cb-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="109cb-111">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="109cb-111">System administrator</span></span>

- <span data-ttu-id="109cb-112">การเข้าถึงไปยังอินสแตนซ์ของ Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="109cb-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="109cb-113">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="109cb-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="109cb-114">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="109cb-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="109cb-115">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="109cb-115">System administrator</span></span>

<span data-ttu-id="109cb-116">บางขั้นตอนในหัวข้อนี้จำเป็นต้องมีการดำเนินการของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="109cb-117">ในบางกรณี การดำเนินการของรูปแบบ ER อาจได้รับผลกระทบจากบริบทของประเทศ/ภูมิภาคของบริษัทที่คุณกำลังลงชื่อเข้าใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="109cb-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="109cb-118">คุณสามารถรันรูปแบบ ER ในอินสแตนซ์ RCS ปัจจุบัน ถ้าบริษัทที่มีบริบทประเทศ/ภูมิภาคที่จำเป็นต้องมีอยู่ใน RCS</span><span class="sxs-lookup"><span data-stu-id="109cb-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="109cb-119">อย่างไรก็ตาม คุณต้องอัพโหลดการแม็ปแบบจำลองER และการตั้งค่าคอนฟิกรูปแบบ ER ที่สมบูรณ์ ซึ่งใช้รูปแบบข้อมูล ER กับอินสแตนซ์ Finance ของคุณ แล้วรันรูปแบบ ER ในอินสแตนซ์ Finance นั้น</span><span class="sxs-lookup"><span data-stu-id="109cb-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="109cb-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการนำเข้าการตั้งค่าคอนฟิกที่มีอยู่ใน RCS ไปยังอินสแตนซ์ Finance ดูที่ [การนำเข้าการตั้งค่าคอนฟิกจาก RCS](rcs-download-configurations.md)</span><span class="sxs-lookup"><span data-stu-id="109cb-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="109cb-121">กรณีการแม็ปแบบจำลองเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="109cb-121">Single model mapping case</span></span>

<span data-ttu-id="109cb-122">ทำตามขั้นตอนใน [ภาคผนวก 1](#appendix1) ของหัวข้อนี้ เพื่อออกแบบส่วนประกอบ ER ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="109cb-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="109cb-123">ขณะนี้คุณมีการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป)** ที่มีการแม็ปแบบจำลองสำหรับคำนิยาม **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-125">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-125">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-126">บน **เพจการตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="109cb-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-127">Select **OK**.</span></span>

<span data-ttu-id="109cb-128">โปรดสังเกตว่าเว็บเบราเซอร์มีให้ดาวน์โหลดไฟล์ข้อความที่สร้างขึ้นโดยรูปแบบ ER ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="109cb-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="109cb-129">เนื่องจากรูปแบบนี้ได้รับการตั้งค่าคอนฟิกที่ใช้คำนิยาม **จุดเข้าใช้งาน 1** และมีเฉพาะการแม็ปแบบจำลองเดี่ยวเท่านั้นที่พร้อมใช้งานสำหรับแบบจำลองพื้นฐานที่มีการแม็ปสำหรับคำนิยามนี้ รูปแบบ ER ที่ดำเนินการที่ใช้การแม็ปแบบจำลอง **การแม็ป (ทั่วไป)** ของการตั้งค่าคอนฟิก **การแม็ป (ทั่วไป)** เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="109cb-130">ดังนั้น ไฟล์ที่ดาวน์โหลดจะประกอบด้วยข้อความ **ฟังก์ชันทั่วไป 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="109cb-131">กรณีการแม็ปแบบจำลองที่ใช้ร่วมกันหลายตัว</span><span class="sxs-lookup"><span data-stu-id="109cb-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="109cb-132">ทำตามขั้นตอนใน [ภาคผนวก 2](#appendix2) ของหัวข้อนี้ เพื่อออกแบบส่วนประกอบ ER ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="109cb-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="109cb-133">ขณะนี้คุณมีการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป)** และ **การแม็ป (ทั่วไป) แบบกำหนดเอง** ที่มีการแม็ปแบบจำลองสำหรับคำนิยาม **จุดเข้าใช้งาน 1** </span><span class="sxs-lookup"><span data-stu-id="109cb-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-135">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-135">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-136">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="109cb-137">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="109cb-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-138">Select **OK**.</span></span>

<span data-ttu-id="109cb-139">โปรดสังเกตว่าการดำเนินการของรูปแบบ ER ที่เลือกไม่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="109cb-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="109cb-140">ข้อความแสดงข้อผิดพลาดแจ้งให้คุณทราบว่ามีการแม็ปแบบจำลองมากกว่าหนึ่งตัวอยู่สำหรับแบบจำลอง **แบบจำลองเพื่อเรียนรู้การแม็ป** และคำนิยาม **จุดเข้าใช้งาน 1** ในการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป)** และ **การแม็ป (ทั่วไป) แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="109cb-141">นอกจากนี้ข้อความขอแนะนำให้คุณเลือกการตั้งค่าคอนฟิกอย่างใดอย่างหนึ่งตามการตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="109cb-143">กำหนดการตั้งค่าคอนฟิกการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-143">Define a default mapping configuration</span></span>

<span data-ttu-id="109cb-144">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป) แบบกำหนดเอง** ตามการตั้งค่าคอนฟิกเริ่มต้น เพื่อให้สามารถใช้การแม็ปเป็นแหล่งข้อมูลสำหรับรูปแบบ ER **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="109cb-145">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ป (ทั่วไป) แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="109cb-146">ถ้าจำเป็น ให้เลือก **แก้ไข้** เพื่อทำให้เพจปัจจุบันพร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="109cb-147">ตั้งค่าตัวเลือก **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="109cb-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="109cb-148">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-148">Select **Save**.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-150">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-150">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-151">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="109cb-152">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="109cb-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-153">Select **OK**.</span></span>

<span data-ttu-id="109cb-154">โปรดสังเกตว่าการดำเนินการของรูปแบบ ER ที่เลือกสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="109cb-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="109cb-155">เว็บเบราเซอร์มีให้ดาวน์โหลดไฟล์ข้อความที่สร้างขึ้นโดยรูปแบบ ER ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="109cb-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="109cb-156">เนื่องจากรูปแบบนี้ได้รับการตั้งค่าคอนฟิกที่ใช้คำนิยาม **จุดเข้าใช้งาน 1** และการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป) แบบกำหนดเอง** ถูกเลือกเป็นการตั้งค่าคอนฟิกเริ่มต้น รูปแบบ ER ที่ดำเนินการที่ใช้การแม็ปแบบจำลอง **สำเนาการแม็ป (ทั่วไป)** ของการตั้งค่าคอนฟิก **การแม็ป (ทั่วไป) แบบกำหนดเอง** เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="109cb-157">ดังนั้น ไฟล์ที่ดาวน์โหลดจะประกอบด้วยข้อความ **ฟังก์ชันทั่วไป 1 แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="109cb-158">ถ้าคุณเปลี่ยนบริษัทที่คุณกำลังลงชื่อเข้าใช้ และรันการจัดรูปแบบ ER นี้อีกครั้ง คุณจะได้รับเนื้อหาเดียวกันในไฟล์ที่สร้างขึ้น เนื่องจากการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER เริ่มต้นไม่มีข้อจำกัดที่ขึ้นอยู่กับบริษัท</span><span class="sxs-lookup"><span data-stu-id="109cb-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="109cb-159">กรณีการแม็ปแบบจำลองผสมกันหลายตัว</span><span class="sxs-lookup"><span data-stu-id="109cb-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="109cb-160">ทำตามขั้นตอนใน [ภาคผนวก 3](#appendix3) ของหัวข้อนี้ เพื่อออกแบบส่วนประกอบ ER ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="109cb-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="109cb-161">ขณะนี้คุณมีการตั้งค่าคอนฟิก **การแม็ป (ทั่วไป)** **การแม็ป (ทั่วไป) แบบกำหนดเอง** และ **การแม็ปแบบจำลองการแม็ป (FR)** ที่มีการแม็ปแบบจำลองสำหรับคำนิยาม **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="109cb-162">โปรดสังเกตรุ่น 1 ของการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (FR)** กำหน้าค่าคอนฟิก เพื่อให้ใช้เฉพาะกับรูปแบบ ER ของแบบบจำลอง **แบบจำลองเพื่อเรียนรู้การแม็ป** ที่รันในบริษัททางการเงินที่มีบริบทของประเทศ/ภูมิภาคฝรั่งเศสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="109cb-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-164">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-164">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-165">เปลี่ยนบริษัทเป็น **FRSI**</span><span class="sxs-lookup"><span data-stu-id="109cb-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="109cb-166">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="109cb-167">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="109cb-168">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-168">Select **OK**.</span></span>

<span data-ttu-id="109cb-169">โปรดสังเกตว่าการดำเนินการของรูปแบบ ER ที่เลือกสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="109cb-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="109cb-170">เว็บเบราเซอร์มีให้ดาวน์โหลดไฟล์ข้อความที่สร้างขึ้นโดยรูปแบบ ER ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="109cb-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="109cb-171">เนื่องจากรูปแบบนี้ได้รับการตั้งค่าคอนฟิกที่ใช้คำนิยาม **จุดเข้าใช้งาน 1** และการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (ทั่วไป) แบบกำหนดเอง** ถูกเลือกเป็นการตั้งค่าคอนฟิกเริ่มต้น รูปแบบ ER ที่ดำเนินการที่ใช้การแม็ปแบบจำลอง **สำเนาการแม็ป (ทั่วไป)** ของการตั้งค่าคอนฟิก **การแม็ป (ทั่วไป) แบบกำหนดเอง** เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="109cb-172">ดังนั้น ไฟล์ที่ดาวน์โหลดจะประกอบด้วยข้อความ **ฟังก์ชันทั่วไป 1 แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="109cb-173">กำหนดการตั้งค่าคอนฟิกการแม็ปเฉพาะฝรั่งเศสเป็นการตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="109cb-174">ทำตามขั้นตอนต่อไปนี้ เพื่อกำหนดการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (FR)** แบบกำหนดเองเป็นการตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="109cb-175">โปรดทราบว่า เนื่องจากการแม็ปนี้เป็นฟิลด์เฉพาะสำหรับประเทศฝรั่งเศส จะถือว่าเป็นการแม็ปเริ่มต้นระหว่างการตั้งค่าคอนฟิกการแม็ปแบบจำลองทั้งหมดที่มีรหัสประเทศ **FR** ที่ระบุไว้ในฟิลด์ **รหัสประเทศ/ภูมิภาค ISO**</span><span class="sxs-lookup"><span data-stu-id="109cb-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="109cb-176">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ป (FR)**</span><span class="sxs-lookup"><span data-stu-id="109cb-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="109cb-177">ถ้าจำเป็น ให้เลือก **แก้ไข้** เพื่อทำให้เพจปัจจุบันพร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="109cb-178">ตั้งค่าตัวเลือก **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="109cb-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="109cb-179">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-179">Select **Save**.</span></span>

![หน้าการตั้งค่าคอนฟิก ER](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-181">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-181">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-182">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="109cb-183">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="109cb-184">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-184">Select **OK**.</span></span>

<span data-ttu-id="109cb-185">โปรดสังเกตว่าการดำเนินการของรูปแบบ ER ที่เลือกสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="109cb-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="109cb-186">เว็บเบราเซอร์มีให้ดาวน์โหลดไฟล์ข้อความที่สร้างขึ้นโดยรูปแบบ ER ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="109cb-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="109cb-187">เนื่องจากรูปแบบนี้ได้รับการตั้งค่าคอนฟิกที่ใช้คำนิยาม **จุดเข้าใช้งาน 1** และการตั้งค่าคอนฟิกการแม็ปแบบจำลอง **การแม็ป (FR)** ถูกเลือกเป็นการตั้งค่าคอนฟิกเริ่มต้น รูปแบบ ER ที่ดำเนินการที่ใช้การแม็ปแบบจำลอง **การแม็ป (FR)** ของการตั้งค่าคอนฟิก **การแม็ป (FR)** เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="109cb-188">ดังนั้น ไฟล์ที่ดาวน์โหลดจะประกอบด้วยข้อความ **ฟังก์ชัน 1 FR**</span><span class="sxs-lookup"><span data-stu-id="109cb-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="109cb-189">ถ้าคุณเปลี่ยนบริษัทที่คุณกำลัลงชื่อเข้าใช้ และรันรูปแบบ ER อีกครั้ง ผลลัพธ์จะขึ้นอยู่กับบริบทของประเทศ/ภูมิภาคของบริษัทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="109cb-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="109cb-190">กรณีการแม็ปแบบจำลองอื่น</span><span class="sxs-lookup"><span data-stu-id="109cb-190">Other model mapping cases</span></span>

<span data-ttu-id="109cb-191">เมื่อคุณได้เห็น การเลือกการแม็ปแบบจำลองสำหรับการดำเนินการของรูปแบบ ER ทำงานในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="109cb-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="109cb-192">ข้อกำหนดของการแม็ปแบบจำลองที่มีการระบุใช้รูปแบบ ER (**จุดเข้าใช้งาน1** ในตัวอย่างในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="109cb-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="109cb-193">การตั้งค่าคอนฟิกการแม็ปทั้งหมดที่มีการแม็ปที่มีคำนิยามที่ระบุ และที่ตอบสนองความต้องการของบริบทของประเทศ/ภูมิภาคใดๆที่มีการตั้งค่าคอนฟิก อาจใช้เพื่อรันรูปแบบ ER (**การแม็ป (ทั่วไป)** **การแม็ป (ทั่วไป) ที่กำหนดเอง** และ **การแม็ป (FR)** ในตัวอย่างนี้ในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="109cb-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="109cb-194">การแม็ปแบบจำลองเริ่มต้นใดๆ ที่มีข้อจำกัดบริบทของประเทศ/ภูมิภาคมีระดับความสำคัญสูงสุดสำหรับการเลือก (**การแม็ป (FR)** ในตัวอย่างนี้ในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="109cb-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="109cb-195">การแม็ปแบบจำลองเริ่มต้นใดๆ ที่ไม่มีข้อจำกัดบริบทของประเทศ/ภูมิภาคมีระดับความสำคัญสูงสุดถัดไปสำหรับการเลือก (**การแม็ป (ทั่วไป) แบบกำหนดเอง** ในตัวอย่างนี้ในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="109cb-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="109cb-196">การแม็ปแบบจำลองใดๆ ที่มีข้อจำกัดบริบทของประเทศ/ภูมิภาคมีระดับความสำคัญสูงสำหรับการเลือกกว่าการแม็ปแบบจำลองที่ไม่มีข้อจำกัดบริบทของประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="109cb-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="109cb-197">ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับผลลัพธ์ของการเลือกการแม็ปแบบจำลองสำหรับกรณีที่เป็นไปได้ทั้งหมดสำหรับการตั้งค่าการแม็ปแบบจำลอง:</span><span class="sxs-lookup"><span data-stu-id="109cb-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="109cb-198">คอลัมน์ 1 บ่งชี้ว่าการแม็ปแบบจำลองแรกที่ไม่มีข้อจำกัดบริบทของประเทศ/ภูมิภาค (ตัวอย่างเช่น การแม็ป **การแม็ป (ทั่วไป)** ที่ใช้ร่วมกัน) จะปรากฏขึ้น และถ้าเป็นเช่นนี้ ไม่ว่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** ถูกตั้งค่าเป็น **ใช่** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="109cb-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="109cb-199">คอลัมน์ 2 บ่งชี้ว่าการแม็ปแบบจำลองที่สองที่ไม่มีข้อจำกัดบริบทของประเทศ/ภูมิภาค (ตัวอย่างเช่น การแม็ป **การแม็ป (ทั่วไป) แบบกำหนดเอง** ที่ใช้ร่วมกัน) จะปรากฏขึ้น และถ้าเป็นเช่นนี้ ไม่ว่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** ถูกตั้งค่าเป็น **ใช่** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="109cb-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="109cb-200">คอลัมน์ 3 บ่งชี้ว่าการแม็ปแบบจำลองแรกที่มีข้อจำกัดบริบทของประเทศ/ภูมิภาค A (ตัวอย่างเช่น การแม็ป **การแม็ป (FR)** เฉพาะของฝรั่งเศส) จะปรากฏขึ้น และถ้าเป็นเช่นนี้ ไม่ว่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** ถูกตั้งค่าเป็น **ใช่** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="109cb-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="109cb-201">คอลัมน์ 4 บ่งชี้ว่าการแม็ปแบบจำลองที่สองที่มีข้อจำกัดบริบทของประเทศ/ภูมิภาค A จะปรากฏขึ้น และถ้าเป็นเช่นนี้ ไม่ว่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** ถูกตั้งค่าเป็น **ใช่** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="109cb-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="109cb-202">คอลัมน์ 5 แสดงผลลัพธ์ของการเลือกการแม็ปแบบจำลองสำหรับการดำเนินการของรูปแบบ ER ภายใต้การควบคุมของบริษัทที่มีบริบทของประเทศ/ภูมิภาค A</span><span class="sxs-lookup"><span data-stu-id="109cb-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="109cb-203">คอลัมน์ 6 แสดงผลลัพธ์ของการเลือกการแม็ปแบบจำลองสำหรับการดำเนินการของรูปแบบ ER ภายใต้การควบคุมของบริษัทที่มีบริบทของประเทศ/ภูมิภาค B</span><span class="sxs-lookup"><span data-stu-id="109cb-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="109cb-204">ในตาราง เครื่องหมายบวก (+) จะบ่งชี้ว่ามีการตั้งค่าคอนฟิกการแม็ปแบบจำลองในอินสแตนซ์ปัจจุบันของบริการ Microsoft Azure ที่ใช้ในการรันรูปแบบ ER (ทั้ง Finance หรือ RCS)</span><span class="sxs-lookup"><span data-stu-id="109cb-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="109cb-205">กรณี</span><span class="sxs-lookup"><span data-stu-id="109cb-205">Case</span></span> | <span data-ttu-id="109cb-206">การแม็ปแบบจำลอง 1 โดยไม่มีบริบทประเทศ/ภูมิภาค (MM1)</span><span class="sxs-lookup"><span data-stu-id="109cb-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="109cb-207">การแม็ปแบบจำลอง 2 โดยไม่มีบริบทประเทศ/ภูมิภาค (MM2)</span><span class="sxs-lookup"><span data-stu-id="109cb-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="109cb-208">การแม็ปแบบจำลอง 1 โดยมีบริบทประเทศ/ภูมิภาค A (MM1A)</span><span class="sxs-lookup"><span data-stu-id="109cb-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="109cb-209">การแม็ปแบบจำลอง 2 โดยมีบริบทประเทศ/ภูมิภาค A (MM2A)</span><span class="sxs-lookup"><span data-stu-id="109cb-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="109cb-210">ทำงานภายใต้การควบคุมของบริษัทที่มีบริบทตามประเทศ/ภูมิภาค A</span><span class="sxs-lookup"><span data-stu-id="109cb-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="109cb-211">ทำงานภายใต้การควบคุมของบริษัทที่มีบริบทตามประเทศ/ภูมิภาค B</span><span class="sxs-lookup"><span data-stu-id="109cb-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="109cb-212">1</span><span class="sxs-lookup"><span data-stu-id="109cb-212">1</span></span>   |     <span data-ttu-id="109cb-213">2</span><span class="sxs-lookup"><span data-stu-id="109cb-213">2</span></span>   |    <span data-ttu-id="109cb-214">3</span><span class="sxs-lookup"><span data-stu-id="109cb-214">3</span></span>    |    <span data-ttu-id="109cb-215">4</span><span class="sxs-lookup"><span data-stu-id="109cb-215">4</span></span>    |           <span data-ttu-id="109cb-216">5</span><span class="sxs-lookup"><span data-stu-id="109cb-216">5</span></span>               |            <span data-ttu-id="109cb-217">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="109cb-217">6</span></span>               |
|     <span data-ttu-id="109cb-218">1</span><span class="sxs-lookup"><span data-stu-id="109cb-218">1</span></span>   |         |         |         |         | <span data-ttu-id="109cb-219">ข้อผิดพลาด (การแม็ปที่ขาดหายไป)</span><span class="sxs-lookup"><span data-stu-id="109cb-219">Error (missing mapping)</span></span>   | <span data-ttu-id="109cb-220">ข้อผิดพลาด (การแม็ปที่ขาดหายไป)</span><span class="sxs-lookup"><span data-stu-id="109cb-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="109cb-221">2</span><span class="sxs-lookup"><span data-stu-id="109cb-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="109cb-222">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-222">MM1</span></span>                       | <span data-ttu-id="109cb-223">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-223">MM1</span></span>                        |
|     <span data-ttu-id="109cb-224">3</span><span class="sxs-lookup"><span data-stu-id="109cb-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="109cb-225">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-225">Error (multiple mappings)</span></span> | <span data-ttu-id="109cb-226">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="109cb-227">4</span><span class="sxs-lookup"><span data-stu-id="109cb-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="109cb-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-228">MM1A</span></span>                      | <span data-ttu-id="109cb-229">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-229">MM1</span></span>                        |
|     <span data-ttu-id="109cb-230">5</span><span class="sxs-lookup"><span data-stu-id="109cb-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="109cb-231">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-231">Error (multiple mappings)</span></span> | <span data-ttu-id="109cb-232">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-232">MM1</span></span>                        |
|     <span data-ttu-id="109cb-233">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="109cb-233">6</span></span>   |     +   | <span data-ttu-id="109cb-234">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-234">default</span></span> |    +    |    +    | <span data-ttu-id="109cb-235">MM2</span><span class="sxs-lookup"><span data-stu-id="109cb-235">MM2</span></span>                       | <span data-ttu-id="109cb-236">MM2</span><span class="sxs-lookup"><span data-stu-id="109cb-236">MM2</span></span>                        |
|     <span data-ttu-id="109cb-237">7</span><span class="sxs-lookup"><span data-stu-id="109cb-237">7</span></span>   |     +   |         | <span data-ttu-id="109cb-238">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-238">default</span></span> |         | <span data-ttu-id="109cb-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-239">MM1A</span></span>                      | <span data-ttu-id="109cb-240">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-240">MM1</span></span>                        |
|     <span data-ttu-id="109cb-241">8</span><span class="sxs-lookup"><span data-stu-id="109cb-241">8</span></span>   |     +   |         | <span data-ttu-id="109cb-242">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-242">default</span></span> |    +    | <span data-ttu-id="109cb-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-243">MM1A</span></span>                      | <span data-ttu-id="109cb-244">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-244">MM1</span></span>                        |
|     <span data-ttu-id="109cb-245">9</span><span class="sxs-lookup"><span data-stu-id="109cb-245">9</span></span>   |     +   |         | <span data-ttu-id="109cb-246">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-246">default</span></span> | <span data-ttu-id="109cb-247">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-247">default</span></span> | <span data-ttu-id="109cb-248">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-248">Error (multiple mappings)</span></span> | <span data-ttu-id="109cb-249">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-249">MM1</span></span>                        |
|    <span data-ttu-id="109cb-250">10</span><span class="sxs-lookup"><span data-stu-id="109cb-250">10</span></span>   | <span data-ttu-id="109cb-251">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-251">default</span></span> |         |         |         | <span data-ttu-id="109cb-252">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-252">MM1</span></span>                       | <span data-ttu-id="109cb-253">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-253">MM1</span></span>                        |
|    <span data-ttu-id="109cb-254">11</span><span class="sxs-lookup"><span data-stu-id="109cb-254">11</span></span>   | <span data-ttu-id="109cb-255">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-255">default</span></span> |    +    |         |         | <span data-ttu-id="109cb-256">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-256">MM1</span></span>                       | <span data-ttu-id="109cb-257">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-257">MM1</span></span>                        |
|    <span data-ttu-id="109cb-258">12</span><span class="sxs-lookup"><span data-stu-id="109cb-258">12</span></span>   | <span data-ttu-id="109cb-259">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-259">default</span></span> |         |    +    |         | <span data-ttu-id="109cb-260">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-260">MM1</span></span>                       | <span data-ttu-id="109cb-261">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-261">MM1</span></span>                        |
|    <span data-ttu-id="109cb-262">13</span><span class="sxs-lookup"><span data-stu-id="109cb-262">13</span></span>   | <span data-ttu-id="109cb-263">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-263">default</span></span> | <span data-ttu-id="109cb-264">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-264">default</span></span> |         |         | <span data-ttu-id="109cb-265">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-265">Error (multiple mappings)</span></span> | <span data-ttu-id="109cb-266">ข้อผิดพลาด (การแม็ปหลายครั้ง)</span><span class="sxs-lookup"><span data-stu-id="109cb-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="109cb-267">14</span><span class="sxs-lookup"><span data-stu-id="109cb-267">14</span></span>   | <span data-ttu-id="109cb-268">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-268">default</span></span> |         | <span data-ttu-id="109cb-269">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-269">default</span></span> |         | <span data-ttu-id="109cb-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-270">MM1A</span></span>                      | <span data-ttu-id="109cb-271">MM1</span><span class="sxs-lookup"><span data-stu-id="109cb-271">MM1</span></span>                        |
|    <span data-ttu-id="109cb-272">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="109cb-272">15</span></span>   | <span data-ttu-id="109cb-273">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-273">default</span></span> |         | <span data-ttu-id="109cb-274">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-274">default</span></span> | <span data-ttu-id="109cb-275">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-275">default</span></span> | <span data-ttu-id="109cb-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-276">MM1A</span></span>                      | <span data-ttu-id="109cb-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="109cb-277">MM2A</span></span>                       |
|    <span data-ttu-id="109cb-278">16</span><span class="sxs-lookup"><span data-stu-id="109cb-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="109cb-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-279">MM1A</span></span>                      | <span data-ttu-id="109cb-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="109cb-280">MM2A</span></span>                       |
|    <span data-ttu-id="109cb-281">17</span><span class="sxs-lookup"><span data-stu-id="109cb-281">17</span></span>   |         |         | <span data-ttu-id="109cb-282">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-282">default</span></span> | <span data-ttu-id="109cb-283">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-283">default</span></span> | <span data-ttu-id="109cb-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="109cb-284">MM1A</span></span>                      | <span data-ttu-id="109cb-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="109cb-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="109cb-286">เรียนรู้ว่ามีการใช้การแม็ปทำอะไรในการดำเนินการของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="109cb-287">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="109cb-288">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="109cb-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="109cb-289">ตั้งค่าตัวเลือก **รันในโหมดดีบัก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="109cb-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="109cb-290">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="109cb-291">รันรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="109cb-291">Run the configured format</span></span>

1.  <span data-ttu-id="109cb-292">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="109cb-293">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="109cb-294">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="109cb-295">ตรวจทานล็อกการดีบัก ER</span><span class="sxs-lookup"><span data-stu-id="109cb-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="109cb-296">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> ล็อกดีบักการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="109cb-297">เลือกปุ่ม **โหลดหน้านี้** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="109cb-297">Select the **Reload this page** button.</span></span>

![หน้าล็อกการรัน ER](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="109cb-299">โปรดสังเกตว่าเรกคอร์ดใหม่ถูกเพิ่มลงในล็อกการดีบัก ER สำหรับรูปแบบ ER ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="109cb-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="109cb-300">เนื่องจากฟิลด์ **ระดับ** ของเรกคอร์ดนี้ถูกตั้งค่าเป็น **ข้อมูล** เรกคอร์ดจะให้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="109cb-301">เนื่องจากฟิลด์ส่วนประกอบรูปแบบถูกตั้งค่าเป็น **การตั้งค่าคอนฟิกการแม็ป** เรกคอร์ดจะแจ้งให้คุณทราบเกี่ยวกับการแม็ปแบบจำลองที่ใช้ในระหว่างการดำเนินการของรูปแบบ ER **รูปแบบเพื่อเรียนรู้การแม็ป** (เลือกไว้ในฟิลด์ **ชื่อการตั้งค่าคอนฟิก**)</span><span class="sxs-lookup"><span data-stu-id="109cb-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="109cb-302">เนื้อหาของฟิลด์ **ข้อความที่สร้างขึ้น** จะแจ้งให้ทราบว่าส่วนประกอบการแม็ป **การแม็ป (FR)** ที่อยู่ในการตั้งค่าคอนฟิก **การแม็ป (FR)** ถูกใช้เพื่อรันรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="109cb-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix1"></a> <span data-ttu-id="109cb-303">ภาคผนวก 1</span><span class="sxs-lookup"><span data-stu-id="109cb-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="109cb-304">ตั้งค่าคอนฟิกแบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-304">Configure a sample data model</span></span>

<span data-ttu-id="109cb-305">ลงชื่อเข้าใช้อินสแตนซ์ RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="109cb-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="109cb-306">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำตามขั้นตอนเหล่านี้ คุณต้องทำขั้นตอนเหล่านี้ในกระบวนการให้เสร็จสมบูรณ์ก่อนเป็นอันดับแรกใน RCS [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่า ใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="109cb-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="109cb-307">สร้างแบบจำลองการจัดโครงแบบข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="109cb-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="109cb-308">บนแดชบอร์ดเริ่มต้น ให้เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="109cb-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="109cb-309">เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="109cb-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="109cb-310">ในหน้า **การตั้งค่าคอนฟิก** เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="109cb-311">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **แบบจำลองในการเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="109cb-312">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="109cb-313">เลือกแท็บด่วน **ส่วนประกอบการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="109cb-314">โปรดสังเกตว่ารุ่นร่างที่ 1 ของการตั้งค่าคอนฟิก ER นี้ พร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="109cb-315">รุ่นนี้มีส่วนประกอบของแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="109cb-316">ออกแบบแบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-316">Design a sample data model</span></span>

1.  <span data-ttu-id="109cb-317">ใน **เพจการตั้งค่าคอนฟิก** เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="109cb-318">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="109cb-318">Select **New**.</span></span>
3.  <span data-ttu-id="109cb-319">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="109cb-320">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="109cb-320">Select **Add**.</span></span>
5.  <span data-ttu-id="109cb-321">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="109cb-321">Select **New**.</span></span>
6.  <span data-ttu-id="109cb-322">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **คำอธิบายฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="109cb-323">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="109cb-323">Select **Add**.</span></span>
8.  <span data-ttu-id="109cb-324">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="109cb-324">Select **New**.</span></span>
9.  <span data-ttu-id="109cb-325">ในกล่องโต้ตอบรายการแบบหล่นลง ในกลุ่มฟิลด์ **โหนดใหม่** เลือก **รากแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="109cb-326">ในฟิลด์ **ชื่อ** ป้อน **จุดเข้าใช้งาน 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="109cb-327">เลือก **จุดเข้าใช้งาน 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="109cb-328">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="109cb-328">Select **Add**.</span></span>
13. <span data-ttu-id="109cb-329">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="109cb-329">Select **New**.</span></span>
14. <span data-ttu-id="109cb-330">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **คำอธิบายฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="109cb-331">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="109cb-331">Select **Add**.</span></span>

    ![เพจตัวออกแบบแบบจำลองข้อมูล ER](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="109cb-333">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-333">Select **Save**.</span></span>
17. <span data-ttu-id="109cb-334">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="109cb-335">ดำเนินการรุ่นที่แก้ไขของการตั้งค่าคอนฟิกแบบจำลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="109cb-336">บนเพจ **การตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="109cb-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="109cb-337">เปลี่ยนสถานะของการตั้งค่าคอนฟิกแบบจำลองที่ออกแบบจาก **ร่าง** เป็น **เสร็จสมบูรณ์** เพื่อให้สามารถใช้เพื่อออกแบบการแม็ปแบบจำลองและรูปแบบที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="109cb-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="109cb-338">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="109cb-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="109cb-339">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-339">Select **OK**.</span></span>

<span data-ttu-id="109cb-340">โปรดสังเกตว่าโครงแบบที่ที่คุณสร้างขึ้นถูกบันทึกเป็นรุ่น 1 เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="109cb-341">ตั้งค่าคอนฟิกการแม็ปแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="109cb-342">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="109cb-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="109cb-343">ในหน้า **การตั้งค่าคอนฟิก** เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="109cb-344">ในกล่องโต้ตอบรายการแบบหล่นลง ในกลุ่มฟิลด์ **สร้าง** ให้เลือก **การแม็ปแบบจำลองที่ขึ้นอยู่กับแบบจำลองข้อมูล แบบจำลองเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="109cb-345">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ป (ทั่วไป)**</span><span class="sxs-lookup"><span data-stu-id="109cb-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="109cb-346">ในฟิลด์ **คำนิยามแบบจำลองข้อมูล**  ให้เลือก **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="109cb-347">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-347">Select **Create configuration**.</span></span>

<span data-ttu-id="109cb-348">โปรดสังเกตว่ารุ่นร่างที่ 1 ของการตั้งค่าคอนฟิก ER นี้ พร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="109cb-349">รุ่นนี้มีส่วนประกอบของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="109cb-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="109cb-350">ออกแบบคอนฟิกการแม็ปแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="109cb-351">ในหน้า **การตั้งค่าคอนฟิก** เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="109cb-352">โปรดสังเกตว่าการแม็ปแบบจำลองของชนิดของทิศทาง **ไปยังแบบจำลอง** ถูกเพิ่มไปยังส่วนประกอบนี้สำหรับคำนิยาม **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="109cb-353">เลือก **ตัวออกแบบ** เพื่อเริ่มต้นการแก้ไขการแม็ปแบบจำลองที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="109cb-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="109cb-354">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="109cb-355">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชันทั่วไป 1"**</span><span class="sxs-lookup"><span data-stu-id="109cb-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="109cb-356">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-356">Select **Save**.</span></span>
6.  <span data-ttu-id="109cb-357">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="109cb-357">Close the **Formula designer** page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="109cb-359">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-359">Select **Save**.</span></span>
8.  <span data-ttu-id="109cb-360">ปิดหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="109cb-361">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="109cb-361">Select **New**.</span></span>
10. <span data-ttu-id="109cb-362">ในฟิลด์ **คำนิยาม**  ให้เลือก **จุดเข้าใช้งาน 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="109cb-363">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ป (ทั่วไป) 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="109cb-364">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-364">Select **Designer**.</span></span>
13. <span data-ttu-id="109cb-365">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="109cb-366">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชันทั่วไป 2"**</span><span class="sxs-lookup"><span data-stu-id="109cb-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="109cb-367">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-367">Select **Save**.</span></span>
16. <span data-ttu-id="109cb-368">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="109cb-368">Close the **Formula designer** page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="109cb-370">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-370">Select **Save**.</span></span>
18. <span data-ttu-id="109cb-371">ปิดหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-371">Close the **Model mapping designer** page.</span></span>

    ![เพจการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="109cb-373">ปิดหน้า **การแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="109cb-374">ดำเนินการรุ่นที่แก้ไขของการตั้งค่าคอนฟิกการแม็ปแบบจำลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="109cb-375">บน **เพจการตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="109cb-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="109cb-376">เปลี่ยนสถานะของการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่ออกแบบจาก **ร่าง** เป็น **เสร็จสมบูรณ์** เพื่อให้สามารถใช้โดยรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="109cb-377">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="109cb-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="109cb-378">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-378">Select **OK**.</span></span>

<span data-ttu-id="109cb-379">โปรดสังเกตว่าโครงแบบที่สร้างขึ้นถูกบันทึกเป็นรุ่น 1 เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="109cb-380">ตั้งค่าคอนฟิกรูปแบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="109cb-381">สร้างการตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="109cb-382">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **แบบจำลองเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="109cb-383">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="109cb-384">ในกล่องโต้ตอบรายการแบบหล่นลง ในกลุ่มฟิลด์ **สร้าง** ให้เลือก **รูปแบบที่ขึ้นอยู่กับแบบจำลองข้อมูล แบบจำลองเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="109cb-385">ในฟิลด์ **ชื่อ** ให้ป้อน **รูปแบบเพื่อเรียนรู้การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="109cb-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="109cb-386">ในฟิลด์ **คำนิยามแบบจำลองข้อมูล**  ให้เลือก **จุดเข้าใช้งาน 1**</span><span class="sxs-lookup"><span data-stu-id="109cb-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="109cb-387">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-387">Select **Create configuration**.</span></span>

<span data-ttu-id="109cb-388">โปรดสังเกตว่ารุ่นร่างที่ 1 ของการตั้งค่าคอนฟิก ER นี้ พร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="109cb-389">เวอร์ชันนี้มีส่วนประกอบของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="109cb-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="109cb-390">ออกแบบรูปแบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-390">Design a sample format</span></span>

1.  <span data-ttu-id="109cb-391">ในหน้า **การตั้งค่าคอนฟิก** เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="109cb-392">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="109cb-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="109cb-393">ในกลุ่ม **ข้อความ** ให้เลือกรายการ **สตริง**</span><span class="sxs-lookup"><span data-stu-id="109cb-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="109cb-394">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="109cb-395">ผูกองค์ประกอบของรูปแบบไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="109cb-396">บนเพจ **ตัวออกแบบรูปแบบ** บนแท็บ **การแม็ป** ให้ขยายแหล่งข้อมูลแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="109cb-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="109cb-397">เลือกฟิลด์ **คำอธิบายฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="109cb-398">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="109cb-398">Select **Bind**.</span></span>

    ![เพจตัวออกแบบรูปแบบ ER](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="109cb-400">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-400">Select **Save**.</span></span>
5.  <span data-ttu-id="109cb-401">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-401">Close the page.</span></span>

## <a name="appendix2"></a> <span data-ttu-id="109cb-402">ภาคผนวก 2</span><span class="sxs-lookup"><span data-stu-id="109cb-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="109cb-403">ตั้งค่าคอนฟิกการแม็ปแบบจำลองตัวอย่างสำหรับการเลือกกำหนดทั่วไป</span><span class="sxs-lookup"><span data-stu-id="109cb-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="109cb-404">คุณอาจต้องการกำหนดค่าการแม็ปแบบจำลองที่ตัวให้บริการการตั้งค่าคอนฟิก (คู่ค้า) กำหนดให้กับคุณ และใช้รุ่นที่กำหนดเองเป็นแหล่งข้อมูลสำหรับรูปแบบ ER ของคุณ</span><span class="sxs-lookup"><span data-stu-id="109cb-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="109cb-405">ในกรณีนี้ คุณต้องสร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER แบบกำหนดเอง เพื่อทำการเปลี่ยนแปลงที่จำเป็น ในการแม็ปแบบจำลองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="109cb-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="109cb-406">ขั้นตอนในภาคผนวกนี้ใช้การแม็ปแบบจำลอง **การแม็ป (ทั่วไป)** เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="109cb-407">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="109cb-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="109cb-408">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ป (ทั่วไป)**</span><span class="sxs-lookup"><span data-stu-id="109cb-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="109cb-409">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="109cb-410">ในกล่องโต้ตอบแบบหล่นลง ในกลุ่มฟิลด์ **ใหม่** ให้เลือก **สืบทอดมาจากชื่อ: การแม็ป (ทั่วไป), Litware, Inc**</span><span class="sxs-lookup"><span data-stu-id="109cb-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="109cb-411">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ป (ทั่วไป) แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="109cb-412">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-412">Select **Create configuration**.</span></span>

<span data-ttu-id="109cb-413">โปรดสังเกตว่ารุ่นร่างที่ 1 ของการตั้งค่าคอนฟิก ER นี้ พร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="109cb-414">ออกแบบคอนฟิกการแม็ปแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="109cb-415">ในหน้า **การตั้งค่าคอนฟิก** เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="109cb-416">โปรดสังเกตว่ามีการคัดลอกการแม็ปแบบจำลองของโครงแบบพื้นฐานไปที่การตั้งค่าคอนฟิกนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="109cb-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="109cb-417">เลือกการแม็ป **สำเนาการแม็ป (ทั่วไป)**</span><span class="sxs-lookup"><span data-stu-id="109cb-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="109cb-418">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="109cb-419">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="109cb-420">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชันทั่วไป 1 แบบกำหนดเอง"**</span><span class="sxs-lookup"><span data-stu-id="109cb-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="109cb-421">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-421">Select **Save**.</span></span>
7.  <span data-ttu-id="109cb-422">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-422">Close the page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="109cb-424">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-424">Select **Save**.</span></span>
9.  <span data-ttu-id="109cb-425">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-425">Close the page.</span></span>
10. <span data-ttu-id="109cb-426">เลือกการแม็ป **สำเนาการแม็ป (ทั่วไป) 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="109cb-427">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-427">Select **Designer**.</span></span>
12. <span data-ttu-id="109cb-428">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="109cb-429">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชันทั่วไป 2 แบบกำหนดเอง"**</span><span class="sxs-lookup"><span data-stu-id="109cb-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="109cb-430">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-430">Select **Save**.</span></span>
15. <span data-ttu-id="109cb-431">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-431">Close the page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="109cb-433">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-433">Select **Save**.</span></span>
17. <span data-ttu-id="109cb-434">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-434">Close the page.</span></span>

    ![เพจการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="109cb-436">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="109cb-437">ดำเนินการรุ่นที่แก้ไขของการตั้งค่าคอนฟิกการแม็ปแบบจำลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="109cb-438">บนเพจ **การตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="109cb-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="109cb-439">เปลี่ยนสถานะของการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่ออกแบบจาก **ร่าง** เป็น **เสร็จสมบูรณ์** เพื่อให้สามารถใช้โดยรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="109cb-440">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="109cb-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="109cb-441">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-441">Select **OK**.</span></span>

<span data-ttu-id="109cb-442">โปรดสังเกตว่าโครงแบบที่สร้างขึ้นถูกบันทึกเป็นรุ่น 1 เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix3"></a> <span data-ttu-id="109cb-443">ภาคผนวก 3</span><span class="sxs-lookup"><span data-stu-id="109cb-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="109cb-444">ตั้งค่าคอนฟิกการแม็ปแบบจำลองตัวอย่างสำหรับการเลือกกำหนดเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="109cb-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="109cb-445">สำหรับรูปแบบ ER บางรูปแบบ อาจมีความต้องการเฉพาะประเทศ/ภูมิภาค สำหรับการจัดเตรียมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="109cb-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="109cb-446">ในกรณีนี้ คุณสามารถจัดการการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER แยกต่างหาก และแยกการใช้งานข้อกำหนดเฉพาะประเทศ/ภูมิภาคเหล่านี้ จากการดำเนินงานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="109cb-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="109cb-447">ขั้นตอนในภาคผนวกนี้ใช้ **รูปแบบเพื่อเรียนรู้การแม็ป** และข้อกำหนดเฉพาะของฝรั่งเศสเป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="109cb-448">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="109cb-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="109cb-449">ขั้นแรก ให้สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ใหม่ เพื่อใช้ข้อกำหนดเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="109cb-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="109cb-450">ใช้การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER แบบกำหนดเองของคุณเป็นฐาน</span><span class="sxs-lookup"><span data-stu-id="109cb-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="109cb-451">บนเพจ **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ป (ทั่วไป) แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="109cb-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="109cb-452">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="109cb-453">ในกล่องโต้ตอบแบบหล่นลง ในกลุ่มฟิลด์ **ใหม่** ให้เลือก **สืบทอดมาจากชื่อ: การแม็ป (ทั่วไป) แบบกำหนดเอง, Litware, Inc**</span><span class="sxs-lookup"><span data-stu-id="109cb-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="109cb-454">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ป (FR)**</span><span class="sxs-lookup"><span data-stu-id="109cb-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="109cb-455">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="109cb-455">Select **Create configuration**.</span></span>

<span data-ttu-id="109cb-456">โปรดสังเกตว่ารุ่นร่างที่ 1 ของการตั้งค่าคอนฟิก ER นี้ พร้อมสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="109cb-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="109cb-457">ออกแบบคอนฟิกการแม็ปแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="109cb-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="109cb-458">ในหน้า **การตั้งค่าคอนฟิก** เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="109cb-459">โปรดสังเกตว่ามีการคัดลอกการแม็ปแบบจำลองของโครงแบบพื้นฐานไปที่การตั้งค่าคอนฟิกนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="109cb-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="109cb-460">เลือกการแม็ป **สำเนาของสำเนาการแม็ป (ทั่วไป)**</span><span class="sxs-lookup"><span data-stu-id="109cb-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="109cb-461">เปลี่ยนชื่อ**การแม็ป (FR)**</span><span class="sxs-lookup"><span data-stu-id="109cb-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="109cb-462">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="109cb-463">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="109cb-464">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชัน FR 1"**</span><span class="sxs-lookup"><span data-stu-id="109cb-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="109cb-465">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-465">Select **Save**.</span></span>
8.  <span data-ttu-id="109cb-466">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-466">Close the page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="109cb-468">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-468">Select **Save**.</span></span>
10. <span data-ttu-id="109cb-469">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-469">Close the page.</span></span>
11. <span data-ttu-id="109cb-470">เลือกการแม็ป **สำเนาของสำเนาการแม็ป (ทั่วไป) 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="109cb-471">เปลี่ยนชื่อ**การแม็ป (FR) 2**</span><span class="sxs-lookup"><span data-stu-id="109cb-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="109cb-472">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="109cb-472">Select **Designer**.</span></span>
14. <span data-ttu-id="109cb-473">ในส่วน **แบบจำลองข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="109cb-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="109cb-474">ในฟิลด์ **สูตร** ให้ป้อน **"ฟังก์ชัน FR 2"**</span><span class="sxs-lookup"><span data-stu-id="109cb-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="109cb-475">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-475">Select **Save**.</span></span>
17. <span data-ttu-id="109cb-476">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-476">Close the page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="109cb-478">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-478">Select **Save**.</span></span>
19. <span data-ttu-id="109cb-479">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-479">Close the page.</span></span>

    ![เพจการแม็ปแบบจำลอง ER](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="109cb-481">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="109cb-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="109cb-482">ระบุข้อจำกัดบริบทของประเทศ/ภูมิภาคสำหรับการใช้</span><span class="sxs-lookup"><span data-stu-id="109cb-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="109cb-483">บนหน้า **การตั้งค่าคอนฟิก** บนแท็บด่วน **รหัสประเทศ/ภูมิภาค ISO** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="109cb-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="109cb-484">ในฟิลด์ **ISO** เลือก **FR**</span><span class="sxs-lookup"><span data-stu-id="109cb-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="109cb-485">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="109cb-485">Select **Save**.</span></span>

<span data-ttu-id="109cb-486">โปรดทราบว่าคุณต้องลงชื่อเข้าใช้สู่บริษัทหนึ่งๆ ใน Finance เพื่อรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="109cb-487">ดังนั้น บริษัทนี้อาจถือเป็นฝ่ายที่ควบคุมทั้งการดำเนินการของรูปแบบ ER และการเลือกของการแม็ปแบบจำลอง ER ที่ถูกต้องของแบบจำลองข้อมูล ER พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="109cb-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="109cb-488">โดยการเพิ่มรหัสประเทศ **FR** คุณระบุว่าการแม็ปแบบจำลองนี้พร้อมใช้งานสำหรับการเลือกโดยรูปแบบ FR ของแบบจำลองข้อมูลพื้นฐานเฉพาะเมื่อมีการรันรูปแบบนั้นภายใต้การควบคุมของบริษัทที่มีบริบทประเทศ/ภูมิภาคของฝรั่งเศสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="109cb-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="109cb-489">คุณสามารถเพิ่มรหัสประเทศ/ภูมิภาคหลายรหัส สำหรับรุ่นเดี่ยวของการตั้งค่าคอนฟิกการแม็ปแบบจำลอง FR</span><span class="sxs-lookup"><span data-stu-id="109cb-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="109cb-490">ด้วยวิธีนี้ การแม็ปแบบจำลองที่อยู่ในการตั้งค่าคอนฟิกการแม็ปแบบจำลองดังกล่าวสามารถใช้สำหรับรูปแบบ ER ซึ่งรันภายใต้การควบคุมของบริษัทที่มีบริบทประเทศ/ภูมิภาคที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="109cb-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="109cb-491">โปรดทราบว่ามีการระบุรายการประเทศ/ภูมิภาคสำหรับแต่ละรุ่นของการตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER และอาจแตกต่างจากรุ่นเป็นรุ่น</span><span class="sxs-lookup"><span data-stu-id="109cb-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="109cb-492">ดำเนินการรุ่นที่แก้ไขของการตั้งค่าคอนฟิกการแม็ปแบบจำลองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="109cb-493">บนเพจ **การตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="109cb-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="109cb-494">เปลี่ยนสถานะของการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่ออกแบบจาก **ร่าง** เป็น **เสร็จสมบูรณ์** เพื่อให้สามารถใช้โดยรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="109cb-495">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="109cb-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="109cb-496">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="109cb-496">Select **OK**.</span></span>

<span data-ttu-id="109cb-497">โปรดสังเกตว่าโครงแบบที่สร้างขึ้นถูกบันทึกเป็นรุ่น 1 เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="109cb-498">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="109cb-498">Additional resources</span></span>

[<span data-ttu-id="109cb-499">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="109cb-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="109cb-500">จัดการการแมปแบบจำลอง ER ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="109cb-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="109cb-501">ใช้บริบทประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="109cb-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="109cb-502">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="109cb-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="109cb-503">ฉันได้ตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่ใช้ร่วมกันสองครั้งใน RCS และทำเครื่องหมายเป็นการตั้งค่าคอนฟิกการแม็ปแบบจำลองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="109cb-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="109cb-504">ฉันรันรูปแบบ ER เสร็จเรียบร้อยแล้ว ซึ่งถูกสร้างขึ้นสำหรับการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER พื้นฐานเดียวกัน เพื่อทดสอบการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="109cb-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="109cb-505">จากนั้น ฉันนำเข้าโซลูชัน ER ทั้งหมด (แบบจำลองข้อมูล ER การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER สองการตั้งค่า และการตั้งค่าคอนฟิกรูปแบบ ER ) ลงใน Finance</span><span class="sxs-lookup"><span data-stu-id="109cb-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="109cb-506">เพราะเหตุใดฉันจึงได้รับข้อความแสดงข้อผิดพลาดเมื่อพยายามรันรูปแบบ ER เดียวกันใน Finance</span><span class="sxs-lookup"><span data-stu-id="109cb-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="109cb-507">การตั้งค่าการแม็ปรูปแบบจำลองเริ่มต้นเป็นสภาพแวดล้อมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="109cb-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="109cb-508">คือการตั้งค่าคอนฟิกไว้ใน RCS แต่ยังไม่ได้ส่งออกไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="109cb-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="109cb-509">เมื่อต้องการรันการจัดรูปแบบ ER นี้เสร็จเรียบร้อย คุณต้องทำเครื่องหมายการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER เป็นการตั้งค่าคอนฟิกการแม็ปแบบจำลองเริ่มต้นใน Finance เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="109cb-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="109cb-510">ฉันได้ตั้งค่าคอนฟิกการแม็ปแบบจำลองหนึ่งเป็นการแม็ปแบบจำลองที่ใช้ร่วมกัน และทำให้รุ่นแบบร่างเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="109cb-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="109cb-511">ฉันเพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองใหม่สำหรับแบบจำลองข้อมูลเดียวกัน และตั้งค่าคอนฟิกเป็นเฉพาะภาษาฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="109cb-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="109cb-512">เหตุใดจึงเป็นการแม็ปแบบจำลองที่ใช้ร่วมกันที่เลือกเมื่อฉันรันรูปแบบ ER ถึงแม้ว่ารูปแบบ ER นี้ใช้คำนิยามราก และการดำเนินการที่ถูกต้องอยู่ภายใต้การควบคุมของบริษัทที่มีบริบทประเทศ/ภูมิภาคของฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="109cb-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="109cb-513">ตรวจสอบให้แน่ใจว่าไม่ได้ทำเครื่องหมายการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่ใช้ร่วมกันเป็นการตั้งค่าคอนฟิกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="109cb-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="109cb-514">มิฉะนั้น จะมีระดับความสำคัญสูงกว่าในระหว่างการเลือกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="109cb-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="109cb-515">นอกจากนี้ ตรวจสอบให้แน่ใจว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองเฉพาะภาษาฝรั่งเศสได้รับการพิจารณา เมื่อการแม็ปถูกเลือกระหว่างการดำเนินการรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="109cb-516">การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER พร้อมใช้งานสำหรับการเลือกเมื่อตรงตามเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="109cb-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="109cb-517">อย่างน้อยหนึ่งรุ่นของการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER มีสถานะ **เสร็จสมบูรณ์** หรือ **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="109cb-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="109cb-518">ในกรณีนี้ รุ่นที่มีหมายเลขรุ่นสูงสุดจะใช้สำหรับการดำเนินการจัดรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="109cb-519">ตัวเลือก **รันฉบับร่าง** สำหรับการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="109cb-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="109cb-520">ในกรณีนี้ รุ่นที่มีสถานะ **ร่าง** จะใช้สำหรับการดำเนินการจัดรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="109cb-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="109cb-521">ตัวเลือก **รันฉบับร่าง** กลายเป็นพร้อมใช้งานบนเพจ **การตั้งค่าคอนฟิก** สำหรับแต่ละการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER เมื่อพารามิเตอร์ผู้ใช้ ER **การตั้งค่าการรัน** เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="109cb-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>
