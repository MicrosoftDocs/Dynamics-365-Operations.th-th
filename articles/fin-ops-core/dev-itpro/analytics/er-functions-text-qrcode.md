---
title: ฟังก์ชัน QRCODE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ QRCODE (ER)
author: NickSelin
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
ms.openlocfilehash: 6a76549ba5d663a7b6cfb858342a56921c5cd56b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746182"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="441cd-103">ฟังก์ชัน QRCODE ER</span><span class="sxs-lookup"><span data-stu-id="441cd-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="441cd-104">ฟังก์ชัน `QRCODE` ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี</span><span class="sxs-lookup"><span data-stu-id="441cd-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="441cd-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="441cd-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="441cd-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="441cd-106">Arguments</span></span>

<span data-ttu-id="441cd-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="441cd-107">`text`: *String*</span></span>

<span data-ttu-id="441cd-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="441cd-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="441cd-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="441cd-109">Return values</span></span>

<span data-ttu-id="441cd-110">*คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="441cd-110">*Container*</span></span>

<span data-ttu-id="441cd-111">สตรีมไบนารีที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="441cd-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="441cd-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="441cd-112">Example</span></span>

<span data-ttu-id="441cd-113">คุณสามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออกในรูปแบบ Microsoft Office (สมุดงาน Excel หรือเอกสาร Word) โดยใช้เท็มเพลตที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="441cd-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="441cd-114">เท็มเพลตนี้อาจมีออบเจ็กต์ **รูปภาพ** (สมุดงาน Excel) หรือ **ตัวควบคุมเนื้อหารูปภาพ** (เอกสาร WORD) เป็นตัวยึดสำหรับรูปภาพคิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="441cd-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="441cd-115">คุณต้องเพิ่มองค์ประกอบ **เซลล์** ไปยังรูปแบบ ER ที่ถูกตั้งค่าคอนฟิกที่จะใช้ในการเติมข้อมูลตัวยึดนี้</span><span class="sxs-lookup"><span data-stu-id="441cd-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="441cd-116">เพื่อระบุข้อมูลที่จะถูกเก็บไว้ในคิวอาร์โค้ด คุณต้องกำหนดการผูกข้อมูลสำหรับองค์ประกอบ **เซลล์** นี้</span><span class="sxs-lookup"><span data-stu-id="441cd-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="441cd-117">ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการผูกข้อมูลดังกล่าวตามที่มีนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="441cd-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="441cd-118">เมื่อคุณเรียกใช้รูปแบบ ER ที่ถูกตั้งค่าคอนฟิก ค่าข้อความของฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels** จะถูกใช้ในการสร้างรูปภาพคิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="441cd-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="441cd-119">รูปนี้จะแทนที่ตัวยึดรูปภาพคิวอาร์โค้ดในเท็มเพลตเอกสารโดยใช้เพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="441cd-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="441cd-120">เมื่อรูปภาพของเอกสารที่สร้างขึ้นนี้ถูกสแกน จะส่งกลับข้อความที่ถูกนำมาจากฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels**</span><span class="sxs-lookup"><span data-stu-id="441cd-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="441cd-121">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฝังรูปภาพและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="441cd-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="441cd-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="441cd-122">Additional resources</span></span>

[<span data-ttu-id="441cd-123">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="441cd-123">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]