---
title: เพิ่มข้อความสงวนลิขสิทธิ์
description: หัวข้อนี้อธิบายวิธีการเพิ่มข้อความสงวนลิขสิทธิ์ให้กับเว็บไซต์อีคอมเมิร์ซของคุณ
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206378"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="8113f-103">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="8113f-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8113f-104">หัวข้อนี้อธิบายวิธีการเพิ่มข้อความสงวนลิขสิทธิ์ให้กับเว็บไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="8113f-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8113f-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8113f-105">Prerequisites</span></span>

<span data-ttu-id="8113f-106">ก่อนที่คุณจะสามารถเพิ่มข้อความสงวนลิขสิทธิ์ลงในไซต์ของคุณ คุณจะต้องมีสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8113f-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="8113f-107">แม่แบบที่รวมส่วนที่เป็นส่วนท้ายที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="8113f-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="8113f-108">เพจที่ใช้แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="8113f-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="8113f-109">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="8113f-109">Add a copyright notice</span></span>

<span data-ttu-id="8113f-110">เมื่อต้องการเพิ่มข้อความสงวนลิขสิทธิ์ที่ด้านล่างของทุกเพจที่ใช้แม่แบบเฉพาะ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8113f-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="8113f-111">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8113f-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="8113f-112">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **ส่วนท้าย** และตั้งชื่อส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="8113f-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="8113f-113">ตัวอย่างเช่น ป้อน **ส่วนท้าย-ลิขสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="8113f-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="8113f-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8113f-114">Select **OK**.</span></span>
1. <span data-ttu-id="8113f-115">ในบานหน้าต่างนำทาง เลือกปุ่มจุดไข่ปลา (**...**) ถัดจาก **ส่วนท้าย** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="8113f-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8113f-116">ในกล่องโต้ตอบ เลือก **ประเภทของส่วนท้าย** แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8113f-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="8113f-117">ในบานหน้าต่างนำทาง เลือกปุ่มจุดไข่ปลาถัดจาก **ประเภทของส่วนท้าย** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="8113f-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8113f-118">ในกล่องโต้ตอบ เลือก **บล็อคข้อความ** แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8113f-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="8113f-119">ในบานหน้าต่างนำทางให้เลือก **บล็อกข้อความ**</span><span class="sxs-lookup"><span data-stu-id="8113f-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="8113f-120">ในบานหน้าต่างคุณสมบัติทางด้านขวา ในฟิลด์ **ย่อหน้า** ให้เพิ่มข้อความลิขสิทธิ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8113f-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="8113f-121">ตัวอย่างเช่น: ป้อน **(C) Fabrikam 2019**</span><span class="sxs-lookup"><span data-stu-id="8113f-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="8113f-122">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** แล้วจากนั้น เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="8113f-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="8113f-123">ไปที่ **เท็มเพลต** เลือกเท็มเพลต และจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8113f-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="8113f-124">ภายใต้ **โครงร่างเพจ** ขยาย **เนื้อหา** แล้วขยาย **เพจเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="8113f-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="8113f-125">เลือกปุ่มจุดไข่ปลาถัดจาก **ช่องส่วนท้าย** จากนั้นเลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="8113f-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="8113f-126">เลือกส่วนที่คุณสร้างไว้ก่อนหน้านี้ แล้วเลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="8113f-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="8113f-127">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8113f-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="8113f-128">ส่วนท้ายที่มีข้อความสงวนลิขสิทธิ์จะปรากฏขึ้นโดยอัตโนมัติที่ด้านล่างของเพจทั้งหมดที่ใช้แม่แบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8113f-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8113f-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8113f-129">Additional resources</span></span>

[<span data-ttu-id="8113f-130">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="8113f-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="8113f-131">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="8113f-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="8113f-132">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="8113f-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="8113f-133">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="8113f-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="8113f-134">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="8113f-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="8113f-135">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8113f-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="8113f-136">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="8113f-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]