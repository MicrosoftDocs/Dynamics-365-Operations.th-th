---
title: การรวมบันทึก
description: หัวข้อนี้อธิบายการรวมข้อมูลบันทึกแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018397"
---
# <a name="note-integration"></a><span data-ttu-id="06ea7-103">การรวมบันทึก</span><span class="sxs-lookup"><span data-stu-id="06ea7-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="06ea7-104">ในระหว่างกระบวนการทางธุรกิจ ผู้ใช้ Microsoft Dynamics 365 มักรวบรวมข้อมูลเกี่ยวกับลูกค้าของตน</span><span class="sxs-lookup"><span data-stu-id="06ea7-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="06ea7-105">ข้อมูลนี้จะบันทึกเป็นกิจกรรมและบันทึก</span><span class="sxs-lookup"><span data-stu-id="06ea7-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="06ea7-106">หัวข้อนี้อธิบายการรวมข้อมูลบันทึกแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="06ea7-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="06ea7-107">ข้อมูลลูกค้าสามารถจัดประเภทได้ในลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06ea7-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="06ea7-108">**ข้อมูลที่สามารถดำเนินการได้ซึ่งผู้ใช้ Dynamics 365 จะจัดการในนามของลูกค้า** – ตัวอย่างเช่น Contoso (ผู้ใช้ Dynamics 365) ได้ดำเนินการจัดรายการเกมโชว์</span><span class="sxs-lookup"><span data-stu-id="06ea7-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="06ea7-109">ลูกค้ารายหนึ่งของ Contoso (ลูกค้า) ต้องการเข้าร่วมเกมโชว์</span><span class="sxs-lookup"><span data-stu-id="06ea7-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="06ea7-110">ลูกค้าขอให้พนักงาน Contoso จองช่องในเกมโชว์ให้พวกเขา</span><span class="sxs-lookup"><span data-stu-id="06ea7-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="06ea7-111">การจองจะเกิดขึ้นในปฏิทินของผู้เข้าร่วมเหตุการณ์ Contoso</span><span class="sxs-lookup"><span data-stu-id="06ea7-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="06ea7-112">**ข้อมูลที่สามารถนําไปปฏิบัติได้กับผู้ใช้ Dynamics 365**  – ตัวอย่างเช่น ลูกค้าที่ซื้อหน่วย Surface จะป้อนคําแนะนําพิเศษที่บ่งชี้ว่าอุปกรณ์ควรมีการห่อของขวัญ ก่อนการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="06ea7-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="06ea7-113">คําแนะนําเหล่านี้เป็นข้อมูลที่สามารถปฏิบัติการได้ซึ่งควรจัดการโดยพนักงาน Contoso ที่รับผิดชอบบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06ea7-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="06ea7-114">**ข้อมูลที่ไม่สามารถดำเนินการได้** – ตัวอย่างเช่น ลูกค้าไปที่ร้านค้า Contoso และในระหว่างการสนทนากับพนักงานขายของร้านค้า จะแสดงความสนใจในเกม *Halo* และอุปกรณ์เสริมสำหรับเล่นเกม</span><span class="sxs-lookup"><span data-stu-id="06ea7-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="06ea7-115">พนักงานขายของร้านค้าได้ออกบันทึกข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="06ea7-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="06ea7-116">จากนั้นกลไกจัดการความคิดเห็นเกี่ยวกับผลิตภัณฑ์จะใช้กลไกจัดการการแนะนำผลิตภัณฑ์เพื่อแนะนำลูกค้า</span><span class="sxs-lookup"><span data-stu-id="06ea7-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="06ea7-117">โดยทั่วไป ข้อมูลที่สามารถดำเนินการได้จะรวบรวมไว้เป็น *กิจกรรม* ในแอป Finance and Operations และแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="06ea7-118">ข้อมูลที่ไม่สามารถดำเนินการได้จะรวบรวมไว้เป็น *บันทึก* ในแอป Finance and Operations และเป็น *คำอธิบาย* ในแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="06ea7-119">แม้ว่าบันทึกจะใช้เพื่อข้อมูลที่ไม่สามารถดำเนินการได้ แต่แอปจะไม่ป้องกันคุณจากการใช้บันทึกเหล่านั้นเพื่อจัดเก็บและจัดการข้อมูลที่สามารถดำเนินการได้หากคุณต้องการใช้บันทึกเหล่านั้นในลักษณะนั้น</span><span class="sxs-lookup"><span data-stu-id="06ea7-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="06ea7-120">ปัจจุบัน Microsoft มีการปล่อยการใช้งานฟังก์ชันการรวมบันทึก</span><span class="sxs-lookup"><span data-stu-id="06ea7-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="06ea7-121">(ฟังก์ชันของการรวมกิจกรรมจะปล่อยออกใช้ในภายหลัง) การรวมบันทึกจะพร้อมใช้งานเฉพาะกับลูกค้า ผู้จัดจำหน่าย ใบสั่งขาย และใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="06ea7-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="06ea7-122">สร้างบันทึกในแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="06ea7-123">หากต้องการสร้างบันทึกในแอป Customer Engagement และซิงค์บันทึกนั้นกับแอป Finance and Operations ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06ea7-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="06ea7-124">ในแอป Customer Engagement ให้เปิดเรกคอร์ดบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="06ea7-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="06ea7-125">ในบานหน้าต่าง **เส้นเวลา** ให้เลือกเครื่องหมายบวก (**+**) แล้วเลือก **บันทึก** เพื่อสร้างบันทึก</span><span class="sxs-lookup"><span data-stu-id="06ea7-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![สร้างบันทึกในแอป Customer Engagement](media/notes-ce-1.png)

