---
title: เพิ่มข้อความต้อนรับ
description: หัวข้อนี้อธิบายวิธีการเพิ่มข้อความต้อนรับให้กับเว็บไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697393"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="d33a2-103">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="d33a2-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d33a2-104">หัวข้อนี้อธิบายวิธีการเพิ่มข้อความต้อนรับให้กับเว็บไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d33a2-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="d33a2-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d33a2-105">Overview</span></span>

<span data-ttu-id="d33a2-106">ข้อความต้อนรับบนเว็บไซต์อีคอมเมิร์ซของคุณสามารถแจ้งผู้เยี่ยมชมเกี่ยวกับการขายต่อเนื่อง การอัพเดตของไซต์ หรือความพร้อมในการเรียกเก็บเงินตามฤดูกาล</span><span class="sxs-lookup"><span data-stu-id="d33a2-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="d33a2-107">ข้อความต้อนรับถูกตั้งค่าโดยใช้โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="d33a2-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="d33a2-108">ควรเพิ่มโมดูลการแจ้งเตือนลงในช่อง **ข้อความแสดงข้อผิดพลาด/ข้อมูล** ของส่วนที่เป็นส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="d33a2-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="d33a2-109">โมดูลการแจ้งเตือนช่วยให้คุณสามารถระบุข้อความที่จะแสดง สีของข้อความ และการจัดตำแหน่งได้</span><span class="sxs-lookup"><span data-stu-id="d33a2-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="d33a2-110">นอกจากนี้ยังช่วยให้คุณสามารถระบุได้ว่าผู้เยี่ยมชมไซต์สามารถยกเลิกข้อความได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d33a2-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="d33a2-111">เมื่อมีการเพิ่มข้อความต้อนรับไปยังส่วนที่เป็นส่วนหัวที่ใช้ร่วมกัน ระบบจะแสดงขึ้นบนทุกเพจ ซึ่งใช้แม่แบบที่มีการใช้ส่วนที่เป็นส่วนหัวที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="d33a2-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="d33a2-112">เมื่อต้องการเพิ่มข้อความต้อนรับให้กับไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d33a2-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="d33a2-113">ใน Dynamics 365 Commerce ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d33a2-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="d33a2-114">เลือก **ส่วน**</span><span class="sxs-lookup"><span data-stu-id="d33a2-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="d33a2-115">เลือกส่วนที่เป็นส่วนหัวเมื่อต้องการเพิ่มข้อความ</span><span class="sxs-lookup"><span data-stu-id="d33a2-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="d33a2-116">ในแผนภูมิเค้าร่าง ให้ขยาย **ข้อความแสดงข้อผิดพลาด/ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d33a2-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="d33a2-117">เลือกโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="d33a2-117">Select the alert module.</span></span>

    <span data-ttu-id="d33a2-118">ถ้ายังไม่มีโมดูลการแจ้งเตือนอยู่ ให้เลือกปุ่ม (**...**) ถัดจาก **ข้อความแสดงข้อผิดพลาด/ข้อมูล** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d33a2-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="d33a2-119">เลือกโมดูลการแจ้งเตือน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d33a2-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="d33a2-120">ในบานหน้าต่างคุณสมบัติทางด้านขวาบนแท็บ **ข้อมูล** ให้เลือก **เพิ่มแหล่งข้อมูล** แล้วเลือก **เนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="d33a2-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="d33a2-121">ในฟิลด์ **ข้อความป้อนเข้า** ให้ป้อนข้อความของข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="d33a2-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="d33a2-122">บันทึกส่วนที่เป็นส่วนหัว เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d33a2-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="d33a2-123">ขณะนี้ข้อความต้อนรับจะปรากฏขึ้นที่ด้านบนของหน้าไซต์ทั้งหมดที่ใช้ส่วนที่เป็นส่วนหัวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d33a2-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d33a2-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d33a2-124">Additional resources</span></span>

[<span data-ttu-id="d33a2-125">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="d33a2-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d33a2-126">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="d33a2-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d33a2-127">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="d33a2-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d33a2-128">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="d33a2-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d33a2-129">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d33a2-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d33a2-130">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="d33a2-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

