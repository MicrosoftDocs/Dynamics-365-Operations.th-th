---
title: สร้างผลิตภัณฑ์ใหม่
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bf15359e085b541407bb49c266f7d9505893e25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203721"
---
# <a name="create-a-new-product"></a><span data-ttu-id="c21fc-103">สร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="c21fc-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c21fc-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่</span><span class="sxs-lookup"><span data-stu-id="c21fc-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="c21fc-105">ซึ่งมักจะถูกดำเนินการโดยผู้ออกแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="c21fc-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="c21fc-106">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c21fc-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="c21fc-107">สร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c21fc-107">Create a product</span></span>
1. <span data-ttu-id="c21fc-108">ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c21fc-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="c21fc-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c21fc-109">Select **New**.</span></span>
3. <span data-ttu-id="c21fc-110">ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c21fc-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="c21fc-111">ถ้าลำดับหมายเลขไม่ได้ถูกตั้งค่าสำหรับหมายเลขผลิตภัณฑ์ ต้องมีการป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c21fc-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="c21fc-112">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c21fc-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="c21fc-113">ชื่อผลิตภัณฑ์เป็นค่าเริ่มต้นที่ใช้เป็นชื่อค้นหา </span><span class="sxs-lookup"><span data-stu-id="c21fc-113">The product name defaults to the search name.</span></span> <span data-ttu-id="c21fc-114">คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="c21fc-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="c21fc-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c21fc-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="c21fc-116">ตั้งค่ากลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="c21fc-116">Set up dimension groups</span></span>
1. <span data-ttu-id="c21fc-117">เลือก **กลุ่มมิติ** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c21fc-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="c21fc-118">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c21fc-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="c21fc-119">กลุ่มมิติการจัดเก็บจะกำหนดว่า มิติการจัดเก็บใดที่คุณต้องป้อนในแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการติดตามในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c21fc-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="c21fc-120">ในฟิลด์ **กลุ่มมิติการติดตาม** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c21fc-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="c21fc-121">กลุ่มมิติการติดตามจะกำหนดว่า มิติการติดตามใดที่คุณต้องป้อนสำหรับแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการจัดการในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c21fc-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="c21fc-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c21fc-122">Select **OK**.</span></span>

