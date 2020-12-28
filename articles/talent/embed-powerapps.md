---
title: ฝังแอป Power Apps ใน Dynamics 365 Human Resources
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งรายการเมนู Microsoft Power Apps หายไปจากโมดูลการดูแลระบบ
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462668"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="ed070-103">ฝังแอป Power Apps ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="ed070-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="ed070-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ed070-104">**Issue**</span></span>

<span data-ttu-id="ed070-105">รายการเมนู **Power Apps** หายไปจากโมดูล **การดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="ed070-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="ed070-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="ed070-106">**Cause**</span></span>

<span data-ttu-id="ed070-107">การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft Power Apps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ed070-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="ed070-108">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="ed070-108">**Resolution**</span></span>

<span data-ttu-id="ed070-109">วิธีการที่ Power Apps ถูกฝังถูกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ed070-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="ed070-110">ขณะนี้ Power Apps ถูกเพิ่มโดยใช้แบบจำลองการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="ed070-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="ed070-111">คุณสามารถเพิ่ม Power Apps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="ed070-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="ed070-112">สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป Power Apps ใน Talent ดู [ฝัง Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)</span><span class="sxs-lookup"><span data-stu-id="ed070-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="ed070-113">ลูกค้า Power Apps ที่ฝังแอปก่อนมีการเปลี่ยนแปลง ที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="ed070-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="ed070-114">ปุ่ม **Power Apps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent</span><span class="sxs-lookup"><span data-stu-id="ed070-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="ed070-115">คุณสามารถใช้ปุ่มนี้ในการแทรกแอป</span><span class="sxs-lookup"><span data-stu-id="ed070-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="ed070-116">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ed070-116">Here is an example.</span></span>

1. <span data-ttu-id="ed070-117">ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**</span><span class="sxs-lookup"><span data-stu-id="ed070-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="ed070-118">เลือกปุ่ม **Power Apps** แล้วเลือก **เพิ่มแอปจาก Power Apps**</span><span class="sxs-lookup"><span data-stu-id="ed070-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![ปุ่ม Power Apps](media/png.png)

3. <span data-ttu-id="ed070-120">กรอกข้อมูลในฟิลด์ในกล่องโต้ตอบ **เพิ่มแอปจาก Power Apps**</span><span class="sxs-lookup"><span data-stu-id="ed070-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![เพิ่มแอปจากกล่องโต้ตอบ Power Apps ](media/insert-powerapp.png)

<span data-ttu-id="ed070-122">หรือทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ed070-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="ed070-123">ที่บานหน้าต่างการดำเนินการของเพจ บนแท็บ **ตัวเลือก** ในกลุ่ม **ปรับให้เป็นแบบส่วนตัว** เลือก **ปรับหน้านี้ให้เป็นแบบส่วนตัว**</span><span class="sxs-lookup"><span data-stu-id="ed070-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    <span data-ttu-id="ed070-125">แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ed070-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="ed070-126">บนแถบเครื่องมือ เลือก **เพิ่มแอปจาก Power Apps**</span><span class="sxs-lookup"><span data-stu-id="ed070-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![เพิ่มแอปจาก Power Apps โดยใช้แถบเครื่องมือแบบรายบุคคล](media/powerapp-bar.png)
