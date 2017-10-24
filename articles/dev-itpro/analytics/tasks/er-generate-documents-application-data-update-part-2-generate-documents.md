--- 
title: "สร้างเอกสารที่มีการอัพเดตข้อมูลใบสมัครสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน สร้างเอกสารที่มีการอัพเดตข้อมูลแอพลิเคชัน (ส่วนที่ 1: นำเข้าการตั้งค่าคอนฟิก) ของ ER ให้เสร็จเรียบร้อยก่อน"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c724ce3c39ed7097a5a842b44a095628dcdfa131
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="5aa3e-103">สร้างเอกสารที่มีการอัพเดตข้อมูลใบสมัครสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="5aa3e-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5aa3e-104">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน สร้างเอกสารที่มีการอัพเดตข้อมูลแอพลิเคชัน (ส่วนที่ 1: นำเข้าการตั้งค่าคอนฟิก) ของ ER ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="5aa3e-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="5aa3e-105">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5aa3e-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="5aa3e-106">ในกระบวนงานนี้ คุณจะเรียกใช้การตั้งค่าคอนฟิกรูปแบบที่นำเข้าของ ER ที่สร้างขึ้นสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5aa3e-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="5aa3e-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5aa3e-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5aa3e-108">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="5aa3e-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="5aa3e-109">ก่อนที่คุณจะเริ่มต้น ให้เปลี่ยนบริบทประเทศสำหรับบริษัท DEMF จาก DEU (เยอรมนี) เป็น BEL (เบลเยียม)</span><span class="sxs-lookup"><span data-stu-id="5aa3e-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="5aa3e-110">คลิก การจัดการองค์กร > องค์กร > นิติบุคคลเพื่ออัพเดตรหัสประเทศในที่อยู่หลักของนิติบุคคล DEMF</span><span class="sxs-lookup"><span data-stu-id="5aa3e-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="5aa3e-111">รีสตาร์ทแอพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="5aa3e-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="5aa3e-112">เรียกใช้รูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="5aa3e-112">Run imported ER format</span></span>
1. <span data-ttu-id="5aa3e-113">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="5aa3e-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5aa3e-114">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="5aa3e-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="5aa3e-115">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (รูปแบบ)'</span><span class="sxs-lookup"><span data-stu-id="5aa3e-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="5aa3e-116">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="5aa3e-116">Click Run.</span></span>
    * <span data-ttu-id="5aa3e-117">เรียกใช้เวอร์ชันแบบร่างของการตั้งค่าคอนฟิกรูปแบบ ER เพื่อสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="5aa3e-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="5aa3e-118">ในฟิลด์ป้อนชื่อไฟล์ พิมพ์ 'intrastat.xml'</span><span class="sxs-lookup"><span data-stu-id="5aa3e-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="5aa3e-119">ระบุชื่อของไฟล์</span><span class="sxs-lookup"><span data-stu-id="5aa3e-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="5aa3e-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5aa3e-120">Click OK.</span></span>
    * <span data-ttu-id="5aa3e-121">ตรวจทานไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5aa3e-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="5aa3e-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5aa3e-122">Close the page.</span></span>
8. <span data-ttu-id="5aa3e-123">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="5aa3e-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="5aa3e-124">เปิดแบบฟอร์มนี้เพื่อดูธุรกรรมอินทราสแทตที่รวมอยู่ในเอกสารทางอิเล็กทรอนิกส์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5aa3e-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="5aa3e-125">คลิก ที่เก็บถาวรของอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="5aa3e-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="5aa3e-126">เนื่องจากรูปแบบ ER ที่มีการดำเนินการไม่ได้ประกอบด้วยการตั้งค่าใด ๆ สำหรับการอัพเดตข้อมูลแอพลิเคชัน รายละเอียดของรายงานอินทราสแทตที่เสร็จสมบูรณ์แล้วจึงไม่ได้ถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="5aa3e-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="5aa3e-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5aa3e-127">Close the page.</span></span>
11. <span data-ttu-id="5aa3e-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5aa3e-128">Close the page.</span></span>


