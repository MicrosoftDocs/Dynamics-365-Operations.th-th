---
title: ตั้งค่าคอนฟิกตารางเสมือน Dataverse
description: หัวข้อนี้แสดงวิธีการตั้งค่าคอนฟิกตารางเสมือนสำหรับ Dynamics 365 Human Resources สร้างและอัพเดตข้อมูลตารางเสมือนที่มีอยู่ และวิเคราะห์ตารางที่สร้างและพร้อมใช้งาน
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
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae36f1436ddd7f41bf0c3510b47cbc440224f484
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890063"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="adaaa-104">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="adaaa-105">Dynamics 365 Human Resources เป็นแหล่งข้อมูลเสมือนใน Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="adaaa-106">ซึ่งให้การดำเนินการส้ราง อ่าน อัปเดต และลบทั้งหมด (CRUD) จาก Dataverse และ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="adaaa-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="adaaa-107">ข้อมูลสำหรับตารางเสมือนไม่ได้จัดเก็บไว้ใน Dataverse แต่อยู่ในฐานข้อมูลใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="adaaa-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="adaaa-108">เมื่อต้องการเปิดใช้งานการดำเนินงาน CRUD บนเอนทิตีทรัพยากรบุคคลจาก Dataverse คุณต้องทำให้เอนทิตีพร้อมใช้งานเป็นตารางเสมือนใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="adaaa-109">ซึ่งช่วยให้คุณสามารถทำการดำเนินงาน CRUD จาก Dataverse และ Microsoft Power Platform บนข้อมูลที่อยู่ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="adaaa-110">การดำเนินงานยังสนับสนุนการตรวจสอบตรรกะทางธุรกิจทั้งหมดของทรัพยากรบุคคล เพื่อให้มั่นใจในความสมบูรณ์ของข้อมูลเมื่อเขียนข้อมูลไปยังเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="adaaa-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="adaaa-111">เอนทิตี Human Resources จะสอดคล้องกับตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="adaaa-112">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="adaaa-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="adaaa-113">ตารางเสมือนพร้อมใช้งานสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="adaaa-114">เอนทิตี Open Data Protocol (OData) ทั้งหมดในทรัพยากรบุคคลพร้อมใช้งานเป็นตารางเสมือนใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="adaaa-115">นอกจากนี้ยังพร้อมใช้งานใน Power Platform ด้วย</span><span class="sxs-lookup"><span data-stu-id="adaaa-115">They're also available in Power Platform.</span></span> <span data-ttu-id="adaaa-116">ขณะนี้ คุณสามารถสร้างแอปและประสบการณ์พร้อมกับข้อมูลโดยตรงจากทรัพยากรบุคคลที่มีความสามารถ CRUD เต็มที่ โดยไม่มีการคัดลอกหรือการซิงโครไนส์ข้อมูลไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="adaaa-117">คุณสามารถใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งเปิดใช้งานสถานการณ์การทำงานร่วมกันสำหรับกระบวนการทางธุรกิจในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="adaaa-118">คุณสามารถดูรายการตารางเสมือนที่เปิดใช้งานในสภาพแวดล้อม และเริ่มต้นการทำงานกับตารางใน [Power Apps](https://make.powerapps.com) ในโซลูชัน **ตารางเสมือนของ Dynamics 365 HR**</span><span class="sxs-lookup"><span data-stu-id="adaaa-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![ตารางเสมือนของ Dynamics 365 HR ใน Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="adaaa-120">ตารางเสมือนเทียบกับตารางดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="adaaa-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="adaaa-121">ตารางเสมือนสำหรับทรัพยากรบุคคลไม่เหมือนกับตาราง Dataverse ธรรมชาติที่สร้างขึ้นสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="adaaa-122">ตารางธรรมชาติสำหรับทรัพยากรบุคคลสร้างขึ้นแยกต่างหาก และรักษาไว้ในโซลูชันทั่วไปของ HCM ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="adaaa-123">ด้วยตารางธรรมชาติ ข้อมูลจะถูกจัดเก็บไว้ใน Dataverse และต้องมีการซิงโครไนส์กับฐานข้อมูลใบสมัครทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="adaaa-124">สำหรับรายการของตาราง Dataverse ธรรมชาติสำหรับทรัพยากรบุคคล ให้ดูที่ [ตาราง Dataverse](./hr-developer-entities.md)</span><span class="sxs-lookup"><span data-stu-id="adaaa-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="adaaa-125">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="adaaa-125">Setup</span></span>

<span data-ttu-id="adaaa-126">ทำตามขั้นตอนการตั้งค่าต่อไปนี้เพื่อเปิดใช้งานตารางเสมือนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="adaaa-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="adaaa-127">เปิดใช้งานตารางเสมือนในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="adaaa-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="adaaa-128">ก่อนอื่นคุณต้องเปิดใช้งานตารางเสมือนในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="adaaa-129">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="adaaa-130">เลือกไทล์ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="adaaa-131">เลือก **การสนับสนุนตารางเสมือนสำหรับ HR ใน Dataverse** แล้วจากนั้น เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="adaaa-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="adaaa-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานและการปิดใช้งานคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="adaaa-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="adaaa-133">ลงทะเบียนแอปใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="adaaa-134">คุณต้องลงทะเบียนอินสแตนซ์ทรัพยากรบุคคลของคุณในพอร์ทัล Azure เพื่อให้แพลตฟอร์มข้อมูลเฉพาะของ Microsoft สามารถให้บริการการรับรองความถูกต้องและการตรวจสอบความถูกต้องสำหรับแอปและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="adaaa-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="adaaa-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนแอปใน Azure ดูที่ [การเริ่มต้นแบบด่วน: ลงทะเบียนโปรแกรมประยุกต์ด้วยฟอร์มข้อมูลเฉพาะของ Microsoft](/azure/active-directory/develop/quickstart-register-app)</span><span class="sxs-lookup"><span data-stu-id="adaaa-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="adaaa-136">เปิด [พอร์ทัล Microsoft Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="adaaa-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="adaaa-137">ในรายการบริการ Azure เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="adaaa-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="adaaa-138">เลือก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="adaaa-138">Select **New registration**.</span></span>

4. <span data-ttu-id="adaaa-139">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="adaaa-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="adaaa-140">ตัวอย่างเช่น **ตารางเสมือน Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="adaaa-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="adaaa-141">ในฟิลด์ **เปลี่ยนเส้นทาง URI** ให้ป้อน URL พื้นที่ว่างในชื่อของอินสแตนซ์ของทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="adaaa-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="adaaa-142">เลือก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="adaaa-142">Select **Register**.</span></span>

7. <span data-ttu-id="adaaa-143">เมื่อลงทะเบียนเสร็จสมบูรณ์แล้ว พอร์ทัล Azure จะแสดงบานหน้าต่าง **ภาพรวม** ของการลงทะเบียนของแอป ซึ่งรวมถึง **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="adaaa-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="adaaa-144">จด **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="adaaa-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="adaaa-145">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลตารางเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)</span><span class="sxs-lookup"><span data-stu-id="adaaa-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="adaaa-146">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบรับรองและข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="adaaa-147">ในส่วน **ข้อมูลลับของไคลเอนต์** ของหน้า ให้เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="adaaa-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="adaaa-148">ระบุคำอธิบาย เลือกช่วงเวลา และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="adaaa-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="adaaa-149">บันทึกค่าของข้อมูลลับจากคุณสมบัติ **ค่า** ของตาราง</span><span class="sxs-lookup"><span data-stu-id="adaaa-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="adaaa-150">คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลตารางเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)</span><span class="sxs-lookup"><span data-stu-id="adaaa-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="adaaa-151">ตรวจสอบให้แน่ใจว่าได้จดบันทึกค่าของข้อมูลลับไว้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="adaaa-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="adaaa-152">ข้อมูลลับจะไม่มีการแสดงอีกครั้งหลังจากที่คุณออกจากหน้านี้</span><span class="sxs-lookup"><span data-stu-id="adaaa-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="adaaa-153">ติดตั้งแอปตารางเสมือน Dynamics 365 HR</span><span class="sxs-lookup"><span data-stu-id="adaaa-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="adaaa-154">ติดตั้งแอปตารางเสมือน Dynamics 365 HR ในสภาพแวดล้อม Power Apps ของคุณ เพื่อจัดวางแพคเกจโซลูชันตารางเสมือนไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="adaaa-155">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="adaaa-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="adaaa-156">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="adaaa-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="adaaa-157">ในส่วน **ทรัพยากร** ของหน้า ให้เลือก **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="adaaa-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="adaaa-158">เลือกการดำเนินการ **ติดตั้งแอป**</span><span class="sxs-lookup"><span data-stu-id="adaaa-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="adaaa-159">เลือก **ตารางเสมือน Dynamics 365 HR** และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="adaaa-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="adaaa-160">ตรวจทานและทำเครื่องหมายเพื่อยอมรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="adaaa-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="adaaa-161">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="adaaa-161">Select **Install**.</span></span>

