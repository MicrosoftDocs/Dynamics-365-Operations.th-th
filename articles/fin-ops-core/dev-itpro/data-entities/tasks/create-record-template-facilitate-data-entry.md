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
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68d3c7dd2f042617a7e2fcc8bee05fae6a82bde9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685229"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="a546a-103">สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a546a-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a546a-104">หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="a546a-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="a546a-105">ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a546a-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="a546a-106">กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="a546a-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="a546a-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="a546a-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="a546a-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a546a-108">Select **New**.</span></span>
3. <span data-ttu-id="a546a-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="a546a-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="a546a-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a546a-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="a546a-111">ตัวอย่างเช่น ป้อน **แล็ปท็อปลูกค้าเป้าหมายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="a546a-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="a546a-112">ในฟิลด์ **ชื่อสำหรับค้นหา** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a546a-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="a546a-113">ตัวอย่างเช่น ป้อน **แล็ปท็อป**</span><span class="sxs-lookup"><span data-stu-id="a546a-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="a546a-114">ขยายส่วน **ข้อมูลทางเทคนิค**</span><span class="sxs-lookup"><span data-stu-id="a546a-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="a546a-115">ในฟิลด์ **สร้าง** **แบบจำลอง** และ **ปีแบบจำลอง** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a546a-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="a546a-116">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="a546a-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="a546a-117">เลือก **ข้อมูลเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a546a-117">Select **Record info**.</span></span>
10. <span data-ttu-id="a546a-118">เลือก **เท็มเพลตผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="a546a-118">Select **User template**.</span></span>
11. <span data-ttu-id="a546a-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a546a-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="a546a-120">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a546a-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="a546a-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a546a-121">Select **OK**.</span></span>
14. <span data-ttu-id="a546a-122">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="a546a-122">Select **Close**.</span></span>

