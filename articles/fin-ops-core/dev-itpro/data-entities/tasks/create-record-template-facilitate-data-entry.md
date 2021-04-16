---
title: สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล
description: หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ
author: margoc
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6a2eec8d730cb4c63c854433cf6160c475ce660
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753975"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="9ddda-103">สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ddda-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ddda-104">หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="9ddda-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="9ddda-105">ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ</span><span class="sxs-lookup"><span data-stu-id="9ddda-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="9ddda-106">กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="9ddda-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="9ddda-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9ddda-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="9ddda-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9ddda-108">Select **New**.</span></span>
3. <span data-ttu-id="9ddda-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9ddda-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="9ddda-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9ddda-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="9ddda-111">ตัวอย่างเช่น ป้อน **แล็ปท็อปลูกค้าเป้าหมายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="9ddda-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="9ddda-112">ในฟิลด์ **ชื่อสำหรับค้นหา** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9ddda-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="9ddda-113">ตัวอย่างเช่น ป้อน **แล็ปท็อป**</span><span class="sxs-lookup"><span data-stu-id="9ddda-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="9ddda-114">ขยายส่วน **ข้อมูลทางเทคนิค**</span><span class="sxs-lookup"><span data-stu-id="9ddda-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="9ddda-115">ในฟิลด์ **สร้าง** **แบบจำลอง** และ **ปีแบบจำลอง** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9ddda-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="9ddda-116">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="9ddda-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="9ddda-117">เลือก **ข้อมูลเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="9ddda-117">Select **Record info**.</span></span>
10. <span data-ttu-id="9ddda-118">เลือก **เท็มเพลตผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9ddda-118">Select **User template**.</span></span>
11. <span data-ttu-id="9ddda-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9ddda-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="9ddda-120">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9ddda-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="9ddda-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9ddda-121">Select **OK**.</span></span>
14. <span data-ttu-id="9ddda-122">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="9ddda-122">Select **Close**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]