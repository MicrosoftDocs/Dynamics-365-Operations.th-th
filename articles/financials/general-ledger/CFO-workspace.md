---
title: "เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO"
description: "หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ebe2766976f2c7a88f9b919c8c13e05e36576e45
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="6f71a-103">เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO</span><span class="sxs-lookup"><span data-stu-id="6f71a-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f71a-104">หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของประธานคณะผู้บริหารด้านการเงิน (CFO) เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6f71a-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="6f71a-105">พื้นที่ทำงานของ CFO มีแท็บ **ภาพรวม** และแท็บ **การเงิน** รายงานบนสองแท็บนี้มีข้อมูลสำรองโดยหน่วยวัดสองแบบ: LedgerActivityMeasure และ BudgetActivityMeasure</span><span class="sxs-lookup"><span data-stu-id="6f71a-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="6f71a-106">ใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) มีความสัมพันธ์ระหว่างหน่วยวัดสองแบบนั้นและเอนทิตี้ DimensionCombinationEntity</span><span class="sxs-lookup"><span data-stu-id="6f71a-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="6f71a-107">ดังนั้น คุณสามารถเลือกมิติได้</span><span class="sxs-lookup"><span data-stu-id="6f71a-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="6f71a-108">ใน Finance and Operations ในหน้า **ที่จัดเก็บเอนทิตี้** อัพเดตหน่วยวัด **LedgerActivityMeasure** และ **BudgetActivityMeasure**</span><span class="sxs-lookup"><span data-stu-id="6f71a-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="6f71a-109">ใน Microsoft Visual Studio เปิดแอพลิเคชัน Application Explorer และค้นหา **LedgerCFO**</span><span class="sxs-lookup"><span data-stu-id="6f71a-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="6f71a-110">ภายใต้ **ทรัพยากร** เปิด **LedgerCFOWorkspacePBIX**</span><span class="sxs-lookup"><span data-stu-id="6f71a-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="6f71a-111">เมื่อทรัพยากรถูกเปิดขึ้นในเดสก์ท็อป Microsoft Power BI เลือก **รับข้อมูล** เลือก**ฐานข้อมูล SQL Server** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="6f71a-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="6f71a-112">ป้อนชื่อเซิร์ฟเวอร์ แล้วป้อน **AxDW** เป็นฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6f71a-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="6f71a-113">เลือก **DirectQuery** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6f71a-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="6f71a-114">ค้นหาและเลือก **LedgerActivityMeasure\_DimensionCombination** แล้วเลือก **โหลด**</span><span class="sxs-lookup"><span data-stu-id="6f71a-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="6f71a-115">ในรายการ **ฟิลด์** เปลี่ยนชื่อตาราง **มิติทางการเงิน** เพื่อให้สามารถระบุได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="6f71a-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="6f71a-116">เลือก **จัดการความสัมพันธ์** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6f71a-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="6f71a-117">ในฟิลด์แรก เลือก **กิจกรรมบัญชีแยกประเภททั่วไป** แล้วเลือก **LedgerDimension**</span><span class="sxs-lookup"><span data-stu-id="6f71a-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="6f71a-118">ในฟิลด์ที่สอง เลือก **LedgerActivityMeasure\_DimensionCombination** (หรือ **มิติทางการเงิน** ถ้าคุณเปลี่ยนชื่อตาราง)</span><span class="sxs-lookup"><span data-stu-id="6f71a-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="6f71a-119">เลือกส่วนหัว **DimensionCombinationRECID**</span><span class="sxs-lookup"><span data-stu-id="6f71a-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="6f71a-120">ในฟิลด์ **จำนวนนับ** เลือก **หลายต่อหนึ่ง**</span><span class="sxs-lookup"><span data-stu-id="6f71a-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="6f71a-121">เปลี่ยนค่า **ทิศทางตัวกรองแบบข้าม** เป็น **เดี่ยว**</span><span class="sxs-lookup"><span data-stu-id="6f71a-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="6f71a-122">เลือกทั้ง **ทำให้ความสัมพันธ์นี้เป็นใช้งานอยู่** และ **ยอมรับความถูกต้องของการอ้างอิง** เลือก **ตกลง** แล้วเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="6f71a-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="6f71a-123">[![สร้างความสัมพันธ์](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="6f71a-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="6f71a-124">ในรายการ **ฟิลด์** คุณควรเห็นตารางและมิติทางการเงินที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6f71a-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="6f71a-125">ลากมิติทางการเงินที่คุณต้องการไปยังตัวกรองระดับรายงาน</span><span class="sxs-lookup"><span data-stu-id="6f71a-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="6f71a-126">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6f71a-126">Save your changes.</span></span>
15. <span data-ttu-id="6f71a-127">ใน Application Object Tree (AOT) คลิกขวาโครงการของคุณ จากนั้นเลือก **ซิงโครไนส์**</span><span class="sxs-lookup"><span data-stu-id="6f71a-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="6f71a-128">สร้างโครงการของคุณ และจากนั้นเปิดแอพลิเคชันเพื่อดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="6f71a-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="6f71a-129">[![พื้นที่ทำงานที่เสร็จสมบูรณ์](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="6f71a-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

