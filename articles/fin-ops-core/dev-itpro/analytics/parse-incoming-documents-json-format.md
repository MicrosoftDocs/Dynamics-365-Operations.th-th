---
title: แยกวิเคราะห์เอกสารที่กำลังจะมาถึงในรูปแบบ JSON
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่ารูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์เอกสารขาเข้าในรูปแบบของ JavaScript Object Notation (JSON)
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 8be4e225507a18a92d642ff0f3a6ca3d0ff68564
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772546"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="59fd6-103">แยกวิเคราะห์เอกสารที่กำลังจะมาถึงในรูปแบบ JSON</span><span class="sxs-lookup"><span data-stu-id="59fd6-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="59fd6-104">คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์เอกสารอิเล็กทรอนิกส์ขาเข้า ซึ่งแสดงข้อมูลในรูปแบบข้อความที่เป็นไปตาม JavaScript (กล่าวได้อีกอย่างหนึ่งว่า ไฟล์ที่อยู่ในรูปแบบ JavaScript Object Notation \[JSON\])</span><span class="sxs-lookup"><span data-stu-id="59fd6-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="59fd6-105">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะ ให้ดาวน์โหลดไฟล์ในตารางต่อไปนี้ แล้วเล่น ER สร้างการตั้งค่าคอนฟิกรูปแบบเพื่อนำเข้าข้อมูลจากคู่มืองานไฟล์ JSON ภายนอก</span><span class="sxs-lookup"><span data-stu-id="59fd6-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="59fd6-106">คู่มืองานนี้แสดงวิธีการที่สามารถใช้รูปแบบ ER เพื่อแยกวิเคราะห์ไฟล์ JSON ขาเข้าเพื่อปรับปรุงข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="59fd6-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="59fd6-107">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="59fd6-107">Title</span></span>                                  | <span data-ttu-id="59fd6-108">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="59fd6-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="59fd6-109">การตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="59fd6-109">ER format configuration</span></span>                | [<span data-ttu-id="59fd6-110">รูปแบบสำหรับการนำเข้า trans_JSON.xml ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="59fd6-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="59fd6-111">ตัวอย่างของไฟล์ขาเข้าในรูปแบบ .csv</span><span class="sxs-lookup"><span data-stu-id="59fd6-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="59fd6-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="59fd6-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="59fd6-113">ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="59fd6-113">Requirements</span></span>

<span data-ttu-id="59fd6-114">ก่อนที่คุณจะดำเนินการ ER สร้างการตั้งค่าคอนฟิกรูปแบบ เพื่อนำเข้าข้อมูลจากคู่มืองานไฟล์ JSON ภายนอก ต้องเป็นไปตามข้อกำหนดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="59fd6-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="59fd6-115">องค์ประกอบหลักในไฟล์ JSON อาจเป็นองค์ประกอบออบเจ็กต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59fd6-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="59fd6-116">องค์ประกอบที่ซ้อนกันสำหรับออบเจ็กต์ควรเป็นองค์ประกอบของคุณสมบัติ ดังนั้นจึงมีการสร้างโครงสร้าง JSON ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="59fd6-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="59fd6-117">อาร์เรย์ JSON สามารถเป็นได้เฉพาะองค์ประกอบที่ซ้อนกันขององค์ประกอบคุณสมบัติของออบเจ็กต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59fd6-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="59fd6-118">อาร์เรย์ JSON สามารถประกอบด้วยออบเจ็กต์ JSON เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59fd6-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="59fd6-119">ไม่สามารถมีค่าสตริงตัวอักษรและตัวเลขโดยตรงและอาร์เรย์ที่ซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="59fd6-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="59fd6-120">องค์ประกอบในอาร์เรย์เหล่านี้จะได้รับการแยกวิเคราะห์ตามลำดับ เมื่อมีการระบุอยู่ในรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="59fd6-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="59fd6-121">การตั้งค่าความหลากหลายของออบเจ็กต์แต่ละ JSON รายการจะถูกพิจารณา</span><span class="sxs-lookup"><span data-stu-id="59fd6-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="59fd6-122">นอกจากนี้ คุณต้องดำเนินการคู่มืองาน [ER สร้างการตั้งค่าคอนฟิกที่จำเป็นเพื่อนำเข้าข้อมูลจากไฟล์ภายนอก](tasks/er-required-configurations-import-data.md) ให้เสร็จสมบูรณ์ ถ้าคุณยังไม่ได้ดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="59fd6-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="59fd6-123">ดาวน์โหลดไฟล์ต่อไปนี้เพื่อดำเนินการคู่มืองานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="59fd6-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="59fd6-124">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="59fd6-124">Title</span></span>                  | <span data-ttu-id="59fd6-125">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="59fd6-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="59fd6-126">การตั้งค่าคอนฟิกแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="59fd6-126">ER model configuration</span></span> | [<span data-ttu-id="59fd6-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="59fd6-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
