---
title: ซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "359255"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="992a6-103">ซิงโครไนส์ผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="992a6-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="992a6-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="992a6-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="992a6-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="992a6-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="992a6-106">เท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="992a6-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="992a6-107">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง](products-template-mapping-direct.md)</span><span class="sxs-lookup"><span data-stu-id="992a6-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="992a6-108">หัวข้อนี้อธิบายเฉพาะความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** และ **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="992a6-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="992a6-109">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="992a6-109">Templates and tasks</span></span>

<span data-ttu-id="992a6-110">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="992a6-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="992a6-111">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="992a6-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="992a6-112">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="992a6-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="992a6-113">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="992a6-113">Products</span></span>

<span data-ttu-id="992a6-114">เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service)** รวมการแม็ปหนึ่งที่ไม่ได้ถูกรวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**</span><span class="sxs-lookup"><span data-stu-id="992a6-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="992a6-115">การแม็ปนี้ช่วยให้มั่นใจว่าหน่วยสินค้าคงคลังที่จำเป็นสำหรับการซิงโครไนส์ระดับสินค้าคงคลังถูกรวมอยู่</span><span class="sxs-lookup"><span data-stu-id="992a6-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="992a6-116">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="992a6-116">Template mapping in Data integration</span></span>

<span data-ttu-id="992a6-117">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="992a6-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="992a6-118">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service): ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="992a6-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="992a6-119">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="992a6-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
