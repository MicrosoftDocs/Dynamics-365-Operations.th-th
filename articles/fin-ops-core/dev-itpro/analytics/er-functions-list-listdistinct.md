---
title: ฟังก์ชัน LISTDISTINCT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LISTDISTINCT (ER)
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2333cfc21a16a5905acadd590982020fdf878330
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682278"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="90248-103">ฟังก์ชัน LISTDISTINCT ER</span><span class="sxs-lookup"><span data-stu-id="90248-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="90248-104">ฟังก์ชัน `LISTDISTINCT` จะคำนวณนิพจน์ที่ระบุเป็นตัวเลือกสำหรับเรกคอร์ดทั้งหมดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="90248-105">โดยจะส่งคืน *รายการเรกคอร์ด* ใหม่ที่มีเรกคอร์ดเดียวสำหรับตัวเลือกที่ไม่ซ้ำกันแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="90248-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="90248-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="90248-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="90248-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="90248-107">Arguments</span></span>

<span data-ttu-id="90248-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="90248-108">`list`: *Record list*</span></span>

<span data-ttu-id="90248-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="90248-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="90248-110">`selector`: *ชนิดข้อมูลพื้นฐาน*</span><span class="sxs-lookup"><span data-stu-id="90248-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="90248-111">นิพจน์ที่ถูกต้องที่ใช้ในการคำนวณค่าตัวเลือกสำหรับเรกคอร์ดทั้งหมดในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="90248-112">ชนิดข้อมูลต่อไปนี้ได้รับการสนับสนุนสำหรับพารามิเตอร์นี้:</span><span class="sxs-lookup"><span data-stu-id="90248-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="90248-113">บูลีน</span><span class="sxs-lookup"><span data-stu-id="90248-113">Boolean</span></span>
- <span data-ttu-id="90248-114">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="90248-114">Date</span></span>
- <span data-ttu-id="90248-115">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="90248-115">DateTime</span></span>
- <span data-ttu-id="90248-116">GUID</span><span class="sxs-lookup"><span data-stu-id="90248-116">GUID</span></span>
- <span data-ttu-id="90248-117">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="90248-117">Integer</span></span>
- <span data-ttu-id="90248-118">Int64</span><span class="sxs-lookup"><span data-stu-id="90248-118">Int64</span></span>
- <span data-ttu-id="90248-119">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="90248-119">Real</span></span>
- <span data-ttu-id="90248-120">สตริง</span><span class="sxs-lookup"><span data-stu-id="90248-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="90248-121">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="90248-121">Return values</span></span>

<span data-ttu-id="90248-122">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="90248-122">*Record list*</span></span>

<span data-ttu-id="90248-123">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="90248-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="90248-124">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="90248-124">Usage notes</span></span>

<span data-ttu-id="90248-125">โครงสร้างของรายการที่สร้างขึ้นตรงกับโครงสร้างของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="90248-126">อาจมีการคำนวณค่าตัวเลือกเดียวกันสำหรับหลายเรกคอร์ดในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="90248-127">ในกรณีนี้ ค่าฟิลด์ของเรกคอร์ดที่เกี่ยวข้องในรายการที่สร้างขึ้นจะเท่ากับค่าของเรกคอร์ดแรกจากรายการที่ระบุที่มีการคำนวณค่าตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="90248-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="90248-128">การดำเนินการของฟังก์ชันนี้เกิดขึ้นในแหล่งข้อมูล [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ของชนิด *รายการเรกคอร์ด* ที่มีอยู่ในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="90248-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="90248-129">นอกจากนี้ยังสามารถใช้แหล่งข้อมูล **GROUPBY** เพื่อสร้างรายการเรกคอร์ดที่มีการคำนวณค่าที่แตกต่างกันของตัวเลือกด้วย</span><span class="sxs-lookup"><span data-stu-id="90248-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="90248-130">อย่างไรก็ตาม จากมุมมองด้านประสิทธิภาพและการใช้หน่วยความจำ การใช้ฟังก์ชัน `LISTDISTINCT` ดีกว่าแหล่งข้อมูล **GROUPBY** เนื่องจากมีการดำเนินการของฟังก์ชันในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="90248-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="90248-131">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="90248-131">Example</span></span>

<span data-ttu-id="90248-132">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถดูรายการของหมายเลขบัญชีลูกค้าที่ไม่ซ้ำกัน ซึ่งมีการออกใบแจ้งหนี้การขายหรือใบแจ้งหนี้โครงการอย่างน้อยหนึ่งรายการในระหว่างรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="90248-133">ป้อนแหล่งข้อมูล **SalesInvoice** ของชนิด `Record list` ที่อ้างถึงตารางแอปพลิเคชัน **CustInvoiceJour** และกรองใบแจ้งหนี้การขายสำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="90248-134">ฟิลด์ `InvoiceAccount` ของแหล่งข้อมูลนี้ส่งคืนหมายเลขบัญชีของลูกค้าที่ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="90248-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="90248-135">ป้อนแหล่งข้อมูล **ProjectInvoice** ของชนิด `Record list` ที่อ้างถึงตารางแอปพลิเคชัน **ProjInvoiceJour** และกรองใบแจ้งหนี้โครงการสำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90248-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="90248-136">ฟิลด์ `InvoiceAccount` ของแหล่งข้อมูลนี้ส่งคืนหมายเลขบัญชีของลูกค้าที่ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="90248-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="90248-137">ตั้งค่าคอนฟิกแหล่งข้อมูล **AllInvoices** ของชนิด `Calculated field` ที่มีนิพจน์ `LISTJOIN(SalesInvoice, ProjectInvoice)`</span><span class="sxs-lookup"><span data-stu-id="90248-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="90248-138">แหล่งข้อมูลนี้ส่งคืนรายการที่รวมของใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="90248-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="90248-139">ตั้งค่าคอนฟิกแหล่งข้อมูล **InvoicedCustomer** ของชนิด `Record list` ที่มีนิพจน์ `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`</span><span class="sxs-lookup"><span data-stu-id="90248-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="90248-140">แหล่งข้อมูลนี้ส่งคืนรายการใหม่ที่มีเรกคอร์ดเดียวสำหรับลูกค้าแต่ละรายที่ไม่ซ้ำกันซึ่งมีการออกใบแจ้งหนี้ในระหว่างรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="90248-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="90248-141">ฟิลด์ `InvoiceAccount` ของรายการนี้มีหมายเลขบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="90248-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90248-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="90248-142">Additional resources</span></span>

[<span data-ttu-id="90248-143">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="90248-143">List functions</span></span>](er-functions-category-list.md)
