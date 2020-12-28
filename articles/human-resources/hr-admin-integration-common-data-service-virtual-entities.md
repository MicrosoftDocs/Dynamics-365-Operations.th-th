---
title: ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service
description: หัวข้อนี้แสดงวิธีการตั้งค่าคอนฟิกเอนทิตีเสมือนสำหรับ Dynamics 365 Human Resources สร้างและอัพเดตข้อมูลเอนทิตีเสมือนที่มีอยู่ และวิเคราะห์เอนทิตีที่สร้างและพร้อมใช้งาน
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645612"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="4e3eb-104">ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4e3eb-105">Dynamics 365 Human Resources เป็นแหล่งข้อมูลเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="4e3eb-106">ซึ่งให้การดำเนินการส้ราง อ่าน อัปเดต และลบทั้งหมด (CRUD) จาก Common Data Service และ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="4e3eb-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="4e3eb-107">ข้อมูลสำหรับเอนทิตีเสมือนไม่ได้จัดเก็บไว้ใน Common Data Service แต่อยู่ในฐานข้อมูลใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="4e3eb-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="4e3eb-108">เมื่อต้องการเปิดใช้งานการดำเนินงาน CRUD บนเอนทิตีทรัพยากรบุคคลจาก Common Data Service คุณต้องทำให้เอนทิตีพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4e3eb-109">ซึ่งช่วยให้คุณสามารถทำการดำเนินงาน CRUD จาก Common Data Service และ Microsoft Power Platform บนข้อมูลที่อยู่ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="4e3eb-110">การดำเนินงานยังสนับสนุนการตรวจสอบตรรกะทางธุรกิจทั้งหมดของทรัพยากรบุคคล เพื่อให้มั่นใจในความสมบูรณ์ของข้อมูลเมื่อเขียนข้อมูลไปยังเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4e3eb-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="4e3eb-111">เอนทิตีเสมือนพร้อมใช้งานสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="4e3eb-112">เอนทิตี Open Data Protocol (OData) ทั้งหมดในทรัพยากรบุคคลพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4e3eb-113">นอกจากนี้ยังพร้อมใช้งานใน Power Platform ด้วย</span><span class="sxs-lookup"><span data-stu-id="4e3eb-113">They're also available in Power Platform.</span></span> <span data-ttu-id="4e3eb-114">ขณะนี้ คุณสามารถสร้างแอปและประสบการณ์พร้อมกับข้อมูลโดยตรงจากทรัพยากรบุคคลที่มีความสามารถ CRUD เต็มที่ โดยไม่มีการคัดลอกหรือการซิงโครไนส์ข้อมูลไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="4e3eb-115">คุณสามารถใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งเปิดใช้งานสถานการณ์การทำงานร่วมกันสำหรับกระบวนการทางธุรกิจในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="4e3eb-116">คุณสามารถดูรายการเอนทิตีเสมือนที่เปิดใช้งานในสภาพแวดล้อม และเริ่มต้นการทำงานกับเอนทิตีใน [Power Apps](https://make.powerapps.com) ในโซลูชัน **เอนทิตีเสมือนของ Dynamics 365 HR**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![เอนทิตีเสมือนของ Dynamics 365 HR ใน Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="4e3eb-118">เอนทิตีเสมือนกับเอนทิตีธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="4e3eb-119">เอนทิตีเสมือนสำหรับทรัพยากรบุคคลไม่เหมือนกับเอนทิตี Common Data Service ธรรมชาติที่สร้างขึ้นสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="4e3eb-120">เอนทิตีธรรมชาติสำหรับทรัพยากรบุคคลสร้างขึ้นแยกต่างหาก และรักษาไว้ในโซลูชันทั่วไปของ HCM ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="4e3eb-121">ด้วยเอนทิตีธรรมชาติ ข้อมูลจะถูกจัดเก็บไว้ใน Common Data Service และต้องมีการซิงโครไนส์กับฐานข้อมูลใบสมัครทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="4e3eb-122">สำหรับรายการของเอนทิตี Common Data Service ธรรมชาติสำหรับทรัพยากรบุคคล ให้ดูที่ [เอนทีตี Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="4e3eb-123">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="4e3eb-123">Setup</span></span>

