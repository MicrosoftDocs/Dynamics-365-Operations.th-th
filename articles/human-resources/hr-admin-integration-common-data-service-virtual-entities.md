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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959586"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="cd049-104">ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cd049-105">Dynamics 365 Human Resources เป็นแหล่งข้อมูลเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="cd049-106">ซึ่งให้การดำเนินการส้ราง อ่าน อัปเดต และลบทั้งหมด (CRUD) จาก Common Data Service และ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="cd049-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="cd049-107">ข้อมูลสำหรับเอนทิตีเสมือนไม่ได้จัดเก็บไว้ใน Common Data Service แต่อยู่ในฐานข้อมูลใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="cd049-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="cd049-108">เมื่อต้องการเปิดใช้งานการดำเนินงาน CRUD บนเอนทิตีทรัพยากรบุคคลจาก Common Data Service คุณต้องทำให้เอนทิตีพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="cd049-109">ซึ่งช่วยให้คุณสามารถทำการดำเนินงาน CRUD จาก Common Data Service และ Microsoft Power Platform บนข้อมูลที่อยู่ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="cd049-110">การดำเนินงานยังสนับสนุนการตรวจสอบตรรกะทางธุรกิจทั้งหมดของทรัพยากรบุคคล เพื่อให้มั่นใจในความสมบูรณ์ของข้อมูลเมื่อเขียนข้อมูลไปยังเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd049-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="cd049-111">เอนทิตีเสมือนพร้อมใช้งานสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="cd049-112">เอนทิตี Open Data Protocol (OData) ทั้งหมดในทรัพยากรบุคคลพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="cd049-113">นอกจากนี้ยังพร้อมใช้งานใน Power Platform ด้วย</span><span class="sxs-lookup"><span data-stu-id="cd049-113">They're also available in Power Platform.</span></span> <span data-ttu-id="cd049-114">ขณะนี้ คุณสามารถสร้างแอปและประสบการณ์พร้อมกับข้อมูลโดยตรงจากทรัพยากรบุคคลที่มีความสามารถ CRUD เต็มที่ โดยไม่มีการคัดลอกหรือการซิงโครไนส์ข้อมูลไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="cd049-115">คุณสามารถใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งเปิดใช้งานสถานการณ์การทำงานร่วมกันสำหรับกระบวนการทางธุรกิจในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="cd049-116">คุณสามารถดูรายการเอนทิตีเสมือนที่เปิดใช้งานในสภาพแวดล้อม และเริ่มต้นการทำงานกับเอนทิตีใน [Power Apps](https://make.powerapps.com) ในโซลูชัน **เอนทิตีเสมือนของ Dynamics 365 HR**</span><span class="sxs-lookup"><span data-stu-id="cd049-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![เอนทิตีเสมือนของ Dynamics 365 HR ใน Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="cd049-118">เอนทิตีเสมือนกับเอนทิตีธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="cd049-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="cd049-119">เอนทิตีเสมือนสำหรับทรัพยากรบุคคลไม่เหมือนกับเอนทิตี Common Data Service ธรรมชาติที่สร้างขึ้นสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="cd049-120">เอนทิตีธรรมชาติสำหรับทรัพยากรบุคคลสร้างขึ้นแยกต่างหาก และรักษาไว้ในโซลูชันทั่วไปของ HCM ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="cd049-121">ด้วยเอนทิตีธรรมชาติ ข้อมูลจะถูกจัดเก็บไว้ใน Common Data Service และต้องมีการซิงโครไนส์กับฐานข้อมูลใบสมัครทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="cd049-122">สำหรับรายการของเอนทิตี Common Data Service ธรรมชาติสำหรับทรัพยากรบุคคล ให้ดูที่ [เอนทีตี Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)</span><span class="sxs-lookup"><span data-stu-id="cd049-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="cd049-123">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="cd049-123">Setup</span></span>