3. <span data-ttu-id="06ea7-127">ป้อนชื่อเรื่องและคำอธิบาย แล้วเลือก **เพิ่มบันทึก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-127">Enter a title and description, and then select **Add note**.</span></span>

    ![ป้อนหัวข้อและคำอธิบาย](media/notes-ce-2.png)

    <span data-ttu-id="06ea7-129">บันทึกใหม่จะเพิ่มลงในเส้นเวลาของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="06ea7-129">The new note is added to the customer timeline.</span></span>

    ![บันทึกใหม่ในเส้นเวลาของลูกค้า](media/notes-ce-3.png)

4. <span data-ttu-id="06ea7-131">ลงชื่อเข้าใช้แอป Finance and Operations แล้วเปิดเรกคอร์ดลูกค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="06ea7-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="06ea7-132">โปรดสังเกตว่าปุ่ม **เอกสารแนบ** (สัญลักษณ์ที่หนีบกระดาษ) ในมุมด้านขวาบน บ่งชี้ว่าเรกคอร์ดมีเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="06ea7-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![การแจ้งเตือนเกี่ยวกับเอกสารแนบ](media/notes-ce-4.png)

5. <span data-ttu-id="06ea7-134">เลือกปุ่ม **เอกสารแนบ** เพื่อเปิดหน้า **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="06ea7-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="06ea7-135">คุณควรค้นหาบันทึกที่คุณสร้างไว้ในแอปพลิเคชัน Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-135">You should find the note that you created in the customer engagement app.</span></span>

    ![บันทึกจากแอป Customer Engagement](media/notes-ce-5.png)

<span data-ttu-id="06ea7-137">การอัพเดตใดๆ ในบันทึกจะมีการซิงค์กลับไปกลับมาระหว่างแอป Finance and Operations และแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="06ea7-138">สร้างบันทึกในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06ea7-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="06ea7-139">คุณสามารถสร้างบันทึกในแอป Finance and Operations และจะซิงค์บันทึกนั้นกับแอป Customer Engagement </span><span class="sxs-lookup"><span data-stu-id="06ea7-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="06ea7-140">ในการสร้างบันทึกในแอป Finance and Operations และซิงค์บันทึกนั้นกับแอป Customer Engagement ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06ea7-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="06ea7-141">ในแอป Finance and Operations ในหน้า **เอกสารแนบ** ให้เลือก **ใหม่**\> **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![สร้างบันทึกในแอป Finance and Operations](media/notes-fo-1.png)

2. <span data-ttu-id="06ea7-143">ป้อนชื่อเรื่องและชุดคําแนะนําสั้นๆ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![ป้อนหัวข้อและคำแนะนำ](media/notes-fo-2.png)

3. <span data-ttu-id="06ea7-145">ในแอปพลิเคชัน Customer Engagement ให้อัพเดตเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="06ea7-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="06ea7-146">คุณควรค้นหาบันทึกใหม่ในเส้นเวลา</span><span class="sxs-lookup"><span data-stu-id="06ea7-146">You should find the new note on the timeline.</span></span>

    ![บันทึกใหม่ในเส้นเวลาในแอป Customer Engagement](media/notes-fo-3.png)

