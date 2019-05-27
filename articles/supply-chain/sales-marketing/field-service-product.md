---
title: ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562706"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="f36f4-103">ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations กับผลิตภัณฑ์ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="f36f4-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f36f4-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f36f4-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f36f4-105">เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="f36f4-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="f36f4-106">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)</span><span class="sxs-lookup"><span data-stu-id="f36f4-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="f36f4-107">หัวข้อนี้อธิบายความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="f36f4-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f36f4-108">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="f36f4-108">Templates and tasks</span></span>

<span data-ttu-id="f36f4-109">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="f36f4-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f36f4-110">ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="f36f4-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="f36f4-111">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="f36f4-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f36f4-112">ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f36f4-112">Products - Products</span></span>

<span data-ttu-id="f36f4-113">เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ประกอบด้วย การแม็ปหนึ่งรายการที่ไม่รวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="f36f4-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="f36f4-114">การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f36f4-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="f36f4-115">มีการใช้การแม็ปค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f36f4-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="f36f4-116">ใน Finance and Operations ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ซึ่งสามารถขายได้** จะถูกคำนวณดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f36f4-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="f36f4-117">**สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง</span><span class="sxs-lookup"><span data-stu-id="f36f4-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="f36f4-118">**NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ</span><span class="sxs-lookup"><span data-stu-id="f36f4-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="f36f4-119">**บริการ:** ชนิดผลิตภัณฑ์ = บริการ</span><span class="sxs-lookup"><span data-stu-id="f36f4-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f36f4-120">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f36f4-120">Template mapping in Data integration</span></span>

<span data-ttu-id="f36f4-121">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f36f4-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="f36f4-122">ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service): ผลิตภัณฑ์ - ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="f36f4-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="f36f4-123">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="f36f4-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
