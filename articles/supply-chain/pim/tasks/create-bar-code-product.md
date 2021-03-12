---
title: สร้างบาร์โค้ดให้ผลิตภัณฑ์
description: หัวข้อนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 ดังตัวอย่าง
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e660ff80db4c73d99efb781e5c55a244769dc6e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986965"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="fc4d2-103">สร้างบาร์โค้ดให้ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fc4d2-103">Create a bar code for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc4d2-104">หัวข้อนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 ดังตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fc4d2-104">This topic shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="fc4d2-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="fc4d2-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="fc4d2-106">เลือก **การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้** บนหน้าแรก</span><span class="sxs-lookup"><span data-stu-id="fc4d2-106">Select **Released product maintenance** on the homepage.</span></span>
2. <span data-ttu-id="fc4d2-107">ไปที่ **ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้** ภายใต้ส่วน **การเชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-107">Go to **Products > Released products** under the **Links** section.</span></span>
3. <span data-ttu-id="fc4d2-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fc4d2-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="fc4d2-109">สำหรับตัวอย่างนี้ ให้เลือก หมายเลขสินค้า **M0001**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-109">For this example, select item number **M0001**.</span></span>
4. <span data-ttu-id="fc4d2-110">ในบานหน้าต่างการดำเนินการ เลือก **จัดการสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-110">On the Action Pane, select **Manage inventory**.</span></span>
5. <span data-ttu-id="fc4d2-111">เลือก **บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-111">Select **Bar codes**.</span></span>
6. <span data-ttu-id="fc4d2-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-112">Select **New**.</span></span>
7. <span data-ttu-id="fc4d2-113">ทำเครื่องหมายแถวที่เลือกที่สร้างไว้ในรายการด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="fc4d2-113">Mark the selected row that is created in the list below.</span></span>
8. <span data-ttu-id="fc4d2-114">ในฟิลด์ **การตั้งค่าบาร์โค้ด** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fc4d2-114">In the **Barcode setup** field, enter or select a value.</span></span>
9. <span data-ttu-id="fc4d2-115">ในฟิลด์ **บาร์โค้ด** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc4d2-115">In the **Bar code** field, enter or select a value.</span></span>
10. <span data-ttu-id="fc4d2-116">ในฟิลด์ **บาร์โค้ด** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fc4d2-116">In the **Bar code** field, type a value.</span></span>  
11. <span data-ttu-id="fc4d2-117">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="fc4d2-117">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="fc4d2-118">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fc4d2-118">Select **Save**.</span></span>
13. <span data-ttu-id="fc4d2-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc4d2-119">Close the page.</span></span> 

