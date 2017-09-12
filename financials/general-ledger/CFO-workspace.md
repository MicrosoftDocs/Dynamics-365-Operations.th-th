---
title: "เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO"
description: "หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ"
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: th-th
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="c76d2-103">เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO</span><span class="sxs-lookup"><span data-stu-id="c76d2-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c76d2-104">หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของประธานคณะผู้บริหารด้านการเงิน (CFO) เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="c76d2-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="c76d2-105">พื้นที่ทำงานของ CFO มีแท็บ **ภาพรวม** และแท็บ **การเงิน**</span><span class="sxs-lookup"><span data-stu-id="c76d2-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="c76d2-106">รายงานบนสองแท็บนี้มีข้อมูลสำรองโดยหน่วยวัดสองแบบ: LedgerActivityMeasure และ BudgetActivityMeasure</span><span class="sxs-lookup"><span data-stu-id="c76d2-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="c76d2-107">ใน Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition การอัพเดตของเดือนกรกฎาคม 2017 มีความสัมพันธ์ระหว่างหน่วยวัดสองแบบนั้นและเอนทิตี้ DimensionCombinationEntity</span><span class="sxs-lookup"><span data-stu-id="c76d2-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="c76d2-108">ดังนั้น คุณสามารถเลือกมิติได้</span><span class="sxs-lookup"><span data-stu-id="c76d2-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="c76d2-109">ใน Finance and Operations ในหน้า **ที่จัดเก็บเอนทิตี้** อัพเดตหน่วยวัด **LedgerActivityMeasure** และ **BudgetActivityMeasure**</span><span class="sxs-lookup"><span data-stu-id="c76d2-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="c76d2-110">ใน Microsoft Visual Studio เปิดแอพลิเคชัน Application Explorer และค้นหา **LedgerCFO**</span><span class="sxs-lookup"><span data-stu-id="c76d2-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="c76d2-111">ภายใต้ **ทรัพยากร** เปิด **LedgerCFOWorkspacePBIX**</span><span class="sxs-lookup"><span data-stu-id="c76d2-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="c76d2-112">เมื่อทรัพยากรถูกเปิดขึ้นในเดสก์ท็อป Microsoft Power BI เลือก **รับข้อมูล** เลือก**ฐานข้อมูล SQL Server** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c76d2-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="c76d2-113">ป้อนชื่อเซิร์ฟเวอร์ แล้วป้อน **AxDW** เป็นฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c76d2-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="c76d2-114">เลือก **DirectQuery** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c76d2-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="c76d2-115">ค้นหาและเลือก **LedgerActivityMeasure\_DimensionCombination** แล้วเลือก **โหลด**</span><span class="sxs-lookup"><span data-stu-id="c76d2-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c76d2-116">ในรายการ **ฟิลด์** เปลี่ยนชื่อตาราง **มิติทางการเงิน** เพื่อให้สามารถระบุได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="c76d2-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="c76d2-117">เลือก **จัดการความสัมพันธ์** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c76d2-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="c76d2-118">ในฟิลด์แรก เลือก **กิจกรรมบัญชีแยกประเภททั่วไป** แล้วเลือก **LedgerDimension**</span><span class="sxs-lookup"><span data-stu-id="c76d2-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="c76d2-119">ในฟิลด์ที่สอง เลือก **LedgerActivityMeasure\_DimensionCombination** (หรือ **มิติทางการเงิน** ถ้าคุณเปลี่ยนชื่อตาราง)</span><span class="sxs-lookup"><span data-stu-id="c76d2-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="c76d2-120">เลือกส่วนหัว **DimensionCombinationRECID**</span><span class="sxs-lookup"><span data-stu-id="c76d2-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="c76d2-121">ในฟิลด์ **จำนวนนับ** เลือก **หลายต่อหนึ่ง**</span><span class="sxs-lookup"><span data-stu-id="c76d2-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="c76d2-122">เปลี่ยนค่า **ทิศทางตัวกรองแบบข้าม** เป็น **เดี่ยว**</span><span class="sxs-lookup"><span data-stu-id="c76d2-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="c76d2-123">เลือกทั้ง **ทำให้ความสัมพันธ์นี้เป็นใช้งานอยู่** และ **ยอมรับความถูกต้องของการอ้างอิง** เลือก **ตกลง** แล้วเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="c76d2-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="c76d2-124">[![สร้างความสัมพันธ์](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="c76d2-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="c76d2-125">ในรายการ **ฟิลด์** คุณควรเห็นตารางและมิติทางการเงินที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c76d2-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="c76d2-126">ลากมิติทางการเงินที่คุณต้องการไปยังตัวกรองระดับรายงาน</span><span class="sxs-lookup"><span data-stu-id="c76d2-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="c76d2-127">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c76d2-127">Save your changes.</span></span>
15. <span data-ttu-id="c76d2-128">ใน Application Object Tree (AOT) คลิกขวาโครงการของคุณ จากนั้นเลือก **ซิงโครไนส์**</span><span class="sxs-lookup"><span data-stu-id="c76d2-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="c76d2-129">สร้างโครงการของคุณ และจากนั้นเปิดแอพลิเคชันเพื่อดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c76d2-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="c76d2-130">[![พื้นที่ทำงานที่เสร็จสมบูรณ์](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="c76d2-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

