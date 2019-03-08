---
title: ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ
description: กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c58cef0609c8f931eace13ee0dec89f3eee7fed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "310748"
---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="ff910-103">ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="ff910-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff910-104">กระบวนงานนี้แสดงวิธีการตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="ff910-104">This procedure shows how to dispose of a fixed asset using the free text invoice.</span></span>

1. <span data-ttu-id="ff910-105">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ff910-105">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="ff910-106">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff910-106">Click New.</span></span>
3. <span data-ttu-id="ff910-107">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ff910-107">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="ff910-108">ตรวจสอบวันที่ในใบแจ้งหนี้เริ่มต้น และแก้ไข ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ff910-108">Validate the default Invoice date and edit if applicable.</span></span>
5. <span data-ttu-id="ff910-109">ตรวจสอบฟิลด์ส่วนหัวค่าเริ่มต้นที่เหลือ เช่น สกุลเงิน และแก้ไข ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ff910-109">Validate remaining default header fields, such as Currency and edit if applicable.</span></span>
6. <span data-ttu-id="ff910-110">ป้อนคำอธิบายลงในรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ff910-110">Enter a Description into the invoice line.</span></span>
7. <span data-ttu-id="ff910-111">ป้อนหรือเลือกบัญชีหลักสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ff910-111">Enter or select the Main account for the invoice line.</span></span>
8. <span data-ttu-id="ff910-112">ตรวจสอบกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ff910-112">Validate the default Sales tax group and Item sales tax group.</span></span>
9. <span data-ttu-id="ff910-113">ป้อนราคาต่อหน่วย หรือยอดของการขายของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="ff910-113">Enter the Unit price or hte Amount of the sale of the fixed asset.</span></span>
10. <span data-ttu-id="ff910-114">คลิกรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="ff910-114">Click Line details.</span></span>  
11. <span data-ttu-id="ff910-115">เลือกหมายเลขสินทรัพย์ถาวรที่จะขาย</span><span class="sxs-lookup"><span data-stu-id="ff910-115">Select the Fixed asset number to be sold.</span></span>
12. <span data-ttu-id="ff910-116">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="ff910-116">Click Post.</span></span>

