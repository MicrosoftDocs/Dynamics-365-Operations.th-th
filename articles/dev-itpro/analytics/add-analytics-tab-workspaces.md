---
title: เพิ่มการวิเคราะห์ไปยังบริการโดยใช้ Power BI Embedded
description: หัวข้อนี้แสดงวิธีการฝังรายงาน Power BI ในแท็บการวิเคราะห์ของพื้นที่ทำงาน
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a190e15dc304f60739c80d75222830ee737c5a32
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548196"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="bf8e1-103">เพิ่มการวิเคราะห์ไปยังบริการโดยใช้ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="bf8e1-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="bf8e1-104">คุณลักษณะนี้ได้รับการสนับสนุนใน Dynamics 365 for Finance and Operations (รุ่น 7.2 และรุ่นที่ใหม่กว่า)</span><span class="sxs-lookup"><span data-stu-id="bf8e1-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="bf8e1-105">คำนำ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-105">Introduction</span></span>
<span data-ttu-id="bf8e1-106">หัวข้อนี้แสดงวิธีการฝังรายงาน Microsoft Power BI ในแท็บ **การวิเคราะห์** ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="bf8e1-107">สำหรับตัวอย่างที่กำหนดที่นี่ เราจะขยายพื้นที่ทำงาน **การจัดการการจอง** ในแอพลิเคชันการจัดการยานพาหนะเพื่อฝังพื้นที่ทำงานการวิเคราะห์บนแท็บ **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf8e1-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bf8e1-108">Prerequisites</span></span>
+ <span data-ttu-id="bf8e1-109">เข้าถึงสภาพแวดล้อมนักพัฒนาที่รันการอัพเดตแพลตฟอร์ม 8 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="bf8e1-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="bf8e1-110">รายงานการวิเคราะห์ (.pbix file) ที่ถูกสร้างโดยใช้ Microsoft Power BI Desktop และที่มีแบบจำลองข้อมูลที่มีแหล่งที่มาจากฐานข้อมูลที่จัดเก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="bf8e1-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="bf8e1-111">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="bf8e1-111">Overview</span></span>
<span data-ttu-id="bf8e1-112">ไม่ว่าคุณจะขยายพื้นที่ทำงานของแอพลิเคชันที่มีอยู่ หรือใช้พื้นที่ทำงานใหม่ของคุณเอง คุณสามารถใช้มุมมองการวิเคราะห์แบบฝังเพื่อจัดส่งมุมมองที่ชาญฉลาดและเชิงโต้ตอบของข้อมูลธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="bf8e1-113">กระบวนการสำหรับการเพิ่มแท็บพื้นที่ทำงานเชิงวิเคราะห์มีสี่ขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="bf8e1-114">เพิ่มไฟล์ .pbix เป็นทรัพยากร Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bf8e1-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="bf8e1-115">กำหนดแท็บพื้นที่ทำงานเชิงวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="bf8e1-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="bf8e1-116">ฝังทรัพยากร .pbix บนแท็บพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="bf8e1-117">ตัวเลือก: เพิ่มส่วนขยายเพื่อกำหนดมุมมองเอง</span><span class="sxs-lookup"><span data-stu-id="bf8e1-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="bf8e1-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างรายงานการวิเคราะห์ ดู [เริ่มต้นใช้งาน Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)</span><span class="sxs-lookup"><span data-stu-id="bf8e1-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="bf8e1-119">หน้านี้คือแหล่งข้อมูลเชิงลึกที่ดีเยี่ยมที่สามารถช่วยคุณในการสร้างโซลูชันการรายงานเชิงวิเคราะห์ที่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="bf8e1-120">เพิ่มไฟล์ .pbix เป็นทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bf8e1-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="bf8e1-121">ก่อนที่คุณจะเริ่มต้น คุณต้องสร้างหรือได้รับรายงาน Power BI ที่คุณจะฝังในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="bf8e1-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างรายงานการวิเคราะห์ ดู [เริ่มต้นใช้งาน Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)</span><span class="sxs-lookup"><span data-stu-id="bf8e1-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="bf8e1-123">ให้ปฏิบัติตามขั้นตอนเหล่านี้ เพื่อเพิ่มไฟล์ .pbix เป็นอาร์ทิแฟกต์โครงการ Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bf8e1-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="bf8e1-124">สร้างโครงการใหม่ในแบบจำลองที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="bf8e1-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="bf8e1-125">ใน Solution Explorer เลือกโครงการ คลิกขวา และจากนั้นเลือก **เพิ่ม** \> **รายการใหม่**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="bf8e1-126">ในกล่องโต้ตอบ **เพิ่มรายการใหม่** ภายใต้ **วัตถุการดำเนินงาน** เลือกเท็มเพลต **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="bf8e1-127">ป้อนชื่อที่จะใช้เป็นการอ้างอิงรายงานในข้อมูลเมตาของ X++ และคลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![เพิ่มกล่องโต้ตอบรายการใหม่](media/analytical-workspace-add.png)

