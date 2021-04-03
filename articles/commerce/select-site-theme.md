---
title: เลือกธีมของไซต์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3f7f38a0b4b1e0be85d619a1c133d1555706d93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254732"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="49f10-103">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="49f10-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49f10-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="49f10-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49f10-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="49f10-105">Overview</span></span>

<span data-ttu-id="49f10-106">โครงร่างและลักษณะของไซต์ (ตัวอย่างเช่น แบบอักษร ขนาด และสี) จะถูกกำหนดโดยชุดรูปแบบที่คุณเลือกและนำไปใช้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="49f10-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="49f10-107">ชุดรูปแบบจะถูกสร้างขึ้น และใช้งานโดยนักพัฒนาที่บริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="49f10-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="49f10-108">สำหรับภาพรวมของชุดรูปแบบโปรดดู [ภาพรวมของชุดรูปแบบ](e-commerce-extensibility/theming.md)</span><span class="sxs-lookup"><span data-stu-id="49f10-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="49f10-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและปรับใช้ชุดรูปแบบ โปรดดู [สร้างชุดรูปแบบใหม่](e-commerce-extensibility/create-theme.md)</span><span class="sxs-lookup"><span data-stu-id="49f10-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="49f10-110">โดยค่าเริ่มต้น เมื่อคุณสร้างไซต์เป็นครั้งแรกระบบจะใช้ชุดรูปแบบที่ชื่อ **Fabrikam**</span><span class="sxs-lookup"><span data-stu-id="49f10-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="49f10-111">ธีมเริ่มต้นนี้ให้ไว้เป็นส่วนหนึ่งของไลบรารีโมดูล Commerce</span><span class="sxs-lookup"><span data-stu-id="49f10-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="49f10-112">หลังจากที่คุณได้ปรับใช้ชุดรูปแบบเพิ่มเติมสำหรับไซต์ของคุณแล้ว คุณสามารถตั้งค่าคอนฟิกไซต์ดังกล่าวเพื่อให้ใช้งานได้อย่างใดอย่างหนึ่งแทน</span><span class="sxs-lookup"><span data-stu-id="49f10-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="49f10-113">เลือกชุดรูปแบบของไซต์</span><span class="sxs-lookup"><span data-stu-id="49f10-113">Select the site theme</span></span>

<span data-ttu-id="49f10-114">เมื่อต้องการเลือกชุดรูปแบบที่จะใช้กับไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49f10-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="49f10-115">ในสภาพแวดล้อมการสร้างและแก้ไขไซต์ ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="49f10-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="49f10-116">ไปที่ **การจัดการไซต์** \> **เพิ่มความสามารถ**</span><span class="sxs-lookup"><span data-stu-id="49f10-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="49f10-117">ภายใต้ **ชุดรูปแบบ** ให้เลือกชุดรูปแบบในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="49f10-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="49f10-118">เมื่อต้องการใช้ชุดรูปแบบที่เลือกกับไซต์ของคุณให้เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="49f10-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="49f10-119">ชุดรูปแบบที่คุณเลือกเผยแพร่ไปยังไซต์ของคุณ ทันทีที่คุณเลือก **บันทึกและเผยแพร่** บนหน้า **เพิ่มความสามารถ**</span><span class="sxs-lookup"><span data-stu-id="49f10-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="49f10-120">เมื่อต้องการแสดงตัวอย่างชุดรูปแบบบนไซต์ของคุณก่อนที่จะใช้งาน คุณสามารถใช้สภาพแวดล้อมการพัฒนาหรือ Sandbox ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="49f10-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49f10-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="49f10-121">Additional resources</span></span>

[<span data-ttu-id="49f10-122">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="49f10-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="49f10-123">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="49f10-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="49f10-124">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="49f10-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="49f10-125">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="49f10-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="49f10-126">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="49f10-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="49f10-127">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="49f10-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="49f10-128">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="49f10-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="49f10-129">ภาพรวมการกำหนดธีม</span><span class="sxs-lookup"><span data-stu-id="49f10-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="49f10-130">สร้างธีมใหม่</span><span class="sxs-lookup"><span data-stu-id="49f10-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]