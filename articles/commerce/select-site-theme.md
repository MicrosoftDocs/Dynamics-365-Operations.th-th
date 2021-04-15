---
title: เลือกธีมของไซต์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794078"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="6dcef-103">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="6dcef-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6dcef-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6dcef-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6dcef-105">โครงร่างและลักษณะของไซต์ (ตัวอย่างเช่น แบบอักษร ขนาด และสี) จะถูกกำหนดโดยชุดรูปแบบที่คุณเลือกและนำไปใช้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="6dcef-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="6dcef-106">ชุดรูปแบบจะถูกสร้างขึ้น และใช้งานโดยนักพัฒนาที่บริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="6dcef-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="6dcef-107">สำหรับภาพรวมของชุดรูปแบบโปรดดู [ภาพรวมของชุดรูปแบบ](e-commerce-extensibility/theming.md)</span><span class="sxs-lookup"><span data-stu-id="6dcef-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="6dcef-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและปรับใช้ชุดรูปแบบ โปรดดู [สร้างชุดรูปแบบใหม่](e-commerce-extensibility/create-theme.md)</span><span class="sxs-lookup"><span data-stu-id="6dcef-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="6dcef-109">โดยค่าเริ่มต้น เมื่อคุณสร้างไซต์เป็นครั้งแรกระบบจะใช้ชุดรูปแบบที่ชื่อ **Fabrikam**</span><span class="sxs-lookup"><span data-stu-id="6dcef-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="6dcef-110">ธีมเริ่มต้นนี้ให้ไว้เป็นส่วนหนึ่งของไลบรารีโมดูล Commerce</span><span class="sxs-lookup"><span data-stu-id="6dcef-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="6dcef-111">หลังจากที่คุณได้ปรับใช้ชุดรูปแบบเพิ่มเติมสำหรับไซต์ของคุณแล้ว คุณสามารถตั้งค่าคอนฟิกไซต์ดังกล่าวเพื่อให้ใช้งานได้อย่างใดอย่างหนึ่งแทน</span><span class="sxs-lookup"><span data-stu-id="6dcef-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="6dcef-112">เลือกชุดรูปแบบของไซต์</span><span class="sxs-lookup"><span data-stu-id="6dcef-112">Select the site theme</span></span>

<span data-ttu-id="6dcef-113">เมื่อต้องการเลือกชุดรูปแบบที่จะใช้กับไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6dcef-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="6dcef-114">ในสภาพแวดล้อมการสร้างและแก้ไขไซต์ ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6dcef-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="6dcef-115">ไปที่ **การจัดการไซต์** \> **เพิ่มความสามารถ**</span><span class="sxs-lookup"><span data-stu-id="6dcef-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="6dcef-116">ภายใต้ **ชุดรูปแบบ** ให้เลือกชุดรูปแบบในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="6dcef-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="6dcef-117">เมื่อต้องการใช้ชุดรูปแบบที่เลือกกับไซต์ของคุณให้เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="6dcef-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="6dcef-118">ชุดรูปแบบที่คุณเลือกเผยแพร่ไปยังไซต์ของคุณ ทันทีที่คุณเลือก **บันทึกและเผยแพร่** บนหน้า **เพิ่มความสามารถ**</span><span class="sxs-lookup"><span data-stu-id="6dcef-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="6dcef-119">เมื่อต้องการแสดงตัวอย่างชุดรูปแบบบนไซต์ของคุณก่อนที่จะใช้งาน คุณสามารถใช้สภาพแวดล้อมการพัฒนาหรือ Sandbox ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6dcef-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dcef-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6dcef-120">Additional resources</span></span>

[<span data-ttu-id="6dcef-121">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="6dcef-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6dcef-122">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="6dcef-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6dcef-123">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="6dcef-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6dcef-124">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="6dcef-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6dcef-125">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="6dcef-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6dcef-126">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6dcef-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6dcef-127">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="6dcef-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="6dcef-128">ภาพรวมการกำหนดธีม</span><span class="sxs-lookup"><span data-stu-id="6dcef-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="6dcef-129">สร้างธีมใหม่</span><span class="sxs-lookup"><span data-stu-id="6dcef-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