5. <span data-ttu-id="bf8e1-129">ค้นหาไฟล์ .pbix ที่ประกอบด้วยข้อกำหนดของรายงานเชิงวิเคราะห์ และจากนั้น คลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![เลือกกล่องโต้ตอบไฟล์ทรัพยากร](media/analytical-workspace-select-resource.png)

<span data-ttu-id="bf8e1-131">หลังจากที่คุณได้เพิ่มไฟล์ .pbix เป็นทรัพยากร Dynamics 365 แล้ว คุณสามารถฝังรายงานในพื้นที่ทำงาน และเพิ่มลิงค์โดยตรงโดยใช้รายการเมนู</span><span class="sxs-lookup"><span data-stu-id="bf8e1-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="bf8e1-132">เพิ่มตัวควบคุมแท็บไปยังพื้นที่ทำงานของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="bf8e1-133">ในตัวอย่างนี้ เราจะขยายพื้นที่ทำงาน **การจัดการการจอง** ในแบบจำลองการจัดการยานพาหนะโดยการเพิ่มแท็บ **การวิเคราะห์** ไปยังคำนิยามของแบบฟอร์ม **FMClerkWorkspace**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="bf8e1-134">ภาพประกอบต่อไปนี้แสดงลักษณะของฟอร์ม **FMClerkWorkspace** ในตัวออกแบบใน Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bf8e1-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![แบบฟอร์ม FMClerkWorkspace ก่อนที่จะเปลี่ยนแปลง](media/analytical-workspace-definition-before.png)

<span data-ttu-id="bf8e1-136">ทำตามขั้นตอนเหล่านี้เพื่อขยายแบบฟอร์มคำนิยามสำหรับพื้นที่ทำงาน **การจัดการการจอง**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="bf8e1-137">เปิดตัวออกแบบแบบฟอร์มเพื่อขยายคำนิยามการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="bf8e1-138">ในข้อกำหนดของการออกแบบ เลือกองค์ประกอบบนสุดที่มีชื่อว่า **ออกแบบ | รูปแบบ: พื้นที่ในการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="bf8e1-139">คลิกขวา และจากนั้นเลือก **สร้าง** \> **แท็บ** เพื่อเพิ่มตัวควบคุมใหม่ที่ชื่อว่า **FormTabControl1**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="bf8e1-140">ในตัวออกแบบแบบฟอร์ม เลือก **FormTabControl1**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="bf8e1-141">คลิกขวา จากนั้นเลือก **หน้าแท็บใหม่** เพื่อเพิ่มหน้าแท็บใหม่</span><span class="sxs-lookup"><span data-stu-id="bf8e1-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="bf8e1-142">เปลี่ยนชื่อหน้าแท็บเป็นบางสิ่งที่สำคัญ เช่น **พื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="bf8e1-143">ในตัวออกแบบแบบฟอร์ม เลือก **FormTabControl1**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="bf8e1-144">คลิกขวา แล้วเลือก **หน้าแท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="bf8e1-145">เปลี่ยนชื่อหน้าแท็บเป็นบางสิ่งที่สำคัญ เช่น **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="bf8e1-146">ในตัวออกแบบแบบฟอร์ม เลือก **การวิเคราะห์ (หน้าแท็บ)**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="bf8e1-147">ตั้งค่าคุณสมบัติ **คำอธิบาย** เป็น **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="bf8e1-148">คลิกขวาตัวควบคุม และจากนั้นเลือก **สร้าง** \> **กลุ่ม** เพื่อเพิ่มตัวควบคุมกลุ่มแบบฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="bf8e1-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="bf8e1-149">เปลี่ยนกลุ่มแบบฟอร์มเป็นบางสิ่งที่สำคัญ เช่น **powerBIReportGroup**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="bf8e1-150">ในแบบฟอร์ม เลือก **PanoramaBody (แท็บ)** แล้วลากตัวควบคุมไปยังแท็บ **พื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="bf8e1-151">ในข้อกำหนดของการออกแบบ เลือกองค์ประกอบบนสุดที่มีชื่อว่า **ออกแบบ | รูปแบบ: พื้นที่ในการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="bf8e1-152">คลิกขวา แล้วเลือก **เอารูปแบบออก**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="bf8e1-153">คลิกขวาอีกครั้ง และจากนั้นเลือก **เพิ่มรูปแบบ** \> **พื้นที่ทำงานที่แตะ**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="bf8e1-154">ดำเนินการสร้างเพื่อตรวจสอบการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="bf8e1-155">ภาพประกอบต่อไปนี้แสดงลักษณะของการออกแบบหลังจากที่มีการใช้การเปลี่ยนแปลงเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="bf8e1-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace หลังจากมีการเปลี่ยนแปลง](media/analytical-workspace-definition-after.png)

