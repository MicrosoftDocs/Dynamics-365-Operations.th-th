---
title: การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ffa0616d51127a024bea526c5926a182c0449971
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996750"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="69eb4-103">การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="69eb4-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69eb4-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365  Field Service</span><span class="sxs-lookup"><span data-stu-id="69eb4-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="69eb4-105">เท็มเพลตที่ใช้กับ **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** มีพื้นฐานบนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง** เท็มเพลตของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสด</span><span class="sxs-lookup"><span data-stu-id="69eb4-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="69eb4-106">สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)</span><span class="sxs-lookup"><span data-stu-id="69eb4-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="69eb4-107">หัวข้อนี้อธิบายเพียวความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="69eb4-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="69eb4-108">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="69eb4-108">Templates and tasks</span></span>

<span data-ttu-id="69eb4-109">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="69eb4-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="69eb4-110">ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="69eb4-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="69eb4-111">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="69eb4-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="69eb4-112">ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69eb4-112">Products - Products</span></span>

<span data-ttu-id="69eb4-113">เท็มเพลต **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** รวมแม็ปที่ไม่ได้ใช้บนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**</span><span class="sxs-lookup"><span data-stu-id="69eb4-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="69eb4-114">การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="69eb4-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="69eb4-115">มีการใช้การแม็ปค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="69eb4-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="69eb4-116">ใน Supply Chain Management ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่สามารถนำออกมาขายได้** สามารถคำนวณได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="69eb4-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="69eb4-117">**สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง</span><span class="sxs-lookup"><span data-stu-id="69eb4-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="69eb4-118">**NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ</span><span class="sxs-lookup"><span data-stu-id="69eb4-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="69eb4-119">**บริการ:** ชนิดผลิตภัณฑ์ = บริการ</span><span class="sxs-lookup"><span data-stu-id="69eb4-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="69eb4-120">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69eb4-120">Template mapping in Data integration</span></span>

<span data-ttu-id="69eb4-121">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69eb4-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="69eb4-122">ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service): ผลิตภัณฑ์ - ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69eb4-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="69eb4-123">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="69eb4-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
