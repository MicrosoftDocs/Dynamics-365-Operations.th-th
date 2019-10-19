---
title: สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล
description: หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181944"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="80507-103">สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80507-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80507-104">หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="80507-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="80507-105">ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ</span><span class="sxs-lookup"><span data-stu-id="80507-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="80507-106">กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="80507-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="80507-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="80507-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="80507-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="80507-108">Select **New**.</span></span>
3. <span data-ttu-id="80507-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="80507-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="80507-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80507-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="80507-111">ตัวอย่างเช่น ป้อน **แล็ปท็อปลูกค้าเป้าหมายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="80507-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="80507-112">ในฟิลด์ **ชื่อสำหรับค้นหา** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80507-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="80507-113">ตัวอย่างเช่น ป้อน **แล็ปท็อป**</span><span class="sxs-lookup"><span data-stu-id="80507-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="80507-114">ขยายส่วน **ข้อมูลทางเทคนิค**</span><span class="sxs-lookup"><span data-stu-id="80507-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="80507-115">ในฟิลด์ **สร้าง** **แบบจำลอง** และ **ปีแบบจำลอง** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="80507-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="80507-116">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="80507-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="80507-117">เลือก **ข้อมูลเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="80507-117">Select **Record info**.</span></span>
10. <span data-ttu-id="80507-118">เลือก **เท็มเพลตผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="80507-118">Select **User template**.</span></span>
11. <span data-ttu-id="80507-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80507-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="80507-120">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80507-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="80507-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="80507-121">Select **OK**.</span></span>
14. <span data-ttu-id="80507-122">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="80507-122">Select **Close**.</span></span>

