---
title: การตั้งค่าแอพลิเคชันการขายหน้าร้าน (POS) และภาษาผู้ใช้
description: หัวข้อนี้อธิบายวิธีการเปลี่ยนการตั้งค่าภาษาใน Retail Modern POS (MPOS) และ Cloud POS
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545111"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="c0478-103">การตั้งค่าแอพลิเคชันการขายหน้าร้าน (POS) และภาษาผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c0478-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0478-104">หัวข้อนี้อธิบายวิธีการเปลี่ยนการตั้งค่าภาษาใน Retail Modern POS (MPOS) และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="c0478-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="c0478-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c0478-105">Overview</span></span>

<span data-ttu-id="c0478-106">Retail Modern POS (MPOS) และ Cloud POS สนับสนุนสภาพแวดล้อมที่ซึ่งการตั้งค่าภาษาและการแปล อาจแตกต่างกันไประหว่างการตั้งค่าร้านค้าและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c0478-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="c0478-107">ตัวอย่างเช่น ร้านค้าสามารถอยู่ในภูมิภาคที่ภาษาอังกฤษเป็นภาษาสามัญสำหรับลูกค้าของพวกเขา แต่ผู้ปฏิบัติงานบางคนต้องการใช้แอพลิเคชันที่มีการแปลภาษาฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="c0478-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="c0478-108">ข้อมูลภาษา</span><span class="sxs-lookup"><span data-stu-id="c0478-108">Data language</span></span>

<span data-ttu-id="c0478-109">โดยไม่คำนึงถึงการตั้งค่าของผู้ใช้ MPOS และ Cloud POS จะใช้การตั้งค่าภาษาของร้านค้าเพื่อกำหนดการแปลที่จะถูกใช้กับข้อมูลเสมอ</span><span class="sxs-lookup"><span data-stu-id="c0478-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="c0478-110">ซึ่งจะทำให้แน่ใจว่าผู้ใช้และลูกค้าทั้งหมดจะมีประสบการณ์ที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="c0478-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="c0478-111">ตัวอย่างของข้อมูล ได้แก่</span><span class="sxs-lookup"><span data-stu-id="c0478-111">Examples of data include:</span></span>

- <span data-ttu-id="c0478-112">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0478-112">Products</span></span>
- <span data-ttu-id="c0478-113">แอททริบิวต์และมูลค่า</span><span class="sxs-lookup"><span data-stu-id="c0478-113">Attributes and values</span></span>
- <span data-ttu-id="c0478-114">ชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="c0478-114">Category names</span></span>
- <span data-ttu-id="c0478-115">ใบเสร็จรับเงินของธุรกรรมที่พิมพ์ออกมาหรือส่งทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="c0478-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="c0478-116">ชื่อวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c0478-116">Payment method names</span></span>
- <span data-ttu-id="c0478-117">ข้อความแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="c0478-117">Line display messages</span></span>

<span data-ttu-id="c0478-118">ภาษาของร้านค้าจะยังใช้สำหรับหน้าจอล็อคอินของ POS หลักด้วย เนื่องจากไม่รู้จักผู้ใช้ก่อนที่จะเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="c0478-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="c0478-119">ถ้าการแปลไม่พร้อมใช้งานสำหรับภาษาของร้านค้า POS จะเปลี่ยนกลับไปเป็นภาษาของบริษัท</span><span class="sxs-lookup"><span data-stu-id="c0478-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="c0478-120">การตั้งค่าคอนฟิกการตั้งค่าภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="c0478-120">Configuring the store's language setting</span></span>

<span data-ttu-id="c0478-121">การตั้งค่าภาษาของร้านค้าถูกตั้งค่าจาก **ร้านค้าปลีกทั้งหมด** ในหน้า **ร้านค้าปลีก** ภายใต้ **ทั่วไป &gt; การตั้งค่าภูมิภาค &gt; ภาษา**</span><span class="sxs-lookup"><span data-stu-id="c0478-121">The store's language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="c0478-122">ใช้รายการแบบหล่นลงเพื่อเลือกภาษาสำหรับแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="c0478-122">Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="c0478-123">ภาษาของอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c0478-123">User interface language</span></span>

