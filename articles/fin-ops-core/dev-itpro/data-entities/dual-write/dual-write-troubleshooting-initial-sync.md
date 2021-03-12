---
title: แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744648"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="a5bfa-103">แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a5bfa-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="a5bfa-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a5bfa-105">กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5bfa-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="a5bfa-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a5bfa-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a5bfa-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="a5bfa-108">ตรวจสอบข้อผิดพลาดของการซิงโครไนส์เริ่มต้นในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bfa-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="a5bfa-109">หลังจากที่คุณเปิดใช้งานเท็มเพลตการแม็ป สถานะของแผนที่ควรเป็น **กำลังรัน**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="a5bfa-110">ถ้าสถานะ **ไม่ได้รันอยู่** ข้อผิดพลาดเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="a5bfa-111">เมื่อต้องการดูข้อผิดพลาด ให้เลือกแท็บ **รายละเอียดการซิงค์เริ่มต้น** บนหน้า **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![ข้อผิดพลาดในแท็บรายละเอียดการซิงค์เริ่มต้น](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="a5bfa-113">คุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้: 400 คำขอไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a5bfa-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="a5bfa-114">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a5bfa-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a5bfa-115">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามรันการแม็ปและการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="a5bfa-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="a5bfa-116">*(\[คำขอไม่ถูกต้อง\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="a5bfa-117">นี่เป็นตัวอย่างของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a5bfa-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="a5bfa-118">ถ้าเกิดข้อผิดพลาดนี้อย่างสม่ำเสมอ และคุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้ ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="a5bfa-119">ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bfa-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="a5bfa-120">เปิด Microsoft Management Console</span><span class="sxs-lookup"><span data-stu-id="a5bfa-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="a5bfa-121">ในบานหน้าต่าง **บริการ** ตรวจสอบให้แน่ใจว่ามีการเรียกใช้บริการกรอบงานการนำเข้าการส่งออกข้อมูล Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a5bfa-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="a5bfa-122">เริ่มต้นใหม่ ถ้าถูกหยุดเนื่องจากการซิงโครไนส์เริ่มต้นต้องการ</span><span class="sxs-lookup"><span data-stu-id="a5bfa-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="a5bfa-123">ข้อผิดพลาดการซิงโครไนส์เริ่มต้น: 403 ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="a5bfa-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="a5bfa-124">คุณอาจได้รับข้อความแสดงข้อผิดพลาดในระหว่างการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="a5bfa-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="a5bfa-125">*(\[ไม่ได้รับอนุญาต\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="a5bfa-126">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a5bfa-127">ลงชื่อเข้าใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bfa-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="a5bfa-128">บนหน้า **แอพลิเคชัน Azure Active Directory** ให้ลบไคลเอนต์ **DtAppID** และจากนั้น เพิ่มใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a5bfa-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![ไคลเอนต์ DtAppID ในรายการของแอพลิเคชัน Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="a5bfa-130">ความล้มเหลวในการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียนในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="a5bfa-131">คุณอาจได้รับข้อความแสดงข้อผิดพลาด ถ้าการแม็ปใดๆ ของคุณมีการอ้างอิงตนเองหรือการอ้างอิงหมุนเวียน</span><span class="sxs-lookup"><span data-stu-id="a5bfa-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="a5bfa-132">ข้อผิดพลาดจะอยู่ในประเภทเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a5bfa-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="a5bfa-133">ข้อผิดพลาดในผู้จัดจำหน่าย V2–สำหรับ–การแม็ปตาราง msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="a5bfa-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="a5bfa-134">ข้อผิดพลาดในลูกค้า V3–สำหรับ–การแม็ปตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="a5bfa-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="a5bfa-135">แก้ไขข้อผิดพลาดในผู้จัดจำหน่าย V2–สำหรับ–การแม็ปตาราง msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="a5bfa-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="a5bfa-136">คุณอาจพบข้อผิดพลาดในการซิงโครไนส์เริ่มต้นสำหรับการแม็ปของ **ผู้จัดจำหน่าย V2** สำหรับ **msdyn\_vendors** ถ้าตารางมีแถวที่มีอยู่ที่ซึ่งมีค่าในคอลัมน์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="a5bfa-137">ข้อผิดพลาดเหล่านี้เกิดขึ้นเนื่องจาก **InvoiceVendorAccountNumber** เป็นคอลัมน์ที่อ้างอิงถึงตนเอง และ **PrimaryContactPersonId** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a5bfa-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a5bfa-138">ข้อความแสดงข้อผิดพลาดที่คุณได้รับจะมีฟอร์มต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="a5bfa-139">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: \<field\> ไม่พบการค้นหา: \<value\> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="a5bfa-140">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-140">Here are some examples:</span></span>

- <span data-ttu-id="a5bfa-141">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="a5bfa-142">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber ไม่พบการค้นหา: V24-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="a5bfa-143">ถ้าแถวใดๆ ในตารางของผู้จัดจำหน่ายมีค่าในคอลัมน์ **PrimaryContactPersonId** และ **InvoiceVendorAccountNumber** ให้ทำตามขั้นตอนเหล่านี้เพื่อทำให้การซิงโครไนส์เริ่มต้นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a5bfa-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="a5bfa-144">ในแอป Finance and Operations ให้ลบคอลัมน์ **PrimaryContactPersonId** และคอลัมน์ **InvoiceVendorAccountNumber** จากการแม็ป และจากนั้น บันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="a5bfa-145">บนหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** บนแท็บ **การแม็ปตาราง** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations apps.Vendors V2**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="a5bfa-146">ในตัวกรองสิทธิ์ เลือก **Sales.Vendor**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="a5bfa-147">ค้นหา **primarycontactperson** เพื่อค้นหาคอลัมน์ต้นทาง **PrimaryContactPersonId**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="a5bfa-148">เลือก **การดำเนินการ** แล้วจากนั้น เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-148">Select **Actions**, and then select **Delete**.</span></span>

        ![การลบคอลัมน์ PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="a5bfa-150">ทำซ้ำขั้นตอนเหล่านี้เพื่อลบคอลัมน์ **InvoiceVendorAccountNumber**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![การลบคอลัมน์ InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="a5bfa-152">บันทึกการเปลี่ยนแปลงของคุณไปยังการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="a5bfa-153">ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับตาราง **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="a5bfa-154">ในพื้นที่ทำงาน **การจัดการข้อมูล** เลือกไทล์ **ตารางข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="a5bfa-155">เลือกตาราง **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="a5bfa-156">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวเลือก** แล้วจากนั้น เลือก **การติดตามการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![การเลือกตัวเลือกการติดตามการเปลี่ยนแปลง](media/selfref_options.png)

    4. <span data-ttu-id="a5bfa-158">เลือก **ปิดใช้งานการติดตามการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-158">Select **Disable Change Tracking**.</span></span>

        ![การเลือกปิดใช้งานการติดตามการเปลี่ยนแปลง](media/selfref_tracking.png)

3. <span data-ttu-id="a5bfa-160">รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="a5bfa-161">การซิงโครไนส์เริ่มต้นควรรันเสร็จเรียบร้อย โดยไม่มีข้อผิดพลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="a5bfa-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="a5bfa-162">รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="a5bfa-163">คุณต้องซิงค์การแม็ปนี้ ถ้าคุณต้องการซิงค์คอลัมน์ผู้ติดต่อหลักบนตารางของผู้จัดจำหน่าย เนื่องจากยังต้องทำการซิงโครไนส์เริ่มต้นสำหรับแถวผู้ติดต่อด้วย</span><span class="sxs-lookup"><span data-stu-id="a5bfa-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="a5bfa-164">เพิ่มคอลัมน์ **PrimaryContactPersonId** และคอลัมน์ **InvoiceVendorAccountNumber** กลับไปยังการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)** และจากนั้น บันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="a5bfa-165">รันการซิงโครไนส์เริ่มต้นอีกครั้งสำหรับการแม็ป **ผู้จัดจำหน่าย V2 (msdyn\_vendors)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="a5bfa-166">เนื่องจากมีการปิดใช้งานการติดตามการเปลี่ยนแปลง แถวทั้งหมดจะถูกซิงค์</span><span class="sxs-lookup"><span data-stu-id="a5bfa-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="a5bfa-167">เปิดการติดตามการเปลี่ยนแปลงอีกครั้งสำหรับตาราง **ผู้จัดจำหน่าย V2**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="a5bfa-168">แก้ไขข้อผิดพลาดในลูกค้า V3–สำหรับ–การแม็ปตารางบัญชี</span><span class="sxs-lookup"><span data-stu-id="a5bfa-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="a5bfa-169">คุณอาจพบข้อผิดพลาดในการซิงโครไนส์เริ่มต้นสำหรับการแม็ปของ **ลูกค้า V3** ไปยัง **บัญชี** ถ้าตารางมีแถวที่มีอยู่ที่ซึ่งมีค่าในคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="a5bfa-170">ข้อผิดพลาดเหล่านี้เกิดขึ้นเนื่องจาก **InvoiceAccount** เป็นคอลัมน์ที่อ้างอิงตนเอง และ **ContactPersonID** เป็นการอ้างอิงหมุนเวียนในการแม็ปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a5bfa-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a5bfa-171">ข้อความแสดงข้อผิดพลาดที่คุณได้รับจะมีฟอร์มต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="a5bfa-172">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: \<field\> ไม่พบการค้นหา: \<value\> ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="a5bfa-173">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="a5bfa-173">Here are some examples:</span></span>

- <span data-ttu-id="a5bfa-174">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: primarycontactid.msdyn\_contactpersonid ไม่พบการค้นหา: 000056 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="a5bfa-175">*ไม่สามารถแก้ไข guid สำหรับฟิลด์: msdyn\_billingaccount.accountnumber ไม่พบการค้นหา: 1206-1 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="a5bfa-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="a5bfa-176">ถ้าแถวใดๆ ในตารางของลูกค้ามีค่าในคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount** ให้ทำตามขั้นตอนเหล่านี้เพื่อทำให้การซิงโครไนส์เริ่มต้นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a5bfa-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="a5bfa-177">คุณสามารถใช้วิธีการนี้สำหรับตารางแบบสำเร็จรูปใดๆ เช่น **บัญชี** และ **ผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="a5bfa-178">ในแอป Finance and Operations ลบคอลัมน์ **ContactPersonID** และคอลัมน์ **InvoiceAccount** จากการแม็ป **ลูกค้า V3 (บัญชี)** และจากนั้น บันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="a5bfa-179">บนหน้าการแม็ปการรวมแบบสองทิศทางสำหรับ **ลูกค้า V3 (บัญชี)** บนแท็บ **การแม็ปตาราง** ในตัวกรองด้านซ้าย ให้เลือก **Finance and Operations app.Customers V3**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="a5bfa-180">ในตัวกรองสิทธิ์ เลือก **Dataverse.Account**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="a5bfa-181">ค้นหา **contactperson** เพื่อค้นหาคอลัมน์ต้นทาง **ContactPersonID**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="a5bfa-182">เลือก **การดำเนินการ** แล้วจากนั้น เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-182">Select **Actions**, and then select **Delete**.</span></span>

        ![การลบคอลัมน์ ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="a5bfa-184">ทำซ้ำขั้นตอนเหล่านี้เพื่อลบคอลัมน์ **InvoiceAccount**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![การลบคอลัมน์ InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="a5bfa-186">บันทึกการเปลี่ยนแปลงของคุณไปยังการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="a5bfa-187">ปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับตาราง **ลูกค้า V3**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="a5bfa-188">ในพื้นที่ทำงาน **การจัดการข้อมูล** เลือกไทล์ **ตารางข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="a5bfa-189">เลือกตาราง **ลูกค้า V3**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="a5bfa-190">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวเลือก** แล้วจากนั้น เลือก **การติดตามการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![การเลือกตัวเลือกการติดตามการเปลี่ยนแปลง](media/selfref_options.png)

    4. <span data-ttu-id="a5bfa-192">เลือก **ปิดใช้งานการติดตามการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-192">Select **Disable Change Tracking**.</span></span>

        ![การเลือกปิดใช้งานการติดตามการเปลี่ยนแปลง](media/selfref_tracking.png)

3. <span data-ttu-id="a5bfa-194">รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ลูกค้า V3 (บัญชี)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a5bfa-195">การซิงโครไนส์เริ่มต้นควรรันเสร็จเรียบร้อย โดยไม่มีข้อผิดพลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="a5bfa-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="a5bfa-196">รันการซิงโครไนส์เริ่มต้นสำหรับการแม็ป **ผู้ติดต่อของ CDS V2 (ผู้ติดต่อ)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a5bfa-197">มีแผนที่สองรายการที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a5bfa-197">There are two maps that have the same name.</span></span> <span data-ttu-id="a5bfa-198">ตรวจสอบให้แน่ใจว่าได้เลือกแม็ปที่มีคำอธิบายต่อไปนี้บนแท็บ **รายละเอียด**: **แม่แบบการรวมแบบสองทิศทางสำหรับการซิงค์ระหว่าง FO.CDS Vendor Contacts V2 ไปยัง CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\]**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="a5bfa-199">เพิ่มคอลัมน์ **InvoiceAccount** และคอลัมน์ **ContactPersonId** กลับไปยังการแม็ป **ลูกค้า V3 (บัญชี)** และจากนั้น บันทึกการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a5bfa-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="a5bfa-200">ตอนนี้ทั้งคอลัมน์ **InvoiceAccount** และคอลัมน์ **ContactPersonId** เป็นส่วนหนึ่งของโหมดการซิงโครไนส์ที่เริ่มใช้งานจริงอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a5bfa-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="a5bfa-201">ในขั้นตอนถัดไป คุณจะดำเนินการซิงค์เริ่มต้นสำหรับคอลัมน์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="a5bfa-202">รันการซิงโครไนส์เริ่มต้นอีกครั้งสำหรับการแม็ป **ลูกค้า V3 (บัญชี)**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a5bfa-203">เนื่องจากการติดตามการเปลี่ยนแปลงถูกปิด จะมีการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จากแอป Finance and Operations ไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="a5bfa-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="a5bfa-204">เมื่อต้องการซิงค์ข้อมูลสำหรับ **InvoiceAccount** และ **ContactPersonId** จาก Dataverse ไปยังแอป Finance and Operations คุณต้องใช้โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a5bfa-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="a5bfa-205">ใน Power Apps ให้สร้างโครงการการรวมข้อมูลระหว่างตาราง **Sales.Account** และ **Finance and Operations apps.Customers V3**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="a5bfa-206">ทิศทางของข้อมูลต้องมาจาก Dataverse ไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bfa-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="a5bfa-207">เนื่องจาก **InvoiceAccount** เป็นแอททริบิวต์ใหม่ในการรวมแบบสองทิศทาง คุณอาจต้องการข้ามการซิงโครไนส์เริ่มต้นสำหรับแอททริบิวต์นี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="a5bfa-208">สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="a5bfa-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="a5bfa-209">ภาพประกอบต่อไปนี้แสดงโครงการที่ปรับปรุง **CustomerAccount** และ **ContactPersonId**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![โครงการการรวมข้อมูลเพื่อปรับปรุง CustomerAccount และ ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="a5bfa-211">เพิ่มเงื่อนไขของบริษัทในตัวกรองในฝั่ง Dataverse เพื่อให้เฉพาะแถวที่ตรงกับเงื่อนไขตัวกรองจะถูกปรับปรุงในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bfa-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="a5bfa-212">เมื่อต้องการเพิ่มตัวกรอง ให้เลือกปุ่มตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="a5bfa-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="a5bfa-213">จากนั้น ในกล่องโต้ตอบ **แก้ไขการสอบถาม** คุณสามารถเพิ่มการสอบถามตัวกรอง เช่น **\_msdyn\_company\_value eq '\<guid\>'**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="a5bfa-214">[หมายเหตุ] ถ้าไม่มีปุ่มตัวกรองอยู่ ให้สร้างตั๋วการสนับสนุนเพื่อขอให้ทีมงานการรวมข้อมูลเปิดใช้งานความสามารถในการกรองของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="a5bfa-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="a5bfa-215">ถ้าคุณไม่ได้ป้อนการสอบถามตัวกรองสำหรับ **\_msdyn\_company\_value** แถวทั้งหมดจะถูกซิงค์</span><span class="sxs-lookup"><span data-stu-id="a5bfa-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![การเพิ่มการสอบถามตัวกรอง](media/cust_selfref7.png)

    <span data-ttu-id="a5bfa-217">การซิงโครไนส์เริ่มต้นของแถวเสร็จสมบูรณ์ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="a5bfa-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="a5bfa-218">ในแอป Finance and Operations เปิดใช้งานการติดตามการเปลี่ยนแปลงอีกครั้งสำหรับตาราง **ลูกค้า V3**</span><span class="sxs-lookup"><span data-stu-id="a5bfa-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>
