---
title: เพิ่มข้อความสงวนลิขสิทธิ์
description: หัวข้อนี้อธิบายวิธีการเพิ่มข้อความสงวนลิขสิทธิ์ให้กับเว็บไซต์อีคอมเมิร์ซของคุณ
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696956"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="a1d44-103">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a1d44-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a1d44-104">หัวข้อนี้อธิบายวิธีการเพิ่มข้อความสงวนลิขสิทธิ์ให้กับเว็บไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="a1d44-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a1d44-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a1d44-105">Prerequisites</span></span>

<span data-ttu-id="a1d44-106">ก่อนที่คุณจะสามารถเพิ่มข้อความสงวนลิขสิทธิ์ลงในไซต์ของคุณ คุณจะต้องมีสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a1d44-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="a1d44-107">แม่แบบที่รวมส่วนที่เป็นส่วนท้ายที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="a1d44-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="a1d44-108">เพจที่ใช้แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="a1d44-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="a1d44-109">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a1d44-109">Add a copyright notice</span></span>

<span data-ttu-id="a1d44-110">เมื่อต้องการเพิ่มข้อความสงวนลิขสิทธิ์ที่ด้านล่างของทุกเพจที่ใช้แม่แบบเฉพาะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a1d44-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="a1d44-111">ไปที่ **ส่วน** จากนั้น ให้เลือก **ส่วนของเพจใหม่**</span><span class="sxs-lookup"><span data-stu-id="a1d44-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="a1d44-112">ในกล่องโต้ตอบ ให้เลือกโมล **ส่วนท้าย** และตั้งชื่อส่วน</span><span class="sxs-lookup"><span data-stu-id="a1d44-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="a1d44-113">ตัวอย่างเช่น ป้อน **ส่วนท้าย-ลิขสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="a1d44-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="a1d44-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a1d44-114">Select **OK**.</span></span>
1. <span data-ttu-id="a1d44-115">ในบานหน้าต่างนำทาง เลือกปุ่มจุดไข่ปลา (**...**) ถัดจาก **ส่วนท้าย** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="a1d44-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a1d44-116">ในกล่องโต้ตอบ เลือก **ประเภทของส่วนท้าย** แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a1d44-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="a1d44-117">ในบานหน้าต่างนำทาง เลือกปุ่มจุดไข่ปลาถัดจาก **ประเภทของส่วนท้าย** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="a1d44-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a1d44-118">ในกล่องโต้ตอบ เลือก **สินค้าบล็อกเนื้อหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a1d44-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="a1d44-119">ในบานหน้าต่างนำทาง ให้เลือก **สินค้าบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="a1d44-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="a1d44-120">ในบานหน้าต่างคุณสมบัติทางด้านขวา ในฟิลด์ **ย่อหน้า** ให้เพิ่มข้อความลิขสิทธิ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a1d44-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="a1d44-121">ตัวอย่างเช่น: ป้อน **(C) Fabrikam 2019**</span><span class="sxs-lookup"><span data-stu-id="a1d44-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="a1d44-122">เลือก **บันทึก** เลือก **เช็คอิน** แล้วจากนั้น เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="a1d44-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="a1d44-123">ไปที่ **แม่แบบ** แล้วเลือกเท็มเพลต จากนั้นเลือก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="a1d44-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="a1d44-124">ภายใต้ **โครงร่างเพจ** ขยาย **เนื้อหา** แล้วขยาย **เพจเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="a1d44-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="a1d44-125">เลือกปุ่มจุดไข่ปลาถัดจาก **ช่องส่วนท้าย** จากนั้นเลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="a1d44-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="a1d44-126">เลือกส่วนที่คุณสร้างไว้ก่อนหน้านี้ แล้วเลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="a1d44-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="a1d44-127">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="a1d44-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="a1d44-128">ส่วนท้ายที่มีข้อความสงวนลิขสิทธิ์จะปรากฏขึ้นโดยอัตโนมัติที่ด้านล่างของเพจทั้งหมดที่ใช้แม่แบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a1d44-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1d44-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a1d44-129">Additional resources</span></span>

[<span data-ttu-id="a1d44-130">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="a1d44-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="a1d44-131">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="a1d44-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="a1d44-132">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="a1d44-132">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="a1d44-133">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="a1d44-133">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="a1d44-134">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a1d44-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a1d44-135">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="a1d44-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

