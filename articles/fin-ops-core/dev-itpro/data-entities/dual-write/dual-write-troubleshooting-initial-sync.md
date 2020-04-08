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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172725"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="057ec-103">แก้ไขปัญหาในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="057ec-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="057ec-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="057ec-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="057ec-105">กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="057ec-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="057ec-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="057ec-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="057ec-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="057ec-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="057ec-108">ตรวจสอบข้อผิดพลาดของการซิงโครไนส์เริ่มต้นในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="057ec-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="057ec-109">หลังจากที่คุณเปิดใช้งานเท็มเพลตการแม็ป สถานะของแผนที่ควรเป็น **กำลังรัน**</span><span class="sxs-lookup"><span data-stu-id="057ec-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="057ec-110">ถ้าสถานะ **ไม่ได้รันอยู่** ข้อผิดพลาดเกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="057ec-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="057ec-111">เมื่อต้องการดูข้อผิดพลาด ให้เลือกแท็บ **รายละเอียดการซิงค์เริ่มต้น** บนหน้า **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="057ec-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![แท็บรายละเอียดการซิงค์เริ่มต้น](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="057ec-113">คุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้: 400 คำขอไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="057ec-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="057ec-114">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="057ec-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="057ec-115">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามรันการแม็ปและการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="057ec-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="057ec-116">*เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="057ec-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="057ec-117">นี่เป็นตัวอย่างของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="057ec-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="057ec-118">ถ้าเกิดข้อผิดพลาดนี้อย่างสม่ำเสมอ และคุณไม่สามารถดำเนินการซิงโครไนส์เริ่มต้นให้เสร็จสมบูรณ์ได้ ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="057ec-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="057ec-119">ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="057ec-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="057ec-120">เปิด Microsoft Management Console</span><span class="sxs-lookup"><span data-stu-id="057ec-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="057ec-121">ในบานหน้าต่าง **บริการ** ตรวจสอบให้แน่ใจว่ามีการเรียกใช้บริการกรอบงานการนำเข้าการส่งออกข้อมูล Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="057ec-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="057ec-122">เริ่มต้นใหม่ ถ้าถูกหยุดเนื่องจากการซิงโครไนส์เริ่มต้นต้องการ</span><span class="sxs-lookup"><span data-stu-id="057ec-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="057ec-123">ข้อผิดพลาดการซิงโครไนส์เริ่มต้น: 403 ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="057ec-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="057ec-124">คุณอาจได้รับข้อความแสดงข้อผิดพลาดในระหว่างการซิงโครไนส์เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="057ec-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="057ec-125">*(\[ไม่ได้รับอนุญาต\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต) AX การส่งออกพบข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="057ec-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="057ec-126">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="057ec-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="057ec-127">ลงชื่อเข้าใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="057ec-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="057ec-128">บนหน้า **แอพลิเคชัน Azure Active Directory** ให้ลบไคลเอนต์ **DtAppID** และจากนั้น เพิ่มใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="057ec-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![รายการของแอพลิเคชัน Azure AD](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="057ec-130">ความล้มเหลวในการอ้างอิงตนเองในระหว่างการซิงโครไนส์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="057ec-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="057ec-131">คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้ ถ้าการแม็ปใดๆ ของคุณมีการอ้างอิงตนเอง:</span><span class="sxs-lookup"><span data-stu-id="057ec-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="057ec-132">*ในผู้จัดจำหน่าย V2 ข้อผิดพลาดต่อไปนี้: รหัสเรกคอร์ด: เรกคอร์ดใหม่ ErrorMessage: ไม่สามารถแก้ไข guid สำหรับฟิลด์นี้: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber ไม่พบค่าการค้นหา: CN-001 ลองใช้ URL นี้เพื่อตรวจสอบว่ามีข้อมูลอ้างอิงอยู่หรือไม่: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="057ec-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="057ec-133">ข้อผิดพลาดชนิดนี้เกิดขึ้นในระหว่างการซิงโครไนส์เริ่มต้นของการแม็ปที่มีการอ้างอิงตนเอง</span><span class="sxs-lookup"><span data-stu-id="057ec-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="057ec-134">ในตัวอย่างก่อนหน้านี้ บัญชีใบแจ้งหนี้ของฟิลด์อ้างอิงถึงเอนทิตี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="057ec-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="057ec-135">เมื่อต้องการแก้ไขปัญหานี้ คุณอาจต้องรันการแม็ปสองครั้ง ก่อนที่การซิงโครไนส์เริ่มต้นจะสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="057ec-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

