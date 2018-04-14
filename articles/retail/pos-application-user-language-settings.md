---
title: "แอพลิเคชัน POS และการตั้งค่าภาษาผู้ใช้"
description: "หัวข้อนี้อธิบายวิธีการเปลี่ยนแปลงการตั้งค่าภาษาใน Modern POS ของการขายปลีก (MPOS) และ Cloud POS"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8c265332b132f51e948fff9e6feffee94c38ff07
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="51bf2-103">แอพลิเคชัน POS และการตั้งค่าภาษาผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="51bf2-103">POS application and user language settings</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="51bf2-104">หัวข้อนี้อธิบายวิธีการเปลี่ยนแปลงการตั้งค่าภาษาใน Modern POS ของการขายปลีก (MPOS) และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="51bf2-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="51bf2-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="51bf2-105">Overview</span></span>
<span data-ttu-id="51bf2-106">Modern POS ของการขายปลีก (MPOS) and Cloud POS สนับสนุนสภาพแวดล้อมที่การตั้งค่าภาษาและการแปลอาจแตกต่างกันระหว่างการตั้งค่าร้านค้าและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="51bf2-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="51bf2-107">ตัวอย่างเช่น ร้านค้าสามารถอยู่ในภูมิภาคที่ภาษาอังกฤษเป็นภาษาสามัญสำหรับลูกค้าของพวกเขา แต่ผู้ปฏิบัติงานบางคนต้องการใช้แอพลิเคชันที่มีการแปลภาษาฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="51bf2-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="51bf2-108">ข้อมูลภาษา</span><span class="sxs-lookup"><span data-stu-id="51bf2-108">Data language</span></span>
<span data-ttu-id="51bf2-109">โดยไม่คำนึงถึงการตั้งค่าของผู้ใช้ MPOS และ Cloud POS จะใช้การตั้งค่าภาษาของร้านค้าเพื่อกำหนดการแปลที่จะถูกใช้กับข้อมูลเสมอ</span><span class="sxs-lookup"><span data-stu-id="51bf2-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="51bf2-110">ซึ่งจะทำให้แน่ใจว่าผู้ใช้และลูกค้าทั้งหมดจะมีประสบการณ์ที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="51bf2-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="51bf2-111">ตัวอย่างของข้อมูล ได้แก่</span><span class="sxs-lookup"><span data-stu-id="51bf2-111">Examples of data include:</span></span>

-   <span data-ttu-id="51bf2-112">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="51bf2-112">Products</span></span>
-   <span data-ttu-id="51bf2-113">แอททริบิวต์และมูลค่า</span><span class="sxs-lookup"><span data-stu-id="51bf2-113">Attributes and values</span></span>
-   <span data-ttu-id="51bf2-114">ชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="51bf2-114">Category names</span></span>
-   <span data-ttu-id="51bf2-115">ใบเสร็จรับเงินของธุรกรรมที่พิมพ์ออกมาหรือส่งทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="51bf2-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="51bf2-116">ชื่อวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51bf2-116">Payment method names</span></span>
-   <span data-ttu-id="51bf2-117">ข้อความแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="51bf2-117">Line display messages</span></span>

