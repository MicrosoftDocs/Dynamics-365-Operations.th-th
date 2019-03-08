---
title: สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก
description: กระบวนงานนี้แสดงวิธีการสร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ ที่แยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 156972cdbf4ffb02b01b00972cc83d003d941378
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "326365"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="4036c-103">สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="4036c-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4036c-104">กระบวนงานนี้แสดงวิธีการสร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ ที่แยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM</span><span class="sxs-lookup"><span data-stu-id="4036c-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="4036c-105">สร้างสถานะที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="4036c-105">Create an obsolete state</span></span>
1. <span data-ttu-id="4036c-106">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > สถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4036c-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="4036c-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4036c-107">Click New.</span></span>
3. <span data-ttu-id="4036c-108">ในฟิลด์สถานะ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4036c-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="4036c-109">เลือก ไม่ ในฟิลด์ ใช้งานอยู่สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4036c-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="4036c-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4036c-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="4036c-111">เชื่อมโยงสถานะที่ล้าสมัยกับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="4036c-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="4036c-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4036c-112">Close the page.</span></span>
2. <span data-ttu-id="4036c-113">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="4036c-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="4036c-114">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="4036c-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4036c-115">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ ค้นหาชื่อ ด้วยค่า 'M00'</span><span class="sxs-lookup"><span data-stu-id="4036c-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="4036c-116">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="4036c-116">Click Edit.</span></span>
5. <span data-ttu-id="4036c-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4036c-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4036c-118">ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="4036c-118">In the Product lifecycle state field, enter or select a value.</span></span>

