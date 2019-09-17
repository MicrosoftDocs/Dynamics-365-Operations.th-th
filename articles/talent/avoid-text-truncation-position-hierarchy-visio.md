---
title: หลีกเลี่ยงการตัดข้อความในลำดับชั้นของตำแหน่งและส่งออกไปยัง Visio
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งชื่อของรายการแต่ละรายการและตำแหน่งถูกตัด เมื่อลูกค้าดูลำดับชั้นตำแหน่งใน Microsoft Dynamics 365 for Talent การตัดข้อความสามารถทำให้ยากในการจับภาพหน้าจอหรือพิมพ์ลำดับชั้น
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 07a972bc1c6dd4076932248edb314992cb7297e5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741832"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="b79de-104">หลีกเลี่ยงการตัดข้อความในลำดับชั้นของตำแหน่งและส่งออกไปยัง Visio</span><span class="sxs-lookup"><span data-stu-id="b79de-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b79de-105">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="b79de-105">**Issue**</span></span>

<span data-ttu-id="b79de-106">เมื่อลูกค้าดูลำดับชั้นตำแหน่งใน Microsoft Dynamics 365 for Talent ชื่อของรายการแต่ละรายการและตำแหน่งถูกตัด</span><span class="sxs-lookup"><span data-stu-id="b79de-106">When a customer views the position hierarchy in Microsoft Dynamics 365 for Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="b79de-107">ดังนั้น จึงอาจจะยากในการจับภาพหน้าจอ หรือในการพิมพ์และเผยแพร่ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="b79de-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![ลำดับชั้นของตำแหน่งงาน](media/position-h.png)

<span data-ttu-id="b79de-109">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="b79de-109">**Cause**</span></span>

<span data-ttu-id="b79de-110">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b79de-110">This behavior is by design.</span></span>

<span data-ttu-id="b79de-111">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="b79de-111">**Resolution**</span></span>

<span data-ttu-id="b79de-112">โชคไม่ดี ผู้ใช้ไม่สามารถเปลี่ยนขนาดของข้อความได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="b79de-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="b79de-113">อย่างไรก็ตาม คุณสามารถส่งออกลำดับชั้นของตำแหน่งจาก Talent และจากนั้นนำเข้าไปยัง Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="b79de-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="b79de-114">ถึงแม้ว่าบทความต่อไปนี้จะถูกเขียนสำหรับ Microsoft Dynamics AX 2012 กระบวนการยังคงถูกนำไปใช้กับ Talent: [ส่งออกลำดับชั้นตำแหน่งไปยัง Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio)</span><span class="sxs-lookup"><span data-stu-id="b79de-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="b79de-115">ทำตามขั้นตอนเหล่านี้เพื่อส่งออกไปยัง Visio</span><span class="sxs-lookup"><span data-stu-id="b79de-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="b79de-116">ใน Talent เปิดหน้ารายการ **ตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="b79de-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="b79de-117">เพื่อรวมข้อมูลเพิ่มเติมในไดอะแกรมโครงสร้างองค์กร เพิ่มฟิลด์ไปยังรายการ **ตำแหน่ง** เพื่อให้พร้อมใช้งานเมื่อคุณใช้วิซาร์ดนี้ภายหลังในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="b79de-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="b79de-118">บนบานหน้าต่างการดำเนินการ เลือกปุ่ม **เปิดใน Microsoft Office** และจากนั้น ภายใต้ **ส่งออกไปยัง Excel** เลือก **ตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="b79de-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="b79de-119">อีกทางหนึ่งคือ กด Ctrl+T</span><span class="sxs-lookup"><span data-stu-id="b79de-119">Alternatively, press Ctrl+T.</span></span>

    ![ส่งออกหน้ารายการตำแหน่งไปยัง Excel](media/org-admin.png)

3. <span data-ttu-id="b79de-121">บันทึกไฟล์ Excel ที่ถูกส่งออก</span><span class="sxs-lookup"><span data-stu-id="b79de-121">Save the Excel file that is exported.</span></span>

    ![ส่งออกไปที่กล่องโต้ตอบ Excel](media/export-excel.png)

4. <span data-ttu-id="b79de-123">ใน Visio เลือก **Visio - สร้างใหม่** และเลือกประเภทเท็มเพลต **ธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="b79de-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![ไดอะแกรมใหม่](media/new.png)

5. <span data-ttu-id="b79de-125">เลือก **ตัวช่วยสร้างแผนภูมิองค์กร** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b79de-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![กล่องโต้ตอบตัวช่วยสร้างแผนภูมิองค์กร](media/orgchart-wizard.png)

6. <span data-ttu-id="b79de-127">เลือก **ข้อมูลที่ถูกเก็บอยู่ในไฟล์หรือฐานข้อมูลแล้ว** แล้วจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="b79de-129">เลือก **ข้อความ Org Plus (\*.txt) หรือไฟล์ Excel** แล้วจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="b79de-131">เรียกดูเพื่อเลือกแฟ้ม Excel ที่ส่งออกซึ่งประกอบด้วยลำดับชั้นของตำแหน่ง และจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="b79de-133">ตั้งค่าฟิลด์ **ชื่อ** เป็น **ตำแหน่ง** ตั้งค่าฟิลด์ **รายงานไปยัง** **รายงานไปยังตำแหน่ง** แล้วจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="b79de-135">เลือกฟิลด์ที่ควรจะแสดงบนแต่ละโหนด และจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="b79de-137">เพิ่มคอลัมน์ **ตำแหน่ง** ไปยังรายการ **ฟิลด์ข้อมูลรูปร่าง** และจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="b79de-139">รูปภาพไม่พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="b79de-139">Pictures aren't currently available.</span></span> <span data-ttu-id="b79de-140">ดังนั้น บนหน้าถัดไป เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="b79de-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="b79de-141">เลือก **ฉันต้องการให้วิซาร์ดแบ่งแผนผังองค์กรของฉันทั้งหน้าโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="b79de-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![ตัวช่วยสร้างแผนภูมิองค์กร 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="b79de-143">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="b79de-143">Select **Finish**.</span></span>

    <span data-ttu-id="b79de-144">ถ้ามีตำแหน่งใดๆ ที่ไม่ได้อยู่ในโครงสร้าง คุณจะถูกขอให้รวมรายการเหล่านั้นไว้ในไดอะแกรม</span><span class="sxs-lookup"><span data-stu-id="b79de-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="b79de-145">ไดอะแกรมที่ถูกสร้างขึ้นใน Visio แสดงผู้จัดการแต่ละรายบนแผ่นงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="b79de-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="b79de-146">ขึ้นอยู่กับฟิลด์ที่คุณเลือกที่จะรวมไว้ในไดอะแกรม โหนดแต่ละโหนดแสดงข้อมูลที่เหมาะสม เมื่อมีการสร้างไฟล์ Visio</span><span class="sxs-lookup"><span data-stu-id="b79de-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![ไดอะแกรมลำดับชั้น](media/hierarchy.png)

<span data-ttu-id="b79de-148">**ตัวเลือกเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="b79de-148">**Additional option**</span></span>

<span data-ttu-id="b79de-149">ใน Talent คุณยังอาจจะสามารถใช้พื้นที่ทำงาน **ผู้คน** เพื่อดูข้อมูลบางอย่างที่เกี่ยวข้องกับลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="b79de-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