<span data-ttu-id="51bf2-118">ภาษาของร้านค้าจะยังใช้สำหรับหน้าจอล็อคอินหลักของ POS เนื่องจากไม่รู้จักผู้ใช้ก่อนที่จะเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="51bf2-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="51bf2-119">ถ้าการแปลไม่พร้อมใช้งานสำหรับภาษาของร้านค้า POS จะเปลี่ยนกลับไปเป็นภาษาของบริษัท</span><span class="sxs-lookup"><span data-stu-id="51bf2-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="51bf2-120">การตั้งค่าคอนฟิกการตั้งค่าภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="51bf2-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="51bf2-121">การตั้งค่าภาษาของร้านค้าจากหน้า **ร้านค้าปลีกทั้งหมด** ในหน้า **ร้านค้าปลีก** ภายใต้ ** ทั่วไป &gt; การตั้งค่าภูมิภาค &gt; ภาษา</span><span class="sxs-lookup"><span data-stu-id="51bf2-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="51bf2-122">**ใช้รายการที่หล่นลงมาเพื่อเลือกภาษาสำหรับแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="51bf2-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="51bf2-123">ภาษาของอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="51bf2-123">User interface language</span></span>
<span data-ttu-id="51bf2-124">การตั้งค่าภาษาของผู้ใช้ POS กำหนดว่าการแปลที่ใช้ในอินเทอร์เฟสผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="51bf2-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="51bf2-125">ซึ่งรวมถึงป้ายชื่อ เมนู และรายการทั้งหมดที่ไม่ถือว่าเป็นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="51bf2-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="51bf2-126">หนึ่งข้อยกเว้นต่อสิ่งนี้คือ ข้อความที่แสดงบนกริดปุ่ม POS</span><span class="sxs-lookup"><span data-stu-id="51bf2-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="51bf2-127">สิ่งเหล่านี้ไม่สนับสนุนการแปล ดังนั้นระบบจะแสดงข้อความตามที่กำหนดบนปุ่มเสมอ</span><span class="sxs-lookup"><span data-stu-id="51bf2-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="51bf2-128">เพื่อที่จะสนับสนุนปุ่มการแปล คุณจะต้องทำการคัดลอกและรักษากริดปุ่มที่แยกต่างหากและมอบหมายกริดปุ่มเหล่านั้นให้กับผู้ใช้ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="51bf2-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="51bf2-129">การตั้งค่าคอนฟิกการตั้งค่าภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="51bf2-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="51bf2-130">ตั้งค่าจากการตั้งค่าภาษาของผู้ใช้ POS มาจากการตั้งค่า **ผู้ปฏิบัติงานทั้งหมด** ในหน้า **ผู้ปฏิบัติงาน** ภายใต้ **การขายปลีก &gt; ภาษา**</span><span class="sxs-lookup"><span data-stu-id="51bf2-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="51bf2-131">การตั้งค่านี้ ไม่ ได้ตั้งค่าบนแท็บโพรไฟล์หลัก  การตั้งค่านี้ไม่มีใช้โดย POS</span><span class="sxs-lookup"><span data-stu-id="51bf2-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="51bf2-132">ถ้าภาษาของผู้ใช่ไม่ได้ถูกตั้งค่าหรือมีการตั้งค่าไปยังภาษาที่การแปลไม่พร้อมใช้งาน POS จะเปลี่ยนกลับไปยังภาษาของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="51bf2-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="51bf2-133">** **</span><span class="sxs-lookup"><span data-stu-id="51bf2-133">** **</span></span>       | <span data-ttu-id="51bf2-134">**ภาษา UI** ** **</span><span class="sxs-lookup"><span data-stu-id="51bf2-134">**UI language** ** **</span></span>      | <span data-ttu-id="51bf2-135">**ข้อมูลภาษา(ผลิตภัณฑ์ รูปแบบใบเสร็จ จอแสดงผลรายการ เป็นต้น)**</span><span class="sxs-lookup"><span data-stu-id="51bf2-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="51bf2-136">**บริษัท**</span><span class="sxs-lookup"><span data-stu-id="51bf2-136">**Company**</span></span> | <span data-ttu-id="51bf2-137">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="51bf2-137">Default</span></span>                    | <span data-ttu-id="51bf2-138">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="51bf2-138">Default</span></span>                                                           |
| <span data-ttu-id="51bf2-139">**ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="51bf2-139">**Store**</span></span>   | <span data-ttu-id="51bf2-140">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="51bf2-140">Overrides company</span></span>          | <span data-ttu-id="51bf2-141">การแทนที่บริษัท</span><span class="sxs-lookup"><span data-stu-id="51bf2-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="51bf2-142">**ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="51bf2-142">**User**</span></span>    | <span data-ttu-id="51bf2-143">การแทนที่ร้านค้าหรือบริษัท</span><span class="sxs-lookup"><span data-stu-id="51bf2-143">Overrides store or company</span></span> | <span data-ttu-id="51bf2-144">ไม่</span><span class="sxs-lookup"><span data-stu-id="51bf2-144">Never</span></span>                                                             |