<span data-ttu-id="06ea7-148">คุณสามารถจัดประเภทบันทึกเป็นบันทึกภายในหรือภายนอก</span><span class="sxs-lookup"><span data-stu-id="06ea7-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="06ea7-149">ในแอป Finance and Operations ในหน้า **เอกสารแนบ** ให้เปิดบันทึก แล้วในฟิลด์ **ข้อจํากัด** ให้เลือก **ภายใน** หรือ **ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![ฟิลด์ข้อจํากัด](media/notes-fo-4.png)

<span data-ttu-id="06ea7-151">คุณยังสามารถสร้าง URL ได้</span><span class="sxs-lookup"><span data-stu-id="06ea7-151">You can also create a URL.</span></span>

1. <span data-ttu-id="06ea7-152">ในแอป Finance and Operations ในหน้า **เอกสารแนบ** ให้เลือก **ใหม่**\> **URL**</span><span class="sxs-lookup"><span data-stu-id="06ea7-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="06ea7-153">ป้อนหัวข้อและ URL</span><span class="sxs-lookup"><span data-stu-id="06ea7-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="06ea7-154">ในฟิลด์ **ข้อจํากัด** ให้เลือก **ภายใน** หรือ **ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![สร้าง URL ในแอป Finance and Operations](media/notes-fo-5.png)

4. <span data-ttu-id="06ea7-156">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="06ea7-156">Select **Save**.</span></span>

    <span data-ttu-id="06ea7-157">เนื่องจากแอป Customer Engagement ไม่มีชนิด URL URL จะรวมเข้ากับการเขียนแบบคู่เป็นบันทึก</span><span class="sxs-lookup"><span data-stu-id="06ea7-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL ที่ปรากฏเป็นบันทึกในแอป Customer Engagement](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="06ea7-159">ไม่สนับสนุนเอกสารแนบไฟล์</span><span class="sxs-lookup"><span data-stu-id="06ea7-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="06ea7-160">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="06ea7-160">Templates</span></span>

<span data-ttu-id="06ea7-161">การรวมบันทึกประกอบด้วยชุดของแผนที่ตารางที่ทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06ea7-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="06ea7-162">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06ea7-162">Finance and Operations app</span></span> | <span data-ttu-id="06ea7-163">แอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="06ea7-163">Customer engagement app</span></span> | <span data-ttu-id="06ea7-164">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="06ea7-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="06ea7-165">เอกสารแนบของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="06ea7-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="06ea7-166">คำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="06ea7-166">Annotations</span></span> | <span data-ttu-id="06ea7-167">ธุรกิจที่ใช้ข้อความธรรมดาและ URL เพื่อรวบรวมข้อมูลเฉพาะลูกค้า (สำหรับทั้งองค์กรและบุคคล)</span><span class="sxs-lookup"><span data-stu-id="06ea7-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="06ea7-168">สิ่งที่แนบของเอกสารสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="06ea7-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="06ea7-169">คำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="06ea7-169">Annotations</span></span> | <span data-ttu-id="06ea7-170">ธุรกิจที่ใช้ข้อความธรรมดาและ URL เพื่อรวบรวมข้อมูลเฉพาะผู้จัดจำหน่าย (สำหรับทั้งองค์กรและบุคคล)</span><span class="sxs-lookup"><span data-stu-id="06ea7-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="06ea7-171">เอกสารแนบส่วนหัวของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="06ea7-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="06ea7-172">คำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="06ea7-172">Annotations</span></span> | <span data-ttu-id="06ea7-173">ธุรกิจที่ใช้ข้อความธรรมดาและ URL เพื่อรวบรวมข้อมูลเฉพาะใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="06ea7-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="06ea7-174">เอกสารแนบส่วนหัวของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="06ea7-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="06ea7-175">คำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="06ea7-175">Annotations</span></span> | <span data-ttu-id="06ea7-176">ธุรกิจที่ใช้ข้อความธรรมดาและ URL เพื่อรวบรวมข้อมูลเฉพาะใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="06ea7-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="06ea7-177">สำหรับข้อมูลเพิ่มเติม ให้ดูที่  [การอ้างอิงการทำแผนที่แบบสองทิศทาง](mapping-reference.md)</span><span class="sxs-lookup"><span data-stu-id="06ea7-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
