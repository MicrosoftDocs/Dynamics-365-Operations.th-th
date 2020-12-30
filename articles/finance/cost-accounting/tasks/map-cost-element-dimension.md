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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f8d5356e6c7f8aff507d3fa87bb3c30cb38cf36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448543"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="0b2a3-103">แม็ปมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0b2a3-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b2a3-104">ผู้ควบคุมต้นทุนสามารถใช้กระบวนงานนี้ในการแม็ปมิติองค์ประกอบต้นทุนไปยังมิติองค์ประกอบต้นทุนในนิติบุคคล MXMF</span><span class="sxs-lookup"><span data-stu-id="0b2a3-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="0b2a3-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="0b2a3-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="0b2a3-106">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0b2a3-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="0b2a3-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0b2a3-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0b2a3-108">สำหรับตัวอย่างนี้ ให้เลือก องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0b2a3-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="0b2a3-109">คลิก การแม็ปมิติ</span><span class="sxs-lookup"><span data-stu-id="0b2a3-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="0b2a3-110">คลิก ตั้งค่าคอนฟิกการแม็ปจากมิตินี้</span><span class="sxs-lookup"><span data-stu-id="0b2a3-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="0b2a3-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0b2a3-111">Click New.</span></span>
6. <span data-ttu-id="0b2a3-112">ในฟิลด์ ไปที่มิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="0b2a3-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="0b2a3-113">สำหรับตัวอย่างนี้ ให้เลือก องค์ประกอบต้นทุน MXMF</span><span class="sxs-lookup"><span data-stu-id="0b2a3-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="0b2a3-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0b2a3-114">Click New.</span></span>
8. <span data-ttu-id="0b2a3-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b2a3-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0b2a3-116">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0b2a3-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b2a3-117">ตัวอย่างนี้ เลือกสมาชิกมิติ 606400 ค่าโทรศัพท์ & โทรสาร</span><span class="sxs-lookup"><span data-stu-id="0b2a3-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="0b2a3-118">ในฟิลด์สมาชิกมิติสิ้นสุด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0b2a3-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0b2a3-119">ตัวอย่างนี้ เลือกสมาชิกมิติ 6001004 Telefono</span><span class="sxs-lookup"><span data-stu-id="0b2a3-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="0b2a3-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0b2a3-120">Click Save.</span></span>

