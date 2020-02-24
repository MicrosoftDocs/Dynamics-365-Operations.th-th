---
title: คัดลอกอินสแตนซ์
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010684"
---
# <a name="copy-an-instance"></a><span data-ttu-id="4f7b1-102">คัดลอกอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="4f7b1-102">Copy an instance</span></span>

<span data-ttu-id="4f7b1-103">คุณสามารถใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อคัดลอกฐานข้อมูล Microsoft Dynamics 365 Human Resources ไปยังสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="4f7b1-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="4f7b1-104">ถ้าคุณมีสภาพแวดล้อม Sandbox อื่นคุณยังสามารถคัดลอกฐานข้อมูลจากสภาพแวดล้อมดังกล่าวไปยังสภาพแวดล้อม Sandbox ที่กำหนดเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="4f7b1-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="4f7b1-105">เมื่อต้องการคัดลอกอินสแตนซ์ คุณต้องตรวจสอบให้แน่ใจว่าตามข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f7b1-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="4f7b1-106">อินสแตนซ์ทรัพยากรบุคคลที่คุณต้องการเขียนทับต้องเป็นสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="4f7b1-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="4f7b1-107">สภาพแวดล้อมที่คุณกำลังคัดลอกมาจากและไปถึง ต้องอยู่ในภูมิภาคเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4f7b1-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="4f7b1-108">คุณไม่สามารถคัดลอกข้ามภูมิภาคได้</span><span class="sxs-lookup"><span data-stu-id="4f7b1-108">You can't copy across regions.</span></span>