<span data-ttu-id="cd049-124">ทำตามขั้นตอนการตั้งค่าต่อไปนี้เพื่อเปิดใช้งานเอนทิตีเสมือนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="cd049-125">ลงทะเบียนแอปใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="cd049-126">ก่อนอื่น คุณจำเป็นต้องลงทะเบียนแอปในพอร์ทัล Azure เพื่อให้แพลตฟอร์มข้อมูลเฉพาะของ Microsoft สามารถให้บริการการรับรองความถูกต้องและการตรวจสอบความถูกต้องสำหรับแอปและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cd049-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="cd049-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนแอปใน Azure ดูที่ [การเริ่มต้นแบบด่วน: ลงทะเบียนโปรแกรมประยุกต์ด้วยฟอร์มข้อมูลเฉพาะของ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)</span><span class="sxs-lookup"><span data-stu-id="cd049-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="cd049-128">เปิด [พอร์ทัล Microsoft Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="cd049-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="cd049-129">ในรายการบริการ Azure เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="cd049-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="cd049-130">เลือก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="cd049-130">Select **New registration**.</span></span>

4. <span data-ttu-id="cd049-131">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="cd049-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="cd049-132">ตัวอย่างเช่น **เอนทีตีเสมือน Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="cd049-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="cd049-133">ในฟิลด์ **เปลี่ยนเส้นทาง URI** ให้ป้อน URL พื้นที่ว่างในชื่อของอินสแตนซ์ของทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="cd049-134">เลือก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="cd049-134">Select **Register**.</span></span>

7. <span data-ttu-id="cd049-135">เมื่อลงทะเบียนเสร็จสมบูรณ์แล้ว พอร์ทัล Azure จะแสดงบานหน้าต่าง **ภาพรวม** ของการลงทะเบียนของแอป ซึ่งรวมถึง **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="cd049-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="cd049-136">จด **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="cd049-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="cd049-137">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="cd049-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="cd049-138">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบรับรองและข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="cd049-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="cd049-139">ในส่วน **ข้อมูลลับของไคลเอนต์** ของหน้า ให้เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cd049-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="cd049-140">ระบุคำอธิบาย เลือกช่วงเวลา และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cd049-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="cd049-141">บันทึกค่าของข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="cd049-141">Record the secret's value.</span></span> <span data-ttu-id="cd049-142">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="cd049-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="cd049-143">ตรวจสอบให้แน่ใจว่าได้จดบันทึกค่าของข้อมูลลับไว้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="cd049-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="cd049-144">ข้อมูลลับจะไม่มีการแสดงอีกครั้งหลังจากที่คุณออกจากหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cd049-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="cd049-145">ติดตั้งแอป Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="cd049-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="cd049-146">ติดตั้งแอป Dynamics 365 HR Virtual Entity ในสภาพแวดล้อม Power Apps ของคุณ เพื่อจัดวางแพคเกจโซลูชันเอนทิตีเสมือนไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cd049-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="cd049-147">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="cd049-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cd049-148">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="cd049-149">ในส่วน **ทรัพยากร** ของหน้า ให้เลือก **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="cd049-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="cd049-150">เลือกการดำเนินการ **ติดตั้งแอป**</span><span class="sxs-lookup"><span data-stu-id="cd049-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="cd049-151">เลือก **Dynamics 365 HR Virtual Entity** และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="cd049-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="cd049-152">ตรวจทานและทำเครื่องหมายเพื่อยอมรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="cd049-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="cd049-153">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="cd049-153">Select **Install**.</span></span>

<span data-ttu-id="cd049-154">การติดตั้งใช้เวลาสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="cd049-154">The install takes a few minutes.</span></span> <span data-ttu-id="cd049-155">เมื่อเสร็จสิ้น ให้ดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="cd049-155">When it completes, continue to the next steps.</span></span>

![ติดตั้งแอป Dynamics 365 HR Virtual Entity จากศูนย์การจัดการ Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="cd049-157">ตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="cd049-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="cd049-158">ขั้นตอนต่อไปคือการตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือนในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="cd049-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="cd049-159">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="cd049-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cd049-160">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="cd049-161">เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="cd049-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="cd049-162">ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้าโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="cd049-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="cd049-163">บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **การตั้งค่าคอนฟิกแหล่งข้อมูลเสมือน Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="cd049-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="cd049-164">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="cd049-164">Select **Results**.</span></span>

7. <span data-ttu-id="cd049-165">เลือกเรกคอร์ด **แหล่งข้อมูล Microsoft HR**</span><span class="sxs-lookup"><span data-stu-id="cd049-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="cd049-166">ป้อนข้อมูลที่จำเป็นสำหรับการตั้งค่าคอนฟิกแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd049-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="cd049-167">**URL เป้าหมาย**: URL ของพื้นที่ว่างในชื่อทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="cd049-168">**รหัสผู้เช่า**: รหัสผู้เช่า Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="cd049-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="cd049-169">**รหัสโปรแกรมประยุกต์ AAD**: รหัสโปรแกรมประยุกต์ (ไคลเอนต์) ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="cd049-170">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="cd049-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="cd049-171">**ข้อมูลลับโปรแกรมประยุกต์ AAD**: ข้อมูลลับของไคลเอนต์ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="cd049-172">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="cd049-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="cd049-173">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="cd049-173">Select **Save & Close**.</span></span>

   ![แหล่งข้อมูล Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="cd049-175">ให้สิทธิ์แอปใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="cd049-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="cd049-176">ให้สิทธิสำหรับใบสมัคร Azure AD สองใบในทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="cd049-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="cd049-177">แอปที่สร้างขึ้นสำหรับผู้เช่าของคุณในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="cd049-178">แอป Dynamics 365 HR Virtual Entity ที่ติดตั้งในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="cd049-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="cd049-179">ในทรัพยากรบุคคล ให้เปิดหน้า **ใบสมัคร Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="cd049-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="cd049-180">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครใหม่:</span><span class="sxs-lookup"><span data-stu-id="cd049-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="cd049-181">ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="cd049-182">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd049-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="cd049-183">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="cd049-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="cd049-184">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครที่สอง:</span><span class="sxs-lookup"><span data-stu-id="cd049-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="cd049-185">**รหัสไคลเอนต์**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="cd049-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="cd049-186">**ชื่อ**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="cd049-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="cd049-187">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="cd049-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="cd049-188">สร้างคอนฟิกเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="cd049-188">Generate virtual entities</span></span>

<span data-ttu-id="cd049-189">เมื่อการตั้งค่าเสร็จสมบูรณ์ คุณสามารถเลือกเอนทิตีเสมือนที่คุณต้องการสร้างและเปิดใช้งานในอินสแตนซ์ Common Data Service ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="cd049-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="cd049-190">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="cd049-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cd049-191">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd049-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="cd049-192">เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="cd049-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="cd049-193">ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="cd049-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="cd049-194">บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **เอนทิตี HR ที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cd049-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="cd049-195">ใช้ตัวเลือกการกรองข้อมูลเพื่อค้นหาหนึ่งเอนทิตี หรือมากกว่าหนึ่งเอนทิตีที่คุณต้องการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cd049-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="cd049-196">เลือกเอนทิตีจากรายการ</span><span class="sxs-lookup"><span data-stu-id="cd049-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="cd049-197">บนหน้าเอนทิตี ให้เปลี่ยนคุณสมบัติ **สร้างขึ้นแล้ว** เป็น **ใช่** สำหรับเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd049-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="cd049-198">บันทึกและปิดหน้าเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd049-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="cd049-199">คุณสามารถสร้างเอนทิตีเสมือนจำนวนมากพร้อมกันได้โดยใช้หน้า **เปลี่ยนหลายเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="cd049-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="cd049-200">เลือกหลายเรกคอร์ดบนหน้า และเลือก **แก้ไข** บน ribbon</span><span class="sxs-lookup"><span data-stu-id="cd049-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="cd049-201">คุณสามารถเปลี่ยนคุณสมบัติ **สร้างขึ้นแล้ว** สำหรับเรกคอร์ดที่เลือกทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="cd049-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![เอนทิตี HR ที่มีอยู่](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="cd049-203">เมื่อต้องการปรับปรุงกระบวนการสร้างเอนทิตีเสมือนในรุ่นต่อไป กระบวนการนี้จะเกิดขึ้นในหน้าในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="cd049-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd049-204">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="cd049-204">See also</span></span>

[<span data-ttu-id="cd049-205">Common Data Service คืออะไร</span><span class="sxs-lookup"><span data-stu-id="cd049-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="cd049-206">ภาพรวมของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd049-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="cd049-207">ภาพรวมความสัมพันธ์ของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd049-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="cd049-208">สร้างและแก้ไขเอนทิตีเสมือนที่มีข้อมูลจากแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="cd049-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="cd049-209">พอร์ทัล Power Apps คืออะไร</span><span class="sxs-lookup"><span data-stu-id="cd049-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="cd049-210">ภาพรวมของการสร้างแอปใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="cd049-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
