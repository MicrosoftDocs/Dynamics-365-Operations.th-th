---
title: ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: หัวข้อนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์ (ส่วนที่ 1 - นำเข้าการตั้งค่าคอนฟิก)
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 417c419dc6925bac337fe74a2f057395316ec75d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092933"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="1e492-104">ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1e492-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e492-105">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน สร้างเอกสารที่มีการอัพเดตข้อมูลแอพลิเคชัน (ส่วนที่ 1: นำเข้าการตั้งค่าคอนฟิก) ของ ER ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="1e492-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="1e492-106">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1e492-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="1e492-107">ในกระบวนงานนี้ คุณจะเรียกใช้การตั้งค่าคอนฟิกรูปแบบที่นำเข้าของ ER ที่สร้างขึ้นสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1e492-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="1e492-108">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1e492-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="1e492-109">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="1e492-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="1e492-110">ก่อนที่คุณจะเริ่มต้น ให้เปลี่ยนบริบทประเทศสำหรับบริษัท DEMF จาก DEU (เยอรมนี) เป็น BEL (เบลเยียม)</span><span class="sxs-lookup"><span data-stu-id="1e492-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="1e492-111">คลิก การจัดการองค์กร > องค์กร > นิติบุคคลเพื่ออัพเดตรหัสประเทศในที่อยู่หลักของนิติบุคคล DEMF</span><span class="sxs-lookup"><span data-stu-id="1e492-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="1e492-112">รีสตาร์ทแอพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="1e492-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="1e492-113">เรียกใช้รูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="1e492-113">Run imported ER format</span></span>
1. <span data-ttu-id="1e492-114">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="1e492-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1e492-115">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="1e492-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="1e492-116">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (รูปแบบ)'</span><span class="sxs-lookup"><span data-stu-id="1e492-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="1e492-117">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="1e492-117">Click Run.</span></span>
    * <span data-ttu-id="1e492-118">เรียกใช้เวอร์ชันแบบร่างของการตั้งค่าคอนฟิกรูปแบบ ER เพื่อสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="1e492-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="1e492-119">ในฟิลด์ป้อนชื่อไฟล์ พิมพ์ 'intrastat.xml'</span><span class="sxs-lookup"><span data-stu-id="1e492-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="1e492-120">ระบุชื่อของไฟล์</span><span class="sxs-lookup"><span data-stu-id="1e492-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="1e492-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1e492-121">Click OK.</span></span>
    * <span data-ttu-id="1e492-122">ตรวจทานไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1e492-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="1e492-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1e492-123">Close the page.</span></span>
8. <span data-ttu-id="1e492-124">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="1e492-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="1e492-125">เปิดแบบฟอร์มนี้เพื่อดูธุรกรรมอินทราสแทตที่รวมอยู่ในเอกสารทางอิเล็กทรอนิกส์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1e492-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="1e492-126">คลิก ที่เก็บถาวรของอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="1e492-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="1e492-127">เนื่องจากรูปแบบ ER ที่มีการดำเนินการไม่ได้ประกอบด้วยการตั้งค่าใด ๆ สำหรับการอัพเดตข้อมูลแอพลิเคชัน รายละเอียดของรายงานอินทราสแทตที่เสร็จสมบูรณ์แล้วจึงไม่ได้ถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="1e492-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="1e492-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1e492-128">Close the page.</span></span>
11. <span data-ttu-id="1e492-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1e492-129">Close the page.</span></span>

