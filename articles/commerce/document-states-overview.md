---
title: สถานะและระยะเวลาใช้งานของเอกสาร
description: หัวข้อนี้จะครอบคลุมถึงสถานะเอกสารต่างๆขององค์ประกอบหน้าใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c30932800beda13ac8fe6b0386fe29efe93f79c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982627"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="d5961-103">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d5961-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5961-104">หัวข้อนี้จะครอบคลุมถึงสถานะเอกสารต่างๆขององค์ประกอบหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d5961-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="d5961-105">คำอธิบายสถานะเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d5961-105">Document state descriptions</span></span>

<span data-ttu-id="d5961-106">หัวข้อ [องค์ประกอบของหน้า](page-elements-overview.md) จะแสดงรายการชนิดเอกสารต่างๆในระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="d5961-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="d5961-107">ชนิดเอกสารเหล่านี้อาจมีหลายสถานะในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="d5961-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="d5961-108">สถานะเอกสารช่วยป้องกันความขัดแย้งของข้อมูล และบังคับใช้การควบคุมเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="d5961-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="d5961-109">ซึ่งจะกำหนดว่าใครบ้างที่สามารถเปลี่ยนแปลงเอกสารได้ เมื่อใดที่สามารถเปลี่ยนเอกสารได้ และเมื่อใดที่สามารถดูการเปลี่ยนแปลงของบุคคลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="d5961-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="d5961-110">ตารางต่อไปนี้แสดงสถานะเอกสารที่เป็นไปได้ขององค์ประกอบใน Commerce</span><span class="sxs-lookup"><span data-stu-id="d5961-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="d5961-111">สถานะเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d5961-111">Document state</span></span>      | <span data-ttu-id="d5961-112">การดำเนินการตัวสร้างไซต์ </span><span class="sxs-lookup"><span data-stu-id="d5961-112">Site builder action</span></span>        | <span data-ttu-id="d5961-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d5961-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="d5961-114">เช็คเอาท์แล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-114">Checked out</span></span>         | <span data-ttu-id="d5961-115">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5961-115">Select **Edit**.</span></span>           | <span data-ttu-id="d5961-116">เอกสารที่ใช้ได้จะถูกเช็คเอาท์ไปยังคุณ</span><span class="sxs-lookup"><span data-stu-id="d5961-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="d5961-117">ในขณะที่เอกสารอยู่ในสถานะนี้ ผู้ใช้ระบบคนอื่นๆ ที่ได้รับการพิสูจน์ตัวจริงแล้วจะไม่สามารถเปลี่ยนแปลงได้ และการเปลี่ยนแปลงใดๆ ที่คุณทำกับเอกสารมีคุณเท่านั้นที่สามารถมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="d5961-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="d5961-118">บันทึกแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-118">Saved</span></span>               | <span data-ttu-id="d5961-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d5961-119">Select **Save**.</span></span>           | <span data-ttu-id="d5961-120">มีการบันทึกการเปลี่ยนแปลงที่เกิดขึ้นกับเอกสารที่มีการเช็คเอาท์และบันทึกไว้ในฐานข้อมูล แต่เอกสารยังไม่ได้รับการเช็คอินหรือเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d5961-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="d5961-121">ผู้ใช้ระบบที่ได้รับการยืนยันตัวตนจะไม่สามารถมองเห็นการเปลี่ยนแปลงที่บันทึกไว้ได้จนกว่าผู้สร้างจะเลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5961-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="d5961-122">ผู้ใช้ภายนอกไม่สามารถมองเห็นได้จนกว่าจะมีการเผยแพร่รายการ</span><span class="sxs-lookup"><span data-stu-id="d5961-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="d5961-123">ละทิ้งเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="d5961-123">Discarded check out</span></span> | <span data-ttu-id="d5961-124">เลือก **ละทิ้งการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5961-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="d5961-125">การเปลี่ยนแปลงที่เกิดขึ้นกับเอกสารการเช็คเอาท์ทั้งหมดจะถูกยกเลิก และสินค้าจะเปลี่ยนเป็นเวอร์ชันล่าสุดที่เช็คอินแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="d5961-126">เช็คอินแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-126">Checked in</span></span>          | <span data-ttu-id="d5961-127">เลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5961-127">Select **Finish editing**.</span></span> | <span data-ttu-id="d5961-128">เช็คอินเอกสารที่ได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-128">The edited document is checked in.</span></span> <span data-ttu-id="d5961-129">การเปลี่ยนแปลงทั้งหมดจะสามารถมองเห็นได้สำหรับผู้ใช้ระบบคนอื่นๆ ที่ได้รับการพิสูจน์ตัวจริง และผู้ใช้เหล่านั้นสามารถแก้ไขเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="d5961-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="d5961-130">การเช็คอินแต่ละครั้งจะสร้างเรกคอร์ดเวอร์ชันเอกสารในประวัติของรายการ</span><span class="sxs-lookup"><span data-stu-id="d5961-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="d5961-131">เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="d5961-131">Published</span></span>           | <span data-ttu-id="d5961-132">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="d5961-132">Select **Publish**.</span></span>        | <span data-ttu-id="d5961-133">เอกสารมีการเผยแพร่ และการเปลี่ยนแปลงจะถูกผลักดดันไปให้กับไซต์ที่ถ่ายทอดสดของคุณ และจะสามารถมองเห็นได้โดยผู้ใช้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d5961-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="d5961-134">สามารถเผยแพร่สินค้าได้เฉพาะเมื่อมีการเช็คอินก่อนแล้วโดยการเลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5961-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d5961-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d5961-135">Additional resources</span></span>

[<span data-ttu-id="d5961-136">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="d5961-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="d5961-137">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="d5961-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="d5961-138">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d5961-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="d5961-139">เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="d5961-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="d5961-140">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="d5961-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="d5961-141">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="d5961-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d5961-142">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="d5961-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d5961-143">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="d5961-143">Customize site navigation</span></span>](customize-site-navigation.md)
