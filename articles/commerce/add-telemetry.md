---
title: เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล
description: หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001288"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="643d9-103">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="643d9-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="643d9-104">หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="643d9-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="643d9-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="643d9-105">Overview</span></span>

<span data-ttu-id="643d9-106">Web analytics เป็นเครื่องมือที่จำเป็น เมื่อคุณต้องการทำความเข้าใจวิธีการที่ลูกค้าของคุณโต้ตอบกับไซต์ของคุณ และตัดสินใจที่จะช่วยปรับปรุงประสบการณ์สำหรับการแปลงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="643d9-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="643d9-107">แพคเกจการวิเคราะห์เว็บจำนวนมากพร้อมให้ความช่วยเหลือในการบรรลุเป้าหมายเหล่านี้ เช่น Google Analytics, Clicky, Moz Analytics และ KISSMetrics</span><span class="sxs-lookup"><span data-stu-id="643d9-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="643d9-108">แพคเกจการวิเคราะห์เว็บส่วนใหญ่กำหนดให้คุณต้องเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ในองค์ประกอบที่เป็น **\<หัวข้อ\>** ของ HTML สำหรับทุกเพจของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="643d9-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="643d9-109">คำแนะนำในหัวข้อนี้จะใช้กับฟังก์ชันฝั่งไคลเอนต์แบบกำหนดเองอื่นๆ ที่ Microsoft Dynamics 365 Commerce ไม่มีข้อเสนอโดยไม่ได้กล่าวถึง</span><span class="sxs-lookup"><span data-stu-id="643d9-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="643d9-110">สร้างส่วนที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="643d9-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="643d9-111">หลังจากที่คุณสร้างส่วนสำหรับรหัสสคริปต์ของคุณแล้ว คุณสามารถนำมาใช้ใหม่ผ่านเพจทั้งหมดบนไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="643d9-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="643d9-112">ไปที่ **ส่วน \>ส่วนของเพจใหม่**</span><span class="sxs-lookup"><span data-stu-id="643d9-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="643d9-113">เลือก **สคริปต์ภายนอก** ป้อนชื่อสำหรับส่วน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="643d9-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="643d9-114">ในลำดับชั้นของส่วน ให้เลือกโมดูลรอง **ตัวส่งสคริปต์** ของส่วนที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="643d9-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="643d9-115">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เพิ่มสคริปต์ฝั่งไคลเอนต์ และตั้งค่าตัวเลือกการตั้งค่าคอนฟิกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="643d9-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="643d9-116">เพิ่มส่วนให้กับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="643d9-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="643d9-117">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="643d9-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="643d9-118">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="643d9-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="643d9-119">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่อง **ส่วนหัวของ HTML** แล้วเลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="643d9-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="643d9-120">เลือกส่วนที่คุณสร้างสำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="643d9-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="643d9-121">บันทึกแม่แบบ และเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="643d9-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="643d9-122">หลังจากที่คุณดำเนินการเสร็จสิ้นแล้ว คุณต้องเผยแพร่ส่วนและแม่แบบหลัก</span><span class="sxs-lookup"><span data-stu-id="643d9-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="643d9-123">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="643d9-123">Additional resources</span></span>

[<span data-ttu-id="643d9-124">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="643d9-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="643d9-125">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="643d9-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="643d9-126">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="643d9-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="643d9-127">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="643d9-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="643d9-128">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="643d9-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="643d9-129">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="643d9-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="643d9-130">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="643d9-130">Add languages to your site</span></span>](add-languages-to-site.md)