<span data-ttu-id="adaaa-162">การติดตั้งใช้เวลาสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="adaaa-162">The install takes a few minutes.</span></span> <span data-ttu-id="adaaa-163">เมื่อเสร็จสิ้น ให้ดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="adaaa-163">When it completes, continue to the next steps.</span></span>

![ติดตั้งแอปตารางเสมือน Dynamics 365 HR จากศูนย์การจัดการ Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="adaaa-165">ตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="adaaa-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="adaaa-166">ขั้นตอนต่อไปคือการตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับตารางเสมือนในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="adaaa-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="adaaa-167">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="adaaa-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="adaaa-168">ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="adaaa-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="adaaa-169">เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="adaaa-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="adaaa-170">ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้าโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="adaaa-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="adaaa-171">บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **การตั้งค่าคอนฟิกแหล่งข้อมูลเสมือน Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="adaaa-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="adaaa-172">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="adaaa-172">Select **Results**.</span></span>

7. <span data-ttu-id="adaaa-173">เลือกเรกคอร์ด **แหล่งข้อมูล Microsoft HR**</span><span class="sxs-lookup"><span data-stu-id="adaaa-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="adaaa-174">ป้อนข้อมูลที่จำเป็นสำหรับการตั้งค่าคอนฟิกแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="adaaa-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="adaaa-175">**URL เป้าหมาย**: URL ของพื้นที่ว่างในชื่อทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="adaaa-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="adaaa-176">รูปแบบของ URL เป้าหมายคือ:</span><span class="sxs-lookup"><span data-stu-id="adaaa-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="adaaa-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="adaaa-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="adaaa-178">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="adaaa-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="adaaa-179">ตรวจสอบให้แน่ใจว่าได้รวมอักขระ "**/**" เมื่อสิ้นสุด URL เพื่อหลีกเลี่ยงการรับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="adaaa-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="adaaa-180">**รหัสผู้เช่า**: รหัสผู้เช่า Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="adaaa-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="adaaa-181">**รหัสโปรแกรมประยุกต์ AAD**: รหัสโปรแกรมประยุกต์ (ไคลเอนต์) ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="adaaa-182">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="adaaa-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="adaaa-183">**ข้อมูลลับโปรแกรมประยุกต์ AAD**: ข้อมูลลับของไคลเอนต์ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="adaaa-184">คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)</span><span class="sxs-lookup"><span data-stu-id="adaaa-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![แหล่งข้อมูล Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="adaaa-186">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="adaaa-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="adaaa-187">ให้สิทธิ์แอปใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="adaaa-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="adaaa-188">ให้สิทธิสำหรับใบสมัคร Azure AD สองใบในทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="adaaa-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="adaaa-189">แอปที่สร้างขึ้นสำหรับผู้เช่าของคุณในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="adaaa-190">แอปตารางเสมือน Dynamics 365 HR ที่ติดตั้งในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="adaaa-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="adaaa-191">ในทรัพยากรบุคคล ให้เปิดหน้า **ใบสมัคร Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="adaaa-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="adaaa-192">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครใหม่:</span><span class="sxs-lookup"><span data-stu-id="adaaa-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="adaaa-193">ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="adaaa-194">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="adaaa-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="adaaa-195">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="adaaa-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="adaaa-196">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครที่สอง:</span><span class="sxs-lookup"><span data-stu-id="adaaa-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="adaaa-197">**รหัสไคลเอนต์**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="adaaa-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="adaaa-198">**ชื่อ**: ตารางเสมือน Dynamics 365 HR</span><span class="sxs-lookup"><span data-stu-id="adaaa-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="adaaa-199">ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="adaaa-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="adaaa-200">สร้างคอนฟิกตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="adaaa-200">Generate virtual tables</span></span>

<span data-ttu-id="adaaa-201">เมื่อการตั้งค่าเสร็จสมบูรณ์ คุณสามารถเลือกตารางเสมือนที่คุณต้องการสร้างและเปิดใช้งานในอินสแตนซ์ Dataverse ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="adaaa-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="adaaa-202">ในทรัพยากรบุคคล ให้เปิดหน้า **การรวม Dataverse**</span><span class="sxs-lookup"><span data-stu-id="adaaa-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="adaaa-203">เลือกแท็บ **ตารางเสมือน**</span><span class="sxs-lookup"><span data-stu-id="adaaa-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="adaaa-204">การสลับ **เปิดใช้งานตารางเสมือน** จะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติเมื่อการตั้งค่าที่จำเป็นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="adaaa-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="adaaa-205">ถ้าการสลับถูกตั้งค่าเป็น **ไม่ใช่** ให้ตรวจสอบขั้นตอนในหัวข้อก่อนหน้านี้ของเอกสารนี้ เพื่อให้แน่ใจว่าการตั้งค่าข้อกำหนดเบื้องต้นทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="adaaa-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="adaaa-206">เลือกตารางหรือตารางมากกว่าหนึ่งที่คุณต้องการสร้าง Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="adaaa-207">เลือก **สร้าง/รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="adaaa-207">Select **Generate/refresh**.</span></span>

![การรวม Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="adaaa-209">ตรวจสอบสถานะการสร้างตาราง</span><span class="sxs-lookup"><span data-stu-id="adaaa-209">Check table generation status</span></span>

<span data-ttu-id="adaaa-210">ตารางเสมือนมีการสร้างใน Dataverse โดยผ่านกระบวนการพื้นหลังแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="adaaa-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="adaaa-211">การอัปเดตในกระบวนการแสดงในศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="adaaa-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="adaaa-212">รายละเอียดเกี่ยวกับกระบวนการ รวมถึงล็อกข้อผิดพลาด จะปรากฏในหน้า **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="adaaa-213">ในทรัพยากรบุคคล ให้เปิดเพจรายการ **กระบวนการระบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="adaaa-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="adaaa-214">เลือกแท็บ **กระบวนการแบบเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="adaaa-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="adaaa-215">เลือก **กระบวนการแบบเบื้องหลังของการดำเนินงานแบบอะซิงโครนัสในการสำรวจตารางเสมือน**</span><span class="sxs-lookup"><span data-stu-id="adaaa-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="adaaa-216">เลือก **ดูผลลัพธ์ล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="adaaa-216">Select **View most recent results**.</span></span>

<span data-ttu-id="adaaa-217">บานหน้าต่าง slideout แสดงผลลัพธ์การดำเนินการล่าสุดสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="adaaa-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="adaaa-218">คุณสามารถดูล็อกสำหรับกระบวนการ รวมถึงข้อผิดพลาดที่ส่งคืนจาก Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="adaaa-219">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="adaaa-219">See also</span></span>

[<span data-ttu-id="adaaa-220">Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="adaaa-220">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="adaaa-221">ตารางใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="adaaa-221">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="adaaa-222">ภาพรวมความสัมพันธ์ของตาราง</span><span class="sxs-lookup"><span data-stu-id="adaaa-222">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="adaaa-223">สร้างและแก้ไขตารางเสมือนที่มีข้อมูลจากแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="adaaa-223">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="adaaa-224">พอร์ทัล Power Apps คืออะไร</span><span class="sxs-lookup"><span data-stu-id="adaaa-224">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="adaaa-225">ภาพรวมของการสร้างแอปใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="adaaa-225">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]