---
title: ฟังก์ชัน GETENUMVALUEBYNAME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETENUMVALUEBYNAME (ER)
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685943"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="899e3-103">ฟังก์ชัน GETENUMVALUEBYNAME ER</span><span class="sxs-lookup"><span data-stu-id="899e3-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="899e3-104">ฟังก์ชัน `GETENUMVALUEBYNAME` ค้นหาค่า *Enum* เฉพาะในแหล่งข้อมูลการแจงนับที่ระบุ โดยใช้ชื่อการแจงนับที่ระบุเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="899e3-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="899e3-105">ถ้าพบค่า *Enum* ฟังก์ชันจะส่งคืน</span><span class="sxs-lookup"><span data-stu-id="899e3-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="899e3-106">มิฉะนั้น ฟังก์ชันจะส่งกลับค่าการแจงนับ **null**</span><span class="sxs-lookup"><span data-stu-id="899e3-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="899e3-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="899e3-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="899e3-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="899e3-108">Arguments</span></span>

<span data-ttu-id="899e3-109">`enumeration data source path`: *การแจงนับ*</span><span class="sxs-lookup"><span data-stu-id="899e3-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="899e3-110">พาธที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดการแจงนับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="899e3-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="899e3-111">การแจงนับแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="899e3-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="899e3-112">การแจงนับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="899e3-112">ER format enumeration</span></span>
- <span data-ttu-id="899e3-113">การแจงนับ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="899e3-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="899e3-114">`enumeration value text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="899e3-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="899e3-115">ค่าสตริงที่แสดงชื่อของค่าการแจงนับเดียว</span><span class="sxs-lookup"><span data-stu-id="899e3-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="899e3-116">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="899e3-116">Return values</span></span>

<span data-ttu-id="899e3-117">*Enum* ที่สามารถเว้นว่างได้</span><span class="sxs-lookup"><span data-stu-id="899e3-117">Nullable *Enum*</span></span>

<span data-ttu-id="899e3-118">ค่าการแจงนับที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="899e3-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="899e3-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="899e3-119">Usage notes</span></span>

<span data-ttu-id="899e3-120">ไม่มีข้อยกเว้น หากไม่พบค่า *Enum* โดยใช้ชื่อของค่าการแจงนับที่ระบุเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="899e3-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="899e3-121">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="899e3-121">Example 1</span></span>

<span data-ttu-id="899e3-122">ในแผนภาพต่อไปนี้ การแจงนับ **ReportDirection** ถูกนำมาใช้ในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="899e3-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="899e3-123">โปรดทราบว่า ป้ายชื่อถูกกำหนดไว้สำหรับค่าแจงนับ</span><span class="sxs-lookup"><span data-stu-id="899e3-123">Notice that labels are defined for the enumeration values.</span></span>

