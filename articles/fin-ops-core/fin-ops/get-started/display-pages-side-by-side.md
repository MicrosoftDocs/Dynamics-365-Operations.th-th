---
title: แสดงหน้าแบบเคียงข้างกันโดยใช้คุณสมบัติเปิดในหน้าต่างใหม่
description: บทความนี้จะอธิบายวิธีการแสดงหน้าแบบเคียงข้างกัน
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b770fe44e4e12c515ca53def697fa345ce3eba3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694456"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a><span data-ttu-id="7b469-103">แสดงหน้าแบบเคียงข้างกันโดยใช้คุณสมบัติเปิดในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="7b469-103">Show pages side-by-side using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b469-104">บทความนี้จะอธิบายวิธีการแสดงหน้าแบบเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="7b469-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="7b469-105">คุณอาจต้องการดูหลายหน้าแบบเคียงข้างกันเพื่อทำงานให้เสร็จสมบูรณ์ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="7b469-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="7b469-106">ตัวอย่าง คุณอาจต้องการตรวจสอบ หรือป้อนบรรทัดในสมุดรายวันมากกว่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b469-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="7b469-107">โดยทั่วไป การตรวจสอบความถูกต้องหรือป้อนรายการในสมุดรายวันมากกว่าหนึ่ง คุณจะต้องกลับไปกลับมาระหว่างหน้าที่แสดงรายการของสมุดรายวัน และหน้าซึ่งแสดงรายการสำหรับสมุดรายวันที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="7b469-107">Typically, to validate or enter lines in more than one journal, you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="7b469-108">อย่างไรก็ตาม คุณลักษณะ **การเปิดในหน้าต่างใหม่** ช่วยให้คุณสามารถแสดงเหล่านี้แบบเคียงข้างกันเพื่อให้คุณสามารถทำงานของคุณได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="7b469-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="7b469-109">โดยอาศัยตัวอย่างที่กล่าวถึงด้านบน เมื่อดูบรรทัด คุณสามารถคลิกไอคอน **เปิดในหน้าต่างใหม่**</span><span class="sxs-lookup"><span data-stu-id="7b469-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="7b469-110">[![คลิกเปิดในไอคอนหน้าต่างใหม่](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="7b469-110">[![Click the Open in new window icon.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="7b469-111">เมื่อคลิกไอคอน **เปิดในหน้าต่างใหม่** ระบบจะเปิดหน้ารายการในเบราเซอร์ป๊อปอัพใหม่ และจากนั้น นำทางเบราเซอร์เดิมกลับในประวัติไปที่หน้าที่แสดงรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7b469-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="7b469-112">จากนั้นคุณสามารถแสดงทั้งสองหน้า--เคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="7b469-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="7b469-113">เมื่อคุณเสร็จสิ้น การดูสมุดรายวัน คุณสามารถเปลี่ยนแปลงสมุดรายวันที่เลือกบนหน้ารายการสมุดรายวัน และหน้ารายการในหน้าต่างป็อปอัพจะแสดงบรรทัดสมุดรายวันที่เลือกใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7b469-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="7b469-114">[![คุณสามารถแสดงเคียงข้างกัน](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="7b469-114">[![You can display pages side-by-side.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="7b469-115">การเชื่อมโยงแบบไดนามิกและรีเฟรชที่เกิดขึ้นเนื่องจากความสัมพันธ์ที่มีอยู่ระหว่างข้อมูลที่ไม่สนับสนุนหน้าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7b469-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="7b469-116">ถ้าระบบไม่ทราบถึงความสัมพันธ์ระหว่างข้อมูล หน้าต่างป็อปอัพจะไม่รีเฟรชโดยอัตโนมัติในการเปลี่ยนแปลงในหน้าต่างที่มาจากการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="7b469-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="7b469-117">บางเพจมีมุมมองต่าง ๆ เช่นมุมมองกริด มุมมองหัวข้อ และดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="7b469-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="7b469-118">ไอคอน **เปิดในหน้าต่างใหม่** ทำให้ทั้งหน้าเปิดในหน้าต่างเบราเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7b469-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="7b469-119">ดังนั้น คุณจึงไม่สามารถเก็บสองมุมมองที่หน้าเดียวกันแบบเคียงข้างกันโดยใช้ลักษณะการทำงาน **การเปิดในหน้าต่างใหม่**</span><span class="sxs-lookup"><span data-stu-id="7b469-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="7b469-120">อย่างไรก็ตาม หน้าดังกล่าวเกือบทั้งหมดมีการนำรายการที่คุณสามารถใช้เพื่อสลับไปมาระหว่างเรกคอร์ด และบรรลุประสบการณ์คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="7b469-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="7b469-121">ก่อนที่จะใช้ในคุณลักษณะ **เปิดในหน้าต่างใหม่** คุณควรตั้งค่าคอนฟิกตัวบล็อกป๊อปอัพเบราเซอร์ของคุณเพื่ออนุญาตป็อปอัพจาก URL ของไซต์</span><span class="sxs-lookup"><span data-stu-id="7b469-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="7b469-122">ตัวอย่างเช่น คุณไม่สามารถอนุญาตป็อปอัพจาก "\*.dynamics.com"</span><span class="sxs-lookup"><span data-stu-id="7b469-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="7b469-123">คุณลักษณะ **การเปิดในหน้าต่างใหม่** จะพร้อมใช้งานเฉพาะเมื่อมีมากกว่าหนึ่งหน้าเปิดในหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="7b469-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="7b469-124">หน้าต่างป๊อปอัพยังปิดโดยอัตโนมัติเมื่อไม่มีจำนวนหน้าเปิดอีกต่อไป (นั่นคือ เมื่อปิดหน้าสุดท้ายในหน้าต่างนั้น)</span><span class="sxs-lookup"><span data-stu-id="7b469-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="7b469-125">ระบบยังสามารถปิดหน้าเปิดเมื่อคุณนำทางไปยังพื้นที่อื่นในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7b469-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="7b469-126">ดังนั้น ถ้าคุณได้ป๊อปอัพเปิด และนำทางไปยังพื้นที่อื่นในแอพลิเคชัน ป๊อปอัพจะปิดโดยอัตโนมัติปิดเนื่องจากหน้าในหน้าต่างเหล่านั้นได้ถูกปิด โดยระบบ</span><span class="sxs-lookup"><span data-stu-id="7b469-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="7b469-127">แถบด้านบนในป๊อปอัพแสดงข้อมูลเกี่ยวกับหน้าของบริษัทที่เปิด และเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="7b469-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="7b469-128">นอกจากนี้วินโดว์ป๊อปอัพขึ้นอยู่กับหน้าต่างเบราเซอร์หลัก</span><span class="sxs-lookup"><span data-stu-id="7b469-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="7b469-129">ถ้าหน้าต่างหลักถูกปิด หรือรีเฟรช ป๊อปอัพเปิดอยู่ทั้งหมดจะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="7b469-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="7b469-130">หากสถานการณ์นี้เกิดขึ้น คุณยังคงสามารถดูข้อมูลในหน้าต่างเหล่านี้ แต่คุณจะไม่สามารถโต้ตอบกลับได้</span><span class="sxs-lookup"><span data-stu-id="7b469-130">If this situation occurs, you can still view the information in these windows, but you will not be able to interact with it.</span></span>
