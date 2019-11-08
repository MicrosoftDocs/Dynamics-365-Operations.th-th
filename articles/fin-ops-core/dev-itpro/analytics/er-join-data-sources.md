---
title: ใช้แหล่งข้อมูล JOIN ในการแม็ปแบบจำลอง ER เพื่อดึงข้อมูลจากหลายตารางแอปพลิเคชัน
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถใช้แหล่งข้อมูลชนิด JOIN ในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667965"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="1d8fc-103">ใช้แหล่งข้อมูล JOIN ในการรับข้อมูลจากหลายตารางแอปพลิเคชันในการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1d8fc-104">ขณะที่กำหนดค่าการแม็ปหรือรูปแบบของแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) คุณสามารถ [เพิ่ม](#review) แหล่งข้อมูลที่จำเป็นจากชนิดของ **การรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="1d8fc-105">ระหว่างการออกแบบ แหล่งข้อมูล **การรวม** จะถูกกำหนดเป็นชุดของหลายแหล่งข้อมูลที่จะมีการส่งคืนเป็นรายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1d8fc-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="1d8fc-106">สำหรับแหล่งข้อมูลทุกประเภท ยกเว้นประเภทแรก คุณจำเป็นต้องกำหนดเงื่อนไขที่จำเป็นเพื่อรวมเรกคอร์ดของแหล่งข้อมูลปัจจุบันและแหล่งข้อมูลก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="1d8fc-107">เมื่อรันไทม์ แหล่งข้อมูลที่กำหนดแล้วของชนิด **การรวม** [จะส่งคืน](#executeERformat) รายการเรกคอร์ดเดี่ยวที่มีฟิลด์จากเรกคอร์ดของแหล่งข้อมูลเรียกซ้อน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="1d8fc-108">ขณะนี้ระบบสนับสนุนชนิดของการรวมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-108">The following type of joins are currently supported:</span></span>

- <span data-ttu-id="1d8fc-109">ตัวเชื่อมภายนอก (ด้านซ้าย):</span><span class="sxs-lookup"><span data-stu-id="1d8fc-109">Outer (left) join:</span></span>
    - <span data-ttu-id="1d8fc-110">รวมเรกคอร์ดทั้งหมดของแหล่งข้อมูลแรก (ด้านซ้ายสุด) แล้วจับคู่ใดๆ ตามเงื่อนไขที่กำหนดค่าไว้ของแหล่งข้อมูลที่สอง (ด้านขวาสุด)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="1d8fc-111">ตัวเชื่อมภายใน (ด้านขวา):</span><span class="sxs-lookup"><span data-stu-id="1d8fc-111">Inner (right) join:</span></span>
    - <span data-ttu-id="1d8fc-112">รวมเรกคอร์ดเฉพาะของแหล่งข้อมูลแรก (ด้านซ้ายสุด) และเฉพาะของแหล่งข้อมูลที่สอง (ด้านขวาสุด) จับคู่กันตามเงื่อนไขที่ได้กำหนดค่าไว้</span><span class="sxs-lookup"><span data-stu-id="1d8fc-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="1d8fc-113">ในแหล่งข้อมูล **การรวม** ที่กำหนดค่าไว้ เมื่อแหล่งข้อมูลทั้งหมดเป็นชนิด **เรกคอร์ดตาราง** การดำเนินการของแหล่งข้อมูล Join สามารถ [ดำเนินการที่ระดับฐานข้อมูลได้](#analyze) โดยใช้คำสั่ง SQL เดี่ยว</span><span class="sxs-lookup"><span data-stu-id="1d8fc-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="1d8fc-114">การทำเช่นนี้จะช่วยลดจำนวนของการเรียกฐานข้อมูล ซึ่งจะช่วยปรับปรุงประสิทธิภาพของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-114">This reduces the number of database calls, which improves model mapping performance.</span></span> <span data-ttu-id="1d8fc-115">มิฉะนั้น การดำเนินการของ **ข้อมูลการรวม** จะดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="1d8fc-116">การใช้ฟังก์ชัน **VALUEIN** ในนิพจน์ ER ที่ระบุเงื่อนไขสำหรับเรกคอร์ดการรวมในแหล่งข้อมูลของชนิด Join ยังไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="1d8fc-117">เยี่ยมชมเพจ [โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md) สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="1d8fc-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="1d8fc-118">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="1d8fc-119">ตัวอย่าง: ใช้แหล่งข้อมูล JOIN ในการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="1d8fc-120">ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ดูแลระบบหรือนักพัฒนาการรายทางทางอิเล็กทรอนิกส์ จะสามารถกำหนดค่าการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อรับข้อมูลจากหลายตารางแอปพลิเคชันในครั้งเดียว โดยใช้แหล่งข้อมูลจากชนิด **การรวม** เพื่อปรับปรุงประสิทธิภาพการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d8fc-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="1d8fc-121">ขั้นตอนเหล่านี้สามารถดำเนินการได้สำหรับบริษัทใดๆ ของ Dynamics 365 Finance หรือ Regulatory Configuration Services (RCS)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1d8fc-122">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="1d8fc-122">Prerequisites</span></span>

<span data-ttu-id="1d8fc-123">เพื่อดำเนินการตามตัวอย่างในหัวข้อนี้ให้สมบูรณ์ คุณจำเป็นต้องมีสิทธิ์เข้าถึงสิ่งต่อไปนี้ โดยขึ้นอยู่กับว่าจะใช้บริการใดในการดำเนินการตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="1d8fc-124">**การเข้าถึง Finance สำหรับหนึ่งในบทบาทต่อไปนี้:**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="1d8fc-125">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-125">Electronic reporting developer</span></span>
- <span data-ttu-id="1d8fc-126">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1d8fc-127">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-127">System administrator</span></span>

<span data-ttu-id="1d8fc-128">**การเข้าถึง RCS สำหรับหนึ่งในบทบาทต่อไปนี้:**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="1d8fc-129">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-129">Electronic reporting developer</span></span>
- <span data-ttu-id="1d8fc-130">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1d8fc-131">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-131">System administrator</span></span>

<span data-ttu-id="1d8fc-132">คุณยังจำเป็นต้องดำเนินการขั้นตอนแรกให้เสร็จสิ้นในขั้นตอนกระบวนงาน [สร้างผู้ให้บริการการกำหนดค่าและทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="1d8fc-133">นอกจากนี้ คุณจำเป็นต้องดาวน์โหลดจาก [ศูนย์ดาวน์โหลด Microsoft](https://go.microsoft.com/fwlink/?linkid=000000) และบันทึกไฟล์ตัวอย่างการกำหนดค่า ER ไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-133">In advance, you must also download from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) and save locally the following sample ER configuration files:</span></span>

| <span data-ttu-id="1d8fc-134">**คำอธิบายเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-134">**Content description**</span></span>  | <span data-ttu-id="1d8fc-135">**ชื่อไฟล์**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="1d8fc-136">ไฟล์ตัวอย่างการกำหนดค่า **แบบจำลองข้อมูล ER** ซึ่งใช้เป็นแหล่งข้อมูลสำหรับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="1d8fc-137">แบบจำลองเพื่อเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="1d8fc-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="1d8fc-138">ไฟล์ตัวอย่างการกำหนดค่า **การแม็ปแบบจำลอง ER** ซึ่งจะนำไปใช้งานกับแบบจำลองข้อมูล ER สำหรับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="1d8fc-139">การแม็ปเพื่อเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="1d8fc-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="1d8fc-140">ไฟล์ตัวอย่างการกำหนดค่า **รูปแบบ ER**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="1d8fc-141">ไฟล์นี้จะอธิบายถึงข้อมูลที่จะนำไปเติมเป็นส่วนประกอบของรูปแบบ ER สำหรับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="1d8fc-142">รูปแบบเพื่อเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="1d8fc-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="1d8fc-143">เรียกใช้ผู้ให้บริการการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="1d8fc-144">เข้าถึง Finance หรือ RCS อย่างใดอย่างหนึ่งในเซสชันแรกของเว็บเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="1d8fc-145">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="1d8fc-146">ในเพจ **การกำหนดค่าการแปลเป็นภาษาท้องถิ่น** ในส่วน **ผู้ให้บริการการกำหนดค่า** ตรวจสอบให้แน่ใจว่าผู้ให้บริการการกำหนดค่าสำหรับบริษัทตัวอย่าง Litware, Inc. (http://www.litware.com) ถูกแสดงและมีการทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the Litware, Inc. (http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="1d8fc-147">ถ้าคุณไม่เห็นผู้ให้บริการการกำหนดค่านี้ ทำตามขั้นตอนในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![พื้นที่ทำงานการรายงานทางอิเล็กทรอนิกส์](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="1d8fc-149">นำเข้าไฟล์ตัวอย่างการกำหนดค่า ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="1d8fc-150">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="1d8fc-151">นำเข้าไฟล์การกำหนดค่าแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="1d8fc-152">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="1d8fc-153">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="1d8fc-154">เลือก **เรียกดู** เพื่อค้นหาไฟล์ **แบบจำลองเพื่อการเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="1d8fc-155">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-155">Select **OK**.</span></span>
3. <span data-ttu-id="1d8fc-156">นำเข้าไฟล์การกำหนดค่าการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-156">Import the ER model mapping configuration file.</span></span>
    1. <span data-ttu-id="1d8fc-157">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="1d8fc-158">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="1d8fc-159">เลือก **เรียกดู** เพื่อค้นหาไฟล์ **การแม็ปเพื่อการเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="1d8fc-160">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-160">Select **OK**.</span></span>
4.  <span data-ttu-id="1d8fc-161">นำเข้าไฟล์การกำหนดค่ารูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="1d8fc-162">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="1d8fc-163">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="1d8fc-164">เลือก **เรียกดู** เพื่อค้นหาไฟล์ **รูปแบบเพื่อการเรียนรู้แหล่งข้อมูล JOIN.รุ่น.1.1.xml**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="1d8fc-165">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-165">Select **OK**.</span></span>
5.  <span data-ttu-id="1d8fc-166">ในแผนภูมิการกำหนดค่า ขยายรายการ **แบบจำลองเพื่อการเรียนรู้แหล่งข้อมูล JOIN** และรายการแบบจำลองอื่น (เมื่อสามารถใช้งานได้)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6.  <span data-ttu-id="1d8fc-167">สังเกตรายการของการกำหนดค่า ER ในแผนภูมิและรายละเอียดรุ่นบนแท็บด่วนของ **รุ่น** ซึ่งจะใช้เป็นแหล่งของข้อมูลสำหรับรายงานตัวอย่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** fast tab – they will be used as the source of data for your sample report.</span></span>

    ![เพจการกำหนดค่าการรายงานทางอิเล็กทรอนิกส์](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="1d8fc-169">เปิดใช้ตัวเลือการติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-169">Turn on execution trace options</span></span>
1.  <span data-ttu-id="1d8fc-170">เลือก **การกำหนดค่า**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-170">Select **CONFIGURATIONS**.</span></span>
2.  <span data-ttu-id="1d8fc-171">เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-171">Select **User parameters**.</span></span>
3.  <span data-ttu-id="1d8fc-172">ตั้งค่าพารามิเตอร์การติดตามการดำเนินการ ตามที่ปรากฏในภาพหน้าจอด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![เพจพารามิเตอร์ผู้ใช้การรายงานทางอิเล็กทรอนิกส์](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="1d8fc-174">เมื่อเปิดใช้งานพารามิเตอร์เหล่านี้แล้ว สำหรับการดำเนินการทุกรายการของไฟล์รูป ER ที่นำเข้ามา การติดตามการดำเนินการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1d8fc-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="1d8fc-175">โดยใช้รายละเอียดของการติดตามการดำเนินการที่สร้างขึ้น คุณสามารถวิเคราะห์การดำเนินการของส่วนประกอบการแม็ปรูปแบบ ER และแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model mapping components.</span></span> <span data-ttu-id="1d8fc-176">เยี่ยมชมเพจ [ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md) สำหรับรายละเอียดเกี่ยวกับคุณลักษณะการติดตามการดำเนินการ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="1d8fc-177">ตรวจทานการแม็ปแบบจำลอง ER (ส่วนที่ 1)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="1d8fc-178">ตรวจทานการตั้งค่าของส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-178">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="1d8fc-179">ส่วนประกอบถูกำหนดค่าให้เข้าถึงข้อมูลเกี่ยวกับรุ่นของการกำหนดค่า ER รายละเอียดของการกำหนดค่าและผู้ให้บริการการกำหนดค่าโดยไม่ใช้แหล่งข้อมูลของชนิด **การรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1.  <span data-ttu-id="1d8fc-180">เลือกการกำหนดค่า **การแม็ปเพื่อการเรียนรู้แหล่งข้อมูล JOIN**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2.  <span data-ttu-id="1d8fc-181">เลือก **ตัวออกแบบ** เพื่อเปิดรายการของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="1d8fc-181">Select **Designer** to open the list of mappings.</span></span>
3.  <span data-ttu-id="1d8fc-182">เลือก **ตัวออกแบบ** เพื่อตรวจทานรายละเอียดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="1d8fc-182">Select **Designer** to review the mapping details.</span></span> 
4.  <span data-ttu-id="1d8fc-183">เลือก **แสดงรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-183">Select **Show details**.</span></span>
5.  <span data-ttu-id="1d8fc-184">ในแผนภูมิการกำหนดค่า ขยายแบบจำลองข้อมูล **Set1** และ **Set1.Details** ของรายการ:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="1d8fc-185">การผูก **Details: Record list = Versions** บ่งชี้ถึงรายการ **Set1.Details** ถูกผูกกับแหล่งข้อมูล **รุ่น** ส่งคืนเรกคอร์ดของตาราง **ERSolutionVersionTable**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="1d8fc-186">แต่ละเรกคอร์ดของตารางนี้แสดงถึงรุ่นเดียวของการกำหนดค่า ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="1d8fc-187">เนื้อหาของตารางนี้แสดงอยู่ในแท็บด่วน **รุ่น** ในเพจ **การกำหนดค่า**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-187">The content of this table is presented in the **Versions** fast tab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="1d8fc-188">การผูก **ConfigurationVersion: String = @.PublicVersionNumber** หมายความว่าค่าของรุ่นสาธารณะของรุ่นการกำหนดค่า ER แต่ละรุ่นถูกนำมาจากฟิลด์ **PublicVersionNumber** ของตาราง **ERSolutionVersionTable** แนะนำไปวางในรายการ **ConfigurationVersion**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="1d8fc-189">การผูก **ConfigurationTitle: String = @.'>Relations'.Solution.Name** บ่งชี้ว่าชื่อของการกำหนดค่า ER ถูกนำมาจากฟิลด์ **ชื่อ** ของตาราง **ERSolutionTable** ประเมินโดนใช้ความสัมพันธ์แบบกลุ่มต่อหนึ่ง (**'>Relations'**) ระหว่างตาราง **ERSolutionVersionTable** และ **ERSolutionTable**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="1d8fc-190">ชื่อของการกำหนดค่า ER ของอินสแตนซ์แอปพลิเคชันปัจจุบันจะแสดงในแผนภูมิการกำหนดค่าในเพจ **การกำหนดค่า**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="1d8fc-191">การผูก **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** หมายความว่าชื่อของผู้ให้บริการการกำหนดค่าที่เป็นเจ้าของการกำหนดค่าปัจจุบันถูกนำมาจากฟิลด์ **ชื่อ** ของตาราง **ERVendorTable** ประเมินโดยใช้ความสัมพันธ์แบบกลุ่มต่อหนึ่งระหว่างตาราง **ERSolutionTable** และ **ERVendorTable**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="1d8fc-192">ชื่อของผู้ให้บริการการกำหนดค่า ER แสดงในแผนภูมิการกำหนดค่าในเพจ **การกำหนดค่า** ในหัวข้อของเพจสำหรับแต่ละการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="1d8fc-193">รายการทั้งหมดของผู้ให้บริการการกำหนดค่ามีอยู่ในเพจตาราง **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> ผู้ให้บริการการกำหนดค่า**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-Set1Review.PNG)

6.  <span data-ttu-id="1d8fc-195">ในแผนภูมิการกำหนดค่า ขยายแบบจำลองข้อมูล **Set1.Summary** ของรายการ:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="1d8fc-196">การผูก **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** บ่งชี้ว่ารายการ **Set1.Summary.VersionsNumber** ถูกผูกกับฟิลด์การรวม **VersionsNumber** ในแหล่งข้อมูล **VersionsSummary** ของชนิด **GroupBy** ที่ถูกกำหนดค่าไว้กับการส่งคืนจำนวนของเรกคอร์ดของตาราง **ERSolutionVersionTable** ผ่านแหล่งข้อมูล **Versions**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![เพจพารามิเตอร์แหล่งข้อมูล GROUPBY](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  <span data-ttu-id="1d8fc-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-198">Close the page.</span></span>

### <a name="review"></a><span data-ttu-id="1d8fc-199">ตรวจทานการแม็ปแบบจำลอง ER (ส่วนที่ 2)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="1d8fc-200">ตรวจทานการตั้งค่าของส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-200">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="1d8fc-201">ส่วนประกอบถูกกำหนดค่าเพื่อเข้าถึงข้อมูลเกี่ยวกับรุ่นของการกำหนดค่า ER รายละเอียดของการกำหนดค่าและผู้ให้บริการการกำหนดค่าด้วยชนิด **การรวม** ของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d8fc-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1.  <span data-ttu-id="1d8fc-202">ในแผนภูมิการกำหนดค่า ขยายแบบจำลองข้อมูล **Set2** และ **Set2.Details** ของรายการ:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="1d8fc-203">โปรดทราบว่าการผูก **Details: Record list = Details** บ่งชี้ว่ารายการ **Set2.Details** ถูกผูกกับแหล่งข้อมูล **รายละเอียด** ตามที่กำหนดค่าเป็นแหล่งข้อมูลของชนิด **การรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-203">Note that the binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="1d8fc-205">แหล่งข้อมูล **การรวม** สามารถเพิ่มโดยการเลือกแหล่งข้อมูล **Functions\Join**:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-AddJoinDS.PNG)

2.  <span data-ttu-id="1d8fc-207">เลือกแหล่งข้อมูล **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-207">Select **Detail**s data source.</span></span>
3.  <span data-ttu-id="1d8fc-208">เลือก **แก้ไข** ในบานหน้าต่าง **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-208">Select **Edit** in the **Data sources** pane.</span></span>
4.  <span data-ttu-id="1d8fc-209">เลือก **แก้ไขการรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-209">Select **Edit join**.</span></span>
5.  <span data-ttu-id="1d8fc-210">เลือก **แสดงรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-210">Select **Show details**.</span></span>

    ![เพจพารามิเตอร์แหล่งข้อมูล JOIN](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="1d8fc-212">เพจนี้ใช้เพื่อออกแบบแหล่งข้อมูลที่จำเป็นของ **ชนิดการรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="1d8fc-213">เมื่อรันไทม์ แหล่งข้อมูลนี้จะสร้างรายการรวมเดี่ยวของเรกคอร์ดจากแหล่งข้อมูลในกริด **รายการที่รวมแล้ว**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="1d8fc-214">การรวมของเรกคอร์ดจะเริ่มจากแหล่งข้อมูล **ConfigurationProviders** ที่อยู่ในกริดเหมือนกับอันแรก (คอลัมน์ **ชนิด** จะว่างเปล่าสำหรับฟิลด์นั้น)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="1d8fc-215">เรกคอร์ดของทุกแหล่งข้อมูลจะถูกรวมตามลำดับไปยังเรกคอร์ดของแหล่งข้อมูลหลักตามลำดับในกริด</span><span class="sxs-lookup"><span data-stu-id="1d8fc-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="1d8fc-216">แหล่งข้อมูลที่มีการรวมต้องถูกกำหนดค่าเป็นแหล่งข้อมูลเรียกซ้อนภายใต้แหล่งข้อมูลเป้าหมาย (แหล่งข้อมูล **1Versions** เรียกซ้อนอยู่ภายใต้ **1Configurations** แหล่งข้อมูล **1Configurations** เรียกซ้อนอยู่ภายใต้ **ConfigurationProviders**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-216">Every joining data source must be configured as a data source nested under a target data source (**1Versions** data source is nested under **1Configurations** one; **1Configurations** data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="1d8fc-217">แหล่งข้อมูลที่กำหนดค่าไว้แต่ละรายการจำเป็นต้องมีเงื่อนไขสำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="1d8fc-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="1d8fc-218">ในแหล่งข้อมูลสำหรับ **การรวม** โดยเฉพาะครั้งนี้ การรวมต่อไปนี้จะถูกกำหนดเป็น:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="1d8fc-219">แต่ละเรกคอร์ดของแหล่งข้อมูล **ConfigurationProviders** (อ้างอิงถึงตาราง **ERVendorTable** ) ถูกรวมกับเฉพาะเรกคอร์ดของ **1Configurations** (อ้างอิงถึงตาราง **ERSolutionTable**) มีค่าเดียวกันกับฟิลด์ **SolutionVendor** และ **RecId**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="1d8fc-220">ชนิด **ตัวเชื่อมภายใน** จะถูกใช้สำหรับการรวมครั้งนี้และเงื่อนไขต่อจากนี้สำหรับเรกคอร์ดที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span> 

    <span data-ttu-id="1d8fc-221">ตัวกรอง (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="1d8fc-222">แต่ละเรกคอร์ดของแหล่งข้อมูล **1Configurations** (อ้างอิงถึงตาราง **ERSolutionTable**) ถูกรวมกับเฉพาะเรกคอร์ดของ **1Versions** (อ้างอิงถึงตาราง **ERSolutionVersionTable**) มีค่าเดียวกันกับฟิลด์ **Solution** และ **RecId**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="1d8fc-223">ชนิด **ตัวเชื่อมภายใน** จะถูกใช้สำหรับการรวมครั้งนี้และเงื่อนไขต่อจากนี้สำหรับเรกคอร์ดที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="1d8fc-224">ตัวกรอง (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="1d8fc-225">ตัวเลือก **ดำเนินการ** ถูกกำหนดค่าเป็น **การสอบถาม** หมายความว่าแหล่งข้อมูลการรวมนี้จะถูกดำเนินการเมื่อรันไทม์บนระดับฐานข้อมูลเป็นการเรียก SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="1d8fc-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="1d8fc-226">โปรดทราบว่าการรวมเรกคอร์ดของแหล่งข้อมูลแสดงถึงตารางแอปพลิเคชัน คุณสามารถระบุเงื่อนไขการรวมโดยการใช้คู่ของฟิลด์นอกจากที่ใช้อธิบายความสัมพันธ์ AOT ระหว่างตารางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1d8fc-226">Note that for joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="1d8fc-227">ชนิดของการรวมนี้สามารถกดหนดค่าเพื่อดำเนินการที่ระดับฐานข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="1d8fc-227">This type of join can be configured to execute at the database level as well.</span></span>

6.  <span data-ttu-id="1d8fc-228">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-228">Close the page.</span></span>
7.  <span data-ttu-id="1d8fc-229">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-229">Select **Cancel**.</span></span>
8.  <span data-ttu-id="1d8fc-230">ในแผนภูมิการกำหนดค่า ขยายแบบจำลองข้อมูล **Set2.Summary** ของรายการ:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="1d8fc-231">การผูก **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** บ่งชี้ว่ารายการ **Set2.Summary.VersionsNumber** ถูกผูกกับฟิลด์การรวม **VersionsNumber** ในแหล่งข้อมูล **DetailsSummary** ของชนิด **GroupBy** ที่ถูกกำหนดค่าไว้กับการส่งคืนจำนวนของเรกคอร์ดที่รวมแล้วของแหล่งข้อมูล **รายละเอียด** ของชนิด **การรวม**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="1d8fc-232">โปรดทราบว่าตัวเลือกสถานที่ **การดำเนินการ** ถูกกำหนดค่าเป็น **การสอบถาม** หมายความว่าแหล่งข้อมูล **GroupBy** นี้จะถูกดำเนินการเมื่อรันไทม์เป็นการเรียก SQL โดยตรงที่ระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d8fc-232">Note that the **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be executed at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="1d8fc-233">การทำเช่นนี้เป็นไปได้เนื่องจากแหล่งข้อมูลฐาน **รายละเอียด** ของชนิด **การรวม** ถูกกำหนดค่าเป็นดำเนินการที่ระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d8fc-233">This is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![เพจพารามิเตอร์แหล่งข้อมูล GROUPBY](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  <span data-ttu-id="1d8fc-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-235">Close the page.</span></span>
10. <span data-ttu-id="1d8fc-236">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-236">Select **Cancel**.</span></span>

### <a name="executeERformat"></a> <span data-ttu-id="1d8fc-237">ดำเนินการรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-237">Execute ER format</span></span>

1.  <span data-ttu-id="1d8fc-238">เข้าถึง Finance หรือ RCS ในเซสชันที่สองของเว็บเบราว์เซอร์ของคุณโดยใช้ข้อมูลประจำตัวและบริษัทเดิมกับที่ใช้ในเซสชันแรก</span><span class="sxs-lookup"><span data-stu-id="1d8fc-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2.  <span data-ttu-id="1d8fc-239">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="1d8fc-240">ขยายการกำหนดค่า **แบบจำลองเพื่อการเรียนรู้แหล่งข้อมูล JOIN**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4.  <span data-ttu-id="1d8fc-241">เลือกการกำหนดค่า **รูปแบบเพื่อการเรียนรู้แหล่งข้อมูล JOIN**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5.  <span data-ttu-id="1d8fc-242">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-242">Select **Designer**.</span></span>
6.  <span data-ttu-id="1d8fc-243">เลือก **แสดงรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-243">Select **Show details**.</span></span>
7.  <span data-ttu-id="1d8fc-244">เลือก **การแม็ป**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-244">Select **Mapping**.</span></span>
8.  <span data-ttu-id="1d8fc-245">เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="1d8fc-246">โปรดทราบว่ารูปแบบนี้ได้รับการออกแบบมาเพื่อเติมข้อมูลไฟล์ข้อความที่สร้างขึ้นด้วยรายการใหม่สำหรับทุกๆ รุ่นของการกำหนดค่า ER (ลำดับ **รุ่น**)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-246">Note that this format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="1d8fc-247">แต่ละรายการที่ถูกสร้างขึ้นจะประกอบด้วยชื่อของผู้ให้บริการการกำหนดค่าที่เป็นเจ้าของการกำหนดค่าปัจจุบัน ชื่อของการกำหนดค่า และรุ่นของการกำหนดค่าถูกคั่นด้วยเครื่องหมายอัฒภาค</span><span class="sxs-lookup"><span data-stu-id="1d8fc-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="1d8fc-248">รายการสุดท้ายที่สร้างขึ้นจะประกอบด้วยจำนวนของรุ่นของการกำหนดค่า ER ที่พบ (ลำดับ **สรุป**)</span><span class="sxs-lookup"><span data-stu-id="1d8fc-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![เพจตัวออกแบบรูปแบบ ER](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="1d8fc-250">แหล่งข้อมูล **ข้อมูล** และ **สรุป** จะถูกใช้เพื่อเติมรายละเอียดรุ่นการกำหนดค่าไปยังไฟล์ที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="1d8fc-251">ข้อมูลจากแบบจำลองข้อมูล **Set1** ถูกใช้เมื่อคุณเลือก **ไม่** สำหรับแหล่งข้อมูล **ตัวเลือก** เมื่อรันไทม์บนเพจโต้ตอบผู้ใช้ระหว่างการเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="1d8fc-252">ข้อมูลจากแบบจำลองข้อมูล **Set2** ถูกใช้เมื่อคุณเลือก **ใช่** สำหรับแหล่งข้อมูล **ตัวเลือก** เมื่อรันไทม์บนเพจโต้ตอบผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="1d8fc-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![เพจตัวออกแบบรูปแบบ ER](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  <span data-ttu-id="1d8fc-254">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-254">Select **Run**.</span></span>
10. <span data-ttu-id="1d8fc-255">ในเพจโต้ตอบ เลือก **ไม่** ในฟิลด์ **ใช้แหล่งข้อมูล JOIN**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="1d8fc-256">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-256">Select **OK**.</span></span>
12. <span data-ttu-id="1d8fc-257">ตรวจทานไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1d8fc-257">Review generated file.</span></span>

    ![เพจโต้ตอบผู้ใช้ ER](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="1d8fc-259">วิเคราะห์การติดตามการเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-259">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="1d8fc-260">ในเซสชันแรกของ Finance หรือ RCS ให้เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="1d8fc-261">เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-261">Select **Performance trac**e.</span></span>
3.  <span data-ttu-id="1d8fc-262">ในกริด **การติดตามประสิทธิภาพ** ให้เลือกเรกคอร์ดบนสุดของการติดตามการเรียกใช้ล่าสุดของรูปแบบ ER ที่ใช้ส่วนประกอบการแม็ปแบบจำลองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="1d8fc-263">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-263">Select **OK**.</span></span>

    <span data-ttu-id="1d8fc-264">โปรดทราบว่าสถิติการเรียกใช้จะช่วยแจ้งให้คุณทราบถึงการเรียกใช้ไปยังตารางแอปพลิเคชันที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-264">Note that execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="1d8fc-265">**ERSolutionTable** ถูกเรียกหลายครั้งตามที่คุณมีเรกคอร์ดรุ่นการกำหนดค่าในตาราง **ERSolutionVersionTable** ขณะที่จำนวนของการเรียกอาจถูกลดจำนวนครั้งเพื่อปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1d8fc-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="1d8fc-266">**ERSolutionTable** ถูกเรียกสองครั้งตามต่อทุกเรกคอร์ดรุ่นการกำหนดค่าที่พบในตาราง **ERSolutionVersionTable** ขณะที่จำนวนของการเรียกอาจถูกลดด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-Set1Run2.PNG)

5.  <span data-ttu-id="1d8fc-268">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1d8fc-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="1d8fc-269">ดำเนินการรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-269">Execute ER format</span></span>

1.  <span data-ttu-id="1d8fc-270">สลับไปยังแท็บเว็บเบราว์เซอร์ของคุณด้วยเซสชันที่สองของ Finance หรือ RCS</span><span class="sxs-lookup"><span data-stu-id="1d8fc-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2.  <span data-ttu-id="1d8fc-271">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-271">Select **Run**.</span></span>
3.  <span data-ttu-id="1d8fc-272">บนเพจโต้ตอบ ให้เลือก **ใช่** ในฟิลด์ **ใช้แหล่งข้อมูล JOIN**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4.  <span data-ttu-id="1d8fc-273">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-273">Select **OK**.</span></span>
5.  <span data-ttu-id="1d8fc-274">ตรวจทานไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1d8fc-274">Review generated file.</span></span>

    ![เพจโต้ตอบผู้ใช้ ER](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> <span data-ttu-id="1d8fc-276">วิเคราะห์การติดตามการเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="1d8fc-276">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="1d8fc-277">ในเซสชันแรกของ Finance หรือ RCS ให้เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="1d8fc-278">เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-278">Select **Performance trace**.</span></span>
3.  <span data-ttu-id="1d8fc-279">ในกริด **การติดตามประสิทธิภาพ** ให้เลือกเรกคอร์ดบนสุดที่แสดงการติดตามการเรียกใช้ล่าสุดของรูปแบบ ER ที่ใช้ส่วนประกอบการแม็ปแบบจำลองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="1d8fc-280">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-280">Select **OK**.</span></span>

    <span data-ttu-id="1d8fc-281">โปรดสังเกตว่าสถิติการดำเนินการจะแจ้งให้คุณทราบถึงสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d8fc-281">Note that execution statistics informs you about the following:</span></span>

    - <span data-ttu-id="1d8fc-282">ฐานข้อมูลแอปพลิเคชันถูกเรียกหนึ่งครั้งเพื่อรับเรกคอร์ดจากตาราง **ERVendorTable**, **ERSolutionTable** และ **ERSolutionVersionTable** เพื่อเข้าถึงฟิลด์ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="1d8fc-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="1d8fc-284">ฐานข้อมูลแอปพลิเคชันถูกเรียกหนึ่งครั้งเพื่อคำนวณจำนวนของรุ่นการกำหนดค่าโดยใช้การรวมที่กำหนดค่าไว้ในแหล่งข้อมูล **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="1d8fc-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a><span data-ttu-id="1d8fc-286">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1d8fc-286">Additional resources</span></span>

[<span data-ttu-id="1d8fc-287">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1d8fc-287">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1d8fc-288">การดำเนินการติดตามของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="1d8fc-288">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

