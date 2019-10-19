---
title: ใบสั่งงานและสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายใบสั่งงาน เเละสินทรัพย์ถาวรในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250841"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="b2a89-103">ใบสั่งงานและสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b2a89-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="b2a89-104">ในการจัดการสินทรัพย์ สินทรัพย์สามารถเกี่ยวข้องกับสินทรัพย์ถาวร เเละคุณสามารถสร้างใบสั่งงานสำหรับสินทรัพย์เหล่านั่นได้</span><span class="sxs-lookup"><span data-stu-id="b2a89-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="b2a89-105">ถ้าคุณใช้ฟังก์ชันนี้ คุณจะได้รับภาพรวมของสินทรัพย์ถาวร โครงการลงทุนที่เกี่ยวข้อง และต้นทุนที่ลงทะเบียนบนโครงการลงทุนโมดูลในโมดูล **การจัดการโครงการ เเละการบัญชี** เเละโมดูล **สินทรัพย์ถาวร** </span><span class="sxs-lookup"><span data-stu-id="b2a89-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="b2a89-106">ฟิลด์ **หมายเลขสินทรัพย์ถาวร** คือการกรอกข้อมูลอย่างเดียวบนโครงการงานใบสั่งงาน ถ้าชนิด "การลงทุน" ถูกเลือกเป็นชนิดโครงการบนโครงการงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="b2a89-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![รูปที่ 1](media/24-work-orders.png)

<span data-ttu-id="b2a89-108">กระบวนงานต่อไปนี้จะอธิบายความสัมพันธ์ระหว่างสินทรัพย์ ใบสั่งงาน โครงการงานใบสั่งงาน และสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b2a89-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="b2a89-109">คุณสร้างสินทรัพย์ที่คุณสัมพันธ์กับสินทรัพย์ถาวร ดังที่แสดงในรูปด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="b2a89-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![รูปที่ 2](media/25-work-orders.png)

2. <span data-ttu-id="b2a89-111">เมื่อคุณตั้งค่าชนิดของใบสั่งงาน (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **ชนิดใบสั่งงาน**) คุณสร้างชนิดใบสั่งงานสำหรับการจัดการการลงทุน</span><span class="sxs-lookup"><span data-stu-id="b2a89-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="b2a89-112">ดูเพิ่มเติมที่ [ชนิดใบสั่งงาน](../setup-for-work-orders/work-order-types.md)</span><span class="sxs-lookup"><span data-stu-id="b2a89-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![รูปที่ 3](media/26-work-orders.png)

3. <span data-ttu-id="b2a89-114">เมื่อคุณตั้งค่ากลุ่มโครงการของใบสั่งงาน (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ** > **กลุ่มโครงการ**ลิงค์) คุณสร้างความสัมพันธ์ระหว่างชนิดของใบสั่งงานที่ใช้สำหรับการลงทุน และกลุ่มโครงการสร้างสำหรับการลงทุนในโมดูล **การจัดการโครงการ เเละการบัญชี** (**การจัดการโครงการ เเละการบัญชี** > **การตั้งค่า** > **การลงรายการบัญชี** > **กลุ่มโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="b2a89-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![รูปที่ 4](media/27-work-orders.png)

4. <span data-ttu-id="b2a89-116">เมื่อคุณสร้างใบสั่งงานที่เกี่ยวข้องกับออบเจ็กต์สินทรัพย์ถาวร คุณเลือกชนิดของใบสั่งงานที่ใช้สำหรับการจัดการการลงทุน ตัวอย่างเช่น "การลงทุน"</span><span class="sxs-lookup"><span data-stu-id="b2a89-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="b2a89-117">เมื่อสร้างใบสั่งงานถูกสร้าง ใบสั่งงานที่เกี่ยวข้องจะเเสดงขึ้นใน **ใบสั่งงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b2a89-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![รูปที่ 5](media/28-work-orders.png)

6. <span data-ttu-id="b2a89-119">เมื่อสร้างใบสั่งงานถูกสร้าง โครงการที่เกี่ยวข้องกับใบสั่งงานจะถูกสร้างขึ้นใน **การจัดการโครงการ เเละการบัญชี** > **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b2a89-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="b2a89-120">คุณสามารถดูข้อมูลที่เกี่ยวข้องกับโครงการโดยการคลิกที่ลิงค์ **รหัสโครงการ** บนใบสั่งงาน (ใน **การจัดการสินทรัพย์** เปิดใบสั่งงานในมุมมองรายละเอียด > เเท็บด่วน **รายละเอียดของรายการ** แท็บ > **ทั่วไป** ฟิลด์ > **รหัสโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="b2a89-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![รูปที่ 6](media/29-work-orders.png)

7. <span data-ttu-id="b2a89-122">ใน **สินทรัพย์ถาวร** คุณสามารถดูภาพรวมของโครงการที่เชื่อมโยงกับสินทรัพย์ถาวร (**สินทรัพย์ถาวร** > **สินทรัพย์ถาวร** > **สินทรัพย์ถาวร** > คลิกที่สินทรัพย์ถาวรในฟิลด์ **หมายเลขสินทรัพย์ถาวร** > ดูเนื้อหาในบานหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** ส่วน > **โครงการที่เชื่อมโยง**)</span><span class="sxs-lookup"><span data-stu-id="b2a89-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

