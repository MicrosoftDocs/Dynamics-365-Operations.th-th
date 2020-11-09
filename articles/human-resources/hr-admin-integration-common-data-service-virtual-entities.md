---
title: ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service
description: หัวข้อนี้แสดงวิธีการตั้งค่าคอนฟิกเอนทิตีเสมือนสำหรับ Dynamics 365 Human Resources สร้างและอัพเดตข้อมูลเอนทิตีเสมือนที่มีอยู่ และวิเคราะห์เอนทิตีที่สร้างและพร้อมใช้งาน
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058165"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="9d946-104">ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9d946-105">Dynamics 365 Human Resources เป็นแหล่งข้อมูลเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="9d946-106">ซึ่งให้การดำเนินการส้ราง อ่าน อัปเดต และลบทั้งหมด (CRUD) จาก Common Data Service และ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="9d946-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="9d946-107">ข้อมูลสำหรับเอนทิตีเสมือนไม่ได้จัดเก็บไว้ใน Common Data Service แต่อยู่ในฐานข้อมูลใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="9d946-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="9d946-108">เมื่อต้องการเปิดใช้งานการดำเนินงาน CRUD บนเอนทิตีทรัพยากรบุคคลจาก Common Data Service คุณต้องทำให้เอนทิตีพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="9d946-109">ซึ่งช่วยให้คุณสามารถทำการดำเนินงาน CRUD จาก Common Data Service และ Microsoft Power Platform บนข้อมูลที่อยู่ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9d946-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="9d946-110">การดำเนินงานยังสนับสนุนการตรวจสอบตรรกะทางธุรกิจทั้งหมดของทรัพยากรบุคคล เพื่อให้มั่นใจในความสมบูรณ์ของข้อมูลเมื่อเขียนข้อมูลไปยังเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9d946-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="9d946-111">เอนทิตีเสมือนพร้อมใช้งานสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9d946-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="9d946-112">เอนทิตี Open Data Protocol (OData) ทั้งหมดในทรัพยากรบุคคลพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="9d946-113">นอกจากนี้ยังพร้อมใช้งานใน Power Platform ด้วย</span><span class="sxs-lookup"><span data-stu-id="9d946-113">They're also available in Power Platform.</span></span> <span data-ttu-id="9d946-114">ขณะนี้ คุณสามารถสร้างแอปและประสบการณ์พร้อมกับข้อมูลโดยตรงจากทรัพยากรบุคคลที่มีความสามารถ CRUD เต็มที่ โดยไม่มีการคัดลอกหรือการซิงโครไนส์ข้อมูลไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="9d946-115">คุณสามารถใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งเปิดใช้งานสถานการณ์การทำงานร่วมกันสำหรับกระบวนการทางธุรกิจในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9d946-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="9d946-116">คุณสามารถดูรายการเอนทิตีเสมือนที่เปิดใช้งานในสภาพแวดล้อม และเริ่มต้นการทำงานกับเอนทิตีใน [Power Apps](https://make.powerapps.com) ในโซลูชัน **เอนทิตีเสมือนของ Dynamics 365 HR**</span><span class="sxs-lookup"><span data-stu-id="9d946-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![เอนทิตีเสมือนของ Dynamics 365 HR ใน Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="9d946-118">เอนทิตีเสมือนกับเอนทิตีธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="9d946-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="9d946-119">เอนทิตีเสมือนสำหรับทรัพยากรบุคคลไม่เหมือนกับเอนทิตี Common Data Service ธรรมชาติที่สร้างขึ้นสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9d946-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="9d946-120">เอนทิตีธรรมชาติสำหรับทรัพยากรบุคคลสร้างขึ้นแยกต่างหาก และรักษาไว้ในโซลูชันทั่วไปของ HCM ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="9d946-121">ด้วยเอนทิตีธรรมชาติ ข้อมูลจะถูกจัดเก็บไว้ใน Common Data Service และต้องมีการซิงโครไนส์กับฐานข้อมูลใบสมัครทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9d946-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="9d946-122">สำหรับรายการของเอนทิตี Common Data Service ธรรมชาติสำหรับทรัพยากรบุคคล ให้ดูที่ [เอนทีตี Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)</span><span class="sxs-lookup"><span data-stu-id="9d946-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="9d946-123">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9d946-123">Setup</span></span>

