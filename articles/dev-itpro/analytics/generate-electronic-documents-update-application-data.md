---
title: "สร้างเอกสารทางอิเล็กทรอนิกส์และอัพเดตข้อมูลใบสมัครโดยใช้เครื่องมือการรายงานทางอิเล็กทรอนิกส์"
description: "คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่สามารถใช้ในแอพลิเคชัน Finance and Operations เพื่อสร้างเอกสารอิเล็กทรอนิกส์ขาออก นอกจากนี้คุณยังสามารถออกแบบรูปแบบ ER ที่แยกวิเคราะห์เอกสารอิเล็กทรอนิกส์ขาเข้า และใช้เนื้อหาในเอกสารเหล่านั้นเพื่ออัพเดตข้อมูลแอพลิเคชัน"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: e2447274016f517db3ec0eb8f55c6b3163822f50
ms.contentlocale: th-th
ms.lasthandoff: 02/27/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="58af7-104">สร้างเอกสารทางอิเล็กทรอนิกส์และอัพเดตข้อมูลใบสมัครโดยใช้เครื่องมือการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="58af7-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58af7-105">คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่สามารถใช้ในแอพลิเคชัน Finance and Operations เพื่อสร้างเอกสารอิเล็กทรอนิกส์ขาออก</span><span class="sxs-lookup"><span data-stu-id="58af7-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="58af7-106">นอกจากนี้คุณยังสามารถออกแบบรูปแบบ ER ที่แยกวิเคราะห์เอกสารอิเล็กทรอนิกส์ขาเข้า และใช้เนื้อหาในเอกสารเหล่านั้นเพื่ออัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="58af7-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="58af7-107">ในฟังก์ชันนี้ คุณสามารถใช้รูปแบบ ER เดียวในการสร้างเอกสารอิเล็กทรอนิกส์ขาออก และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="58af7-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="58af7-108">ลักษณะการทำงานนี้ยังสามารถนำไปใช้ในสถานการณ์จำลองต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="58af7-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="58af7-109">เพื่อป้องกันการใช้ซ้ำของข้อมูลแอพลิเคชันในกระบวนการในเวลาต่อมา คุณสามารถเลือกข้อมูลแอพลิเคชันทันทีหลังจากที่ใช้ในการสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="58af7-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="58af7-110">ตัวอย่างเช่น คุณสามารถทำเครื่องหมายธุรกรรมการชำระเงินที่ดำเนินการอยู่แล้วในทันทีหลังจากที่มีการรวมข้อความการชำระเงินที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="58af7-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="58af7-111">เพื่อจัดเก็บรายละเอียดการประมวลผลเอกสารอิเล็กทรอนิกส์ที่สร้างขึ้นโดยใช้ตรรกะ ER</span><span class="sxs-lookup"><span data-stu-id="58af7-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="58af7-112">ตัวอย่างเช่น รหัสประจำตัวของข้อความการชำระเงินที่ไม่ซ้ำกันที่สร้างขึ้นโดยใช้นิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="58af7-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="58af7-113">นิพจน์จะยึดตามข้อมูลที่ป้อนไว้ในกล่องโต้ตอบ ER เมื่อรันรูปแบบ ER เพื่อสร้างเอกสาร</span><span class="sxs-lookup"><span data-stu-id="58af7-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="58af7-114">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้เปิดชุดเอกสารการสร้าง ER ที่มีคู่มืองานการอัพเดตข้อมูลแอพลิเคชัน (ส่วนหนึ่งของ 7.5.4.3 รับ/พัฒนาบริการ IT/ส่วนประกอบของโซลูชัน IT (10677 )กระบวนการทางธุรกิจ) ที่แนะนำเกี่ยวกับรายละเอียดของการรายงานและการเก็บอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="58af7-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="58af7-115">ไฟล์ต่อไปนี้จำเป็นต้องใช้เพื่อทำตามขั้นตอนบางอย่างในคู่มืองานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="58af7-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="58af7-116">ดาวน์โหลดและบันทึกแฟ้มเหล่านี้ลงในเครื่องคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="58af7-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="58af7-117">การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER: อินทราสแทต (แบบจำลอง)</span><span class="sxs-lookup"><span data-stu-id="58af7-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="58af7-118">การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER: อินทราสแทต (การแม็ป)</span><span class="sxs-lookup"><span data-stu-id="58af7-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="58af7-119">การตั้งค่าคอนฟิกรูปแบบ ER: อินทราสแทต (รูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="58af7-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

