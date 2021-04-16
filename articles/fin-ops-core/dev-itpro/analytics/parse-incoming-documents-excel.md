---
title: แยกวิเคราะห์เอกสารขาเข้าในรูปแบบ Excel
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์เนื้อหาที่มีในไฟล์ Microsoft Excel ขาเข้า
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755191"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="1bd00-103">แยกวิเคราะห์เอกสารที่กำลังจะมาถึงในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="1bd00-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1bd00-104">คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์ไฟล์ Microsoft Excel ขาเข้าที่แสดงข้อมูลในสมุดงาน Microsoft Excel (ไฟล์ในรูปแบบ XLSX)</span><span class="sxs-lookup"><span data-stu-id="1bd00-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="1bd00-105">จากนั้นคุณสามารถใช้เนื้อหาจากไฟล์เหล่านี้เพื่ออัพเดตข้อมูลแอพลิเคชันได้</span><span class="sxs-lookup"><span data-stu-id="1bd00-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="1bd00-106">สิ่งนี้มีประโยชน์ ถ้าคุณ:</span><span class="sxs-lookup"><span data-stu-id="1bd00-106">This is useful if you:</span></span>

- <span data-ttu-id="1bd00-107">ออกแบบแบบจำลองและรูปแบบใหม่ และต้องการทดสอบในขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="1bd00-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="1bd00-108">ในกรณีนี้ Excel จะจำลองข้อมูลแอพลิเคชันจริง</span><span class="sxs-lookup"><span data-stu-id="1bd00-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="1bd00-109">จัดการข้อมูลนอกเหนือจากแอพลิเคชันของคุณใน Excel และต้องการนำเข้าข้อมูลนี้เพื่อส่งรายงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1bd00-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="1bd00-110">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ เล่นคู่มืองาน **ER นำเข้าข้อมูลจากไฟล์ Microsoft Excel (ส่วนที่ 1: ออกแบบรูปแบบ)** และ **ER นำเข้าข้อมูลจากไฟล์ Microsoft Excel (ส่วนที่ 2: นำเข้าข้อมูล)** (ส่วนของ 7.5.4.3 รับ/พัฒนาองค์ประกอบบริการ/โซลูชันด้าน IT (10677) กระบวนการทางธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="1bd00-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="1bd00-111">คู่มืองานเหล่านี้จะแนะนำวิธีในการแยกวิเคราะห์ไฟล์ Excel ขาเข้า โดยใช้รูปแบบ ER เพื่อนำเข้าข้อมูลจากเอกสารขาเข้าและอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1bd00-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="1bd00-112">คุณสามารถดาวน์โหลดไฟล์คู่มืองานได้จาก [ศูนย์ดาวน์โหลด Microsoft](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="1bd00-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="1bd00-113">ดาวน์โหลดไฟล์ต่อไปนี้เพื่อดำเนินการคู่มืองานที่กล่าวถึงด้านบนให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1bd00-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="1bd00-114">คำอธิบายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1bd00-114">Content description</span></span>                         | <span data-ttu-id="1bd00-115">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="1bd00-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="1bd00-116">ไฟล์ขาเข้าในรูปแบบ XLSX - เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1bd00-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="1bd00-117">1099import template.xlsx</span><span class="sxs-lookup"><span data-stu-id="1bd00-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="1bd00-118">ไฟล์ขาเข้าในรูปแบบ XLSX - ข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1bd00-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="1bd00-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="1bd00-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="1bd00-120">ถ้าคุณยังไม่ได้เล่นคู่มืองานต่อไปนี้ [ER สร้างการตั้งค่าคอนฟิกที่จำเป็นเพื่อนำเข้าข้อมูลจากไฟล์ภายนอก](./tasks/er-required-configurations-import-data.md) ในโปรแกรมประยุกต์ Finance and Operations ปัจจุบัน ดาวน์โหลดไฟล์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1bd00-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="1bd00-121">คำอธิบายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1bd00-121">Content description</span></span>    | <span data-ttu-id="1bd00-122">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="1bd00-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1bd00-123">การตั้งค่าคอนฟิกแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="1bd00-123">ER model configuration</span></span> | [<span data-ttu-id="1bd00-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="1bd00-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]