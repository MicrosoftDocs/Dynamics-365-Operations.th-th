---
title: รายการของฟังก์ชั่น ER ในประเภทเฉพาะโดเมนธุรกิจ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันเฉพาะโดเมนธุรกิจที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 37f62dc03fe791857b6a6f5df6b2b3bc0083381f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561625"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a><span data-ttu-id="f15d7-103">รายการของฟังก์ชั่น ER ในประเภทเฉพาะโดเมนธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="f15d7-103">List of ER functions in the business domain–specific category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f15d7-104">ฟังก์ชันเฉพาะโดเมนของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำการคำนวณและการร้องขอการเข้าถึงข้อมูลที่เฉพาะเจาะจงสำหรับการดำเนินการของ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f15d7-104">Electronic reporting (ER) domain-specific functions can be used to perform calculations and data access requests that are specific to the implementation of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f15d7-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f15d7-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="f15d7-106">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f15d7-106">List of supported functions</span></span>

| <span data-ttu-id="f15d7-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="f15d7-107">Function</span></span>| <span data-ttu-id="f15d7-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f15d7-108">Description</span></span> |
|---------|-------------|
| [<span data-ttu-id="f15d7-109">CH_Bank_Mod_10</span><span class="sxs-lookup"><span data-stu-id="f15d7-109">CH_Bank_Mod_10</span></span>](er-functions-other-chbankmode10.md) | <span data-ttu-id="f15d7-110">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD10 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-110">This function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="f15d7-111">CN_GBT_AdditionalDimensionID</span><span class="sxs-lookup"><span data-stu-id="f15d7-111">CN_GBT_AdditionalDimensionID</span></span>](er-functions-other-cngbtadditionaldimensionid.md) | <span data-ttu-id="f15d7-112">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงรหัสมิติทางการเงินเดียวที่ถูกนำมาจากสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-112">This function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="f15d7-113">สตริงที่ระบุแสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="f15d7-113">The specified string presents all dimensions as a comma-separated list of IDs.</span></span> |
| [<span data-ttu-id="f15d7-114">ConvertCurrency</span><span class="sxs-lookup"><span data-stu-id="f15d7-114">ConvertCurrency</span></span>](er-functions-other-convertcurrency.md) | <span data-ttu-id="f15d7-115">ฟังก์ชันนี้ส่งคืนค่า *จริง* ที่แสดงผลลัพธ์ของการแปลงยอดเงินที่ระบุจากสกุลเงินต้นทางที่ระบุเป็นสกุลเงินเป้าหมายที่ระบุ โดยใช้การตั้งค่าของบริษัทที่ระบุในวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-115">This function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span> |
| [<span data-ttu-id="f15d7-116">CurCredRef</span><span class="sxs-lookup"><span data-stu-id="f15d7-116">CurCredRef</span></span>](er-functions-other-curcredref.md) | <span data-ttu-id="f15d7-117">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-117">This function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="f15d7-118">FA_Balance</span><span class="sxs-lookup"><span data-stu-id="f15d7-118">FA_Balance</span></span>](er-functions-other-fabalance.md) | <span data-ttu-id="f15d7-119">ฟังก์ชันส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดดุลสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า ปีการรายงาน และวันที่ที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="f15d7-119">This function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span> |
| [<span data-ttu-id="f15d7-120">FA_Sum</span><span class="sxs-lookup"><span data-stu-id="f15d7-120">FA_Sum</span></span>](er-functions-other-fasum.md) | <span data-ttu-id="f15d7-121">ฟังก์ชันนี้ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดเงินสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า และรอบระยะเวลาของวันที่</span><span class="sxs-lookup"><span data-stu-id="f15d7-121">This function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span> |
| [<span data-ttu-id="f15d7-122">GetCurrentCompany</span><span class="sxs-lookup"><span data-stu-id="f15d7-122">GetCurrentCompany</span></span>](er-functions-other-getcurrentcompany.md) | <span data-ttu-id="f15d7-123">ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่แสดงรหัสสำหรับนิติบุคคล (บริษัท) ที่ผู้ใช้ลงชื่อเข้าใช้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f15d7-123">This function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span> |
| [<span data-ttu-id="f15d7-124">ISOCredRef</span><span class="sxs-lookup"><span data-stu-id="f15d7-124">ISOCredRef</span></span>](er-functions-other-isocredref.md) | <span data-ttu-id="f15d7-125">ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-125">This function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span> |
| [<span data-ttu-id="f15d7-126">IsValidCharacterISO7064</span><span class="sxs-lookup"><span data-stu-id="f15d7-126">IsValidCharacterISO7064</span></span>](er-functions-other-isvalidchariso7064.md) | <span data-ttu-id="f15d7-127">ฟังก์ชันนี้ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN)</span><span class="sxs-lookup"><span data-stu-id="f15d7-127">This function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="f15d7-128">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f15d7-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="f15d7-129">Mod_97</span><span class="sxs-lookup"><span data-stu-id="f15d7-129">Mod_97</span></span>](er-functions-other-mod97.md) | <span data-ttu-id="f15d7-130">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD97 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-130">This function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="f15d7-131">NumSeqValue</span><span class="sxs-lookup"><span data-stu-id="f15d7-131">NumSeqValue</span></span>](er-functions-other-numseqvalue.md) | <span data-ttu-id="f15d7-132">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข ตามลำดับหมายเลข ขอบเขต และรหัสขอบเขตที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-132">This function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="f15d7-133">รหัสขอบเขตจะเท่ากับรหัสบริษัทที่จัดหาโดยบริบทที่เรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="f15d7-133">The scope ID equals the company code that is supplied by the context that the ER format is run under.</span></span> |
| [<span data-ttu-id="f15d7-134">RoundAmount</span><span class="sxs-lookup"><span data-stu-id="f15d7-134">RoundAmount</span></span>](er-functions-other-roundamount.md) | <span data-ttu-id="f15d7-135">ฟังก์ชันนี้ส่งกลับค่า *จริง* ที่แสดงถึงผลลัพธ์ของการปัดเศษจำนวนที่ระบุให้เป็นจำนวนตำแหน่งทศนิยมที่ระบุตามกฎการปัดเศษที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f15d7-135">This function returns a *Real* value that represents the result of rounding the specified amount to the specified number of decimal places according to the specified rounding rule.</span></span> |
| [<span data-ttu-id="f15d7-136">TableName2ID</span><span class="sxs-lookup"><span data-stu-id="f15d7-136">TableName2ID</span></span>](er-functions-other-tablename2id.md) | <span data-ttu-id="f15d7-137">ฟังก์ชันนี้ส่งกลับการแสดงตัวเลขของรหัสตารางสำหรับชื่อตารางที่ระบุเป็นค่า *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="f15d7-137">This function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="f15d7-138">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f15d7-138">Additional resources</span></span>

[<span data-ttu-id="f15d7-139">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f15d7-139">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="f15d7-140">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f15d7-140">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="f15d7-141">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f15d7-141">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]