- <span data-ttu-id="4f7b1-109">คุณต้องเป็นผู้ดูแลระบบในสภาพแวดล้อมเป้าหมายเพื่อให้คุณสามารถลงชื่อเข้าใช้สู่ระบบได้หลังจากการคัดลอกอินสแตนซ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="4f7b1-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="4f7b1-110">เมื่อคุณคัดลอกฐานข้อมูลทรัพยากรบุคคล คุณจะไม่คัดลอกองค์ประกอบ (แอปหรือข้อมูล) ที่มีอยู่ในสภาพแวดล้อม Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="4f7b1-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="4f7b1-111">สำหรับข้อมูลเกี่ยวกับการคัดลอกองค์ประกอบในสภาพแวดล้อม PowerApps ให้ดูที่ [คัดลอกสภาพแวดล้อม](https://docs.microsoft.com/power-platform/admin/copy-environment)</span><span class="sxs-lookup"><span data-stu-id="4f7b1-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="4f7b1-112">สภาพแวดล้อม PowerApps ที่คุณต้องการเขียนทับต้องเป็นสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="4f7b1-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="4f7b1-113">คุณต้องเป็นผู้ดูแลระบบผู้เช่าทั่วโลกเพื่อเปลี่ยนสภาพแวดล้อมการใช้จริง PowerApps ไปยังสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="4f7b1-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="4f7b1-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปลี่ยนสภาพแวดล้อม ให้ดู PowerApps [สลับอินสแตนซ์](https://docs.microsoft.com/dynamics365/admin/switch-instance)</span><span class="sxs-lookup"><span data-stu-id="4f7b1-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="4f7b1-115">ผลของการคัดลอกฐานข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4f7b1-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="4f7b1-116">เหตุการณ์ต่อไปนี้เกิดขึ้นเมื่อคุณคัดลอกฐานข้อมูลทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="4f7b1-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="4f7b1-117">กระบวนการคัดลอกจะลบฐานข้อมูลที่มีอยู่ในสภาพแวดล้อมเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="4f7b1-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="4f7b1-118">หลังจากที่กระบวนการคัดลอกเสร็จสมบูรณ์แล้ว คุณจะไม่สามารถกู้คืนฐานข้อมูลที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="4f7b1-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="4f7b1-119">สภาพแวดล้อมเป้าหมายจะไม่พร้อมใช้งานจนกว่ากระบวนการคัดลอกจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4f7b1-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="4f7b1-120">เอกสารในที่จัดเก็บ Microsoft Azure Blob จะไม่ถูกคัดลอกจากสภาพแวดล้อมหนึ่งไปยังอีกสภาพแวดล้อมหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4f7b1-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="4f7b1-121">ดังนั้น เอกสารและเท็มเพลตที่แนบจะไม่ถูกคัดลอกและจะยังคงอยู่ในสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4f7b1-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="4f7b1-122">ผู้ใช้ทั้งหมดยกเว้นผู้ใช้ที่เป็นผู้ดูแลระบบและบัญชีผู้ใช้บริการภายในอื่นๆ จะไม่สามารถใช้งานได้​</span><span class="sxs-lookup"><span data-stu-id="4f7b1-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="4f7b1-123">ดังนั้นผู้ใช้ผู้ดูแลระบบจึงสามารถลบหรือทำให้ข้อมูลยุ่งเหยิงก่อนที่ผู้ใช้คนอื่นได้รับอนุญาตให้กลับเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="4f7b1-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="4f7b1-124">ผู้ใช้ผู้ดูแลระบบต้องทำการเปลี่ยนแปลงการตั้งค่าคอนฟิก เช่น การเชื่อมต่อปลายทางการรวมกับบริการหรือ URL เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4f7b1-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="4f7b1-125">คัดลอกฐานข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4f7b1-125">Copy the Human Resources database</span></span>

<span data-ttu-id="4f7b1-126">เมื่อต้องการทำงานนี้ให้เสร็จสมบูรณ์ คุณจะคัดลอกอินสแตนซ์ก่อน แล้วลงชื่อเข้าสู่ศูนย์การจัดการ Microsoft Power Platform เพื่อคัดลอกสภาพแวดล้อม PowerApps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4f7b1-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="4f7b1-127">เมื่อคุณคัดลอกอินสแตนซ์ฐาน ข้อมูลจะถูกลบออกในอินสแตนซ์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="4f7b1-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="4f7b1-128">อินสแตนซ์เป้าหมายไม่พร้อมใช้งานในระหว่างกระบวนการนี้</span><span class="sxs-lookup"><span data-stu-id="4f7b1-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="4f7b1-129">ลงชื่อเข้าสู่ LCS และเลือกโครงการ LCS ที่มีอินสแตนซ์ที่คุณต้องการคัดลอก</span><span class="sxs-lookup"><span data-stu-id="4f7b1-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="4f7b1-130">ในโครงการ LCS ของคุณ เลือกไทล์ **การจัดการแอป Human Resources**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="4f7b1-131">เลือกอินสแตนซ์ที่จะคัดลอก แล้วเลือก **copy**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="4f7b1-132">ในบานหน้าต่างงาน **คัดลอกอินสแตนซ์** ให้เลือกอินสแตนซ์ที่จะเขียนทับ แล้วเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="4f7b1-133">รอให้มีการอัปเดตค่าของฟิลด์ **สถานะการคัดลอก** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="4f7b1-134">เลือกอินสแตนซ์ที่จะเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="4f7b1-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="4f7b1-135">เลือก **Power Platform** และลงชื่อเข้าใช้ไปยังศูนย์การจัดการ Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="4f7b1-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="4f7b1-136">เลือก Power Platform</span><span class="sxs-lookup"><span data-stu-id="4f7b1-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="4f7b1-137">เลือกอินสแตนซ์ PowerApps ที่จะคัดลอก แล้วเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="4f7b1-138">เมื่อกระบวนการคัดลอกเสร็จสมบูรณ์ ให้ลงชื่อเข้าใช้ไปยังอินสแตนซ์เป้าหมาย และเปิดใช้งานการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f7b1-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="4f7b1-139">สำหรับข้อมูลและคำแนะนำเพิ่มเติม ดูที่ [ตั้งค่าคอนฟิกการรวม Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration)</span><span class="sxs-lookup"><span data-stu-id="4f7b1-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="4f7b1-140">องค์ประกอบและสถานะของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f7b1-140">Data elements and statuses</span></span>

<span data-ttu-id="4f7b1-141">องค์ประกอบข้อมูลต่อไปนี้ไม่ได้รับการคัดลอกเมื่อคุณคัดลอกอินสแตนซ์ทรัพยากรบุคคล:</span><span class="sxs-lookup"><span data-stu-id="4f7b1-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="4f7b1-142">ที่อยู่อีเมลในตาราง **LogisticsElectronicAddress** </span><span class="sxs-lookup"><span data-stu-id="4f7b1-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="4f7b1-143">ประวัติชุดงานในตาราง **BatchJobHistory** **BatchHistory** และ **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="4f7b1-144">รหัสผ่าน Mail Transfer Protocol (SMTP) แบบธรรมดาในตาราง **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="4f7b1-145">เซิร์ฟเวอร์สับเปลี่ยน SMTP ในตาราง **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="4f7b1-146">การตั้งค่าการจัดการการพิมพ์ในตาราง **PrintMgmtSettings** และ **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="4f7b1-147">เรกคอร์ดเฉพาะสภาพแวดล้อมในตาราง **SysServerConfig** **SysServerSessions** **SysCorpNetPrinters** **SysClientSessions** **BatchServerConfig** และ **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="4f7b1-148">เอกสารแนบในตาราง DocuValue</span><span class="sxs-lookup"><span data-stu-id="4f7b1-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="4f7b1-149">เอกสารแนบเหล่านี้รวมถึงเท็มเพลต Microsoft Office ที่ถูกเขียนทับในสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4f7b1-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="4f7b1-150">สตริงการเชื่อมต่อในตาราง **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="4f7b1-151">องค์ประกอบบางอย่างเหล่านี้ไม่ได้รับการคัดลอกเนื่องจากเป็นองค์ประกอบเฉพาะของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="4f7b1-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="4f7b1-152">ตัวอย่าง ได้แก่ เรกคอร์ด **BatchServerConfig** และ **SysCorpNetPrinters**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="4f7b1-153">องค์ประกอบอื่นๆ ที่ไม่ได้รับการคัดลอก เนื่องจากปริมาณของตั๋วสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4f7b1-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="4f7b1-154">ตัวอย่างเช่น อาจมีการส่งอีเมลที่ซ้ำกันเนื่องจาก SMTP ยังคงเปิดใช้งานอยู่ในสภาพแวดล้อมการทดสอบ (Sandbox) การยอมรับของผู้ใช้ อาจมีการส่งข้อความการรวมที่ไม่ถูกต้องเนื่องจากชุดงานยังคงเปิดใช้งานอยู่ และอาจเปิดใช้งานผู้ใช้ก่อนที่ผู้ดูแลระบบสามารถดำเนินการล้างข้อมูลหลังการรีเฟรชได้</span><span class="sxs-lookup"><span data-stu-id="4f7b1-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="4f7b1-155">นอกจากนี้ สถานะดังต่อไปนี้จะเปลี่ยนไปเมื่อคุณคัดลอกอินสแตนซ์:</span><span class="sxs-lookup"><span data-stu-id="4f7b1-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="4f7b1-156">ผู้ใช้ทั้งหมดยกเว้นผู้ดูแลระบบถูกตั้งค่าเป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="4f7b1-157">ชุดงานทั้งหมดยกเว้นงานระบบบางงานจะถูกตั้งค่าเป็น **ระงับ**</span><span class="sxs-lookup"><span data-stu-id="4f7b1-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="4f7b1-158">รหัสสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="4f7b1-158">Environment admin</span></span>

<span data-ttu-id="4f7b1-159">ผู้ใช้ทั้งหมดในสภาพแวดล้อม Sandbox เป้าหมาย รวมถึงผู้ดูแลระบบ จะถูกแทนที่โดยผู้ใช้ของสภาพแวดล้อมต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4f7b1-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="4f7b1-160">ก่อนที่คุณจะคัดลอกอินสแตนซ์ โปรดตรวจสอบให้แน่ใจว่าคุณเป็นผู้ดูแลระบบในสภาพแวดล้อมเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="4f7b1-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="4f7b1-161">ถ้าคุณไม่ได้ใช้ คุณจะไม่สามารถลงชื่อเข้าสู่สภาพแวดล้อม Sandbox เป้าหมาย หลังจากที่การคัดลอกเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="4f7b1-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="4f7b1-162">ผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบทั้งหมดในสภาพแวดล้อม Sandbox เป้าหมายจะถูกปิดใช้งานเพื่อป้องกันไม่ให้มีการลงชื่อเข้าใช้ในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="4f7b1-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="4f7b1-163">ผู้ดูแลระบบสามารถเป็นผู้ใช้ที่เปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="4f7b1-163">Administrators can reenable users if needed.</span></span>
