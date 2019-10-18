---
title: ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ
description: หัวข้อนี้อธิบายวิธีการได้รับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร
author: saraschi2
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179a6e45d57baf810068cb5c14aed670ebb94706
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186980"
---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="48674-103">ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="48674-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48674-104">หัวข้อนี้อธิบายวิธีการตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="48674-104">This topic explains how to dispose of a fixed asset using the free text invoice.</span></span>

1. <span data-ttu-id="48674-105">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="48674-105">In the navigation pane, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="48674-106">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="48674-106">Select **New**.</span></span>
3. <span data-ttu-id="48674-107">ในฟิลด์ **บัญชีลูกค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="48674-107">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="48674-108">ตรวจสอบวันที่ใน **ใบแจ้งหนี้** เริ่มต้น และแก้ไข ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="48674-108">Validate the default **Invoice** date and edit if applicable.</span></span>
5. <span data-ttu-id="48674-109">ตรวจสอบฟิลด์ส่วนหัวค่าเริ่มต้นที่เหลือ เช่น **สกุลเงิน** และแก้ไข ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="48674-109">Validate remaining default header fields, such as **Currency** and edit if applicable.</span></span>
6. <span data-ttu-id="48674-110">ในส่วน **รายการใบแจ้งหนี้** ตรวจสอบฟิลด์ **คำอธิบาย** และ **บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="48674-110">In the **Invoice lines** section, validate the **Description** and **Main account** fields.</span></span>
7. <span data-ttu-id="48674-111">ตรวจสอบ **กลุ่มภาษีขาย** และ **กลุ่มภาษีขายตามประเภทสินค้า** เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="48674-111">Validate the default **Sales tax group** and **Item sales tax group** fields.</span></span>
8. <span data-ttu-id="48674-112">ป้อน **ราคาต่อหน่วย** หรือ **ยอด** ของการขายของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="48674-112">Enter the **Unit price** or the **Amount** of the sale of the fixed asset.</span></span>
9. <span data-ttu-id="48674-113">เลือกส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="48674-113">Select the **Line details** section.</span></span>  
10. <span data-ttu-id="48674-114">ป้อนหรือเลือกค่าในฟิลด์ **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="48674-114">Enter or select a value in the **Fixed asset** field.</span></span>
11. <span data-ttu-id="48674-115">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="48674-115">Select **Post**.</span></span> 

