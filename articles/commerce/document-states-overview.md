---
title: สถานะและระยะเวลาใช้งานของเอกสาร
description: หัวข้อนี้จะครอบคลุมถึงสถานะเอกสารต่างๆขององค์ประกอบหน้าใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002992"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="a6a9e-103">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a6a9e-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a6a9e-104">หัวข้อนี้จะครอบคลุมถึงสถานะเอกสารต่างๆขององค์ประกอบหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a6a9e-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="a6a9e-105">คำอธิบายสถานะเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a6a9e-105">Document state descriptions</span></span>

<span data-ttu-id="a6a9e-106">หัวข้อ [องค์ประกอบของหน้า](page-elements-overview.md) จะแสดงรายการชนิดเอกสารต่างๆในระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="a6a9e-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="a6a9e-107">ชนิดเอกสารเหล่านี้อาจมีหลายสถานะในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="a6a9e-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="a6a9e-108">สถานะเอกสารช่วยป้องกันความขัดแย้งของข้อมูล และบังคับใช้การควบคุมเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="a6a9e-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="a6a9e-109">ซึ่งจะกำหนดว่าใครบ้างที่สามารถเปลี่ยนแปลงเอกสารได้ เมื่อใดที่สามารถเปลี่ยนเอกสารได้ และเมื่อใดที่สามารถดูการเปลี่ยนแปลงของบุคคลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="a6a9e-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="a6a9e-110">ตารางต่อไปนี้แสดงสถานะเอกสารที่เป็นไปได้ขององค์ประกอบใน Commerce</span><span class="sxs-lookup"><span data-stu-id="a6a9e-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="a6a9e-111">สถานะเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a6a9e-111">Document state</span></span> | <span data-ttu-id="a6a9e-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a6a9e-112">Description</span></span> |
|---|---|
| <span data-ttu-id="a6a9e-113">เช็คเอาท์แล้ว</span><span class="sxs-lookup"><span data-stu-id="a6a9e-113">Checked out</span></span> | <span data-ttu-id="a6a9e-114">เมื่อมีการเช็คเอาท์ CMS ใด ๆ ให้กับคุณ จะไม่สามารถแก้ไขได้โดยผู้ใช้ระบบที่มีการพิสูจน์ตัวจริงอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a6a9e-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="a6a9e-115">ทุกความเปลี่ยนแปลงที่คุณสร้างบนรายการ จะมองเห็นได้เฉพาะคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a6a9e-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="a6a9e-116">เช็คอินแล้ว</span><span class="sxs-lookup"><span data-stu-id="a6a9e-116">Checked in</span></span> | <span data-ttu-id="a6a9e-117">เมื่อมีการเช็คอิน CMS การเปลี่ยนแปลงทั้งหมดจะสามารถมองเห็นได้สำหรับผู้ใช้ที่มีการพิสูจน์ตัวจริงอื่น ๆ และผู้ใช้เหล่านั้นสามารถตรวจสอบและแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a6a9e-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="a6a9e-118">การเช็คอินแต่ละครั้งจะสร้างเรกคอร์ดเวอร์ชันเอกสารในประวัติของรายการ</span><span class="sxs-lookup"><span data-stu-id="a6a9e-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="a6a9e-119">เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="a6a9e-119">Published</span></span> | <span data-ttu-id="a6a9e-120">เมื่อมีการเผยแพร่รายการ CMS จะมีการผลักดันให้กับไซต์จริงของคุณ และจะสามารถมองเห็นได้บนอินเทอร์เน็ตโดยผู้ใช้ภายนอกที่ไม่ได้ยืนยันตัวตน</span><span class="sxs-lookup"><span data-stu-id="a6a9e-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="a6a9e-121">สามารถเผยแพร่รายการได้เฉพาะเมื่อเช็คอินแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a6a9e-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="a6a9e-122">บันทึกแล้ว</span><span class="sxs-lookup"><span data-stu-id="a6a9e-122">Saved</span></span> | <span data-ttu-id="a6a9e-123">คุณสามารถบันทึกการเปลี่ยนแปลงที่เกิดขึ้นกับรายการที่มีการเช็คเอาท์ CMS ไปยัง CMS ก่อนที่จะเช็คอินหรือเผยแพร่รายการ</span><span class="sxs-lookup"><span data-stu-id="a6a9e-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="a6a9e-124">ผู้ใช้ที่ได้รับการยืนยันตัวตนที่บันทึกไว้ จะไม่สามารถมองเห็นได้จนกว่าจะมีการเช็คอินรายการ</span><span class="sxs-lookup"><span data-stu-id="a6a9e-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="a6a9e-125">ผู้ใช้ภายนอกไม่สามารถมองเห็นได้จนกว่าจะมีการเผยแพร่รายการ</span><span class="sxs-lookup"><span data-stu-id="a6a9e-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="a6a9e-126">ละทิ้งเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="a6a9e-126">Discarded check out</span></span> | <span data-ttu-id="a6a9e-127">เมื่อมีการยกเลิกรายการ CMS ที่มีการเช็คเอาท์ การเปลี่ยนแปลงที่บันทึกไว้ทั้งหมดจะถูกลบออกและรายการนั้นจะเปลี่ยนไปเป็นเวอร์ชันที่เช็คอินล่าสุด</span><span class="sxs-lookup"><span data-stu-id="a6a9e-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a6a9e-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a6a9e-128">Additional resources</span></span>

[<span data-ttu-id="a6a9e-129">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="a6a9e-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="a6a9e-130">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="a6a9e-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="a6a9e-131">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="a6a9e-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="a6a9e-132">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="a6a9e-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="a6a9e-133">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="a6a9e-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="a6a9e-134">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="a6a9e-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a6a9e-135">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="a6a9e-135">Customize site navigation</span></span>](customize-site-navigation.md)
