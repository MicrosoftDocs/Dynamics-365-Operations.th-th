---
title: ฝังแอป Power Apps ใน Dynamics 365 - Core HR
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898723"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="f4f98-103">ฝังแอป Power Apps ใน Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="f4f98-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="f4f98-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f4f98-104">**Issue**</span></span>

<span data-ttu-id="f4f98-105">รายการเมนู **Power Apps** หายไปจากโมดูล **การดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="f4f98-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="f4f98-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="f4f98-106">**Cause**</span></span>

<span data-ttu-id="f4f98-107">การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft Power Apps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f4f98-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="f4f98-108">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="f4f98-108">**Resolution**</span></span>

<span data-ttu-id="f4f98-109">วิธีการที่ Power Apps ถูกฝังถูกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="f4f98-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="f4f98-110">ขณะนี้ Power Apps ถูกเพิ่มโดยใช้แบบจำลองการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="f4f98-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="f4f98-111">คุณสามารถเพิ่ม Power Apps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="f4f98-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="f4f98-112">สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป Power Apps ใน Talent ดู [ฝัง Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)</span><span class="sxs-lookup"><span data-stu-id="f4f98-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="f4f98-113">ลูกค้า Power Apps ที่ฝังแอปก่อนมีการเปลี่ยนแปลง ที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="f4f98-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="f4f98-114">ปุ่ม **Power Apps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent</span><span class="sxs-lookup"><span data-stu-id="f4f98-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="f4f98-115">คุณสามารถใช้ปุ่มนี้เพื่อแทรก Power Apps ได้</span><span class="sxs-lookup"><span data-stu-id="f4f98-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="f4f98-116">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f4f98-116">Here is an example.</span></span>

1. <span data-ttu-id="f4f98-117">ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**</span><span class="sxs-lookup"><span data-stu-id="f4f98-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="f4f98-118">เลือกปุ่ม **Power Apps** และจากนั้น เลือก **แทรก PowerApp**</span><span class="sxs-lookup"><span data-stu-id="f4f98-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![ปุ่ม Power Apps](media/png.png)

3. <span data-ttu-id="f4f98-120">กรอกข้อมูลฟิลด์ในกล่องโต้ตอบ **แทรก PowerApp**</span><span class="sxs-lookup"><span data-stu-id="f4f98-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![แทรกกล่องโต้ตอบ PowerApp](media/insert-powerapp.png)

<span data-ttu-id="f4f98-122">หรือทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f4f98-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="f4f98-123">บนบานหน้าต่างการดำเนินการของหน้า บนแท็บ **ตัวเลือก** ในกลุ่ม **ตั้งค่าส่วนบุคคล** เลือก **ตั้งค่าแบบฟอร์มนี้ให้เป็นแบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="f4f98-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    <span data-ttu-id="f4f98-125">แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="f4f98-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="f4f98-126">บนแถบเครื่องมือ เลือก **แทรก \> PowerApp**</span><span class="sxs-lookup"><span data-stu-id="f4f98-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![แทรกแอป Power Apps โดยใช้แถบเครื่องมือการตั้งค่าส่วนบุคคล](media/powerapp-bar.png)
