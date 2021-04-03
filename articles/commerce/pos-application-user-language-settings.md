---
title: การตั้งค่าแอพลิเคชันการขายหน้าร้าน (POS) และภาษาผู้ใช้
description: หัวข้อนี้อธิบายวิธีเปลี่ยนการตั้งค่าภาษาใน Modern POS (MPOS) และ Cloud POS
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
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 09824d3b2eb8e3c1602882f19131d9fe312baaac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263167"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="9efa0-103">การตั้งค่าแอพลิเคชันการขายหน้าร้าน (POS) และภาษาผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9efa0-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9efa0-104">หัวข้อนี้อธิบายวิธีเปลี่ยนการตั้งค่าภาษาใน Modern POS (MPOS) และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="9efa0-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="9efa0-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9efa0-105">Overview</span></span>
<span data-ttu-id="9efa0-106">Modern POS (MPOS) และ Cloud POS รองรับสภาพแวดล้อมที่การตั้งค่าภาษาและการแปลอาจแตกต่างกันระหว่างร้านค้าและการตั้งค่าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9efa0-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="9efa0-107">ตัวอย่างเช่น ร้านค้าสามารถอยู่ในภูมิภาคที่ภาษาอังกฤษเป็นภาษาสามัญสำหรับลูกค้าของพวกเขา แต่ผู้ปฏิบัติงานบางคนต้องการใช้แอพลิเคชันที่มีการแปลภาษาฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="9efa0-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="9efa0-108">ข้อมูลภาษา</span><span class="sxs-lookup"><span data-stu-id="9efa0-108">Data language</span></span>

<span data-ttu-id="9efa0-109">โดยไม่คำนึงถึงการตั้งค่าของผู้ใช้ MPOS และ Cloud POS จะใช้การตั้งค่าภาษาของร้านค้าเพื่อกำหนดการแปลที่จะถูกใช้กับข้อมูลเสมอ</span><span class="sxs-lookup"><span data-stu-id="9efa0-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="9efa0-110">ซึ่งจะทำให้แน่ใจว่าผู้ใช้และลูกค้าทั้งหมดจะมีประสบการณ์ที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="9efa0-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="9efa0-111">ตัวอย่างของข้อมูล ได้แก่</span><span class="sxs-lookup"><span data-stu-id="9efa0-111">Examples of data include:</span></span>

- <span data-ttu-id="9efa0-112">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9efa0-112">Products</span></span>
- <span data-ttu-id="9efa0-113">แอททริบิวต์และมูลค่า</span><span class="sxs-lookup"><span data-stu-id="9efa0-113">Attributes and values</span></span>
- <span data-ttu-id="9efa0-114">ชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="9efa0-114">Category names</span></span>
- <span data-ttu-id="9efa0-115">ใบเสร็จรับเงินของธุรกรรมที่พิมพ์ออกมาหรือส่งทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="9efa0-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="9efa0-116">ชื่อวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9efa0-116">Payment method names</span></span>
- <span data-ttu-id="9efa0-117">ข้อความแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="9efa0-117">Line display messages</span></span>

<span data-ttu-id="9efa0-118">ภาษาของร้านค้าจะยังใช้สำหรับหน้าจอล็อคอินของ POS หลักด้วย เนื่องจากไม่รู้จักผู้ใช้ก่อนที่จะเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="9efa0-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="9efa0-119">ถ้าการแปลไม่พร้อมใช้งานสำหรับภาษาของร้านค้า POS จะเปลี่ยนกลับไปเป็นภาษาของบริษัท</span><span class="sxs-lookup"><span data-stu-id="9efa0-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="9efa0-120">การตั้งค่าคอนฟิกการตั้งค่าภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="9efa0-120">Configuring the store's language setting</span></span>

