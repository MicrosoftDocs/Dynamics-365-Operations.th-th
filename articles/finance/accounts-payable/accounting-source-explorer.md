---
title: โปรแกรมตรวจดูบัญชีต้นทาง
description: บทความนี้แสดงข้อมูลเกี่ยวกับโปรแกรมตรวจดูบัญชีต้นทาง ซึ่งคุณสามารถใช้สำหรับการวิเคราะห์แหล่งข้อมูลเบื้องหลังรายการบัญชีแยกประเภททั่วไปโดยละเอียด
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 904f1f9fb139248205b426aec5a0372f2edb1e59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180232"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="9e677-103">โปรแกรมตรวจดูบัญชีต้นทาง</span><span class="sxs-lookup"><span data-stu-id="9e677-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e677-104">บทความนี้แสดงข้อมูลเกี่ยวกับโปรแกรมตรวจดูบัญชีต้นทาง ซึ่งคุณสามารถใช้สำหรับการวิเคราะห์แหล่งข้อมูลเบื้องหลังรายการบัญชีแยกประเภททั่วไปโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="9e677-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="9e677-105">โปรแกรมตรวจดูต้นทางบัญชีคือ หน้าใหม่ที่แสดงข้อมูลแหล่งที่มา</span><span class="sxs-lookup"><span data-stu-id="9e677-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="9e677-106">คุณสามารถใช้โปรแกรมตรวจดูบัญชีต้นทางเป็นเครื่องมือแบบสแตนด์อโลน หรือเพื่อวิเคราะห์รายละเอียดหลังรายการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9e677-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="9e677-107">ตัวอย่างเช่น คุณสามารถใช้โปรแกรมตรวจดูต้นทางบัญชีในการเรียกข้อมูลแหล่งที่มาของรายละเอียดมากที่สุด สำหรับยอดดุลในงบทดลอง หรือสำหรับธุรกรรมใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="9e677-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="9e677-108">จากนั้น คุณสามารถใช้คุณลักษณะ Export to MS Excel เพื่อแยกและย่อยข้อมูลเพิ่มเติมใน Microsoft Excel (ตัวอย่างเช่น ใน PivotTable หรือในรายงาน PivotTable)</span><span class="sxs-lookup"><span data-stu-id="9e677-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="9e677-109">โปรแกรมตรวจดูต้นทางบัญชีแสดงเช่นเดียวกันกับยอดเงินรวมต่อบัญชีแยกประเภทเสมอขณะรายการบัญชีแยกประเภททั่วไปแสดงอยู่ (ตัวอย่างเช่น ในงบทดลอง)</span><span class="sxs-lookup"><span data-stu-id="9e677-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="9e677-110">ดังเช่นในงบทดลอง คุณสามารถแสดงเซ็กเมนต์ในคอลัมน์ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="9e677-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="9e677-111">เพียงแค่เลือกเซ็ตมิติทางการเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9e677-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="9e677-112">คุณสามารถใช้พารามิเตอร์เพื่อกำหนดช่วงวันที่สำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="9e677-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="9e677-113">ฟังก์ชันนี้คล้ายกับฟังก์ชันในงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="9e677-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="9e677-114">สำหรับเอกสารทั้งหมดที่ใช้ในกรอบงานเอกสารต้นทาง โปรแกรมตรวจดูบัญชีต้นทางแสดงข้อมูลเพิ่มเติม ตามการกระจายการลงบัญชี และ ถ้ามี โครงการกระจายการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="9e677-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="9e677-115">ข้อมูลนี้รวมถึงชนิดยอดเงิน โครงการ กิจกรรม ประเภท และลักษณะของรายการ</span><span class="sxs-lookup"><span data-stu-id="9e677-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="9e677-116">ต่อไปนี้เป็นตัวอย่างของการวิเคราะห์บางประการที่คุณสามารถทำได้:</span><span class="sxs-lookup"><span data-stu-id="9e677-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="9e677-117">ผลต่างระหว่างใบสั่งซื้อและใบแจ้งหนี้ของผู้จัดจำหน่าย เนื่องจากผลต่างของแต่ละรายการถูกแสดง ด้วยชนิดยอดเงิน เช่นผลต่างค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9e677-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="9e677-118">เรียกเก็บเงินได้และชั่วโมงที่ไม่ได้เรียกเก็บเงินและค่าใช้จ่ายสำหรับโครงการแต่ละโครงการ หน่วยธุรกิจ และบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="9e677-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="9e677-119">สำหรับเอกสารต้นทางที่ใช้แนวคิดข้อมูลเฉพาะตัวอ้างอิงของเอกสารต้นทาง โปรแกรมตรวจดูบัญชีต้นทาง จะแสดงรายละเอียดเพิ่มเติม เช่นลูกค้า ผู้จัดจำหน่าย ผู้ปฏิบัติงาน ผลิตภัณฑ์ ปริมาณ ข้อความหน่วย และคำอธิบายต่างๆ</span><span class="sxs-lookup"><span data-stu-id="9e677-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="9e677-120">ต่อไปนี้เป็นตัวอย่างของการวิเคราะห์บางประการที่คุณสามารถทำได้:</span><span class="sxs-lookup"><span data-stu-id="9e677-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="9e677-121">ค่าใช้จ่ายโรงแรมต่อหน่วยธุรกิจและแบรนด์ของโรงแรมสำหรับรอบระยะเวลาทางบัญชี ขึ้นกับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9e677-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="9e677-122">ส่วนลดสำหรับแต่ละผู้จัดจำหน่าย สินค้า แผนก</span><span class="sxs-lookup"><span data-stu-id="9e677-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="9e677-123">สำหรับเอกสารเหล่านี้ คุณสามารถหาเส้นทางไปยังเอกสารต้นทางที่แท้จริงจากโปรแกรมตรวจดูต้นทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="9e677-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



