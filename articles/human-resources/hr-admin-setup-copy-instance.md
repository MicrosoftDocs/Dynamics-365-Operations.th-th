---
title: คัดลอกอินสแตนซ์
description: คุณสามารถใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อคัดลอกฐานข้อมูล Microsoft Dynamics 365 Human Resources ไปยังสภาพแวดล้อม Sandbox
author: andreabichsel
manager: tfehr
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e38abf3537d88bb147fbf0030999953025e5820f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466915"
---
# <a name="copy-an-instance"></a><span data-ttu-id="ed98d-103">คัดลอกอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="ed98d-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ed98d-104">คุณสามารถใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อคัดลอกฐานข้อมูล Microsoft Dynamics 365 Human Resources ไปยังสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="ed98d-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="ed98d-105">ถ้าคุณมีสภาพแวดล้อม Sandbox อื่นคุณยังสามารถคัดลอกฐานข้อมูลจากสภาพแวดล้อมดังกล่าวไปยังสภาพแวดล้อม Sandbox ที่กำหนดเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="ed98d-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="ed98d-106">เมื่อต้องการคัดลอกอินสแตนซ์ ให้ใช้คำแนะนำต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed98d-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="ed98d-107">อินสแตนซ์ทรัพยากรบุคคลที่คุณต้องการเขียนทับต้องเป็นสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="ed98d-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="ed98d-108">สภาพแวดล้อมที่คุณกำลังคัดลอกมาจากและไปถึง ต้องอยู่ในภูมิภาคเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ed98d-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="ed98d-109">คุณไม่สามารถคัดลอกข้ามภูมิภาคได้</span><span class="sxs-lookup"><span data-stu-id="ed98d-109">You can't copy across regions.</span></span>

