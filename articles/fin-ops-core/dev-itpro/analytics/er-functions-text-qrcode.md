---
title: ฟังก์ชัน QRCODE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ QRCODE (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562672"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="c9cc2-103">ฟังก์ชัน QRCODE ER</span><span class="sxs-lookup"><span data-stu-id="c9cc2-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9cc2-104">ฟังก์ชัน `QRCODE` ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี</span><span class="sxs-lookup"><span data-stu-id="c9cc2-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cc2-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c9cc2-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="c9cc2-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c9cc2-106">Arguments</span></span>

<span data-ttu-id="c9cc2-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9cc2-107">`text`: *String*</span></span>

<span data-ttu-id="c9cc2-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="c9cc2-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9cc2-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="c9cc2-109">Return values</span></span>

<span data-ttu-id="c9cc2-110">*คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="c9cc2-110">*Container*</span></span>

<span data-ttu-id="c9cc2-111">สตรีมไบนารีที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c9cc2-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="c9cc2-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c9cc2-112">Example</span></span>

<span data-ttu-id="c9cc2-113">คุณสามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออกในรูปแบบ Microsoft Office (สมุดงาน Excel หรือเอกสาร Word) โดยใช้เท็มเพลตที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c9cc2-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="c9cc2-114">เท็มเพลตนี้อาจมีออบเจ็กต์ **รูปภาพ** (สมุดงาน Excel) หรือ **ตัวควบคุมเนื้อหารูปภาพ** (เอกสาร WORD) เป็นตัวยึดสำหรับรูปภาพคิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="c9cc2-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="c9cc2-115">คุณต้องเพิ่มองค์ประกอบ **เซลล์** ไปยังรูปแบบ ER ที่ถูกตั้งค่าคอนฟิกที่จะใช้ในการเติมข้อมูลตัวยึดนี้</span><span class="sxs-lookup"><span data-stu-id="c9cc2-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="c9cc2-116">เพื่อระบุข้อมูลที่จะถูกเก็บไว้ในคิวอาร์โค้ด คุณต้องกำหนดการผูกข้อมูลสำหรับองค์ประกอบ **เซลล์** นี้</span><span class="sxs-lookup"><span data-stu-id="c9cc2-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="c9cc2-117">ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการผูกข้อมูลดังกล่าวตามที่มีนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9cc2-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="c9cc2-118">เมื่อคุณเรียกใช้รูปแบบ ER ที่ถูกตั้งค่าคอนฟิก ค่าข้อความของฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels** จะถูกใช้ในการสร้างรูปภาพคิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="c9cc2-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="c9cc2-119">รูปนี้จะแทนที่ตัวยึดรูปภาพคิวอาร์โค้ดในเท็มเพลตเอกสารโดยใช้เพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="c9cc2-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="c9cc2-120">เมื่อรูปภาพของเอกสารที่สร้างขึ้นนี้ถูกสแกน จะส่งกลับข้อความที่ถูกนำมาจากฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="c9cc2-121">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฝังรูปภาพและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="c9cc2-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9cc2-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c9cc2-122">Additional resources</span></span>

[<span data-ttu-id="c9cc2-123">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="c9cc2-123">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]