---
title: สร้างผลิตภัณฑ์ใหม่
description: 'งานนี้แสดงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "328550"
---
# <a name="create-a-new-product"></a><span data-ttu-id="daab5-103">สร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="daab5-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="daab5-104">งานนี้แสดงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่ </span><span class="sxs-lookup"><span data-stu-id="daab5-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="daab5-105">ซึ่งมักจะถูกดำเนินการโดยผู้ออกแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="daab5-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="daab5-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="daab5-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="daab5-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="daab5-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="daab5-108">สร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="daab5-108">Create a product</span></span>
1. <span data-ttu-id="daab5-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="daab5-109">Click New.</span></span>
2. <span data-ttu-id="daab5-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="daab5-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="daab5-111">ถ้าลำดับหมายเลขไม่ได้ถูกตั้งค่าสำหรับหมายเลขผลิตภัณฑ์ ต้องมีการป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="daab5-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="daab5-112">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="daab5-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="daab5-113">ชื่อผลิตภัณฑ์เป็นค่าเริ่มต้นที่ใช้เป็นชื่อค้นหา </span><span class="sxs-lookup"><span data-stu-id="daab5-113">The product name defaults to the search name.</span></span> <span data-ttu-id="daab5-114">คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="daab5-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="daab5-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="daab5-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="daab5-116">ตั้งค่ากลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="daab5-116">Set up dimension groups</span></span>
1. <span data-ttu-id="daab5-117">คลิกกลุ่มมิติเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="daab5-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="daab5-118">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="daab5-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="daab5-119">กลุ่มมิติการจัดเก็บจะกำหนดว่า มิติการจัดเก็บใดที่คุณต้องป้อนในแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการติดตามในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="daab5-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="daab5-120">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="daab5-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="daab5-121">กลุ่มมิติการติดตามจะกำหนดว่า มิติการติดตามใดที่คุณต้องป้อนสำหรับแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการจัดการในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="daab5-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="daab5-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="daab5-122">Click OK.</span></span>

