---
title: ฟังก์ชัน Base64StringToContainer ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) Base64StringToContainer
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754385"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="a5d68-103">ฟังก์ชัน Base64StringToContainer ER</span><span class="sxs-lookup"><span data-stu-id="a5d68-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5d68-104">`BASE64STRINGTOCONTAINER` [ฟังก์ชัน](er-formula-language.md#functions) แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *[คอนเทนเนอร์](er-functions-category-container.md)*</span><span class="sxs-lookup"><span data-stu-id="a5d68-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d68-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a5d68-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="a5d68-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a5d68-106">Arguments</span></span>

<span data-ttu-id="a5d68-107">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a5d68-107">`input`: *String*</span></span>

<span data-ttu-id="a5d68-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a5d68-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5d68-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a5d68-109">Return values</span></span>

<span data-ttu-id="a5d68-110">*ตู้บรรจุสินค้า*</span><span class="sxs-lookup"><span data-stu-id="a5d68-110">*Container*</span></span>

<span data-ttu-id="a5d68-111">ค่าฐานสองที่ได้ในรูปแบบฐานสองของออบเจ็กต์ขนาดใหญ่ (BLOB)</span><span class="sxs-lookup"><span data-stu-id="a5d68-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a5d68-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a5d68-112">Usage notes</span></span>

<span data-ttu-id="a5d68-113">มีข้อยกเว้น "พารามิเตอร์ไม่ถูกต้อง" ถ้าสตริงอินพุทไม่มีกลุ่ม Base64 ที่ถูกต้องของแผนงานการเข้ารหัสฐานสองต่อข้อความ</span><span class="sxs-lookup"><span data-stu-id="a5d68-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="a5d68-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a5d68-114">Example</span></span>

<span data-ttu-id="a5d68-115">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="a5d68-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="a5d68-116">แหล่งข้อมูล **DocuTypeGroupEnum** ราก ของชนิด *Dynamics 365 for Operations / การแจงนับ* ที่อ้างอิงถึงการแจงนับของแอพลิเคชัน **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="a5d68-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="a5d68-117">แหล่งข้อมูล **ลูกค้า** ราก ของชนิด *Dynamics 365 for Operations / เรกคอร์ดของตาราง* ที่อ้างอิงถึงตารางของแอพลิเคชัน **CustTable**</span><span class="sxs-lookup"><span data-stu-id="a5d68-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="a5d68-118">แหล่งข้อมูล **\#สื่อ** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5d68-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a5d68-119">เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="a5d68-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="a5d68-120">ซึ่งมีนิจน์ของ `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`</span><span class="sxs-lookup"><span data-stu-id="a5d68-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="a5d68-121">แหล่งข้อมูล **\#MediaAsBase64String** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5d68-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a5d68-122">เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **Customer.'\#Media'**</span><span class="sxs-lookup"><span data-stu-id="a5d68-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="a5d68-123">ซึ่งมีนิจน์ของ `Customer.'#Media'.'getFileContentAsBase64String()'`</span><span class="sxs-lookup"><span data-stu-id="a5d68-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="a5d68-124">แหล่งข้อมูล **\#BlobFomBase64** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5d68-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a5d68-125">เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **Customer.'\#Media'**</span><span class="sxs-lookup"><span data-stu-id="a5d68-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="a5d68-126">ซึ่งมีนิจน์ของ `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`</span><span class="sxs-lookup"><span data-stu-id="a5d68-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="a5d68-127">ในตัวอย่างนี้ แหล่งข้อมูล **\#MediaAsBase64String** จะเข้ารหัสเนื้อหาฐานสองของส่วนแนบของสื่อปัจจุบัน เป็นข้อความที่แสดงถึงกลุ่ม Base64 ของแผนงานการเข้ารหัสฐานสองถึงข้อความ</span><span class="sxs-lookup"><span data-stu-id="a5d68-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="a5d68-128">แหล่งข้อมูล **\#BlobFomBase64** จะถอดรหัสสตริง Base64 และส่งคืนค่าฐานสองในรูปแบบ BLOB</span><span class="sxs-lookup"><span data-stu-id="a5d68-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![แหล่งข้อมูลตัวอย่างในหน้าตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="a5d68-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a5d68-130">Additional resources</span></span>

[<span data-ttu-id="a5d68-131">ฟังก์ชันคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="a5d68-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]