<span data-ttu-id="9d946-124">ทำตามขั้นตอนการตั้งค่าต่อไปนี้เพื่อเปิดใช้งานเอนทิตีเสมือนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d946-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="9d946-125">ลงทะเบียนแอปใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="9d946-126">ก่อนอื่น คุณจำเป็นต้องลงทะเบียนแอปในพอร์ทัล Azure เพื่อให้แพลตฟอร์มข้อมูลเฉพาะของ Microsoft สามารถให้บริการการรับรองความถูกต้องและการตรวจสอบความถูกต้องสำหรับแอปและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9d946-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="9d946-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนแอปใน Azure ดูที่ [การเริ่มต้นแบบด่วน: ลงทะเบียนโปรแกรมประยุกต์ด้วยฟอร์มข้อมูลเฉพาะของ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)</span><span class="sxs-lookup"><span data-stu-id="9d946-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="9d946-128">เปิด [พอร์ทัล Microsoft Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="9d946-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="9d946-129">ในรายการบริการ Azure เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="9d946-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="9d946-130">เลือก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="9d946-130">Select **New registration**.</span></span>

4. <span data-ttu-id="9d946-131">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="9d946-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="9d946-132">ตัวอย่างเช่น **เอนทีตีเสมือน Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="9d946-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="9d946-133">ในฟิลด์ **เปลี่ยนเส้นทาง URI** ให้ป้อน URL พื้นที่ว่างในชื่อของอินสแตนซ์ของทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d946-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="9d946-134">เลือก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="9d946-134">Select **Register**.</span></span>

7. <span data-ttu-id="9d946-135">เมื่อลงทะเบียนเสร็จสมบูรณ์แล้ว พอร์ทัล Azure จะแสดงบานหน้าต่าง **ภาพรวม** ของการลงทะเบียนของแอป ซึ่งรวมถึง **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="9d946-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="9d946-136">จด **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="9d946-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="9d946-137">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="9d946-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="9d946-138">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบรับรองและข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="9d946-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="9d946-139">ในส่วน **ข้อมูลลับของไคลเอนต์** ของหน้า ให้เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9d946-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="9d946-140">ระบุคำอธิบาย เลือกช่วงเวลา และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9d946-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="9d946-141">บันทึกค่าของข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="9d946-141">Record the secret's value.</span></span> <span data-ttu-id="9d946-142">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="9d946-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9d946-143">ตรวจสอบให้แน่ใจว่าได้จดบันทึกค่าของข้อมูลลับไว้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="9d946-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="9d946-144">ข้อมูลลับจะไม่มีการแสดงอีกครั้งหลังจากที่คุณออกจากหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9d946-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="9d946-145">ติดตั้งแอป Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="9d946-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="9d946-146">ติดตั้งแอป Dynamics 365 HR Virtual Entity ในสภาพแวดล้อม Power Apps ของคุณ เพื่อจัดวางแพคเกจโซลูชันเอนทิตีเสมือนไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="9d946-147">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="9d946-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9d946-148">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d946-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="9d946-149">ในส่วน **ทรัพยากร** ของหน้า ให้เลือก **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="9d946-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="9d946-150">เลือกการดำเนินการ **ติดตั้งแอป**</span><span class="sxs-lookup"><span data-stu-id="9d946-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="9d946-151">เลือก **Dynamics 365 HR Virtual Entity** และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="9d946-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="9d946-152">ตรวจทานและทำเครื่องหมายเพื่อยอมรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="9d946-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="9d946-153">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="9d946-153">Select **Install**.</span></span>

<span data-ttu-id="9d946-154">การติดตั้งใช้เวลาสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="9d946-154">The install takes a few minutes.</span></span> <span data-ttu-id="9d946-155">เมื่อเสร็จสิ้น ให้ดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="9d946-155">When it completes, continue to the next steps.</span></span>

![ติดตั้งแอป Dynamics 365 HR Virtual Entity จากศูนย์การจัดการ Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="9d946-157">ตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="9d946-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="9d946-158">ขั้นตอนต่อไปคือการตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือนในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="9d946-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="9d946-159">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="9d946-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9d946-160">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d946-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="9d946-161">เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="9d946-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="9d946-162">ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้าโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="9d946-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="9d946-163">บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **การตั้งค่าคอนฟิกแหล่งข้อมูลเสมือน Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="9d946-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="9d946-164">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="9d946-164">Select **Results**.</span></span>

7. <span data-ttu-id="9d946-165">เลือกเรกคอร์ด **แหล่งข้อมูล Microsoft HR**</span><span class="sxs-lookup"><span data-stu-id="9d946-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="9d946-166">ป้อนข้อมูลที่จำเป็นสำหรับการตั้งค่าคอนฟิกแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d946-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="9d946-167">**URL เป้าหมาย** : URL ของพื้นที่ว่างในชื่อทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d946-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="9d946-168">**รหัสผู้เช่า** : รหัสผู้เช่า Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="9d946-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="9d946-169">**รหัสโปรแกรมประยุกต์ AAD** : รหัสโปรแกรมประยุกต์ (ไคลเอนต์) ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="9d946-170">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="9d946-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="9d946-171">**ข้อมูลลับโปรแกรมประยุกต์ AAD** : ข้อมูลลับของไคลเอนต์ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="9d946-172">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="9d946-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="9d946-173">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="9d946-173">Select **Save & Close**.</span></span>

   ![แหล่งข้อมูล Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="9d946-175">ให้สิทธิ์แอปใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="9d946-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="9d946-176">ให้สิทธิสำหรับใบสมัคร Azure AD สองใบในทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="9d946-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="9d946-177">แอปที่สร้างขึ้นสำหรับผู้เช่าของคุณในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="9d946-178">แอป Dynamics 365 HR Virtual Entity ที่ติดตั้งในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="9d946-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="9d946-179">ในทรัพยากรบุคคล ให้เปิดหน้า **ใบสมัคร Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="9d946-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="9d946-180">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครใหม่:</span><span class="sxs-lookup"><span data-stu-id="9d946-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="9d946-181">ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="9d946-182">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9d946-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="9d946-183">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="9d946-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="9d946-184">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครที่สอง:</span><span class="sxs-lookup"><span data-stu-id="9d946-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="9d946-185">**รหัสไคลเอนต์** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="9d946-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="9d946-186">**ชื่อ** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="9d946-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="9d946-187">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="9d946-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="9d946-188">สร้างคอนฟิกเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="9d946-188">Generate virtual entities</span></span>

<span data-ttu-id="9d946-189">เมื่อการตั้งค่าเสร็จสมบูรณ์ คุณสามารถเลือกเอนทิตีเสมือนที่คุณต้องการสร้างและเปิดใช้งานในอินสแตนซ์ Common Data Service ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="9d946-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="9d946-190">ในทรัพยากรบุคคล ให้เปิดหน้า **การรวม Common Data Service (CDS)**</span><span class="sxs-lookup"><span data-stu-id="9d946-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="9d946-191">เลือกแท็บ **เอนทิตีเสมือน**</span><span class="sxs-lookup"><span data-stu-id="9d946-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="9d946-192">การสลับ **เปิดใช้งานเอนทิตีเสมือน** จะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติเมื่อการตั้งค่าที่จำเป็นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="9d946-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="9d946-193">ถ้าการสลับถูกตั้งค่าเป็น **ไม่ใช่** ให้ตรวจสอบขั้นตอนในหัวข้อก่อนหน้านี้ของเอกสารนี้ เพื่อให้แน่ใจว่าการตั้งค่าข้อกำหนดเบื้องต้นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="9d946-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="9d946-194">เลือกเอนทิตีหรือเอนทิตีมากกว่าหนึ่งที่คุณต้องการสร้าง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="9d946-195">เลือก **สร้าง/รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="9d946-195">Select **Generate/refresh**.</span></span>

![การรวม Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="9d946-197">ตรวจสอบสถานะการสร้างเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9d946-197">Check entity generation status</span></span>

<span data-ttu-id="9d946-198">เอนทิตีเสมือนมีการสร้างใน Common Data Service โดยผ่านกระบวนการพื้นหลังแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="9d946-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="9d946-199">การอัปเดตในกระบวนการแสดงในศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9d946-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="9d946-200">รายละเอียดเกี่ยวกับกระบวนการ รวมถึงล็อกข้อผิดพลาด จะปรากฏในหน้า **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="9d946-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="9d946-201">ในทรัพยากรบุคคล ให้เปิดเพจรายการ **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="9d946-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="9d946-202">เลือกแท็บ **กระบวนการแบบเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="9d946-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="9d946-203">เลือก **กระบวนการแบบเบื้องหลังของการดำเนินงานแบบอะซิงโครนัสในการสำรวจเอนทิตีเสมือน**</span><span class="sxs-lookup"><span data-stu-id="9d946-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="9d946-204">เลือก **ดูผลลัพธ์ล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="9d946-204">Select **View most recent results**.</span></span>

<span data-ttu-id="9d946-205">บานหน้าต่าง slideout แสดงผลลัพธ์การดำเนินการล่าสุดสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="9d946-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="9d946-206">คุณสามารถดูล็อกสำหรับกระบวนการ รวมถึงข้อผิดพลาดที่ส่งคืนจาก Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9d946-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d946-207">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="9d946-207">See also</span></span>

[<span data-ttu-id="9d946-208">Common Data Service คืออะไร</span><span class="sxs-lookup"><span data-stu-id="9d946-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="9d946-209">ภาพรวมของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9d946-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="9d946-210">ภาพรวมความสัมพันธ์ของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9d946-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="9d946-211">สร้างและแก้ไขเอนทิตีเสมือนที่มีข้อมูลจากแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="9d946-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="9d946-212">พอร์ทัล Power Apps คืออะไร</span><span class="sxs-lookup"><span data-stu-id="9d946-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="9d946-213">ภาพรวมของการสร้างแอปใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="9d946-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
