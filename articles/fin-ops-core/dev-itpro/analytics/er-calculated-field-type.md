---
title: สนับสนุนการเรียกแบบพารามิเตอร์ ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่คำนวณได้
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการใช้ชนิดฟิลด์ที่คำนวณได้สำหรับแหล่งข้อมูล ER
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 02d53f4326d8f31abf6ec7404575728837954bef
ms.sourcegitcommit: c9baf9a3b4552f0317b5ec87d252834f52df1b98
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665621"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="cb825-103">สนับสนุนการเรียกแบบพารามิเตอร์ ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="cb825-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb825-104">หัวข้อนี้จะอธิบายวิธีการออกแบบแหล่งข้อมูลของการรายงานทางอิเล็กทรอนิกส์ (ER) โดยใช้ชนิด **ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="cb825-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="cb825-105">แหล่งข้อมูลนี้อาจประกอบด้วยนิพจน์ ER ที่ซึ่งเมื่อดำเนินการ สามารถควบคุมโดยค่าของอาร์กิวเมนต์พารามิเตอร์ที่ได้รับการตั้งค่าคอนฟิกในการผูกที่เรียกแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="cb825-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="cb825-106">โดยการตั้งค่าคอนฟิกการเรียกแบบพารามิเตอร์ของแหล่งข้อมูลดังกล่าว คุณสามารถนำแหล่งข้อมูลหนึ่งมาใช้ใหม่ในการผูกหลายจำนวน ซึ่งจะลดจำนวนแหล่งข้อมูลทั้งหมดที่ต้องมีการตั้งค่าคอนฟิกในการแม็ปแบบจำลอง ER หรือรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="cb825-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="cb825-107">นอกจากนี้ยังช่วยให้คอมโพเนนต์ ER ที่ตั้งค่าคอนฟิก ช่วยลดต้นทุนการบำรุงรักษา และต้นทุนการใช้งานของผู้บริโภครายอื่นๆได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="cb825-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cb825-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="cb825-108">Prerequisites</span></span>
<span data-ttu-id="cb825-109">เพื่อทำตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องมีการเข้าถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="cb825-110">การเข้าถึงบทบาทอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="cb825-111">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cb825-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="cb825-112">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cb825-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cb825-113">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-113">System administrator</span></span>

- <span data-ttu-id="cb825-114">การเข้าถึง Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance and Operations สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="cb825-115">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cb825-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="cb825-116">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cb825-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cb825-117">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-117">System administrator</span></span>

<span data-ttu-id="cb825-118">นอกจากนี้ คุณต้องดาวน์โหลดและจัดเก็บไฟล์ต่อไปนี้โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cb825-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="cb825-119">**เนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="cb825-119">**Content**</span></span>                           | <span data-ttu-id="cb825-120">**ชื่อไฟล์**</span><span class="sxs-lookup"><span data-stu-id="cb825-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb825-121">การตั้งค่าคอนฟิกรูปแบบข้อมูล ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb825-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="cb825-122">แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="cb825-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="cb825-123">การตั้งค่าคอนฟิกข้อมูลเมตา ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb825-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="cb825-124">ข้อมูลเมตาเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="cb825-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="cb825-125">การตั้งค่าคอนฟิกการแม็ปรูปแบบข้อมูล ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb825-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="cb825-126">การแม็ปเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="cb825-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="cb825-127">การตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb825-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="cb825-128">รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="cb825-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="cb825-129">ลงชื่อเข้าใช้อินสแตนซ์ RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cb825-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="cb825-130">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. คุณต้องทำขั้นตอนเหล่านี้ในกระบวนการ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่า ใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์ก่อนเป็นอันดับแรก ใน RCS</span><span class="sxs-lookup"><span data-stu-id="cb825-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="cb825-131">บนแดชบอร์ดเริ่มต้น ให้เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cb825-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="cb825-132">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="cb825-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="cb825-133">นำเข้าการตั้งค่าคอนฟิกที่ดาวน์โหลดไปยัง RCS ในลำดับต่อไปนี้: รูปแบบข้อมูล, ข้อมูลเมตา, การแม็ปรูปแบบ, รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="cb825-134">ดำเนินการขั้นตอนต่อไปนี้ให้สำเร็จ สำหรับแต่ละการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="cb825-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="cb825-135">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="cb825-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="cb825-136">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="cb825-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="cb825-137">เลือก **เรียกดู** จากนั้นเลือกการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="cb825-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="cb825-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="cb825-139">ตรวจทานโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cb825-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="cb825-140">ตรวจทานการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-140">Review model mapping</span></span>