<span data-ttu-id="bf8e1-157">หลังจากที่คุณได้เพิ่มตัวควบคุมแบบฟอร์มที่จะใช้เพื่อฝังรายงานพื้นที่ทำงาน คุณต้องกำหนดขนาดของตัวควบคุมหลักเพื่อให้รองรับกับโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="bf8e1-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="bf8e1-158">โดยค่าเริ่มต้น ทั้งหน้า **บานหน้าต่างตัวกรอง** และหน้า **แท็บ** จะปรากฏในรายงาน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="bf8e1-159">อย่างไรก็ตาม คุณสามารถเปลี่ยนการมองเห็นได้ของตัวควบคุมเหล่านี้ตามความเหมาะสมสำหรับผู้ใช้ปลายทางของรายงาน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="bf8e1-160">สำหรับพื้นที่ทำงานแบบฝัง เราขอแนะนำให้คุณใช้ส่วนขยายเพื่อซ่อนทั้งหน้า **บานหน้าต่างตัวกรอง** และหน้า **แท็บ** เพื่อความสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="bf8e1-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="bf8e1-161">เมื่อถึงขั้นตอนนี้ คุณได้ทำการขยายคำนิยามแบบฟอร์มแอพลิเคชันเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="bf8e1-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="bf8e1-162">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ส่วนขยายเพื่อทำการเลือกกำหนด ให้ดูที่ [การเลือกกำหนด: การโอเวอร์เลย์และการขยายออก](../extensibility/customization-overlayering-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="bf8e1-162">For more information about how to use extensions to do customizations, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="bf8e1-163">เพิ่มตรรกะทางธุรกิจ X++ เพื่อฝังการควบคุมตัวแสดง</span><span class="sxs-lookup"><span data-stu-id="bf8e1-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="bf8e1-164">ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มตรรกะทางธุรกิจที่เริ่มต้นการควบคุม Report Viewer ที่ฝังอยู่ในพื้นที่ทำงาน **การจัดการการจอง**</span><span class="sxs-lookup"><span data-stu-id="bf8e1-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="bf8e1-165">เปิดตัวออกแบบแบบฟอร์ม **FMClerkWorkspace** เพื่อขยายคำนิยามการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="bf8e1-166">กด F7 เพื่อเข้าถึงรหัสเบื้องหลังคำนิยามของรหัส</span><span class="sxs-lookup"><span data-stu-id="bf8e1-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="bf8e1-167">ให้เพิ่มรหัส X++ ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bf8e1-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="bf8e1-168">ดำเนินการสร้างเพื่อตรวจสอบการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="bf8e1-169">ในขณะนี้คุณได้ทำงานในการเพิ่มตรรกะทางธุรกิจเพื่อเริ่มต้นการควบคุม Report Viewer แบบฝังเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="bf8e1-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="bf8e1-170">ภาพประกอบต่อไปนี้แสดงลักษณะของพื้นที่ทำงานหลังจากที่มีการใช้การเปลี่ยนแปลงเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="bf8e1-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![รายงานที่ฝังอยู่ในพื้นที่ทำงาน](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="bf8e1-172">คุณสามารถเข้าถึงมุมมองการดำเนินงานที่มีอยู่ได้โดยใช้แท็บพื้นที่ทำงานที่อยู่ด้านล่างชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="bf8e1-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="bf8e1-173">ข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="bf8e1-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="bf8e1-174">วิธีการ PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="bf8e1-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="bf8e1-175">ส่วนนี้ให้ช้อมูลเกี่ยวกับคลาสตัวช่วยเหลือที่ถูกใช้เพื่อฝังรายงาน Power BI (ทรัพยากร .pbix) ในการควบคุมกลุ่มฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="bf8e1-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="bf8e1-176">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="bf8e1-176">Syntax</span></span>
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="bf8e1-177">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="bf8e1-177">Parameters</span></span>

| <span data-ttu-id="bf8e1-178">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="bf8e1-178">Name</span></span>             | <span data-ttu-id="bf8e1-179">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bf8e1-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8e1-180">ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bf8e1-180">resourceName</span></span>     | <span data-ttu-id="bf8e1-181">ชื่อของทรัพยากร .pbix</span><span class="sxs-lookup"><span data-stu-id="bf8e1-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="bf8e1-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="bf8e1-182">formGroupControl</span></span> | <span data-ttu-id="bf8e1-183">การควบคุมกลุ่มฟอร์มที่จะนำการควบคุมรายงาน Power BI ไปใช้</span><span class="sxs-lookup"><span data-stu-id="bf8e1-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="bf8e1-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="bf8e1-184">defaultPageName</span></span>  | <span data-ttu-id="bf8e1-185">ชื่อหน้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bf8e1-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="bf8e1-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="bf8e1-186">showFilterPane</span></span>   | <span data-ttu-id="bf8e1-187">ค่าบูลีนที่บ่งชี้ว่าควรแสดงบานหน้าต่างตัวกรอง (**จริง**) หรือ (**เท็จ**) ที่ซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="bf8e1-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="bf8e1-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="bf8e1-188">showNavPane</span></span>      | <span data-ttu-id="bf8e1-189">ค่าบูลีนที่บ่งชี้ว่าควรแสดงบานหน้าต่างนำทาง (**จริง**) หรือ (**เท็จ**) ที่ซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="bf8e1-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="bf8e1-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="bf8e1-190">defaultFilters</span></span>   | <span data-ttu-id="bf8e1-191">ตัวกรองเริ่มต้นสำหรับรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="bf8e1-191">The default filters for the Power BI report.</span></span>                                                                 |
