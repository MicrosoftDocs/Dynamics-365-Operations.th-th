---
title: ฟังก์ชัน ER FORMATELEMENTNAME
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FORMATELEMENTNAME
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561313"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="efb84-103">ฟังก์ชัน ER FORMATELEMENTNAME</span><span class="sxs-lookup"><span data-stu-id="efb84-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efb84-104">`FORMATELEMENTNAME` ฟังก์ชันส่งกลับค่า *สตริง* ที่แสดงถึงชื่อขององค์ประกอบรูปแบบการรายงานอิเล็กทรอนิกส์ปัจจุบัน (ER)</span><span class="sxs-lookup"><span data-stu-id="efb84-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb84-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="efb84-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="efb84-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="efb84-106">Return values</span></span>

<span data-ttu-id="efb84-107">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="efb84-107">*String*</span></span>

<span data-ttu-id="efb84-108">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="efb84-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="efb84-109">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="efb84-109">Usage notes</span></span>

<span data-ttu-id="efb84-110">ฟังก์ชันนี้สามารถถูกเรียกในนิพจน์ ER ที่ถูกกำหนดค่าสำหรับ **ชื่อคีย์ข้อมูลที่เก็บรวบรวม** และคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวมไว้** ของส่วนประกอบรูปแบบ ER จากกลุ่ม **ข้อความ** ที่อยู่ภายใต้ส่วนประกอบ **ทั่วไป\\ไฟล์** ซึ่งมีเปิดตัวเลือก **รายละเอียดของผลลัพธ์การรวบรวม**</span><span class="sxs-lookup"><span data-stu-id="efb84-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="efb84-111">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="efb84-111">Example</span></span>

<span data-ttu-id="efb84-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**</span><span class="sxs-lookup"><span data-stu-id="efb84-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efb84-113">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="efb84-113">Additional resources</span></span>

[<span data-ttu-id="efb84-114">ฟังก์ชันการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="efb84-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]