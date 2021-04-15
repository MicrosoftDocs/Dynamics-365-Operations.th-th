---
title: ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: หัวข้อนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์ (ส่วนที่ 1 - นำเข้าการตั้งค่าคอนฟิก)
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751093"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="325ce-104">ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="325ce-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="325ce-105">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน สร้างเอกสารที่มีการอัพเดตข้อมูลแอพลิเคชัน (ส่วนที่ 1: นำเข้าการตั้งค่าคอนฟิก) ของ ER ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="325ce-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="325ce-106">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="325ce-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="325ce-107">ในกระบวนงานนี้ คุณจะเรียกใช้การตั้งค่าคอนฟิกรูปแบบที่นำเข้าของ ER ที่สร้างขึ้นสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="325ce-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="325ce-108">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="325ce-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="325ce-109">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="325ce-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="325ce-110">ก่อนที่คุณจะเริ่มต้น ให้เปลี่ยนบริบทประเทศสำหรับบริษัท DEMF จาก DEU (เยอรมนี) เป็น BEL (เบลเยียม)</span><span class="sxs-lookup"><span data-stu-id="325ce-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="325ce-111">คลิก การจัดการองค์กร > องค์กร > นิติบุคคลเพื่ออัพเดตรหัสประเทศในที่อยู่หลักของนิติบุคคล DEMF</span><span class="sxs-lookup"><span data-stu-id="325ce-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="325ce-112">รีสตาร์ทแอพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="325ce-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="325ce-113">เรียกใช้รูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="325ce-113">Run imported ER format</span></span>
1. <span data-ttu-id="325ce-114">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="325ce-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="325ce-115">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="325ce-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="325ce-116">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (รูปแบบ)'</span><span class="sxs-lookup"><span data-stu-id="325ce-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="325ce-117">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="325ce-117">Click Run.</span></span>
    * <span data-ttu-id="325ce-118">เรียกใช้เวอร์ชันแบบร่างของการตั้งค่าคอนฟิกรูปแบบ ER เพื่อสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="325ce-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="325ce-119">ในฟิลด์ป้อนชื่อไฟล์ พิมพ์ 'intrastat.xml'</span><span class="sxs-lookup"><span data-stu-id="325ce-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="325ce-120">ระบุชื่อของไฟล์</span><span class="sxs-lookup"><span data-stu-id="325ce-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="325ce-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="325ce-121">Click OK.</span></span>
    * <span data-ttu-id="325ce-122">ตรวจทานไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="325ce-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="325ce-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="325ce-123">Close the page.</span></span>
8. <span data-ttu-id="325ce-124">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="325ce-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="325ce-125">เปิดแบบฟอร์มนี้เพื่อดูธุรกรรมอินทราสแทตที่รวมอยู่ในเอกสารทางอิเล็กทรอนิกส์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="325ce-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="325ce-126">คลิก ที่เก็บถาวรของอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="325ce-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="325ce-127">เนื่องจากรูปแบบ ER ที่มีการดำเนินการไม่ได้ประกอบด้วยการตั้งค่าใด ๆ สำหรับการอัพเดตข้อมูลแอพลิเคชัน รายละเอียดของรายงานอินทราสแทตที่เสร็จสมบูรณ์แล้วจึงไม่ได้ถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="325ce-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="325ce-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="325ce-128">Close the page.</span></span>
11. <span data-ttu-id="325ce-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="325ce-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]