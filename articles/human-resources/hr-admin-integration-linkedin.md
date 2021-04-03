---
title: รวมกับฮับความสามารถพิเศษของ LinkedIn
description: หัวข้อนี้อธิบายวิธีตั้งค่าการรวมระหว่าง Microsoft Dynamics 365 Human Resources และรวมกับฮับความสามารถพิเศษของของ LinkedIn
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a017d67177bcbee86abf920cf8d83f37312c5eb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465209"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="3bb88-103">รวมกับฮับความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3bb88-104">[ฮับความสามารถพิเศษของของ LinkedIn](https://business.linkedin.com/talent-solutions/talent-hub) เป็นแพลตฟอร์มของระบบติดตามผู้สมัคร (ATS)</span><span class="sxs-lookup"><span data-stu-id="3bb88-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="3bb88-105">ซึ่งช่วยให้คุณสามารถจัดหา จัดการ และจ้างงานพนักงานทั้งหมดได้ในที่เดียว</span><span class="sxs-lookup"><span data-stu-id="3bb88-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="3bb88-106">โดยการรวม Microsoft Dynamics 365 Human Resources เข้ากับฮับความสามารถพิเศษของของ LinkedIn คุณสามารถสร้างเรกคอร์ดพนักงานในทรัพยากรบุคคลสำหรับผู้สมัครที่ได้รับการว่าจ้างสำหรับตำแหน่งได้</span><span class="sxs-lookup"><span data-stu-id="3bb88-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="3bb88-107">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3bb88-107">Setup</span></span>

<span data-ttu-id="3bb88-108">ผู้ดูแลระบบต้องทำงานการติดตั้งให้เสร็จสมบูรณ์ เพื่อเปิดใช้งานการรวมกับฮับความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="3bb88-109">อันดับแรก ในสภาพแวดล้อม Power Apps คุณต้องตั้งค่าผู้ใช้และบทบาทความปลอดภัยเพื่อให้มีสิทธิการได้รับอนุญาตที่เหมาะสมกับฮับความสามารถพิเศษของ LinkedIn ในการเขียนข้อมูลลงในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3bb88-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="3bb88-110">เชื่อมโยงสภาพแวดล้อมของคุณกับฮับความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="3bb88-111">เปิด [ฮับความสามารถพิเศษของ LinkedIn](https://business.linkedin.com/talent-solutions/talent-hub)</span><span class="sxs-lookup"><span data-stu-id="3bb88-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="3bb88-112">บนเมนูแบบหล่นลงของผู้ใช้ ให้เลือก **การตั้งค่าผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="3bb88-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="3bb88-113">ในบานหน้าต่างนำทางซ้าย ในส่วน **ขั้นสูง** ให้เลือก **การรวม**</span><span class="sxs-lookup"><span data-stu-id="3bb88-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="3bb88-114">เลือก **อนุมัติ** สำหรับการรวม Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3bb88-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="3bb88-115">บนหน้า **Dynamics 365 Human Resources** ให้เลือกสภาพแวดล้อมที่จะเชื่อมโยงฮับความสามารถของ LinkedIn เข้า แล้วเลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="3bb88-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![การเตรียมความพร้อมสำหรับฮับความสามารถพิเศษของ LinkedIn](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="3bb88-117">คุณสามารถเชื่อมโยงกับสภาพแวดล้อมที่บัญชีผู้ใช้ของคุณมีสิทธิการเข้าถึงผู้ดูแลระบบทั้งในสภาพแวดล้อมของฝ่ายทรัพยากรบุคคลและสภาพแวดล้อม Power Apps ที่เกี่ยวข้องเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3bb88-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="3bb88-118">ถ้าไม่มีสภาพแวดล้อมที่แสดงรายการอยู่บนหน้าลิงค์ของฝ่ายทรัพยากรบุคคล โปรดตรวจสอบให้แน่ใจว่าคุณมีสิทธิการได้รับอนุญาตให้ใช้งานในสภาพแวดล้อมของฝ่ายทรัพยากรบุคคลในผู้เช่า และผู้ใช้ที่คุณลงชื่อเข้าสู่หน้าลิงค์มีสิทธิการได้รับอนุญาตของผู้ดูแลระบบทั้งในสภาพแวดล้อมของฝ่ายทรัพยากรบุคคลและสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="3bb88-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="3bb88-119">สร้างบทบาทความปลอดภัยของ Power Apps</span><span class="sxs-lookup"><span data-stu-id="3bb88-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="3bb88-120">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="3bb88-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3bb88-121">ในรายการของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อมที่สัมพันธ์กับสภาพแวดล้อมของทรัพยากรบุคคลที่คุณต้องการเชื่อมโยงกับอินสแตนซ์ของความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="3bb88-122">เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3bb88-122">Select **Settings**.</span></span>

4. <span data-ttu-id="3bb88-123">ขยายโหนด **ผู้ใช้ + สิทธิ์** และเลือก **บทบาทความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="3bb88-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="3bb88-124">บนหน้า **บทบาทความปลอดภัย** บนแถบเครื่องมือ ให้เลือก **บทบาทใหม่**</span><span class="sxs-lookup"><span data-stu-id="3bb88-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="3bb88-125">บนแท็บ **รายละเอียด** ให้ป้อนชื่อสำหรับบทบาท เช่น **การรวม HRIS ของฮับความสามารถพิเศษของ LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="3bb88-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="3bb88-126">บนแท็บ **การกำหนดเอง** ให้เลือกสิทธิ์ **การอ่าน** ระดับองค์กรสำหรับเอนทิตี้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3bb88-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="3bb88-127">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3bb88-127">Entity</span></span>
    - <span data-ttu-id="3bb88-128">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3bb88-128">Field</span></span>
    - <span data-ttu-id="3bb88-129">ความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="3bb88-129">Relationship</span></span>

8. <span data-ttu-id="3bb88-130">บันทึกและปิดบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3bb88-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="3bb88-131">สร้างผู้ใช้แอพลิเคชัน Power Apps</span><span class="sxs-lookup"><span data-stu-id="3bb88-131">Create a Power Apps application user</span></span>

<span data-ttu-id="3bb88-132">ผู้ใช้แอพลิเคชันต้องสร้างสำหรับตัวปรับต่อฮับความสามารถพิเศษของ LinkedIn เพื่อให้สิทธิ์แก่ตัวปรับต่อ เพื่อเขียนเรกคอร์ดผู้สมัครเข้าในสภาพแวดล้อม Power Apps</span><span class="sxs-lookup"><span data-stu-id="3bb88-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="3bb88-133">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="3bb88-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3bb88-134">ในรายการของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อมที่สัมพันธ์กับสภาพแวดล้อมของทรัพยากรบุคคลที่คุณต้องการเชื่อมโยงกับอินสแตนซ์ของความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="3bb88-135">เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3bb88-135">Select **Settings**.</span></span>

4. <span data-ttu-id="3bb88-136">ขยายโหนด **ผู้ใช้ + สิทธิ์** และเลือก **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3bb88-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="3bb88-137">เลือก **จัดการผู้ใช้ใน Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="3bb88-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="3bb88-138">ใช้เมนูแบบเลื่อนลงเหนือรายการเพื่อเปลี่ยนมุมมองจากมุมมอง **ผู้ใช้ที่เปิดใช้งาน** เริ่มต้นเป็น **ผู้ใช้แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3bb88-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![มุมมองผู้ใช้แอพลิเคชัน](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="3bb88-140">บนแถบเครื่องมือ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3bb88-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="3bb88-141">ในหน้า **ผู้ใช้ใหม่** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3bb88-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="3bb88-142">เปลี่ยนค่าของฟิลด์ **ชนิดผู้ใช้** เป็น **ผู้ใช้แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3bb88-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="3bb88-143">ตั้งค่าฟิลด์ **ชื่อผู้ใช้** เป็น **การรวม HRIS ของ Dynamics365 HR LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="3bb88-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="3bb88-144">ตั้งค่าฟิลด์ **รหัสแอพลิเคชัน** เป็น **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**</span><span class="sxs-lookup"><span data-stu-id="3bb88-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="3bb88-145">ป้อนค่าใดๆ ในฟิลด์ **ชื่อ** **นามสกุล** และ **อีเมลหลัก**</span><span class="sxs-lookup"><span data-stu-id="3bb88-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="3bb88-146">ในแถบเครื่องมือ เลือก **บันทึก \& ปิด**</span><span class="sxs-lookup"><span data-stu-id="3bb88-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="3bb88-147">การกำหนดบทบาทความปลอดภัยให้กับผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3bb88-147">Assign a security role to the new user</span></span>

<span data-ttu-id="3bb88-148">หลังจากที่คุณบันทึกและปิดผู้ใช้แอพลิเคชันใหม่ในส่วนก่อนหน้านี้แล้ว คุณจะถูกส่งกลับไปที่หน้า **รายการผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3bb88-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="3bb88-149">ในหน้า **รายการผู้ใช้** ให้เปลี่ยนมุมมองเป็น **ผู้ใช้แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3bb88-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="3bb88-150">เลือกผู้ใช้แอพลิเคชันที่คุณสร้างขึ้นในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3bb88-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="3bb88-151">บนแถบเครื่องมือ ให้เลือก **จัดการบทบาท**</span><span class="sxs-lookup"><span data-stu-id="3bb88-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="3bb88-152">เลือกบทบาทความปลอดภัยที่คุณสร้างไว้ก่อนหน้านี้สำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="3bb88-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="3bb88-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bb88-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="3bb88-154">เพิ่มแอป Azure Active Directory ใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="3bb88-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="3bb88-155">ใน Dynamics 365 Human Resources ให้เปิดหน้า **ใบสมัคร Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="3bb88-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="3bb88-156">เพิ่มเรกคอร์ดใหม่ไปยังรายการ และตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3bb88-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="3bb88-157">**รหัสไคลเอนต์**: ป้อน **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**</span><span class="sxs-lookup"><span data-stu-id="3bb88-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="3bb88-158">**ชื่อ**: ให้ป้อนชื่อของบทบาทความปลอดภัย Power Apps ที่คุณสร้างไว้ก่อนหน้านี้ เช่น **การรวม HRIS ของฮับความสามารถพิเศษของ LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="3bb88-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="3bb88-159">**รหัสผู้ใช้**: เลือกผู้ใช้ที่มีสิทธิ์ในการเขียนข้อมูลในการจัดการบุคลากร</span><span class="sxs-lookup"><span data-stu-id="3bb88-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="3bb88-160">สร้างตารางใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3bb88-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bb88-161">การรวมฮับความสามารถพิเศษของ LinkedIn จะขึ้นอยู่กับตารางเสมือนใน Dataverse สำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3bb88-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="3bb88-162">ในฐานะที่เป็นข้อกำหนดเบื้องต้นสำหรับขั้นตอนนี้ในการตั้งค่า คุณต้องตั้งค่าคอนฟิกตารางเสมือน</span><span class="sxs-lookup"><span data-stu-id="3bb88-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="3bb88-163">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกตารางเสมือน ให้ดูที่ [ตั้งค่าคอนฟิกตารางเสมือน Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)</span><span class="sxs-lookup"><span data-stu-id="3bb88-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="3bb88-164">ในทรัพยากรบุคคล ให้เปิดหน้า **การรวม Dataverse**</span><span class="sxs-lookup"><span data-stu-id="3bb88-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="3bb88-165">เลือกแท็บ **ตารางเสมือน**</span><span class="sxs-lookup"><span data-stu-id="3bb88-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="3bb88-166">กรองรายการเอนทิตีตามป้ายชื่อเอนทิตีเพื่อค้นหา **ผู้สมัครที่ส่งออก LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="3bb88-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="3bb88-167">เลือกเอนทิตี แล้วเลือก **สร้าง/รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="3bb88-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="3bb88-168">การส่งออกเรกคอร์ดผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="3bb88-168">Exporting candidate records</span></span>

<span data-ttu-id="3bb88-169">หลังจากที่การตั้งค่าเสร็จสิ้นแล้ว ผู้เชี่ยวชาญด้านการสรรหาบุคลากรและทรัพยากรบุคคล (HR) จะสามารถใช้ฟังก์ชัน **ส่งออกไปยัง HRIS** ในฮับความสามารถพิเศษของ LinkedIn เพื่อส่งออกเรกคอร์ดผู้สมัครที่ได้รับการว่าจ้างจากฮับความสามารถพิเศษของ LinkedIn ไปยังทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3bb88-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="3bb88-170">ส่งออกเรกคอร์ดจากฮับความสามารถพิเศษของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="3bb88-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="3bb88-171">หลังจากที่ผู้สมัครได้ย้ายผ่านกระบวนการสรรหาบุคลากรและได้รับการว่าจ้างแล้ว คุณสามารถส่งออกเรกคอร์ดผู้สมัครจากฮับความสามารถพิเศษของ LinkedIn ไปที่ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3bb88-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="3bb88-172">ในฮับความสามารถพิเศษของ LinkedIn ให้เปิดโครงการที่คุณได้จ้างงานให้กับพนักงานใหม่</span><span class="sxs-lookup"><span data-stu-id="3bb88-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="3bb88-173">เลือกเรกคอร์ดผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="3bb88-173">Select a candidate record.</span></span>

3. <span data-ttu-id="3bb88-174">เลือก **เปลี่ยนขั้น** และจากนั้น เลือก **ได้รับการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="3bb88-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="3bb88-175">บนเมนูจุดไข่ปลา (**...**) สำหรับผู้สมัคร เลือก **ส่งออกไปที่ HRIS**</span><span class="sxs-lookup"><span data-stu-id="3bb88-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="3bb88-176">ในบานหน้าต่าง **ส่งออกไปยัง HRIS** ให้ป้อนข้อมูลที่ต้องส่งออก:</span><span class="sxs-lookup"><span data-stu-id="3bb88-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="3bb88-177">ในฟิลด์ของ **ผู้ให้บริการ HRIS** เลือก **Microsoft Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="3bb88-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="3bb88-178">ในฟิลด์ **วันเริ่มต้น** เลือกค่าสำหรับพนักงานใหม่</span><span class="sxs-lookup"><span data-stu-id="3bb88-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="3bb88-179">ในฟิลด์ **ตำแหน่งงาน** ให้ป้อนตำแหน่งงานสำหรับงานของพนักงานใหม่</span><span class="sxs-lookup"><span data-stu-id="3bb88-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="3bb88-180">ในฟิลด์ **ที่ตั้ง** ให้ป้อนที่ตั้งที่พนักงานจะใช้ในการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3bb88-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="3bb88-181">ให้ป้อนหรือตรวจสอบที่อยู่อีเมลของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3bb88-181">Enter or verify the employee's email address.</span></span>

![ส่งออกไปยังบานหน้าต่าง HRIS ในฮับความสามารถพิเศษของ LinkedIn](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="3bb88-183">การปฐมนิเทศให้เสร็จสมบูรณ์ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3bb88-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="3bb88-184">เรกคอร์ดผู้สมัครที่ส่งออกจากฮับความสามารถพิเศษของ LinkedIn ไปยังทรัพยากรบุคคลจะปรากฏในส่วน **ผู้สมัครเพื่อจ้างงาน** ของหน้า **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="3bb88-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="3bb88-185">ในทรัพยากรบุคคล ให้เปิดหน้า **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="3bb88-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="3bb88-186">ในส่วน **ผู้สมัครที่จะจ้างงาน** ให้เลือก **จ้าง** สำหรับผู้สมัครที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3bb88-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="3bb88-187">ในกล่องโต้ตอบ **จ้างผู้ปฏิบัติงานใหม่** ให้ทบทวนเรกคอร์ด และเพิ่มข้อมูลที่จำเป็นใดๆ</span><span class="sxs-lookup"><span data-stu-id="3bb88-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="3bb88-188">นอกจากนี้คุณยังสามารถเลือกหมายเลขตำแหน่งที่มีการจ้างงานผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="3bb88-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="3bb88-189">หลังจากที่ป้อนข้อมูลที่จำเป็นแล้ว คุณสามารถดำเนินการกับกระบวนการมาตรฐานสำหรับการสร้างเรกคอร์ดพนักงานและพนักงานการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="3bb88-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="3bb88-190">รายละเอียดต่อไปนี้จะถูกนำเข้าและรวมอยู่ในเรกคอร์ดพนักงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="3bb88-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="3bb88-191">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3bb88-191">First name</span></span>
- <span data-ttu-id="3bb88-192">นามสกุล</span><span class="sxs-lookup"><span data-stu-id="3bb88-192">Last name</span></span>
- <span data-ttu-id="3bb88-193">วันที่เริ่มต้นการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="3bb88-193">Employment start date</span></span>
- <span data-ttu-id="3bb88-194">ที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="3bb88-194">Email address</span></span>
- <span data-ttu-id="3bb88-195">หมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="3bb88-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="3bb88-196">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3bb88-196">See also</span></span>

[<span data-ttu-id="3bb88-197">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="3bb88-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="3bb88-198">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3bb88-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]