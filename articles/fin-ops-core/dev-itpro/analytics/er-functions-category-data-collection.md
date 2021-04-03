---
title: รายการของฟังก์ชั่น ER ในประเภทการรวบรวมข้อมูล
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการรวบรวมข้อมูลที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561745"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="894e8-103">รายการของฟังก์ชั่น ER ในประเภทการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="894e8-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="894e8-104">ฟังก์ชันการรวบรวมข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) จะถูกใช้เพื่อทำการนับและการสรุปในรูปแบบ ER ที่กำลังรัน ขึ้นอยู่กับข้อมูลของผลลัพธ์ที่สร้างไว้ในรูปแบบ **ข้อความ** หรือ **Xml**</span><span class="sxs-lookup"><span data-stu-id="894e8-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="894e8-105">วิธีการนี้จะใช้เพื่อช่วยปรับปรุงประสิทธิภาพของรูปแบบ ER ที่รันเพื่อป้อนค่าของการรันผลรวมในเอกสารที่สร้างขึ้นและเพื่อวัตถุประสงค์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="894e8-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="894e8-106">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="894e8-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="894e8-107">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="894e8-107">List of supported functions</span></span>

| <span data-ttu-id="894e8-108">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="894e8-108">Function</span></span> | <span data-ttu-id="894e8-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="894e8-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="894e8-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="894e8-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="894e8-111">ฟังก์ชันนี้ส่งคืนค่า *รายการเรกคอร์ด* ที่ประกอบด้วยรายการของค่าที่ถูกส่งกลับโดยคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ขององค์ประกอบรูปแบบและเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="894e8-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="894e8-112">แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="894e8-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="894e8-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="894e8-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="894e8-114">ฟังก์ชันนี้ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="894e8-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="894e8-115">เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="894e8-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="894e8-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="894e8-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="894e8-117">ฟังก์ชันนี้ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="894e8-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="894e8-118">แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="894e8-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="894e8-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="894e8-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="894e8-120">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงชื่อขององค์ประกอบรูปแบบ ER ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="894e8-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="894e8-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="894e8-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="894e8-122">ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="894e8-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="894e8-123">เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="894e8-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="894e8-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="894e8-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="894e8-125">ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="894e8-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="894e8-126">แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="894e8-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="894e8-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="894e8-127">Additional resources</span></span>

[<span data-ttu-id="894e8-128">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="894e8-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="894e8-129">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="894e8-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="894e8-130">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="894e8-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]