- <span data-ttu-id="ed98d-110">คุณต้องเป็นผู้ดูแลระบบในสภาพแวดล้อมเป้าหมายเพื่อให้คุณสามารถลงชื่อเข้าใช้สู่ระบบได้หลังจากการคัดลอกอินสแตนซ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="ed98d-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="ed98d-111">เมื่อคุณคัดลอกฐานข้อมูลทรัพยากรบุคคล คุณจะไม่คัดลอกองค์ประกอบ (แอปหรือข้อมูล) ที่มีอยู่ในสภาพแวดล้อม Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="ed98d-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="ed98d-112">สำหรับข้อมูลเกี่ยวกับการคัดลอกองค์ประกอบในสภาพแวดล้อม Power Apps ให้ดูที่ [คัดลอกสภาพแวดล้อม](https://docs.microsoft.com/power-platform/admin/copy-environment)</span><span class="sxs-lookup"><span data-stu-id="ed98d-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="ed98d-113">สภาพแวดล้อม Power Apps ที่คุณต้องการเขียนทับต้องเป็นสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="ed98d-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="ed98d-114">คุณต้องเป็นผู้ดูแลระบบผู้เช่าทั่วโลกเพื่อเปลี่ยนสภาพแวดล้อมการใช้จริง Power Apps ไปยังสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="ed98d-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="ed98d-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปลี่ยนสภาพแวดล้อม ให้ดู Power Apps [สลับอินสแตนซ์](https://docs.microsoft.com/dynamics365/admin/switch-instance)</span><span class="sxs-lookup"><span data-stu-id="ed98d-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="ed98d-116">ถ้าคุณคัดลอกอินสแตนซ์ไปยังสภาพแวดล้อม Sandbox และต้องการรวมสภาพแวดล้อม Sandbox กับ Dataverseคุณต้องนำฟิลด์ที่กำหนดเองไปใช้กับตาราง Dataverse ใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ed98d-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="ed98d-117">ดูที่ [ใช้ฟิลด์ที่กำหนดเองกับ Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service)</span><span class="sxs-lookup"><span data-stu-id="ed98d-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="ed98d-118">ผลของการคัดลอกฐานข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ed98d-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="ed98d-119">เหตุการณ์ต่อไปนี้เกิดขึ้นเมื่อคุณคัดลอกฐานข้อมูลทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="ed98d-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="ed98d-120">กระบวนการคัดลอกจะลบฐานข้อมูลที่มีอยู่ในสภาพแวดล้อมเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="ed98d-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="ed98d-121">หลังจากที่กระบวนการคัดลอกเสร็จสมบูรณ์แล้ว คุณจะไม่สามารถกู้คืนฐานข้อมูลที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="ed98d-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="ed98d-122">สภาพแวดล้อมเป้าหมายจะไม่พร้อมใช้งานจนกว่ากระบวนการคัดลอกจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ed98d-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="ed98d-123">เอกสารในที่จัดเก็บ Microsoft Azure Blob จะไม่ถูกคัดลอกจากสภาพแวดล้อมหนึ่งไปยังอีกสภาพแวดล้อมหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ed98d-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="ed98d-124">ดังนั้น เอกสารและเท็มเพลตที่แนบจะไม่ถูกคัดลอกและจะยังคงอยู่ในสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ed98d-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="ed98d-125">ผู้ใช้ทั้งหมดยกเว้นผู้ใช้ที่เป็นผู้ดูแลระบบและบัญชีผู้ใช้บริการภายในอื่นๆ จะไม่สามารถใช้งานได้​</span><span class="sxs-lookup"><span data-stu-id="ed98d-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="ed98d-126">ผู้ใช้ที่เป็นผู้ดูแลระบบจึงสามารถลบหรือทำให้ข้อมูลยุ่งเหยิงก่อนที่ผู้ใช้คนอื่นได้รับอนุญาตให้กลับเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="ed98d-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="ed98d-127">ผู้ใช้ผู้ดูแลระบบต้องทำการเปลี่ยนแปลงการตั้งค่าคอนฟิก เช่น การเชื่อมต่อปลายทางการรวมกับบริการหรือ URL เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ed98d-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="ed98d-128">คัดลอกฐานข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ed98d-128">Copy the Human Resources database</span></span>

<span data-ttu-id="ed98d-129">เมื่อต้องการทำงานนี้ให้เสร็จสมบูรณ์ คุณจะคัดลอกอินสแตนซ์ก่อน แล้วลงชื่อเข้าสู่ศูนย์การจัดการ Microsoft Power Platform เพื่อคัดลอกสภาพแวดล้อม Power Apps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed98d-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="ed98d-130">เมื่อคุณคัดลอกอินสแตนซ์ฐาน ข้อมูลจะถูกลบออกในอินสแตนซ์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="ed98d-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="ed98d-131">อินสแตนซ์เป้าหมายไม่พร้อมใช้งานในระหว่างกระบวนการนี้</span><span class="sxs-lookup"><span data-stu-id="ed98d-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="ed98d-132">ลงชื่อเข้าสู่ LCS และเลือกโครงการ LCS ที่มีอินสแตนซ์ที่คุณต้องการคัดลอก</span><span class="sxs-lookup"><span data-stu-id="ed98d-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="ed98d-133">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="ed98d-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="ed98d-134">เลือกอินสแตนซ์ที่จะคัดลอก แล้วเลือก **copy**</span><span class="sxs-lookup"><span data-stu-id="ed98d-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="ed98d-135">ในบานหน้าต่างงาน **คัดลอกอินสแตนซ์** ให้เลือกอินสแตนซ์ที่จะเขียนทับ แล้วเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="ed98d-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="ed98d-136">รอให้มีการอัปเดตค่าของฟิลด์ **สถานะการคัดลอก** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="ed98d-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="ed98d-137">เลือกอินสแตนซ์ที่จะเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="ed98d-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="ed98d-138">เลือก **Power Platform** และลงชื่อเข้าใช้ไปยังศูนย์การจัดการ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="ed98d-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="ed98d-139">เลือก Power Platform</span><span class="sxs-lookup"><span data-stu-id="ed98d-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="ed98d-140">เลือกอินสแตนซ์ Power Apps ที่จะคัดลอก แล้วเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="ed98d-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="ed98d-141">เมื่อกระบวนการคัดลอกเสร็จสมบูรณ์ ให้ลงชื่อเข้าใช้ไปยังอินสแตนซ์เป้าหมาย และเปิดใช้งานการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="ed98d-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="ed98d-142">สำหรับข้อมูลและคำแนะนำเพิ่มเติม ดูที่ [ตั้งค่าคอนฟิกการรวม Dataverse](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration)</span><span class="sxs-lookup"><span data-stu-id="ed98d-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="ed98d-143">องค์ประกอบและสถานะของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed98d-143">Data elements and statuses</span></span>

<span data-ttu-id="ed98d-144">องค์ประกอบข้อมูลต่อไปนี้ไม่ได้รับการคัดลอกเมื่อคุณคัดลอกอินสแตนซ์ทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="ed98d-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="ed98d-145">ที่อยู่อีเมลในตาราง **LogisticsElectronicAddress** </span><span class="sxs-lookup"><span data-stu-id="ed98d-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="ed98d-146">ประวัติชุดงานในตาราง **BatchJobHistory** **BatchHistory** และ **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="ed98d-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="ed98d-147">รหัสผ่าน Mail Transfer Protocol (SMTP) แบบธรรมดาในตาราง **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="ed98d-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="ed98d-148">เซิร์ฟเวอร์สับเปลี่ยน SMTP ในตาราง **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="ed98d-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="ed98d-149">การตั้งค่าการจัดการการพิมพ์ในตาราง **PrintMgmtSettings** และ **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="ed98d-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="ed98d-150">เรกคอร์ดเฉพาะสภาพแวดล้อมในตาราง **SysServerConfig** **SysServerSessions** **SysCorpNetPrinters** **SysClientSessions** **BatchServerConfig** และ **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="ed98d-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="ed98d-151">เอกสารแนบในตาราง DocuValue</span><span class="sxs-lookup"><span data-stu-id="ed98d-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="ed98d-152">เอกสารแนบเหล่านี้รวมถึงเท็มเพลต Microsoft Office ที่ถูกเขียนทับในสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ed98d-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="ed98d-153">สตริงการเชื่อมต่อในตาราง **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="ed98d-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="ed98d-154">องค์ประกอบบางอย่างเหล่านี้ไม่ได้รับการคัดลอกเนื่องจากเป็นองค์ประกอบเฉพาะของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ed98d-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="ed98d-155">ตัวอย่าง ได้แก่ เรกคอร์ด **BatchServerConfig** และ **SysCorpNetPrinters**</span><span class="sxs-lookup"><span data-stu-id="ed98d-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="ed98d-156">องค์ประกอบอื่นๆ ที่ไม่ได้รับการคัดลอก เนื่องจากปริมาณของตั๋วสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="ed98d-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="ed98d-157">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="ed98d-157">For example:</span></span>

- <span data-ttu-id="ed98d-158">อาจมีการส่งอีเมลที่ซ้ำกันเนื่องจาก SMTP ยังคงเปิดใช้งานอยู่ในสภาพแวดล้อมการทดสอบการยอมรับของผู้ใช้ (Sandbox)</span><span class="sxs-lookup"><span data-stu-id="ed98d-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="ed98d-159">อาจมีการส่งข้อความการรวมที่ไม่ถูกต้องเนื่องจากชุดงานยังคงเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="ed98d-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="ed98d-160">ผู้ใช้อาจเปิดใช้งานก่อนที่ผู้ดูแลระบบจะสามารถดำเนินการล้างข้อมูลหลังการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="ed98d-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="ed98d-161">นอกจากนี้ สถานะดังต่อไปนี้จะเปลี่ยนไปเมื่อคุณคัดลอกอินสแตนซ์:</span><span class="sxs-lookup"><span data-stu-id="ed98d-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="ed98d-162">ผู้ใช้ทั้งหมดยกเว้นผู้ดูแลระบบถูกตั้งค่าเป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="ed98d-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="ed98d-163">ชุดงานทั้งหมดยกเว้นงานระบบบางงานจะถูกตั้งค่าเป็น **ระงับ**</span><span class="sxs-lookup"><span data-stu-id="ed98d-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="ed98d-164">รหัสสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ed98d-164">Environment admin</span></span>

<span data-ttu-id="ed98d-165">ผู้ใช้ทั้งหมดในสภาพแวดล้อม Sandbox เป้าหมาย รวมถึงผู้ดูแลระบบ จะถูกแทนที่โดยผู้ใช้ของสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ed98d-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="ed98d-166">ก่อนที่คุณจะคัดลอกอินสแตนซ์ โปรดตรวจสอบให้แน่ใจว่าคุณเป็นผู้ดูแลระบบในสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ed98d-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="ed98d-167">ถ้าคุณไม่ได้ใช้เป็น คุณไม่สามารถลงชื่อเข้าสู่สภาพแวดล้อม Sandbox เป้าหมาย หลังจากที่การคัดลอกเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="ed98d-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="ed98d-168">ผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบทั้งหมดในสภาพแวดล้อม Sandbox เป้าหมายจะถูกปิดใช้งานเพื่อป้องกันไม่ให้มีการลงชื่อเข้าใช้ในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="ed98d-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="ed98d-169">ผู้ดูแลระบบสามารถเป็นผู้ใช้ที่เปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ed98d-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="ed98d-170">ใช้ฟิลด์ที่กำหนดเองกับ Dataverse</span><span class="sxs-lookup"><span data-stu-id="ed98d-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="ed98d-171">ถ้าคุณคัดลอกอินสแตนซ์ไปยังสภาพแวดล้อม Sandbox และต้องการรวมสภาพแวดล้อม Sandbox กับ Dataverseคุณต้องนำฟิลด์ที่กำหนดเองไปใช้กับตาราง Dataverse ใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ed98d-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="ed98d-172">สำหรับแต่ละฟิลด์ที่กำหนดเองที่มีการแสดงในตาราง Dataverse ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed98d-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="ed98d-173">ไปที่ฟิลด์ที่กำหนดเองและเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ed98d-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="ed98d-174">ยกเลิกการเลือกฟิลด์ **เปิดใช้งานแล้ว** สำหรับแต่ละเอนทิตี้ cdm_ \* ซึ่งเปิดใช้งานฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ed98d-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="ed98d-175">เลือก **ใช้การเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="ed98d-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="ed98d-176">เลือก **แก้ไข** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ed98d-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="ed98d-177">เลือกฟิลด์ **เปิดใช้งานแล้ว** สำหรับแต่ละเอนทิตี้ cdm_ \* ซึ่งเปิดใช้งานฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ed98d-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="ed98d-178">เลือก **ใช้การเปลี่ยนแปลง** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ed98d-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="ed98d-179">กระบวนการยกเลิกการเลือก การใช้การเปลี่ยนแปลง การเลือกใหม่ และการใช้การเปลี่ยนแปลงอีกครั้งจะพร้อมท์ Schema เพื่ออัพเดตใน Dataverse ให้รวมฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ed98d-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="ed98d-180">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟิลด์ที่กำหนดเอง ให้ดูที่ [สร้างและทำงานกับฟิลด์ที่กำหนดเอง](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)</span><span class="sxs-lookup"><span data-stu-id="ed98d-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed98d-181">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ed98d-181">See also</span></span>

[<span data-ttu-id="ed98d-182">เตรียมใช้งาน Human Resources</span><span class="sxs-lookup"><span data-stu-id="ed98d-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="ed98d-183">เอาอินสแตนซ์ออก</span><span class="sxs-lookup"><span data-stu-id="ed98d-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="ed98d-184">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="ed98d-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]