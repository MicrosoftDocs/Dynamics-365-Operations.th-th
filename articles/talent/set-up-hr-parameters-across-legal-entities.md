---
title: ตั้งค่าพารามิเตอร์ทรัพยากรบุคคล (HR) ทั่วทั้งนิติบุคคล
description: คุณต้องตั้งค่าพารามิเตอร์ที่ใช้ร่วมกันสำหรับเรกคอร์ดที่ใช้ร่วมกันระหว่างบริษัท เช่นเรกคอร์ดตำแหน่ง บทความนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ทรัพยากรบุคคลสำหรับนิติบุคคล
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306349"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="f11db-104">ตั้งค่าพารามิเตอร์ทรัพยากรบุคคล (HR) ทั่วทั้งนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="f11db-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f11db-105">คุณต้องตั้งค่าพารามิเตอร์ที่ใช้ร่วมกันสำหรับเรกคอร์ดที่ใช้ร่วมกันระหว่างบริษัท เช่นเรกคอร์ดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="f11db-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="f11db-106">บทความนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ทรัพยากรบุคคลสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="f11db-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="f11db-107">บางชนิดของเรกคอร์ด เช่น เรกคอร์ดตำแหน่ง ถูกใช้ร่วมกันระหว่างบริษัทต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="f11db-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="f11db-108">สำหรับเรกคอร์ดเหล่านี้ คุณต้องตั้งค่าพารามิเตอร์ที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f11db-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="f11db-109">ตัวอย่างเช่น คุณใช้หน้า **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล** เพื่อตั้งค่าพารามิเตอร์ทรัพยากรบุคคลสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="f11db-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="f11db-110">ในหน้า **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล** พารามิเตอร์จะถูกจัดกลุ่มเป็นพื้นที่ ตามแต่ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="f11db-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="f11db-111">ฟังก์ชันที่นำออกใช้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f11db-111">Previously released functionality</span></span>
<span data-ttu-id="f11db-112">ในแท็บ **การระบุรหัสประจำตัว** คุณต้องเลือกชนิดการระบุรหัสประจำตัวที่แสดงถึงหมายเลขการระบุรหัสประจำตัวที่ถูกแสดงอยู่บนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="f11db-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="f11db-113">คุณต้องตั้งค่าชนิดการระบุรหัสประจำตัวก่อนคุณจะสามารถป้อนข้อมูลการระบุรหัสประจำตัวสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f11db-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="f11db-114">ข้อมูลเกี่ยวกับหมายเลขประกันสังคม หมายเลขรหัสประจำตัวประชาชน หมายเลขรหัสประจำตัวคนต่างด้าว และรหัสส่วนบุคคลในหน้า **ชนิดการระบุรหัสประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="f11db-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="f11db-115">การกำหนดชนิดการระบุรหัสประจำตัวใหม่ หรือตรวจทานรายการของชนิดที่มีอยู่ คลิก **การจัดการบุคลากร** &gt; **แท็บลิงก์** &gt; **การตั้งค่า** &gt; **ชนิดการระบุรหัสประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="f11db-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="f11db-116">คุณสามารถป้อนรหัสแบบง่ายและคำอธิบายได้</span><span class="sxs-lookup"><span data-stu-id="f11db-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="f11db-117">ถ้าคุณกำลังใช้ Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="f11db-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="f11db-118">ในแท็บ **การระบุรหัสประจำตัว** คุณต้องเลือกชนิดการระบุรหัสประจำตัวที่แสดงถึงหมายเลขการระบุรหัสประจำตัวที่ถูกแสดงอยู่บนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="f11db-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="f11db-119">คุณต้องตั้งค่าชนิดการระบุรหัสประจำตัวก่อนคุณจะสามารถป้อนข้อมูลการระบุรหัสประจำตัวสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f11db-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="f11db-120">ข้อมูลเกี่ยวกับหมายเลขประกันสังคม หมายเลขรหัสประจำตัวประชาชน หมายเลขรหัสประจำตัวคนต่างด้าว และรหัสส่วนบุคคลในหน้า **ชนิดการระบุรหัสประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="f11db-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="f11db-121">การกำหนดชนิดการระบุรหัสประจำตัวใหม่ หรือตรวจทานรายการของชนิดที่มีอยู่ คลิก **ทรัพยากรบุคคล** &gt; **ตั้งค่า** &gt; **ชนิดการระบุรหัสประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="f11db-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="f11db-122">คุณสามารถป้อนรหัสแบบง่ายและคำอธิบายได้</span><span class="sxs-lookup"><span data-stu-id="f11db-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="f11db-123">ในแท็บ **ลำดับหมายเลข** คุณสามารถเลือกลำดับหมายเลขที่ถูกใช้สำหรับเรกคอร์ดต่อไปนี้: หมายเลขบุคลากร ตำแหน่ง รหัสคำขอของผู้ใช้ เอกสาร I-9 ผู้สมัคร การสนทนา รหัสสวัสดิการ และการดำเนินการด้านบุคลากร (ถ้าเรกคอร์ดชนิดนี้ถูกเปิดใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="f11db-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="f11db-124">การรักษาการอ้างอิงลำดับหมายเลขและรหัส ใช้หน้ารายการ **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="f11db-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="f11db-125">การค้นหาหน้านี้ ใช้คุณลักษณะการค้นหาหน้า</span><span class="sxs-lookup"><span data-stu-id="f11db-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="f11db-126">ในแท็บ **ตำแหน่ง** บ่งชี้ว่าตำแหน่งใหม่จะพร้อมใช้งานหรือไม่สำหรับการกำหนดโดยค่าเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="f11db-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="f11db-127">**ตลอดเวลา** – คุณไม่สามารถมอบหมายผู้ปฏิบัติงานไปยังตำแหน่งใหม่เมื่อตำแหน่งนั้นถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="f11db-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="f11db-128">เมื่อตำแหน่งดังกล่าวถูกสร้างขึ้น วันที่และเวลาของ **ความพร้อมในการกำหนด** ในแท็บ **ทั่วไป** ของ**ตำแหน่ง** จะถูกตั้งค่าโดยอัตโนมัติเป็นวันที่และเวลาที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="f11db-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="f11db-129">**ไม่มีวัน** – คุณไม่สามารถมอบหมายผู้ปฏิบัติงานไปยังตำแหน่งใหม่เมื่อตำแหน่งนั้นถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="f11db-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="f11db-130">ถ้าคุณเลือกตัวเลือกนี้ คุณต้องเปิดหน้า **ตำแหน่ง** สำหรับแต่ละตำแหน่งใหม่เมื่อพร้อมใช้งาน จากนั้น ในแท็บ **ทั่วไป** ป้อนวันที่ **พร้อมใช้งานสำหรับการกำหนด**เพื่อเปิดใช้งานการกำหนดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f11db-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="f11db-131">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f11db-131">Additional resources</span></span>
--------

[<span data-ttu-id="f11db-132">ตั้งค่าพารามิเตอร์ทรัพยากรบุคคลเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="f11db-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)



