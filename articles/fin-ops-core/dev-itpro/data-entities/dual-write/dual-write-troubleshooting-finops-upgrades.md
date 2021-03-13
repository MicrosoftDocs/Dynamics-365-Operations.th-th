---
title: แก้ไขปัญหาจากการอัปเกรดของแอป Finance and Operations
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131232"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="e334e-103">แก้ไขปัญหาจากการอัปเกรดของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="e334e-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="e334e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="e334e-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการปรับปรุงของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e334e-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="e334e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e334e-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e334e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="e334e-108">ข้อผิดพลาดในการซิงโครไนส์ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e334e-108">Database synchronization errors</span></span>

<span data-ttu-id="e334e-109">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e334e-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e334e-110">คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณพยายามใช้ตาราง **DualWriteProjectConfiguration** เพื่ออัพเดตแอป Finance and Operations เป็น Platform update 30</span><span class="sxs-lookup"><span data-stu-id="e334e-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="e334e-111">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e334e-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="e334e-112">ลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="e334e-113">เปิด Visual Studio ในฐานะผู้ดูแลระบบ และเปิด Application Object Tree (AOT)</span><span class="sxs-lookup"><span data-stu-id="e334e-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="e334e-114">ค้นหา **DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e334e-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="e334e-115">ใน AOT ให้คลิกขวาที่ **DualWriteProjectConfiguration** แล้วเลือก **เพิ่มไปยังโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="e334e-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="e334e-116">เลือก **ตกลง** เพื่อสร้างโครงการใหม่ที่ใช้ตัวเลือกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e334e-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="e334e-117">ใน Solution Explorer คลิกขวาที่ **คุณสมบัติโครงการ** และตั้งค่า **ซิงโครไนส์ฐานข้อมูลในการสร้าง** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="e334e-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="e334e-118">สร้างโครงการ และยืนยันว่าการสร้างเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="e334e-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="e334e-119">บนเมนู **Dynamics 365** เลือก **ซิงโครไนส์ฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="e334e-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="e334e-120">เลือก **ซิงโครไนส์** เพื่อทำการซิงโครไนส์ฐานข้อมูลแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="e334e-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="e334e-121">หลังจากการซิงโครไนส์ฐานข้อมูลทั้งหมดเสร็จเรียบร้อยแล้ว รันขั้นตอนการซิงโครไนส์ฐานข้อมูลอีกครั้งใน Microsoft Dynamics Lifecycle Services (LCS) และใช้สคริปต์การอัพเกรดด้วยตนเองตามความเหมาะสม เพื่อให้คุณสามารถดำเนินการปรับปรุงต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="e334e-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="e334e-122">ปัญหาคอลัมน์ตารางที่ขาดหายไปในแผนผัง</span><span class="sxs-lookup"><span data-stu-id="e334e-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="e334e-123">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e334e-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e334e-124">บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e334e-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="e334e-125">*ฟิลด์แหล่งข้อมูลที่ขาดหายไป \<field name\> ในเค้าร่าง*</span><span class="sxs-lookup"><span data-stu-id="e334e-125">*Missing source field \<field name\> in the schema.*</span></span>

![ตัวอย่างของข้อความแสดงข้อผิดพลาดของคอลัมน์ต้นทางที่ขาดหายไป](media/error_missing_field.png)

<span data-ttu-id="e334e-127">เมื่อต้องการแก้ไขปัญหานี้ อันดับแรกให้ทำตามขั้นตอนเหล่านี้เพื่อตรวจสอบให้แน่ใจว่าคอลัมน์อยู่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="e334e-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="e334e-128">ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="e334e-129">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกไทล์ **พารามิเตอร์กรอบงาน** และจากนั้น บนแท็บ **การตั้งค่าตาราง** เลือก **รีเฟรชรายการตาราง** เพื่อรีเฟรชตาราง</span><span class="sxs-lookup"><span data-stu-id="e334e-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="e334e-130">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** เลือกแท็บ **ตารางข้อมูล** และตรวจสอบให้แน่ใจว่ามีการแสดงรายการตาราง</span><span class="sxs-lookup"><span data-stu-id="e334e-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="e334e-131">ถ้าไม่มีการแสดงรายการตาราง ให้ลงชื่อเข้าใช้ใน VM สำหรับแอป Finance and Operations และตรวจสอบให้แน่ใจว่าตารางพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e334e-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="e334e-132">เปิดหน้า **การแม็ปตาราง** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="e334e-133">เลือก **รีเฟรชรายการตาราง** เพื่อเติมข้อมูลคอลัมน์โดยอัตโนมัติในการแม็ปตาราง</span><span class="sxs-lookup"><span data-stu-id="e334e-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="e334e-134">ถ้ายังไม่มีการแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e334e-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e334e-135">ขั้นตอนเหล่านี้จะให้คำแนะนำเกี่ยวกับกระบวนการลบตาราง แล้วจากนั้น เพิ่มอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e334e-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="e334e-136">เมื่อต้องการหลีกเลี่ยงปัญหา ให้ตรวจสอบให้แน่ใจว่าได้ปฏิบัติตามขั้นตอนต่างๆ อย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="e334e-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="e334e-137">ในแอป Finance and Operations ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **ตารางข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="e334e-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="e334e-138">ค้นหาตารางที่ขาดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="e334e-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="e334e-139">คลิก **ปรับเปลี่ยนการแม็ปเป้าหมาย** ในแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="e334e-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="e334e-140">บนบานหน้าต่าง **แม็ปการแบ่งระยะไปยังเป้าหมาย** คลิก **สร้างการแม็ป**</span><span class="sxs-lookup"><span data-stu-id="e334e-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="e334e-141">เปิดหน้า **การแม็ปตาราง** จากหน้า **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e334e-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="e334e-142">ถ้าแอททริบิวต์ไม่ถูกเติมข้อมูลโดยอัตโนมัติบนแผนที่ ให้เพิ่มด้วยตนเองโดยการคลิกปุ่ม **เพิ่มแอททริบิวต์** แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e334e-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="e334e-143">เลือกแผนที่ และคลิก **รัน**</span><span class="sxs-lookup"><span data-stu-id="e334e-143">Select the map and click **Run**.</span></span>
