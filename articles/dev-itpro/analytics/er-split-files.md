---
title: แบ่งไฟล์ XML ที่สร้างตามขนาดไฟล์และปริมาณเนื้อหา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการแบ่งไฟล์ที่สร้างตามขนาดไฟล์และปริมาณสินค้าในเนื้อหา
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "347111"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="14bd8-103">แบ่งไฟล์ XML ที่สร้างตามขนาดไฟล์และปริมาณเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="14bd8-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14bd8-104">คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออกในรูปแบบ XML ได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="14bd8-105">บางครั้ง เอกสารเหล่านั้นสามารถได้รับการยอมรับ เมื่อพวกเขาเป็นไปตามเกณฑ์ที่ระบุ เช่น ขนาดไฟล์สูงสุด หรือจำนวนสูงสุดของโหนด XML บางโหนด</span><span class="sxs-lookup"><span data-stu-id="14bd8-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="14bd8-106">คุณสามารถออกแบบรูปแบบ ER ที่จะสร้างเอกสารทางอิเล็กทรอนิกส์ที่ตอบสนองความต้องการที่ผู้รับของเหล่านั้นระบุ</span><span class="sxs-lookup"><span data-stu-id="14bd8-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="14bd8-107">สำหรับองค์ประกอบรูปแบบไฟล์ คุณสามารถกำหนดขีดจำกัดในขนาดไฟล์เป็นนิพจน์ ER ได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="14bd8-108">ถ้าเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการสร้างรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป</span><span class="sxs-lookup"><span data-stu-id="14bd8-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="14bd8-109">สำหรับรูปแบบองค์ประกอบไฟล์ XML ใดๆ คุณสามารถกำหนดขีดจำกัดในจำนวนขององค์ประกอบเป็นนิพจน์ ER ได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="14bd8-110">ถ้าจำนวนของโหนด XML ในไฟล์ที่สร้างเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการรันรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป</span><span class="sxs-lookup"><span data-stu-id="14bd8-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="14bd8-111">สำหรับองค์ประกอบรูปแบบลำดับ XML ใดๆ คุณสามารถกำหนดขีดจำกัดในจำนวนขององค์ประกอบรองเป็นนิพจน์ ER ได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="14bd8-112">ถ้าจำนวนของโหนด XML ที่ซ้อนกันขององค์ประกอบรูปแบบในไฟล์ที่สร้างเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการรันรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป</span><span class="sxs-lookup"><span data-stu-id="14bd8-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="14bd8-113">คุณสามารถทำเครื่องหมายรูปแบบองค์ประกอบ XML ใดๆ เป็นไม่สามารถหยุดได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="14bd8-114">ด้วยวิธีนี้ คุณสามารถทำให้รายการที่ซ้อนกันของโหนด XML ที่สร้างขึ้นภายใต้องค์ประกอบรูปแบบอยู่ในไฟล์เดียวที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="14bd8-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="14bd8-115">นอกเหนือจากการใช้องค์ประกอบ XML และองค์ประกอบรูปแบบลำดับ XML เพื่อเพิ่มโหนด XML ไปยังไฟล์ที่สร้างขึ้น คุณสามารถใช้องค์ประกอบรูปแบบ XML ดิบได้</span><span class="sxs-lookup"><span data-stu-id="14bd8-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="14bd8-116">อย่างไรก็ตาม โหนดที่คุณเพิ่มโดยใช้องค์ประกอบรูปแบบ XML ดิบ จะไม่ได้รับการพิจารณา เมื่อมีการคำนวณจำนวนของโหนดที่จะประเมินข้อจำกัดเกี่ยวกับจำนวนขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="14bd8-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="14bd8-117">ถ้าคุณตั้งค่าคอนฟิกปลายทางของไฟล์สำหรับองค์ประกอบรูปแบบไฟล์ที่มีการตั้งค่าคอนฟิก เพื่อแบ่งผลลัพธ์ที่สร้างขึ้นทุกครั้งที่เกินขีดจำกัดเฉพาะ แต่ละส่วนของผลลัพธ์ที่สร้างขึ้นถูกส่งไปที่ปลายทางไฟล์ที่ตั้งค่าคอนฟิกเป็นไฟล์แต่ละไฟล์</span><span class="sxs-lookup"><span data-stu-id="14bd8-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="14bd8-118">ในการตั้งชื่อไฟล์ที่สร้างโดยแบ่งผลลัพธ์โดยไม่ซ้ำกัน คุณต้องตั้งค่าคอนฟิกนิพจน์ ER สำหรับองค์ประกอบรูปแบบไฟล์</span><span class="sxs-lookup"><span data-stu-id="14bd8-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="14bd8-119">ถ้าคุณรวมแหล่งข้อมูล ER ของชนิดลำดับหมายเลข ระบบจะเพิ่มลำดับหมายเลขสำหรับแต่ละส่วนของผลลัพธ์ที่แบ่ง</span><span class="sxs-lookup"><span data-stu-id="14bd8-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="14bd8-120">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ เล่นคู่มืองาน **ER แบ่งไฟล์ XML ตามขนาดไฟล์หรือปริมาณรายการเนื้อหา** ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 จัดหา/พัฒนาส่วนประกอบของบริการ/โซลูชันด้านไอที (10677)** และคุณสามารถดาวน์โหลดได้จาก [ศูนย์ดาวน์โหลด Microsoft](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="14bd8-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="14bd8-121">คู่มืองานนี้จะแนะนำคุณตลอดกระบวนการตั้งค่าคอนฟิกรูปแบบ ER ที่จะแบ่งไฟล์ที่สร้างตามขีดจำกัดในขนาดไฟล์และปริมาณสินค้าเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="14bd8-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="14bd8-122">เพื่อดำเนินการคู่มืองานให้เสร็จสมบูรณ์ คุณต้องดาวน์โหลดไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14bd8-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="14bd8-123">การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="14bd8-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="14bd8-124">การตั้งค่าคอนฟิกรูปแบบ ER - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="14bd8-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="14bd8-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="14bd8-125">Additional resources</span></span>
[<span data-ttu-id="14bd8-126">ปลายทางการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="14bd8-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="14bd8-127">ผู้ออกแบบสูตรรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="14bd8-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
