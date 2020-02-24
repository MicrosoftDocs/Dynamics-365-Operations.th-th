---
title: การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน
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
ms.openlocfilehash: c87e4cbfa375ef99d00c9a145c190af78e912d56
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029416"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="e9cd7-103">การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="e9cd7-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9cd7-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365  Field Service</span><span class="sxs-lookup"><span data-stu-id="e9cd7-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="e9cd7-105">เท็มเพลตที่ใช้กับ **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** มีพื้นฐานบนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง** เท็มเพลตของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสด</span><span class="sxs-lookup"><span data-stu-id="e9cd7-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="e9cd7-106">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)</span><span class="sxs-lookup"><span data-stu-id="e9cd7-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="e9cd7-107">หัวข้อนี้อธิบายเพียวความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="e9cd7-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e9cd7-108">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="e9cd7-108">Templates and tasks</span></span>

<span data-ttu-id="e9cd7-109">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="e9cd7-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="e9cd7-110">ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="e9cd7-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="e9cd7-111">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="e9cd7-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="e9cd7-112">ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e9cd7-112">Products - Products</span></span>

<span data-ttu-id="e9cd7-113">เท็มเพลต **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** รวมแม็ปที่ไม่ได้ใช้บนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="e9cd7-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="e9cd7-114">การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e9cd7-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="e9cd7-115">มีการใช้การแม็ปค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e9cd7-115">The following value mapping is used.</span></span>

```Text
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="e9cd7-116">ใน Supply Chain Management ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่สามารถนำออกมาขายได้** สามารถคำนวณได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="e9cd7-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="e9cd7-117">**สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง</span><span class="sxs-lookup"><span data-stu-id="e9cd7-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="e9cd7-118">**NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ</span><span class="sxs-lookup"><span data-stu-id="e9cd7-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="e9cd7-119">**บริการ:** ชนิดผลิตภัณฑ์ = บริการ</span><span class="sxs-lookup"><span data-stu-id="e9cd7-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e9cd7-120">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e9cd7-120">Template mapping in Data integration</span></span>

<span data-ttu-id="e9cd7-121">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e9cd7-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="e9cd7-122">ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service): ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e9cd7-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="e9cd7-123">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="e9cd7-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
