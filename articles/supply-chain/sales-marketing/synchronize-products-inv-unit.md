---
title: ซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2019
ms.locfileid: "836313"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="0c800-103">ซิงโครไนส์ผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="0c800-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0c800-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="0c800-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="0c800-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="0c800-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="0c800-106">เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service)** ที่ใช้ ขึ้นอยู่กับเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="0c800-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="0c800-107">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)](field-service-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c800-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="0c800-108">หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="0c800-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="0c800-109">**ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales)**</span><span class="sxs-lookup"><span data-stu-id="0c800-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="0c800-110">**ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="0c800-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="0c800-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="0c800-111">Templates and tasks</span></span>

<span data-ttu-id="0c800-112">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="0c800-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0c800-113">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="0c800-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="0c800-114">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="0c800-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0c800-115">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0c800-115">Products</span></span>

<span data-ttu-id="0c800-116">เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service)** รวมการแม็ปหนึ่งที่ไม่ได้ถูกรวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="0c800-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="0c800-117">การแม็ปนี้ช่วยให้มั่นใจว่าหน่วยสินค้าคงคลังที่จำเป็นสำหรับการซิงโครไนส์ระดับสินค้าคงคลังถูกรวมอยู่</span><span class="sxs-lookup"><span data-stu-id="0c800-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0c800-118">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0c800-118">Template mapping in Data integration</span></span>

<span data-ttu-id="0c800-119">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0c800-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="0c800-120">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service): ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0c800-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="0c800-121">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="0c800-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