<span data-ttu-id="9efa0-121">การตั้งค่าภาษาของร้านค้า ถูกตั้งค่าจาก **ร้านค้าทั้งหมด** ในหน้า **ร้านค้า** ภายใต้ **ทั่วไป &gt; การตั้งค่าภูมิภาค &gt; ภาษา**</span><span class="sxs-lookup"><span data-stu-id="9efa0-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="9efa0-122">ใช้รายการแบบหล่นลงเพื่อเลือกภาษาสำหรับแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="9efa0-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="9efa0-123">ภาษาของอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9efa0-123">User interface language</span></span>

<span data-ttu-id="9efa0-124">การตั้งค่าภาษาของผู้ใช้ POS กำหนดการแปลที่ใช้ในอินเทอร์เฟสผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="9efa0-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="9efa0-125">ซึ่งรวมถึงป้ายชื่อ เมนู และรายการทั้งหมดที่ไม่ถือว่าเป็นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9efa0-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="9efa0-126">หนึ่งข้อยกเว้นต่อสิ่งนี้คือ ข้อความที่แสดงบนกริดปุ่ม POS</span><span class="sxs-lookup"><span data-stu-id="9efa0-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="9efa0-127">สิ่งเหล่านี้ไม่สนับสนุนการแปล ดังนั้นระบบจะแสดงข้อความตามที่กำหนดบนปุ่มเสมอ</span><span class="sxs-lookup"><span data-stu-id="9efa0-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="9efa0-128">เพื่อที่จะสนับสนุนปุ่มการแปล คุณจะต้องทำการคัดลอกและรักษากริดปุ่มที่แยกต่างหากและมอบหมายกริดปุ่มเหล่านั้นให้กับผู้ใช้ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9efa0-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="9efa0-129">การตั้งค่าคอนฟิกการตั้งค่าภาษาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9efa0-129">Configuring the user's language setting</span></span>

<span data-ttu-id="9efa0-130">การตั้งค่าภาษาของผู้ใช้ POS ถูกตั้งค่าจาก **คนงานทั้งหมด** ในหน้า **คนงาน** ภายใต้ **การขายปลีกและการค้า &gt; ภาษา**</span><span class="sxs-lookup"><span data-stu-id="9efa0-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="9efa0-131">การตั้งค่านี้ไม่ได้อยู่บนแท็บโพรไฟล์หลัก การตั้งค่านี้ไม่มีการใช้โดย POS</span><span class="sxs-lookup"><span data-stu-id="9efa0-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="9efa0-132">ถ้าภาษาของผู้ใช้ไม่ได้ถูกตั้งค่า หรือมีการตั้งค่าเป็นภาษาที่การแปลไม่พร้อมใช้งาน POS จะเปลี่ยนกลับไปยังภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="9efa0-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="9efa0-133">ภาษา UI  </span><span class="sxs-lookup"><span data-stu-id="9efa0-133">UI language</span></span>                | <span data-ttu-id="9efa0-134">ข้อมูลภาษา(ผลิตภัณฑ์ รูปแบบใบเสร็จ จอแสดงผลรายการ เป็นต้น)</span><span class="sxs-lookup"><span data-stu-id="9efa0-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9efa0-135">**บริษัท**</span><span class="sxs-lookup"><span data-stu-id="9efa0-135">**Company**</span></span> | <span data-ttu-id="9efa0-136">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9efa0-136">Default</span></span>                    | <span data-ttu-id="9efa0-137">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9efa0-137">Default</span></span>                                                       |
| <span data-ttu-id="9efa0-138">**ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="9efa0-138">**Store**</span></span>   | <span data-ttu-id="9efa0-139">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="9efa0-139">Overrides company</span></span>          | <span data-ttu-id="9efa0-140">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="9efa0-140">Overrides company</span></span>                                             |
| <span data-ttu-id="9efa0-141">**ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9efa0-141">**User**</span></span>    | <span data-ttu-id="9efa0-142">การแทนที่ร้านค้าหรือบริษัท</span><span class="sxs-lookup"><span data-stu-id="9efa0-142">Overrides store or company</span></span> | <span data-ttu-id="9efa0-143">ไม่</span><span class="sxs-lookup"><span data-stu-id="9efa0-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]