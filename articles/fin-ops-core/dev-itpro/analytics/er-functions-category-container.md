---
title: รายการของฟังก์ชั่น ER ในประเภทคอนเทนเนอร์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันคอนเทนเนอร์ที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561769"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="4c8c0-103">รายการของฟังก์ชั่น ER ในประเภทคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4c8c0-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c8c0-104">[การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) คอนเทนเนอร์ [ฟังก์ชัน](er-formula-language.md#functions) สามารถใช้เพื่อดำเนินการกับแหล่งข้อมูลที่เกี่ยวข้องของชนิดข้อมูล *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="4c8c0-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="4c8c0-105">การดําเนินงานเหล่านี้เกิดขึ้นเมื่อข้อมูลการประมวลผลแสดงถึงชุดข้อมูลฐานสอง ในรูปแบบฐานสองของออบเจ็กต์ขนาดใหญ่ (BLOB)</span><span class="sxs-lookup"><span data-stu-id="4c8c0-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="4c8c0-106">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4c8c0-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4c8c0-107">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4c8c0-107">List of supported functions</span></span>

| <span data-ttu-id="4c8c0-108">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4c8c0-108">Function</span></span> | <span data-ttu-id="4c8c0-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4c8c0-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4c8c0-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="4c8c0-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="4c8c0-111">ฟังก์ชันนี้จะส่งคืนค่า *คอนเทนเนอร์* ที่ประกอบด้วยเนื้อหาฐานสอ งซึ่งตัดออกจากสตริง ASCII ที่ระบุ ซึ่งแสดงถึงกลุ่ม Base64 ของแผนงานการเข้ารหัสฐานสองถึงข้อความ</span><span class="sxs-lookup"><span data-stu-id="4c8c0-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4c8c0-112">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4c8c0-112">Additional resources</span></span>

[<span data-ttu-id="4c8c0-113">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4c8c0-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4c8c0-114">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4c8c0-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4c8c0-115">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4c8c0-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]