<span data-ttu-id="c0478-124">การตั้งค่าภาษาของผู้ใช้ POS กำหนดการแปลที่ใช้ในอินเทอร์เฟสผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c0478-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="c0478-125">ซึ่งรวมถึงป้ายชื่อ เมนู และรายการทั้งหมดที่ไม่ถือว่าเป็นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c0478-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="c0478-126">หนึ่งข้อยกเว้นต่อสิ่งนี้คือ ข้อความที่แสดงบนกริดปุ่ม POS</span><span class="sxs-lookup"><span data-stu-id="c0478-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="c0478-127">สิ่งเหล่านี้ไม่สนับสนุนการแปล ดังนั้นระบบจะแสดงข้อความตามที่กำหนดบนปุ่มเสมอ</span><span class="sxs-lookup"><span data-stu-id="c0478-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="c0478-128">เพื่อที่จะสนับสนุนปุ่มการแปล คุณจะต้องทำการคัดลอกและรักษากริดปุ่มที่แยกต่างหากและมอบหมายกริดปุ่มเหล่านั้นให้กับผู้ใช้ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c0478-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="c0478-129">การตั้งค่าคอนฟิกการตั้งค่าภาษาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c0478-129">Configuring the user's language setting</span></span>

<span data-ttu-id="c0478-130">การตั้งค่าภาษาของผู้ใช้ POS ถูกตั้งค่ามาจาก **พนักงานทั้งหมด** ในหน้า **ผู้ปฏิบัติงาน** ภายใต้ **การขายปลีก &gt; ภาษา**</span><span class="sxs-lookup"><span data-stu-id="c0478-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span> <span data-ttu-id="c0478-131">การตั้งค่านี้ไม่ได้อยู่บนแท็บโพรไฟล์หลัก การตั้งค่านี้ไม่มีการใช้โดย POS</span><span class="sxs-lookup"><span data-stu-id="c0478-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="c0478-132">ถ้าภาษาของผู้ใช้ไม่ได้ถูกตั้งค่า หรือมีการตั้งค่าเป็นภาษาที่การแปลไม่พร้อมใช้งาน POS จะเปลี่ยนกลับไปยังภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="c0478-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="c0478-133">ภาษา UI  </span><span class="sxs-lookup"><span data-stu-id="c0478-133">UI language</span></span>                | <span data-ttu-id="c0478-134">ข้อมูลภาษา(ผลิตภัณฑ์ รูปแบบใบเสร็จ จอแสดงผลรายการ เป็นต้น)</span><span class="sxs-lookup"><span data-stu-id="c0478-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c0478-135">**บริษัท**</span><span class="sxs-lookup"><span data-stu-id="c0478-135">**Company**</span></span> | <span data-ttu-id="c0478-136">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0478-136">Default</span></span>                    | <span data-ttu-id="c0478-137">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0478-137">Default</span></span>                                                       |
| <span data-ttu-id="c0478-138">**ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="c0478-138">**Store**</span></span>   | <span data-ttu-id="c0478-139">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="c0478-139">Overrides company</span></span>          | <span data-ttu-id="c0478-140">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="c0478-140">Overrides company</span></span>                                             |
| <span data-ttu-id="c0478-141">**ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="c0478-141">**User**</span></span>    | <span data-ttu-id="c0478-142">การแทนที่ร้านค้าหรือบริษัท</span><span class="sxs-lookup"><span data-stu-id="c0478-142">Overrides store or company</span></span> | <span data-ttu-id="c0478-143">ไม่</span><span class="sxs-lookup"><span data-stu-id="c0478-143">Never</span></span>                                                         |
