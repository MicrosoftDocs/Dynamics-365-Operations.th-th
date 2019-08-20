---
title: แม็ปมิติองค์ประกอบต้นทุน
description: ผู้ควบคุมต้นทุนสามารถใช้กระบวนงานนี้ในการแม็ปมิติองค์ประกอบต้นทุนไปยังมิติองค์ประกอบต้นทุนในนิติบุคคล MXMF
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 346c64ffb19e320d0babf886c15f1b46959b4f32
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841164"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="5c5a4-103">แม็ปมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c5a4-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c5a4-104">ผู้ควบคุมต้นทุนสามารถใช้กระบวนงานนี้ในการแม็ปมิติองค์ประกอบต้นทุนไปยังมิติองค์ประกอบต้นทุนในนิติบุคคล MXMF</span><span class="sxs-lookup"><span data-stu-id="5c5a4-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="5c5a4-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="5c5a4-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="5c5a4-106">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c5a4-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="5c5a4-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5c5a4-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5c5a4-108">สำหรับตัวอย่างนี้ ให้เลือก องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c5a4-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="5c5a4-109">คลิก การแม็ปมิติ</span><span class="sxs-lookup"><span data-stu-id="5c5a4-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="5c5a4-110">คลิก ตั้งค่าคอนฟิกการแม็ปจากมิตินี้</span><span class="sxs-lookup"><span data-stu-id="5c5a4-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="5c5a4-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5c5a4-111">Click New.</span></span>
6. <span data-ttu-id="5c5a4-112">ในฟิลด์ ไปที่มิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="5c5a4-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="5c5a4-113">สำหรับตัวอย่างนี้ ให้เลือก องค์ประกอบต้นทุน MXMF</span><span class="sxs-lookup"><span data-stu-id="5c5a4-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="5c5a4-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5c5a4-114">Click New.</span></span>
8. <span data-ttu-id="5c5a4-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5c5a4-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="5c5a4-116">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5c5a4-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5c5a4-117">ตัวอย่างนี้ เลือกสมาชิกมิติ 606400 ค่าโทรศัพท์ & โทรสาร</span><span class="sxs-lookup"><span data-stu-id="5c5a4-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="5c5a4-118">ในฟิลด์สมาชิกมิติสิ้นสุด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5c5a4-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="5c5a4-119">ตัวอย่างนี้ เลือกสมาชิกมิติ 6001004 Telefono</span><span class="sxs-lookup"><span data-stu-id="5c5a4-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="5c5a4-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5c5a4-120">Click Save.</span></span>