![ค่าที่พร้อมใช้งานสำหรับการแจงนับรูปแบบข้อมูล](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="899e3-125">ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="899e3-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="899e3-126">แหล่งข้อมูล **$ทิศทาง** ถูกตั้งค่าคอนฟิกในรายงาน ER</span><span class="sxs-lookup"><span data-stu-id="899e3-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="899e3-127">แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแบบจำลอง **ReportDirection**</span><span class="sxs-lookup"><span data-stu-id="899e3-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="899e3-128">นิพจน์ `$IsArrivals` ถูกออกแบบมาเพื่อใช้การแจงนับแบบจำลอง–ที่ขึ้นกับ **$ทิศทาง** เป็นพารามิเตอร์ของฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="899e3-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="899e3-129">ค่าของนิพจน์การเปรียบเทียบนี้คือ **จริง**</span><span class="sxs-lookup"><span data-stu-id="899e3-129">The value of this comparison expression is **TRUE**.</span></span>

![ตัวอย่างของการแจงนับรูปแบบข้อมูล](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="899e3-131">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="899e3-131">Example 2</span></span>

<span data-ttu-id="899e3-132">ฟังก์ชัน `GETENUMVALUEBYNAME` และ [`LISTOFFIELDS`](er-functions-list-listoffields.md) ช่วยให้คุณสามารถนำค่าและป้ายชื่อของการแจงนับที่ได้รับการสนับสนุนเป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="899e3-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="899e3-133">(การแจงนับได้รับการสนับสนุนเป็นการแจงนับแอปพลิเคชัน การแจงนับรูปแบบข้อมูล และรูปแบบการแจงนับ)</span><span class="sxs-lookup"><span data-stu-id="899e3-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="899e3-134">ในแผนภาพต่อไปนี้ แหล่งข้อมูล **TransType** ถูกนำมาใช้ในการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="899e3-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="899e3-135">แหล่งข้อมูลนี้อ้างอิงถึงการแจงนับแอพลิเคชัน **LedgerTransType**</span><span class="sxs-lookup"><span data-stu-id="899e3-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![แหล่งข้อมูลของการแม็ปแบบจำลองที่อ้างอิงถึงการแจงนับของแอพลิเคชัน](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="899e3-137">ในแผนภาพต่อไปนี้แสเงแหล่งข้อมูล **TransTypeList** ที่ถูกตั้งค่าคอนฟิกในการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="899e3-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="899e3-138">แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแอพลิเคชัน **TransType**</span><span class="sxs-lookup"><span data-stu-id="899e3-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="899e3-139">ฟังก์ชัน `LISTOFFIELDS` ใช้เพื่อส่งคืนค่าการแจงนับทั้งหมดเป็นรายการเรกคอร์ดที่มีฟิลด์</span><span class="sxs-lookup"><span data-stu-id="899e3-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="899e3-140">ในลักษณะนี้ จะมีการเปิดเผยรายละเอียดของค่าการแจงนับทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="899e3-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="899e3-141">ฟิลด์ **EnumValue** ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล **TransTypeList** โดยใช้นิพจน์ `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`</span><span class="sxs-lookup"><span data-stu-id="899e3-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="899e3-142">ฟิลด์นี้ส่งคืนค่าการแจงนับสำหรับเร็กคอร์ดทั้งหมดในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="899e3-142">This field returns an enumeration value for every record in this list.</span></span>

![แหล่งข้อมูลของการแม็ปแบบจำลองที่ส่งคืนค่าการแจงนับทั้งหมดของการแจงนับที่เลือกเป็นรายการของเรกคอร์ด](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="899e3-144">ในแผนภาพต่อไปนี้แสเงแหล่งข้อมูล **VendTrans** ที่ถูกตั้งค่าคอนฟิกในการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="899e3-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="899e3-145">แหล่งข้อมูลนี้ส่งคืนเรกคอร์ดธุรกรรมผู้จัดจำหน่ายจากตารางแอพลิเคชัน **VendTrans**</span><span class="sxs-lookup"><span data-stu-id="899e3-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="899e3-146">ชนิดบัญชีแยกประเภทของธุรกรรมทั้งหมดจะถูกกำหนดโดยค่าของฟิลด์ **TransType**</span><span class="sxs-lookup"><span data-stu-id="899e3-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="899e3-147">ฟิลด์ **TransTypeTitle** ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล **VendTrans** โดยใช้นิพจน์ `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`</span><span class="sxs-lookup"><span data-stu-id="899e3-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="899e3-148">ฟิลด์นี้จะส่งคืนป้ายชื่อของค่าการแจงนับของธุรกรรมปัจจุบันเป็นข้อความ ถ้าค่าการแจงนับนี้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="899e3-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="899e3-149">มิฉะนั้น จะส่งกลับค่าสตริงที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="899e3-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="899e3-150">ฟิลด์ **TransTypeTitle** ถูกผูกไว้กับฟิลด์ **LedgerType** ของรูปแบบข้อมูลซึ่งช่วยให้สามารถใช้ข้อมูลนี้ในทุกรูปแบบ ER ซึ่งใช้รูปแบบข้อมูลเป็นแหล่งที่มาของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="899e3-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![แหล่งข้อมูลของการแม็ปแบบจำลองที่ส่งคืนธุรกรรมผู้จัดจำหน่าย](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="899e3-152">ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถใช้ [ดีบักเกอร์แหล่งข้อมูล](er-debug-data-sources.md) เพื่อทดสอบการแม็ปแบบจำลองที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="899e3-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![การใช้ดีบักเกอร์แหล่งข้อมูลเพื่อทดสอบการแม็ปแบบจำลองที่ตั้งค่าคอนฟิก](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="899e3-154">ฟิลด์ **LedgerType** ของป้ายชื่อที่แสดงรูปแบบข้อมูลของชนิดธุรกรรมตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="899e3-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="899e3-155">ถ้าคุณวางแผนที่จะใช้วิธีการนี้สำหรับข้อมูลของธุรกรรมจำนวนมาก คุณต้องพิจารณาประสิทธิภาพของการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="899e3-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="899e3-156">สำหรับข้อมูลเพิ่มเติม ให้ดู [ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="899e3-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="899e3-157">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="899e3-157">Additional resources</span></span>

[<span data-ttu-id="899e3-158">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="899e3-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="899e3-159">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="899e3-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="899e3-160">ฟังก์ชัน LISTOFFIELDS ER</span><span class="sxs-lookup"><span data-stu-id="899e3-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="899e3-161">ฟังก์ชัน FIRSTORNULL ER</span><span class="sxs-lookup"><span data-stu-id="899e3-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="899e3-162">ฟังก์ชั่น WHERE ER</span><span class="sxs-lookup"><span data-stu-id="899e3-162">WHERE ER function</span></span>](er-functions-list-where.md)