<span data-ttu-id="4e3eb-124">ทำตามขั้นตอนการตั้งค่าต่อไปนี้เพื่อเปิดใช้งานเอนทิตีเสมือนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="4e3eb-125">เปิดใช้งานเอนทิตีเสมือนในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e3eb-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="4e3eb-126">ก่อนอื่นคุณต้องเปิดใช้งานเอนทิตีเสมือนในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="4e3eb-127">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="4e3eb-128">เลือกไทล์ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="4e3eb-129">เลือก **การสนับสนุนเอนทิตีเสมือนใน HR/CDS** แล้วจากนั้น เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="4e3eb-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานและการปิดใช้งานคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="4e3eb-131">ลงทะเบียนแอปใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="4e3eb-132">คุณต้องลงทะเบียนอินสแตนซ์ทรัพยากรบุคคลของคุณในพอร์ทัล Azure เพื่อให้แพลตฟอร์มข้อมูลเฉพาะของ Microsoft สามารถให้บริการการรับรองความถูกต้องและการตรวจสอบความถูกต้องสำหรับแอปและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4e3eb-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="4e3eb-133">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนแอปใน Azure ดูที่ [การเริ่มต้นแบบด่วน: ลงทะเบียนโปรแกรมประยุกต์ด้วยฟอร์มข้อมูลเฉพาะของ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="4e3eb-134">เปิด [พอร์ทัล Microsoft Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="4e3eb-135">ในรายการบริการ Azure เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="4e3eb-136">เลือก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-136">Select **New registration**.</span></span>

4. <span data-ttu-id="4e3eb-137">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="4e3eb-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="4e3eb-138">ตัวอย่างเช่น **เอนทีตีเสมือน Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="4e3eb-139">ในฟิลด์ **เปลี่ยนเส้นทาง URI** ให้ป้อน URL พื้นที่ว่างในชื่อของอินสแตนซ์ของทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="4e3eb-140">เลือก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-140">Select **Register**.</span></span>

7. <span data-ttu-id="4e3eb-141">เมื่อลงทะเบียนเสร็จสมบูรณ์แล้ว พอร์ทัล Azure จะแสดงบานหน้าต่าง **ภาพรวม** ของการลงทะเบียนของแอป ซึ่งรวมถึง **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="4e3eb-142">จด **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="4e3eb-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="4e3eb-143">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="4e3eb-144">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบรับรองและข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="4e3eb-145">ในส่วน **ข้อมูลลับของไคลเอนต์** ของหน้า ให้เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="4e3eb-146">ระบุคำอธิบาย เลือกช่วงเวลา และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="4e3eb-147">บันทึกค่าของข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-147">Record the secret's value.</span></span> <span data-ttu-id="4e3eb-148">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4e3eb-149">ตรวจสอบให้แน่ใจว่าได้จดบันทึกค่าของข้อมูลลับไว้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="4e3eb-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="4e3eb-150">ข้อมูลลับจะไม่มีการแสดงอีกครั้งหลังจากที่คุณออกจากหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4e3eb-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="4e3eb-151">ติดตั้งแอป Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="4e3eb-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="4e3eb-152">ติดตั้งแอป Dynamics 365 HR Virtual Entity ในสภาพแวดล้อม Power Apps ของคุณ เพื่อจัดวางแพคเกจโซลูชันเอนทิตีเสมือนไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="4e3eb-153">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4e3eb-154">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4e3eb-155">ในส่วน **ทรัพยากร** ของหน้า ให้เลือก **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="4e3eb-156">เลือกการดำเนินการ **ติดตั้งแอป**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="4e3eb-157">เลือก **Dynamics 365 HR Virtual Entity** และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="4e3eb-158">ตรวจทานและทำเครื่องหมายเพื่อยอมรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="4e3eb-159">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-159">Select **Install**.</span></span>

<span data-ttu-id="4e3eb-160">การติดตั้งใช้เวลาสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="4e3eb-160">The install takes a few minutes.</span></span> <span data-ttu-id="4e3eb-161">เมื่อเสร็จสิ้น ให้ดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="4e3eb-161">When it completes, continue to the next steps.</span></span>

