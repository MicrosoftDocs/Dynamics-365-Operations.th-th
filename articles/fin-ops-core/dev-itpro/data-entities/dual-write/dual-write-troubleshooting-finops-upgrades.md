---
title: แก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172888"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="796e7-103">แก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="796e7-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="796e7-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="796e7-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="796e7-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="796e7-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="796e7-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="796e7-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="796e7-108">ข้อผิดพลาดในการซิงโครไนส์ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="796e7-108">Database synchronization errors</span></span>

<span data-ttu-id="796e7-109">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="796e7-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="796e7-110">คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณพยายามใช้เอนทิตี้ **DualWriteProjectConfiguration** เพื่อปรับปรุงแอป Finance and Operations เป็น Platform update 30</span><span class="sxs-lookup"><span data-stu-id="796e7-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="796e7-111">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="796e7-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="796e7-112">ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="796e7-113">เปิด Visual Studio ในฐานะผู้ดูแลระบบ และเปิด Application Object Tree (AOT)</span><span class="sxs-lookup"><span data-stu-id="796e7-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="796e7-114">ค้นหา **DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="796e7-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="796e7-115">ใน AOT ให้คลิกขวาที่ **DualWriteProjectConfiguration** แล้วเลือก **เพิ่มไปยังโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="796e7-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="796e7-116">เลือก **ตกลง** เพื่อสร้างโครงการใหม่ที่ใช้ตัวเลือกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="796e7-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="796e7-117">ใน Solution Explorer คลิกขวาที่ **คุณสมบัติโครงการ** และตั้งค่า **ซิงโครไนส์ฐานข้อมูลในการสร้าง** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="796e7-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="796e7-118">สร้างโครงการ และยืนยันว่าการสร้างเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="796e7-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="796e7-119">บนเมนู **Dynamics 365** เลือก **ซิงโครไนส์ฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="796e7-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="796e7-120">เลือก **ซิงโครไนส์** เพื่อทำการซิงโครไนส์ฐานข้อมูลแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="796e7-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="796e7-121">หลังจากการซิงโครไนส์ฐานข้อมูลทั้งหมดเสร็จเรียบร้อยแล้ว รันขั้นตอนการซิงโครไนส์ฐานข้อมูลอีกครั้งใน Microsoft Dynamics Lifecycle Services (LCS) และใช้สคริปต์การอัพเกรดด้วยตนเองตามความเหมาะสม เพื่อให้คุณสามารถดำเนินการปรับปรุงต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="796e7-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="796e7-122">ปัญหาฟิลด์เอนทิตี้ที่หายไปบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="796e7-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="796e7-123">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="796e7-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="796e7-124">บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="796e7-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="796e7-125">*ฟิลด์แหล่งข้อมูลที่ขาดหายไป \<ชื่อฟิลด์\> ในเค้าร่าง*</span><span class="sxs-lookup"><span data-stu-id="796e7-125">*Missing source field \<field name\> in the schema.*</span></span>

![ตัวอย่างของข้อความแสดงข้อผิดพลาดของฟิลด์ต้นทางที่ขาดหายไป](media/error_missing_field.png)

<span data-ttu-id="796e7-127">เมื่อต้องการแก้ไขปัญหานี้ อันดับแรกให้ทำตามขั้นตอนเหล่านี้เพื่อตรวจสอบให้แน่ใจว่าฟิลด์อยู่ในเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="796e7-128">ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="796e7-129">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกไทล์ **พารามิเตอร์กรอบงาน** และจากนั้น บนแท็บ **การตั้งค่าเอนทิตี้** เลือก **รีเฟรชรายการเอนทิตี้** เพื่อรีเฟรชเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="796e7-130">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกแท็บ **เอนทิตี้ข้อมูล** และตรวจสอบให้แน่ใจว่ามีการแสดงรายการเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="796e7-131">ถ้าไม่มีการแสดงรายการเอนทิตี้ ให้ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations และตรวจสอบให้แน่ใจว่าเอนทิตี้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="796e7-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="796e7-132">เปิดหน้า **การแม็ปเอนทิตี้** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="796e7-133">เลือก **รีเฟรชรายการเอนทิตี้** เพื่อเติมข้อมูลในฟิลด์โดยอัตโนมัติในการแม็ปเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="796e7-134">ถ้ายังไม่มีการแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="796e7-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="796e7-135">ขั้นตอนเหล่านี้จะให้คำแนะนำเกี่ยวกับกระบวนการลบเอนทิตี้ แล้วเพิ่มอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="796e7-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="796e7-136">เมื่อต้องการหลีกเลี่ยงปัญหา ให้ตรวจสอบให้แน่ใจว่าได้ปฏิบัติตามขั้นตอนต่างๆ อย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="796e7-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="796e7-137">ในแอป Finance and Operations ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **เอนทิตี้ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="796e7-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="796e7-138">ค้นหาเอนทิตี้ที่ขาดฟิลด์</span><span class="sxs-lookup"><span data-stu-id="796e7-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="796e7-139">จัดทำบันทึกย่อของเอนทิตี้เป้าหมาย ตารางการแบ่งระยะ ชื่อเอนทิตี้ และค่าคอลัมน์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="796e7-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="796e7-140">ถ้ากลุ่มการประมวลผลใดๆ ของคุณขึ้นอยู่กับเอนทิตี้นี้ ให้ใช้การดำเนินการที่เหมาะสมสำหรับกลุ่มการประมวลผล ก่อนที่คุณจะลบเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="796e7-141">ลบเอนทิตี้ที่ขาดฟิลด์</span><span class="sxs-lookup"><span data-stu-id="796e7-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="796e7-142">เลือก **สร้าง** และเพิ่มเอนทิตี้กลับ</span><span class="sxs-lookup"><span data-stu-id="796e7-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="796e7-143">ระบุค่าที่คุณได้บันทึกไว้ในขั้นตอนที่2</span><span class="sxs-lookup"><span data-stu-id="796e7-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="796e7-144">เปิดหน้า **การแม็ปเอนทิตี้** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="796e7-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="796e7-145">เลือก **รีเฟรชรายการเอนทิตี้** เพื่อเติมข้อมูลในฟิลด์โดยอัตโนมัติในการแม็ปเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="796e7-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>
