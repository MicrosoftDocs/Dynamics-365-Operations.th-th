---
title: ฝังแอป PowerApps ใน Dynamics 365 - Core HR
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งรายการเมนู PowerApps หายไปจากโมดูลการดูแลระบบ
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551014"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="63a78-103">ฝังแอป PowerApps ใน Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="63a78-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="63a78-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="63a78-104">**Issue**</span></span>

<span data-ttu-id="63a78-105">รายการเมนู **PowerApps** หายไปจากโมดูล **การดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="63a78-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="63a78-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="63a78-106">**Cause**</span></span>

<span data-ttu-id="63a78-107">การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft PowerApps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="63a78-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="63a78-108">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="63a78-108">**Resolution**</span></span>

<span data-ttu-id="63a78-109">มีการเปลี่ยนแปลงวิธีการที่แอป PowerApps ถูกฝัง</span><span class="sxs-lookup"><span data-stu-id="63a78-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="63a78-110">PowerApps ขณะนี้ ถูกเพิ่มโดยใช้แบบจำลองการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="63a78-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="63a78-111">คุณสามารถเพิ่มแอป PowerApps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="63a78-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="63a78-112">สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป PowerApps ใน Talent ดู [ฝังแอป PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)</span><span class="sxs-lookup"><span data-stu-id="63a78-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="63a78-113">ลูกค้า PowerApps ที่ฝังแอปก่อนมีการเปลี่ยนแปลง ที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="63a78-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="63a78-114">ปุ่ม **PowerApps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent</span><span class="sxs-lookup"><span data-stu-id="63a78-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="63a78-115">คุณสามารถใช้ปุ่มนี้เพื่อแทรกแอป PowerApps ได้</span><span class="sxs-lookup"><span data-stu-id="63a78-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="63a78-116">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="63a78-116">Here is an example.</span></span>

1. <span data-ttu-id="63a78-117">ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**</span><span class="sxs-lookup"><span data-stu-id="63a78-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="63a78-118">เลือกปุ่ม **PowerApps** และจากนั้น เลือก **แทรก PowerApp**</span><span class="sxs-lookup"><span data-stu-id="63a78-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![ปุ่ม PowerApps](media/png.png)

3. <span data-ttu-id="63a78-120">กรอกข้อมูลฟิลด์ในกล่องโต้ตอบ **แทรก PowerApp**</span><span class="sxs-lookup"><span data-stu-id="63a78-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![แทรกกล่องโต้ตอบ PowerApp](media/insert-powerapp.png)

<span data-ttu-id="63a78-122">หรือทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="63a78-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="63a78-123">บนบานหน้าต่างการดำเนินการของหน้า บนแท็บ **ตัวเลือก** ในกลุ่ม **ตั้งค่าส่วนบุคคล** เลือก **ตั้งค่าแบบฟอร์มนี้ให้เป็นแบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="63a78-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    <span data-ttu-id="63a78-125">แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="63a78-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="63a78-126">บนแถบเครื่องมือ เลือก **แทรก \> PowerApp**</span><span class="sxs-lookup"><span data-stu-id="63a78-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![แทรกแอป PowerApps โดยใช้แถบเครื่องมือการตั้งค่าส่วนบุคคล](media/powerapp-bar.png)
