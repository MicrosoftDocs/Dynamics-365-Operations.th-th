--- 
title: "ตั้งค่าคอนฟิกปลายทางสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "กระบวนงานนี้สาธิตวิธีการตั้งค่าและการใช้ปลายทางที่ต่างกัน สำหรับส่วนประกอบเอาท์พุทของการรายงานทางอิเล็กทรอนิกส์ (ER) เช่น โฟลเดอร์ หรือไฟล์ "
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1187448393e4905ed5f2dfe826ec843fdcf0cb67
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="configure-destinations-for-electronic-reporting-er"></a><span data-ttu-id="8eee9-103">ตั้งค่าคอนฟิกปลายทางสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="8eee9-103">Configure destinations for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8eee9-104">กระบวนงานนี้สาธิตวิธีการตั้งค่าและการใช้ปลายทางที่ต่างกัน สำหรับส่วนประกอบเอาท์พุทของการรายงานทางอิเล็กทรอนิกส์ (ER) เช่น โฟลเดอร์ หรือไฟล์ </span><span class="sxs-lookup"><span data-stu-id="8eee9-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="8eee9-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="8eee9-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="8eee9-106">ประเทศเยอรมนีเป็นประเทศ/ภูมิภาคของที่อยู่หลักของนิติบุคคล อย่างไรก็ตาม คุณสามารถใช้นิติบุคคลใดๆ สำหรับกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="8eee9-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="8eee9-107">รูปแบบที่ใช้ในตัวอย่างนี้คือ การโอนย้ายเครดิต (DE) ISO20022 แต่คุณสามารถใช้รูปแบบใดๆ ที่คุณได้นำเข้ามาแล้วได้ </span><span class="sxs-lookup"><span data-stu-id="8eee9-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="8eee9-108">โปรดทราบว่า กระบวนงานนี้เป็นตัวอย่างของไฟล์เดี่ยวและการตั้งค่าปลายทางเดี่ยว </span><span class="sxs-lookup"><span data-stu-id="8eee9-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="8eee9-109">ข้อมูลเพิ่มเติมเกี่ยวกับการจัดการปลายทางของการรายงานทางอิเล็กทรอนิกส์ สามารถพบได้ในวิธีใช้ของ Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8eee9-109">More information about Electronic reporting destination management can be found in the Dynamics 365 for Finance and Operations Help.</span></span>