1. <span data-ttu-id="cb825-141">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="cb825-142">เลือก **การแม็ปเพื่อเรียนรู้การเรียบแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="cb825-143">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-143">Select **Designer**.</span></span>
4. <span data-ttu-id="cb825-144">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="cb825-145">การแม็ปรูปแบบ ER นี้ ได้รับการออกแบบมาให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="cb825-146">ดึงข้อมูลรายการรหัสภาษี (แหล่งข้อมูล **ภาษี**) ที่อยู่ในตาราง **TaxTable**</span><span class="sxs-lookup"><span data-stu-id="cb825-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="cb825-147">ดึงข้อมูลรายการธุรกรรมภาษี (แหล่งข้อมูล **ธุรกรรม**) ที่อยู่ในตาราง **TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="cb825-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="cb825-148">จัดกลุ่มรายการของธุรกรรมที่นำมาใช้ (แหล่งข้อมูล **Gr**) โดยรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="cb825-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="cb825-149">คำนวณสำหรับการจัดกลุ่มธุรกรรมตามมูลค่ารวมสำหรับแต่ละรหัสภาษี:</span><span class="sxs-lookup"><span data-stu-id="cb825-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="cb825-150">ผลรวมของมูลค่าฐานภาษี</span><span class="sxs-lookup"><span data-stu-id="cb825-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="cb825-151">ผลรวมของมูลค่าภาษี</span><span class="sxs-lookup"><span data-stu-id="cb825-151">Sum of tax values.</span></span>
            - <span data-ttu-id="cb825-152">มูลค่าต่ำสุดของอัตราภาษีที่ใช้</span><span class="sxs-lookup"><span data-stu-id="cb825-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="cb825-153">การแม็ปรูปแบบในการตั้งค่าคอนฟิกนี้จะใช้รูปแบบข้อมูลพื้นฐาน สำหรับรูปแบบ ER ใดๆ ที่สร้างขึ้นสำหรับรูปแบบนี้ และดำเนินการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb825-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="cb825-154">ดังนั้นจึงมีการเปิดเผยเนื้อหาของแหล่งข้อมูล **ภาษี** และ **Gr** สำหรับรูปแบบ ER เช่น แหล่งข้อมูลที่เป็นนามธรรม</span><span class="sxs-lookup"><span data-stu-id="cb825-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![หน้าตัวออกแบบการแม็ปรูปแบบแสดงแหล่งข้อมูลของข้อมูลภาษี และ Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="cb825-156">ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="cb825-157">ปิดหน้า **การแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="cb825-158">ตรวจทานรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-158">Review format</span></span>

1. <span data-ttu-id="cb825-159">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="cb825-160">เลือก **รูปแบบเพื่อเรียนรู้การเรียบแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="cb825-161">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-161">Select **Designer**.</span></span> <span data-ttu-id="cb825-162">รูปแบบ ER นี้ ได้รับการออกแบบมาให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="cb825-163">สร้างรายงานภาษี ในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="cb825-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="cb825-164">แสดงระดับของภาษีต่อไปนี้ ในรายงานภาษี: ปกติ, ลดลง และ ไม่มี</span><span class="sxs-lookup"><span data-stu-id="cb825-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="cb825-165">แสดงรายละเอียดหลายรายการในแต่ละระดับภาษี ที่มีรายละเอียดที่แตกต่างกันในแต่ละระดับ</span><span class="sxs-lookup"><span data-stu-id="cb825-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![หน้าตัวออกแบบรูปแบบ](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="cb825-167">เลือก **การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="cb825-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="cb825-168">ขยายรายการ **รูปแบบ** **ข้อมูล** และ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="cb825-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="cb825-169">ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ประกอบด้วยนิพจน์ที่ส่งคืนรหัสของระดับภาษี (**ปกติ** **ลดลง** **ไม่มี** หรือ **อื่นๆ**) เป็นค่าข้อความสำหรับรหัสภาษีใดๆ ที่สามารถดึงข้อมูลมาจากแหล่งข้อมูล **Model.Data.Summary** ในเวลารัน</span><span class="sxs-lookup"><span data-stu-id="cb825-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![หน้าตัวออกแบบรูปแบบที่แสดงรายละเอียดของรูปแบบข้อมูลเพื่อเรียนรู้การเรียกแบบพารามิเตอร์](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="cb825-171">ขยายรายการ **Model**.**Data2**</span><span class="sxs-lookup"><span data-stu-id="cb825-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="cb825-172">ขยายรายการ **Model**.**Data2.Summary2**</span><span class="sxs-lookup"><span data-stu-id="cb825-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="cb825-173">แหล่งข้อมูล **Model**.**Data2.Summary2** ถูกตั้งค่าคอนฟิกให้จัดกลุ่มรายละเอียดธุรกรรมแหล่งข้อมูล **Model.Data.Summary** ตามระดับภาษี (ส่งคืนโดยฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level**) และคำนวณการรวม</span><span class="sxs-lookup"><span data-stu-id="cb825-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![หน้าตัวออกแบบรูปแบบที่แสดงรายละเอียดของแหล่งข้อมูล Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="cb825-175">ตรวจทานฟิลด์ที่คำนวณได้ **Model**.**Data2 Level1**, **Model**.**Data2 Level2** และ **Model**.**Data2 Level3**</span><span class="sxs-lookup"><span data-stu-id="cb825-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="cb825-176">ฟิลด์ที่คำนวณได้เหล่านี้จะใช้ในการกรองรายการเรกคอร์ด **Model**.**Data2 Summary2** และส่งคืนเฉพาะเรกคอร์ดที่แสดงถึงระดับภาษีเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cb825-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="cb825-177">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="cb825-178">สร้างรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="cb825-178">Create a derived format</span></span>
<span data-ttu-id="cb825-179">คุณสามารถปรับปรุงรูปแบบที่ระบุได้โดยการเพิ่มฟิลด์ที่คำนวณได้หนึ่งฟิลด์ เพื่อกรองระดับภาษีที่จำเป็นแทนการใช้ฟิลด์สามฟิลด์ที่มีอยู่: **Model**.**Data2 Level1**, **Model**.**Data2 Level2** และ **Model**.**Data2 Level3**</span><span class="sxs-lookup"><span data-stu-id="cb825-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="cb825-180">สามารถระบุระดับภาษีที่จำเป็น ในสถานที่ที่ฟิลด์ที่คำนวณได้ใหม่จะถูกเรียก</span><span class="sxs-lookup"><span data-stu-id="cb825-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="cb825-181">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="cb825-182">เลือก **รูปแบบเพื่อเรียนรู้การเรียบแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="cb825-183">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="cb825-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="cb825-184">เลือก **ได้รับมาจากชื่อ: รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์, Microsoft**</span><span class="sxs-lookup"><span data-stu-id="cb825-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="cb825-185">ในฟิลด์ **ชื่อ** ป้อน **รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์ (กำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="cb825-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="cb825-186">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="cb825-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="cb825-187">ตั้งค่าคอนฟิกฟิลด์ที่คำนวณแบบพารามิเตอร์ ซึ่งส่งคืนรายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="cb825-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="cb825-188">เริ่มต้นการเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="cb825-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="cb825-189">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-189">Select **Designer**.</span></span>
2. <span data-ttu-id="cb825-190">เลือก **ขยาย/ยุบ** เพื่อขยายรายการรูปแบบทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cb825-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="cb825-191">เลือก **การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="cb825-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="cb825-192">ขยายรายการ **Model**</span><span class="sxs-lookup"><span data-stu-id="cb825-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="cb825-193">เลือกรายการ **Model.Data2**</span><span class="sxs-lookup"><span data-stu-id="cb825-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="cb825-194">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cb825-194">Select **Add**.</span></span>
7. <span data-ttu-id="cb825-195">เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="cb825-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="cb825-196">ในฟิลด์ **ชื่อ** ให้ป้อน **เงินสด**</span><span class="sxs-lookup"><span data-stu-id="cb825-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="cb825-197">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="cb825-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="cb825-198">กำหนดพารามิเตอร์สำหรับการเพิ่มฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="cb825-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="cb825-199">เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="cb825-200">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cb825-200">Select **New**.</span></span>
3. <span data-ttu-id="cb825-201">ในฟิลด์ **ชื่อ** ป้อน **ระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="cb825-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="cb825-202">ในฟิลด์ **ชนิด** เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="cb825-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="cb825-203">ชนิดข้อมูลพื้นฐานเท่านั้นที่สามารถใช้ในการระบุชนิดของอาร์กิวเมนต์ของพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="cb825-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="cb825-204">ดังนั้น ชนิด **รายการเรกคอร์ด** **เรกคอร์ด** และ **Enum** จึงไม่สามารถใช้สำหรับวัตถุประสงค์นี้ได้</span><span class="sxs-lookup"><span data-stu-id="cb825-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="cb825-205">จำนวนสูงสุดของพารามิเตอร์ที่สามารถระบุสำหรับฟิลด์ที่คำนวณได้เพียงครั้งเดียว คือ 8</span><span class="sxs-lookup"><span data-stu-id="cb825-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![รายการแหล่งข้อมูลพารามิเตอร์](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="cb825-207">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-207">Select **OK**.</span></span>

<span data-ttu-id="cb825-208">โดยการเพิ่มพารามิเตอร์นี้ คุณระบุเงื่อนไขที่ต้องอยู่ในสถานที่ที่จะเรียกฟิลด์ที่คำนวณได้นี้</span><span class="sxs-lookup"><span data-stu-id="cb825-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="cb825-209">เมื่อคุณเรียกฟิลด์ที่คำนวณได้นี้ คุณต้องระบุอาร์กิวเมนต์ของพารามิเตอร์ **ระดับภาษี** เป็นค่าที่มีรูปแบบ **สตริง**</span><span class="sxs-lookup"><span data-stu-id="cb825-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="cb825-210">ตรวจสอบให้แน่ใจว่าคุณได้กำหนดพารามิเตอร์เฉพาะสำหรับฟิลด์ที่คำนวณได้ที่มีอยู่ในคอนเทนเนอร์ (**รายการเรกคอร์ด** **เรกคอร์ด** หรือ **คอนเทนเนอร์** อย่างใดอย่างหนึ่งเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="cb825-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="cb825-211">พารามิเตอร์ที่ตั้งค่าคอนฟิกจะพร้อมใช้งานในรายการของแหล่งข้อมูลสำหรับฟิลด์ที่คำนวณได้นี้</span><span class="sxs-lookup"><span data-stu-id="cb825-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="cb825-212">คุณสามารถเพิ่มพารามิเตอร์ให้กับนิพจน์ที่ตั้งค่าคอนฟิก โดยการเลือก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cb825-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![ฟิลด์แหล่งข้อมูล](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="cb825-214">กำหนดนิพจน์สำหรับการเพิ่มฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="cb825-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="cb825-215">ในฟิลด์ **สูตร** ป้อน:</span><span class="sxs-lookup"><span data-stu-id="cb825-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="cb825-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="cb825-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="cb825-217">เลือกพารามิเตอร์ **ระดับภาษี** ในรายการของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cb825-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="cb825-218">เลือก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cb825-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="cb825-219">ในฟิลด์ **สูตร** ดำเนินการนิพจน์ขั้นสุดท้ายดังนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="cb825-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="cb825-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="cb825-221">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cb825-221">Select **Save**.</span></span>

    ![ข้อมูลของฟิลด์แหล่งข้อมูล](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="cb825-223">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="cb825-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="cb825-224">เสร็จสิ้นการเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="cb825-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="cb825-225">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-225">Select **OK**.</span></span>

<span data-ttu-id="cb825-226">บนหน้า **ตัวออกแบบรูปแบบ** ฟิลด์ที่คำนวณได้ของพารามิเตอร์การตั้งค่าคอนฟิก **ระดับ** ต้องมีอาร์กิวเมนต์ **สตริง**</span><span class="sxs-lookup"><span data-stu-id="cb825-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![รายการที่ขยายของระดับฟิลด์ที่คำนวณได้](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="cb825-228">ใช้ฟิลด์ที่คำนวณได้ที่ตั้งค่าคอนฟิกสำหรับองค์ประกอบรูปแบบการผูก</span><span class="sxs-lookup"><span data-stu-id="cb825-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="cb825-229">เลือก **Model.Data2.Levels** เพื่อเลือกฟิลด์ที่คำนวณได้ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cb825-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="cb825-230">เลือกองค์ประกอบรูปแบบ **Statement.Taxation.Regular**</span><span class="sxs-lookup"><span data-stu-id="cb825-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="cb825-231">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="cb825-231">Select **Bind**.</span></span>
4. <span data-ttu-id="cb825-232">เลือก **ใช่** เพื่อยืนยันการแทนที่ของแหล่งข้อมูลที่ใช้อยู่ในปัจจุบัน **Level1** โดยแหล่งข้อมูลใหม่ **Levels** ในองค์ประกอบรูปแบบซ้อนกันทั้งหมดขององค์ประกอบรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb825-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="cb825-233">การผูกที่นำไปใช้ถูกสร้างขึ้นเป็นการเรียกของฟิลด์ที่คำนวณได้แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="cb825-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="cb825-234">โดยค่าเริ่มต้น ชื่อขององค์ประกอบรูปแบบที่ผูกไว้ถูกใช้เป็นอาร์กิวเมนต์สำหรับฟิลด์ที่คำนวณได้แบบพารามิเตอร์ ภายใต้เงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="cb825-235">ฟิลด์ที่คำนวณได้มีที่การตั้งค่าคอนฟิกให้ใช้พารามิเตอร์เดียว</span><span class="sxs-lookup"><span data-stu-id="cb825-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="cb825-236">ชนิดข้อมูลของพารามิเตอร์นี้ ถูกกำหนดเป็น **สตริง**</span><span class="sxs-lookup"><span data-stu-id="cb825-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="cb825-237">เมื่อชื่อขององค์ประกอบรูปแบบที่ผูกไว้ว่างเปล่า ชื่อแหล่งข้อมูลขององค์ประกอบนี้จะถูกใช้ในการผูกที่นำไปใช้</span><span class="sxs-lookup"><span data-stu-id="cb825-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="cb825-238">เลือกองค์ประกอบรูปแบบ **Statement.Taxation.Reduced**</span><span class="sxs-lookup"><span data-stu-id="cb825-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="cb825-239">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="cb825-239">Select **Bind**.</span></span>
7. <span data-ttu-id="cb825-240">เลือก **ใช่** เพื่อยืนยันการแทนที่ของแหล่งข้อมูลที่ใช้อยู่ในปัจจุบัน **Level2** โดยแหล่งข้อมูลใหม่ **Levels** ในองค์ประกอบรูปแบบซ้อนกันทั้งหมดภายใต้องค์ประกอบรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb825-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="cb825-241">เลือกองค์ประกอบรูปแบบ **Statement.Taxation.None**</span><span class="sxs-lookup"><span data-stu-id="cb825-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="cb825-242">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="cb825-242">Select **Bind**.</span></span>
10. <span data-ttu-id="cb825-243">เลือก **ใช่** เพื่อยืนยันการแทนที่ของแหล่งข้อมูลที่ใช้อยู่ในปัจจุบัน **Level3** โดยแหล่งข้อมูลใหม่ **Levels** ในองค์ประกอบรูปแบบซ้อนกันทั้งหมดภายใต้องค์ประกอบรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb825-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="cb825-244">เมื่อคุณระบุอาร์กิวเมนต์ของฟิลด์ที่คำนวณได้แบบพารามิเตอร์สำหรับองค์ประกอบ XML ซึ่งแสดงถึงระดับภาษี (ตัวอย่าง เช่น **Model.Data2.Levels("ลดลง")** เป็นค่าข้อความ) คุณไม่จำเป็นต้องทำแบบเดียวกันสำหรับแอททริบิวต์ XML ที่ซ้อนกัน— การผูกจะสืบทอดค่าของอาร์กิวเมนต์ที่กำหนดไว้ในระดับหลัก (**Model.Data2.Levels.aggregated.Base** ไม่ใช่ **Model.Data2.Levels("Reduced").aggregated.Base**) โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cb825-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="cb825-245">ไม่สนับสนุนการเรียกซ้ำของฟิลด์ที่คำนวณได้แบบพารามิเตอร์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="cb825-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="cb825-246">คุณสามารถเลือก **แก้ไขสูตร** และเปลี่ยนอาร์กิวเมนต์ที่ใช้เป็นค่าเริ่มต้นของฟิลด์ที่คำนวณได้แบบพารามิเตอร์ ในการผูกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb825-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="cb825-247">ถ้าอาร์กิวเมนต์นี้หายไป อาจทำให้เกิดข้อผิดพลาดในเวลาที่ใช้—ผู้ใช้จะได้รับการแจ้งเกี่ยวกับสถานการณ์ดังกล่าว เมื่อรูปแบบปัจจุบันได้มีการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="cb825-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![การแจ้งเตือนการเตือนการตรวจสอบความถูกต้อง](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="cb825-249">ตั้งค่าคอนฟิกฟิลด์ที่คำนวณได้แบบพารามิเตอร์ เพื่อส่งคืนเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="cb825-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="cb825-250">เมื่อฟิลด์ที่คำนวณได้แบบพารามิเตอร์ส่งคืนเรกคอร์ด คุณต้องสนับสนุนการผูกฟิลด์แต่ละฟิลด์ของเรกคอร์ดนี้ เพื่อจัดรูปแบบองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cb825-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="cb825-251">ในกรณีดังกล่าว จะไม่มีการผูกหลักที่มีค่าของอาร์กิวเมนต์ในการเรียกฟิลด์ที่คำนวณได้แบบพารามิเตอร์ ซึ่งต้องมีการกำหนดค่านี้ในการผูกฟิลด์ของเรกคอร์ดเดียว</span><span class="sxs-lookup"><span data-stu-id="cb825-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="cb825-252">เริ่มต้นการเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="cb825-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="cb825-253">เลือกรายการ **Model.Data2**</span><span class="sxs-lookup"><span data-stu-id="cb825-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="cb825-254">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cb825-254">Select **Add**.</span></span>
3. <span data-ttu-id="cb825-255">เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="cb825-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="cb825-256">ในฟิลด์ **ชื่อ** ให้ป้อน **LevelRecord**</span><span class="sxs-lookup"><span data-stu-id="cb825-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="cb825-257">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="cb825-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="cb825-258">กำหนดพารามิเตอร์สำหรับการเพิ่มฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="cb825-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="cb825-259">เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="cb825-260">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cb825-260">Select **New**.</span></span>
3. <span data-ttu-id="cb825-261">ในฟิลด์ **ชื่อ** ป้อน **ระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="cb825-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="cb825-262">ในฟิลด์ **ชนิด** เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="cb825-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="cb825-263">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="cb825-264">กำหนดนิพจน์สำหรับการเพิ่มฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="cb825-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="cb825-265">ในฟิลด์ **สูตร** ป้อนดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="cb825-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="cb825-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="cb825-267">เลือกพารามิเตอร์ **ระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="cb825-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="cb825-268">เลือก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cb825-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="cb825-269">ในฟิลด์ **สูตร** ผนวก **'ระดับภาษี'))** กับสิ่งที่คุณป้อนไว้ในขั้นตอนที่ 1 เพื่อจบนิพจน์ให้กับ:</span><span class="sxs-lookup"><span data-stu-id="cb825-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="cb825-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="cb825-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="cb825-271">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cb825-271">Select **Save**.</span></span>
6. <span data-ttu-id="cb825-272">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="cb825-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="cb825-273">เสร็จสิ้นการเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="cb825-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="cb825-274">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="cb825-275">ใช้ฟิลด์ที่คำนวณได้ที่ตั้งค่าคอนฟิกเพื่อผูกองค์ประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="cb825-276">ขยาย **Model.Data2.LevelRecord** เพื่อเลือกฟิลด์ที่คำนวณได้ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cb825-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="cb825-277">ขยายคอนเทนเนอร์ **Model.Data2.LevelRecord.aggregated** บองฟิลด์ที่คำนวณได้ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cb825-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="cb825-278">เลือกฟิลด์ **Model.Data2.LevelRecord.aggregated.Base**</span><span class="sxs-lookup"><span data-stu-id="cb825-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="cb825-279">เลือกองค์ประกอบรูปแบบ **Statement.Taxation.None**</span><span class="sxs-lookup"><span data-stu-id="cb825-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="cb825-280">เลือก **ยกเลิกการผูก**</span><span class="sxs-lookup"><span data-stu-id="cb825-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="cb825-281">เลือกองค์ประกอบรูปแบบ **Statement.Taxation.None.Base**</span><span class="sxs-lookup"><span data-stu-id="cb825-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="cb825-282">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="cb825-282">Select **Bind**.</span></span>
8. <span data-ttu-id="cb825-283">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="cb825-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="cb825-284">เปลี่ยนนิพจน์เป็น **Model.Data2.LevelRecord("None").aggregated.Base**</span><span class="sxs-lookup"><span data-stu-id="cb825-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![นิพจน์ที่อัพเดตแล้ว](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="cb825-286">ลบฟิลด์ที่คำนวณได้ที่ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="cb825-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="cb825-287">เลือก **Model.Data2.Level1**</span><span class="sxs-lookup"><span data-stu-id="cb825-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="cb825-288">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-288">Select **Delete**.</span></span>
3. <span data-ttu-id="cb825-289">เลือก **Model.Data2.Level2**</span><span class="sxs-lookup"><span data-stu-id="cb825-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="cb825-290">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-290">Select **Delete**.</span></span>
5. <span data-ttu-id="cb825-291">เลือก **Model.Data2.Level3**</span><span class="sxs-lookup"><span data-stu-id="cb825-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="cb825-292">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-292">Select **Delete**.</span></span>
7. <span data-ttu-id="cb825-293">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cb825-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="cb825-294">คุณนำฟิลด์ที่คำนวณได้เดียวกัน **Model.Data2.Levels** มาใช้ซ้ำหลายครั้งในการผูกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="cb825-295">เป็นการง่ายมากที่จะใช้และรักษาฟิลด์ที่คำนวณได้เดียว แทนที่จะทำเช่นนี้สำหรับฟิลด์ที่คล้ายกันหลายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="cb825-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="cb825-296">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb825-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="cb825-297">เวอร์ชันที่ปรับปรุงเสร็จสมบูรณ์ของรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="cb825-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="cb825-298">ในแท็บด่วน **เวอร์ชัน** เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="cb825-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="cb825-299">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="cb825-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="cb825-300">ส่งออกเวอร์ชันที่เสร็จสมบูรณ์ของรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="cb825-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="cb825-301">เลือกรูปแบบ **รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์ (กำหนดเอง)** ในแผนภูมิการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cb825-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="cb825-302">ในแท็บด่วน **เวอร์ชัน** เลือกเวอร์ชันที่เสร็จสมบูรณ์ 1.1.1</span><span class="sxs-lookup"><span data-stu-id="cb825-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="cb825-303">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="cb825-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="cb825-304">เลือก **ส่งออกเป็นไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="cb825-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="cb825-305">จัดเก็บการตั้งค่าคอนฟิกที่ดาวน์โหลดไว้ภายในเครื่องในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="cb825-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="cb825-306">ทดสอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="cb825-306">Test ER formats</span></span> 
<span data-ttu-id="cb825-307">คุณสามารถรันรูปแบบ ER เริ่มต้นและที่ปรับปรุงแล้ว เพื่อให้แน่ใจว่าฟิลด์ที่คำนวณได้แบบพารามิเตอร์ที่ตั้งค่าคอนฟิกทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cb825-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="cb825-308">นำเข้าการตั้งค่าคอนฟิกของ ER</span><span class="sxs-lookup"><span data-stu-id="cb825-308">Import ER configurations</span></span>
<span data-ttu-id="cb825-309">คุณสามารถนำเข้าการตั้งค่าคอนฟิกที่ตรวจทานจาก RCS โดยใช้ที่จัดเก็บ ER ของชนิด **RCS**</span><span class="sxs-lookup"><span data-stu-id="cb825-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="cb825-310">หากคุณดำเนินการตามขั้นตอนในหัวข้อแล้ว [นำเข้าการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์( ER) จากRegulatory Configuration Services (RCS)](rcs-download-configurations.md) ใช้ที่จัดเก็บ ER ที่ตั้งค่าคอนฟิกเพื่อนำเข้าการตั้งค่าคอนฟิกที่กล่าวถึงก่อนหน้าในหัวข้อนี้ไปยังสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="cb825-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="cb825-311">มิฉะนั้น ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cb825-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="cb825-312">เลือกบริษัท **DEMF** และในแดชบอร์ดเริ่มต้น เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="cb825-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="cb825-313">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="cb825-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="cb825-314">นำเข้าการตั้งค่าคอนฟิกจาก ศูนย์ดาวน์โหลด Microsoft ในลำดับต่อไปนี้: รูปแบบข้อมูล, การแม็ปรูปแบบ, รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="cb825-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="cb825-315">ดำเนินการขั้นตอนต่อไปนี้ให้สำเร็จ สำหรับแต่ละการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="cb825-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="cb825-316">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="cb825-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="cb825-317">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="cb825-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="cb825-318">เลือก **เรียกดู** เพื่อเลือกการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="cb825-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="cb825-319">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-319">Select **OK**.</span></span>

4. <span data-ttu-id="cb825-320">นำเข้าการส่งออกจาก RCS เวอร์ชั่นเสร็จสมบูรณ์ 1.1.1 ของรูปแบบ **รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์ (กำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="cb825-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="cb825-321">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="cb825-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="cb825-322">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="cb825-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="cb825-323">เลือก **เรียกดู** เพื่อเลือกไฟล์ที่จัดเก็บภายใน **รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์ (กำหนดเอง)** ในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="cb825-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="cb825-324">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb825-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="cb825-325">รันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="cb825-325">Run ER formats</span></span>

1. <span data-ttu-id="cb825-326">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="cb825-327">เลือก **รูปแบบเพื่อเรียนรู้การเรียบแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="cb825-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="cb825-328">เลือก **รัน** บน ribbon บนสุด</span><span class="sxs-lookup"><span data-stu-id="cb825-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="cb825-329">บันทึกผลลัพธ์ที่สร้างขึ้นภายใน</span><span class="sxs-lookup"><span data-stu-id="cb825-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="cb825-330">เลือกรายการ **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์ (กำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="cb825-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="cb825-331">เลือก **รัน** บน ribbon บนสุด</span><span class="sxs-lookup"><span data-stu-id="cb825-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="cb825-332">บันทึกผลลัพธ์ที่สร้างขึ้นภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="cb825-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="cb825-333">เปรียบเทียบเนื้อหาของผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="cb825-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb825-334">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cb825-334">Additional resources</span></span>
[<span data-ttu-id="cb825-335">โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cb825-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