![ติดตั้งแอป Dynamics 365 HR Virtual Entity จากศูนย์การจัดการ Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="4e3eb-163">ตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="4e3eb-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="4e3eb-164">ขั้นตอนต่อไปคือการตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือนในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="4e3eb-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="4e3eb-165">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4e3eb-166">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4e3eb-167">เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="4e3eb-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="4e3eb-168">ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้าโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="4e3eb-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="4e3eb-169">บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **การตั้งค่าคอนฟิกแหล่งข้อมูลเสมือน Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="4e3eb-170">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-170">Select **Results**.</span></span>

7. <span data-ttu-id="4e3eb-171">เลือกเรกคอร์ด **แหล่งข้อมูล Microsoft HR**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="4e3eb-172">ป้อนข้อมูลที่จำเป็นสำหรับการตั้งค่าคอนฟิกแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="4e3eb-173">**URL เป้าหมาย**: URL ของพื้นที่ว่างในชื่อทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="4e3eb-174">รูปแบบของ URL เป้าหมายคือ:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="4e3eb-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="4e3eb-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="4e3eb-176">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="4e3eb-177">ตรวจสอบให้แน่ใจว่าได้รวมอักขระ "**/**" เมื่อสิ้นสุด URL เพื่อหลีกเลี่ยงการรับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="4e3eb-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="4e3eb-178">**รหัสผู้เช่า**: รหัสผู้เช่า Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="4e3eb-179">**รหัสโปรแกรมประยุกต์ AAD**: รหัสโปรแกรมประยุกต์ (ไคลเอนต์) ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4e3eb-180">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="4e3eb-181">**ข้อมูลลับโปรแกรมประยุกต์ AAD**: ข้อมูลลับของไคลเอนต์ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4e3eb-182">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="4e3eb-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![แหล่งข้อมูล Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="4e3eb-184">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="4e3eb-185">ให้สิทธิ์แอปใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="4e3eb-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="4e3eb-186">ให้สิทธิสำหรับใบสมัคร Azure AD สองใบในทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="4e3eb-187">แอปที่สร้างขึ้นสำหรับผู้เช่าของคุณในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="4e3eb-188">แอป Dynamics 365 HR Virtual Entity ที่ติดตั้งในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="4e3eb-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="4e3eb-189">ในทรัพยากรบุคคล ให้เปิดหน้า **ใบสมัคร Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="4e3eb-190">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครใหม่:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="4e3eb-191">ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4e3eb-192">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4e3eb-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4e3eb-193">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="4e3eb-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="4e3eb-194">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครที่สอง:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="4e3eb-195">**รหัสไคลเอนต์**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="4e3eb-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="4e3eb-196">**ชื่อ**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="4e3eb-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="4e3eb-197">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="4e3eb-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="4e3eb-198">สร้างคอนฟิกเอนทิตีเสมือน</span><span class="sxs-lookup"><span data-stu-id="4e3eb-198">Generate virtual entities</span></span>

<span data-ttu-id="4e3eb-199">เมื่อการตั้งค่าเสร็จสมบูรณ์ คุณสามารถเลือกเอนทิตีเสมือนที่คุณต้องการสร้างและเปิดใช้งานในอินสแตนซ์ Common Data Service ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="4e3eb-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="4e3eb-200">ในทรัพยากรบุคคล ให้เปิดหน้า **การรวม Common Data Service (CDS)**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="4e3eb-201">เลือกแท็บ **เอนทิตีเสมือน**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="4e3eb-202">การสลับ **เปิดใช้งานเอนทิตีเสมือน** จะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติเมื่อการตั้งค่าที่จำเป็นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="4e3eb-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="4e3eb-203">ถ้าการสลับถูกตั้งค่าเป็น **ไม่ใช่** ให้ตรวจสอบขั้นตอนในหัวข้อก่อนหน้านี้ของเอกสารนี้ เพื่อให้แน่ใจว่าการตั้งค่าข้อกำหนดเบื้องต้นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="4e3eb-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="4e3eb-204">เลือกเอนทิตีหรือเอนทิตีมากกว่าหนึ่งที่คุณต้องการสร้าง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="4e3eb-205">เลือก **สร้าง/รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-205">Select **Generate/refresh**.</span></span>

![การรวม Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="4e3eb-207">ตรวจสอบสถานะการสร้างเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4e3eb-207">Check entity generation status</span></span>

<span data-ttu-id="4e3eb-208">เอนทิตีเสมือนมีการสร้างใน Common Data Service โดยผ่านกระบวนการพื้นหลังแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="4e3eb-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="4e3eb-209">การอัปเดตในกระบวนการแสดงในศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="4e3eb-210">รายละเอียดเกี่ยวกับกระบวนการ รวมถึงล็อกข้อผิดพลาด จะปรากฏในหน้า **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="4e3eb-211">ในทรัพยากรบุคคล ให้เปิดเพจรายการ **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="4e3eb-212">เลือกแท็บ **กระบวนการแบบเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="4e3eb-213">เลือก **กระบวนการแบบเบื้องหลังของการดำเนินงานแบบอะซิงโครนัสในการสำรวจเอนทิตีเสมือน**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="4e3eb-214">เลือก **ดูผลลัพธ์ล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="4e3eb-214">Select **View most recent results**.</span></span>

<span data-ttu-id="4e3eb-215">บานหน้าต่าง slideout แสดงผลลัพธ์การดำเนินการล่าสุดสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="4e3eb-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="4e3eb-216">คุณสามารถดูล็อกสำหรับกระบวนการ รวมถึงข้อผิดพลาดที่ส่งคืนจาก Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4e3eb-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e3eb-217">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4e3eb-217">See also</span></span>

[<span data-ttu-id="4e3eb-218">Common Data Service คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4e3eb-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="4e3eb-219">ภาพรวมของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4e3eb-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="4e3eb-220">ภาพรวมความสัมพันธ์ของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4e3eb-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="4e3eb-221">สร้างและแก้ไขเอนทิตีเสมือนที่มีข้อมูลจากแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="4e3eb-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="4e3eb-222">พอร์ทัล Power Apps คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4e3eb-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="4e3eb-223">ภาพรวมของการสร้างแอปใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="4e3eb-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