1. <span data-ttu-id="8eee9-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > ปลายทางการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="8eee9-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="8eee9-111">คลิก ใหม่ เพื่อสร้างชุดใหม่ของปลายทางสำหรับรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8eee9-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="8eee9-112">ในฟิลด์การอ้างอิง ให้เลือกรูปแบบสำหรับรายการที่คุณต้องการตั้งค่าคอนฟิกปลายทาง</span><span class="sxs-lookup"><span data-stu-id="8eee9-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="8eee9-113">ถ้าคุณไม่มีค่าที่จะเลือก แสดงว่าคุณไม่ได้นำเข้าการตั้งค่าคอนฟิกรูปแบบการรายงานอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="8eee9-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="8eee9-114">คุณต้องนำเข้าการตั้งค่าคอนฟิกรูปแบบ ก่อนการตั้งค่าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="8eee9-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="8eee9-115">คลิก สร้าง เพื่อสร้างปลายทางของไฟล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="8eee9-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="8eee9-116">โปรดทราบว่าคุณสามารถสร้างปลายทางไฟล์หนึ่งแห่งได้อย่างไรสำหรับแต่ละส่วนประกอบเอาท์พุทของรูปแบบเดียวกัน เช่น โฟลเดอร์ หรือไฟล์ </span><span class="sxs-lookup"><span data-stu-id="8eee9-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="8eee9-117">คุณจะสามาระเปิดใช้งานและปิดใช้งานปลายทางโดยแยกกันในการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8eee9-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="8eee9-118">ในฟิลด์ชื่อ ให้ป้อนชื่อที่เป็นมิตรของผู้ใช้ของส่วนประกอบเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="8eee9-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="8eee9-119">เราขอแนะนำให้คุณตั้งชื่อที่มีความหมาย เช่น "ไฟล์การชำระเงิน" หรือ "รายงานการควบคุม" </span><span class="sxs-lookup"><span data-stu-id="8eee9-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="8eee9-120">ชื่อเหล่านี้จะถูกแสดงไปยังผู้ใช้ที่รันไทม์ของการตั้งค่าคอนฟิก พร้อมกับการตั้งค่าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="8eee9-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="8eee9-121">ในชื่อไฟล์ ให้เลือกไฟล์หรือโฟลเดอร์ที่เป็นข้อมูลเฉพาะของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8eee9-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="8eee9-122">คลิกการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8eee9-122">Click Settings.</span></span>
8. <span data-ttu-id="8eee9-123">เลือก ใช่ ในฟิลด์ เปิดใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="8eee9-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="8eee9-124">กล่องกาเครื่องหมายที่เปิดใช้งานบนแท็บแต่ละแท็บ จะเปิดใช้การงานและปิดการใช้งานปลายทางแต่ละแห่งโดยแยกกัน </span><span class="sxs-lookup"><span data-stu-id="8eee9-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="8eee9-125">ในตัวอย่างนี้ คุณจะเปิดใช้งานการส่งไฟล์เอาท์พุทไปยังผู้รับเมล์ เมื่อมีการสร้างไฟล์</span><span class="sxs-lookup"><span data-stu-id="8eee9-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="8eee9-126">คลิกแก้ไข เพื่อตั้งค่าผู้รับอีเมล</span><span class="sxs-lookup"><span data-stu-id="8eee9-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="8eee9-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="8eee9-127">Click Add.</span></span>
11. <span data-ttu-id="8eee9-128">คลิก พิมพ์อีเมลการจัดการ</span><span class="sxs-lookup"><span data-stu-id="8eee9-128">Click Print Management email.</span></span>
12. <span data-ttu-id="8eee9-129">ในฟิลด์ แหล่งที่มาอีเมล ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8eee9-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="8eee9-130">คุณสามารถเลือกชนิดแหล่งที่มาอีเมลอื่น เช่น ชนิดลูกค้าหรือผู้จัดจำหน่าย ได้ </span><span class="sxs-lookup"><span data-stu-id="8eee9-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="8eee9-131">ซึ่งจะบ่งชี้ชนิดของอาร์กิวเมนต์ที่ถูกส่งคืนโดยสูตรของบัญชีแหล่งที่มาอีเมล </span><span class="sxs-lookup"><span data-stu-id="8eee9-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="8eee9-132">สูตรของบัญชีแหล่งที่มาอีเมลที่อธิบายในขั้นตอนต่อไปนี้ คือที่ซึ่งคุณจะผูกข้อมูลแหล่งที่มาอีเมล </span><span class="sxs-lookup"><span data-stu-id="8eee9-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="8eee9-133">เลือกผู้จัดจำหน่าย ถ้าสูตรของคุณจะส่งคืนไปยังบัญชีผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="8eee9-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="8eee9-134">ใช้ผู้จัดจำหน่าย ถ้าคุณกำลังใช้ตัวอย่างการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO 20022</span><span class="sxs-lookup"><span data-stu-id="8eee9-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="8eee9-135">คลิกปุ่มผูกข้อมูลแหล่งที่มาอีเมล</span><span class="sxs-lookup"><span data-stu-id="8eee9-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="8eee9-136">ในสูตร ให้ป้อนการอ้างอิงเฉพาะเอกสารไปยังชนิดฝ่ายที่คุณเลือกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8eee9-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="8eee9-137">แทนที่การพิมพ์ คุณสามารถหาโหนดแหล่งข้อมูลที่แสดงบัญชีฝ่ายได้ แล้วคลิกปุ่มเพิ่มแหล่งข้อมูลเพื่ออัพเดตสูตร </span><span class="sxs-lookup"><span data-stu-id="8eee9-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="8eee9-138">ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO 20022 โหนดที่แสดงบัญชีผู้จัดจำหน่ายคือ '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID</span><span class="sxs-lookup"><span data-stu-id="8eee9-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="8eee9-139">หรือ ป้อนค่าสตริงใดๆ เช่น "DE-001" เพื่อบันทึกสูตร</span><span class="sxs-lookup"><span data-stu-id="8eee9-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="8eee9-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8eee9-140">Click Save.</span></span>
16. <span data-ttu-id="8eee9-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8eee9-141">Close the page.</span></span>
17. <span data-ttu-id="8eee9-142">คลิกแก้ไขเพื่อตั้งค่าคอนฟิกรายละเอียดผู้ติดต่อสำหรับฝ่าย</span><span class="sxs-lookup"><span data-stu-id="8eee9-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="8eee9-143">เลือก ใช่ ในฟิลด์ผู้ติดต่อหลัก</span><span class="sxs-lookup"><span data-stu-id="8eee9-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="8eee9-144">คุณอาจใช้ตัวเลือกอื่นเพื่อบ่งชี้ว่าควรใช้ชนิดของผู้ติดต่อของฝ่ายใดเป็นที่อยู่อีเมสำหรับปลายทางนี้ </span><span class="sxs-lookup"><span data-stu-id="8eee9-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="8eee9-145">เราใช้ผู้ติดต่อหลักในตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="8eee9-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="8eee9-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8eee9-146">Click OK.</span></span>
20. <span data-ttu-id="8eee9-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8eee9-147">Click OK.</span></span>
21. <span data-ttu-id="8eee9-148">ในฟิลด์ชื่อเรื่อง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8eee9-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="8eee9-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8eee9-149">Click OK.</span></span>


