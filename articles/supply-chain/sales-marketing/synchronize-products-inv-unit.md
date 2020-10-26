---
title: ซิงโครไนส์ผลิตภัณฑ์ที่มากับหน่วยสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958704"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="58220-103">ซิงโครไนส์ผลิตภัณฑ์ที่มากับหน่วยสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="58220-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58220-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="58220-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="58220-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="58220-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="58220-106">เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Field Service)** ที่ใช้ ขึ้นอยู่กับเท็มเพลต **ผลิตภัณฑ์ Field Service (Supply Chain Management ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="58220-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="58220-107">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์ผลิตภัณฑ์ใน Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service](field-service-product.md)</span><span class="sxs-lookup"><span data-stu-id="58220-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="58220-108">หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="58220-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="58220-109">**ผลิตภัณฑ์ Field Service ที่มากับหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Sales)**</span><span class="sxs-lookup"><span data-stu-id="58220-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="58220-110">**ผลิตภัณฑ์ Field Service (Supply Chain Management ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="58220-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="58220-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="58220-111">Templates and tasks</span></span>

<span data-ttu-id="58220-112">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="58220-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="58220-113">ผลิตภัณฑ์ Field Service ที่มากับหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="58220-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="58220-114">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="58220-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="58220-115">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58220-115">Products</span></span>

<span data-ttu-id="58220-116">เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Field Service)** รวมถึงการแม็ปหนึ่งรายการที่ไม่ได้ถูกรวมใน **ผลิตภัณฑ์ Field Service (Supply Chain Management ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="58220-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="58220-117">การแม็ปนี้ช่วยให้มั่นใจว่าหน่วยสินค้าคงคลังที่จำเป็นสำหรับการซิงโครไนส์ระดับสินค้าคงคลังถูกรวมอยู่</span><span class="sxs-lookup"><span data-stu-id="58220-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="58220-118">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="58220-118">Template mapping in Data integration</span></span>

<span data-ttu-id="58220-119">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="58220-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="58220-120">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Field Service): ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58220-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="58220-121">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="58220-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
