---
title: ผู้ผลิตและแบบจำลองของสินทรัพย์
description: หัวข้อนี้อธิบายวิธีการตั้งค่าผู้ผลิตสินทรัพย์และแบบจำลองที่เกี่ยวข้องในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14a73f49064911a2b28c742cfc19469f4bf95e74
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569972"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="82744-103">ผู้ผลิตและแบบจำลองของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="82744-104">หัวข้อนี้อธิบายวิธีการตั้งค่าผู้ผลิตสินทรัพย์และแบบจำลองที่เกี่ยวข้องในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="82744-105">แบบจำลองสามารถเกี่ยวข้องกับชนิดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="82744-106">ตั้งค่าความสัมพันธ์ของแบบจำลอง-ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="82744-106">Set up product-model relations</span></span>

1. <span data-ttu-id="82744-107">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **ผู้ผลิตและแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="82744-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="82744-108">เลือก **สร้าง** เพื่อสร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="82744-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="82744-109">ในฟิลด์ **ผู้ผลิต** ให้ป้อนชื่อสำหรับผู้ผลิตสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="82744-110">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="82744-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="82744-111">บน FastTab **แบบจำลอง** ให้เลือก **เพิ่ม** เพื่อสร้างแบบจำลองสินทรัพย์ที่ควรเกี่ยวข้องกับผู้ผลิตสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="82744-112">ในฟิลด์ **แบบจำลอง** ให้ป้อนชื่อสำหรับแบบจำลองสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="82744-113">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="82744-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="82744-114">ในฟิลด์ **ชนิดสินทรัพย์** ให้เลือกชนิดสินทรัพย์ที่แบบจำลองผู้ผลิตควรเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="82744-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="82744-115">นอกจากนี้ คุณยังสามารถตั้งค่าความสัมพันธ์สำหรับชนิดของสินทรัพย์ ผู้ผลิต และแบบจำลองได้ในการค้นหา **ชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="82744-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="82744-116">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างชนิดสินทรัพย์](../setup-for-objects/object-types.md)</span><span class="sxs-lookup"><span data-stu-id="82744-116">For more information, see [Create asset type](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="82744-117">ใน FastTab **รายละเอียด** ฟิลด์ **แบบจำลอง** จะแสดงจำนวนของแบบจำลองสินทรัพย์ที่ตั้งค่าไว้ในผู้ผลิตสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82744-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="82744-118">ฟิลด์ **สินทรัพย์** แสดงจำนวนของสินทรัพย์ที่ใช้ผู้ผลิตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82744-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="82744-119">ฟิลด์ **สินทรัพย์** แสดงจำนวนของออบเจ็กต์ที่ใช้แบบจำลองผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="82744-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="82744-120">ชนิดของสินทรัพย์อาจไม่มีความสัมพันธ์ของแบบจำลองผู้ผลิตสินทรัพย์ อาจเกี่ยวข้องกับแบบจำลองผู้ผลิตสินทรัพย์หนึ่งรายการ หรืออาจเกี่ยวข้องกับแบบจำลองผู้ผลิตสินทรัพย์หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="82744-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="82744-121">ถ้าชนิดของสินทรัพย์เกี่ยวข้องกับแบบจำลองผู้ผลิตอย่างน้อยหนึ่งรายการ เฉพาะชุดที่ตั้งค่าไว้ในการค้นหา **แบบจำลองผู้ผลิต** เท่านั้นที่สามารถถูกเลือกได้บนหน้าการจัดการสินทรัพย์เหล่านั้น ที่ซึ่งสามารถตั้งค่าชุดของชนิดสินทรัพย์ ผู้ผลิต และแบบจำลองได้</span><span class="sxs-lookup"><span data-stu-id="82744-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="82744-122">หน้าเหล่านี้รวมถึง **สินทรัพย์ทั้งหมด** **ระดับบริการสินทรัพย์** **ค่าเริ่มต้นชนิดงาน** และ **รายการงบประมาณการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="82744-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="82744-123">ถ้าชนิดสินทรัพย์บางชนิดไม่เกี่ยวข้องกับแบบจำลองผู้ผลิตใดๆ เฉพาะชนิดของสินทรัพย์เหล่านั้น และแบบจำลองผู้ผลิตที่ยังไม่มีความสัมพันธ์กับชนิดสินทรัพย์ จะแสดงอยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="82744-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="82744-124">เลือกผู้ผลิตและแบบจำลองบนออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="82744-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="82744-125">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="82744-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="82744-126">ในคอลัมน์ **สินทรัพย์** ให้เลือกลิงค์สำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="82744-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="82744-127">หน้า **รายละเอียด** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="82744-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="82744-128">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="82744-128">Select **Edit**.</span></span>
4. <span data-ttu-id="82744-129">บน FastTab **ทั่วไป** ให้เลือกค่าในฟิลด์ **ผู้ผลิต** และฟิลด์ **แบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="82744-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
