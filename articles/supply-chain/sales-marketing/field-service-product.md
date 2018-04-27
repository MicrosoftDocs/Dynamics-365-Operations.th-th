---
title: "ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: th-th
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="a9dc3-103">ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="a9dc3-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a9dc3-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="a9dc3-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a9dc3-105">เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="a9dc3-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="a9dc3-106">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)</span><span class="sxs-lookup"><span data-stu-id="a9dc3-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="a9dc3-107">หัวข้อนี้อธิบายความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="a9dc3-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a9dc3-108">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="a9dc3-108">Templates and tasks</span></span>

<span data-ttu-id="a9dc3-109">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="a9dc3-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a9dc3-110">ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="a9dc3-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="a9dc3-111">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="a9dc3-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a9dc3-112">ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a9dc3-112">Products - Products</span></span>

<span data-ttu-id="a9dc3-113">เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ประกอบด้วย การแม็ปหนึ่งรายการที่ไม่รวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="a9dc3-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="a9dc3-114">การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a9dc3-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="a9dc3-115">มีการใช้การแม็ปค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9dc3-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="a9dc3-116">ใน Finance and Operations ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ซึ่งสามารถขายได้** จะถูกคำนวณดังนี้:</span><span class="sxs-lookup"><span data-stu-id="a9dc3-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="a9dc3-117">**สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง</span><span class="sxs-lookup"><span data-stu-id="a9dc3-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="a9dc3-118">**NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ</span><span class="sxs-lookup"><span data-stu-id="a9dc3-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="a9dc3-119">**บริการ:** ชนิดผลิตภัณฑ์ = บริการ</span><span class="sxs-lookup"><span data-stu-id="a9dc3-119">**Service:** Product type = Service</span></span>

