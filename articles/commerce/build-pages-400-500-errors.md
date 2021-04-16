---
title: สร้างหน้าการตอบสนองที่กำหนดเองสำหรับข้อผิดพลาดที่มีรหัสสถานะ 4xx/5xx
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าการตอบสนองที่กำหนดเองสำหรับข้อผิดพลาดที่มีรหัสสถานะ 4xx และ 5xx โดยใช้เครื่องมือการสร้างใน Microsoft Dynamics 365 Commerce
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799669"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="8145e-103">สร้างหน้าการตอบสนองที่กำหนดเองสำหรับข้อผิดพลาดที่มีรหัสสถานะ 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="8145e-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8145e-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าการตอบสนองที่กำหนดเองสำหรับข้อผิดพลาดที่มีรหัสสถานะ 4xx และ 5xx โดยใช้เครื่องมือการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8145e-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8145e-105">ถ้าคำขอหนึ่งไม่สำเร็จ เซิร์ฟเวอร์จะออกการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะของ HTTP</span><span class="sxs-lookup"><span data-stu-id="8145e-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="8145e-106">รหัสสถานะ 404 จะถูกรวบรวมและส่งคืนถ้าหาหน้าหน้าหนึ่งไม่พบ และรหัสสถานะ 500 จะถูกรวบรวมและส่งคืนถ้าข้อผิดพลาดของเซิร์ฟเวอร์เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="8145e-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="8145e-107">ใน Dynamics 365 Commerce ผู้ใช้แอปพลิเคชันสามารถสร้างหน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะที่กำหนดเองซึ่งจะแสดงต่อผู้ใช้ในการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8145e-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="8145e-108">สร้างหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ</span><span class="sxs-lookup"><span data-stu-id="8145e-108">Build a status code error response page</span></span>

<span data-ttu-id="8145e-109">เมื่อต้องการสร้างหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8145e-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="8145e-110">ในเว็บเบราเซอร์ที่คุณต้องการ ให้ลงชื่อเข้าสู่ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8145e-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="8145e-111">เลือกไซต์ที่คุณต้องการสร้างหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="8145e-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="8145e-112">สร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8145e-112">Build the template</span></span>

<span data-ttu-id="8145e-113">เมื่อต้องการสร้างเท็มเพลตของหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8145e-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="8145e-114">ไปที่ **เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="8145e-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="8145e-115">เลือก **สร้าง** เพื่อสร้างเท็มเพลตของหน้า</span><span class="sxs-lookup"><span data-stu-id="8145e-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="8145e-116">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อสำหรับเท็มเพลตใหม่ และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8145e-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="8145e-117">สร้างเท็มเพลต โดยยึดตามโครงสร้างที่คุณต้องการให้หน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะมี</span><span class="sxs-lookup"><span data-stu-id="8145e-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="8145e-118">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8145e-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="8145e-119">สร้างหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ</span><span class="sxs-lookup"><span data-stu-id="8145e-119">Build the status code error response page</span></span>

<span data-ttu-id="8145e-120">เมื่อต้องการสร้างหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8145e-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="8145e-121">ไปที่ **หน้า**</span><span class="sxs-lookup"><span data-stu-id="8145e-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="8145e-122">เลือก **สร้าง** เพื่อสร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="8145e-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="8145e-123">ในกล่องโต้ตอบ **เลือกเท็มเพลต** เลือกเท็มเพลต และจากนั้น ภายใต้ **ชื่อหน้า** ให้ป้อนชื่อสำหรับหน้าการตอบสนองข้อผิดพลาดของรหัสสถานะ</span><span class="sxs-lookup"><span data-stu-id="8145e-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="8145e-124">ปล่อยฟิลด์ **URL ของหน้า** ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="8145e-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="8145e-125">สร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="8145e-125">Build the page.</span></span>
1. <span data-ttu-id="8145e-126">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8145e-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="8145e-127">คุณสามารถสร้างหน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะที่แยกจากกันต่างหากสำหรับข้อผิดพลาดที่มีรหัสสถานะ 4xx และ 5xx ได้</span><span class="sxs-lookup"><span data-stu-id="8145e-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="8145e-128">อีกทางหนึ่ง คือ คุณสามารถใช้หน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะทั่วไปที่เหมือนกันสำหรับประเภทของข้อผิดพลาดทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="8145e-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="8145e-129">ตั้งค่าการเปลี่ยนเส้นทางสำหรับหน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะ</span><span class="sxs-lookup"><span data-stu-id="8145e-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="8145e-130">เมื่อต้องการตั้งค่าการเปลี่ยนเส้นทางของหน้าการตอบสนองของข้อผิดพลาดที่มีรหัสสถานะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8145e-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="8145e-131">ไปที่ **URL \> ใหม่ \> ชื่อเสริมใหม่** และเลือกหน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8145e-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="8145e-132">ในฟิลด์ **ชื่อเสริม** ให้ป้อนว่า **ค่าเริ่มต้น-4xx** หรือ **ค่าเริ่มต้น-5xx** ขึ้นอยู่กับว่าหน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะที่คุณกำลังตั้งค่าการเปลี่ยนเส้นทางคืออะไร</span><span class="sxs-lookup"><span data-stu-id="8145e-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="8145e-133">ชื่อเสริมเหล่านี้ต้องถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8145e-133">These aliases must be published.</span></span> <span data-ttu-id="8145e-134">มิฉะนั้น การเปลี่ยนเส้นทางจะใช้งานไม่ได้</span><span class="sxs-lookup"><span data-stu-id="8145e-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="8145e-135">เลือก **ตกลง** เพื่อยืนยันการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="8145e-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="8145e-136">ถ้าคุณกำลังใช้หน้าการตอบสนองข้อผิดพลาดที่มีรหัสสถานะเดียวสำหรับประเภทข้อผิดพลาดทั้งสองประเภท ให้ทำกระบวนงานนี้ซ้ำเพื่อเชื่อมโยงชื่อเสริมสำหรับประเภทข้อผิดพลาดอื่น ๆ กับหน้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8145e-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8145e-137">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8145e-137">Additional resources</span></span>

[<span data-ttu-id="8145e-138">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="8145e-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="8145e-139">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="8145e-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8145e-140">สร้าง URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="8145e-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
